# Useful Linux Aliases

## Why Use Aliases?

Aliases are shortcuts that allow you to execute commands or a series of commands with simple keystrokes. They can make your workflow more efficient by saving time on repetitive tasks and reducing the likelihood of errors when typing complex commands.

## How to Add Aliases to Your Shell Configuration

To easily apply these aliases, you can copy them to your `.bashrc`, `.zshrc`, or similar shell configuration file. This will ensure that they are loaded every time you open a new terminal session.

You can quickly add these aliases to your shell configuration with the following command:

```bash
curl -s https://raw.githubusercontent.com/sheesetfs/usefulAliases/main/aliases >> ~/.bashrc && source ~/.bashrc
```

If you use Zsh:

```bash
curl -s https://raw.githubusercontent.com/sheesetfs/usefulAliases/main/aliases >> ~/.zshrc && source ~/.zshrc
```

This command will download the aliases from the provided URL, append them to your shell configuration file, and then reload the file so that the aliases take effect immediately.

### Applying Aliases Globally

To make these aliases available for all users on the server, you can add them to the global shell configuration file, usually located at `/etc/bash.bashrc` or `/etc/zsh/zshrc`. Run the following command with superuser privileges:

```bash
sudo curl -s https://raw.githubusercontent.com/sheesetfs/usefulAliases/main/aliases >> /etc/bash.bashrc
```

Or for Zsh:

```bash
sudo curl -s https://raw.githubusercontent.com/sheesetfs/usefulAliases/main/aliases >> /etc/zsh/zshrc
```

After this, all users will have access to these aliases when they open a new terminal session.

## Alias Descriptions

- `alias c='clear'`: Clears the terminal screen.
- `alias ll='ls -lah --color=auto'`: Lists directory contents in long format with human-readable sizes and color output.
- `alias ..='cd ..'`: Moves up one directory level.
- `alias ...='cd ../../../'`: Moves up three directory levels.
- `alias ....='cd ../../../../'`: Moves up four directory levels.
- `alias .....='cd ../../../../'`: Moves up five directory levels.
- `alias grep='grep --color=auto'`: Adds color to the grep search results for easier reading.
- `alias mkdir='mkdir -pv'`: Creates directories, including parent directories, and prints what it creates.
- `alias ports='netstat -tulanp'`: Lists all open ports and associated programs.
- `alias update='sudo apt update && sudo apt dist-upgrade -y'`: Updates the package lists and upgrades all packages on Debian-based systems.
- `alias nginxrestart='sudo systemctl restart nginx'`: Restarts the Nginx service.
- `alias nginxtest='sudo nginx -t'`: Tests the Nginx configuration for errors.
- `alias nginxstatus='sudo systemctl status nginx'`: Shows the status of the Nginx service.
- `alias wget='wget -c'`: Resumes partially downloaded files with wget.

These aliases are designed to streamline common tasks and make your Linux experience more efficient.
