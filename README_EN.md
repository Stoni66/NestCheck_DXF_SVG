# NestCheck DXF/SVG v2.2.0

**NestCheck DXF/SVG** is a Windows application for preparing, checking, nesting, and exporting DXF and SVG files for laser cutting workflows. It is designed for makers, workshops, laser users, and small production environments that need to place multiple parts efficiently on material sheets and export laser-ready files.

Version **v2.2.0** includes the current SVG proportion import fix. SVG motifs are no longer stretched unevenly when the actual motif bounds and the declared SVG page size differ significantly.

## Key Features

- Import SVG and DXF files
- Check and classify contours
- Multi-part and multi-sheet nesting
- Fast outer-contour nesting for complex files
- Manual editing of placed parts
- Material and remnant material management
- Save remnant sheets with already cut areas as blocked zones
- Reuse saved remnant material for later jobs
- Export SVG and DXF files
- Machine profiles for common laser systems
- Multilingual user interface
- Integrated trial and license workflow
- Windows installer with desktop shortcut and uninstaller

## Typical Workflow

1. **Start a project**
   - Create a new project or open an existing one.
   - Optionally load a demo file to test the workflow.

2. **Import files**
   - Load SVG or DXF files.
   - Set the quantity for each imported file.
   - NestCheck displays contours, warnings, and relevant file hints.

3. **Set material**
   - Define the sheet size, for example 600 x 400 mm.
   - Set border distance and minimum spacing between parts.
   - Optionally load a saved remnant sheet.

4. **Run nesting**
   - Configure nesting mode, search step, density, angle grid, and related parameters.
   - Parts are placed on the material sheet.
   - Only real outer contours are relevant for nesting, so complex engraving and inner lines do not unnecessarily slow down placement.

5. **Manual editing**
   - Move, rotate, duplicate, or delete parts if needed.
   - Arrow keys allow precise manual corrections.

6. **Check layout**
   - Validate the layout for collisions, spacing, and plausibility.
   - Warnings and notes can be reviewed before export.

7. **Export**
   - Export the current sheet or all sheets as SVG or DXF.
   - Select a machine profile and adjust colors or stroke widths where needed.

8. **Save remnant material**
   - After nesting, the remaining sheet can be saved as remnant material.
   - Already cut part outlines are stored as blocked areas.
   - The remnant can be loaded again for a future job.

## Remnant Material Management

The remnant workflow is designed for real workshop use. When a sheet is only partially used, the remaining area can be stored as reusable remnant material. NestCheck keeps track of:

- the outer boundary of the material sheet
- all part outlines that have already been cut
- the resulting blocked areas
- material size and relevant sheet settings

When the remnant is loaded again later, new parts are only placed in the remaining free areas. If the remnant is no longer useful, it can be discarded or deleted.

## Export Profiles

NestCheck supports SVG and DXF export for different laser systems. Depending on the machine and driver, colors and stroke widths may be interpreted differently. For that reason, the app includes export profiles and an export settings dialog.

Typical profiles:

- Trotec / Laser Cut
- LightBurn / RDWorks
- Epilog / Universal
- xTool / Generic

SVG export can include line types such as:

- outer cut
- inner cut
- engraving
- ignored remnant or helper geometry
- open or problematic contours as a control layer

## Notes About Laser Colors

Many laser systems use colors to distinguish operations. However, color interpretation is not identical across all manufacturers. Export colors should always be verified in the target laser software or driver before production.

In many Trotec workflows, red is commonly used for cut contours. Other colors may be used for engraving, marking, or ignored helper geometry. NestCheck allows these values to be adjusted in the export dialog.

## Installation

1. Download **NestCheck_DXF_SVG_v2_2_0_multilingual_Setup.exe**.
2. Run the installer.
3. Follow the setup wizard.
4. Start NestCheck from the desktop shortcut or the Windows Start menu.

The installer also includes an uninstaller.

## System Requirements

- Windows 10 or Windows 11
- 64-bit system recommended
- Display resolution suitable for technical layout preview
- External software such as Inkscape, LightBurn, or machine-specific software is recommended for final SVG/DXF verification

## Licensing

NestCheck includes a trial period. After the trial period, a license is required. Licensing is based on an installation ID. This ID can be copied from the app and used for a license request.

The app includes fields for:

- Name / company
- E-mail address
- Installation ID
- License code

## Known Notes

- Nesting complex contours is a mathematically challenging task. Very complex files may require more processing time.
- Best results are achieved with clean, closed outer contours.
- Inner lines and engraving geometry are preserved for export, but should not be treated as outer contours for nesting.
- Always check the exported file in the target software before production.

## Project Status

Current version: **v2.2.0 multilingual with SVG proportion import fix**

This version is intended as a Windows installer and includes the current NestCheck feature set for import, checking, nesting, remnant material handling, and export.

## Author

Designed by **Oswald Steiner**

