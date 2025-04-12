---

## 🍏 2. `mac_terminal_cheat_sheet.md`

```markdown
# 🍏 macOS Terminal Cheat Sheet

Essential terminal commands for navigating, editing, and surviving on macOS (zsh or bash).

---

## 📁 Navigation

```bash
pwd           # print working directory
ls            # list files in current directory
cd folder/    # change directory
cd ..         # move up one level
```

---

## 📄 Files & Folders

```bash
touch file.txt            # create a new file
mkdir new_folder          # create directory
rm file.txt               # delete file
rm -r folder/             # delete folder and contents
cp file1.txt file2.txt    # copy file
mv file.txt new_name.txt  # rename or move
```

---

## 🛠 File Permissions

```bash
chmod +x script.sh       # make executable
ls -l                    # view permissions
sudo command             # run with admin privileges
```

---

## 🔍 Finding Stuff

```bash
find . -name \"file.txt\"         # search for a file
grep \"text\" file.txt            # find text inside file
grep -r \"pattern\" folder/       # recursive grep
```

---

## ✍️ Editing

```bash
nano file.txt             # basic text editor
```

---

## 📦 Install with Homebrew

```bash
brew install packagename
```

---

## 💡 Tips

- Use Tab for autocomplete
- Use ↑ and ↓ to scroll through command history
- Use clear to wipe the screen

---