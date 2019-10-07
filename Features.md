REDGPU is here with an explicit goal to beat other GPU APIs with the most intuitive API in the world that is easy to use, debug and profile.

REDGPU SDK and latest SDK and drivers from PC GPU vendors is everything you need to start writing robust and predictable GPU software.

REDGPU API features:

* Standard C99 API. Fully procedural, not object-oriented. No macros, no obscure code practices. Clean, well structured and readable code.

* Manual memory management on CPU and GPU. No variable-length arrays, no heap memory is allocated or freed behind your back, with an exception of context initialization call that takes your custom malloc and free function pointers which are not used anywhere except for context initialization.

* Ecto gammat: nothing will happen without your command. No shader will be recompiled, no synchronization will be issued, no GPU memory will be allocated without you explicitly asking for it.

* No dependencies on other third-party headers and libraries. API headers include only stddef.h.

* No dependencies on C or C++ standard libraries. No dependencies on any dynamic or shared libraries, with an exception of vulkan-1.dll on Windows.

* Complete, self-contained SDK. Easy to setup and get started for programmers, easy to distribute runtime components to end users.

* Fully robust. All internal runtime errors are always propagated and returned for your program to handle.

* Completely thread safe. No other GPU abstraction can guarantee thread safety REDGPU API guarantees. No mutexes or locks are used inside the API.

* No global variables or thread-local storage is used inside the API. Everything is passed explicitly with handles and pointers to structs as procedure parameters.

* Explicit CPU and GPU synchronization. Nothing is synchronized for you, all explicit synchronization primitives are exposed to program.

* Easy multi-GPU support. All available GPUs are returned as handles you can pass to all procedures just as you would pass a single GPU handle.

* Support for operating systems: Windows 10, Ubuntu 18.04 and higher.

* Offline GPU code compilation to an industry standard, portable IR with DXC compiler (HLSL) on both Windows 10 and Ubuntu 18.04 operating systems.

* First class support for Team Green GPU vendor's debugger and timeline profiler on both Windows 10 and Ubuntu 18.04 operating systems.

* DRM-free, license-key-free, a single perpetual license per company for unlimited number of employees and projects.

* 5 hours a day, 5 days a week, 5-month live chat and code support.

For any questions, email: iamvfx@gmail.com

For updates, see: https://github.com/redgpu/redgpu

For news, follow: https://twitter.com/redgpus

For more, read: https://medium.com/@redgpu
