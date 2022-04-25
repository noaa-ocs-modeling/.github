## Changing the color scheme of the command window
### 1. Download the latest Microsoft release of ColorTool
https://github.com/microsoft/terminal/releases/tag/1904.29002
extract the ZIP archive to a directory of your choice
### 2. From the console of your choice, navigate to the directory where you extracted the ZIP archive
#### WSL:
```bash
cd /mnt/c/Users/Zachary.Burnett/Downloads/ColorTool
```
#### cmd:
```cmd
cd C:\Users\Zachary.Burnett\Downloads\ColorTool
```
### 3. Display available themes
```bash
./ColorTool.exe -s
```
![image](https://user-images.githubusercontent.com/52422935/109822209-be56b900-7c04-11eb-80f4-1cd68b90d98e.png)
### 4. Set the desired theme
```bash
./ColorTool.exe -x schemes/solarized_dark.itermcolors
```
![image](https://user-images.githubusercontent.com/52422935/109822373-e1816880-7c04-11eb-995d-276f4d0ff299.png)

## Using `zsh` instead of `bash`
### install `zsh` with the `oh-my-zsh` installer
```bash
sh -c "$(wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"
```
### add a newline to your prompt (optional)
add the following lines to the end of your `~/.zshrc` file
```bash
prompt_end() {
  if [[ -n $CURRENT_BG ]]; then
    print -n "%{%k%F{$CURRENT_BG}%}$SEGMENT_SEPARATOR"
  else
    print -n "%{%k%}"
  fi

  print -n "%{%f%}"
  CURRENT_BG=''

  #Adds the new line and ➜ as the start character.
  printf "\n ➜";
}
```
