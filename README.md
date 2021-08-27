# goph-to-stylesheet
goph-to-stylesheet supports conversion from goph to any file format.

## Synopsis
```bash
goph-to-stylesheet [-t goph_theme] [-i input_file] [-o output_file]
```

## Options
- `-t --theme`
    - Enter the name of the Goph theme
    - You can find the Goph theme [here](https://mayccoll.github.io/Gogh/)
- `-i --input`
    - Enter the template file
    - Colors can be set in the template file using `[[ COLOR ]]`
        - `COLOR` can be any of the following colors defined in Goph
            - `black` , `red` , `green` , `yellow` , `blue` , `purple` , `cyan` , `white` , `brightBlack` , `brightRed` , `brightGreen` , `brightYellow` , `brightBlue` , `brightPurple` , `brightCyan` , `brightWhite` , `foreground` , `background` , `cursorColor`
        - The specified color will be replaced by the HEX color code defined in Goph
        - See [template/shell.scss](template/shell.scss) for details
- `-o --output`
    - Enter the output file
    - Not only style sheets(.css, .scss), but also text files can be specified.

## Example
If you want to use the "3024Day" theme in Goph with [Yukuro/hugo-theme-shell](https://github.com/Yukuro/hugo-theme-shell)
```bash
goph-to-stylesheet -t 3024Day -i template/shell.scss -o goph.scss
```