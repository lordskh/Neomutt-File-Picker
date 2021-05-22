# NeomuttFilePicker
Attach files to your emails in [NeoMutt](https://github.com/neomutt/) using [Ranger](https://github.com/ranger/ranger), [Vifm](https://github.com/vifm), or [nnn](https://github.com/jarun/nnn) as your file manager.

This script is based on the [this topic](https://www.reddit.com/r/commandline/comments/cbxvdf/combine_neomutt_with_ranger/) and improved to allow attaching mulptiple files with spaces in the name and path.

## Usage
1. Make the script executable with `chmod +x mutt_filepicker`
2. Copy the `mutt_filepicker` file to somewhere in your `$PATH`
3. Add the following line to your `.muttrc` so that you can attach files with `A`

```
macro compose A "<shell-escape>mutt_filepicker<enter><enter-command>source /tmp/muttattach<enter><shell-escape>mutt_filepicker clean<enter>" "Attach with your file manager"
```
3. Now, on the email sending screen (when you already wrote the text and saved it) type `A` instead of standard `a` to call the script. The file manager should appear. Choose files that you want to attach (tag them if multiple files) and hit Enter. Hit Enter twice more when asked. 

## Settings
In the `mutt_filepicker` file you can choose which file manager to use by commenting/uncommenting. 
