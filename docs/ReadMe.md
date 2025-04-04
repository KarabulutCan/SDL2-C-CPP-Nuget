# SDL2Package

SDL2Package is a native C++ NuGet package that bundles [SDL2](https://www.libsdl.org/) and its main extensions (SDL2_image, SDL2_mixer, and SDL2_ttf). By installing this package, you get all the necessary headers, libraries, and DLLs automatically added to your project.

## Features

- Single-step integration of SDL2, SDL2_image, SDL2_mixer, and SDL2_ttf
- Automatic library linking via `.targets` (no manual setup required)
- Post-build copy of DLLs to your output folder, so you can run your application without missing DLL errors
- Works for both x86 and x64 configurations on Windows

## Installation

Using Visual Studio:

Open your C++ project and go to Project → Manage NuGet Packages…
Select your feed source (e.g., nuget.org or a local feed), search for SDL2Package, and click Install

Using nuget.exe or dotnet CLI:

nuget install SDL2Package

or

dotnet add package SDL2Package

## Usage

Include the headers:

```cpp
#include <SDL2/SDL.h>
#include <SDL2/SDL_image.h>
#include <SDL2/SDL_mixer.h>
#include <SDL2/SDL_ttf.h>
```

## Initialize and use SDL:

#include <SDL2/SDL.h>
#include <iostream>

int main(int argc, char\* argv[])
{
if (SDL_Init(SDL_INIT_VIDEO) != 0)
{
std::cerr << "SDL_Init failed: " << SDL_GetError() << std::endl;
return 1;
}
std::cout << "SDL is initialized successfully!\n";

    // Your SDL code here...

    SDL_Quit();
    return 0;

}
