
# Setting Up OpenGL Through Visual Studio Community




## Visual Studio Community
1. Visual Studio Community is the IDE used to edit and run your OpenGL code. The first step is to install it on your machine if you haven’t already. This can be done through the Microsoft Store or through their [website](https://visualstudio.microsoft.com/vs/).

2. During your setup of Visual Studio Community, you should select the **Desktop development with C++** component for installation. If you already have Visual Studio Community installed you can go through the tab: **Tools>Get Tools and Features…** to install the component if you don't have the component.
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

2. In the new project go to **`Project>Properties`**.

    Select **All Configuration** from the **Configuration** dropdown menu on the top left corner.

    Select **`Configuration Properties>C/C++>Precompiled Headers`** and change **Precompiled Header** option’s value to **Not Using Precompiled Headers**.

3. Still in **Properties**, Select **`Configuration Properties>Linker>Input`**. Now right click on **Additional Dependencies** found on right panel and click **Edit** from the dropdown menu.

    Now type this in the **Edit** text box (Note that each .lib is on a new line):
    ```put this in edit
    opengl32.lib
    glu32.lib
    glut32.lib
    ```

4. Try to run OpenGL code. If you are able to run it without errors, congratulations. If not, continue on.


## Additional Steps (If Needed)

1. Paste `glut.h` into `C:\Program Files (x86)\Windows Kits\10\Include\10.0.22621.0\um\gl`. In your program you may need to rewrite your include statement to `#include<gl/glut.h>` instead of `#include<GL/glut.h>`. It depends on the name of the file `glut.h` is in, whether lower or uppercase GL.

2. Paste `glut32.lib` into both the `x64` and `x86` files in `C:\Program Files (x86)\Windows Kits\10\Lib\10.0.19041.0\um`

3. In the **`Project>Properties`** window select **x64** from the dropdown menu. On the main screen in Visual Studio, select **x86** from the dropdown menu next to the debugger dropdown.

    If this does not resolve your errors and red squigglies try out different combinations of the two platform dropdowns in the **Properties** window and on the main screen of the Visual Studio editor. The above configuration in Step 3. worked for me, your machine might be different.
