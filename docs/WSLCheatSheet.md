# WSL Power User Cheat Sheet

### 1. The "What is happening?" Section
| Command | What it does |
| :--- | :--- |
| `wsl -l -v` | Lists all distros and their status. The "Who is actually running?" check. |
| `wsl --list --online` | Shows the menu of distros available for installation. |
| `wsl --status` | Checks your default version and kernel info. |

### 2. The "Kill" Switches
| Command | What it does |
| :--- | :--- |
| `wsl --terminate <DistroName>` | Shuts down one specific distro. Use this when one is acting up but you need the others to stay alive. |
| `wsl --shutdown` | The nuclear option. Kills every distro and the WSL 2 VM instantly. |
| `wsl --unregister <DistroName>` | Warning: This deletes the distro and every file inside it forever. |

### 3. Backdoor & Root Access
| Command | What it does |
| :--- | :--- |
| `wsl -d <DistroName> -u root` | Enters as the root user. This is your "get out of jail free" card for OOBE errors or permission fits. |
| `wsl -d <DistroName> -u <User>` | Logs in as a specific user. |
| `wsl ~ -d <DistroName>` | Launches the distro and teleports you straight to the Linux home directory. |

### 4. Installation & Maintenance
| Command | What it does |
| :--- | :--- |
| `wsl --install -d <DistroName>` | Installs a specific distro (e.g., `Ubuntu-22.04`) from the cloud. |
| `wsl --update` | Forces a check for WSL kernel updates. |
| `wsl --set-default <DistroName>` | Sets your favorite distro as the one that opens when you just type `wsl`. |

### 5. File System Magic
*   **Open Linux files in Windows:** Type `explorer.exe .` inside your Linux terminal to open a Windows folder at your current location.
*   **Access Windows files from Linux:** Your Windows drive is mounted at `/mnt/c/`.
*   **Direct Path:** You can also type `\\wsl$` into the Windows File Explorer address bar to browse all your Linux files.

