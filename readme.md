### My Configurations
----
Every developer's workstation configuration is highly variable and tailored to their  desires + software stack. I tend to spend a chunk of time each month tuning my machine for maximum efficiency, and this is my guide tracking the updates.

This is how I GROK, TRUNK, and LIVE!

### Assumptions
----
* The workstation is running the latest production release of [Apple OSX](http://www.apple.com/osx/).
* The latest release of [Xcode](https://developer.apple.com/xcode/) has been installed with the command line tools.
* [Homebrew](http://brew.sh/) has been successfully installed.
* Running ```brew doctor``` does not report any configuration issues.
* [Google Chrome](http://www.google.com/chrome) is your primary development browser.
* [rbenv](https://github.com/sstephenson/rbenv) is how you're running ruby locally, pre-installed.
* [ruby-build](https://github.com/sstephenson/ruby-build) installed via brew.

### Software
----

* [Atom](https://atom.io/): Atom is a text editor that's modern, approachable, yet hackable to the core—a tool you can customize to do anything but also use productively without ever touching a config file.
* [iterm2](http://www.iterm2.com/#/section/home): iTerm2 is a replacement for Terminal and the successor to iTerm. It works on Macs with OS 10.5 (Leopard) or newer. iTerm2 brings the terminal into the modern age with features you never knew you always wanted.
* [Zsh](http://www.zsh.org/) + [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh): Zsh is a shell designed for interactive use, although it is also a powerful scripting language.
* [Postgres App](http://postgresapp.com/): The easiest way to get started with PostgreSQL on the Mac
* [Autojump](https://github.com/joelthelion/autojump) ```brew install autojump```: Memorizes your favorite locations and allows you to quickly navigate to a path from anywhere in your shell.
* [The Silver Searcher](https://github.com/ggreer/the_silver_searcher) ```brew install the_silver_searcher```: Replaces ack and is by far the fastest search utility I have used.
* [Evernote](http://evernote.com/): For notes and local documentation.
* [Mou](http://mouapp.com/): For editing markdown files.
* [Paw](https://luckymarmot.com/paw): For API testing and construction.
* [Pathfinder](http://cocoatech.com/pathfinder/): For a finder on steroids.
* [Arq + S3](http://www.haystacksoftware.com/arq/): For encrypted cloud backup.
* [Cloak](https://www.getcloak.com/): For cloud based VPN.
* [Dash](http://kapeli.com/dash): For local documentation.
* [Divvy](https://mizage.com/divvy/): For osx window management.
* [Adobe Creative Cloud](http://www.adobe.com/):
For design things, primarily Ai and Photoshop.
* [Alfred](http://www.alfredapp.com/): Alfred is an award-winning app for Mac OS X which boosts your efficiency with hotkeys and keywords. Search your Mac and the web effortlessly, and control your Mac using customised actions with the Powerpack.
  * [Community Workflows](https://github.com/chrishough/myconfigurations/tree/master/software/alfredapp/community.md)
  * [Hough Workflows](https://github.com/chrishough/myconfigurations/tree/master/software/alfredapp/noconformity.md)
* [Keyboard Maestro](http://www.keyboardmaestro.com/main/): The leading software for Mac OS X automation. It will increase business productivity by using macros(or short cuts) with simple keystrokes.
  * [Hough Maestro Macros](https://github.com/chrishough/myconfigurations/tree/master/software/maestro/noconformity.md).
* [iStat Menus](http://bjango.com/mac/istatmenus/): System performance monitoring.

### rbenv plugins
----
* [rbenv-default-gems](https://github.com/sstephenson/rbenv-default-gems): This rbenv plugin hooks into the rbenv install command to automatically install gems every time you install a new version of Ruby.
* [rbenv-gem-rehash](https://github.com/sstephenson/rbenv-gem-rehash): Never run rbenv rehash again. This rbenv plugin automatically runs rbenv rehash every time you install or uninstall a gem.
* [rbenv-vars](https://github.com/sstephenson/rbenv-vars): This is a plugin for rbenv that lets you set global and project-specific environment variables before spawning Ruby processes.
* [rbenv-binstubs](https://github.com/ianheggie/rbenv-binstubs): This plugin makes rbenv transparently aware of project-specific binstubs created by bundler. This means you don't have to type bundle exec ${command} ever again!

### Atom Packages
----
I use the [Inconsolata](http://levien.com/type/myfonts/inconsolata.html) font for development.

Via `Package Control` these are my favorite packages:  

![atom-package-list](https://github.com/chrishough/myconfigurations/raw/master/graphics/atom/atom-package-list.png)

### Shell Theme
----
![shell-theme-example](https://github.com/chrishough/myconfigurations/raw/master/graphics/shell-screenshots/shell-theme-example.png)

Download the [Base16 iTerm2](https://github.com/chriskempson/base16-iterm2) colors, and import them under the colors panel in iterm2 preferences. My theme uses ```base16-railscasts.dark``` which can be loaded in the presets.  You will need to set the contrast as shown to have a clearer definition of the font icons.

![shell-theme-iterm-colors-example](https://github.com/chrishough/myconfigurations/raw/master/graphics/shell-screenshots/shell-theme-iterm-colors-example.png)

Under the terminal tab, make sure to change the report terminal type to ```xterm-256color``` and your character encoding to ```Unicode (UTF-8)```.

![shell-theme-iterm-terminal-example](https://github.com/chrishough/myconfigurations/raw/master/graphics/shell-screenshots/shell-theme-iterm-terminal-example.png)

The background image I created can be found [here](https://github.com/chrishough/myconfigurations/raw/master/graphics/terminal-background.png).  Once attached as the background you will notice a red box around your shell window.  
![shell-theme-iterm-window-example](https://github.com/chrishough/myconfigurations/raw/master/graphics/shell-screenshots/shell-theme-iterm-window-example.png)

### New Machine Checklist
----
0. files migrated, software installed, all software setups in place
1. setup xcode + command line tools
2. install homebrew, and update homebrew
3. brew install git
4. brew install autojump
5. brew install the_silver_searcher
6. brew install postgres
7. brew install nvm
8. brew install direnv
9. install postgresapp from postgresapp.com
10. copy ~/.gitconfig and ~/.ssh to new computer
11. verify git works by cloning git .myconfigurations
12. download and install iterm2, set auto check for updates
13. install .oh-my-zsh
14. brew install zsh
15. ```chsh -s /bin/zsh``` to set zsh as the default shell
16. in iterm2 change the default background to my terminal-background.jpg
17. download and install the inconsolata font
18. download and install atom
19. install atom plugins
20. setup atom theme, keymap.cson, and config.cson files
21. backup current settings file by running ruby settings/backup.rb
22. brew install rbenv ruby-build
23. make sure each dotfile exists, if it does not create it
24. symlink the current dotfiles to the git versions via ruby settings/symlinks.rb
25. setup my shell theme
26. install rbenv plugins
27. make sure to setup rbenv vars
28. run brew doctor to make sure there are no errors
29. install rbenv versions
30. install [java](http://support.apple.com/kb/DL1572)
31. cd into scripts and run ruby backup.rb
32. cd into scripts and run ruby symlinks.rb

...*Time to drink beer!*

![open-source-projects.jpeg](https://github.com/chrishough/myconfigurations/raw/master/graphics/open-source-projects.jpeg)
