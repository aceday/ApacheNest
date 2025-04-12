# ApacheNest

ApacheNest is a shell-based utility for setting up and managing a lightweight Apache + PHP environment using Nix Portable. It provides a streamlined way to configure and control Apache and PHP installations, making local development and testing quick and simple.

## Features

- Easy setup for Apache and PHP with Nix Portable.
- Manage multiple PHP versions.
- Customizable Apache and PHP configurations.
- Interactive menus for starting, stopping, and restarting services.
- Self-contained installation in the user's home directory.

## Installation

### Homebrew

```sh
brew install JianZcar/packages/fuzpad
```

### Git Clone

To install ApacheNest, clone this repository and execute the `bin/apachenest` script:

```bash
git clone https://github.com/JianZcar/ApacheNest.git
cd ApacheNest
./bin/apachenest
```

## Usage

Once installed, ApacheNest provides an interactive menu to manage services. Run the command below to access the main menu:

```bash
./bin/apachenest
```

### Main Menu

- **All**: Manage both Apache and PHP services together.
- **Apache**: Start, stop, and restart the Apache server.
- **PHP**: Start, stop, restart, and select PHP versions.
- **Settings**: Customize configurations.

### Service Management

- **Start All**: Start both Apache and PHP services.
- **Stop All**: Stop both Apache and PHP services.
- **Restart All**: Restart both Apache and PHP services.

### PHP Version Management

You can easily switch between PHP versions using the interactive menu under the **PHP** section. ApacheNest will handle the download and setup for the selected PHP version.

## Configuration

ApacheNest stores its configuration files in the following directory:

```plaintext
$HOME/Documents/.apachenest/conf
```

Key configuration files include:

- `httpd.conf`: Apache configuration.
- `php-fpm.conf`: PHP-FPM configuration.
- `php-version.conf`: Selected PHP version.

## Logs

Logs for both Apache and PHP services are stored in:

- Apache logs: `$HOME/Documents/.apachenest/apache/logs/`
- PHP logs: `$HOME/Documents/.apachenest/php-fpm.log`

## Requirements

- `bash`
- `curl`
- `fzf` (for interactive menus)
- `jq` (for JSON parsing)

## Troubleshooting

If you encounter issues with database locks, ApacheNest will automatically detect and remove them or just select Refresh

## Uninstallation

To completely remove ApacheNest, delete the installation directory:

```bash
rm -rf $HOME/Documents/.apachenest
```

## Contributing

Contributions are welcome! Please open an issue or submit a pull request to suggest improvements or report bugs.

## License

This project is licensed under the [License here](LICENSE).

---

🎉 Happy coding with ApacheNest!
