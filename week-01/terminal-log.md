# Terminal Drill Log

## Commands Used
```bash
mkdir cs-foundations
cd cs-foundations
touch README.md
mkdir week-01
cd week-01
touch notes.md
touch conversions.md
mkdir logic
cp notes.md notes-copy.md
mv notes-copy.md scratch.md
rm scratch.md
ls -la

cat << 'EOF' > week-01/terminal-log.md
# Terminal Drill Log

## Commands Used
mkdir cs-foundations
cd cs-foundations
touch README.md
mkdir week-01
cd week-01
touch notes.md
touch conversions.md
mkdir logic
cp notes.md notes-copy.md
mv notes-copy.md scratch.md
rm scratch.md
ls -la

## What do the extra columns in ls -la mean?
1. Permissions and Type (drwxr-xr-x / -rw-r--r--): Starts with d for directory or - for file, followed by read (r), write (w), and execute (x) permissions.
2. Links (1): Number of hard links.
3. Owner (p): The user who owns the file.
4. Size (0): File size in bytes.
5. Date and Time: Last modification timestamp.
6. Name: The file or directory name.
