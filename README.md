# godot_modbus

My goal is to use the modbus library c++ https://github.com/fanzhe98/modbuspp as a godot module. But I can't figure where the Error "no matching function modbus::modbus()" comes from as I only call it like that modbus(host,  port); 

## Error :

<!-- language: lang-none -->
<pre><code>

scons: Building targets ...
[ 36%] Compiling ==> modules/summator/register_types.cpp
[ 36%] Compiling ==> modules/summator/summator.cpp
[ 43%] modules/summator/summator.cpp: In constructor 'Summator::Summator()':
modules/summator/summator.cpp:71:20: error: no matching function for call to 'modbus::modbus()'
   71 | Summator::Summator() {
      |                    ^
In file included from modules/summator/summator.h:12,
                 from modules/summator/summator.cpp:3:
modules/summator/modbus.h:72:5: note: candidate: 'modbus::modbus(std::string)'
   72 |     modbus(string host);
      |     ^~~~~~
modules/summator/modbus.h:72:5: note:   candidate expects 1 argument, 0 provided
modules/summator/modbus.h:71:5: note: candidate: 'modbus::modbus(std::string, uint16_t)'
   71 |     modbus(string host, uint16_t port);
      |     ^~~~~~
modules/summator/modbus.h:71:5: note:   candidate expects 2 arguments, 0 provided
modules/summator/modbus.h:49:7: note: candidate: 'modbus::modbus(const modbus&)'
   49 | class modbus {
      |       ^~~~~~
modules/summator/modbus.h:49:7: note:   candidate expects 1 argument, 0 provided
[ 99%] progress_finish(["progress_finish"], [])
[100%] scons: *** [modules/summator/summator.x11.opt.tools.64.o] Error 1
scons: building terminated because of errors.
</code></pre>.
