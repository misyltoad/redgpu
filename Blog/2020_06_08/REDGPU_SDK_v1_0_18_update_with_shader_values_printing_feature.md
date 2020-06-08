REDGPU SDK version 1.0.18 is here with a new exciting feature that makes shader debugging a lot easier: now you can print any values from any of the executing shaders!

Just include the new `redgpu_debug.h` file and link against `libredgpu_debug.so` or `redgpu_debug.dll` library, set the `RedContextOptionalSettingsDebugArray::debugArrayStructsCount` and `RedContextOptionalSettingsDebugArray::debugArrayStructsFloat4sCount` parameters and pass them to context's optional settings, get the debug array handle with `redDebugArrayGetHandle()` and pass it to GPU procedures with shaders you want to investigate, in HLSL write the values you need to the debug array, call `redDebugArrayCallPrint()` in GPU calls and see the shader values printed in your terminal window in real time!

You can also do whatever you want with the returned shader values by setting your own print callback to `RedContextOptionalSettingsDebugArray::printCallback` parameter.

This feature is very robust and guaranteed to work reliably every time, but it highly depends on operating system's and GPU driver's capabilities. Currenlty, it works on Linux and NVIDIA GPUs, but for other combinations of operating systems, GPUs and GPU drivers it may fail to initialize properly on the first print call. So you've been warned! With great power comes great responsibility!

If you'll need any help, send me an email to [iamvfx@gmail.com](mailto:iamvfx@gmail.com) or DM me on twitter: [https://twitter.com/redgpus](https://twitter.com/redgpus)

Happy shader programming!
