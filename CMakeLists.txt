Add_Library(LuaJIT "")

get_filename_component(ParentDirectory ${CMAKE_CURRENT_SOURCE_DIR} DIRECTORY)
include(dynasm/CMakeLists.txt)
include(src/CMakeLists.txt)

target_include_directories(LuaJIT PUBLIC ${ParentDirectory} ${CMAKE_CURRENT_SOURCE_DIR})
target_compile_definitions(LuaJIT PUBLIC _CRT_SECURE_NO_WARNINGS)

target_include_directories(LuaJIT PRIVATE src)

if (${WIN32} AND CMAKE_SIZEOF_VOID_P EQUAL 4)
    set(platformPath Win32)
elseif(${WIN32} AND CMAKE_SIZEOF_VOID_P EQUAL 8)
    set(platformPath Win64)
endif()

target_include_directories(LuaJIT PRIVATE src/platform/${platformPath})
target_include_directories(LuaJIT PRIVATE src/platform/${platformPath}/host)

get_filename_component(pathToLuaJITLib 
                            src/platform/${platformPath}/Object/lj_vm.lib 
                        ABSOLUTE 
                        BASE_DIR 
                            ${CMAKE_CURRENT_SOURCE_DIR})

target_link_libraries(LuaJIT ${pathToLuaJITLib})
