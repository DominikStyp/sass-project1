# Setup live SASS compiler in PHPStorm
- Make sure you have last NodeJS version
- Install SASS plugin
  ```
  npm install -g sass
  ```
- If you want to use LESS install it also
  ```
  npm install --global less
  ```
- Click CTRL+ALT+S (Settings)
- Go to: Tools -> File Watchers
- Setup SASS Watcher with following settings
  - Arguments 
    ```
    $FileName$:$FileParentDir$/../public/css/$FileNameWithoutExtension$.css
    ```
  - Output paths to refresh
    ```
    $FileParentDir$/../public/css/$FileNameWithoutExtension$.css:$FileParentDir$/../public/css/$FileNameWithoutExtension$.css.map
    ```
  - Program should be set up automatically as absolute path to NodeJS program
    ```
    sass.cmd
    ```
  PHPStorm Help: <a href="https://www.jetbrains.com/help/phpstorm/transpiling-sass-less-and-scss-to-css.html">How to setup SASS Compiler</a>