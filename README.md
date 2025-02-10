
# Graphics.h Setup for Dev-C++

This guide will help you set up the `graphics.h` library in Dev-C++ for simple graphical programs. Please note that `graphics.h` works best with a 32-bit compiler.

---

## Prerequisites
- **Dev-C++ (32-bit)**: Ensure you have the 32-bit version of Dev-C++ installed.

---

## Steps to Set Up `graphics.h`

1. **Download Required Files**
   - Download `graphics.h` and `libbgi.a`.

2. **Copy Files to Appropriate Directories**
   - Place `graphics.h` in:
     ```
     C:\Program Files (x86)\Dev-Cpp\MinGW32\include
     ```
   - Place `libbgi.a` in:
     ```
     C:\Program Files (x86)\Dev-Cpp\MinGW32\lib
     ```

3. **Update Linker Settings**
   - Open Dev-C++ and go to **Tools > Compiler Options**.
   - Under the "Linker" section, add the following flags:
     ```
     -lbgi -lgdi32 -lcomdlg32 -luuid -loleaut32 -lole32
     ```

4. **Test with a Sample Program**
   - Use the following program to test your setup:
     ```cpp
     #include <graphics.h>
     #include <conio.h>

     int main() {
         int gd = DETECT, gm;
         initgraph(&gd, &gm, "");

         circle(200, 200, 100);
         getch();
         closegraph();
         return 0;
     }
     ```
   - Compile and run the program.

---

## Important Notes
- **Switch to a 32-Bit Compiler**: The `graphics.h` library is not compatible with 64-bit compilers. Make sure you use the 32-bit version of Dev-C++ or a similar environment.
- **Consider Modern Alternatives**: For better performance and support, consider switching to modern libraries like **SFML**, **SDL2**, or **Raylib**.

---

If you encounter any issues, feel free to raise them in this repository!

