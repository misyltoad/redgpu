I have recently updated REDGPU SDK to version 1.0.4. If you have any questions, as always, you can reach me via email: iamvfx@gmail.com or twitter: https://twitter.com/redgpus

v1.0.4 changes include:

  * The texture and sponza examples now come with precompiled executables for Ubuntu 18.04. On Windows, any Visual Studio version since 2012 should build and run the examples out of the box, given that REDGPU and GPU vendor SDKs are installed as shown in RedGpuSDK/docs/2019_09_07/RedGpuSDKInstallationGuides

  * Since v1.0.0, 4 extensions were added, see RedSdkExtension enum in redgpu.h. Extensions include: fixed function hardware depth and stencil MSAA resolves, dedicated memory allocations for NVIDIA GPUs, additional driver properties query and an enforcement for coherent memory to be treated as non-coherent. All the extensions are optional but are used in the example programs.

  * All the high level wrapper procedures with source code now live in a single RedGpuSDKExamples/Common/redgpu_quick.h file.

  * HLSL compiler is updated to the latest version for both Ubuntu 18.04 and Windows 10.
