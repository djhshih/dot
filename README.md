# Customize Shell Configuration
This repo contains personal configuration files for various tools and environments.

## Contents
- **Shell**: `.bash_profile`, `.my.bashrc` (main custom config)  
- **Terminal**: `.Xresources` (X11 theming), `.terminfo/r` (terminal compatibility)  
- **Tools**: `.vimrc` (Vim), `.tmux.conf` (Tmux), `.Rprofile` (R), `.xinitrc` (X11 startup)  
- **Setup**: `install.sh` (automated symlinking)  

## Quick Setup
1. **Clone the repo** to your machine:
   ```bash
   git clone git@github.com:djhshih/dot.git
   cd dot
   ```
2. **Run the install script**:
   ```bash
   bash install.sh
   ```
   This script:
  * Creates symbolic links from the repo to your home directory (~/) for:
    - `.my.bashrc` (always linked)
    - `.bash_profile` (only if doesn't exist)
    - `.Rprofile`, `.Xresources`, `.tmux.conf`, `.terminfo/` (force updated)
  * Secures SSH config permissions (chmod 600 .ssh/config if exists)
3. **Add this line to your `.bashrc`**:
    ```bash
    echo ". ~/.my.bashrc" >> ~/.bashrc
    ```
    This ensures your custom configurations load automatically in all new terminal sessions.
4. **Source your `.bashrc` to apply changes immediately**:
    ```bash
    source ~/.bashrc
    ```
