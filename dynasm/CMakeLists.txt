target_sources(LuaJIT
  PRIVATE
#  PUBLIC
    ${CMAKE_CURRENT_LIST_DIR}/dasm_arm.h
    ${CMAKE_CURRENT_LIST_DIR}/dasm_mips.h
    ${CMAKE_CURRENT_LIST_DIR}/dasm_ppc.h
    ${CMAKE_CURRENT_LIST_DIR}/dasm_proto.h
    ${CMAKE_CURRENT_LIST_DIR}/dasm_x86.h
)
