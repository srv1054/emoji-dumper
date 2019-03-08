# emoji-converter

This go program will take a command line parameter of `-p` specifying the path to a directory of slack emoji's.
The assumption is made that:
- Emoji's are already 128x128 in size
- Files are all .jpg, .gif or .png
- Filenames will become the :emoji: name inside slack

The output from emoji-convert is a .JSON file formatted correctly for https://github.com/jackellenberger/emojme to slurp it in and upload it with your personal Slack Token.

**Check releases for latest binaries** https://github.com/srv1054/emoji-dumper/releases

emoji-convert format:
`dump -p /my/path/to/all/emojis`

This creates a json file called `output.json` with all the pathing in it

emojme format:
`node emojeme.js upload --subdomain <your slack domain name> --token <your slack token xoxs-xxx> --src output.json`

