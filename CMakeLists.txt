Set(LuaJIT_Source)


Get_Filename_Component(ParentDirectory ${CMAKE_CURRENT_SOURCE_DIR} DIRECTORY)
Add_Subdirectory(dynasm)
Add_Subdirectory(src)
Include_Directories(${ParentDirectory} ${CMAKE_CURRENT_SOURCE_DIR})



SET ( DEPS
  ${LJ_VM_SRC}
  ${CMAKE_CURRENT_BINARY_DIR}/lj_ffdef.h
  ${CMAKE_CURRENT_BINARY_DIR}/lj_bcdef.h
  ${CMAKE_CURRENT_BINARY_DIR}/lj_libdef.h
  ${CMAKE_CURRENT_BINARY_DIR}/lj_recdef.h
  ${CMAKE_CURRENT_BINARY_DIR}/lj_folddef.h
)

Add_Library(LuaJIT ${LuaJIT_Source})
Target_Compile_Definitions(LuaJIT PUBLIC "_CRT_SECURE_NO_WARNINGS")

If (${WIN32} AND CMAKE_SIZEOF_VOID_P EQUAL 4)
    target_include_directories(LuaJIT PRIVATE src)
    target_include_directories(LuaJIT PRIVATE src/platform/Win32)
    target_include_directories(LuaJIT PRIVATE src/platform/Win32/host)
    target_link_libraries(LuaJIT ${CMAKE_CURRENT_SOURCE_DIR}src/platform/Win32/Object/lj_vm)
ElseIf(${WIN32} AND CMAKE_SIZEOF_VOID_P EQUAL 8)
    target_include_directories(LuaJIT PRIVATE src)
    target_include_directories(LuaJIT PRIVATE src/platform/Win64)
    target_include_directories(LuaJIT PRIVATE src/platform/Win64/host)
    target_link_libraries(LuaJIT ${CMAKE_CURRENT_SOURCE_DIR}/src/platform/Win64/Object/lj_vm)
EndIf()