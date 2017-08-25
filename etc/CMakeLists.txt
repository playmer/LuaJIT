Set(Previous_LuaJIT_Source ${LuaJIT_Source})

AddFile(LuaJIT_Source Previous_LuaJIT_Source luajit.1)
AddFile(LuaJIT_Source Previous_LuaJIT_Source luajit.pc)

Set(LuaJIT_Source ${Previous_LuaJIT_Source} PARENT_SCOPE)
