# WordFinder

## Usage

```
python wordfinder.py
```

This will create an `outfile.csv` in your working directory of the discovered words. 

#### Optional Directory Argument

Optionally, pass in the directory you would like to search.

For example:

```
python wordfinder.py ~/code
```

## Dependencies

You must have [ripgrep](https://github.com/BurntSushi/ripgrep) and python installed. The script works on both python2 and 3, and does not require any other dependencies.

Ripgrep was chosen because of its speed. To install ripgrep:

```
brew install ripgrep
```


#### Troubleshooting ripgrep

Note: recursively searching your current working directory is the default mode of operation for ripgrep.

If you see an error message from ripgrep saying that it didn't search any files, then re-run ripgrep with the --debug flag. One likely cause of this is that you have a * rule in a $HOME/.gitignore file.
 
#### Ripgrep References  

[https://github.com/BurntSushi/ripgrep/blob/master/GUIDE.md](https://github.com/BurntSushi/ripgrep/blob/master/GUIDE.md)

## Future work

Please make PRs! And add to the issues section.