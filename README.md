# MergeCrunch

***

## Description

MergeCrunch is a small bash script that combine youtube-dl and mkvmerge for get anime.

The main feature is to generate a mkv file with all availables soft-subtitles and fonts attachment of downloaded files from **Crunchyroll** streaming.

Tested in Ubuntu 14.04

## Dependencies

You must have installed youtube-dl and mkvmerge, as minimum.

Rhash is recommended for can calculate CRC32 hash sum.

For get this dependencies, execute the classic sudo apt-get install.

```sh
sudo apt-get install youtube-dl
sudo apt-get install mkvtoolnix
sudo apt-get install rhash
```

For solve fonts text dependencies, create a folder in your home dir called ~/.fonts and put here any font text missing.
When you run this script, mkvmerge needs fonts text installed previous in your system for able to add it as attachment.

## Usage

For this section, I ilustrate how to use it with examples:

**Basic example (argument -i):**
```sh
./mergecrunch.sh -i URL_CRUNCH_HERE
```
Episode will be downloaded with max resolution in the current directory

**CRC32 example (argument -c):**
```sh
./mergecrunch.sh -i URL_CRUNCH_HERE -c
```
Same top, but now CRC32 will be calculated and stored in the filename.

**Format example (argument -f):**
```sh
./mergecrunch.sh -i URL_CRUNCH_HERE -c -f 720p
```
Same top, but now resolution will be 1280x720. Be careful with this argument. Check before your available resolution with:
```sh
 youtube-dl -F URL_CRUNCH_HERE
```

**Prefered language (argument -s):**

Using a prefered language, you set a default subtitle track in your mkv. Also, title description and default output filename are set according to language.

```sh
./mergecrunch.sh -i URL_CRUNCH_HERE -c -f 720p -s esES
```
Same top, but now I set spanish subtitle track as prefered.  Also, default output filename will be in spanish.

Argument -s only admit this values:
- "enUS" for  English.
- "esES" for Spanish Castillian.
- "esLA" for Spanish Mejicano.
- "frFR" for force Français.
- "itIT" for force Italiano.
- "ptBR" for force Português.
- "deDE" for force Deutsch.
- "arME" for force العربية


**Output file name (argument -o):**
```sh
./mergecrunch.sh -i URL_CRUNCH_HERE -c -f 720p -s esES -o 'Sket Dance 01.mkv'
```
Same top, but now output file will renamed as "Sket Dance 01 [CRC32_HERE].mkv"

## FEEDBACK, BUGS OR CONTRIBUTION
- If you need help, I will be glad to help.
- Report errors is great! Do it, please.
- If you want help with something, I will hear you :)

## LICENSE
GNU General Public License v2.0