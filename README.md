# Move-Songs

## Description

A simple script written in python to sort music files (.mp3, .flac, .m4a) into folders based on their metadata. Artist, Year, Album, Song  

I mainly use it to sort and move music from my downloads folder to my music folder

## Dependencies

- python 3.10
- mutagen   
`pip install mutagen`

## Usage

```
usage: move-songs [-h] [-y] [-a] [-s] [-t TARGET_DIR] start-dir

Sort music files by metadata

positional arguments:
  start-dir             Directory of the unsorted music files

options:
  -h, --help            show this help message and exit
  -y, --year            sort by year
  -a, --album           sort by album
  -s, --song            add each song to its own folder
  -t TARGET_DIR, --target-dir TARGET_DIR
                        Directory where the files will be
                        sorted
```

Songs are always sorted by artist and (optionally) by Year, Album, Song in that order.  
If the user doesn't provide a target directory where the files will be moved and sorted, they will be sorted inside the starting directory

## Install

You can clone this repository
```
git clone https://github.com/HliasOuzounis/move-songs.git
```
and run the script from inside the folder
```
cd move-songs
move-songs [-h] [-y] [-a] [-s] [-t TARGET_DIR] start-dir
```
or alternatively move the script to a directory in the PATH so you can run it from anywhere

## Troubleshooting

It's possible that some of your songs don't have correct metadata or it's missing. Unfortunately I can't do anything about that and they will not be sorted correctly :(  
You can check the metadata of any song with
```
ffprobe [path to file]
```

## TODO

- recursively search for songs in the starting dir
- fix any bugs that may appear
- more sorting options (maybe genre)  

### Forks and merges are welcome