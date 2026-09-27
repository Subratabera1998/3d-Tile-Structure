# 3D Block Structure

An interactive web-based 3D block structure visualization and editing tool.

## Features

- Create 3D block structures of different dimensions.
- Change the colour of individual blocks.
- Select, group, separate, reverse, and move blocks.
- Rotate the 3D structure using mouse controls.
- Show block numbers on the structure.
- Show A-B-C direction indicators.
- Show the ket representation of selected blocks.
- Display a flattened representation of the structure.
- Undo and redo operations.
- Enter fullscreen mode for the 3D structure.
- Export the current 3D view as a high-resolution PDF.

## Dimensions

The structure can be defined as

n × m × r

using the dimension controls at the bottom of the application.

Each block is labelled using the form:

ABC

where A, B, and C denote the three coordinates.

## Selecting and Deselecting Blocks

### Select a block

First click a colour in the colour palette to paint blocks.

To select blocks instead of painting, click the active colour again. This removes the active colour selection and switches to block-selection mode.

Click a block to select it. The selected block is highlighted.

### Select multiple blocks

Click additional blocks to select them. Each click toggles the selection of that block.

### Deselect a block

Click a selected block again to deselect it.

### Select all blocks

Click the **Select All** button to select all blocks.

### Clear all selections

Double-click on an empty area (white space) of the 3D view.

This clears both:

- all selected blocks
- the active colour selection

The same double-click action works on empty areas of the flattened view.

## PDF Export

The PDF export contains the current 3D view as a high-resolution image.

### Download button

Click the download icon to download the PDF directly to the browser's default **Downloads** folder.

### Ctrl+S

Press **Ctrl+S** to open the **Save As** dialog. The dialog starts in the **Downloads** folder, allowing you to choose the filename and location.

## Keyboard Shortcuts

- **Ctrl+S**: Save PDF As
- **Ctrl+Z**: Undo
- **Ctrl+Y**: Redo
- **Ctrl+G**: Group selected blocks
- **Ctrl+Shift+G**: Ungroup
- **Esc**: Exit fullscreen mode

## Icon Guide

The main controls use the following icons:

| Icon | Name | Function |
|---|---|---|
| `+` | Add Colour | Opens the colour picker so a custom colour can be added to the palette. |
| `🧊` | Flattened View | Shows or hides the flattened 2D representation of the 3D block structure. |
| `A` | A Direction | Selects the A-fixed flattened view. |
| `B` | B Direction | Selects the B-fixed flattened view. |
| `C` | C Direction | Selects the C-fixed flattened view. |
| `↑ / ↓` | Layer Order | Toggles the flattened layer order between ascending and descending. |
| <svg viewBox="0 0 24 24" aria-hidden="true" style="width:18px;height:18px;vertical-align:middle"><path d="M12 3v11m0 0-4-4m4 4 4-4M5 17v3h14v-3" fill="none" stroke="currentColor" stroke-width="1.9" stroke-linecap="round" stroke-linejoin="round"/></svg> | Download PDF | Downloads the current 3D view as a PDF directly to the browser's default Downloads folder. |
| `⛶` | Full Screen | Opens the custom fullscreen view of the 3D structure. |
| `×` | Exit Full Screen | Closes the custom fullscreen view and returns to the normal page. The fullscreen button changes from `⛶` to `×` while fullscreen is active. |
| `⚙` | Settings | Opens or closes the settings panel containing display options and History Count. |
| `▦` | Select All | Selects all blocks. When all blocks are selected, the same control can deselect them. |
| `⧉` | Group | Groups the selected blocks. When a complete existing group is selected, the control performs the corresponding ungroup action. |
| `⤢` | Separate | Separates the selected blocks or groups. |
| `↺` | Reverse | Reverses the separation of selected blocks or groups by returning them toward their original positions. |
| <svg viewBox="0 0 24 24" aria-hidden="true" style="width:18px;height:18px;vertical-align:middle"><path d="M12 3v18M3 12h18" fill="none" stroke="currentColor" stroke-width="1.9" stroke-linecap="round"/><path d="M12 3l-2.6 2.6M12 3l2.6 2.6M12 21l-2.6-2.6M12 21l2.6-2.6M3 12l2.6-2.6M3 12l2.6 2.6M21 12l-2.6-2.6M21 12l-2.6 2.6" fill="none" stroke="currentColor" stroke-width="1.9" stroke-linecap="round" stroke-linejoin="round"/></svg> | Free Move | Toggles Free Move mode. When enabled, selected blocks or groups can be dragged in the 3D view. |
| `↶` | Undo | Reverts the most recent stored action. |
| `↷` | Redo | Reapplies an action that was undone. |
| `↻` | Reset | Resets the current structure to its initial arrangement using the current dimensions. |

### Download icon

The **Download** icon is <svg viewBox="0 0 24 24" aria-hidden="true" style="width:18px;height:18px;vertical-align:middle"><path d="M12 3v11m0 0-4-4m4 4 4-4M5 17v3h14v-3" fill="none" stroke="currentColor" stroke-width="1.9" stroke-linecap="round" stroke-linejoin="round"/></svg>, the downward arrow pointing into a tray. Clicking it performs a direct PDF download rather than opening the Save As dialog.

### Free Move icon

The **Free Move** icon is <svg viewBox="0 0 24 24" aria-hidden="true" style="width:18px;height:18px;vertical-align:middle"><path d="M12 3v18M3 12h18" fill="none" stroke="currentColor" stroke-width="1.9" stroke-linecap="round"/><path d="M12 3l-2.6 2.6M12 3l2.6 2.6M12 21l-2.6-2.6M12 21l2.6-2.6M3 12l2.6-2.6M3 12l2.6 2.6M21 12l-2.6-2.6M21 12l-2.6 2.6" fill="none" stroke="currentColor" stroke-width="1.9" stroke-linecap="round" stroke-linejoin="round"/></svg>, the four-direction movement symbol. When Free Move is enabled, a selected block or group can be dragged to a new position in the 3D view.

### Cross icon

The **×** icon appears in place of the fullscreen icon when the custom fullscreen view is active. Clicking it exits the custom fullscreen view.

### Settings icon

The **⚙ Settings** icon opens a panel containing:

- Show block numbers
- Show A-B-C directions
- Show ket
- Show shadow
- History Count

## History Count

**History Count** controls how many previous actions are kept for **Undo** and **Redo**.

Available options are:

**1, 2, 3, 5, 10, and 20**

The default value is **5**.

For example, when History Count is set to **5**, the application keeps the five most recent actions available for Undo/Redo. When the limit is reached, older history is removed to keep the history within the selected limit.

Changing the History Count immediately adjusts both the Undo and Redo history to the selected limit.

## Controls

### 3D View

- Drag with the mouse to rotate the structure.
- Use the selection and manipulation controls to work with blocks.

### Settings

- Show block numbers
- Show A-B-C directions
- Show ket
- Show shadow
- History count

## Technology

- HTML
- CSS
- JavaScript
- Three.js

## Author

Developed by **Subrata Bera**

Department of Applied Mathematics  
University of Calcutta

Rajabazar Science College  
92, Acharya Prafulla Chandra Road  
Kolkata-700009, West Bengal, India

Email: 98subratabera@gmail.com

Year of Development: 2026
