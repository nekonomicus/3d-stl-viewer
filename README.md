# 3D STL Viewer

A clean, minimalistic web application for viewing 3D STL files with 360-degree rotation.

## Features

- 🔄 360-degree rotation with auto-rotate
- 🖱️ Interactive controls (drag to rotate, scroll to zoom, right-click to pan)
- 🎨 Beautiful gradient background
- 📱 Fully responsive design
- ⚡ Fast loading with CDN-hosted Three.js

## Setup Instructions

1. **Place your STL file**: Ensure your `Example.stl` file is in the root directory alongside `index.html`

2. **Test locally**:
   ```bash
   # Using Python (if installed)
   python3 -m http.server 8000
   
   # Or using Node.js
   npm install
   npm run serve
   ```
   Then open http://localhost:8000 in your browser

## Deployment to Render

### Prerequisites
- GitHub account (username: nekonomicus)
- Render account (sign up at https://render.com)

### Steps

1. **Initialize Git repository**:
   ```bash
   cd "/Users/samuel/Downloads/3D page"
   git init
   git add .
   git commit -m "Initial commit - 3D STL viewer"
   ```

2. **Create GitHub repository**:
   - Go to https://github.com/new
   - Name it something like `3d-stl-viewer`
   - Keep it public
   - Don't initialize with README (we already have one)

3. **Push to GitHub**:
   ```bash
   git branch -M main
   git remote add origin https://github.com/nekonomicus/3d-stl-viewer.git
   git push -u origin main
   ```

4. **Deploy on Render**:
   - Go to https://dashboard.render.com
   - Click "New +" → "Static Site"
   - Connect your GitHub account if not already connected
   - Select your repository: `nekonomicus/3d-stl-viewer`
   - Use these settings:
     - **Name**: `3d-stl-viewer` (or your preferred name)
     - **Branch**: `main`
     - **Build Command**: *(leave completely empty - no build needed)*
     - **Publish Directory**: `.` *(just a single dot)*
   - Click "Create Static Site"

5. **Access your site**:
   - Render will provide you with a URL like `https://3d-stl-viewer.onrender.com`
   - Your 3D model viewer will be live!

## File Structure

```
/Users/samuel/Downloads/3D page/
├── index.html        # Main application file
├── Example.stl       # Your 3D model file
├── package.json      # Node.js configuration
├── render.yaml       # Render deployment configuration
├── .gitignore        # Git ignore file
└── README.md         # This file
```

## Technologies Used

- **Three.js**: 3D graphics library
- **OrbitControls**: Interactive camera controls
- **STLLoader**: STL file loading capability

## Customization

To use a different STL file, simply:
1. Replace `Example.stl` with your file
2. Update line 186 in `index.html` to match your filename:
   ```javascript
   loader.load('YourFile.stl', ...
   ```

## Browser Compatibility

Works on all modern browsers:
- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

## License

MIT
