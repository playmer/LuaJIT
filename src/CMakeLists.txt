target_sources(LuaJIT
  PRIVATE
    ${CMAKE_CURRENT_LIST_DIR}/lib_aux.c
    ${CMAKE_CURRENT_LIST_DIR}/lib_base.c
    ${CMAKE_CURRENT_LIST_DIR}/lib_bit.c
    ${CMAKE_CURRENT_LIST_DIR}/lib_debug.c
    ${CMAKE_CURRENT_LIST_DIR}/lib_ffi.c
    ${CMAKE_CURRENT_LIST_DIR}/lib_init.c
    ${CMAKE_CURRENT_LIST_DIR}/lib_io.c
    ${CMAKE_CURRENT_LIST_DIR}/lib_jit.c
    ${CMAKE_CURRENT_LIST_DIR}/lib_math.c
    ${CMAKE_CURRENT_LIST_DIR}/lib_os.c
    ${CMAKE_CURRENT_LIST_DIR}/lib_package.c
    ${CMAKE_CURRENT_LIST_DIR}/lib_string.c
    ${CMAKE_CURRENT_LIST_DIR}/lib_table.c
#    ${CMAKE_CURRENT_LIST_DIR}/ljamalg.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_alloc.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_api.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_asm.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_bc.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_bcread.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_bcwrite.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_carith.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_ccall.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_ccallback.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_cconv.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_cdata.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_char.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_clib.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_cparse.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_crecord.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_ctype.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_debug.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_dispatch.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_err.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_ffrecord.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_func.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_gc.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_gdbjit.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_ir.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_lex.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_lib.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_load.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_mcode.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_meta.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_obj.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_opt_dce.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_opt_fold.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_opt_loop.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_opt_mem.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_opt_narrow.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_opt_sink.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_opt_split.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_parse.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_record.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_snap.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_state.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_str.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_strscan.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_tab.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_trace.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_udata.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_vmevent.c
    ${CMAKE_CURRENT_LIST_DIR}/lj_vmmath.c
    ${CMAKE_CURRENT_LIST_DIR}/luajit.c
#    ${CMAKE_CURRENT_LIST_DIR}/host/buildvm.c
#    ${CMAKE_CURRENT_LIST_DIR}/host/buildvm_asm.c
#    ${CMAKE_CURRENT_LIST_DIR}/host/buildvm_fold.c
#    ${CMAKE_CURRENT_LIST_DIR}/host/buildvm_lib.c
#    ${CMAKE_CURRENT_LIST_DIR}/host/buildvm_peobj.c
#    ${CMAKE_CURRENT_LIST_DIR}/host/minilua.c
#  PUBLIC
    ${CMAKE_CURRENT_LIST_DIR}/lauxlib.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_alloc.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_arch.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_asm.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_asm_arm.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_asm_mips.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_asm_ppc.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_asm_x86.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_bc.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_bcdump.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_carith.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_ccall.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_ccallback.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_cconv.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_cdata.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_char.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_clib.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_cparse.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_crecord.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_ctype.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_debug.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_def.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_dispatch.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_emit_arm.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_emit_mips.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_emit_ppc.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_emit_x86.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_err.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_errmsg.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_ff.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_ffrecord.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_frame.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_func.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_gc.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_gdbjit.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_ir.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_ircall.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_iropt.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_jit.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_lex.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_lib.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_mcode.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_meta.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_obj.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_parse.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_record.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_snap.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_state.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_str.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_strscan.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_tab.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_target.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_target_arm.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_target_mips.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_target_ppc.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_target_x86.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_trace.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_traceerr.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_udata.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_vm.h
    ${CMAKE_CURRENT_LIST_DIR}/lj_vmevent.h
    ${CMAKE_CURRENT_LIST_DIR}/lua.h
    ${CMAKE_CURRENT_LIST_DIR}/lua.hpp
    ${CMAKE_CURRENT_LIST_DIR}/luaconf.h
    ${CMAKE_CURRENT_LIST_DIR}/luajit.h
    ${CMAKE_CURRENT_LIST_DIR}/lualib.h
#    ${CMAKE_CURRENT_LIST_DIR}/host/buildvm.h
    ${CMAKE_CURRENT_LIST_DIR}/platform/Win32/lj_bcdef.h
    ${CMAKE_CURRENT_LIST_DIR}/platform/Win32/lj_ffdef.h
    ${CMAKE_CURRENT_LIST_DIR}/platform/Win32/lj_folddef.h
    ${CMAKE_CURRENT_LIST_DIR}/platform/Win32/lj_libdef.h
    ${CMAKE_CURRENT_LIST_DIR}/platform/Win32/lj_recdef.h
    ${CMAKE_CURRENT_LIST_DIR}/platform/Win64/lj_bcdef.h
    ${CMAKE_CURRENT_LIST_DIR}/platform/Win64/lj_ffdef.h
    ${CMAKE_CURRENT_LIST_DIR}/platform/Win64/lj_folddef.h
    ${CMAKE_CURRENT_LIST_DIR}/platform/Win64/lj_libdef.h
    ${CMAKE_CURRENT_LIST_DIR}/platform/Win64/lj_recdef.h
)
