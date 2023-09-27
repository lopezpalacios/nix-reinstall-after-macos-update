# Nix Reinstaller Utility

A simple shell script designed to assist in re-installing Nix on macOS, especially after an OS update.

## Description

macOS tends to overwrite `/etc/zshrc` and `/etc/bashrc` files with every update. Since Nix installs configurations to these files, this script helps in preparing the environment for a fresh Nix installation after such updates.

This repository contains a shell script to perform specific `mv` and `rm` operations to cater to this specific Nix installation issue.

## Installation & Usage

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/lopezpalacios/nix-reinstall-after-macos-update.git
   cd nix-reinstaller-utility
   ```

2. **Provide Execution Permissions:**
   ```bash
   chmod +x myscript.sh
   ```

3. **Run the Script (with sudo):**
   ```bash
   sudo ./myscript.sh
   ```

> **Caution:** Before running the script, ensure you understand the implications, as it performs file deletions. Ensure you've backed up any important configurations.

## Next Steps

After running this script, proceed to re-install Nix. For the daemon-based installation:

```bash
sh <(curl -L https://nixos.org/nix/install) --daemon
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License

[MIT](https://choosealicense.com/licenses/mit/)
