# OpenArabic Project (@ AvH Lehrstuhl für Digital Humanities, U Leipzig)

Arabic texts from different periods, collected and reformatted into machine-readable formats (mARkdown > CTS-compliant TEI XML > Perseus DL)

Currently uploaded texts are converted automatically into [*mARkdown*](http://maximromanov.github.io/mARkdown/) format and require further manual tagging of the structure; when manual tagging is complete they will be converted into CTS-compliant XML format.

For the list of added books, see **report.md** (Mostly premoderns chronicles, biographical collections, encyclopaedic dictionaries, gazetteers).

# Text Description Tags

Tags follow the URI of a text in the following format **(TAGS: TAG,TAG,TAG)**. Combinations of tags specify the description of the text, for example, **BIO** refers to 'a biographical text', but **BIO,COL** refers more specifically to 'a biographical collection'. 

* **BIB** : bibliographical
* **BIO** : biographical
* **CHR** : chronicle
* **COL** : collection/dictionary
* **GEO** : geographical
* **ONO** : onomastic

# Project/Folder structure

- everything is divided into centuries
- each century includes `data` folder
- `data` folder includes `author` folders
- `author` folders include `title` folders
- `title` folders include:
	- texts (often different versions)
	- `arc` folder, where texts are preserved in their pre-formatted form
	- `PDF` folder, which include:
		- **urls.txt** with links to PDFs of a book (usually on [archive.org](archive.org))
		- PDFs can be downloaded with `wget -i urls.txt` (on commandLine/Terminal)
		- on Mac/Linux all PDFs can be also downloaded with `make` command
		- `wget` must be installed on Windows (Macs usually have it)
		- to save space, PDFs are ignored in this GitHub repository 
		- if you find new PDFs, add urls (one per line) into a new file **urls_additional.txt**
