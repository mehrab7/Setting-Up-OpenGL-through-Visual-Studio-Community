
# Setting Up OpenGL Through Visual Studio Community




## Visual Studio Community
1. Visual Studio Community is the IDE used to edit and run your OpenGL code. The first step is to install it on your machine if you haven’t already. This can be done through the Microsoft Store or through their [website](https://visualstudio.microsoft.com/vs/).

2. During your setup of Visual Studio Community, you should select the **Desktop development with C++ component for installation**. If you already have Visual Studio Community installed you can go through the tab: **Tools>Get Tools and Features…** to install the component if you haven’t.
![visualexample](https://github.com/mehrab7/Setting-Up-OpenGL-through-Visual-Studio-Community/assets/98127515/cccaad0b-584e-4d2a-a0ee-9940767800a1)

## Glut (.h, .lib, .dll) Installation

1. Download GLUT header, lib, and dll files from [OpenGL](https://www.opengl.org/resources/libraries/glut/glutdlls37beta.zip). This will be a zip file.

2. Extract the contents of the file. Paste `glut.h` in `C:\ProgramFiles(x86)\MicrosoftVisualStudio\2019*\Community\BuildTools\VC\Tools\MSVC\{14.16.27023}*\include\GL`.
Create the `\GL` file if it doesn’t exist. 

**The version {###} and the year of the build may differ. This applies for all subsequent steps.*

3. Paste `glut.lib` in `C:\ProgramFiles(x86)\MicrosoftVisualStudio\2019\Community\BuildTools\VC\Tools\MSVC\{14.16.27023}\lib\x64`.

4. Paste `glut32.lib` in `C:\ProgramFiles(x86)\MicrosoftVisualStudio\2019\Community\BuildTools\VC\Tools\MSVC\{14.16.27023}\lib\x86`.

5. Paste `glut.dll` and `glut32.dll` in `C:\Windows\SysWOW64`.

6. Paste `glut32.dll` to `C:\Windows\System32`.

## Linking glut to Visual Studio

1. Open a new project in Visual Studio. This can be done through the tab **File>New>Project...** and select the **Console App** Project Template.![project template](https://github.com/mehrab7/Setting-Up-OpenGL-through-Visual-Studio-Community/assets/98127515/e172399f-99c6-4021-904b-394dbbe47f97)
