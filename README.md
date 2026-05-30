# Spreedy

A 3D spreadsheet app based on [Excel3](https://github.com/gewfy/excel3).

## Installation

```bash
# Install dependencies
npm install

# Start the development server
npm run dev
```

The application will open at `http://localhost:5173`

## How to use

### Basic Navigation

#### Mouse Controls

- **Click**: Select a cell
- **Click + Drag**: Select a range of cells (creates 3D cubic selection)
- **Shift + Click**: Extend selection from current cell
- **Cmd/Ctrl + Drag**: Rotate the 3D matrix
- **Right-Click + Drag**: Pan the camera view
- **Mouse Wheel**: Zoom in/out

#### Keyboard Controls

**Cell Navigation** (adapts to viewing angle):

- `↑↓←→`: Navigate cells - horizontal keys adapt based on rotation
  - Front view: Left/Right = X-axis (columns)
  - Side view: Left/Right = Z-axis (depth)
- `Alt + ↑↓`: Navigate through depth axis (swaps with columns when viewing from side)
- `Shift + Arrows`: Extend selection while navigating

**Cell Editing**:

- `Type`: Start editing selected cell
- `Enter`: Save and move to cell below
- `Escape`: Cancel editing
- `Delete/Backspace`: Clear selected cells

### Text Formatting

Select cells, then use the toolbar:

- **B** - Bold text
- **I** - Italic text
- **S** - Strikethrough
- **A⁺** - Increase font size (+10px)
- **A⁻** - Decrease font size (-10px)
- **Font Dropdown** - Change font family
- **Color Pickers** - Set background and text colors

### Special Features

**Version Management**

- **Save**: Opens version save dialog - enter a name and save
- **Load**: View list of saved versions, click to load or delete
- Each version stores complete state including all formatting

**AutoSum (Σ)**

1. Select a range of cells with numeric values
2. Click the Σ button in toolbar
3. Sum appears in the cell immediately below your selection
4. Original selection remains active

**Quantum Uncertainty (magic wand icon)**:

- Numeric values fluctuate ±10%
- Click a cell to "observe" and collapse the wave function
- Values freeze once observed
- Great for demonstrating quantum superposition

### Special View Modes

**Hide Borders (grid icon)**:

- Toggles cell border visibility
- Cleaner view for presentations

**3D Anaglyph (glasses icon)**:

- Enables red-cyan stereoscopic 3D
- Put on red-cyan 3D glasses for depth perception
- Automatically switches to perspective camera

**4D Projection (cube icon)**:

- Projects 4D coordinates into 3D space
- Continuous rotation through 4th dimension
- Barrel distortion creates fisheye effect
- Switches to ultra-wide FOV camera
