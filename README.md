# OpenArabic Project (@ AvH Lehrstuhl für Digital Humanities, U Leipzig)

Arabic texts from different periods, collected and reformatted into machine-readable formats (mARkdown > CTS-compliant TEI XML > Perseus DL)

Currently uploaded texts are converted automatically into *mARkdown* format and require further manual tagging of the structure; when manual tagging is complete they will be converted into CTS-compliant XML format.

For the list of added books, see **report.md** (Mostly premoderns chronicles, biographical collections, encyclopaedic dictionaries, gazetteers).

# Book folder structure

- `data` has subfolders by authors, which have subfolders by titles
- each title subfolder has `PDF` subfolder:
	- **urls.txt**: includes links to PDFs of a book (usually on archive.org)
	- on Mac/Linux all PDFs can be downloaded by typing `make` in Terminal/CommandLine
	- on Windows: `wget` must be installed; then run `wget -i urls.txt`
	- to save space, PDFs are ignored in this GitHub repository 
	- if you find new PDFs, add urls (one per line) to **urls_additional.txt**
