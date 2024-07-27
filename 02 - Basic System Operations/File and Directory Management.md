#

1. **List Files (ls):** The `ls` command lists files in the current directory. By default, it displays files in the current folder. For example:
    ```bash
    ls
    ```

2. **Change Directory (cd):** Use `cd` to navigate between directories:
    - To move up one level (e.g., from `/home/user/docs` to `/home/user`), use `cd ..`.
    - To go directly to a specific directory (e.g., `/home/user/music`), provide the absolute path: `cd /home/user/music`.
    - To return home from any location, use `cd ~`.

3. **Create Directories (mkdir):** You can create directories using `mkdir`. For example:
    - Create a directory named "dir1":
        ```bash
        mkdir dir1
        ```
    - Create nested directories (with `-p` flag):
        ```bash
        mkdir -p dir1/dir2/dir3
        ```

4. **Remove Files (rm):** The `rm` command deletes files. For example:
    ```bash
    rm testfile
    ```

5. **Remove Directories (rmdir and rm -rf):**
    - Use `rmdir` to remove empty directories:
        ```bash
        rmdir dir1
        ```
    - Use `rm -rf` with caution to forcefully remove a directory and its contents:
        ```bash
        rm -rf dir1
        ```


- [(1) How to Perform File and Directory Management (Part 3) - Tecmint.](https://www.tecmint.com/file-and-directory-management-in-linux/.)
- [(2) How to Manage Files from the Linux Terminal: 11 Commands ... - How-To Geek.](https://www.howtogeek.com/107808/how-to-manage-files-from-the-linux-terminal-11-commands-you-need-to-know/.)
- [(3) Linux File Management Series for Beginners - Linux Shell Tips.](https://www.ubuntumint.com/linux-file-management/.)
- [(4) Linux Commands Cheat Sheet {with Free Downloadable PDF} - phoenixNAP.](https://phoenixnap.com/kb/linux-commands-cheat-sheet.)