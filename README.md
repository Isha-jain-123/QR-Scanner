# QR Scanner

Two small Python scripts for generating QR codes: one for a single item and one for batch processing from a CSV file.

## Scripts

### `scanner.py`

Generates a single QR code containing herbal/medicinal information (peppermint: uses, steep time) and saves it as `peppermint.png`.

### `multi_items.py`

Reads a CSV file (`herbs.csv`) with **Name** and **Details** columns and generates one QR code image per row. Each image is saved as `<Name>.png` with a blue-on-white colour scheme.

## Requirements

```bash
pip install qrcode[pil]
```

For the batch script, create a `herbs.csv` with at least a `Name` and `Details` column:

```
Name,Details
Peppermint,"Uses: indigestion, nausea. Steep time: 5-10 mins."
Chamomile,"Uses: sleep, anxiety. Steep time: 5 mins."
```

Then run:

```bash
python multi_items.py
```
