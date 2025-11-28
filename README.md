OLED Pixel Architect
====================

The **OLED Pixel Architect** is a single-file, responsive web application designed for creating and exporting monochrome (1-bit) bitmap graphics, primarily for use on small OLED displays like the popular 128x64 or 128x32 SSD1306 screens.

It provides an intuitive pixel-level editing experience with real-time code generation for Arduino (C/C++) and MicroPython/CircuitPython framebuf libraries.

![Screenshot](https://github.com/GeorgeYT9769/oled-architect/blob/main/screenshot.png?raw=true)

✨ Features
----------

*   **Pixel-Perfect Canvas:** A scalable grid environment where you can design your graphics.
    
*   **Real-time Code Output:** Automatically generates bitmap arrays in the popular formats:
    
    *   **Arduino/C:** const unsigned char myBitmap\[\] PROGMEM
        
    *   **MicroPython/Python:** bytearray format for framebuf.FrameBuffer
        
*   **Drawing Tools:** Includes standard tools for pixel manipulation:
    
    *   **Pencil (P):** Draw single pixels or lines.
        
    *   **Eraser (E):** Erase pixels.
        
    *   **Fill Bucket (B):** Flood-fill areas.
        
    *   **Shape Tools:** Draw **Lines (L)**, **Rectangles (R)**, **Circles (C)**, and **Triangles (T)**.
        
*   **Object Manipulation:** Shape tools and imported images create temporary "active objects" that can be:
    
    *   Moved with arrow keys.
        
    *   Rotated (R).
        
    *   Resized (drag the bottom-right handle).
        
    *   Confirmed (Enter) or discarded (Esc).
        
*   **History & Utility:** Undo, Clear Canvas, and Invert Pixels.
    
*   **Icon Library:** Import popular vector icons directly onto the canvas as editable bitmaps.
    
*   **Reference Layer:** Load external bitmap code to trace or align your designs.
    

💻 How to Use
-------------

### 1\. Drawing

1.  **Select a Tool:** Click a tool in the left sidebar (Pencil, Eraser, Line, etc.) or use the keyboard shortcuts (P, E, B, L, R, C, T).
    
2.  **Draw:** Click and drag on the canvas to draw.
    
3.  **Shapes:** For shape tools (Line, Rect, Circle, Triangle), click to set the starting point and drag to the desired end point. The shape is rendered as a temporary "Active Object."
    
4.  **Editing Active Objects:** While an object is active, move it with the **Arrow Keys**, resize it using the bottom-right handle, or press **R** to rotate it.
    
5.  **Commit:** Press **Enter** or click the **Check** icon in the status bar to permanently merge the object onto the canvas.
    

### 2\. Canvas Management

*   **Zoom:** Use the slider at the top to adjust the pixel scale (zoom level).
    
*   **Resize:** Use the **W** and **H** input fields in the header to set new dimensions (e.g., 128x32 or 64x48) and click **Resize**. **Note:** Resizing wipes the current drawing.
    

### 3\. Code Generation and Export

1.  **View Code:** Look at the bottom panel (Code Output).
    
2.  **Switch Tabs:** Click the **Arduino** or **MicroPython** tab to view the generated code in the desired format.
    
3.  **Copy:** Click the **Copy** button to quickly copy the code block to your clipboard for use in your microcontroller project.
    

### 4\. Importing and Reference

1.  **Import:** Click **Import** in the header. Paste a raw C array or Python byte string. This imports the graphic as a new "Active Object" you can position and commit.
    
2.  **Reference:** Click **Ref** in the header. Paste code here to load a graphic faintly _under_ your current drawing, allowing you to trace or align your new design to an existing bitmap.
    

💡 Pro Tips
-----------

*   **Keyboard Shortcuts:** The most efficient way to use the app is with shortcuts (P, E, B, L, R, C, T).
    
*   **Constraint Drawing:** Hold **Shift** while drawing shapes to constrain them (e.g., a square rectangle, a perfect circle, or 45/90-degree lines).
    
*   **Undo:** Use Ctrl+Z (or Cmd+Z on Mac) to quickly undo the last action.
