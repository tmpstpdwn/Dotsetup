# Dotsetup

The Dotsetup script automates the installation of dotfiles from a specified Git repository. It backs up existing files in your home directory and clones the latest commit of the dotfiles repository.

## Features

- Backs up existing files in your home directory to a .backup folder.
- Clones the specified dotfiles repository as a bare Git repository.
- Checks out the dotfiles into your home directory.
- Configures Git to hide untracked files during usage.

## Requirements

Git must be installed on your system.

## Usage

- The script is inside [src/](src)

```bash
./dotsetup.sh <repository-url>
```

- Follow the Prompts:

- The script will ask for confirmation before proceeding to move your existing files.
- If you confirm, it will move all files in your home directory (except the backup directory itself) to .backup/.

## Important Notes

- Backup Directory: The script will create a .backup directory in your home folder where all existing files will be moved. Ensure you have enough space and remember that this operation is irreversible.
- Shallow Clone: The script performs a shallow clone of the repository (only the most recent commit) to save time and bandwidth.
- Configuration: After running the script, the Git configuration will be set to hide untracked files when using the dotfiles alias.
- The git repo should represent your $HOME dir. refer my dotfiles [repo](https://github.com/tmpstpdwn/.dotfiles).
- Got this idea from this [blog](https://www.atlassian.com/git/tutorials/dotfiles).

## Example

```bash
./dotsetup.sh https://github.com/yourusername/dotfiles.git
```

## Troubleshooting

If you encounter issues, ensure that the repository URL is correct and that you have appropriate permissions to access it.
Check that you have Git installed and properly configured on your machine.

## License
This script is licensed under AGPL3 [LICENSE](LICENSE).

