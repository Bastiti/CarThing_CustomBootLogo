# CarThing_CustomBootLogo

## Requirements:
* Python 2.7
* Spotify Car Thing
* Picture Editing software
### Clone aml-imgpack
```bash
git clone https://github.com/steeve/aml-imgpack
```

### Clone superbird-bulkcmd
```bash
git clone https://github.com/frederic/superbird-bulkcmd
```

## How to create your custom logo ?
- Copy hacked_logo.img into aml-imgpack folder.
- Run the command:
```bash
python3 aml-imgpack.py --unpack hacked_logo.img
```
- Modify bootup_spotify.bmp using your favorite image editor (GIMP, ...)
- Export the picture in 16bits color mode
- Pack the .img file
```bash
python3 aml-imgpack.py --pack logo.img *.bmp
```
- Move logo.img into superbird-bulkcmd/images
- Modify superbird-bulkcmd/scripts/hacked_logo.sh, change hacked_logo.img to logo.img
- In superbird-bulkcmd folder, run:
```bash
./scripts/hacked_logo.sh
```
- Enjoy
