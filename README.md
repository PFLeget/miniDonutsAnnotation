# Mini Donuts Annotation

Collaborative annotation of PSF images to classify image quality for the Vera C. Rubin Observatory.

## Goal

Classify each 3x3 star grid image as:
- **Good (0)**: Stars look normal, round/elliptical PSF shapes
- **Unsure (0.5)**: Not sure if good or bad
- **Bad (1)**: Donuts, weird shapes, artifacts, or clearly problematic PSF

## Examples

See the `examples/` directory for reference images:
- `examples/good/` - Examples of good PSF images
- `examples/bad/` - Examples of bad PSF images (donuts, artifacts)
- `examples/unsure/` - Examples of ambiguous cases

## Getting Started

### 1. Get the images

Download and extract the image tarball from SLAC/S3DF:
```bash
# Location at SLAC (update path as needed):
# /sdf/home/l/leget/plotForAnnotation.tar.gz

# Extract to a local directory
tar -xzf plotForAnnotation.tar.gz
```

### 2. Clone this repository and create your branch

```bash
git clone https://github.com/PFLeget/miniDonutsAnnotation.git
cd miniDonutsAnnotation

# Create your branch with your name and batch file
# Format: {your_name}/batch_XX
git checkout -b alex/batch_05
```

### 3. Pick a batch file

Coordinate with the team to avoid duplicates. Each person should work on a different batch file from `csv_files/`:
- `batch_01.csv` through `batch_20.csv`

### 4. Run the annotation tool

```bash
python annotate.py --csv csv_files/batch_XX.csv --image_dir /path/to/plotForAnnotation
```

### 5. Annotate!

Use keyboard shortcuts (displayed on screen):
- **0** = Good
- **8** = Unsure  
- **9** = Bad
- **s** = Skip (leave for later)
- **b** = Go back to previous image
- **q** = Quit (auto-saves)

Progress is saved after each keystroke. You can quit and resume anytime.

### 6. Submit your annotations

When you're done (or want to checkpoint):

```bash
git add csv_files/batch_XX.csv
git commit -m "Completed batch_XX annotations"
git push -u origin your_name/batch_XX
```

Then create a Pull Request on GitHub.

## Tips

- Look at the `examples/` folder before starting to calibrate your judgement
- When in doubt, use "Unsure" (8)
- Take breaks - annotation fatigue leads to inconsistent labels
- Each batch has ~4,500 images, expect ~2-3 hours to complete

## Batch Assignment

| Batch | Annotator | Status |
|-------|-----------|--------|
| batch_01.csv | | |
| batch_02.csv | | |
| batch_03.csv | | |
| batch_04.csv | | |
| batch_05.csv | | |
| batch_06.csv | | |
| batch_07.csv | | |
| batch_08.csv | | |
| batch_09.csv | | |
| batch_10.csv | | |
| batch_11.csv | | |
| batch_12.csv | | |
| batch_13.csv | | |
| batch_14.csv | | |
| batch_15.csv | | |
| batch_16.csv | | |
| batch_17.csv | | |
| batch_18.csv | | |
| batch_19.csv | | |
| batch_20.csv | | |

## Questions?

Contact PF if you have questions about ambiguous cases.
