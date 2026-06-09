# NestCheck DXF/SVG v2.5.0

**NestCheck DXF/SVG** is a Windows application for importing, checking, nesting, and exporting SVG and DXF files for laser cutting workflows. It is designed for makers, workshops, laser users, and small production environments that need to place multiple cut and engraving motifs efficiently on material sheets or saved remnant material.

Version **v2.5.0** adds improved handling for **engraving images with a cuttable outer contour**. Files created with LaserCut KonturFix v2.5.0 can now be imported, nested, previewed, and exported with the embedded raster engraving, red cut frame, and additional cut lines kept in alignment.

## Download

Current Windows installer:

[**Download NestCheck_DXF_SVG_v2_5_0_nuitka_multilingual_Setup.exe**](https://github.com/Stoni66/NestCheck_DXF_SVG/releases/download/v2_5_0/NestCheck_DXF_SVG_v2_5_0_nuitka_multilingual_Setup.exe)

Release tag: **v2_5_0**

## What is new in v2.5.0?

- Support for SVG files with embedded raster engraving images
- Engraving image and cuttable outer contour remain aligned during nesting
- Shared transformation for contours and embedded images during placement, rotation, and export
- Improved preview for engraving files with a frame
- Updated help and tooltips
- Refined user interface for v2.5.0
- Nuitka-based Windows build for better source-code protection against simple extraction
- Multilingual user interface with saved language preference

## Key Features

- Import SVG and DXF files
- Import SVG files with embedded raster images for engraving
- Classify outer cuts, inner cuts, engraving, open lines, ignored lines, and problematic contours
- Multi-part and multi-sheet nesting
- Outer-contour nesting for complex files
- Rotation with configurable angle steps
- Manual editing of placed parts
- Material setup with sheet size, border distance, and minimum spacing
- Remnant material management with already cut areas as blocked zones
- Reuse saved remnant sheets for later jobs
- Export SVG and DXF files for the current sheet or all sheets
- Machine profiles for Trotec, LightBurn/RDWorks, Epilog/Universal, and xTool/Generic
- Export dialog for colors and stroke widths
- Integrated trial and license activation workflow
- Windows installer with desktop shortcut and uninstaller

## Typical Workflow

1. **Start a project**
   - Create a new project or open an existing one.
   - Optionally load a demo file to test the workflow.

2. **Import SVG/DXF files**
   - Load one or more SVG or DXF files.
   - Set quantities for each file.
   - Review contours, warnings, and file hints.

3. **Set material**
   - Define the sheet size, for example 600 x 400 mm.
   - Set border distance and minimum spacing.
   - Optionally load a saved remnant sheet.

4. **Run nesting**
   - Configure nesting mode, search step, angle, density, and related settings.
   - The app places the parts on the sheet.
   - For the actual nesting calculation, the real outer contour is most important. Inner lines and engraving images are preserved for output.

5. **Manual editing**
   - Move, rotate, duplicate, or delete placed parts if needed.
   - For engraving motifs with a frame, the raster image and the frame move together.

6. **Check layout**
   - Validate the layout for collisions, spacing, and plausibility.
   - Review warnings and notes before export.

7. **Export**
   - Select the correct machine profile.
   - Export SVG or DXF for the current sheet or all sheets.
   - Adjust colors and stroke widths if required.

8. **Save remnant material**
   - After nesting, the remaining sheet can be saved as remnant material.
   - Already cut outer contours are stored as blocked areas.
   - The remnant can be loaded again for a future job.

## Engraving With Cuttable Frame

NestCheck v2.5.0 can handle SVG files where a detailed engraving is stored as an embedded raster image and a cuttable outer contour is present in the same file. This is especially useful for motifs created in LaserCut KonturFix using the **Engraving + Outer Contour** output mode.

Important points:

- The red outer contour is used as the cut contour and defines the nesting shape.
- The embedded engraving image remains visually intact.
- During nesting and export, the image and outer contour are moved and rotated together.
- The final export should still be checked in Inkscape or the target laser software before production.

## Remnant Material Management

The remnant workflow is designed for real workshop use. When a sheet is only partially used, the remaining area can be saved. NestCheck stores:

- material size
- sheet outer boundary
- already cut part outlines
- resulting blocked zones
- relevant material settings

When the remnant is loaded later, new parts are only placed in free areas. If a remnant is no longer useful, it can be deleted or discarded.

## Export Profiles and Laser Colors

Many laser systems use colors and stroke widths as operation commands. NestCheck therefore includes machine profiles and allows the output to be adjusted.

Typical assignment:

- **Red**: outer cut
- **Green**: inner cut
- **Blue**: engraving
- **Gray**: ignored remnant or helper geometry
- **Orange/Magenta**: open or problematic control lines

The exact meaning can differ depending on machine and software. Always verify the exported file in the target software before production.

## Installation

1. Download `NestCheck_DXF_SVG_v2_5_0_nuitka_multilingual_Setup.exe`.
2. Run the installer.
3. Follow the setup wizard.
4. Start NestCheck from the desktop shortcut or the Windows Start menu.

The installer also includes an uninstaller.

## System Requirements

- Windows 10 or Windows 11
- 64-bit system recommended
- Display resolution suitable for technical layout preview
- Optional: Inkscape, LightBurn, RDWorks, or machine-specific laser software for final export verification

## Licensing

NestCheck includes a trial period. After the trial period, a license is required. Licensing is based on an installation ID shown inside the app and used for license requests.

The app includes fields for:

- Name / company
- E-mail address
- Installation ID
- License code

## Tips for Best Results

- Clean, closed outer contours improve nesting quality.
- Engraving details should not be interpreted as the nesting outer contour.
- For complex motifs, outer-contour nesting is usually faster and more stable.
- Always inspect exported files in the target software before production.
- When working with remnant sheets, make sure old cutouts are shown correctly as blocked areas.

## Project Status

Current version: **NestCheck DXF/SVG v2.5.0 multilingual Nuitka**

This version is intended as a Windows installer and includes the current NestCheck feature set for import, checking, nesting, remnant material handling, engraving-with-frame processing, and laser-ready export.

## Author

Designed by **Oswald Steiner**
