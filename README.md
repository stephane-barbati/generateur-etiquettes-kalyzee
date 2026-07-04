# generateur-etiquettes-kalyzee
Standalone web app for generating and printing Kalyzée cable label sheets on Mr-Label US Letter paper.
# Kalyzee Cable Label Sheet Generator

Standalone web app for generating and printing Kalyzee cable label sheets on Mr-Label US Letter paper.

The app is a single HTML file and does not require a server, build step, package manager, or internet connection.

## Features

- One sheet per label: the selected label is repeated across all 32 positions.
- Print all labels from a label library, one sheet per label.
- Calibration mode with printable label boundaries.
- Final print mode with text only.
- Millimeter-based physical settings.
- Save and load calibration settings as JSON.
- Import and export label libraries as CSV.
- Save and load full projects as JSON.

## Template

- Paper size: US Letter, 215.9 mm x 279.4 mm
- Layout: 4 rows x 8 columns
- Labels per sheet: 32
- Full label size: 26 mm x 60 mm
- Printable text area: 26 mm x 21 mm
- Text position: top printable area of each label

## How To Use

Open `generateur-etiquettes-kalyzee.html` directly in a browser.

Choose a label from the library, or type a custom label in the printed text field. Click `Fill` to repeat that label across the whole sheet.

Use `Next` to move through the label library one sheet at a time.

## Printing

Use the browser print dialog with:

- Scale: 100%
- Paper size: US Letter
- Margins: none
- Fit to page: disabled
- Browser auto-centering: disabled when available

The app controls the physical position of the label grid using millimeter-based settings.

## Calibration

Enable `Calibration` to show label boundaries on screen.

When calibration is enabled during printing, the app prints:

- a solid outline around each full label;
- a dashed outline around the top printable text area.

When calibration is disabled, printing outputs text only.

Recommended first calibration values:

- Top margin: 8.8 mm
- Left margin: 4.2 mm
- Horizontal gap: 0 mm
- Vertical gap: 7 mm
- Label width: 26 mm
- Label height: 60 mm
- Printable area width: 26 mm
- Printable area height: 21 mm

Adjust these values by small increments, then print a calibration sheet until the outlines match the physical labels.

## Saving Settings

In `Physical settings`:

- `Save` stores the current settings in the browser.
- `Export` downloads a settings JSON file.
- `Load` imports a previously exported settings JSON file.

Project JSON export also includes the current settings and label library.

## CSV Format

CSV import/export uses one label per line:

```csv
Camera board
Camera presenter
Microphone
HDMI IN Presenter
USB IN Capture Card
WAN
VLAN
PC Orchestrator
```

## Project Files

- `generateur-etiquettes-kalyzee.html`: the app.
- `reglages-etiquettes-kalyzee.json`: example calibration settings.

## License

MIT License
