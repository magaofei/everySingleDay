PHP

```shell
The php.ini file can be found in:
    /usr/local/etc/php/7.1/php.ini

✩✩✩✩ Extensions ✩✩✩✩

If you are having issues with custom extension compiling, ensure that you are using the brew version, by placing /usr/local/bin before /usr/sbin in your PATH:

      PATH="/usr/local/bin:$PATH"

PHP71 Extensions will always be compiled against this PHP. Please install them using --without-homebrew-php to enable compiling against system PHP.

✩✩✩✩ PHP CLI ✩✩✩✩

If you wish to swap the PHP you use on the command line, you should add the following to ~/.bashrc, ~/.zshrc, ~/.profile or your shell's equivalent configuration file:
  export PATH="$(brew --prefix homebrew/php/php71)/bin:$PATH"

✩✩✩✩ FPM ✩✩✩✩

To launch php-fpm on startup:
    mkdir -p ~/Library/LaunchAgents
    cp /usr/local/opt/php71/homebrew.mxcl.php71.plist ~/Library/LaunchAgents/
    launchctl load -w ~/Library/LaunchAgents/homebrew.mxcl.php71.plist

The control script is located at /usr/local/opt/php71/sbin/php71-fpm

OS X 10.8 and newer come with php-fpm pre-installed, to ensure you are using the brew version you need to make sure /usr/local/sbin is before /usr/sbin in your PATH:

  PATH="/usr/local/sbin:$PATH"

You may also need to edit the plist to use the correct "UserName".

Please note that the plist was called 'homebrew-php.josegonzalez.php71.plist' in old versions of this formula.

With the release of macOS Sierra the Apache module is now not built by default. If you want to build it on your system you have to install php with the --with-httpd option. See  brew options php71 for more details.

To have launchd start homebrew/php/php71 now and restart at login:
  brew services start homebrew/php/php71
```



