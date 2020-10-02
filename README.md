# WordFinder 🔍

## Philosophy

Searching for words through the GitHub UI is slow and limits how you can prioritize occurrences. Let's have a standardized, lightweight script that outputs an .csv, which you can then sort by file extension, codebase, or priority.

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

## Sample CSV output

| Root_Directory | File_Path                    | Line_Number | Snippet                        | Priority | Searched_Word | File_Extension |
|----------------|------------------------------|-------------|--------------------------------|----------|---------------|----------------|
| codebase       | ~/codebase/components/foo.js | 3           | myString = "I bought an apple" | 1        | apple         | .js            |
| codebase2      | ~/codebase2/script.rb        | 104         | DOG_CONSTANT: "woof"           | 2        | dog           | .rb            |

## Dependencies

You must have [ripgrep](https://github.com/BurntSushi/ripgrep) and python installed. The script works on both python2 and 3, and does not require any other dependencies other than ripgrep.

Ripgrep was chosen because of its blazing fast speed. To install ripgrep:

```
brew install ripgrep
```

#### Troubleshooting ripgrep

Note: recursively searching your current working directory is the default mode of operation for ripgrep, and in turn, wordfinder.py.

It's unlikely, but if you were expecting to find occurrences but did not, it's possible ripgrep didn't search any files because you have a * rule in a $HOME/.gitignore file. (ripgrep ignores .gitignore files by default.) You can fix this by adding the `--debug` flag to the ripgrep command sequence itself.

#### Ripgrep References  

[https://github.com/BurntSushi/ripgrep/blob/master/GUIDE.md](https://github.com/BurntSushi/ripgrep/blob/master/GUIDE.md)

## Future work

Please give feedback and make PRs! Also, checkout the issues section.
