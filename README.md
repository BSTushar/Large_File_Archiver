A lightweight Bash script to compress and archive files larger than 20MB within a specified directory. This script is useful for managing disk space by organizing and compressing large files in development environments.
Project Structure

/mnt/c/Users/Lenovo/projects/
├── archive/         # Automatically created if not present
├── large files
└── archive_large.sh # This script

Author

Tushar
Script Overview

    BASE: Target directory path.

    DAYS: Reserved for future use.

    DEPTH: Directory search depth (1 by default).

    RUN: Flag to control execution (currently set to 0 to allow compression).

The script performs the following steps:

    Checks if the target directory exists.

    Creates an archive folder if it does not already exist.

    Finds all files larger than 20MB in the specified directory (up to the defined depth).

    Compresses each file using gzip.

    Moves the compressed file to the archive folder.

Usage

    Update the BASE variable in the script to point to your desired directory.

    Make the script executable:

chmod +x archive_large.sh

Run the script:

    ./archive_large.sh

Sample Output

[Mon Jun 17 22:00:00 IST 2025] Compressing: /mnt/c/Users/Lenovo/projects/large_file.mp4

After compression, the file will be moved to:

/mnt/c/Users/Lenovo/projects/archive/large_file.mp4.gz

Notes

    Requires gzip to be installed on the system.

    Only files larger than 20MB are compressed.

    Operates only within the specified directory depth.

    Files are moved to the archive directory after compression.
