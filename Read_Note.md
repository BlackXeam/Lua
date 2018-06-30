# Lua
Efficient method
--《Lua Programming Gems》
--高性能之--Local

--[[
  --------------------------------------
  Lua 5.0 后采用类似寄存器的虚拟机模式。
  Lua的寄存器储存在栈中，每个活动函数Lua都会分配一个栈，用于储存该函数里的活动记录。
  这个栈是用8 bit表示的，所以可以储存至多250个寄存器。
  因此，Lua预编译器能把所有的local变量储存在其中，当要获取local变量时，可以使效率提高
  ---------------------------------------
  for i=1,1000000 do 
    local x = sin(i)
  end
  --------------------------
  local sin = math.sin
  for i=1,1000000 do
    local x = sin(i)
  end
  
]]--
