# Convert Markdown to Word with Pandoc
Let's look at how to convert Markdown (.md) files to Word (.docx) using Pandoc.

> Pandoc is a command-line tool and does not have a graphical interface.

At first check if Pandoc is installed on your computer:

   - Open a terminal and run the command: ```brew info pandoc```

If the response says ```not installed```, then Pandoc is not installed.

### Install Pandoc
To install Pandoc, run the following command in the terminal: ```brew install pandoc```

> **Pandoc** is written in **Haskell** and is installed via **brew**, not **pip**.   
> There is a **Python** wrapper called **pypandoc**, but it wraps **Pandoc**.

### Basics of working with Pandoc
After installation, check Pandoc help to get acquainted with its capabilities: ```pandoc --help```

![pandoc --help result.png](image/pandoc/pandoc%20--help%20result.png)

Command structure:

* Enter the command pandoc.
* Specify the required options (the list can be found in the help).
* Upload files for conversion.

### Convert Markdown files to Word
For example, we will convert Markdown files to Word.

To perform the conversion, use the following command:

```pandoc -f markdown -t docx -o <path_to_result.docx> <path_to_source.md>```

Explanation of command parameters:

```-f markdown``` – source file format (Markdown).
```-t docx``` – result format (Word).
```-o``` – path and name of the resulting file.

**Example command:**
```pandoc -f markdown -t docx -o 'docs/Project Setup.docx' docs/Project\ Setup.md```

> Note that in the shell we need to specify a backslash for the md file name so that the terminal will read the command as one argument. You can also wrap the entire document in quotes.

If the file name contains spaces, note:

* Use a backslash \ to indicate a space (e.g. ```Project\ Setup.md```).
* Or wrap the file name in quotes (e.g. ```Project Setup.md```).

> Use Tab to autocomplete file names in the terminal - this will also automatically add the necessary slashes.