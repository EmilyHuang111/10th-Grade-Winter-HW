# Image Renaming Script

This script renames image files in the current directory based on specific patterns and logs the original and new file names in a CSV file. It is useful for organizing and standardizing image file names, especially when working with large batches of images. Additionally, the CSV file can be imported into Google Sheets to view and manage file name changes.

## How It Works

1. The script loops through all `.JPG` files in the current directory.
2. For each file, it checks if the file name matches one of two specific patterns:
   - **Pattern 1**: File names starting with `IMG_`, `DSC_`, `MMA`, or `WJ2_` followed by numbers (e.g., `IMG_1234.JPG`).
   - **Pattern 2**: File names starting with `SM__` followed by numbers (e.g., `SM__5678.JPG`).
3. Based on the matched pattern, a new name is generated:
   - **Pattern 1**: Files are renamed to `PWP2024_000[number]E_EMILY.JPG`.
   - **Pattern 2**: Files are renamed to `PWP2024_000[number]EM_EMILY.JPG`.
4. The original and new file names are appended to a CSV file named `file_log.csv` for tracking and reference.

## Usage

1. Place the script in the directory containing the `.JPG` files you want to rename.
2. Run the script in the terminal:
   ```bash
   bash rename_images.sh

## Requirements

- **Bash**: This script is written for a Unix-like shell that supports Bash.
- **Perl**: The script uses Perl for pattern matching and renaming operations.

