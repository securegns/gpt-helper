# gpt-helper
This project has codes that help working with ChatGPT or other GPT tools 

## List the folder structure and all the contents of the files
### Windows
##### Powershell
```
tree /f | clip
Get-ChildItem -File -Recurse | ForEach-Object {
    "File: $($_.FullName)"
    Get-Content $_.FullName
} | clip
```
##### WSL
```
tree -a | clip.exe
for f in $(find . -type f); do
  echo "=== $f ==="
  cat "$f"
  echo
done | clip.exe
```
### Linux
```
sudo apt-get update
sudo apt-get install tree

tree -a | xclip -selection clipboard
find . -type f -print0 | while IFS= read -r -d '' file; do
  echo "=== $file ==="
  cat "$file"
  echo
done | xclip -selection clipboard
```
## Diagrams
