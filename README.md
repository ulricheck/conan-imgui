# conan-imgui

[Conan.io](https://conan.io) package for imgui library. 

## Add Remotes

    $ conan remote add camposs "https://conan.campar.in.tum.de/api/conan/conan-camposs"
    $ conan remote add ubitrack "https://conan.campar.in.tum.de/api/conan/conan-ubitrack"

## For Users: Use this package

### Basic setup

    $ conan install ubitrack_imgui/0.3.5@camposs/stable
    
### Project setup

If you handle multiple dependencies in your project is better to add a *conanfile.txt*
    
    [requires]
    ubitrack_imgui/1.66@camposs/stable

    [options]
    
    [generators]
    txt
    cmake

Complete the installation of requirements for your project running:</small></span>

    $ mkdir build && cd build && conan install .. 

Project setup installs the library (and all his dependencies) and generates the files *conanbuildinfo.txt* and *conanbuildinfo.cmake* with all the paths and variables that you need to link with your dependencies.

## For Packagers: Publish this Package

The example below shows the commands used to publish to campar conan repository. To publish to your own conan respository (for example, after forking this git repository), you will need to change the commands below accordingly. 

## Build packages

    $ conan create . ubitrack/stable

## Upload packages to server

    $ conan upload -r ubitrack ubitrack_imgui/1.66@camposs/stable --all