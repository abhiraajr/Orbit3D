# Orbit3D - A 3D Model Viewer (3DViewer.net Embedded)

This project uses the official 3DViewer.net embedded viewer to display interactive 3D models directly in the browser.  
Models can be switched instantly using the top-right menu. Adding new models is extremely simple — just upload your file and add one button.

---

## 📁 Included Models

The default build includes the following four sample models:

- 20mm_cube.stl
- airplane.obj
- alienspaceship.glb
- floatplane.obj

All models are stored in the same folder as the viewer page.

---

## ✔️ Supported Model Formats

The viewer supports all formats accepted by 3DViewer.net, including:

- STL
- OBJ
- GLB / GLTF
- FBX
- DAE
- PLY
- 3MF
- OFF
- DXF
- X3D

Basically, if 3DViewer.net can load it, this viewer can load it too.

---

## 🛠 How to Add or Change Models

1. **Upload the model file**  
   Place your model in the same folder as the viewer HTML page. For example:  


2. **Add a menu button**  
Open `index.html` and locate the top-right menu panel:  

```html
<div id="menu" class="panel">
  <button class="menu-button" data-model="20mm_cube.stl">20mm_cube.stl</button>
  <button class="menu-button" data-model="airplane.obj">airplane.obj</button>
  <!-- Add your new model button below -->
  <button class="menu-button" data-model="my_model.obj">my_model.obj</button>
</div>
```

3. **Set the default model on page load**  
In the `<script>` section, the initial model is loaded using `loadIframe("...")`. Change the model filename to your preferred default:

```javascript
// Load default model on page load
loadIframe('20mm_cube.stl'); // Replace '20mm_cube.stl' with your model
```

4. **Save and reload the page**  
   The viewer will automatically load your new model, and it will appear in the top-right menu.

---

## ⚙ Viewer Settings

- **Background Color** – Change the 3D scene background using the color picker.  
- **Default Object Color** – Apply a base color to models without a predefined material.  
- **Apply Settings** – Click to update the viewer with your chosen colors.  

---

## 🖱 Interaction

- **Rotate** – Click and drag with the mouse or swipe on touch devices.  
- **Zoom** – Use the mouse wheel or pinch on touch devices (scrolling horizontally in the menu is separate).  
- **Pan** – Hold right-click (or two-finger drag) to move the model in the viewport.  

---

## 🎛 Top-Right Menu Behavior

- If more than three buttons exist, the menu becomes a horizontal scrollable row.  
- Mouse scroll wheel over the menu converts vertical scroll to horizontal movement.  
- The menu automatically hides the scrollbar for a cleaner look.

---

## 📂 Folder Structure Example
```text
main (branch)
│
├─ index.html
├─ 20mm_cube.stl
├─ airplane.obj
├─ alienspaceship.glb
├─ floatplane.obj
├─ LICENSE
└─ README.md
```

---

## ⚡ Notes

- All models must reside in the same folder as the viewer page or you must adjust the `data-model` path.  
- The viewer relies on 3DViewer.net for rendering; ensure your device has an active internet connection.  
- The viewer supports both small and large models, but extremely high-poly models may load slower in the browser.

---

## 🎨 Credits

- **Project Author:** me (GitHub: `abhiraajr`)  
- **3D Rendering Engine:** [3DViewer.net](https://3dviewer.net)
