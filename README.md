# OpenArabic Project (@ AvH Lehrstuhl für Digital Humanities, U Leipzig, led and curated by Maxim Romanov)

**Short description**: a short description goes here — what, who, why, etc.

**Team**: ... 



# Contents

- [General Description](#general-description)
- [Prospects and Progress](#prospects-and-progress)
- [Text Description Tags](#text-description-tags)
- [Folder structure](#folder-structure)
- [General description of the workflow with mARkdown](#general-description-of-the-workflow-with-markdown)
- [Status Report](#status-report)
- [List of books by centuries (626 titles)](#list-of-books-by-centuries-626-titles)
- [Statistics on the corpus](#statistics-on-the-corpus)
- [Summary statistics on the lengths of texts in the corpus](#summary-statistics-on-the-lengths-of-texts-in-the-corpus)
- [Texts by length (duplicates excluded)](#texts-by-length-duplicates-excluded)
- [Texts in chronological order (duplicates excluded)](#texts-in-chronological-order-duplicates-excluded)
- [Themes and Genres Report](#themes-and-genres-report)




## General Description

The goal of the project is to build a machine-actionable corpus of premodern texts in Arabic to encourage computational analysis of Arabic literary tradition. Currently, most of the text are historical texts (chronicles, biographical collections, geographical treatises and gazetteers, thematic dictionaries); if you are interested in having other genres and forms, please, get in touch with us.

Most of the texts are coming from open online collections of premodern and modern Arabic texts, such as [http://shamela.ws/](http://shamela.ws/) and [http://shiaonlinelibrary.com/](http://shiaonlinelibrary.com/) (These texts have `Shamela+NUMBER` and `Shia+NUMBER`; some texts are coming from _al-Jāmiʿ al-kabīr_, which has been published on an external HDD and is not available online (`JK+NUMBER`). Initial metadata from these collections is preserved in the beginning of each file.

Currently uploaded have been automatically converted from their initial formats into `mARkdown` format—a flavor of `markdown` for tagging premodern Arabic text; they all require further editing, so that the structure of each text is tagged properly; the detailed description of `mARkdown` scheme and the tagging workflow can be found [http://maximromanov.github.io/mARkdown/](http://maximromanov.github.io/mARkdown/). When manual tagging is complete text will be converted into CTS-compliant XML format.

For the list of added books, see below (Mostly premodern chronicles, biographical collections, encyclopaedic dictionaries, gazetteers).

## Prospects and Progress

| *Texts* | *Status* |
|:--- | ------:|
| Total in the Collection | 10,393 |
| Unique texts | 7,781 |
| Added texts (listed below) | 626 |
| Orphans (no TXT) | 2 |

| *Texts* | *Status* |
|:--- | ------:|
| In Progress (`.inProgress`) | 5 |
| Tagged (`.completed`) | 41 |
| Vetted (`.mARkdown`) | 4 |
| Converted to TEI XML  (`.xml`) | _pending_ |


## Text Description Tags

Tags follow the URI of a text in the following format `(TAGS: TAG,TAG,TAG)`. Combinations of tags specify the description of the text, for example, `BIO` refers to 'a biographical text', but `BIO,COL` refers more specifically to 'a biographical collection'. 

*****************************
* `BIB` : bibliographical
* `BIO` : biographical
* `CHR` : chronicle
* `COL` : collection, dictionary, anthology
* `GEN` : genealogical
* `GEO` : geographical
* `ONO` : onomastic
* `HAD` : hadith

*****************************
* `SHC` : a Šīʿī text

*****************************
* `DHB` : ‘al-Ḏahabī Corpus’—his sources _&_ his books 
* `ORPHAN` : _no text_, orphan

*****************************
**NB**: Title descriptions also have temporary tags (they start with `_`, an undescore), which are generated and updated automatically from the initial metadata. These tags are usefully suggestive, but not entirely reliable.



## Folder structure

- everything is divided into centuries
- each century includes `data` folder
- `data` folder includes `author` folders
- `author` folders include `title` folders
- `title` folders include:
	- texts (often different versions)
	- `arc` folder, where zipped texts are preserved in their pre-formatted form
	- `PDF` folder, which include:
		- **urls.txt** with links to PDFs (for about 125 books), mostly on [archive.org](archive.org)), which can be downloaded with `wget -i urls.txt` (on 'command line' or 'Terminal')
			- on Mac/Linux all PDFs can be also downloaded with `make` command
			- `wget` must be installed on Windows (Macs usually have it)
		- to save space, PDFs are ignored in this GitHub repositories 
		- if you find new PDFs, add urls (one per line) into a new file **urls_additional.txt**. PDFs can be found via Google, most commonly on the following websites:
			- [http://waqfeya.com/](http://waqfeya.com/), with most links lead to [archive.org](archive.org)); other useful sites are:
			- [http://kt-b.com/](http://kt-b.com/) (books are often bulked into large collections, but the selection seems to be larger than on [http://waqfeya.com/](http://waqfeya.com/));
			- [http://bib-alex.com/](http://bib-alex.com/), which has scanned books from the Bibliotheca Alexandrina (unfortunately, most files are stored on file-sharing services and lots of links are already dead)
			- [http://wqf.me/](http://wqf.me/) for manuscripts (search is rather complicated though); most links lead to [archive.org](archive.org) as well.



## General description of the workflow with mARkdown

0. Have Github installed and setup on your computer.
	1. Create a github account if you do not have one
	2. You will be added to the `OpenArabic` organisation (email me your `username`)
	3. Install `github` software on you machine
		1. On Mac: it is likely to be installed already (try `git` in Terminal)
		2. On Windows: `github` for Windows comes with the interface (Github) and with the Powershell terminal (`Git shell`). First open the interface and login into `github` there; go through the setup steps; close the interface. Now open `Git shell`
		3. It will help to know a couple of general commands, but `cd path` is the main one (https://en.wikipedia.org/wiki/Cd_(command)):
		4. Using `cd` command go to your github folder (on Windows you can select on in the Interface mode and it will become the forlder that will open automatically when you open `git shell`)
		5. Main git commands in command line are the same in Mac's `Terminal` and in Windows' `Powershell`):
			* `git clone link` clones a repository from www.github.com to your machine. For example, `git clone https://github.com/OpenArabic/0700AH.git` will make a copy of the `0700AH` repository on you machine.
			* type `cd 0700AH` to get into the folder of the cloned repository
			* `git status` prints the current status of the repository on the screen, showing if there are any changes (new files, changed files, deleted files, etc.)
			* `git pull origin master` pulls---or copies---updates from the online repository to your machine; run this command to ensure that you have the latest version on your machine.
			* after you changed/added files, run `git add .` (period/punkt/point at the end); this command adds all new files to the repository.
			* `git commit -m "MESSAGE"` saves the current status of the repository to the git versioning system; MESSAGE contains your own human readable description of what you have done. For example, if you finished tagging 3 volumes in the book that has 10, you can do `git commit -m "Finished tagging first 3 volumes of ZZZ"`, where `ZZZ` is the URI of the book you work on (please, include only the `DateAuthor.Title` part, i.e. if the complete URI is `0310Tabari.Tarikh.JK000157-ara1.mARkdown`, you should include only `0310Tabari.Tarikh`). These messages will be visible in github repository online and help tracking progress. Also, you can roll back to the committed stage, if something wrong goes with the repository.
			* `git push origin master` will upload your changes to the online repository. If somebody else has already updated the same repository, you may need to run `git pull origin master` first.
1. Clone repositories; either work with the texts of your interest, or with the ones that are assigned to you.
3. Make sure that nobody else is editing the text that you chose; to avoid that keep me posted on text you are planning to work with. **NB**: if there is a file has one of the following extensions—`.inProgress`, `.completed`, `.mARkdown`, it means that somebody is working on that text!
	* Files can have the following extensions:
		* Initially, there is no extension: the names of all text files end with `-ara1`, which is a part of the file-naming CTS-scheme; extensions were not added deliberately in order to avoid accidental opening of files by default programs: on Windows the default text editor is `Notepad`, which cannot handle large files and will freeze the system.
		* `.inProgress` : if a file has this extension, it means somebody is actively working on it, tagging logical units.
		* `.completed` : the tagging is complete, but has not been vetted yet.
		* `.mARkdown` : the file has been vetted and is ready for conversion to TEI XML and can be used for computational analysis.
4. In most cases there are multiple versions of the same text; you need to identify relevant editions and do a preliminary evaluation.
5. Ideally,  you should be able to find a text that corresponds to an edition,  which you can access (scans of most editions can be found online; links to some editions can be found in the PDF folder in text repositories; if there are links in `urls.txt`, they can be downloaded in batch using `wget`, by running `wget -i url.txt` (while in PDF folder); this program comes preinstalled on Macs, but has to be downloaded on Windows). 
6. It is likely that there will be more than one text based on the same edition. `Shamela` texts are often improved versions of `JK` texts (with more tags already in place);  it makes sense to compare the number of tags already in place and choose the text that will require less time to finish. Keep in mind that there is no solid rule about which text is likely to be better; you need to evaluate them all.
7. **Only one text** should be converted into `mARkdown`—the text that according to your evaluation is of better/best available quality. Make sure to record your observations on each text file into a `README.md` file in the folder with the text group you are working on (answer the questions that are in the `text_questionnaire.md` file; this file will be updated periodically).
 	* __NB__: If your research focuses on specific texts, you may want having multiple editions converted into `.mARkdown`; this will allow to compare how editions are different from each other.
8. When you selected the text that you will be converting to `mARkdown`, work with the copy of that text file. The file name of that copy should retain the `URI` + `.inProgress` (period + inProgress,  where the third letter is capitalized!). For example, `0310Tabari.Tarikh.JK000157-ara1` > `0310Tabari.Tarikh.JK000157-ara1.inProgress`. Make sure that the `URI` is not broken: when you make a copy of a file on Windows, it will insert `- Copy` in the middle on the filename; make sure to remove this.
	* __NB__ by default, Windows hides file extensions, so you will need to change some settings so that they are displayed. *How to do that*: 1) Open `File explorer` (Win+E); 2) press `F10` to see the menu; 3) in the menu: `Tools` > `Folder options`; then choose tab `View`; then uncheck `Hide extensions for known file types`; 4) Click `Apply to Folders`, then `Ok`.
9. When you start working on a file, you add extension `.inProgress`, which will indicate to others that the file is been processed. After you renamed the file, make sure to stage your progress and push the changes to the online repository so that others could see your progress. Run the following commands in git:
	* `git add .`
	* `git commit -m "Started working on ZZZ"` (where `ZZZ` is the URI of the book you work on (please, include only the `DateAuthor.Title` part, i.e. if the complete URI is `0310Tabari.Tarikh.JK000157-ara1.mARkdown`, you should include only `0310Tabari.Tarikh`).
	* `git push origin master`
	* **NB:** Before you start a new text, make sure to pull the latest changes to the repository, i.e., run `git pull origin master`
9. Keep in mind that you need to tag only the structure of a book you are working with,  which includes tagging chapter headers (`### |`, `### ||`, `### |||`, etc.) and major information units, like biographies (`### $`, `### $$`, `### $$$`, etc.) or lexicon items (these we should discuss before you start). Please, do not tag anything else—at least without consulting with me first.
10. **IMPORTANT!** Do not delete anything from the text! At this point we do not know what is valuable and what is not (things like numbers, random characters, punctuation, stray HTML tags, etc.). **Your goal is to provide the structure to texts, not to edit them**. If you think something should be deleted, please, consult me first. Time is the most valuable asset at the moment and we cannot afford to spend it on fixing messed-up texts; we want to invest it into tagging logical units of as many new texts as possible.
10. Make commits to relevant github repositories after each working session. In addition to saving/backing up your work, this will also allow me to check periodically on your progress and make suggestions along the way.
11. When you have finished tagging a text, change its extension from `.inProgress` to `.completed`; then push your changes to the online repository.\* After that I will review the tagging and if everything is fine, I will change the extension to `.mARkdown`, which will indicate that the tagging of the file has been complete and vetted.
	* Git commands:
		* `git add .`
		* `git commit -m "tagging of ZZZ is complete"` (where `ZZZ` is the URI of the book you work on (please, include only the `DateAuthor.Title` part, i.e. if the complete URI is `0310Tabari.Tarikh.JK000157-ara1.mARkdown`, you should include only `0310Tabari.Tarikh`).
		* `git push origin master`
	* **NB:** The extensions are important as they allow everyone to see at which stage the files are; they are also used to generate the progress report, which will be included into the `README.md` file of each repository. 
11. Into the `README.md` which is in the same folder as the text file you are working on, please add the number of hours it took you to process the file. We are trying to get estimates on how much time it is going to take to process the entire corpus; we also know at the moment that the amount of time is not proportional to the length of a text, since what matters most is how much structural information is preserved in the initial file and that differs drastically from text to text.

These are the major steps.  Please, do not hesitate to contact the me if you have any questions, no matter how insignificant they may seem to you.



## Status Report
 
* 50 titles
* 28,293,672 words
* 130,688 logical units
* 108,771 bios

### `*.inProgress` (5 titles: 7,728,642 words; 33,212 units; 24,351 bios)

- `0230IbnSacd.TabaqatKubra (920,980 words; 6,386 units; 4,081 bios)`
- `0256Bukhari.TarikhKabir (519,629 words; 15,061 units; 10,845 bios)`
- `0310Tabari.JamicBayan (2,850,544 words; 0 units; 0 bios)`
- `0310Tabari.Tarikh (1,468,698 words; 554 units; 0 bios)`
- `0764Safadi.WafiBiWafayat (1,968,791 words; 11,211 units; 9,425 bios)`


### `*.completed` (41 titles: 19,238,656 words; 84,474 units; 72,439 bios)

- `0292Yacqubi.TarikhYacqubi (192,205 words; 139 units; 0 bios)`
- `0355MuhammadKindi.WulatMisr (50,870 words; 131 units; 128 bios)`
- `0369AbuShaykhIsbahani.TabaqatMuhaddithin (110,658 words; 1,098 units; 356 bios)`
- `0379MuhammadRabci.TarikhMawlidCulama (35,122 words; 301 units; 301 bios)`
- `0390Muqaddasi.AhsanTaqasim (103,553 words; 67 units; 0 bios)`
- `0403IbnFaradi.TarikhCulamaAndalus (118,911 words; 1,977 units; 1,653 bios)`
- `0405HakimNaysaburi.TalkhisTarikhNaysabur (32,641 words; 2,522 units; 2,509 bios)`
- `0412Sulami.TabaqatSufiya (68,554 words; 193 units; 186 bios)`
- `0427HamzaJurjani.TarikhJurjan (106,677 words; 1,357 units; 1,193 bios)`
- `0430AbuNucaymIsbahani.HilyaAwliya (1,188,077 words; 678 units; 674 bios)`
- `0430AbuNucaymIsbahani.TarikhIsbahan (228,661 words; 1,959 units; 1,890 bios)`
- `0442Tanukhi.TarikhCulamaNahwiyyin (10,765 words; 95 units; 95 bios)`
- `0446AbuYaclaKhalili.IrshadFiMacrifaCulama (81,543 words; 994 units; 921 bios)`
- `0450Najashi.Rijal (88,987 words; 1,330 units; 1,268 bios)`
- `0458Bayhaqi.DalailNubuwwa (528,431 words; 678 units; 0 bios)`
- `0460ShaykhTusi.IkhtiyarMacrifaRijal (224,038 words; 416 units; 416 bios)`
- `0460ShaykhTusi.Rijal (75,644 words; 6,745 units; 6,428 bios)`
- `0463IbnCabdBarr.IsticabFiMacrifaAshab (397,653 words; 4,049 units; 3,612 bios)`
- `0463KhatibBaghdadi.TarikhBaghdad (1,883,359 words; 8,484 units; 7,838 bios)`
- `0466CabdAzizKattani.DhaylTarikhMawlidCulama (18,115 words; 463 units; 352 bios)`
- `0476AbuIshaqShirazi.TabaqatFuqaha (30,392 words; 508 units; 437 bios)`
- `0482AbuIshaqHabbal.WafayatMisriyyin (6,616 words; 497 units; 420 bios)`
- `0521IbnAbiYacla.TabaqatHanabila (169,915 words; 880 units; 703 bios)`
- `0524IbnAkfani.DhaylDhaylTarikhMawlidCulama (4,082 words; 84 units; 63 bios)`
- `0544CiyadIbnMusaYahsubi.TartibMadarik (320,968 words; 1,177 units; 1,020 bios)`
- `0555IbnQalanisi.Tarikh (120,986 words; 157 units; 4 bios)`
- `0565IbnZaydBayhaqi.TarikhBayhaq (121,031 words; 299 units; 139 bios)`
- `0571IbnCasakir.TarikhDimashq (8,193,674 words; 10,910 units; 9,641 bios)`
- `0577IbnAnbari.NuzhaAlibba (43,678 words; 183 units; 181 bios)`
- `0578IbnBashkuwal.Sila (139,358 words; 1,724 units; 1,543 bios)`
- `0597IbnJawzi.Muntazam (1,529,901 words; 7,351 units; 4,331 bios)`
- `0600KatibMarrakushi.Istibsar (60,658 words; 200 units; 130 bios)`
- `0626YaqutHamawi.MucjamBuldan (1,273,690 words; 13,668 units; 12,973 bios)`
- `0630IbnAthirCizzDin.LubabFiTahdhibAnsab (339,004 words; 5,168 units; 4,592 bios)`
- `0658IbnAbbar.HullaSiyara (98,490 words; 228 units; 216 bios)`
- `0658IbnAbbar.TakmilaLiSila (303,300 words; 3,925 units; 3,580 bios)`
- `0658IbnAbbar.TuhfaQadim (28,899 words; 114 units; 113 bios)`
- `0685IbnCibri.TarikhMukhtasarDuwal (97,240 words; 234 units; 0 bios)`
- `0748Dhahabi.CibarFiKhabar (270,948 words; 868 units; 0 bios)`
- `0774IbnKathir.TabaqatShaficiyyin (180,888 words; 965 units; 919 bios)`
- `0900AbuCabdAllahHimyari.RawdMictar (360,474 words; 1,658 units; 1,614 bios)`


### `*.mARkdown` (4 titles: 1,326,374 words; 13,002 units; 11,981 bios)

- `0276IbnQutaybaDinawari.AdabKatib (69,366 words; 299 units; 0 bios)`
- `0681IbnKhallikan.WafayatAcyan (677,511 words; 1,528 units; 862 bios)`
- `1339IsmacilBashaBaghdadi.HadiyaCarifin (421,313 words; 8,842 units; 8,814 bios)`
- `1450MawsucaShicriya.MucjamShucara (158,184 words; 2,333 units; 2,305 bios)`




# Text currently included in the Coprus

## List of books by centuries (626 titles)


* **0100AH [[ [Re]generated on 2016-08-29 (16:53:58) ]]**

 * _no texts at the moment_

* **0200AH [[ [Re]generated on 2016-08-29 (16:53:58) ]]**

 * `0110HasanBasri.FadailMakka `
	- *TAGS: CENT0200, PPE, _AJZA, _BULDAN, _HADITH, _TABAQAT, _TARAJIM, _TARIKH*
 * `0195MuarrijSadusi.HadhfMinNasabQuraysh `
	- *TAGS: CENT0200, GEN, PPE, _ANSAB, _BULDAN, _TARIKH*
 * `0200AbuShis.Diwan `
	- *TAGS: CENT0200, _CABBASI, _SHICR*

* **0300AH [[ [Re]generated on 2016-08-29 (16:53:58) ]]**

 * `0204IbnKalbi.AnsabKhayl `
	- *TAGS: CENT0300, GEN, PPE, _ADAB, _BALAGHA, _GHARIB, _MACAJIM, _MUSTALAHAT*
 * `0204IbnKalbi.JamharaAnsab `
	- *TAGS: CENT0300, GEN, PPE, _ANSAB, _BULDAN, _TARIKH*
 * `0204IbnKalbi.NasabMacad `
	- *TAGS: CENT0300, GEN, PPE, _ANSAB, _BULDAN, _TARIKH*
 * `0207Waqidi.FutuhSham `
	- *TAGS: CENT0300, PPE, _BULDAN, _TARIKH*
 * `0207Waqidi.Maghazi `
	- *TAGS: CENT0300, PPE, _ASHAB, _SHAMAIL, _SIRA*
 * `0207Waqidi.Ridda `
	- *TAGS: CENT0300, PPE, _TARIKH*
 * `0209MacmarIbnMuthanna.Khayl `
	- *TAGS: CENT0300, PPE, _ADAB, _BALAGHA, _GHARIB, _MACAJIM, _MUSTALAHAT*
 * `0211AbuCatahiya.Diwan `
	- *TAGS: CENT0300, _CABBASI, _SHICR*
 * `0213IbnHisham.SiraNabawiyya `
	- *TAGS: BIO, CENT0300, DHB, PPE, _ASHAB, _IMAM, _NABI, _SHAMAIL, _SIRA*
 * `0213IbnHisham.Tijan `
	- *TAGS: CENT0300, PPE, _TARIKH*
 * `0222IbnBakkarDabi.AkhbarWafidat `
	- *TAGS: CENT0300, _TABAQAT, _TARAJIM, _TARIKH*
 * `0222IbnBakkarDabi.AkhbarWafidin `
	- *TAGS: CENT0300, _TABAQAT, _TARAJIM, _TARIKH*
 * `0228IbnHammadKhuzaci.Fitan `
	- *TAGS: CENT0300, _AJZA, _CAQAID, _HADITH, _MILAL, _TARIKH*
 * `0230IbnSacd.TabaqatKubra `
	- *TAGS: BIO, CENT0300, COL, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0231IbnSallamJumahi.TabaqatFuhulShucara `
	- *TAGS: CENT0300, PPE, _ADAB, _TABAQAT, _TARAJIM, _TARIKH*
 * `0233YahyaIbnMacin.MacrifaRijal `
	- *TAGS: CENT0300, PPE, _TABAQAT, _TARAJIM*
 * `0233YahyaIbnMacin.MinKalamFiRijal `
	- *TAGS: CENT0300, PPE, _CILAL, _HADITH, _SUALAT, _TARAJIM*
 * `0233YahyaIbnMacin.TarikhIbnMacin `
	- *TAGS: CENT0300, PPE, _HADITH, _SUALAT, _SUNNI, _TABAQAT, _TARAJIM*
 * `0234AbuHasanSacdi.TasmiyaManRuwiya `
	- *TAGS: CENT0300, PPE, _HADITH, _MISC, _TABAQAT, _TARAJIM*
 * `0236AbuCabdAllahZubayri.NasabQuraysh `
	- *TAGS: CENT0300, _ANSAB, _TARAJIM, _TARIKH*
 * `0240KhalifaIbnKhayyat.Tabaqat `
	- *TAGS: CENT0300, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0240KhalifaIbnKhayyat.Tarikh `
	- *TAGS: CENT0300, PPE, _HADITH, _SUNNI, _TARAJIM, _TARIKH*
 * `0241IbnHanbal.AsamiWaKuna `
	- *TAGS: CENT0300, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0241IbnHanbal.CilalWaMacrifa `
	- *TAGS: CENT0300, PPE, _AHKAM, _CILAL, _DACIF, _HADITH, _MAWDUC, _SUALAT, _SUNNI, _TARAJIM*
 * `0241IbnHanbal.FadailSahaba `
	- *TAGS: CENT0300, PPE, _ASHAB, _HADITH, _SIRA, _TABAQAT, _TARAJIM*
 * `0245MuhammadIbnHabib.MukhtalafQabail `
	- *TAGS: CENT0300, GEN, PPE, _ANSAB, _BULDAN, _TARIKH*
 * `0245MuhammadIbnHabib.MunammaqFiAkhbarQuraysh `
	- *TAGS: CENT0300, _BULDAN, _TARIKH*
 * `0248AbuHatimSijistani.FuhulaShucara `
	- *TAGS: CENT0300, _TARAJIM, _TARIKH*
 * `0249Azraqi.AkhbarMakka `
	- *TAGS: CENT0300, PPE, _BULDAN, _HADITH, _TABAQAT, _TARAJIM, _TARIKH*
 * `0255Jahiz.AmilWaMamul `
	- *TAGS: CENT0300, SBS, _ADAB, _BALAGHA, _QISAS, _TARAIF*
 * `0255Jahiz.BayanWaTabyin `
	- *TAGS: CENT0300, SBS, _ADAB, _ADAB, _BALAGHA, _FASAHA*
 * `0255Jahiz.Bighal `
	- *TAGS: CENT0300, SBS, _ADAB, _BALAGHA, _GHARIB, _MACAJIM, _MUSTALAHAT*
 * `0255Jahiz.Bukhala `
	- *TAGS: CENT0300, SBS, _ADAB, _ADAB, _BALAGHA, _QISAS, _TARAIF*
 * `0255Jahiz.BursanWaCurjan `
	- *TAGS: CENT0300, SBS, _ADAB, _BALAGHA, _TARAJIM, _TARIKH*
 * `0255Jahiz.Cuthmaniya `
	- *TAGS: CENT0300, SBS, _FARQ, _RUDUD, _TARIKH*
 * `0255Jahiz.Hayawan `
	- *TAGS: CENT0300, SBS, _ADAB, _BALAGHA, _CULUM, _TIBB*
 * `0255Jahiz.MahasinWaAddad `
	- *TAGS: CENT0300, SBS, _ADAB, _ADAB, _BALAGHA, _QISAS, _TARAIF*
 * `0255Jahiz.MukhtarFiRaddCalaNasara `
	- *TAGS: CENT0300, _FARQ, _RUDUD*
 * `0255Jahiz.Rasail `
	- *TAGS: CENT0300, SBS, _ADAB, _BALAGHA*
 * `0255Jahiz.TabsiraBiTijara `
	- *TAGS: CENT0300, SBS, _ADAB, _BULDAN, _JUGHRAFIYA, _QISAS, _RIHLAT, _TARAIF*
 * `0255Jahiz.TajFiAkhlaq `
	- *TAGS: CENT0300, SBS, _ADAB, _BALAGHA, _SIYASA*
 * `0256Bukhari.Ducafa `
	- *TAGS: CENT0300, PPE, _TABAQAT, _TARAJIM*
 * `0256Bukhari.DucafaSaghir `
	- *TAGS: BIO, CENT0300, HAD, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0256Bukhari.TarikhKabir `
	- *TAGS: CENT0300, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0256Bukhari.TarikhSaghir `
	- *TAGS: CENT0300, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0256ZubayrIbnBakkar.AkhbarMuwaffaqiyat `
	- *TAGS: CENT0300, PPE, _AJZA, _HADITH*
 * `0256ZubayrIbnBakkar.JamharaNasabQuraysh `
	- *TAGS: CENT0300, PPE, _ANSAB, _BULDAN, _TARIKH*
 * `0256ZubayrIbnBakkar.Muntakhab `
	- *TAGS: CENT0300, PPE, _AJZA, _ASHAB, _HADITH, _SIRA, _TABAQAT, _TARAJIM*
 * `0257IbnCabdHakam.FutuhMisr `
	- *TAGS: CENT0300, PPE, _BULDAN, _TARIKH*
 * `0259IbnYacqubJuzjani.AhwalRijal `
	- *TAGS: CENT0300, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0261AbuHasanCijli.MacrifaThiqat `
	- *TAGS: CENT0300, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM, _THIQAT*
 * `0261Muslim.KunaWaAsma `
	- *TAGS: CENT0300, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0261Muslim.Munfaridat `
	- *TAGS: CENT0300, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0262AbuZaydNumayri.TarikhMadina `
	- *TAGS: CENT0300, PPE, _BULDAN, _HADITH, _TABAQAT, _TARAJIM, _TARIKH*
 * `0264AbyZurca.Ducafa `
	- *TAGS: CENT0300, _HADITH, _SUALAT, _TARAJIM*
 * `0272Fakihi.AkhbarMakka `
	- *TAGS: CENT0300, PPE, _BULDAN, _HADITH, _TABAQAT, _TARAJIM, _TARIKH*
 * `0276IbnQutaybaDinawari.AdabKatib `
	- *TAGS: CENT0300, SBS, _ADAB, _ADAB, _BALAGHA, _CARUD, _KITABA*
 * `0276IbnQutaybaDinawari.Macarif `
	- *TAGS: CENT0300, PPE, _ANSAB, _MACAJIM, _TARIKH*
 * `0277AbuHatimRazi.JarhWaTacdil `
	- *TAGS: CENT0400, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0277IbnSyfyanFasawi.MacrifaWaTarikh `
	- *TAGS: CENT0300, PPE, _HADITH, _MISC, _TABAQAT, _TARAJIM, _TARIKH*
 * `0279Baladhuri.AnsabAshraf `
	- *TAGS: CENT0300, GEN, PPE, _ANSAB, _BULDAN, _MACAJIM, _TARIKH*
 * `0279Baladhuri.FutuhBuldan `
	- *TAGS: CENT0300, PPE, _BULDAN, _TARIKH*
 * `0279IbnAbiKhaythama.TarikhKabir `
	- *TAGS: CENT0300, PPE, _BULDAN, _HADITH, _TABAQAT, _TARAJIM*
 * `0280IbnTayfur.Baghdad `
	- *TAGS: CENT0300, PPE, _BULDAN, _HADITH, _TABAQAT, _TARAJIM*
 * `0280IbnTayfur.BallaghatNisa `
	- *TAGS: CENT0300, CENT0400, _ADAB, _ADAB, _BALAGHA, _CHRONOMULTIPLE, _FASAHA, _TARIKH*
 * `0281AbuZurcaDimashqi.Tarikh `
	- *TAGS: CENT0300, PPE, _HADITH, _TARAJIM, _TARIKH*
 * `0282AbuHanifaDinawari.AkhbarTiwal `
	- *TAGS: CENT0300, PPE, _HADITH, _SUNNI, _TARAJIM, _TARIKH*
 * `0286Mubarrad.NasabCadnan `
	- *TAGS: CENT0300, GEN, PPE, _ANSAB, _BULDAN, _TARIKH*
 * `0287Dahhak.AhadWaMathani `
	- *TAGS: CENT0300, PPE, _HADITH, _MACAJIM, _MASANID, _SUNNI, _TABAQAT, _TARAJIM*
 * `0292Bahshal.TarikhWasit `
	- *TAGS: CENT0300, PPE, _BULDAN, _HADITH, _TABAQAT, _TARAJIM, _TARIKH*
 * `0292Yacqubi.Buldan `
	- *TAGS: CENT0300, PPE, _BULDAN, _JUGHRAFIYA, _RIHLAT, _TARIKH*
 * `0292Yacqubi.TarikhYacqubi `
	- *TAGS: CENT0300, PPE, _TARIKH*
 * `0296IbnMuctazz.Diwan `
	- *TAGS: CENT0300, _CABBASI, _SHICR*
 * `0296IbnMuctazz.TabaqatShucara `
	- *TAGS: CENT0300, PPE, _TABAQAT, _TARAJIM*
 * `0296MuhammadIbnJarrah.ManIsmuhCamr `
	- *TAGS: CENT0300, _TABAQAT, _TARAJIM, _TARIKH*
 * `0300IbnKhurdadhbih.MasalikWaMamalik `
	- *TAGS: CENT0300, GEO, PPE, _BULDAN, _JUGHRAFIYA, _MUDHAKKARAT, _RIHLAT, _TARIKH*
 * `0300MuallifMajhul.AkhbarDawlaCabbasiya `
	- *TAGS: CENT0300, PPE, _TARIKH*

* **0400AH [[ [Re]generated on 2016-08-29 (16:53:58) ]]**

 * `0301Bardiji.TabaqatAsma `
	- *TAGS: CENT0400, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0303Nasai.DucafaWaMatrukin `
	- *TAGS: CENT0400, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0303Nasai.FadailSahaba `
	- *TAGS: CENT0400, PPE, _ASHAB, _FIQH, _HADITH, _SIRA, _SUNNI, _TABAQAT, _TARAJIM*
 * `0303Nasai.Tabaqat `
	- *TAGS: CENT0400, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0303Nasai.TasmiyaFuqaha `
	- *TAGS: CENT0400, PPE, _HADITH, _TABAQAT, _TARAJIM, _THIQAT*
 * `0303Nasai.TasmiyaManLamYarwi `
	- *TAGS: CENT0400, PPE, _CULUM, _HADITH, _MISC, _MUSTALAHAT, _SUNNI, _TABAQAT, _TARAJIM*
 * `0303Nasai.TasmiyaShuyukh `
	- *TAGS: CENT0400, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0306IbnHayyanDabbi.AkhbarQudat `
	- *TAGS: CENT0400, PPE, _ANSAB, _MACAJIM, _TABAQAT, _TARAJIM, _TARIKH*
 * `0308IbnIbrahimJundi.FadailMadina `
	- *TAGS: CENT0400, _AJZA, _BULDAN, _HADITH, _TABAQAT, _TARAJIM, _TARIKH*
 * `0308IbnIbrahimJundi.FadailMadina `
	- *TAGS: CENT0400, _TARIKH*
 * `0309IbnFadlan.Rihla `
	- *TAGS: CENT0400, GEO, PPE, _BULDAN, _JUGHRAFIYA, _MUDHAKKARAT, _RIHLAT, _TARIKH*
 * `0310IbnAhmadDulabi.Dhariyya `
	- *TAGS: CENT0400, PPE, _ASHAB, _HADITH, _SIRA, _SUNNI, _TABAQAT, _TARAJIM*
 * `0310IbnAhmadDulabi.KunaWaAsma `
	- *TAGS: CENT0400, PPE, _HADITH, _TARAJIM*
 * `0310Tabari.JamicBayan `
	- *TAGS: CENT0400, SBS, _AHKAM, _CULUM, _HADITH, _QURAN, _SUNNI, _TAFSIR*
 * `0310Tabari.MuntakhabMinDhayl `
	- *TAGS: CENT0400, PPE, _MISC, _TABAQAT, _TARAJIM, _TARIKH*
 * `0310Tabari.Tarikh `
	- *TAGS: CENT0400, CHR, PPE, _TARIKH*
 * `0317AbuQasimBaghawi.MucjamSahaba `
	- *TAGS: CENT0400, PPE, _TABAQAT, _TARAJIM*
 * `0317AbuQasimBaghawi.TarikhWafatShuyukh `
	- *TAGS: BIO, CENT0400, PPE, _AJZA, _HADITH*
 * `0318AbuCurubaHarrani.MuntaqaMinTabaqat `
	- *TAGS: CENT0400, PPE, _AJZA, _HADITH, _TABAQAT, _TARAJIM*
 * `0320CaribQurtubi.SilaTarikhTabari `
	- *TAGS: CENT0400, CHR, PPE, _TARIKH*
 * `0322AbuJacfarCuqayli.DucafaKabir `
	- *TAGS: CENT0400, PPE, _CILAL, _HADITH, _SUALAT, _SUNNI, _TARAJIM*
 * `0322KatibBaghdadi.TarikhAimma `
	- *TAGS: CENT0400, _HADITH, _SHICI*
 * `0330Sirafi.Rihla `
	- *TAGS: CENT0400, GEO, PPE, _BULDAN, _JUGHRAFIYA, _RIHLAT*
 * `0333AbuCarabTamimi.Mihan `
	- *TAGS: CENT0400, PPE, _MISC, _TARIKH*
 * `0333AbuCarabTamimi.TabaqatCulama `
	- *TAGS: BIO, CENT0400, COL, PPE, _TABAQAT, _TARAJIM*
 * `0334IbnHaikHamdani.Iklil `
	- *TAGS: CENT0400, _ANSAB, _MISC*
 * `0334IbnHaikHamdani.SifaJaziraCarab `
	- *TAGS: CENT0400, _BULDAN, _GHARIB, _JUGHRAFIYA, _MACAJIM, _MUSTALAHAT, _RIHLAT*
 * `0334IbnSacidQushayri.TarikhRaqqa `
	- *TAGS: CENT0400, PPE, _AJZA, _HADITH*
 * `0337IbnIshaqZajjaji.Akhbar `
	- *TAGS: CENT0400, _NAHW, _SARF, _TARAJIM, _TARIKH*
 * `0346Istakhri.MasalikWaMamalik `
	- *TAGS: CENT0400, GEO, PPE, _BULDAN, _JUGHRAFIYA, _MUDHAKKARAT, _RIHLAT, _TARIKH*
 * `0346Mascudi.AkhbarZaman `
	- *TAGS: CENT0400, PPE, _TARIKH*
 * `0346Mascudi.MurujDhahab `
	- *TAGS: CENT0400, PPE, _MISC*
 * `0346Mascudi.TanbihWaIshraf `
	- *TAGS: CENT0400, _MISC, _TARIKH*
 * `0347IbnYunusSadafi.Tarikh `
	- *TAGS: CENT0400, PPE, _TABAQAT, _TARAJIM*
 * `0349IbnCumarMuqri.AkhbarNahwiyyin `
	- *TAGS: CENT0400, PPE, _AJZA, _HADITH, _TABAQAT, _TARAJIM, _TARIKH*
 * `0351IbnQanic.MucjamSahaba `
	- *TAGS: CENT0400, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0354IbnHibban.Majruhin `
	- *TAGS: CENT0400, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0354IbnHibban.MashahirCulamaAmsar `
	- *TAGS: CENT0400, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM, _THIQAT*
 * `0354IbnHibban.Sira `
	- *TAGS: CENT0400, PPE, _SHAMAIL, _SIRA*
 * `0354IbnHibban.Thiqat `
	- *TAGS: CENT0400, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM, _THIQAT*
 * `0355AbuFarajIsbahani.Aghani `
	- *TAGS: CENT0400, PPE, _ADAB, _TARAJIM, _TARIKH*
 * `0355AbuFarajIsbahani.Diyarat `
	- *TAGS: CENT0400, GEO, PPE, _BULDAN, _JUGHRAFIYA, _RIHLAT, _TARIKH*
 * `0355MuhammadKindi.FadailMisr `
	- *TAGS: CENT0400, PPE, _BULDAN, _JUGHRAFIYA, _RIHLAT, _TARIKH*
 * `0355MuhammadKindi.WulatMisr `
	- *TAGS: BIO, CENT0400, COL, PPE, _BULDAN, _TABAQAT, _TARAJIM, _TARIKH*
 * `0360Khawlani.TarikhDaraya `
	- *TAGS: CENT0400, HIS, PPE, _BULDAN, _HADITH, _TARIKH*
 * `0360Tabarani.MucjamKabir `
	- *TAGS: CENT0400, COL, HAD, PPE, _HADITH, _MACAJIM, _MASANID, _SUNNI, _TARAJIM*
 * `0365IbnCadiJurjani.AsamiManRawaCanhum `
	- *TAGS: CENT0400, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0365IbnCadiJurjani.KamilFiDucafa `
	- *TAGS: CENT0400, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0365IbnFaqihHamadhani.Buldan `
	- *TAGS: CENT0400, PPE, _BULDAN, _JUGHRAFIYA, _RIHLAT*
 * `0367IbnHawqal.SuraArd `
	- *TAGS: CENT0400, GEO, PPE, _BULDAN, _JUGHRAFIYA, _RIHLAT*
 * `0368AbuGhalibZurari.Risala `
	- *TAGS: BIO, CENT0400, PPE, SHC, _HADITH, _SHICI, _TARAJIM*
 * `0368Sirafi.AkhbarNahwiyyin `
	- *TAGS: CENT0400, PPE, _TABAQAT, _TARAJIM*
 * `0369AbuShaykhIsbahani.TabaqatMuhaddithin `
	- *TAGS: CENT0400, PPE, _BULDAN, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0370IbnBishrAmidi.MutalifWaMukhtalif `
	- *TAGS: BIO, CENT0400, PPE, _TABAQAT, _TARAJIM, _TARIKH*
 * `0371AhmadJurjani.Mucjam `
	- *TAGS: CENT0400, _HADITH, _MACAJIM, _MASANID, _TARAJIM*
 * `0372AbuSacidQayruwani.TahdhibMudawwana `
	- *TAGS: CENT0400, _FIQH, _MALIKI*
 * `0374IbnHusaynAzdi.AsmaManYucrafBiKunya `
	- *TAGS: CENT0400, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0374IbnHusaynAzdi.DhikrIsmKullAshab `
	- *TAGS: CENT0400, _TABAQAT, _TARAJIM*
 * `0374IbnHusaynAzdi.KunaLiManLaYucrafLahuIsm `
	- *TAGS: CENT0400, PPE, _TABAQAT, _TARAJIM*
 * `0374IbnHusaynAzdi.Makhzun `
	- *TAGS: CENT0400, HAD, PPE, _CULUM, _HADITH, _MUSTALAHAT, _TARAJIM*
 * `0374IbnHusaynAzdi.ManWafaqaIsmuhuIsmAbihi `
	- *TAGS: CENT0400, PPE, _HADITH, _MISC, _TABAQAT, _TARAJIM*
 * `0379MuhammadRabci.TarikhMawlidCulama `
	- *TAGS: BIO, CENT0400, COL, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0380Muhallabi.MasalikWaMamalik `
	- *TAGS: CENT0400, GEO, PPE, _BULDAN, _JUGHRAFIYA, _RIHLAT*
 * `0382IbnCabdAllahCaskari.AkhbarMusahhifin `
	- *TAGS: CENT0400, PPE, _HADITH, _LUGHA, _SUNNI, _TABAQAT, _TARAJIM, _TARIKH*
 * `0384IbnCimranMarzubani.MucjamShucara `
	- *TAGS: CENT0400, PPE, _TABAQAT, _TARAJIM, _TARIKH*
 * `0385Daruqutni.DhikrAsmaTabicin `
	- *TAGS: CENT0400, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0385Daruqutni.Ducafa `
	- *TAGS: CENT0400, PPE, _TABAQAT, _TARAJIM*
 * `0385Daruqutni.MutalifWaMukhtalif `
	- *TAGS: CENT0400, PPE, _TABAQAT, _TARAJIM*
 * `0385Daruqutni.SualatBarqani `
	- *TAGS: CENT0400, PPE, _CILAL, _HADITH, _SUALAT, _SUNNI, _TARAJIM*
 * `0385Daruqutni.SualatNaysaburi `
	- *TAGS: CENT0400, PPE, _CILAL, _HADITH, _SUALAT, _SUNNI, _TARAJIM*
 * `0385IbnNadim.Fihrist `
	- *TAGS: BIB, CENT0400, PPE, _ADILLA, _FAHARIS, _KUTUB, _MACAJIM*
 * `0385IbnShahin.TarikhAsmaDucafa `
	- *TAGS: CENT0400, PPE, _TABAQAT, _TARAJIM*
 * `0385IbnShahin.TarikhAsmaThiqat `
	- *TAGS: CENT0400, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM, _THIQAT*
 * `0388Shabushti.Diyarat `
	- *TAGS: CENT0400, GEO, PPE, _BULDAN, _JUGHRAFIYA, _RIHLAT, _TARIKH*
 * `0390Muqaddasi.AhsanTaqasim `
	- *TAGS: CENT0400, GEO, PPE, _BULDAN, _JUGHRAFIYA, _MUDHAKKARAT, _RIHLAT, _TARIKH*
 * `0395AbuHilalCaskari.Talkhis `
	- *TAGS: CENT0400, _FIQH, _GHARIB, _MACAJIM, _MUSTALAHAT*
 * `0395IbnMandahMuhammad.Asami `
	- *TAGS: CENT0400, PPE, _AJZA, _HADITH*
 * `0395IbnMandahMuhammad.FathBab `
	- *TAGS: CENT0400, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0395IbnMandahMuhammad.MacrifaSahaba `
	- *TAGS: CENT0400, PPE, _TABAQAT, _TARAJIM*
 * `0398AbuNasrKalabadhi.HidayaWaIrshad `
	- *TAGS: CENT0400, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0400IbnTahirMaqdisi.BadWaTarikh `
	- *TAGS: CENT0600, PPE, _TARIKH*
 * `0400IshaqMunajjim.AkamMarjan `
	- *TAGS: CENT0400, _BULDAN, _JUGHRAFIYA, _RIHLAT*

* **0500AH [[ [Re]generated on 2016-08-29 (16:53:58) ]]**

 * `0402MuhammadSaydawi.MucjamShuyukh `
	- *TAGS: CENT0500, _HADITH, _MACAJIM, _MASANID, _TABAQAT, _TARAJIM*
 * `0403IbnFaradi.TarikhCulamaAndalus `
	- *TAGS: CENT0500, PPE, _BULDAN, _TABAQAT, _TARAJIM, _TARIKH*
 * `0405AbuFadlHarawi.MucjamFiMushtabah `
	- *TAGS: CENT0500, PPE, _HADITH, _MISC, _TABAQAT, _TARAJIM*
 * `0405HakimNaysaburi.TalkhisTarikhNaysabur `
	- *TAGS: CENT0500, PPE, _TABAQAT, _TARAJIM*
 * `0405HakimNaysaburi.TasmiyaManAkhrajahum `
	- *TAGS: CENT0500, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0409CabdGhaniAzdi.KitabMutawarin `
	- *TAGS: CENT0500, _TARIKH*
 * `0412Sulami.TabaqatSufiya `
	- *TAGS: CENT0500, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `0418WazirMaghribi.AdabKhawas `
	- *TAGS: CENT0500, _ADAB, _BALAGHA, _MISC*
 * `0418WazirMaghribi.Inas `
	- *TAGS: CENT0500, GEN, PPE, _ANSAB, _TARIKH*
 * `0421IbnMuhammadMarzuqi.AzminaWaAmkina `
	- *TAGS: CENT0500, GEO, PPE, _ADAB, _BALAGHA, _GHARIB, _MACAJIM, _MASAIL, _MUSTALAHAT*
 * `0421Miskawayh.Tajarib `
	- *TAGS: CENT0500, PPE, _TARIKH*
 * `0427HamzaJurjani.TarikhJurjan `
	- *TAGS: CENT0500, PPE, _BULDAN, _HADITH, _TABAQAT, _TARAJIM, _TARIKH*
 * `0428IbnManjuwayhIsbahani.RijalSahihMuslim `
	- *TAGS: CENT0500, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0429AbuMansurThacalibi.YatimaDahr `
	- *TAGS: CENT0500, PPE, _ADAB, _SHICR, _TABAQAT, _TARAJIM, _TARIKH*
 * `0429Thacalibi.ThimarQulub `
	- *TAGS: CENT0500, SBS, _ADAB, _ADAB, _AMTHAL, _BALAGHA*
 * `0430AbuNucaymIsbahani.DhikrManIsmuhuShucba `
	- *TAGS: CENT0500, PPE, _AJZA, _HADITH, _MISC, _TARAJIM*
 * `0430AbuNucaymIsbahani.Ducafa `
	- *TAGS: CENT0500, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0430AbuNucaymIsbahani.HilyaAwliya `
	- *TAGS: CENT0500, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0430AbuNucaymIsbahani.MacrifaSahaba `
	- *TAGS: CENT0500, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0430AbuNucaymIsbahani.TarikhIsbahan `
	- *TAGS: CENT0500, PPE, _BULDAN, _HADITH, _TABAQAT, _TARAJIM, _TARIKH*
 * `0430AbuNucaymIsbahani.TasmiyaMaIntahaIlayna `
	- *TAGS: CENT0500, PPE, _AJZA, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0436HusaynSaymari.AkhbarAbiHanifa `
	- *TAGS: CENT0500, PPE, _TABAQAT, _TARAJIM, _TARIKH*
 * `0440AbuRayhanBiruni.TahqiqMaLilHind `
	- *TAGS: CENT0500, _BULDAN, _CAQAID, _FIRAQ, _JUGHRAFIYA, _MILAL, _RIHLAT*
 * `0442Tanukhi.TarikhCulamaNahwiyyin `
	- *TAGS: CENT0500, PPE, _TABAQAT, _TARAJIM, _TARIKH*
 * `0444AbuFadlIbnMahdi.DhikrShuyukh `
	- *TAGS: CENT0500, _HADITH, _MAKHTUTAT*
 * `0446AbuYaclaKhalili.IrshadFiMacrifaCulama `
	- *TAGS: CENT0500, PPE, _HADITH, _MUSTALAHAT, _TABAQAT, _TARAJIM*
 * `0448HilalSabi.TuhfaUmara `
	- *TAGS: CENT0500, PPE, _TARAJIM, _TARIKH*
 * `0449AbuCalaMacarri.Diwan `
	- *TAGS: CENT0500, _CABBASI, _SHICR*
 * `0450Najashi.Rijal `
	- *TAGS: BIO, CENT0500, PPE, SHC, _HADITH, _SHICI, _TARAJIM*
 * `0456IbnHazm.AsmaKhulafa `
	- *TAGS: CENT0500, PPE, _TARAJIM, _TARIKH*
 * `0456IbnHazm.FadailAndalus `
	- *TAGS: CENT0500, PPE, _BULDAN, _JUGHRAFIYA, _RIHLAT, _TARIKH*
 * `0456IbnHazm.JamharaAnsab `
	- *TAGS: CENT0500, PPE, _ANSAB, _TARAJIM, _TARIKH*
 * `0456IbnHazm.NaqtCarus `
	- *TAGS: CENT0500, PPE, _TARAJIM, _TARIKH*
 * `0456IbnHazm.RisalaFiFutuhIslam `
	- *TAGS: CENT0500, _TARIKH*
 * `0456IbnHazm.RisalaFiMaratibCulum `
	- *TAGS: BIB, CENT0500, PPE, _FAHARIS, _KUTUB*
 * `0456IbnHazm.UmmahatKhulafa `
	- *TAGS: CENT0500, PPE, _TARAJIM, _TARIKH*
 * `0458Bayhaqi.DalailNubuwwa `
	- *TAGS: CENT0500, DHB, PPE, _ASHAB, _CAQAID, _HADITH, _SHAMAIL, _SIRA*
 * `0460ShaykhTusi.IkhtiyarMacrifaRijal `
	- *TAGS: CENT0500, PPE, SHC, _HADITH, _SHICI, _TARAJIM*
 * `0460ShaykhTusi.Rijal `
	- *TAGS: CENT0500, PPE, SHC, _HADITH, _SHICI, _TARAJIM*
 * `0463IbnCabdBarr.InbahCalaQabail `
	- *TAGS: CENT0500, _ANSAB, _HADITH, _SUNNI, _TARIKH*
 * `0463IbnCabdBarr.IsticabFiMacrifaAshab `
	- *TAGS: BIO, CENT0500, COL, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0463KhatibBaghdadi.GhunyaMultamis `
	- *TAGS: CENT0500, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0463KhatibBaghdadi.MuttafiqWaMuftariq `
	- *TAGS: CENT0500, PPE, _TABAQAT, _TARAJIM*
 * `0463KhatibBaghdadi.SabiqWaLahiq `
	- *TAGS: CENT0500, _CULUM, _HADITH*
 * `0463KhatibBaghdadi.TalkhisMutashabih `
	- *TAGS: CENT0500, _HADITH, _MISC, _MUSTALAHAT, _TABAQAT, _TARAJIM*
 * `0463KhatibBaghdadi.TarikhBaghdad `
	- *TAGS: BIO, CENT0500, COL, DHB, PPE, _BULDAN, _HADITH, _SUNNI, _TABAQAT, _TARAJIM, _TARIKH*
 * `0466CabdAzizKattani.DhaylTarikhMawlidCulama `
	- *TAGS: CENT0500, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0469IbnHayyanQurtubi.Muqtabas `
	- *TAGS: CENT0500, PPE, _BULDAN, _TARIKH*
 * `0474IbnKhalafBaji.TacdilWaTakhrij `
	- *TAGS: CENT0500, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0475IbnMakula.IkmalFiRafcIrtiyab `
	- *TAGS: CENT0500, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0475IbnMakula.TahdhibMustamirr `
	- *TAGS: CENT0500, PPE, _HADITH, _MISC, _TABAQAT, _TARAJIM*
 * `0476AbuIshaqShirazi.TabaqatFuqaha `
	- *TAGS: BIO, CENT0500, COL, PPE, _FIQH, _TABAQAT, _TARAJIM, _TARIKH*
 * `0482AbuIshaqHabbal.WafayatMisriyyin `
	- *TAGS: CENT0500, PPE, _BULDAN, _HADITH, _TABAQAT, _TARAJIM, _TARIKH*
 * `0487AbuCubaydBakri.MasalikWaMamalik `
	- *TAGS: CENT0500, GEO, PPE, _BULDAN, _JUGHRAFIYA, _RIHLAT*
 * `0487AbuCubaydBakri.MucjamMaIstacjama `
	- *TAGS: CENT0500, _BULDAN, _FAHARIS, _GHARIB, _JUGHRAFIYA, _LUGHA, _MACAJIM, _MUSTALAHAT, _NAHW, _RIHLAT, _SARH*
 * `0488IbnFutuhHumaydi.JadhwaMuqtabis `
	- *TAGS: CENT0500, PPE, _TABAQAT, _TARAJIM, _TARIKH*
 * `0498AbuCaliJayyani.AlqabSahaba `
	- *TAGS: CENT0500, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0498AbuCaliJayyani.TaqyidMuhmal `
	- *TAGS: CENT0500, PPE, _HADITH, _MISC, _TABAQAT, _TARAJIM*

* **0600AH [[ [Re]generated on 2016-08-29 (16:53:58) ]]**

 * `0507AbuBakrShashi.HilyaCulama `
	- *TAGS: CENT0600, PPE, _FIQH, _SHAFICI*
 * `0507IbnQaysarani.AnsabMuttafiqa `
	- *TAGS: CENT0600, PPE, _ANSAB, _HADITH, _MISC, _TABAQAT, _TARAJIM*
 * `0508FattalNaysaburi.RawdaWacizin `
	- *TAGS: CENT0600, PPE, SHC, _HADITH, _SHICI*
 * `0511IbnMandahYahya.MacrifaAsamiArdaf `
	- *TAGS: CENT0600, PPE, _HADITH, _MISC, _TABAQAT, _TARAJIM*
 * `0511SalmaSahari.Ansab `
	- *TAGS: CENT0600, _ANSAB, _BULDAN, _TARIKH*
 * `0515IbnQattac.DurraKhatira `
	- *TAGS: CENT0600, _TABAQAT, _TARAJIM*
 * `0521IbnAbiYacla.TabaqatHanabila `
	- *TAGS: BIO, CENT0600, COL, PPE, _CAQAID, _FIQH, _MILAL, _TABAQAT, _TARAJIM, _TARIKH*
 * `0521MuhammadHamadhani.TakmilaTarikhTabari `
	- *TAGS: CENT0600, PPE, _TARIKH*
 * `0524IbnAkfani.DhaylDhaylTarikhMawlidCulama `
	- *TAGS: CENT0600, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0528FathIbnKhaqan.QalaidCiqyan `
	- *TAGS: CENT0300, _TABAQAT, _TARAJIM*
 * `0535QawwamSunna.DalailNubuwwa `
	- *TAGS: CENT0600, PPE, _ASHAB, _CAQAID, _HADITH, _SHAMAIL, _SIRA, _SUNNI, _TABAQAT, _TARAJIM*
 * `0535QawwamSunna.SiyarSalaf `
	- *TAGS: BIO, CENT0600, PPE, _TABAQAT, _TARAJIM*
 * `0538MahmudZamakhshari.JibalWaAmkina `
	- *TAGS: CENT0600, GEO, PPE, _BULDAN, _JUGHRAFIYA, _RIHLAT*
 * `0541IbnCatiyyaMuharibi.Fahrasa `
	- *TAGS: CENT0600, PPE, _ADILLA, _FAHARIS, _KUTUB*
 * `0542IbnBassamShantarini.Dhakhira `
	- *TAGS: CENT0600, PPE, _ADAB, _BULDAN, _TABAQAT, _TARAJIM, _TARIKH*
 * `0544CiyadIbnMusaYahsubi.Ghunya `
	- *TAGS: CENT0600, PPE, _AJZA, _HADITH*
 * `0544CiyadIbnMusaYahsubi.TartibMadarik `
	- *TAGS: BIO, CENT0600, COL, PPE, _TABAQAT, _TARAJIM, _TARIKH*
 * `0550AbuHajjajAshcari.TacrifBiAnsab `
	- *TAGS: CENT0600, PPE, _ANSAB, _BULDAN, _TARIKH*
 * `0555IbnQalanisi.Tarikh `
	- *TAGS: BIO, CENT0600, PPE, _TARIKH*
 * `0560SharifIdrisi.NuzhaMushtaq `
	- *TAGS: CENT0600, _BULDAN, _JUGHRAFIYA, _MUDHAKKARAT, _RIHLAT, _TARIKH*
 * `0561Samcani.Ansab `
	- *TAGS: CENT0600, COL, DHB, ONO, PPE, _ANSAB, _MACAJIM, _TABAQAT, _TARAJIM, _TARIKH*
 * `0561Samcani.Muntakhab `
	- *TAGS: CENT0600, PPE, _TABAQAT, _TARAJIM*
 * `0561Samcani.Tahbir `
	- *TAGS: CENT0600, PPE, _TABAQAT, _TARAJIM, _TARIKH*
 * `0565IbnZaydBayhaqi.LubabAnsab `
	- *TAGS: CENT0600, PPE, _ANSAB, _MISC*
 * `0565IbnZaydBayhaqi.TarikhBayhaq `
	- *TAGS: CENT0600, PPE, _TABAQAT, _TARAJIM*
 * `0565IbnZaydBayhaqi.TatimmaSiwanHikma `
	- *TAGS: CENT0600, PPE, _MISC, _TABAQAT, _TARAJIM*
 * `0567IbnKhashshabBaghdadi.TarikhMawalidAimma `
	- *TAGS: CENT0600, _HADITH, _SHICI*
 * `0569CumaraHakami.NukatCasriyya `
	- *TAGS: CENT0600, PPE, _ADAB, _BALAGHA*
 * `0571IbnCasakir.MucjamShuyukh `
	- *TAGS: CENT0600, PPE, _HADITH*
 * `0571IbnCasakir.TarikhDimashq `
	- *TAGS: BIO, CENT0600, COL, PPE, _BULDAN, _HADITH, _SUNNI, _TABAQAT, _TARAJIM, _TARIKH*
 * `0573NashwanHimyari.KhulasaSiyar `
	- *TAGS: CENT0600, _TARAJIM, _TARIKH*
 * `0575IbnBabawayh.Fihrist `
	- *TAGS: CENT0600, PPE, SHC, _HADITH, _SHICI, _TARAJIM*
 * `0575IbnKhayrIshbili.Fahrasa `
	- *TAGS: CENT0600, PPE, _ADILLA, _FAHARIS, _KUTUB*
 * `0576IbnMuhammadSilafi.Mashyakha `
	- *TAGS: CENT0600, PPE, _AJZA, _HADITH, _MISC, _TARAJIM*
 * `0576IbnMuhammadSilafi.MashyakhaBaghdadiyya `
	- *TAGS: CENT0600, PPE, _HADITH, _MAKHTUTAT*
 * `0576IbnMuhammadSilafi.MucjamSafar `
	- *TAGS: BIO, CENT0600, COL, PPE, _ADAB, _BALAGHA, _HADITH, _MISC, _TABAQAT, _TARAJIM*
 * `0576IbnMuhammadSilafi.Wajiz `
	- *TAGS: CENT0600, PPE, _HADITH, _MUSTALAHAT, _TABAQAT, _TARAJIM*
 * `0577IbnAnbari.NuzhaAlibba `
	- *TAGS: CENT0600, PPE, _TABAQAT, _TARAJIM*
 * `0578IbnBashkuwal.GhawamidAsma `
	- *TAGS: CENT0600, PPE, _HADITH, _MISC, _TABAQAT, _TARAJIM*
 * `0578IbnBashkuwal.Sila `
	- *TAGS: BIO, CENT0600, COL, PPE, _TARAJIM, _TARIKH*
 * `0580IbnCimrani.InbaFiTarikhKhulafa `
	- *TAGS: CENT0600, HIS, PPE, _TARIKH*
 * `0584IbnMunqidhShayzari.Ictibar `
	- *TAGS: CENT0600, _TARAJIM, _TARIKH*
 * `0584IbnMusaHazimi.Amakin `
	- *TAGS: CENT0600, GEO, PPE, _BULDAN, _GHARIB, _JUGHRAFIYA, _MACAJIM, _MUSTALAHAT, _RIHLAT*
 * `0584IbnMusaHazimi.CujalaMubtadi `
	- *TAGS: CENT0600, GEN, PPE, _ANSAB, _MISC*
 * `0597CimadDinKatib.BarqShami `
	- *TAGS: CENT0600, PPE, _BULDAN, _TARIKH*
 * `0597CimadDinKatib.KharidaQasr `
	- *TAGS: CENT0600, COL, POE, PPE, _ADAB, _ADAB, _BALAGHA, _TARAJIM, _TARIKH*
 * `0597IbnJawzi.DucafaWaMatrukin `
	- *TAGS: CENT0600, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0597IbnJawzi.FadailQuds `
	- *TAGS: CENT0600, _BULDAN, _JUGHRAFIYA, _RIHLAT, _TARIKH*
 * `0597IbnJawzi.Mashyakha `
	- *TAGS: BIO, CENT0600, PPE, _AJZA, _HADITH*
 * `0597IbnJawzi.Muntazam `
	- *TAGS: BIO, CENT0600, CHR, COL, DHB, PPE, _TARIKH*
 * `0597IbnJawzi.MuthirGharam `
	- *TAGS: CENT0600, GEO, PPE, _BULDAN, _JUGHRAFIYA, _RIHLAT*
 * `0597IbnJawzi.SifaSafwa `
	- *TAGS: BIO, CENT0600, COL, PPE, _ADAB, _ADHKAR, _FIQH, _MISC, _RAQAIQ, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `0597IbnJawzi.TalqihFuhum `
	- *TAGS: CENT0600, PPE, _TARIKH*
 * `0597IbnJawzi.TarikhBaytMuqaddas `
	- *TAGS: CENT0600, PPE, _BULDAN, _TARIKH*
 * `0599IbnYahyaDabbi.BughyaMultamis `
	- *TAGS: CENT0600, PPE, _TABAQAT, _TARAJIM*
 * `0600AbuBaqaHilli.ManaqibMazidiya `
	- *TAGS: CENT0600, _TARAJIM, _TARIKH*
 * `0600KatibMarrakushi.Istibsar `
	- *TAGS: CENT0600, _BULDAN, _JUGHRAFIYA, _RIHLAT*

* **0700AH [[ [Re]generated on 2016-08-29 (16:53:58) ]]**

 * `0606IbnMamati.LataifDhakhira `
	- *TAGS: CENT0700, PPE, _TABAQAT, _TARAJIM*
 * `0611CaliHarawi.Isharat `
	- *TAGS: CENT0700, GEO, PPE, _BULDAN, _JUGHRAFIYA, _RIHLAT*
 * `0611SharafDinMuqaddasi.Arbacin `
	- *TAGS: CENT0700, PPE, _AJZA, _HADITH*
 * `0614IbnJubayr.Rihla `
	- *TAGS: CENT0700, GEO, PPE, _BULDAN, _JUGHRAFIYA, _MUDHAKKARAT, _RIHLAT, _TARIKH*
 * `0615MuwaffaqDinShafici.MurshidZuwwar `
	- *TAGS: CENT0700, GEO, PPE, _BULDAN, _JUGHRAFIYA, _RIHLAT*
 * `0617MansurIbnShahanshah.MidmarHaqaiq `
	- *TAGS: CENT0700, PPE, _MISC, _TARIKH*
 * `0623Qazwini.Tadwin `
	- *TAGS: CENT0700, PPE, _BULDAN, _HADITH, _TARAJIM, _TARIKH*
 * `0626YaqutHamawi.Khazal `
	- *TAGS: CENT0700, GEO, PPE, _BULDAN, _JUGHRAFIYA, _RIHLAT*
 * `0626YaqutHamawi.MucjamBuldan `
	- *TAGS: CENT0700, COL, GEO, PPE, _ANSAB, _BULDAN, _FAHARIS, _GHARIB, _JUGHRAFIYA, _MACAJIM, _MUSTALAHAT, _RIHLAT*
 * `0626YaqutHamawi.MucjamUdaba `
	- *TAGS: BIO, CENT0700, COL, POE, PPE, _ADAB, _TABAQAT, _TARAJIM, _TARIKH*
 * `0628IbnCaliSanhaji.AkhbarMuluk `
	- *TAGS: CENT0700, _BULDAN, _TARIKH*
 * `0629IbnNuqta.IfadaWaIctibar `
	- *TAGS: CENT0700, _BULDAN, _JUGHRAFIYA, _RIHLAT*
 * `0629IbnNuqta.TakmilaIkmal `
	- *TAGS: CENT0700, PPE, _HADITH, _MISC, _TABAQAT, _TARAJIM*
 * `0629IbnNuqta.TaqyidLiMacrifa `
	- *TAGS: BIO, CENT0700, COL, PPE, _FAHARIS, _KUTUB, _TABAQAT, _TARAJIM*
 * `0630IbnAthirCizzDin.Kamil `
	- *TAGS: CENT0700, CHR, PPE, _TARIKH*
 * `0630IbnAthirCizzDin.LubabFiTahdhibAnsab `
	- *TAGS: CENT0700, COL, ONO, PPE, _ANSAB, _HADITH, _MACAJIM, _MISC, _TARAJIM*
 * `0630IbnAthirCizzDin.UsdGhaba `
	- *TAGS: CENT0700, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0632AbyHafsSuhrawardi.Mashyakha `
	- *TAGS: CENT0700, PPE, _AJZA, _HADITH*
 * `0632IsmacilMarwazi.FakhriFiAnsab `
	- *TAGS: CENT0700, _BULDAN, _TARIKH*
 * `0637IbnMustafwi.TarikhIrbil `
	- *TAGS: CENT0700, PPE, _BULDAN, _TABAQAT, _TARAJIM, _TARIKH*
 * `0639AbuBakrMalaqi.MatlacAnwar `
	- *TAGS: CENT0700, PPE, _TABAQAT, _TARAJIM*
 * `0640AbuHafsDunaysiri.TarikhDunaysir `
	- *TAGS: CENT0700, PPE, _AJZA, _HADITH*
 * `0641Sarifini.Muntakhab `
	- *TAGS: CENT0700, PPE, _BULDAN, _HADITH, _TABAQAT, _TARAJIM, _TARIKH*
 * `0642IbnNajjar.DhaylTarikhBaghdad `
	- *TAGS: BIO, CENT0700, COL, PPE, _BULDAN, _HADITH, _SUNNI, _TARAJIM*
 * `0643DiyaDinMuqaddasi.FadailBaytMaqdis `
	- *TAGS: CENT0700, _AJZA, _BULDAN, _HADITH, _TABAQAT, _TARAJIM, _TARIKH*
 * `0643DiyaDinMuqaddasi.JuzAwham `
	- *TAGS: CENT0700, PPE, _HADITH, _MISC, _TABAQAT, _TARAJIM*
 * `0643IbnSalahShahrazuri.TabaqatFuqaha `
	- *TAGS: BIO, CENT0700, COL, PPE, _TABAQAT, _TARAJIM, _TARIKH*
 * `0645TilimsaniBurri.Jawhara `
	- *TAGS: CENT0700, GEN, PPE, _ANSAB, _BULDAN, _TARIKH*
 * `0646IbnQifti.IkhbarCulama `
	- *TAGS: CENT0700, PPE, _TABAQAT, _TARAJIM, _TARIKH*
 * `0646IbnQifti.InbahRuwat `
	- *TAGS: CENT0700, PPE, _TABAQAT, _TARAJIM*
 * `0646IbnQifti.Muhammadun `
	- *TAGS: CENT0700, PPE, _TABAQAT, _TARAJIM, _TARIKH*
 * `0647CabdWahidMarrakushi.Mucjib `
	- *TAGS: CENT0700, PPE, _BULDAN, _TARIKH*
 * `0650IbnNazifHamawi.TarikhMansuri `
	- *TAGS: CENT0700, PPE, _TARIKH*
 * `0657IbnIbrahimIrbili.MudhakaraFiAlqab `
	- *TAGS: CENT0700, _TABAQAT, _TARAJIM, _TARIKH*
 * `0658IbnAbbar.HullaSiyara `
	- *TAGS: CENT0700, PPE, _BULDAN, _TARIKH*
 * `0658IbnAbbar.MucjamAshab `
	- *TAGS: CENT0700, PPE, _AJZA, _HADITH, _TABAQAT, _TARAJIM*
 * `0658IbnAbbar.TakmilaLiSila `
	- *TAGS: BIO, CENT0700, COL, PPE, _TARIKH*
 * `0658IbnAbbar.TuhfaQadim `
	- *TAGS: CENT0700, PPE, _MISC, _TABAQAT, _TARAJIM*
 * `0659SainDinNaccal.Mashyakha `
	- *TAGS: CENT0700, PPE, _AJZA, _HADITH*
 * `0660IbnCadim.BughyatTalib `
	- *TAGS: CENT0700, PPE, _BULDAN, _TABAQAT, _TARAJIM, _TARIKH*
 * `0660IbnCadim.ZubdaHalab `
	- *TAGS: CENT0700, PPE, _BULDAN, _TARIKH*
 * `0662RashidAttar.NuzhatNazir `
	- *TAGS: CENT0700, _AJZA, _HADITH*
 * `0665AbuShama.Rawdatayn `
	- *TAGS: CENT0700, PPE, _BULDAN, _TARIKH*
 * `0668IbnAbiUsaybica.CuyunAnba `
	- *TAGS: BIO, CENT0700, COL, PPE, _ANSAB, _MACAJIM, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `0673AbuMahasinYaghmuri.NurQabas `
	- *TAGS: CENT0700, PPE, _MISC, _TABAQAT, _TARAJIM*
 * `0676Nawawi.TahdhibAsma `
	- *TAGS: CENT0700, PPE, _GHARIB, _LUGHA, _MACAJIM, _MISC, _MUSTALAHAT, _TABAQAT, _TARAJIM*
 * `0677SahibTaji.HalbaFiAsmaKhayl `
	- *TAGS: CENT0300, _GHARIB, _MACAJIM, _MASAIL, _MUSTALAHAT*
 * `0680IbnSabuni.TakmilaIkmalIkmal `
	- *TAGS: CENT0700, ONO, PPE, _HADITH, _MISC, _TABAQAT, _TARAJIM*
 * `0681IbnKhallikan.WafayatAcyan `
	- *TAGS: BIO, CENT0700, COL, DHB, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `0682ZakariyaQazwini.AtharBilad `
	- *TAGS: CENT0700, PPE, _BULDAN, _JUGHRAFIYA, _RIHLAT, _TARIKH*
 * `0684IbnShaddad.AclaqKhatira `
	- *TAGS: CENT0700, PPE, _BULDAN, _JUGHRAFIYA, _RIHLAT, _TARAJIM, _TARIKH*
 * `0685IbnCibri.TarikhMukhtasarDuwal `
	- *TAGS: CENT0700, PPE, _TARIKH*
 * `0685IbnSacidMaghribi.GhusunYanica `
	- *TAGS: BIO, CENT0700, PPE, _TABAQAT, _TARAJIM*
 * `0685IbnSacidMaghribi.Jughrafiya `
	- *TAGS: CENT0700, GEO, PPE, _BULDAN, _JUGHRAFIYA, _MISC, _RIHLAT*
 * `0685IbnSacidMaghribi.Mughrib `
	- *TAGS: CENT0700, PPE, _BULDAN, _TARIKH*
 * `0690IbnMujawirDimashqi.TarikhMustabsir `
	- *TAGS: CENT0700, PPE, _BULDAN, _JUGHRAFIYA, _MISC, _RIHLAT*
 * `0691IbnYusufLabli.Fihrist `
	- *TAGS: CENT0700, _ADILLA, _FAHARIS, _KUTUB*
 * `0694MuhibbDinTabari.Dhakhair `
	- *TAGS: CENT0700, PPE, _ASHAB, _HADITH, _SHAMAIL, _SHICI, _SIRA*
 * `0694MuhibbDinTabari.RiyadNadira `
	- *TAGS: CENT0700, PPE, _ASHAB, _SIRA, _TABAQAT, _TARAJIM*
 * `0695IbnCidhariMarrakushi.BayanMaghrib `
	- *TAGS: CENT0700, _BULDAN, _TARIKH*
 * `0696Dabbagh.MacalimIman `
	- *TAGS: BIO, CENT0700, COL, ORPHAN, PPE*
 * `0696IbnZahiri.Mashyakha `
	- *TAGS: CENT0700, PPE, _AJZA, _HADITH, _TARAJIM*

* **0800AH [[ [Re]generated on 2016-08-29 (16:53:58) ]]**

 * `0701SharafDinYunini.Mashyakha `
	- *TAGS: CENT0800, PPE, _AJZA, _HADITH*
 * `0703MuhammadMarrakushi.DhaylWaTakmila `
	- *TAGS: CENT0800, PPE, _MISC, _TABAQAT, _TARAJIM*
 * `0705SharafDinDimyatti.MucjamShuyukh `
	- *TAGS: CENT0800, PPE, _HADITH, _MAKHTUTAT*
 * `0709CaliCalawi.Majdi `
	- *TAGS: CENT0800, GEN, PPE, SHC, _ANSAB, _MACAJIM*
 * `0711IbnManzurIfriqi.MukhtasarTarikhDimashq `
	- *TAGS: BIO, CENT0800, COL, PPE, _TABAQAT, _TARAJIM, _TARIKH*
 * `0714AhmadGhibrini.CunwanDiraya `
	- *TAGS: BIO, CENT0800, PPE, _TABAQAT, _TARAJIM*
 * `0723IbnFuwati.Hawadith `
	- *TAGS: CENT0800, PPE, _TARIKH*
 * `0726CallamaHilli.KhulasaAqwal `
	- *TAGS: BIO, CENT0800, PPE, _HADITH, _SHICI, _TARAJIM*
 * `0726Yunini.DhaylMiratZaman `
	- *TAGS: BIO, CENT0800, CHR, COL, PPE, _TARIKH*
 * `0730MuhammadTujibi.Barnamaj `
	- *TAGS: CENT0800, PPE, _HADITH*
 * `0732AbuFida.MukhtasarFiAkhbar `
	- *TAGS: CENT0800, PPE, _TARIKH*
 * `0732AbuFida.Yawaqit `
	- *TAGS: CENT0800, _BULDAN, _TARIKH*
 * `0732IbnYacqubJanadi.SulukFiTabaqat `
	- *TAGS: BIO, CENT0800, COL, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `0733IbnJamaca.Mashyakha `
	- *TAGS: BIO, CENT0800, PPE, _AJZA, _HADITH*
 * `0733Nuwayri.NihayaArab `
	- *TAGS: CENT0800, PPE, _ADAB, _ADAB, _BALAGHA, _MISC*
 * `0739SafiDinHanbali.Marasid `
	- *TAGS: CENT0800, _BULDAN, _JUGHRAFIYA, _RIHLAT*
 * `0740IbnDawudHilli.Rijal `
	- *TAGS: BIO, CENT0800, PPE, SHC, _HADITH, _SHICI, _TARAJIM*
 * `0741KhatibTabrizi.Ikmal `
	- *TAGS: BIO, CENT0800, PPE, SHC, _HADITH, _SHICI, _TARAJIM*
 * `0742Mizzi.TahdhibKamal `
	- *TAGS: CENT0800, DHB, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0747MuhyiDinYunini.Mashyakha `
	- *TAGS: CENT0800, PPE, _AJZA, _HADITH*
 * `0748Dhahabi.CibarFiKhabar `
	- *TAGS: CENT0800, CHR, PPE, _TARIKH*
 * `0748Dhahabi.Culuww `
	- *TAGS: CENT0800, DHB, PPE, _CAQAID, _MILAL*
 * `0748Dhahabi.DhaylCibar `
	- *TAGS: CENT0800, PPE, _TARIKH*
 * `0748Dhahabi.DhaylDiwanDucafa `
	- *TAGS: CENT0800, PPE, _TABAQAT, _TARAJIM*
 * `0748Dhahabi.DhikrAsmaManTakallama `
	- *TAGS: CENT0800, DHB, PPE, _HADITH, _TABAQAT, _TARAJIM, _THIQAT*
 * `0748Dhahabi.DiwanDucafa `
	- *TAGS: CENT0800, PPE, _TABAQAT, _TARAJIM*
 * `0748Dhahabi.Kashif `
	- *TAGS: CENT0800, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0748Dhahabi.MacrifaQurraKibar `
	- *TAGS: BIO, CENT0800, COL, PPE, _MUFASSIRUN, _TABAQAT, _TARAJIM, _TARIKH*
 * `0748Dhahabi.MizanIctidal `
	- *TAGS: CENT0800, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0748Dhahabi.MucinFiTabaqatMuhaddithin `
	- *TAGS: CENT0800, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0748Dhahabi.MucjamMuhaddithin `
	- *TAGS: CENT0800, PPE, _HADITH, _MISC, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `0748Dhahabi.MucjamShuyukh `
	- *TAGS: BIO, CENT0800, COL, PPE, _TABAQAT, _TARAJIM*
 * `0748Dhahabi.MughniFiDucafa `
	- *TAGS: CENT0800, DHB, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0748Dhahabi.MukhtasarCuluww `
	- *TAGS: CENT0800, DHB, PPE, _ALBANI*
 * `0748Dhahabi.MukhtasarMinDubaythi `
	- *TAGS: CENT0800, PPE, _BULDAN, _HADITH, _SUNNI, _TARAJIM*
 * `0748Dhahabi.Muqtana `
	- *TAGS: CENT0800, DHB, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0748Dhahabi.Radd `
	- *TAGS: CENT0800, _CILAL, _HADITH, _MUSHKIL, _TAKHRIJ, _TARAJIM*
 * `0748Dhahabi.RuwatThiqat `
	- *TAGS: CENT0800, DHB, PPE, _HADITH, _TABAQAT, _TARAJIM, _THIQAT*
 * `0748Dhahabi.SiyarAclamNubala `
	- *TAGS: BIO, CENT0800, COL, DHB, PPE, _FIQH, _HADITH, _SUNNI, _TABAQAT, _TARAJIM, _TARIKH, _THIQAT, _WAFAYAT*
 * `0748Dhahabi.TadhkiraHuffaz `
	- *TAGS: BIO, CENT0800, COL, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM, _THIQAT*
 * `0748Dhahabi.TarikhIslam `
	- *TAGS: BIO, CENT0800, CHR, COL, DHB, PPE, _TABAQAT, _TARAJIM, _TARIKH*
 * `0748IbnDimyati.Mustafad `
	- *TAGS: CENT0800, PPE, _BULDAN, _HADITH, _SUNNI, _TARAJIM*
 * `0749IbnWardi.KharidaCajaib `
	- *TAGS: CENT0900, _BULDAN, _JUGHRAFIYA, _RIHLAT*
 * `0749IbnWardi.Tarikh `
	- *TAGS: CENT0800, PPE, _TARIKH*
 * `0749ShihabDinCumari.MasalikAbsar `
	- *TAGS: CENT0800, PPE, _BULDAN, _JUGHRAFIYA, _RIHLAT, _TARIKH*
 * `0749Wadiashi.Barnamaj `
	- *TAGS: BIB, CENT0800, PPE, _ADILLA, _FAHARIS, _KUTUB*
 * `0750AbuHafsQazwini.Mashyakha `
	- *TAGS: BIO, CENT0800, PPE, _CULUM, _HADITH*
 * `0751IbnQayyimJawziyya.IghathaLahfan `
	- *TAGS: CENT0800, SBS, _FIQH, _IBNQAYYIM, _MASAIL, _USUL*
 * `0761IbnKaykaldi.JamicTahsil `
	- *TAGS: CENT0800, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0761IbnKaykaldi.Mukhtalitin `
	- *TAGS: CENT0800, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0762MughaltayIbnQalij.IkmalTahdhib `
	- *TAGS: CENT0800, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0764IbnShakirKutubi.FawatWafayat `
	- *TAGS: CENT0800, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `0764Safadi.AcyanCasr `
	- *TAGS: BIO, CENT0800, COL, PPE, _TABAQAT, _TARAJIM*
 * `0764Safadi.NaktHimyan `
	- *TAGS: CENT0800, PPE, _ADAB, _QISAS, _TABAQAT, _TARAIF, _TARAJIM*
 * `0764Safadi.WafiBiWafayat `
	- *TAGS: BIO, CENT0800, COL, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `0765AbuMahasinHusayni.DhaylTadhkira `
	- *TAGS: CENT0800, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM, _THIQAT*
 * `0765AbuMahasinHusayni.IkmalLiRijal `
	- *TAGS: CENT0800, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0767Balawi.TajMafriq `
	- *TAGS: CENT0800, PPE, _BULDAN, _JUGHRAFIYA, _RIHLAT, _TARAJIM, _TARIKH*
 * `0768Yafici.MiratJanan `
	- *TAGS: CENT0800, PPE, _TARIKH*
 * `0771Subki.MucjamShuyukh `
	- *TAGS: CENT0800, PPE, _TABAQAT, _TARAJIM*
 * `0771Subki.TabaqatShaficiyaKubra `
	- *TAGS: BIO, CENT0800, COL, PPE, _FIQH, _TABAQAT, _TARAJIM, _TARIKH*
 * `0774IbnKathir.Bidaya `
	- *TAGS: BIO, CENT0800, CHR, COL, PPE, _ASHAB, _IMAM, _NABI, _SHAMAIL, _SIRA, _TARIKH*
 * `0774IbnKathir.TabaqatShaficiyyin `
	- *TAGS: BIO, CENT0800, COL, PPE, _TABAQAT, _TARAJIM*
 * `0774IbnKathir.Takmil `
	- *TAGS: CENT0800, PPE, _TABAQAT, _TARAJIM*
 * `0774IbnRaficSallami.MashyakhaBayani `
	- *TAGS: CENT0800, PPE, _AJZA, _HADITH*
 * `0774IbnRaficSallami.Wafayat `
	- *TAGS: CENT0800, PPE, _TABAQAT, _TARAJIM, _TARIKH*
 * `0775IbnAbiWafa.JawahirMudiya `
	- *TAGS: BIO, CENT0800, COL, PPE, _FIQH, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `0776LisanDinIbnKhatib.Ihata `
	- *TAGS: CENT0800, PPE, _BULDAN, _TABAQAT, _TARAJIM, _TARIKH*
 * `0776LisanDinIbnKhatib.KatibaKamina `
	- *TAGS: CENT0800, PPE, _MISC, _TABAQAT, _TARAJIM*
 * `0776LisanDinIbnKhatib.KhatraTayf `
	- *TAGS: CENT0800, GEO, PPE, _BULDAN, _JUGHRAFIYA, _MISC, _RIHLAT*
 * `0776LisanDinIbnKhatib.MicyarIkhtiyar `
	- *TAGS: CENT0800, GEO, PPE, _BULDAN, _JUGHRAFIYA, _RIHLAT*
 * `0776LisanDinIbnKhatib.NafadaJirab `
	- *TAGS: CENT0800, _BULDAN, _JUGHRAFIYA, _MISC, _RIHLAT*
 * `0779IbnBattuta.Rihla `
	- *TAGS: CENT0800, GEO, PPE, _BULDAN, _JUGHRAFIYA, _MUDHAKKARAT, _RIHLAT, _TARIKH*
 * `0782IbnSallar.TabaqatQurra `
	- *TAGS: BIO, CENT0800, PPE, _QIRAAT, _QURAN, _TAJWID*
 * `0793AbuHasanMalaqi.TarikhQudat `
	- *TAGS: CENT0800, PPE, _TABAQAT, _TARAJIM, _TARIKH*
 * `0795IbnRajabHanbali.DhaylTabaqatHanabila `
	- *TAGS: BIO, CENT0800, COL, PPE, _TABAQAT, _TARAJIM, _TARIKH*
 * `0799IbnFarhun.DibajMudhahhab `
	- *TAGS: CENT0800, PPE, _FIQH, _TABAQAT, _TARAJIM, _TARIKH*

* **0900AH [[ [Re]generated on 2016-08-29 (16:53:58) ]]**

 * `0804IbnMulaqqin.TabaqatAwliya `
	- *TAGS: CENT0900, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `0806IbnHusaynCiraqi.DhaylMizan `
	- *TAGS: BIO, CENT0900, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0807IbnAhmarKhazraji.NafhaNisriniyya `
	- *TAGS: CENT0900, PPE, _BULDAN, _TARIKH*
 * `0808IbnKhaldun.Rihla `
	- *TAGS: CENT0900, GEO, PPE, _BULDAN, _JUGHRAFIYA, _RIHLAT*
 * `0808IbnKhaldun.Tarikh `
	- *TAGS: CENT0900, CHR, PPE, _MISC, _TARIKH*
 * `0809IbnQunfudh.Wafayat `
	- *TAGS: CENT0900, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `0812CaliKhazraji.CuqudLuluiyya `
	- *TAGS: CENT0900, PPE, _TARIKH*
 * `0816AbuBakrMaraghi.Mashyakha `
	- *TAGS: CENT0900, PPE, _AJZA, _HADITH*
 * `0817IbnYacqubFiruzabadi.BulghaFiTarajim `
	- *TAGS: CENT0900, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `0821Qalqashandi.NihayaArab `
	- *TAGS: CENT0900, PPE, _ANSAB*
 * `0821Qalqashandi.QalaidJuman `
	- *TAGS: CENT0900, PPE, _ANSAB, _BULDAN, _TARIKH*
 * `0821Qalqashandi.SubhAcsha `
	- *TAGS: CENT0900, _ADAB, _ADAB, _BALAGHA, _CARUD, _KITABA*
 * `0821ShihabDinQalqashandi.Maathir `
	- *TAGS: CENT0900, _MISC, _QADA, _SIYASA*
 * `0825IbnQasimSabti.IkhtisarAkhbar `
	- *TAGS: CENT0900, PPE, _BULDAN, _JUGHRAFIYA, _RIHLAT*
 * `0826IbnCiraqi.Mudallisin `
	- *TAGS: CENT0900, _TABAQAT, _TARAJIM*
 * `0826IbnCiraqi.TuhfaTahsil `
	- *TAGS: CENT0900, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0832AbuTayyibFasi.DhaylTaqyid `
	- *TAGS: CENT0900, PPE, _FAHARIS, _KUTUB, _TABAQAT, _TARAJIM*
 * `0832AbuTayyibFasi.ShifaGharam `
	- *TAGS: CENT0900, PPE, _TARIKH*
 * `0833IbnJazari.GhayaNihaya `
	- *TAGS: CENT0900, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `0842IbnNasirDinDimashqi.RaddWafir `
	- *TAGS: CENT0900, PPE, _TABAQAT, _TARAJIM, _TARIKH*
 * `0842IbnNasirDinDimashqi.TawdihMushtabih `
	- *TAGS: CENT0900, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0845Maqrizi.Bayan `
	- *TAGS: CENT0900, _BULDAN, _TARIKH*
 * `0845Maqrizi.IqazHunafa `
	- *TAGS: CENT0900, PPE, _BULDAN, _TARIKH*
 * `0845Maqrizi.Mawaciz `
	- *TAGS: CENT0900, PPE, _BULDAN, _JUGHRAFIYA, _RIHLAT*
 * `0845Maqrizi.MukhtasarKamil `
	- *TAGS: CENT0900, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0845Maqrizi.Suluk `
	- *TAGS: CENT0900, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `0851IbnQadiShuhba.TabaqatShaficiya `
	- *TAGS: BIO, CENT0900, COL, PPE, _FIQH, _TABAQAT, _TARAJIM, _TARIKH*
 * `0852IbnHajarCasqalani.DurarKamina `
	- *TAGS: BIO, CENT0900, COL, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `0852IbnHajarCasqalani.FathBari `
	- *TAGS: CENT0900, _FIQH, _HADITH, _SHARH, _SUNNI, _TARAJIM*
 * `0852IbnHajarCasqalani.InbaGhumr `
	- *TAGS: CENT0900, PPE, _TARIKH*
 * `0852IbnHajarCasqalani.IsabaFiTamyiz `
	- *TAGS: CENT0900, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0852IbnHajarCasqalani.ItharBiMacrifa `
	- *TAGS: CENT0900, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0852IbnHajarCasqalani.LisanMizan `
	- *TAGS: BIO, CENT0900, COL, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0852IbnHajarCasqalani.MucjamMufahras `
	- *TAGS: CENT0900, PPE, _ADILLA, _FAHARIS, _KUTUB*
 * `0852IbnHajarCasqalani.MucjamShaykhaMaryam `
	- *TAGS: CENT0900, _HADITH, _MAKHTUTAT*
 * `0852IbnHajarCasqalani.NuzhaAlbab `
	- *TAGS: CENT0900, PPE, _HADITH, _MISC, _TABAQAT, _TARAJIM*
 * `0852IbnHajarCasqalani.RafcCisr `
	- *TAGS: CENT0900, PPE, _TABAQAT, _TARAJIM, _TARIKH*
 * `0852IbnHajarCasqalani.TabaqatMudallisin `
	- *TAGS: BIO, CENT0900, COL, PPE, _HADITH, _SUNNI, _TARAJIM*
 * `0852IbnHajarCasqalani.TabsirMuntabih `
	- *TAGS: CENT0900, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0852IbnHajarCasqalani.TacjilManfaca `
	- *TAGS: CENT0900, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0852IbnHajarCasqalani.TacrifAhlTaqbis `
	- *TAGS: CENT0900, _TABAQAT, _TARAJIM*
 * `0852IbnHajarCasqalani.TahdhibTahdhib `
	- *TAGS: CENT0900, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0852IbnHajarCasqalani.TaqribTahdhib `
	- *TAGS: CENT0900, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0854IbnCarabshah.CajaibMaqdur `
	- *TAGS: CENT0900, _TARAJIM, _TARIKH*
 * `0854IbnDiyaMakki.TarikhMakka `
	- *TAGS: CENT0900, PPE, _BULDAN, _TARIKH*
 * `0855Cayni.CiqdJuman `
	- *TAGS: CENT0900, PPE, _TARIKH*
 * `0855Cayni.CumdaQari `
	- *TAGS: CENT0900, PPE, _FIQH, _HADITH, _SHARH, _SUNNI, _TARAJIM*
 * `0855Cayni.MaghaniAkhyar `
	- *TAGS: CENT0900, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0862IbnMuhammadMujari.Barnamaj `
	- *TAGS: CENT0900, _ADILLA, _FAHARIS, _KUTUB*
 * `0871IbnFahdMakki.LahzAlhaz `
	- *TAGS: BIO, CENT0900, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `0874IbnTaghribirdi.HawadithDahriya `
	- *TAGS: CENT0900, PPE, _TARIKH*
 * `0874IbnTaghribirdi.ManhalSafi `
	- *TAGS: CENT0900, PPE, _TABAQAT, _TARAJIM*
 * `0874IbnTaghribirdi.MawridLatafa `
	- *TAGS: CENT0900, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `0874IbnTaghribirdi.NujumZahira `
	- *TAGS: CENT0900, PPE, _BULDAN, _TARIKH*
 * `0879IbnQutlubugha.TajTarajim `
	- *TAGS: CENT0900, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `0879IbnQutlubugha.Thiqat `
	- *TAGS: CENT0900, PPE, _TABAQAT, _TARAJIM*
 * `0884IbnMuflih.MaqsidArshad `
	- *TAGS: CENT0900, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0884SibtIbnCajami.Ightibat `
	- *TAGS: CENT0900, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0884SibtIbnCajami.KashfHathith `
	- *TAGS: CENT0900, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0884SibtIbnCajami.KunuzDhahab `
	- *TAGS: CENT0900, PPE, _TABAQAT, _TARAJIM*
 * `0884SibtIbnCajami.TabyinLiAsma `
	- *TAGS: CENT0900, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0900AbuCabdAllahHimyari.RawdMictar `
	- *TAGS: CENT0900, COL, GEO, PPE, _BULDAN, _GHARIB, _JUGHRAFIYA, _MACAJIM, _MUSTALAHAT, _RIHLAT*

* **1000AH [[ [Re]generated on 2016-08-29 (16:53:58) ]]**

 * `0902Sakhawi.Buldaniyyat `
	- *TAGS: CENT1000, PPE, _AJZA, _HADITH, _MISC, _TARAJIM*
 * `0902Sakhawi.DuLamic `
	- *TAGS: BIO, CENT1000, COL, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `0902Sakhawi.ManhalCadhb `
	- *TAGS: CENT1000, PPE, _HADITH, _MUSTALAHAT, _TABAQAT, _TARAJIM*
 * `0902Sakhawi.TuhfaLatifa `
	- *TAGS: CENT1000, PPE, _BULDAN, _TABAQAT, _TARAJIM, _TARIKH*
 * `0904Burayhi.TabaqatSulahaYaman `
	- *TAGS: CENT1000, PPE, _BULDAN, _TARIKH*
 * `0905Basrawi.Tarikh `
	- *TAGS: CENT1000, PPE, _BULDAN, _TARIKH*
 * `0909IbnMibradHanbali.BahrDamm `
	- *TAGS: CENT1000, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0909IbnMibradHanbali.MucjamKutub `
	- *TAGS: BIB, CENT1000, PPE, _ADILLA, _FAHARIS, _KUTUB*
 * `0911Samhudi.KhulasaWafaWafa `
	- *TAGS: CENT1000, PPE, _TARIKH*
 * `0911Samhudi.WafaWafa `
	- *TAGS: CENT1000, PPE, _ASHAB, _BULDAN, _JUGHRAFIYA, _RIHLAT, _SIRA*
 * `0911Suyuti.AsmaMudallisin `
	- *TAGS: CENT1000, PPE, _HADITH, _MUSTALAHAT, _TABAQAT, _TARAJIM*
 * `0911Suyuti.AsmaMukhadramin `
	- *TAGS: CENT1000, PPE, _TARAJIM, _TARIKH*
 * `0911Suyuti.BughyaWucat `
	- *TAGS: BIO, CENT1000, COL, PPE, _TABAQAT, _TARAJIM, _TARIKH*
 * `0911Suyuti.DhaylTabaqatHuffaz `
	- *TAGS: CENT1000, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `0911Suyuti.HusnMuhadara `
	- *TAGS: CENT1000, PPE, _BULDAN, _TARIKH*
 * `0911Suyuti.IscafMubatta `
	- *TAGS: CENT1000, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0911Suyuti.ItmamDiraya `
	- *TAGS: CENT1000, _ADILLA, _FAHARIS, _KUTUB*
 * `0911Suyuti.LubbLubab `
	- *TAGS: CENT1000, PPE, _ANSAB, _TARAJIM, _TARIKH*
 * `0911Suyuti.NazmCiqyan `
	- *TAGS: CENT1000, PPE, _TABAQAT, _TARAJIM, _TARIKH*
 * `0911Suyuti.RihNisrin `
	- *TAGS: CENT1000, PPE, _HADITH, _MISC, _TABAQAT, _TARAJIM*
 * `0911Suyuti.Shamarikh `
	- *TAGS: CENT1000, _MISC, _TARIKH*
 * `0911Suyuti.TabaqatHuffaz `
	- *TAGS: BIO, CENT1000, COL, PPE, _HADITH, _TABAQAT, _TARAJIM, _THIQAT*
 * `0911Suyuti.TabaqatMufassirin `
	- *TAGS: CENT1000, PPE, _MUFASSIRUN, _TABAQAT, _TARAJIM, _TARIKH*
 * `0911Suyuti.TarikhKhulafa `
	- *TAGS: CENT1000, PPE, _BULDAN, _TARAJIM, _TARIKH*
 * `0922IbnShaykhTarabulusi.IscafAwqaf `
	- *TAGS: CENT1000, PPE, _BUHUTH, _MASAIL*
 * `0923IbnCabdAllahKhazraji.KhulasaTahdhib `
	- *TAGS: CENT1000, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0927Culaymi.UnsJalil `
	- *TAGS: CENT1000, PPE, _BULDAN, _TARIKH*
 * `0927Nucaymi.DarisFiMadaris `
	- *TAGS: CENT1000, COL, PPE, _MISC, _TARIKH*
 * `0929IbnKayyal.KawakibNayyirat `
	- *TAGS: CENT1000, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0938IbnCaliBalawi.Thabat `
	- *TAGS: BIB, CENT1000, PPE, _ADILLA, _FAHARIS, _KUTUB*
 * `0945ShamsDinDawudi.TabaqatMufassirin `
	- *TAGS: CENT1000, PPE, _TABAQAT, _TARAJIM*
 * `0953IbnTulun.MufakahaKhillan `
	- *TAGS: CENT1000, PPE, _BULDAN, _TARIKH*
 * `0966HusaynDiyarbakri.TarikhKhamis `
	- *TAGS: CENT1000, _SHAMAIL, _SIRA*
 * `0968Tashkubruizadah.ShaqaiqNucmaniyya `
	- *TAGS: BIO, CENT1000, COL, PPE, _FIQH, _TABAQAT, _TARAJIM, _TARIKH*
 * `0973CabdWahhabShacrani.LawaqihAnwar `
	- *TAGS: CENT1000, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `0984BardDinGhazzi.MatalicBadriya `
	- *TAGS: CENT1000, _BULDAN, _JUGHRAFIYA, _RIHLAT*

* **1100AH [[ [Re]generated on 2016-08-29 (16:53:58) ]]**

 * `1010TamimiDari.TabaqatSaniya `
	- *TAGS: BIO, CENT1100, COL, PPE, _TABAQAT, _TARAJIM, _TARIKH*
 * `1011SahibMacalim.TahrirTawusi `
	- *TAGS: CENT1100, PPE, SHC, _HADITH, _SHICI, _TARAJIM*
 * `1016MuhibbDinHamawi.HadiAzcan `
	- *TAGS: CENT1100, GEO, PPE, _BULDAN, _JUGHRAFIYA, _MISC, _RIHLAT*
 * `1037CabdQadirCaydarus.TarikhNurSafir `
	- *TAGS: CENT1100, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `1041BurhanDinMaliki.BahjaMahafil `
	- *TAGS: CENT1100, PPE, _TABAQAT, _TARAJIM*
 * `1041Maqarri.AzharRiyad `
	- *TAGS: CENT1100, PPE, _TABAQAT, _TARAJIM, _TARIKH*
 * `1041Maqarri.NafhTib `
	- *TAGS: CENT1100, PPE, _ADAB, _ADAB, _BALAGHA, _BULDAN, _TARAJIM, _TARIKH*
 * `1051Cimadi.RawdaRayya `
	- *TAGS: CENT1100, PPE, _BULDAN, _HADITH, _TABAQAT, _TARAJIM, _TARIKH*
 * `1061NajmDinGhazzi.KawakibSaira `
	- *TAGS: CENT1100, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `1067HajjiKhalifa.KashfZunun `
	- *TAGS: BIB, CENT1100, COL, PPE, _ADILLA, _FAHARIS, _KUTUB, _MACAJIM*
 * `1069ShihabDinKhafaji.RayhanaAlibba `
	- *TAGS: CENT1100, PPE, _MISC, _TABAQAT, _TARAJIM*
 * `1070MuhammadKibrit.RihlaShita `
	- *TAGS: CENT1100, GEO, PPE, _BULDAN, _JUGHRAFIYA, _RIHLAT*
 * `1078RiyadZadah.AsmaKutub `
	- *TAGS: BIB, CENT1100, PPE, _ADILLA, _FAHARIS, _KUTUB*
 * `1086IbnCajamiMisri.DhaylLubbLubab `
	- *TAGS: CENT1100, ONO, PPE, _ANSAB*
 * `1089IbnCimad.Shadharat `
	- *TAGS: BIO, CENT1100, CHR, COL, PPE, _TARIKH*
 * `1100IbnMuhammadAdnahwi.TabaqatMufassirin `
	- *TAGS: CENT1100, PPE, _MUFASSIRUN, _TABAQAT, _TARAJIM, _TARIKH*
 * `1100MuhammadItlidi.IclamNas `
	- *TAGS: CENT1100, _BULDAN, _TARIKH*
 * `1100MustafaTafrishi.NaqdRijal `
	- *TAGS: BIO, CENT1100, PPE, SHC, _HADITH, _SHICI, _TARAJIM*

* **1200AH [[ [Re]generated on 2016-08-29 (16:53:58) ]]**

 * `1101MuhammadCaliArdabili.JamicRuwat `
	- *TAGS: CENT1200, PPE, SHC, _HADITH, _SHICI, _TARAJIM*
 * `1111MuhammadAminMuhibbi.KhulasaAthr `
	- *TAGS: CENT1200, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `1119IbnMacsum.SulafaCasr `
	- *TAGS: BIO, CENT1200, PPE, _TABAQAT, _TARAJIM, _TARIKH*
 * `1120CaliKhanMadani.DarajatRafica `
	- *TAGS: CENT1200, PPE, SHC, _HADITH, _SHICI, _TARAJIM*
 * `1126MuhammadHanbali.Mashyakha `
	- *TAGS: CENT1200, PPE, _TABAQAT, _TARAJIM*
 * `1147CabdAllahSancani.TarikhYaman `
	- *TAGS: CENT1200, PPE, _BULDAN, _TARIKH*
 * `1153IbnKannan.YawmiyyatShamiyya `
	- *TAGS: CENT1200, PPE, _BULDAN, _TARIKH*
 * `1167IbnCabrRahmanGhazzi.DiwanIslam `
	- *TAGS: CENT1200, _CUTHMANI, _SHICR, _TABAQAT, _TARAJIM*
 * `1172IbnKhalifaMasakini.Fahrasa `
	- *TAGS: CENT1200, _ADILLA, _FAHARIS, _KUTUB*
 * `1174AbuBarakatSuwaydi.NafhaMiskiya `
	- *TAGS: CENT1200, _BULDAN, _JUGHRAFIYA, _RIHLAT*
 * `1175AhmadBudayri.HawadithDimashq `
	- *TAGS: CENT1200, PPE, _BULDAN, _TARIKH*
 * `1175MuhammadKarabisi.IklilManhaj `
	- *TAGS: BIO, CENT1200, PPE, SHC, _HADITH, _SHICI, _TARAJIM*
 * `1187SulaymanMahasini.HululTacab `
	- *TAGS: CENT1200, _TARIKH*
 * `1195CabdRahmanAnsari.Tuhfa `
	- *TAGS: CENT1200, _ANSAB, _MISC*

* **1300AH [[ [Re]generated on 2016-08-29 (16:53:58) ]]**

 * `1206Muradi.SilkDurar `
	- *TAGS: CENT1300, PPE, _TABAQAT, _TARAJIM*
 * `1212BahrCulum.FawaidRijaliya `
	- *TAGS: CENT1300, PPE, SHC, _HADITH, _SHICI, _TARAJIM*
 * `1212BahrCulum.FawaidRijaliya `
	- *TAGS: CENT1300, PPE, SHC, _HADITH, _SHICI, _TARAJIM*
 * `1218SalihFulani.QatfThamar `
	- *TAGS: BIB, CENT1300, PPE, _ADILLA, _FAHARIS, _KUTUB*
 * `1232IbnKhatibCumari.RawdaFayha `
	- *TAGS: CENT1300, PPE, _TABAQAT, _TARAJIM*
 * `1237Jabarti.CajaibAthar `
	- *TAGS: CENT1300, PPE, _TARIKH*
 * `1246IbnHamadBassam.DurarMafakhir `
	- *TAGS: CENT1300, _ANSAB, _TARAJIM, _TARIKH*
 * `1250IbnCaliShaykani.BadrTalic `
	- *TAGS: CENT1300, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `1269CabdMalikCasimi.SamtNujum `
	- *TAGS: CENT1200, PPE, _TARIKH*
 * `1270ShihabDinAlusi.GharaibIghtirab `
	- *TAGS: CENT1300, _BULDAN, _JUGHRAFIYA, _RIHLAT*
 * `1277MuhammadTantawi.NashaNahw `
	- *TAGS: _ADILLA, _CENT00NO, _FAHARIS, _KUTUB*
 * `1285CabdRahmanTamimi.Maqamat `
	- *TAGS: CENT1300, _TABAQAT, _TARAJIM*
 * `1286IcjazHusaynKunturi.KashfHajb `
	- *TAGS: BIB, CENT1300, PPE, _FAHARIS, _KUTUB*

* **1400AH [[ [Re]generated on 2016-08-29 (16:53:58) ]]**

 * `1307Qannawji.AbjadCulum `
	- *TAGS: CENT1400, PPE, _ADILLA, _FAHARIS, _KUTUB, _MACAJIM*
 * `1307Qannawji.HittaFiDhikr `
	- *TAGS: CENT1400, PPE, _ADILLA, _FAHARIS, _KUTUB*
 * `1307Qannawji.LuqtaCajlan `
	- *TAGS: BIB, CENT1400, PPE, _ADILLA, _FAHARIS, _KUTUB*
 * `1313Barujirdi.Taraif `
	- *TAGS: CENT1400, PPE, SHC, _HADITH, _SHICI, _TARAJIM*
 * `1313VanDyck.IktifaQunuc `
	- *TAGS: CENT1400, PPE, _ADILLA, _FAHARIS, _KUTUB*
 * `1315AbuMacaliKalbasi.RasailRijaliyya `
	- *TAGS: CENT1400, PPE, SHC, _HADITH, _SHICI, _TARAJIM*
 * `1315Salawi.IstiqsaLiAhkbar `
	- *TAGS: CENT1400, PPE, _BULDAN, _TARIKH*
 * `1318MuhammadSanusi.Musamarat `
	- *TAGS: CENT1400, PPE, _TABAQAT, _TARAJIM*
 * `1330IbnMusaTabrizi.MiratKutub `
	- *TAGS: BIB, CENT1400, PPE, _FAHARIS, _KUTUB*
 * `1332ZaynabFawwaz.DurrManthur `
	- *TAGS: CENT1400, PPE, _TABAQAT, _TARAJIM*
 * `1335CabdRazzaqBaytar.HilyaBashar `
	- *TAGS: CENT1400, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `1338MuhammadFaridBey.Bahja `
	- *TAGS: CENT1400, PPE, _BULDAN, _TARIKH*
 * `1338MuhammadFaridBey.Tarikh `
	- *TAGS: CENT1400, PPE, _BULDAN, _TARIKH*
 * `1339IsmacilBashaBaghdadi.HadiyaCarifin `
	- *TAGS: BIB, BIO, CENT1400, COL, PPE, _ADILLA, _FAHARIS, _KUTUB*
 * `1339IsmacilBashaBaghdadi.IdahMaknun `
	- *TAGS: BIB, CENT1400, COL, PPE, _ADILLA, _FAHARIS, _KUTUB*
 * `1341CabdHayyTalibi.IclamBiMan `
	- *TAGS: CENT1400, PPE, _TABAQAT, _TARAJIM*
 * `1345IbnJacfarKattani.RisalaMustatrafa `
	- *TAGS: CENT1400, PPE, _ADILLA, _FAHARIS, _KUTUB*
 * `1346CbdQadirBadran.Munadama `
	- *TAGS: CENT1400, PPE, _BULDAN, _JUGHRAFIYA, _MISC, _RIHLAT, _TARIKH*
 * `1347BashirYamut.Shacirat `
	- *TAGS: _CENT00NO, _TABAQAT, _TARAJIM*
 * `1351IbnHusaynGhazzi.NahrDhahab `
	- *TAGS: CENT1400, PPE, _BULDAN, _JUGHRAFIYA, _RIHLAT*
 * `1351YusufIlyanSarkis.MucjamMatbucat `
	- *TAGS: BIB, CENT1400, PPE, _ADILLA, _FAHARIS, _KUTUB*
 * `1354HasanSadr.Takmila `
	- *TAGS: BIO, CENT1400, PPE, _HADITH, _SHICI, _TARAJIM*
 * `1354RashidRida.Manar `
	- *TAGS: CENT1400, _MAJALLAT, _MAJMUCAT*
 * `1355AhmadTahtawi.TanbihWaIqaz `
	- *TAGS: BIO, CENT1400, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `1356AbuHudaKalbasi.SamaMaqal `
	- *TAGS: BIO, CENT1400, COL, PPE, SHC, _HADITH, _SHICI, _TARAJIM*
 * `1359CabbasQummi.Kuna `
	- *TAGS: CENT1400, ONO, PPE, _IMAM, _NABI, _SIRA*
 * `1360IbnQasimMakhluf.ShajaraNur `
	- *TAGS: BIO, CENT1400, COL, PPE, _MISC*
 * `1364IbnHamdMughiri.MuntakhabQabail `
	- *TAGS: CENT1400, _ANSAB, _BULDAN, _TARIKH*
 * `1368HasanAmin.MustadrakatAcyanShica `
	- *TAGS: CENT1400, PPE, _TARIKH*
 * `1371MuhsinCamili.AcyanShica `
	- *TAGS: CENT1400, PPE, _TARIKH*
 * `1372KurdCali.KhitatSham `
	- *TAGS: CENT1400, PPE, _BULDAN, _JUGHRAFIYA, _RIHLAT*
 * `1373AbuYaclaZuwawi.TarikhZuwawa `
	- *TAGS: CENT1400, _TARIKH*
 * `1376CabdRahmanSacdi.Muallafat `
	- *TAGS: CENT1400, PPE, _FAHARIS, _KUTUB*
 * `1376MuhammadHajwiThacalibi.FikrSami `
	- *TAGS: CENT1400, _FIQH, _QAWACID, _USUL*
 * `1381MuhammadSancani.MulhaqBadr `
	- *TAGS: CENT1400, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `1383CadbHayyKattani.FihrisFaharis `
	- *TAGS: BIB, CENT1400, PPE, _FAHARIS, _KUTUB, _TABAQAT, _TARAJIM*
 * `1389AghaBuzurgTihrani.DharicaFiTasanifShica `
	- *TAGS: BIB, CENT1400, PPE, _FAHARIS, _KUTUB*
 * `1389AghaBuzurgTihrani.DhaylKashfZunun `
	- *TAGS: BIB, CENT1400, COL, PPE, _FAHARIS, _KUTUB*
 * `1389AghaBuzurgTihrani.TASHAnwarSatica `
	- *TAGS: CENT1400, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `1389AghaBuzurgTihrani.TASHNawabighRuwat `
	- *TAGS: CENT1400, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `1396KhayrDinZirikli.Aclam `
	- *TAGS: BIO, CENT1400, COL, PPE, _FAHARIS, _KUTUB, _TABAQAT, _TARAJIM*

* **1500AH [[ [Re]generated on 2016-08-29 (16:53:58) ]]**

 * `1405CaliShahrudi.Mustadrakat `
	- *TAGS: CENT1500, PPE, SHC, _HADITH, _SHICI, _TARAJIM*
 * `1408CumarKahhala.MucjamMuallifin `
	- *TAGS: BIB, BIO, CENT1500, COL, PPE, _FAHARIS, _KUTUB, _TABAQAT, _TARAJIM*
 * `1408CumarKahhala.MucjamQabail `
	- *TAGS: CENT1500, COL, GEN, PPE, _ANSAB, _MACAJIM*
 * `1411SayyidKhui.MucjamRijal `
	- *TAGS: CENT1500, PPE, _HADITH, _SHICI, _TARAJIM*
 * `1411SayyidMarcashi.SharhIhqaq `
	- *TAGS: CENT1500, _CAQAID, _SHICI, _TWELVERS*
 * `1414SalimIbadi.IscafAcyan `
	- *TAGS: CENT1500, _ANSAB*
 * `1418SalihAhmadArkani.TihfaMajalis `
	- *TAGS: BIB, CENT1500, PPE, _FAHARIS, _KUTUB*
 * `1419MahmudTanahi.MujizFiMarajic `
	- *TAGS: BIB, CENT1500, PPE, _ADILLA, _FAHARIS, _KUTUB*
 * `1421HamdJasir.MucjamQabailMCS `
	- *TAGS: CENT1500, _ANSAB*
 * `1422IbnHadiWadici.RijalHakim `
	- *TAGS: CENT1500, _TABAQAT, _TARAJIM*
 * `1422MuhammadSalimMuhaysin.MucjamHuffazQuran `
	- *TAGS: CENT1500, PPE, _TABAQAT, _TARAJIM*
 * `1429BakrIbnCabdAllah.TabaqatNassabin `
	- *TAGS: CENT1500, _TABAQAT, _TARAJIM*
 * `1450AbuTayyibMansuri.Irshad `
	- *TAGS: _CENT00NO, _TABAQAT, _TARAJIM*
 * `1450AkramFaluji.MucjamSaghir `
	- *TAGS: CENT1500, _TABAQAT, _TARAJIM*
 * `1450CabdRahmanAlShaykh.Mashahir `
	- *TAGS: CENT1500, PPE, _TABAQAT, _TARAJIM*
 * `1450CadilNuwayhid.MucjamAclamJazair `
	- *TAGS: _CENT00NO, _TABAQAT, _TARAJIM*
 * `1450DarIftaMisriyya.FatawaDarIfta `
	- *TAGS: CENT1500, _FATAWA*
 * `1450MajmacFikrIslami.MawsucaMuallifiImamiya `
	- *TAGS: CENT1500, PPE, _FAHARIS, _KUTUB*
 * `1450MawsucaShicriya.MucjamShucara `
	- *TAGS: _CENT1500, _TABAQAT, _TARAJIM*
 * `1450MuhammadHadiAmini.MucjamMatbicatNajafiya `
	- *TAGS: BIB, CENT1500, PPE, _FAHARIS, _KUTUB*
 * `1450MuhammadKhayrRamadan.TakmilaMucjamMuallifin `
	- *TAGS: BIB, CENT1500, COL, PPE, _TABAQAT, _TARAJIM*
 * `1450MuhammadSancani.NaylWatar `
	- *TAGS: BIO, CENT1500, COL, ORPHAN, PPE*
 * `1450Musannifun.MawsucaMujaza `
	- *TAGS: _CENT1500, _TARIKH*
 * `1450TarhibDawsari.MucjamMuallafatMalikiyya `
	- *TAGS: _ADILLA, _CENT00NO, _FAHARIS, _KUTUB*
 * `1450TarhibDawsari.MucjamMuallafatShaficiyya `
	- *TAGS: _ADILLA, _CENT00NO, _FAHARIS, _KUTUB*
 * `1450WizaraAwqafMisriyya.TarajimMujaza `
	- *TAGS: CENT1500, _TABAQAT, _TARAJIM*


## Statistics on the corpus

| **Category** | **Stats** |
|:--- | ------:|
| Number of text files | 1265 |
| Number of books      | 625 |
| Number of authors    | 407 |
| Length in words (all)| 379,355,486 |
| Length in pages (300 w/p)| 1,264,518 |
| Length in words (unique) | 174,379,056 |
| Length in pages (300 w/p)| 581,263 |


## Summary statistics on the lengths of texts in the corpus

| | Words  | Pages (300 w/p) |
|:--- | ------:| -----:|
| *Min.* | 150 | 0 |
| *1st Qu.* | 32,700 | 109 |
| *Median* | 105,300 | 351 |
| *Mean* | 306,700 | 1,022 |
| *3rd Qu.* | 266,700 | 889 |
| *Max.* | 10,410,000 | 34,700 |


## Texts by length (duplicates excluded)

| Num | TextGroup URI | Words  | Pages (300 w/p) |
| --: | :--- | ------:| -----:|
| 1 | 0571IbnCasakir.TarikhDimashq | 10,412,929 | 34,709 |
| 2 | 0855Cayni.CumdaQari | 4,680,632 | 15,602 |
| 3 | 1371MuhsinCamili.AcyanShica | 4,675,215 | 15,584 |
| 4 | 0742Mizzi.TahdhibKamal | 4,541,150 | 15,137 |
| 5 | 1111Majlisi.BiharAnwar | 4,430,411 | 14,768 |
| 6 | 1411SayyidMarcashi.SharhIhqaq | 4,126,172 | 13,753 |
| 7 | 0852IbnHajarCasqalani.FathBari | 3,545,728 | 11,819 |
| 8 | 0748Dhahabi.TarikhIslam | 3,437,381 | 11,457 |
| 9 | 0748Dhahabi.SiyarAclamNubala | 3,145,544 | 10,485 |
| 10 | 0310Tabari.JamicBayan | 3,041,268 | 10,137 |
| 11 | 1389AghaBuzurgTihrani.DharicaFiTasanifShica | 2,918,325 | 9,727 |
| 12 | 0463KhatibBaghdadi.TarikhBaghdad | 2,621,786 | 8,739 |
| 13 | 1411SayyidKhui.MucjamRijal | 2,594,210 | 8,647 |
| 14 | 0733Nuwayri.NihayaArab | 2,455,687 | 8,185 |
| 15 | 0711IbnManzurIfriqi.MukhtasarTarikhDimashq | 2,408,342 | 8,027 |
| 16 | 0774IbnKathir.Bidaya | 2,329,940 | 7,766 |
| 17 | 0764Safadi.WafiBiWafayat | 1,980,068 | 6,600 |
| 18 | 1450DarIftaMisriyya.FatawaDarIfta | 1,911,816 | 6,372 |
| 19 | 1396KhayrDinZirikli.Aclam | 1,634,967 | 5,449 |
| 20 | 0821Qalqashandi.SubhAcsha | 1,616,289 | 5,387 |
| 21 | 0310Tabari.Tarikh | 1,613,108 | 5,377 |
| 22 | 0808IbnKhaldun.Tarikh | 1,596,529 | 5,321 |
| 23 | 0360Tabarani.MucjamKabir | 1,590,311 | 5,301 |
| 24 | 0355AbuFarajIsbahani.Aghani | 1,537,021 | 5,123 |
| 25 | 0597IbnJawzi.Muntazam | 1,529,894 | 5,099 |
| 26 | 0852IbnHajarCasqalani.TahdhibTahdhib | 1,415,254 | 4,717 |
| 27 | 0630IbnAthirCizzDin.Kamil | 1,385,342 | 4,617 |
| 28 | 0660IbnCadim.BughyatTalib | 1,373,052 | 4,576 |
| 29 | 0902Sakhawi.DuLamic | 1,335,630 | 4,452 |
| 30 | 0874IbnTaghribirdi.NujumZahira | 1,314,867 | 4,382 |
| 31 | 0626YaqutHamawi.MucjamBuldan | 1,274,659 | 4,248 |
| 32 | 0430AbuNucaymIsbahani.HilyaAwliya | 1,227,955 | 4,093 |
| 33 | 0749ShihabDinCumari.MasalikAbsar | 1,182,722 | 3,942 |
| 34 | 0852IbnHajarCasqalani.IsabaFiTamyiz | 1,153,468 | 3,844 |
| 35 | 1408CumarKahhala.MucjamMuallifin | 1,145,173 | 3,817 |
| 36 | 0852IbnHajarCasqalani.LisanMizan | 1,131,427 | 3,771 |
| 37 | 0279Baladhuri.AnsabAshraf | 1,128,932 | 3,763 |
| 38 | 0277AbuHatimRazi.JarhWaTacdil | 1,121,289 | 3,737 |
| 39 | 1089IbnCimad.Shadharat | 1,097,722 | 3,659 |
| 40 | 1405CaliShahrudi.Mustadrakat | 1,015,230 | 3,384 |
| 41 | 0630IbnAthirCizzDin.UsdGhaba | 963,485 | 3,211 |
| 42 | 0365IbnCadiJurjani.KamilFiDucafa | 962,139 | 3,207 |
| 43 | 0561Samcani.Ansab | 943,976 | 3,146 |
| 44 | 0230IbnSacd.TabaqatKubra | 921,111 | 3,070 |
| 45 | 0475IbnMakula.IkmalFiRafcIrtiyab | 868,430 | 2,894 |
| 46 | 0762MughaltayIbnQalij.IkmalTahdhib | 861,631 | 2,872 |
| 47 | 1041Maqarri.NafhTib | 848,136 | 2,827 |
| 48 | 0845Maqrizi.Suluk | 826,074 | 2,753 |
| 49 | 0626YaqutHamawi.MucjamUdaba | 794,903 | 2,649 |
| 50 | 0256Bukhari.TarikhKabir | 791,001 | 2,636 |
| 51 | 0430AbuNucaymIsbahani.MacrifaSahaba | 785,050 | 2,616 |
| 52 | 0845Maqrizi.Mawaciz | 683,850 | 2,279 |
| 53 | 0421Miskawayh.Tajarib | 679,990 | 2,266 |
| 54 | 0681IbnKhallikan.WafayatAcyan | 677,482 | 2,258 |
| 55 | 0771Subki.TabaqatShaficiyaKubra | 676,731 | 2,255 |
| 56 | 1450Musannifun.MawsucaMujaza | 668,172 | 2,227 |
| 57 | 0748Dhahabi.MizanIctidal | 649,090 | 2,163 |
| 58 | 1341CabdHayyTalibi.IclamBiMan | 634,469 | 2,114 |
| 59 | 1111MuhammadAminMuhibbi.KhulasaAthr | 623,533 | 2,078 |
| 60 | 1101MuhammadCaliArdabili.JamicRuwat | 614,459 | 2,048 |
| 61 | 1315AbuMacaliKalbasi.RasailRijaliyya | 613,389 | 2,044 |
| 62 | 0764Safadi.AcyanCasr | 604,057 | 2,013 |
| 63 | 0458Bayhaqi.DalailNubuwwa | 602,949 | 2,009 |
| 64 | 1269CabdMalikCasimi.SamtNujum | 594,712 | 1,982 |
| 65 | 0542IbnBassamShantarini.Dhakhira | 593,086 | 1,976 |
| 66 | 1067HajjiKhalifa.KashfZunun | 580,572 | 1,935 |
| 67 | 0966HusaynDiyarbakri.TarikhKhamis | 552,947 | 1,843 |
| 68 | 0842IbnNasirDinDimashqi.TawdihMushtabih | 550,678 | 1,835 |
| 69 | 1368HasanAmin.MustadrakatAcyanShica | 547,076 | 1,823 |
| 70 | 0354IbnHibban.Thiqat | 535,985 | 1,786 |
| 71 | 1237Jabarti.CajaibAthar | 514,968 | 1,716 |
| 72 | 1100MustafaTafrishi.NaqdRijal | 500,280 | 1,667 |
| 73 | 0879IbnQutlubugha.Thiqat | 473,854 | 1,579 |
| 74 | 1408CumarKahhala.MucjamQabail | 467,206 | 1,557 |
| 75 | 1315Salawi.IstiqsaLiAhkbar | 464,659 | 1,548 |
| 76 | 0776LisanDinIbnKhatib.Ihata | 462,435 | 1,541 |
| 77 | 0255Jahiz.Hayawan | 455,685 | 1,518 |
| 78 | 1351IbnHusaynGhazzi.NahrDhahab | 434,840 | 1,449 |
| 79 | 0855Cayni.MaghaniAkhyar | 426,063 | 1,420 |
| 80 | 0768Yafici.MiratJanan | 424,088 | 1,413 |
| 81 | 0852IbnHajarCasqalani.DurarKamina | 414,702 | 1,382 |
| 82 | 1372KurdCali.KhitatSham | 414,117 | 1,380 |
| 83 | 0463IbnCabdBarr.IsticabFiMacrifaAshab | 413,421 | 1,378 |
| 84 | 1339IsmacilBashaBaghdadi.HadiyaCarifin | 412,771 | 1,375 |
| 85 | 0852IbnHajarCasqalani.InbaGhumr | 410,739 | 1,369 |
| 86 | 1351YusufIlyanSarkis.MucjamMatbucat | 401,654 | 1,338 |
| 87 | 0902Sakhawi.TuhfaLatifa | 394,353 | 1,314 |
| 88 | 0637IbnMustafwi.TarikhIrbil | 385,144 | 1,283 |
| 89 | 0597CimadDinKatib.KharidaQasr | 385,025 | 1,283 |
| 90 | 0346Mascudi.MurujDhahab | 382,786 | 1,275 |
| 91 | 0911Samhudi.WafaWafa | 376,631 | 1,255 |
| 92 | 0874IbnTaghribirdi.ManhalSafi | 368,687 | 1,228 |
| 93 | 0429AbuMansurThacalibi.YatimaDahr | 362,496 | 1,208 |
| 94 | 1206Muradi.SilkDurar | 358,759 | 1,195 |
| 95 | 0623Qazwini.Tadwin | 353,391 | 1,177 |
| 96 | 0676Nawawi.TahdhibAsma | 352,183 | 1,173 |
| 97 | 0262AbuZaydNumayri.TarikhMadina | 351,743 | 1,172 |
| 98 | 1335CabdRazzaqBaytar.HilyaBashar | 346,616 | 1,155 |
| 99 | 0630IbnAthirCizzDin.LubabFiTahdhibAnsab | 341,753 | 1,139 |
| 100 | 0277IbnSyfyanFasawi.MacrifaWaTarikh | 340,450 | 1,134 |
| 101 | 1212BahrCulum.FawaidRijaliya | 338,918 | 1,129 |
| 102 | 0833IbnJazari.GhayaNihaya | 338,862 | 1,129 |
| 103 | 0748Dhahabi.TadhkiraHuffaz | 337,969 | 1,126 |
| 104 | 1313Barujirdi.Taraif | 331,121 | 1,103 |
| 105 | 0597IbnJawzi.SifaSafwa | 330,284 | 1,100 |
| 106 | 0923IbnCabdAllahKhazraji.KhulasaTahdhib | 328,135 | 1,093 |
| 107 | 0642IbnNajjar.DhaylTarikhBaghdad | 326,501 | 1,088 |
| 108 | 0372AbuSacidQayruwani.TahdhibMudawwana | 325,423 | 1,084 |
| 109 | 0726Yunini.DhaylMiratZaman | 323,810 | 1,079 |
| 110 | 0544CiyadIbnMusaYahsubi.TartibMadarik | 322,807 | 1,076 |
| 111 | 0900AbuCabdAllahHimyari.RawdMictar | 322,499 | 1,074 |
| 112 | 0665AbuShama.Rawdatayn | 317,787 | 1,059 |
| 113 | 0732AbuFida.MukhtasarFiAkhbar | 316,828 | 1,056 |
| 114 | 0322AbuJacfarCuqayli.DucafaKabir | 314,435 | 1,048 |
| 115 | 0911Suyuti.AsmaMudallisin | 306,751 | 1,022 |
| 116 | 0832AbuTayyibFasi.ShifaGharam | 305,946 | 1,019 |
| 117 | 0658IbnAbbar.TakmilaLiSila | 303,591 | 1,011 |
| 118 | 1359CabbasQummi.Kuna | 299,903 | 999 |
| 119 | 1360IbnQasimMakhluf.ShajaraNur | 299,618 | 998 |
| 120 | 0646IbnQifti.InbahRuwat | 295,800 | 986 |
| 121 | 1383CadbHayyKattani.FihrisFaharis | 295,736 | 985 |
| 122 | 0213IbnHisham.SiraNabawiyya | 295,600 | 985 |
| 123 | 0487AbuCubaydBakri.MucjamMaIstacjama | 291,075 | 970 |
| 124 | 1339IsmacilBashaBaghdadi.IdahMaknun | 288,661 | 962 |
| 125 | 0764IbnShakirKutubi.FawatWafayat | 288,315 | 961 |
| 126 | 0855Cayni.CiqdJuman | 274,376 | 914 |
| 127 | 1307Qannawji.AbjadCulum | 274,005 | 913 |
| 128 | 0732IbnYacqubJanadi.SulukFiTabaqat | 272,623 | 908 |
| 129 | 0748Dhahabi.CibarFiKhabar | 270,945 | 903 |
| 130 | 0272Fakihi.AkhbarMakka | 269,999 | 899 |
| 131 | 0779IbnBattuta.Rihla | 267,265 | 890 |
| 132 | 1318MuhammadSanusi.Musamarat | 266,110 | 887 |
| 133 | 0287Dahhak.AhadWaMathani | 265,863 | 886 |
| 134 | 0207Waqidi.Maghazi | 264,920 | 883 |
| 135 | 0430AbuNucaymIsbahani.TarikhIsbahan | 260,298 | 867 |
| 136 | 0774IbnKathir.Takmil | 255,916 | 853 |
| 137 | 0668IbnAbiUsaybica.CuyunAnba | 253,484 | 844 |
| 138 | 0749IbnWardi.Tarikh | 252,903 | 843 |
| 139 | 1450AkramFaluji.MucjamSaghir | 251,265 | 837 |
| 140 | 0354IbnHibban.Majruhin | 250,389 | 834 |
| 141 | 1450MajmacFikrIslami.MawsucaMuallifiImamiya | 249,154 | 830 |
| 142 | 0207Waqidi.FutuhSham | 248,628 | 828 |
| 143 | 1061NajmDinGhazzi.KawakibSaira | 242,384 | 807 |
| 144 | 1332ZaynabFawwaz.DurrManthur | 238,367 | 794 |
| 145 | 0306IbnHayyanDabbi.AkhbarQudat | 237,235 | 790 |
| 146 | 0748Dhahabi.Kashif | 235,822 | 786 |
| 147 | 1376MuhammadHajwiThacalibi.FikrSami | 234,888 | 782 |
| 148 | 0973CabdWahhabShacrani.LawaqihAnwar | 232,710 | 775 |
| 149 | 0629IbnNuqta.TakmilaIkmal | 231,460 | 771 |
| 150 | 0775IbnAbiWafa.JawahirMudiya | 230,720 | 769 |
| 151 | 0460ShaykhTusi.IkhtiyarMacrifaRijal | 227,637 | 758 |
| 152 | 1356AbuHudaKalbasi.SamaMaqal | 226,396 | 754 |
| 153 | 0927Nucaymi.DarisFiMadaris | 224,568 | 748 |
| 154 | 0739SafiDinHanbali.Marasid | 220,179 | 733 |
| 155 | 0927Culaymi.UnsJalil | 218,375 | 727 |
| 156 | 0317AbuQasimBaghawi.MucjamSahaba | 218,356 | 727 |
| 157 | 0911Suyuti.HusnMuhadara | 218,158 | 727 |
| 158 | 0463KhatibBaghdadi.MuttafiqWaMuftariq | 218,096 | 726 |
| 159 | 0852IbnHajarCasqalani.TaqribTahdhib | 217,589 | 725 |
| 160 | 0241IbnHanbal.CilalWaMacrifa | 214,328 | 714 |
| 161 | 0795IbnRajabHanbali.DhaylTabaqatHanabila | 213,679 | 712 |
| 162 | 0852IbnHajarCasqalani.TabsirMuntabih | 209,171 | 697 |
| 163 | 0560SharifIdrisi.NuzhaMushtaq | 207,532 | 691 |
| 164 | 0385Daruqutni.MutalifWaMukhtalif | 207,158 | 690 |
| 165 | 0694MuhibbDinTabari.RiyadNadira | 205,681 | 685 |
| 166 | 1175MuhammadKarabisi.IklilManhaj | 203,395 | 677 |
| 167 | 0911Suyuti.BughyaWucat | 197,961 | 659 |
| 168 | 0400IbnTahirMaqdisi.BadWaTarikh | 197,348 | 657 |
| 169 | 0571IbnCasakir.MucjamShuyukh | 195,776 | 652 |
| 170 | 0645TilimsaniBurri.Jawhara | 194,697 | 648 |
| 171 | 0292Yacqubi.TarikhYacqubi | 193,018 | 643 |
| 172 | 1250IbnCaliShaykani.BadrTalic | 192,663 | 642 |
| 173 | 0347IbnYunusSadafi.Tarikh | 190,889 | 636 |
| 174 | 1450MuhammadKhayrRamadan.TakmilaMucjamMuallifin | 189,829 | 632 |
| 175 | 0561Samcani.Muntakhab | 188,251 | 627 |
| 176 | 0463KhatibBaghdadi.TalkhisMutashabih | 187,352 | 624 |
| 177 | 0310IbnAhmadDulabi.KunaWaAsma | 186,967 | 623 |
| 178 | 1041Maqarri.AzharRiyad | 185,770 | 619 |
| 179 | 0845Maqrizi.IqazHunafa | 185,230 | 617 |
| 180 | 0852IbnHajarCasqalani.MucjamMufahras | 183,759 | 612 |
| 181 | 0487AbuCubaydBakri.MasalikWaMamalik | 181,326 | 604 |
| 182 | 0774IbnKathir.TabaqatShaficiyyin | 180,884 | 602 |
| 183 | 0474IbnKhalafBaji.TacdilWaTakhrij | 180,381 | 601 |
| 184 | 0832AbuTayyibFasi.DhaylTaqyid | 177,958 | 593 |
| 185 | 1120CaliKhanMadani.DarajatRafica | 174,564 | 581 |
| 186 | 0255Jahiz.Rasail | 172,282 | 574 |
| 187 | 0521IbnAbiYacla.TabaqatHanabila | 171,812 | 572 |
| 188 | 0508FattalNaysaburi.RawdaWacizin | 170,713 | 569 |
| 189 | 0255Jahiz.BayanWaTabyin | 170,368 | 567 |
| 190 | 0884SibtIbnCajami.KunuzDhahab | 170,224 | 567 |
| 191 | 1422MuhammadSalimMuhaysin.MucjamHuffazQuran | 169,932 | 566 |
| 192 | 0911Samhudi.KhulasaWafaWafa | 168,018 | 560 |
| 193 | 0812CaliKhazraji.CuqudLuluiyya | 167,694 | 558 |
| 194 | 0615MuwaffaqDinShafici.MurshidZuwwar | 167,271 | 557 |
| 195 | 1119IbnMacsum.SulafaCasr | 165,783 | 552 |
| 196 | 0421IbnMuhammadMarzuqi.AzminaWaAmkina | 165,458 | 551 |
| 197 | 0511SalmaSahari.Ansab | 162,120 | 540 |
| 198 | 1010TamimiDari.TabaqatSaniya | 161,681 | 538 |
| 199 | 0597IbnJawzi.TalqihFuhum | 160,269 | 534 |
| 200 | 1011SahibMacalim.TahrirTawusi | 157,260 | 524 |
| 201 | 1450MawsucaShicriya.MucjamShucara | 155,885 | 519 |
| 202 | 1338MuhammadFaridBey.Tarikh | 155,747 | 519 |
| 203 | 0279IbnAbiKhaythama.TarikhKabir | 155,627 | 518 |
| 204 | 0535QawwamSunna.SiyarSalaf | 154,547 | 515 |
| 205 | 0695IbnCidhariMarrakushi.BayanMaghrib | 153,641 | 512 |
| 206 | 0748Dhahabi.MucjamShuyukh | 152,971 | 509 |
| 207 | 1422IbnHadiWadici.RijalHakim | 152,657 | 508 |
| 208 | 0365IbnFaqihHamadhani.Buldan | 147,644 | 492 |
| 209 | 0682ZakariyaQazwini.AtharBilad | 146,837 | 489 |
| 210 | 0696IbnZahiri.Mashyakha | 146,557 | 488 |
| 211 | 0968Tashkubruizadah.ShaqaiqNucmaniyya | 145,615 | 485 |
| 212 | 1450AbuTayyibMansuri.Irshad | 144,616 | 482 |
| 213 | 0845Maqrizi.MukhtasarKamil | 142,932 | 476 |
| 214 | 0821ShihabDinQalqashandi.Maathir | 142,487 | 474 |
| 215 | 0385IbnNadim.Fihrist | 141,796 | 472 |
| 216 | 0945ShamsDinDawudi.TabaqatMufassirin | 139,971 | 466 |
| 217 | 1376CabdRahmanSacdi.Muallafat | 139,967 | 466 |
| 218 | 0351IbnQanic.MucjamSahaba | 139,882 | 466 |
| 219 | 0578IbnBashkuwal.Sila | 139,365 | 464 |
| 220 | 0709CaliCalawi.Majdi | 138,926 | 463 |
| 221 | 0249Azraqi.AkhbarMakka | 136,671 | 455 |
| 222 | 0576IbnMuhammadSilafi.MashyakhaBaghdadiyya | 135,363 | 451 |
| 223 | 0245MuhammadIbnHabib.MunammaqFiAkhbarQuraysh | 135,021 | 450 |
| 224 | 0703MuhammadMarrakushi.DhaylWaTakmila | 133,973 | 446 |
| 225 | 0911Suyuti.TarikhKhulafa | 133,130 | 443 |
| 226 | 0241IbnHanbal.FadailSahaba | 132,367 | 441 |
| 227 | 0369AbuShaykhIsbahani.TabaqatMuhaddithin | 132,063 | 440 |
| 228 | 0456IbnHazm.JamharaAnsab | 130,859 | 436 |
| 229 | 0852IbnHajarCasqalani.TacjilManfaca | 127,930 | 426 |
| 230 | 0953IbnTulun.MufakahaKhillan | 127,338 | 424 |
| 231 | 1286IcjazHusaynKunturi.KashfHajb | 126,032 | 420 |
| 232 | 0395IbnMandahMuhammad.FathBab | 124,908 | 416 |
| 233 | 0279Baladhuri.FutuhBuldan | 124,892 | 416 |
| 234 | 0428IbnManjuwayhIsbahani.RijalSahihMuslim | 124,175 | 413 |
| 235 | 0367IbnHawqal.SuraArd | 123,793 | 412 |
| 236 | 0884IbnMuflih.MaqsidArshad | 123,777 | 412 |
| 237 | 0852IbnHajarCasqalani.RafcCisr | 123,094 | 410 |
| 238 | 0276IbnQutaybaDinawari.Macarif | 121,880 | 406 |
| 239 | 0565IbnZaydBayhaqi.TarikhBayhaq | 121,037 | 403 |
| 240 | 0555IbnQalanisi.Tarikh | 120,986 | 403 |
| 241 | 0449AbuCalaMacarri.Diwan | 120,379 | 401 |
| 242 | 0429Thacalibi.ThimarQulub | 119,721 | 399 |
| 243 | 0228IbnHammadKhuzaci.Fitan | 119,494 | 398 |
| 244 | 0851IbnQadiShuhba.TabaqatShaficiya | 119,436 | 398 |
| 245 | 0748Dhahabi.MughniFiDucafa | 119,182 | 397 |
| 246 | 0403IbnFaradi.TarikhCulamaAndalus | 118,911 | 396 |
| 247 | 0575IbnKhayrIshbili.Fahrasa | 117,769 | 392 |
| 248 | 0771Subki.MucjamShuyukh | 117,371 | 391 |
| 249 | 0599IbnYahyaDabbi.BughyaMultamis | 116,987 | 389 |
| 250 | 0684IbnShaddad.AclaqKhatira | 116,670 | 388 |
| 251 | 0257IbnCabdHakam.FutuhMisr | 116,282 | 387 |
| 252 | 0427HamzaJurjani.TarikhJurjan | 114,881 | 382 |
| 253 | 0799IbnFarhun.DibajMudhahhab | 114,355 | 381 |
| 254 | 1037CabdQadirCaydarus.TarikhNurSafir | 113,966 | 379 |
| 255 | 1270ShihabDinAlusi.GharaibIghtirab | 113,165 | 377 |
| 256 | 0233YahyaIbnMacin.TarikhIbnMacin | 112,871 | 376 |
| 257 | 0629IbnNuqta.TaqyidLiMacrifa | 112,296 | 374 |
| 258 | 1313VanDyck.IktifaQunuc | 112,098 | 373 |
| 259 | 0213IbnHisham.Tijan | 111,971 | 373 |
| 260 | 0440AbuRayhanBiruni.TahqiqMaLilHind | 111,411 | 371 |
| 261 | 1346CbdQadirBadran.Munadama | 110,741 | 369 |
| 262 | 0660IbnCadim.ZubdaHalab | 110,479 | 368 |
| 263 | 0578IbnBashkuwal.GhawamidAsma | 110,027 | 366 |
| 264 | 0354IbnHibban.Sira | 109,974 | 366 |
| 265 | 0561Samcani.Tahbir | 109,525 | 365 |
| 266 | 0685IbnSacidMaghribi.Mughrib | 109,402 | 364 |
| 267 | 0685IbnCibri.TarikhMukhtasarDuwal | 109,030 | 363 |
| 268 | 0240KhalifaIbnKhayyat.Tarikh | 108,050 | 360 |
| 269 | 0726CallamaHilli.KhulasaAqwal | 106,878 | 356 |
| 270 | 0300MuallifMajhul.AkhbarDawlaCabbasiya | 106,130 | 353 |
| 271 | 0748Dhahabi.DiwanDucafa | 105,284 | 350 |
| 272 | 0748Dhahabi.MukhtasarMinDubaythi | 103,004 | 343 |
| 273 | 0240KhalifaIbnKhayyat.Tabaqat | 102,233 | 340 |
| 274 | 0597IbnJawzi.DucafaWaMatrukin | 100,991 | 336 |
| 275 | 1450CadilNuwayhid.MucjamAclamJazair | 100,098 | 333 |
| 276 | 0658IbnAbbar.HullaSiyara | 98,508 | 328 |
| 277 | 0390Muqaddasi.AhsanTaqasim | 98,198 | 327 |
| 278 | 0507AbuBakrShashi.HilyaCulama | 98,130 | 327 |
| 279 | 0282AbuHanifaDinawari.AkhbarTiwal | 97,880 | 326 |
| 280 | 0576IbnMuhammadSilafi.MucjamSafar | 97,869 | 326 |
| 281 | 0748Dhahabi.MacrifaQurraKibar | 97,714 | 325 |
| 282 | 0821Qalqashandi.NihayaArab | 97,039 | 323 |
| 283 | 0646IbnQifti.IkhbarCulama | 96,909 | 323 |
| 284 | 0641Sarifini.Muntakhab | 96,486 | 321 |
| 285 | 0575IbnBabawayh.Fihrist | 96,438 | 321 |
| 286 | 1041BurhanDinMaliki.BahjaMahafil | 96,298 | 320 |
| 287 | 0854IbnDiyaMakki.TarikhMakka | 96,272 | 320 |
| 288 | 0448HilalSabi.TuhfaUmara | 95,725 | 319 |
| 289 | 0600AbuBaqaHilli.ManaqibMazidiya | 95,644 | 318 |
| 290 | 0580IbnCimrani.InbaFiTarikhKhulafa | 92,814 | 309 |
| 291 | 0398AbuNasrKalabadhi.HidayaWaIrshad | 90,817 | 302 |
| 292 | 0395IbnMandahMuhammad.MacrifaSahaba | 90,565 | 301 |
| 293 | 0741KhatibTabrizi.Ikmal | 90,307 | 301 |
| 294 | 0236AbuCabdAllahZubayri.NasabQuraysh | 90,262 | 300 |
| 295 | 0450Najashi.Rijal | 90,256 | 300 |
| 296 | 0204IbnKalbi.NasabMacad | 88,977 | 296 |
| 297 | 1330IbnMusaTabrizi.MiratKutub | 88,818 | 296 |
| 298 | 0460ShaykhTusi.Rijal | 88,503 | 295 |
| 299 | 1354HasanSadr.Takmila | 88,094 | 293 |
| 300 | 0346Mascudi.TanbihWaIshraf | 87,579 | 291 |
| 301 | 0355MuhammadKindi.WulatMisr | 86,621 | 288 |
| 302 | 0256Bukhari.TarikhSaghir | 86,362 | 287 |
| 303 | 0384IbnCimranMarzubani.MucjamShucara | 86,047 | 286 |
| 304 | 0256ZubayrIbnBakkar.AkhbarMuwaffaqiyat | 85,750 | 285 |
| 305 | 0255Jahiz.Cuthmaniya | 85,453 | 284 |
| 306 | 0488IbnFutuhHumaydi.JadhwaMuqtabis | 85,167 | 283 |
| 307 | 0597CimadDinKatib.BarqShami | 84,900 | 283 |
| 308 | 0528FathIbnKhaqan.QalaidCiqyan | 84,437 | 281 |
| 309 | 1389AghaBuzurgTihrani.TASHNawabighRuwat | 84,082 | 280 |
| 310 | 0446AbuYaclaKhalili.IrshadFiMacrifaCulama | 82,456 | 274 |
| 311 | 0694MuhibbDinTabari.Dhakhair | 81,328 | 271 |
| 312 | 0597IbnJawzi.MuthirGharam | 81,078 | 270 |
| 313 | 1100MuhammadItlidi.IclamNas | 80,344 | 267 |
| 314 | 0292Bahshal.TarikhWasit | 80,039 | 266 |
| 315 | 1153IbnKannan.YawmiyyatShamiyya | 79,567 | 265 |
| 316 | 0748Dhahabi.Muqtana | 77,096 | 256 |
| 317 | 0261AbuHasanCijli.MacrifaThiqat | 76,492 | 254 |
| 318 | 0658IbnAbbar.MucjamAshab | 76,471 | 254 |
| 319 | 0761IbnKaykaldi.JamicTahsil | 76,460 | 254 |
| 320 | 0565IbnZaydBayhaqi.LubabAnsab | 76,424 | 254 |
| 321 | 0749IbnWardi.KharidaCajaib | 75,947 | 253 |
| 322 | 0281AbuZurcaDimashqi.Tarikh | 75,765 | 252 |
| 323 | 0346Istakhri.MasalikWaMamalik | 75,599 | 251 |
| 324 | 0733IbnJamaca.Mashyakha | 75,126 | 250 |
| 325 | 0614IbnJubayr.Rihla | 74,329 | 247 |
| 326 | 0764Safadi.NaktHimyan | 74,306 | 247 |
| 327 | 0904Burayhi.TabaqatSulahaYaman | 74,213 | 247 |
| 328 | 0767Balawi.TajMafriq | 73,852 | 246 |
| 329 | 0911Suyuti.TabaqatHuffaz | 73,614 | 245 |
| 330 | 0535QawwamSunna.DalailNubuwwa | 72,728 | 242 |
| 331 | 0854IbnCarabshah.CajaibMaqdur | 72,705 | 242 |
| 332 | 1174AbuBarakatSuwaydi.NafhaMiskiya | 71,961 | 239 |
| 333 | 0723IbnFuwati.Hawadith | 71,739 | 239 |
| 334 | 0730MuhammadTujibi.Barnamaj | 71,375 | 237 |
| 335 | 0748Dhahabi.MukhtasarCuluww | 71,152 | 237 |
| 336 | 0334IbnHaikHamdani.SifaJaziraCarab | 70,929 | 236 |
| 337 | 0647CabdWahidMarrakushi.Mucjib | 70,871 | 236 |
| 338 | 0255Jahiz.MahasinWaAddad | 70,477 | 234 |
| 339 | 0333AbuCarabTamimi.Mihan | 70,365 | 234 |
| 340 | 0261Muslim.KunaWaAsma | 70,202 | 234 |
| 341 | 0296IbnMuctazz.TabaqatShucara | 69,665 | 232 |
| 342 | 0276IbnQutaybaDinawari.AdabKatib | 69,368 | 231 |
| 343 | 1147CabdAllahSancani.TarikhYaman | 69,040 | 230 |
| 344 | 0673AbuMahasinYaghmuri.NurQabas | 68,955 | 229 |
| 345 | 0750AbuHafsQazwini.Mashyakha | 68,872 | 229 |
| 346 | 0412Sulami.TabaqatSufiya | 68,774 | 229 |
| 347 | 1195CabdRahmanAnsari.Tuhfa | 68,557 | 228 |
| 348 | 0740IbnDawudHilli.Rijal | 68,088 | 226 |
| 349 | 1307Qannawji.HittaFiDhikr | 67,880 | 226 |
| 350 | 1421HamdJasir.MucjamQabailMCS | 67,689 | 225 |
| 351 | 0690IbnMujawirDimashqi.TarikhMustabsir | 65,633 | 218 |
| 352 | 0639AbuBakrMalaqi.MatlacAnwar | 65,139 | 217 |
| 353 | 0584IbnMusaHazimi.Amakin | 64,697 | 215 |
| 354 | 0816AbuBakrMaraghi.Mashyakha | 64,167 | 213 |
| 355 | 0346Mascudi.AkhbarZaman | 63,951 | 213 |
| 356 | 1232IbnKhatibCumari.RawdaFayha | 63,383 | 211 |
| 357 | 0643IbnSalahShahrazuri.TabaqatFuqaha | 63,126 | 210 |
| 358 | 0826IbnCiraqi.TuhfaTahsil | 62,996 | 209 |
| 359 | 1450CabdRahmanAlShaykh.Mashahir | 62,418 | 208 |
| 360 | 0871IbnFahdMakki.LahzAlhaz | 62,047 | 206 |
| 361 | 0793AbuHasanMalaqi.TarikhQudat | 62,043 | 206 |
| 362 | 0938IbnCaliBalawi.Thabat | 61,539 | 205 |
| 363 | 0774IbnRaficSallami.Wafayat | 61,135 | 203 |
| 364 | 0600KatibMarrakushi.Istibsar | 60,550 | 201 |
| 365 | 0521MuhammadHamadhani.TakmilaTarikhTabari | 60,016 | 200 |
| 366 | 1307Qannawji.LuqtaCajlan | 59,600 | 198 |
| 367 | 0874IbnTaghribirdi.MawridLatafa | 59,510 | 198 |
| 368 | 1338MuhammadFaridBey.Bahja | 59,305 | 197 |
| 369 | 0714AhmadGhibrini.CunwanDiraya | 58,461 | 194 |
| 370 | 0395AbuHilalCaskari.Talkhis | 57,835 | 192 |
| 371 | 1069ShihabDinKhafaji.RayhanaAlibba | 57,614 | 192 |
| 372 | 0911Suyuti.LubbLubab | 57,394 | 191 |
| 373 | 0646IbnQifti.Muhammadun | 57,364 | 191 |
| 374 | 0255Jahiz.BursanWaCurjan | 57,316 | 191 |
| 375 | 0256ZubayrIbnBakkar.JamharaNasabQuraysh | 56,650 | 188 |
| 376 | 0310Tabari.MuntakhabMinDhayl | 56,329 | 187 |
| 377 | 0808IbnKhaldun.Rihla | 55,833 | 186 |
| 378 | 1167IbnCabrRahmanGhazzi.DiwanIslam | 55,685 | 185 |
| 379 | 0909IbnMibradHanbali.BahrDamm | 55,202 | 184 |
| 380 | 0255Jahiz.Bukhala | 55,171 | 183 |
| 381 | 0475IbnMakula.TahdhibMustamirr | 55,129 | 183 |
| 382 | 0231IbnSallamJumahi.TabaqatFuhulShucara | 54,921 | 183 |
| 383 | 0776LisanDinIbnKhatib.KatibaKamina | 54,854 | 182 |
| 384 | 0804IbnMulaqqin.TabaqatAwliya | 54,595 | 181 |
| 385 | 0765AbuMahasinHusayni.IkmalLiRijal | 54,306 | 181 |
| 386 | 0911Suyuti.ItmamDiraya | 54,179 | 180 |
| 387 | 0280IbnTayfur.BallaghatNisa | 53,601 | 178 |
| 388 | 1277MuhammadTantawi.NashaNahw | 52,381 | 174 |
| 389 | 0776LisanDinIbnKhatib.NafadaJirab | 52,268 | 174 |
| 390 | 0884SibtIbnCajami.KashfHathith | 52,220 | 174 |
| 391 | 0748Dhahabi.Culuww | 51,813 | 172 |
| 392 | 0370IbnBishrAmidi.MutalifWaMukhtalif | 51,486 | 171 |
| 393 | 1381MuhammadSancani.MulhaqBadr | 51,442 | 171 |
| 394 | 0782IbnSallar.TabaqatQurra | 51,171 | 170 |
| 395 | 0296IbnMuctazz.Diwan | 51,131 | 170 |
| 396 | 0606IbnMamati.LataifDhakhira | 51,074 | 170 |
| 397 | 1070MuhammadKibrit.RihlaShita | 50,647 | 168 |
| 398 | 0550AbuHajjajAshcari.TacrifBiAnsab | 50,496 | 168 |
| 399 | 0748IbnDimyati.Mustafad | 50,153 | 167 |
| 400 | 0806IbnHusaynCiraqi.DhaylMizan | 49,484 | 164 |
| 401 | 0280IbnTayfur.Baghdad | 48,570 | 161 |
| 402 | 0611SharafDinMuqaddasi.Arbacin | 47,514 | 158 |
| 403 | 0569CumaraHakami.NukatCasriyya | 47,005 | 156 |
| 404 | 0984BardDinGhazzi.MatalicBadriya | 46,951 | 156 |
| 405 | 0354IbnHibban.MashahirCulamaAmsar | 45,365 | 151 |
| 406 | 0617MansurIbnShahanshah.MidmarHaqaiq | 45,270 | 150 |
| 407 | 0233YahyaIbnMacin.MacrifaRijal | 45,156 | 150 |
| 408 | 0749Wadiashi.Barnamaj | 44,950 | 149 |
| 409 | 1450MuhammadHadiAmini.MucjamMatbicatNajafiya | 44,242 | 147 |
| 410 | 0748Dhahabi.MucjamMuhaddithin | 44,241 | 147 |
| 411 | 0577IbnAnbari.NuzhaAlibba | 43,683 | 145 |
| 412 | 0922IbnShaykhTarabulusi.IscafAwqaf | 43,648 | 145 |
| 413 | 0852IbnHajarCasqalani.NuzhaAlbab | 43,292 | 144 |
| 414 | 0584IbnMunqidhShayzari.Ictibar | 42,824 | 142 |
| 415 | 0507IbnQaysarani.AnsabMuttafiqa | 42,469 | 141 |
| 416 | 1364IbnHamdMughiri.MuntakhabQabail | 42,407 | 141 |
| 417 | 0680IbnSabuni.TakmilaIkmalIkmal | 42,252 | 140 |
| 418 | 0300IbnKhurdadhbih.MasalikWaMamalik | 41,035 | 136 |
| 419 | 0436HusaynSaymari.AkhbarAbiHanifa | 41,024 | 136 |
| 420 | 0337IbnIshaqZajjaji.Akhbar | 40,895 | 136 |
| 421 | 1100IbnMuhammadAdnahwi.TabaqatMufassirin | 40,783 | 135 |
| 422 | 0476AbuIshaqShirazi.TabaqatFuqaha | 40,668 | 135 |
| 423 | 0320CaribQurtubi.SilaTarikhTabari | 39,699 | 132 |
| 424 | 0905Basrawi.Tarikh | 39,659 | 132 |
| 425 | 1345IbnJacfarKattani.RisalaMustatrafa | 39,163 | 130 |
| 426 | 0388Shabushti.Diyarat | 38,993 | 129 |
| 427 | 0817IbnYacqubFiruzabadi.BulghaFiTarajim | 38,540 | 128 |
| 428 | 0902Sakhawi.Buldaniyyat | 37,943 | 126 |
| 429 | 0207Waqidi.Ridda | 37,811 | 126 |
| 430 | 1347BashirYamut.Shacirat | 37,705 | 125 |
| 431 | 1389AghaBuzurgTihrani.TASHAnwarSatica | 37,497 | 124 |
| 432 | 0748Dhahabi.DhaylCibar | 37,477 | 124 |
| 433 | 0463KhatibBaghdadi.SabiqWaLahiq | 37,301 | 124 |
| 434 | 0685IbnSacidMaghribi.Jughrafiya | 35,291 | 117 |
| 435 | 0573NashwanHimyari.KhulasaSiyar | 35,216 | 117 |
| 436 | 0379MuhammadRabci.TarikhMawlidCulama | 35,176 | 117 |
| 437 | 0657IbnIbrahimIrbili.MudhakaraFiAlqab | 35,060 | 116 |
| 438 | 1373AbuYaclaZuwawi.TarikhZuwawa | 34,902 | 116 |
| 439 | 1078RiyadZadah.AsmaKutub | 33,076 | 110 |
| 440 | 1175AhmadBudayri.HawadithDimashq | 32,858 | 109 |
| 441 | 1355AhmadTahtawi.TanbihWaIqaz | 32,723 | 109 |
| 442 | 0405HakimNaysaburi.TalkhisTarikhNaysabur | 32,674 | 108 |
| 443 | 0874IbnTaghribirdi.HawadithDahriya | 32,505 | 108 |
| 444 | 0626YaqutHamawi.Khazal | 32,504 | 108 |
| 445 | 0292Yacqubi.Buldan | 32,476 | 108 |
| 446 | 0385IbnShahin.TarikhAsmaThiqat | 31,929 | 106 |
| 447 | 0845Maqrizi.Bayan | 31,900 | 106 |
| 448 | 0911Suyuti.NazmCiqyan | 31,489 | 104 |
| 449 | 0371AhmadJurjani.Mucjam | 31,101 | 103 |
| 450 | 0821Qalqashandi.QalaidJuman | 30,592 | 101 |
| 451 | 1389AghaBuzurgTihrani.DhaylKashfZunun | 30,484 | 101 |
| 452 | 0544CiyadIbnMusaYahsubi.Ghunya | 29,789 | 99 |
| 453 | 0463KhatibBaghdadi.GhunyaMultamis | 29,514 | 98 |
| 454 | 0611CaliHarawi.Isharat | 29,278 | 97 |
| 455 | 1354RashidRida.Manar | 29,042 | 96 |
| 456 | 0658IbnAbbar.TuhfaQadim | 28,899 | 96 |
| 457 | 0902Sakhawi.ManhalCadhb | 28,425 | 94 |
| 458 | 0333AbuCarabTamimi.TabaqatCulama | 28,320 | 94 |
| 459 | 0264AbyZurca.Ducafa | 28,257 | 94 |
| 460 | 0334IbnHaikHamdani.Iklil | 27,740 | 92 |
| 461 | 0650IbnNazifHamawi.TarikhMansuri | 27,313 | 91 |
| 462 | 0879IbnQutlubugha.TajTarajim | 26,463 | 88 |
| 463 | 1450WizaraAwqafMisriyya.TarajimMujaza | 26,409 | 88 |
| 464 | 0842IbnNasirDinDimashqi.RaddWafir | 26,176 | 87 |
| 465 | 0402MuhammadSaydawi.MucjamShuyukh | 26,156 | 87 |
| 466 | 0310IbnAhmadDulabi.Dhariyya | 26,063 | 86 |
| 467 | 1414SalimIbadi.IscafAcyan | 25,921 | 86 |
| 468 | 0632IsmacilMarwazi.FakhriFiAnsab | 25,627 | 85 |
| 469 | 0255Jahiz.TajFiAkhlaq | 25,314 | 84 |
| 470 | 0748Dhahabi.MucinFiTabaqatMuhaddithin | 23,934 | 79 |
| 471 | 0929IbnKayyal.KawakibNayyirat | 23,699 | 78 |
| 472 | 0584IbnMusaHazimi.CujalaMubtadi | 23,180 | 77 |
| 473 | 1429BakrIbnCabdAllah.TabaqatNassabin | 23,042 | 76 |
| 474 | 1086IbnCajamiMisri.DhaylLubbLubab | 22,972 | 76 |
| 475 | 0576IbnMuhammadSilafi.Mashyakha | 22,872 | 76 |
| 476 | 0662RashidAttar.NuzhatNazir | 22,772 | 75 |
| 477 | 0368AbuGhalibZurari.Risala | 22,769 | 75 |
| 478 | 0418WazirMaghribi.AdabKhawas | 22,658 | 75 |
| 479 | 0418WazirMaghribi.Inas | 22,614 | 75 |
| 480 | 0776LisanDinIbnKhatib.MicyarIkhtiyar | 22,471 | 74 |
| 481 | 0209MacmarIbnMuthanna.Khayl | 22,392 | 74 |
| 482 | 0911Suyuti.DhaylTabaqatHuffaz | 22,369 | 74 |
| 483 | 0640AbuHafsDunaysiri.TarikhDunaysir | 22,117 | 73 |
| 484 | 0303Nasai.FadailSahaba | 21,802 | 72 |
| 485 | 0385IbnShahin.TarikhAsmaDucafa | 21,637 | 72 |
| 486 | 0732AbuFida.Yawaqit | 21,381 | 71 |
| 487 | 0330Sirafi.Rihla | 21,280 | 70 |
| 488 | 0204IbnKalbi.JamharaAnsab | 21,042 | 70 |
| 489 | 0565IbnZaydBayhaqi.TatimmaSiwanHikma | 20,359 | 67 |
| 490 | 0515IbnQattac.DurraKhatira | 20,292 | 67 |
| 491 | 0385Daruqutni.DhikrAsmaTabicin | 19,767 | 65 |
| 492 | 0748Dhahabi.DhikrAsmaManTakallama | 19,394 | 64 |
| 493 | 0380Muhallabi.MasalikWaMamalik | 18,868 | 62 |
| 494 | 0629IbnNuqta.IfadaWaIctibar | 18,784 | 62 |
| 495 | 0385Daruqutni.SualatBarqani | 18,719 | 62 |
| 496 | 0466CabdAzizKattani.DhaylTarikhMawlidCulama | 18,658 | 62 |
| 497 | 0463IbnCabdBarr.InbahCalaQabail | 18,464 | 61 |
| 498 | 0309IbnFadlan.Rihla | 18,416 | 61 |
| 499 | 0255Jahiz.Bighal | 18,305 | 61 |
| 500 | 0677SahibTaji.HalbaFiAsmaKhayl | 18,268 | 60 |
| 501 | 0296MuhammadIbnJarrah.ManIsmuhCamr | 18,234 | 60 |
| 502 | 0334IbnSacidQushayri.TarikhRaqqa | 17,955 | 59 |
| 503 | 1016MuhibbDinHamawi.HadiAzcan | 17,554 | 58 |
| 504 | 0597IbnJawzi.Mashyakha | 17,396 | 57 |
| 505 | 0469IbnHayyanQurtubi.Muqtabas | 17,127 | 57 |
| 506 | 0355AbuFarajIsbahani.Diyarat | 17,102 | 57 |
| 507 | 1218SalihFulani.QatfThamar | 16,905 | 56 |
| 508 | 0691IbnYusufLabli.Fihrist | 16,803 | 56 |
| 509 | 0911Suyuti.IscafMubatta | 16,433 | 54 |
| 510 | 0498AbuCaliJayyani.TaqyidMuhmal | 16,017 | 53 |
| 511 | 0405HakimNaysaburi.TasmiyaManAkhrajahum | 15,868 | 52 |
| 512 | 0456IbnHazm.FadailAndalus | 15,744 | 52 |
| 513 | 0685IbnSacidMaghribi.GhusunYanica | 15,713 | 52 |
| 514 | 0538MahmudZamakhshari.JibalWaAmkina | 15,676 | 52 |
| 515 | 0765AbuMahasinHusayni.DhaylTadhkira | 15,407 | 51 |
| 516 | 1126MuhammadHanbali.Mashyakha | 14,775 | 49 |
| 517 | 0659SainDinNaccal.Mashyakha | 14,631 | 48 |
| 518 | 0909IbnMibradHanbali.MucjamKutub | 14,490 | 48 |
| 519 | 1418SalihAhmadArkani.TihfaMajalis | 14,467 | 48 |
| 520 | 0430AbuNucaymIsbahani.Ducafa | 14,296 | 47 |
| 521 | 0456IbnHazm.NaqtCarus | 14,078 | 46 |
| 522 | 0360Khawlani.TarikhDaraya | 13,813 | 46 |
| 523 | 0261Muslim.Munfaridat | 13,798 | 45 |
| 524 | 0211AbuCatahiya.Diwan | 13,740 | 45 |
| 525 | 0541IbnCatiyyaMuharibi.Fahrasa | 13,427 | 44 |
| 526 | 0256Bukhari.Ducafa | 13,146 | 43 |
| 527 | 0748Dhahabi.DhaylDiwanDucafa | 12,664 | 42 |
| 528 | 1450TarhibDawsari.MucjamMuallafatShaficiyya | 12,526 | 41 |
| 529 | 1419MahmudTanahi.MujizFiMarajic | 12,525 | 41 |
| 530 | 0701SharafDinYunini.Mashyakha | 11,855 | 39 |
| 531 | 0911Suyuti.TabaqatMufassirin | 11,806 | 39 |
| 532 | 0374IbnHusaynAzdi.Makhzun | 11,516 | 38 |
| 533 | 0643DiyaDinMuqaddasi.FadailBaytMaqdis | 11,474 | 38 |
| 534 | 0576IbnMuhammadSilafi.Wajiz | 10,969 | 36 |
| 535 | 0442Tanukhi.TarikhCulamaNahwiyyin | 10,863 | 36 |
| 536 | 0256Bukhari.DucafaSaghir | 10,791 | 35 |
| 537 | 0444AbuFadlIbnMahdi.DhikrShuyukh | 10,738 | 35 |
| 538 | 0400IshaqMunajjim.AkamMarjan | 10,606 | 35 |
| 539 | 0628IbnCaliSanhaji.AkhbarMuluk | 10,423 | 34 |
| 540 | 0405AbuFadlHarawi.MucjamFiMushtabah | 10,379 | 34 |
| 541 | 0368Sirafi.AkhbarNahwiyyin | 10,206 | 34 |
| 542 | 1246IbnHamadBassam.DurarMafakhir | 10,058 | 33 |
| 543 | 0374IbnHusaynAzdi.DhikrIsmKullAshab | 9,862 | 32 |
| 544 | 0809IbnQunfudh.Wafayat | 9,725 | 32 |
| 545 | 0245MuhammadIbnHabib.MukhtalafQabail | 9,630 | 32 |
| 546 | 0498AbuCaliJayyani.AlqabSahaba | 9,492 | 31 |
| 547 | 0705SharafDinDimyatti.MucjamShuyukh | 9,252 | 30 |
| 548 | 0259IbnYacqubJuzjani.AhwalRijal | 9,088 | 30 |
| 549 | 0195MuarrijSadusi.HadhfMinNasabQuraysh | 9,074 | 30 |
| 550 | 0385Daruqutni.Ducafa | 9,054 | 30 |
| 551 | 0852IbnHajarCasqalani.TabaqatMudallisin | 8,929 | 29 |
| 552 | 0852IbnHajarCasqalani.ItharBiMacrifa | 8,858 | 29 |
| 553 | 0747MuhyiDinYunini.Mashyakha | 8,748 | 29 |
| 554 | 0862IbnMuhammadMujari.Barnamaj | 8,697 | 28 |
| 555 | 0852IbnHajarCasqalani.TacrifAhlTaqbis | 8,687 | 28 |
| 556 | 0511IbnMandahYahya.MacrifaAsamiArdaf | 8,637 | 28 |
| 557 | 0751IbnQayyimJawziyya.IghathaLahfan | 8,563 | 28 |
| 558 | 0318AbuCurubaHarrani.MuntaqaMinTabaqat | 8,422 | 28 |
| 559 | 0385Daruqutni.SualatNaysaburi | 8,317 | 27 |
| 560 | 0597IbnJawzi.FadailQuds | 8,290 | 27 |
| 561 | 0303Nasai.DucafaWaMatrukin | 8,237 | 27 |
| 562 | 0456IbnHazm.RisalaFiMaratibCulum | 7,743 | 25 |
| 563 | 0365IbnCadiJurjani.AsamiManRawaCanhum | 7,679 | 25 |
| 564 | 0234AbuHasanSacdi.TasmiyaManRuwiya | 7,575 | 25 |
| 565 | 0308IbnIbrahimJundi.FadailMadina | 7,557 | 25 |
| 566 | 0807IbnAhmarKhazraji.NafhaNisriniyya | 7,528 | 25 |
| 567 | 0748Dhahabi.Radd | 7,489 | 24 |
| 568 | 0255Jahiz.MukhtarFiRaddCalaNasara | 7,481 | 24 |
| 569 | 0255Jahiz.AmilWaMamul | 7,425 | 24 |
| 570 | 0222IbnBakkarDabi.AkhbarWafidat | 7,319 | 24 |
| 571 | 1285CabdRahmanTamimi.Maqamat | 7,256 | 24 |
| 572 | 0355MuhammadKindi.FadailMisr | 7,140 | 23 |
| 573 | 0256ZubayrIbnBakkar.Muntakhab | 7,125 | 23 |
| 574 | 0482AbuIshaqHabbal.WafayatMisriyyin | 7,037 | 23 |
| 575 | 0884SibtIbnCajami.TabyinLiAsma | 6,877 | 22 |
| 576 | 0456IbnHazm.AsmaKhulafa | 6,660 | 22 |
| 577 | 0774IbnRaficSallami.MashyakhaBayani | 6,654 | 22 |
| 578 | 0301Bardiji.TabaqatAsma | 6,594 | 21 |
| 579 | 0204IbnKalbi.AnsabKhayl | 6,506 | 21 |
| 580 | 0409CabdGhaniAzdi.KitabMutawarin | 6,452 | 21 |
| 581 | 0597IbnJawzi.TarikhBaytMuqaddas | 6,394 | 21 |
| 582 | 0303Nasai.TasmiyaShuyukh | 6,216 | 20 |
| 583 | 1450TarhibDawsari.MucjamMuallafatMalikiyya | 6,095 | 20 |
| 584 | 0632AbyHafsSuhrawardi.Mashyakha | 6,008 | 20 |
| 585 | 0241IbnHanbal.AsamiWaKuna | 5,950 | 19 |
| 586 | 0825IbnQasimSabti.IkhtisarAkhbar | 5,839 | 19 |
| 587 | 0884SibtIbnCajami.Ightibat | 5,716 | 19 |
| 588 | 0233YahyaIbnMacin.MinKalamFiRijal | 5,551 | 18 |
| 589 | 0222IbnBakkarDabi.AkhbarWafidin | 5,286 | 17 |
| 590 | 0852IbnHajarCasqalani.MucjamShaykhaMaryam | 4,980 | 16 |
| 591 | 1051Cimadi.RawdaRayya | 4,849 | 16 |
| 592 | 0200AbuShis.Diwan | 4,549 | 15 |
| 593 | 0286Mubarrad.NasabCadnan | 4,412 | 14 |
| 594 | 0524IbnAkfani.DhaylDhaylTarikhMawlidCulama | 4,178 | 13 |
| 595 | 0395IbnMandahMuhammad.Asami | 4,056 | 13 |
| 596 | 0776LisanDinIbnKhatib.KhatraTayf | 3,992 | 13 |
| 597 | 0911Suyuti.Shamarikh | 3,874 | 12 |
| 598 | 0322KatibBaghdadi.TarikhAimma | 3,821 | 12 |
| 599 | 0317AbuQasimBaghawi.TarikhWafatShuyukh | 3,802 | 12 |
| 600 | 0911Suyuti.AsmaMukhadramin | 3,736 | 12 |
| 601 | 1172IbnKhalifaMasakini.Fahrasa | 3,704 | 12 |
| 602 | 0374IbnHusaynAzdi.KunaLiManLaYucrafLahuIsm | 3,572 | 11 |
| 603 | 0826IbnCiraqi.Mudallisin | 3,392 | 11 |
| 604 | 0748Dhahabi.RuwatThiqat | 3,391 | 11 |
| 605 | 0761IbnKaykaldi.Mukhtalitin | 3,340 | 11 |
| 606 | 0110HasanBasri.FadailMakka | 3,334 | 11 |
| 607 | 0567IbnKhashshabBaghdadi.TarikhMawalidAimma | 3,254 | 10 |
| 608 | 0382IbnCabdAllahCaskari.AkhbarMusahhifin | 3,184 | 10 |
| 609 | 0430AbuNucaymIsbahani.DhikrManIsmuhuShucba | 3,082 | 10 |
| 610 | 0248AbuHatimSijistani.FuhulaShucara | 2,637 | 8 |
| 611 | 0430AbuNucaymIsbahani.TasmiyaMaIntahaIlayna | 2,501 | 8 |
| 612 | 0255Jahiz.TabsiraBiTijara | 2,497 | 8 |
| 613 | 0374IbnHusaynAzdi.AsmaManYucrafBiKunya | 2,362 | 7 |
| 614 | 0456IbnHazm.RisalaFiFutuhIslam | 2,234 | 7 |
| 615 | 0303Nasai.TasmiyaManLamYarwi | 2,100 | 7 |
| 616 | 1187SulaymanMahasini.HululTacab | 2,064 | 6 |
| 617 | 0643DiyaDinMuqaddasi.JuzAwham | 2,001 | 6 |
| 618 | 0349IbnCumarMuqri.AkhbarNahwiyyin | 1,790 | 5 |
| 619 | 0374IbnHusaynAzdi.ManWafaqaIsmuhuIsmAbihi | 1,753 | 5 |
| 620 | 0303Nasai.TasmiyaFuqaha | 1,162 | 3 |
| 621 | 0911Suyuti.RihNisrin | 795 | 2 |
| 622 | 0456IbnHazm.UmmahatKhulafa | 693 | 2 |
| 623 | 0303Nasai.Tabaqat | 612 | 2 |
| 624 | 0696Dabbagh.MacalimIman | 187 | 0 |
| 625 | 1450MuhammadSancani.NaylWatar | 150 | 0 |


## Texts in chronological order (duplicates excluded)

| TextGroup URI | Words  | Pages (300 w/p) |
|:--- | ------:| -----:|
| 0110HasanBasri.FadailMakka | 3,334 | 11 |
| 0195MuarrijSadusi.HadhfMinNasabQuraysh | 9,074 | 30 |
| 0200AbuShis.Diwan | 4,549 | 15 |
| 0204IbnKalbi.AnsabKhayl | 6,506 | 21 |
| 0204IbnKalbi.JamharaAnsab | 21,042 | 70 |
| 0204IbnKalbi.NasabMacad | 88,977 | 296 |
| 0207Waqidi.FutuhSham | 248,628 | 828 |
| 0207Waqidi.Maghazi | 264,920 | 883 |
| 0207Waqidi.Ridda | 37,811 | 126 |
| 0209MacmarIbnMuthanna.Khayl | 22,392 | 74 |
| 0211AbuCatahiya.Diwan | 13,740 | 45 |
| 0213IbnHisham.SiraNabawiyya | 295,600 | 985 |
| 0213IbnHisham.Tijan | 111,971 | 373 |
| 0222IbnBakkarDabi.AkhbarWafidat | 7,319 | 24 |
| 0222IbnBakkarDabi.AkhbarWafidin | 5,286 | 17 |
| 0228IbnHammadKhuzaci.Fitan | 119,494 | 398 |
| 0230IbnSacd.TabaqatKubra | 921,111 | 3,070 |
| 0231IbnSallamJumahi.TabaqatFuhulShucara | 54,921 | 183 |
| 0233YahyaIbnMacin.MacrifaRijal | 45,156 | 150 |
| 0233YahyaIbnMacin.MinKalamFiRijal | 5,551 | 18 |
| 0233YahyaIbnMacin.TarikhIbnMacin | 112,871 | 376 |
| 0234AbuHasanSacdi.TasmiyaManRuwiya | 7,575 | 25 |
| 0236AbuCabdAllahZubayri.NasabQuraysh | 90,262 | 300 |
| 0240KhalifaIbnKhayyat.Tabaqat | 102,233 | 340 |
| 0240KhalifaIbnKhayyat.Tarikh | 108,050 | 360 |
| 0241IbnHanbal.AsamiWaKuna | 5,950 | 19 |
| 0241IbnHanbal.CilalWaMacrifa | 214,328 | 714 |
| 0241IbnHanbal.FadailSahaba | 132,367 | 441 |
| 0245MuhammadIbnHabib.MukhtalafQabail | 9,630 | 32 |
| 0245MuhammadIbnHabib.MunammaqFiAkhbarQuraysh | 135,021 | 450 |
| 0248AbuHatimSijistani.FuhulaShucara | 2,637 | 8 |
| 0249Azraqi.AkhbarMakka | 136,671 | 455 |
| 0255Jahiz.AmilWaMamul | 7,425 | 24 |
| 0255Jahiz.BayanWaTabyin | 170,368 | 567 |
| 0255Jahiz.Bighal | 18,305 | 61 |
| 0255Jahiz.Bukhala | 55,171 | 183 |
| 0255Jahiz.BursanWaCurjan | 57,316 | 191 |
| 0255Jahiz.Cuthmaniya | 85,453 | 284 |
| 0255Jahiz.Hayawan | 455,685 | 1,518 |
| 0255Jahiz.MahasinWaAddad | 70,477 | 234 |
| 0255Jahiz.MukhtarFiRaddCalaNasara | 7,481 | 24 |
| 0255Jahiz.Rasail | 172,282 | 574 |
| 0255Jahiz.TabsiraBiTijara | 2,497 | 8 |
| 0255Jahiz.TajFiAkhlaq | 25,314 | 84 |
| 0256Bukhari.Ducafa | 13,146 | 43 |
| 0256Bukhari.DucafaSaghir | 10,791 | 35 |
| 0256Bukhari.TarikhKabir | 791,001 | 2,636 |
| 0256Bukhari.TarikhSaghir | 86,362 | 287 |
| 0256ZubayrIbnBakkar.AkhbarMuwaffaqiyat | 85,750 | 285 |
| 0256ZubayrIbnBakkar.JamharaNasabQuraysh | 56,650 | 188 |
| 0256ZubayrIbnBakkar.Muntakhab | 7,125 | 23 |
| 0257IbnCabdHakam.FutuhMisr | 116,282 | 387 |
| 0259IbnYacqubJuzjani.AhwalRijal | 9,088 | 30 |
| 0261AbuHasanCijli.MacrifaThiqat | 76,492 | 254 |
| 0261Muslim.KunaWaAsma | 70,202 | 234 |
| 0261Muslim.Munfaridat | 13,798 | 45 |
| 0262AbuZaydNumayri.TarikhMadina | 351,743 | 1,172 |
| 0264AbyZurca.Ducafa | 28,257 | 94 |
| 0272Fakihi.AkhbarMakka | 269,999 | 899 |
| 0276IbnQutaybaDinawari.AdabKatib | 69,368 | 231 |
| 0276IbnQutaybaDinawari.Macarif | 121,880 | 406 |
| 0277AbuHatimRazi.JarhWaTacdil | 1,121,289 | 3,737 |
| 0277IbnSyfyanFasawi.MacrifaWaTarikh | 340,450 | 1,134 |
| 0279Baladhuri.AnsabAshraf | 1,128,932 | 3,763 |
| 0279Baladhuri.FutuhBuldan | 124,892 | 416 |
| 0279IbnAbiKhaythama.TarikhKabir | 155,627 | 518 |
| 0280IbnTayfur.Baghdad | 48,570 | 161 |
| 0280IbnTayfur.BallaghatNisa | 53,601 | 178 |
| 0281AbuZurcaDimashqi.Tarikh | 75,765 | 252 |
| 0282AbuHanifaDinawari.AkhbarTiwal | 97,880 | 326 |
| 0286Mubarrad.NasabCadnan | 4,412 | 14 |
| 0287Dahhak.AhadWaMathani | 265,863 | 886 |
| 0292Bahshal.TarikhWasit | 80,039 | 266 |
| 0292Yacqubi.Buldan | 32,476 | 108 |
| 0292Yacqubi.TarikhYacqubi | 193,018 | 643 |
| 0296IbnMuctazz.Diwan | 51,131 | 170 |
| 0296IbnMuctazz.TabaqatShucara | 69,665 | 232 |
| 0296MuhammadIbnJarrah.ManIsmuhCamr | 18,234 | 60 |
| 0300IbnKhurdadhbih.MasalikWaMamalik | 41,035 | 136 |
| 0300MuallifMajhul.AkhbarDawlaCabbasiya | 106,130 | 353 |
| 0301Bardiji.TabaqatAsma | 6,594 | 21 |
| 0303Nasai.DucafaWaMatrukin | 8,237 | 27 |
| 0303Nasai.FadailSahaba | 21,802 | 72 |
| 0303Nasai.Tabaqat | 612 | 2 |
| 0303Nasai.TasmiyaFuqaha | 1,162 | 3 |
| 0303Nasai.TasmiyaManLamYarwi | 2,100 | 7 |
| 0303Nasai.TasmiyaShuyukh | 6,216 | 20 |
| 0306IbnHayyanDabbi.AkhbarQudat | 237,235 | 790 |
| 0308IbnIbrahimJundi.FadailMadina | 7,557 | 25 |
| 0309IbnFadlan.Rihla | 18,416 | 61 |
| 0310IbnAhmadDulabi.Dhariyya | 26,063 | 86 |
| 0310IbnAhmadDulabi.KunaWaAsma | 186,967 | 623 |
| 0310Tabari.JamicBayan | 3,041,268 | 10,137 |
| 0310Tabari.MuntakhabMinDhayl | 56,329 | 187 |
| 0310Tabari.Tarikh | 1,613,108 | 5,377 |
| 0317AbuQasimBaghawi.MucjamSahaba | 218,356 | 727 |
| 0317AbuQasimBaghawi.TarikhWafatShuyukh | 3,802 | 12 |
| 0318AbuCurubaHarrani.MuntaqaMinTabaqat | 8,422 | 28 |
| 0320CaribQurtubi.SilaTarikhTabari | 39,699 | 132 |
| 0322AbuJacfarCuqayli.DucafaKabir | 314,435 | 1,048 |
| 0322KatibBaghdadi.TarikhAimma | 3,821 | 12 |
| 0330Sirafi.Rihla | 21,280 | 70 |
| 0333AbuCarabTamimi.Mihan | 70,365 | 234 |
| 0333AbuCarabTamimi.TabaqatCulama | 28,320 | 94 |
| 0334IbnHaikHamdani.Iklil | 27,740 | 92 |
| 0334IbnHaikHamdani.SifaJaziraCarab | 70,929 | 236 |
| 0334IbnSacidQushayri.TarikhRaqqa | 17,955 | 59 |
| 0337IbnIshaqZajjaji.Akhbar | 40,895 | 136 |
| 0346Istakhri.MasalikWaMamalik | 75,599 | 251 |
| 0346Mascudi.AkhbarZaman | 63,951 | 213 |
| 0346Mascudi.MurujDhahab | 382,786 | 1,275 |
| 0346Mascudi.TanbihWaIshraf | 87,579 | 291 |
| 0347IbnYunusSadafi.Tarikh | 190,889 | 636 |
| 0349IbnCumarMuqri.AkhbarNahwiyyin | 1,790 | 5 |
| 0351IbnQanic.MucjamSahaba | 139,882 | 466 |
| 0354IbnHibban.Majruhin | 250,389 | 834 |
| 0354IbnHibban.MashahirCulamaAmsar | 45,365 | 151 |
| 0354IbnHibban.Sira | 109,974 | 366 |
| 0354IbnHibban.Thiqat | 535,985 | 1,786 |
| 0355AbuFarajIsbahani.Aghani | 1,537,021 | 5,123 |
| 0355AbuFarajIsbahani.Diyarat | 17,102 | 57 |
| 0355MuhammadKindi.FadailMisr | 7,140 | 23 |
| 0355MuhammadKindi.WulatMisr | 86,621 | 288 |
| 0360Khawlani.TarikhDaraya | 13,813 | 46 |
| 0360Tabarani.MucjamKabir | 1,590,311 | 5,301 |
| 0365IbnCadiJurjani.AsamiManRawaCanhum | 7,679 | 25 |
| 0365IbnCadiJurjani.KamilFiDucafa | 962,139 | 3,207 |
| 0365IbnFaqihHamadhani.Buldan | 147,644 | 492 |
| 0367IbnHawqal.SuraArd | 123,793 | 412 |
| 0368AbuGhalibZurari.Risala | 22,769 | 75 |
| 0368Sirafi.AkhbarNahwiyyin | 10,206 | 34 |
| 0369AbuShaykhIsbahani.TabaqatMuhaddithin | 132,063 | 440 |
| 0370IbnBishrAmidi.MutalifWaMukhtalif | 51,486 | 171 |
| 0371AhmadJurjani.Mucjam | 31,101 | 103 |
| 0372AbuSacidQayruwani.TahdhibMudawwana | 325,423 | 1,084 |
| 0374IbnHusaynAzdi.AsmaManYucrafBiKunya | 2,362 | 7 |
| 0374IbnHusaynAzdi.DhikrIsmKullAshab | 9,862 | 32 |
| 0374IbnHusaynAzdi.KunaLiManLaYucrafLahuIsm | 3,572 | 11 |
| 0374IbnHusaynAzdi.Makhzun | 11,516 | 38 |
| 0374IbnHusaynAzdi.ManWafaqaIsmuhuIsmAbihi | 1,753 | 5 |
| 0379MuhammadRabci.TarikhMawlidCulama | 35,176 | 117 |
| 0380Muhallabi.MasalikWaMamalik | 18,868 | 62 |
| 0382IbnCabdAllahCaskari.AkhbarMusahhifin | 3,184 | 10 |
| 0384IbnCimranMarzubani.MucjamShucara | 86,047 | 286 |
| 0385Daruqutni.DhikrAsmaTabicin | 19,767 | 65 |
| 0385Daruqutni.Ducafa | 9,054 | 30 |
| 0385Daruqutni.MutalifWaMukhtalif | 207,158 | 690 |
| 0385Daruqutni.SualatBarqani | 18,719 | 62 |
| 0385Daruqutni.SualatNaysaburi | 8,317 | 27 |
| 0385IbnNadim.Fihrist | 141,796 | 472 |
| 0385IbnShahin.TarikhAsmaDucafa | 21,637 | 72 |
| 0385IbnShahin.TarikhAsmaThiqat | 31,929 | 106 |
| 0388Shabushti.Diyarat | 38,993 | 129 |
| 0390Muqaddasi.AhsanTaqasim | 98,198 | 327 |
| 0395AbuHilalCaskari.Talkhis | 57,835 | 192 |
| 0395IbnMandahMuhammad.Asami | 4,056 | 13 |
| 0395IbnMandahMuhammad.FathBab | 124,908 | 416 |
| 0395IbnMandahMuhammad.MacrifaSahaba | 90,565 | 301 |
| 0398AbuNasrKalabadhi.HidayaWaIrshad | 90,817 | 302 |
| 0400IbnTahirMaqdisi.BadWaTarikh | 197,348 | 657 |
| 0400IshaqMunajjim.AkamMarjan | 10,606 | 35 |
| 0402MuhammadSaydawi.MucjamShuyukh | 26,156 | 87 |
| 0403IbnFaradi.TarikhCulamaAndalus | 118,911 | 396 |
| 0405AbuFadlHarawi.MucjamFiMushtabah | 10,379 | 34 |
| 0405HakimNaysaburi.TalkhisTarikhNaysabur | 32,674 | 108 |
| 0405HakimNaysaburi.TasmiyaManAkhrajahum | 15,868 | 52 |
| 0409CabdGhaniAzdi.KitabMutawarin | 6,452 | 21 |
| 0412Sulami.TabaqatSufiya | 68,774 | 229 |
| 0418WazirMaghribi.AdabKhawas | 22,658 | 75 |
| 0418WazirMaghribi.Inas | 22,614 | 75 |
| 0421IbnMuhammadMarzuqi.AzminaWaAmkina | 165,458 | 551 |
| 0421Miskawayh.Tajarib | 679,990 | 2,266 |
| 0427HamzaJurjani.TarikhJurjan | 114,881 | 382 |
| 0428IbnManjuwayhIsbahani.RijalSahihMuslim | 124,175 | 413 |
| 0429AbuMansurThacalibi.YatimaDahr | 362,496 | 1,208 |
| 0429Thacalibi.ThimarQulub | 119,721 | 399 |
| 0430AbuNucaymIsbahani.DhikrManIsmuhuShucba | 3,082 | 10 |
| 0430AbuNucaymIsbahani.Ducafa | 14,296 | 47 |
| 0430AbuNucaymIsbahani.HilyaAwliya | 1,227,955 | 4,093 |
| 0430AbuNucaymIsbahani.MacrifaSahaba | 785,050 | 2,616 |
| 0430AbuNucaymIsbahani.TarikhIsbahan | 260,298 | 867 |
| 0430AbuNucaymIsbahani.TasmiyaMaIntahaIlayna | 2,501 | 8 |
| 0436HusaynSaymari.AkhbarAbiHanifa | 41,024 | 136 |
| 0440AbuRayhanBiruni.TahqiqMaLilHind | 111,411 | 371 |
| 0442Tanukhi.TarikhCulamaNahwiyyin | 10,863 | 36 |
| 0444AbuFadlIbnMahdi.DhikrShuyukh | 10,738 | 35 |
| 0446AbuYaclaKhalili.IrshadFiMacrifaCulama | 82,456 | 274 |
| 0448HilalSabi.TuhfaUmara | 95,725 | 319 |
| 0449AbuCalaMacarri.Diwan | 120,379 | 401 |
| 0450Najashi.Rijal | 90,256 | 300 |
| 0456IbnHazm.AsmaKhulafa | 6,660 | 22 |
| 0456IbnHazm.FadailAndalus | 15,744 | 52 |
| 0456IbnHazm.JamharaAnsab | 130,859 | 436 |
| 0456IbnHazm.NaqtCarus | 14,078 | 46 |
| 0456IbnHazm.RisalaFiFutuhIslam | 2,234 | 7 |
| 0456IbnHazm.RisalaFiMaratibCulum | 7,743 | 25 |
| 0456IbnHazm.UmmahatKhulafa | 693 | 2 |
| 0458Bayhaqi.DalailNubuwwa | 602,949 | 2,009 |
| 0460ShaykhTusi.IkhtiyarMacrifaRijal | 227,637 | 758 |
| 0460ShaykhTusi.Rijal | 88,503 | 295 |
| 0463IbnCabdBarr.InbahCalaQabail | 18,464 | 61 |
| 0463IbnCabdBarr.IsticabFiMacrifaAshab | 413,421 | 1,378 |
| 0463KhatibBaghdadi.GhunyaMultamis | 29,514 | 98 |
| 0463KhatibBaghdadi.MuttafiqWaMuftariq | 218,096 | 726 |
| 0463KhatibBaghdadi.SabiqWaLahiq | 37,301 | 124 |
| 0463KhatibBaghdadi.TalkhisMutashabih | 187,352 | 624 |
| 0463KhatibBaghdadi.TarikhBaghdad | 2,621,786 | 8,739 |
| 0466CabdAzizKattani.DhaylTarikhMawlidCulama | 18,658 | 62 |
| 0469IbnHayyanQurtubi.Muqtabas | 17,127 | 57 |
| 0474IbnKhalafBaji.TacdilWaTakhrij | 180,381 | 601 |
| 0475IbnMakula.IkmalFiRafcIrtiyab | 868,430 | 2,894 |
| 0475IbnMakula.TahdhibMustamirr | 55,129 | 183 |
| 0476AbuIshaqShirazi.TabaqatFuqaha | 40,668 | 135 |
| 0482AbuIshaqHabbal.WafayatMisriyyin | 7,037 | 23 |
| 0487AbuCubaydBakri.MasalikWaMamalik | 181,326 | 604 |
| 0487AbuCubaydBakri.MucjamMaIstacjama | 291,075 | 970 |
| 0488IbnFutuhHumaydi.JadhwaMuqtabis | 85,167 | 283 |
| 0498AbuCaliJayyani.AlqabSahaba | 9,492 | 31 |
| 0498AbuCaliJayyani.TaqyidMuhmal | 16,017 | 53 |
| 0507AbuBakrShashi.HilyaCulama | 98,130 | 327 |
| 0507IbnQaysarani.AnsabMuttafiqa | 42,469 | 141 |
| 0508FattalNaysaburi.RawdaWacizin | 170,713 | 569 |
| 0511IbnMandahYahya.MacrifaAsamiArdaf | 8,637 | 28 |
| 0511SalmaSahari.Ansab | 162,120 | 540 |
| 0515IbnQattac.DurraKhatira | 20,292 | 67 |
| 0521IbnAbiYacla.TabaqatHanabila | 171,812 | 572 |
| 0521MuhammadHamadhani.TakmilaTarikhTabari | 60,016 | 200 |
| 0524IbnAkfani.DhaylDhaylTarikhMawlidCulama | 4,178 | 13 |
| 0528FathIbnKhaqan.QalaidCiqyan | 84,437 | 281 |
| 0535QawwamSunna.DalailNubuwwa | 72,728 | 242 |
| 0535QawwamSunna.SiyarSalaf | 154,547 | 515 |
| 0538MahmudZamakhshari.JibalWaAmkina | 15,676 | 52 |
| 0541IbnCatiyyaMuharibi.Fahrasa | 13,427 | 44 |
| 0542IbnBassamShantarini.Dhakhira | 593,086 | 1,976 |
| 0544CiyadIbnMusaYahsubi.Ghunya | 29,789 | 99 |
| 0544CiyadIbnMusaYahsubi.TartibMadarik | 322,807 | 1,076 |
| 0550AbuHajjajAshcari.TacrifBiAnsab | 50,496 | 168 |
| 0555IbnQalanisi.Tarikh | 120,986 | 403 |
| 0560SharifIdrisi.NuzhaMushtaq | 207,532 | 691 |
| 0561Samcani.Ansab | 943,976 | 3,146 |
| 0561Samcani.Muntakhab | 188,251 | 627 |
| 0561Samcani.Tahbir | 109,525 | 365 |
| 0565IbnZaydBayhaqi.LubabAnsab | 76,424 | 254 |
| 0565IbnZaydBayhaqi.TarikhBayhaq | 121,037 | 403 |
| 0565IbnZaydBayhaqi.TatimmaSiwanHikma | 20,359 | 67 |
| 0567IbnKhashshabBaghdadi.TarikhMawalidAimma | 3,254 | 10 |
| 0569CumaraHakami.NukatCasriyya | 47,005 | 156 |
| 0571IbnCasakir.MucjamShuyukh | 195,776 | 652 |
| 0571IbnCasakir.TarikhDimashq | 10,412,929 | 34,709 |
| 0573NashwanHimyari.KhulasaSiyar | 35,216 | 117 |
| 0575IbnBabawayh.Fihrist | 96,438 | 321 |
| 0575IbnKhayrIshbili.Fahrasa | 117,769 | 392 |
| 0576IbnMuhammadSilafi.Mashyakha | 22,872 | 76 |
| 0576IbnMuhammadSilafi.MashyakhaBaghdadiyya | 135,363 | 451 |
| 0576IbnMuhammadSilafi.MucjamSafar | 97,869 | 326 |
| 0576IbnMuhammadSilafi.Wajiz | 10,969 | 36 |
| 0577IbnAnbari.NuzhaAlibba | 43,683 | 145 |
| 0578IbnBashkuwal.GhawamidAsma | 110,027 | 366 |
| 0578IbnBashkuwal.Sila | 139,365 | 464 |
| 0580IbnCimrani.InbaFiTarikhKhulafa | 92,814 | 309 |
| 0584IbnMunqidhShayzari.Ictibar | 42,824 | 142 |
| 0584IbnMusaHazimi.Amakin | 64,697 | 215 |
| 0584IbnMusaHazimi.CujalaMubtadi | 23,180 | 77 |
| 0597CimadDinKatib.BarqShami | 84,900 | 283 |
| 0597CimadDinKatib.KharidaQasr | 385,025 | 1,283 |
| 0597IbnJawzi.DucafaWaMatrukin | 100,991 | 336 |
| 0597IbnJawzi.FadailQuds | 8,290 | 27 |
| 0597IbnJawzi.Mashyakha | 17,396 | 57 |
| 0597IbnJawzi.Muntazam | 1,529,894 | 5,099 |
| 0597IbnJawzi.MuthirGharam | 81,078 | 270 |
| 0597IbnJawzi.SifaSafwa | 330,284 | 1,100 |
| 0597IbnJawzi.TalqihFuhum | 160,269 | 534 |
| 0597IbnJawzi.TarikhBaytMuqaddas | 6,394 | 21 |
| 0599IbnYahyaDabbi.BughyaMultamis | 116,987 | 389 |
| 0600AbuBaqaHilli.ManaqibMazidiya | 95,644 | 318 |
| 0600KatibMarrakushi.Istibsar | 60,550 | 201 |
| 0606IbnMamati.LataifDhakhira | 51,074 | 170 |
| 0611CaliHarawi.Isharat | 29,278 | 97 |
| 0611SharafDinMuqaddasi.Arbacin | 47,514 | 158 |
| 0614IbnJubayr.Rihla | 74,329 | 247 |
| 0615MuwaffaqDinShafici.MurshidZuwwar | 167,271 | 557 |
| 0617MansurIbnShahanshah.MidmarHaqaiq | 45,270 | 150 |
| 0623Qazwini.Tadwin | 353,391 | 1,177 |
| 0626YaqutHamawi.Khazal | 32,504 | 108 |
| 0626YaqutHamawi.MucjamBuldan | 1,274,659 | 4,248 |
| 0626YaqutHamawi.MucjamUdaba | 794,903 | 2,649 |
| 0628IbnCaliSanhaji.AkhbarMuluk | 10,423 | 34 |
| 0629IbnNuqta.IfadaWaIctibar | 18,784 | 62 |
| 0629IbnNuqta.TakmilaIkmal | 231,460 | 771 |
| 0629IbnNuqta.TaqyidLiMacrifa | 112,296 | 374 |
| 0630IbnAthirCizzDin.Kamil | 1,385,342 | 4,617 |
| 0630IbnAthirCizzDin.LubabFiTahdhibAnsab | 341,753 | 1,139 |
| 0630IbnAthirCizzDin.UsdGhaba | 963,485 | 3,211 |
| 0632AbyHafsSuhrawardi.Mashyakha | 6,008 | 20 |
| 0632IsmacilMarwazi.FakhriFiAnsab | 25,627 | 85 |
| 0637IbnMustafwi.TarikhIrbil | 385,144 | 1,283 |
| 0639AbuBakrMalaqi.MatlacAnwar | 65,139 | 217 |
| 0640AbuHafsDunaysiri.TarikhDunaysir | 22,117 | 73 |
| 0641Sarifini.Muntakhab | 96,486 | 321 |
| 0642IbnNajjar.DhaylTarikhBaghdad | 326,501 | 1,088 |
| 0643DiyaDinMuqaddasi.FadailBaytMaqdis | 11,474 | 38 |
| 0643DiyaDinMuqaddasi.JuzAwham | 2,001 | 6 |
| 0643IbnSalahShahrazuri.TabaqatFuqaha | 63,126 | 210 |
| 0645TilimsaniBurri.Jawhara | 194,697 | 648 |
| 0646IbnQifti.IkhbarCulama | 96,909 | 323 |
| 0646IbnQifti.InbahRuwat | 295,800 | 986 |
| 0646IbnQifti.Muhammadun | 57,364 | 191 |
| 0647CabdWahidMarrakushi.Mucjib | 70,871 | 236 |
| 0650IbnNazifHamawi.TarikhMansuri | 27,313 | 91 |
| 0657IbnIbrahimIrbili.MudhakaraFiAlqab | 35,060 | 116 |
| 0658IbnAbbar.HullaSiyara | 98,508 | 328 |
| 0658IbnAbbar.MucjamAshab | 76,471 | 254 |
| 0658IbnAbbar.TakmilaLiSila | 303,591 | 1,011 |
| 0658IbnAbbar.TuhfaQadim | 28,899 | 96 |
| 0659SainDinNaccal.Mashyakha | 14,631 | 48 |
| 0660IbnCadim.BughyatTalib | 1,373,052 | 4,576 |
| 0660IbnCadim.ZubdaHalab | 110,479 | 368 |
| 0662RashidAttar.NuzhatNazir | 22,772 | 75 |
| 0665AbuShama.Rawdatayn | 317,787 | 1,059 |
| 0668IbnAbiUsaybica.CuyunAnba | 253,484 | 844 |
| 0673AbuMahasinYaghmuri.NurQabas | 68,955 | 229 |
| 0676Nawawi.TahdhibAsma | 352,183 | 1,173 |
| 0677SahibTaji.HalbaFiAsmaKhayl | 18,268 | 60 |
| 0680IbnSabuni.TakmilaIkmalIkmal | 42,252 | 140 |
| 0681IbnKhallikan.WafayatAcyan | 677,482 | 2,258 |
| 0682ZakariyaQazwini.AtharBilad | 146,837 | 489 |
| 0684IbnShaddad.AclaqKhatira | 116,670 | 388 |
| 0685IbnCibri.TarikhMukhtasarDuwal | 109,030 | 363 |
| 0685IbnSacidMaghribi.GhusunYanica | 15,713 | 52 |
| 0685IbnSacidMaghribi.Jughrafiya | 35,291 | 117 |
| 0685IbnSacidMaghribi.Mughrib | 109,402 | 364 |
| 0690IbnMujawirDimashqi.TarikhMustabsir | 65,633 | 218 |
| 0691IbnYusufLabli.Fihrist | 16,803 | 56 |
| 0694MuhibbDinTabari.Dhakhair | 81,328 | 271 |
| 0694MuhibbDinTabari.RiyadNadira | 205,681 | 685 |
| 0695IbnCidhariMarrakushi.BayanMaghrib | 153,641 | 512 |
| 0696Dabbagh.MacalimIman | 187 | 0 |
| 0696IbnZahiri.Mashyakha | 146,557 | 488 |
| 0701SharafDinYunini.Mashyakha | 11,855 | 39 |
| 0703MuhammadMarrakushi.DhaylWaTakmila | 133,973 | 446 |
| 0705SharafDinDimyatti.MucjamShuyukh | 9,252 | 30 |
| 0709CaliCalawi.Majdi | 138,926 | 463 |
| 0711IbnManzurIfriqi.MukhtasarTarikhDimashq | 2,408,342 | 8,027 |
| 0714AhmadGhibrini.CunwanDiraya | 58,461 | 194 |
| 0723IbnFuwati.Hawadith | 71,739 | 239 |
| 0726CallamaHilli.KhulasaAqwal | 106,878 | 356 |
| 0726Yunini.DhaylMiratZaman | 323,810 | 1,079 |
| 0730MuhammadTujibi.Barnamaj | 71,375 | 237 |
| 0732AbuFida.MukhtasarFiAkhbar | 316,828 | 1,056 |
| 0732AbuFida.Yawaqit | 21,381 | 71 |
| 0732IbnYacqubJanadi.SulukFiTabaqat | 272,623 | 908 |
| 0733IbnJamaca.Mashyakha | 75,126 | 250 |
| 0733Nuwayri.NihayaArab | 2,455,687 | 8,185 |
| 0739SafiDinHanbali.Marasid | 220,179 | 733 |
| 0740IbnDawudHilli.Rijal | 68,088 | 226 |
| 0741KhatibTabrizi.Ikmal | 90,307 | 301 |
| 0742Mizzi.TahdhibKamal | 4,541,150 | 15,137 |
| 0747MuhyiDinYunini.Mashyakha | 8,748 | 29 |
| 0748Dhahabi.CibarFiKhabar | 270,945 | 903 |
| 0748Dhahabi.Culuww | 51,813 | 172 |
| 0748Dhahabi.DhaylCibar | 37,477 | 124 |
| 0748Dhahabi.DhaylDiwanDucafa | 12,664 | 42 |
| 0748Dhahabi.DhikrAsmaManTakallama | 19,394 | 64 |
| 0748Dhahabi.DiwanDucafa | 105,284 | 350 |
| 0748Dhahabi.Kashif | 235,822 | 786 |
| 0748Dhahabi.MacrifaQurraKibar | 97,714 | 325 |
| 0748Dhahabi.MizanIctidal | 649,090 | 2,163 |
| 0748Dhahabi.MucinFiTabaqatMuhaddithin | 23,934 | 79 |
| 0748Dhahabi.MucjamMuhaddithin | 44,241 | 147 |
| 0748Dhahabi.MucjamShuyukh | 152,971 | 509 |
| 0748Dhahabi.MughniFiDucafa | 119,182 | 397 |
| 0748Dhahabi.MukhtasarCuluww | 71,152 | 237 |
| 0748Dhahabi.MukhtasarMinDubaythi | 103,004 | 343 |
| 0748Dhahabi.Muqtana | 77,096 | 256 |
| 0748Dhahabi.Radd | 7,489 | 24 |
| 0748Dhahabi.RuwatThiqat | 3,391 | 11 |
| 0748Dhahabi.SiyarAclamNubala | 3,145,544 | 10,485 |
| 0748Dhahabi.TadhkiraHuffaz | 337,969 | 1,126 |
| 0748Dhahabi.TarikhIslam | 3,437,381 | 11,457 |
| 0748IbnDimyati.Mustafad | 50,153 | 167 |
| 0749IbnWardi.KharidaCajaib | 75,947 | 253 |
| 0749IbnWardi.Tarikh | 252,903 | 843 |
| 0749ShihabDinCumari.MasalikAbsar | 1,182,722 | 3,942 |
| 0749Wadiashi.Barnamaj | 44,950 | 149 |
| 0750AbuHafsQazwini.Mashyakha | 68,872 | 229 |
| 0751IbnQayyimJawziyya.IghathaLahfan | 8,563 | 28 |
| 0761IbnKaykaldi.JamicTahsil | 76,460 | 254 |
| 0761IbnKaykaldi.Mukhtalitin | 3,340 | 11 |
| 0762MughaltayIbnQalij.IkmalTahdhib | 861,631 | 2,872 |
| 0764IbnShakirKutubi.FawatWafayat | 288,315 | 961 |
| 0764Safadi.AcyanCasr | 604,057 | 2,013 |
| 0764Safadi.NaktHimyan | 74,306 | 247 |
| 0764Safadi.WafiBiWafayat | 1,980,068 | 6,600 |
| 0765AbuMahasinHusayni.DhaylTadhkira | 15,407 | 51 |
| 0765AbuMahasinHusayni.IkmalLiRijal | 54,306 | 181 |
| 0767Balawi.TajMafriq | 73,852 | 246 |
| 0768Yafici.MiratJanan | 424,088 | 1,413 |
| 0771Subki.MucjamShuyukh | 117,371 | 391 |
| 0771Subki.TabaqatShaficiyaKubra | 676,731 | 2,255 |
| 0774IbnKathir.Bidaya | 2,329,940 | 7,766 |
| 0774IbnKathir.TabaqatShaficiyyin | 180,884 | 602 |
| 0774IbnKathir.Takmil | 255,916 | 853 |
| 0774IbnRaficSallami.MashyakhaBayani | 6,654 | 22 |
| 0774IbnRaficSallami.Wafayat | 61,135 | 203 |
| 0775IbnAbiWafa.JawahirMudiya | 230,720 | 769 |
| 0776LisanDinIbnKhatib.Ihata | 462,435 | 1,541 |
| 0776LisanDinIbnKhatib.KatibaKamina | 54,854 | 182 |
| 0776LisanDinIbnKhatib.KhatraTayf | 3,992 | 13 |
| 0776LisanDinIbnKhatib.MicyarIkhtiyar | 22,471 | 74 |
| 0776LisanDinIbnKhatib.NafadaJirab | 52,268 | 174 |
| 0779IbnBattuta.Rihla | 267,265 | 890 |
| 0782IbnSallar.TabaqatQurra | 51,171 | 170 |
| 0793AbuHasanMalaqi.TarikhQudat | 62,043 | 206 |
| 0795IbnRajabHanbali.DhaylTabaqatHanabila | 213,679 | 712 |
| 0799IbnFarhun.DibajMudhahhab | 114,355 | 381 |
| 0804IbnMulaqqin.TabaqatAwliya | 54,595 | 181 |
| 0806IbnHusaynCiraqi.DhaylMizan | 49,484 | 164 |
| 0807IbnAhmarKhazraji.NafhaNisriniyya | 7,528 | 25 |
| 0808IbnKhaldun.Rihla | 55,833 | 186 |
| 0808IbnKhaldun.Tarikh | 1,596,529 | 5,321 |
| 0809IbnQunfudh.Wafayat | 9,725 | 32 |
| 0812CaliKhazraji.CuqudLuluiyya | 167,694 | 558 |
| 0816AbuBakrMaraghi.Mashyakha | 64,167 | 213 |
| 0817IbnYacqubFiruzabadi.BulghaFiTarajim | 38,540 | 128 |
| 0821Qalqashandi.NihayaArab | 97,039 | 323 |
| 0821Qalqashandi.QalaidJuman | 30,592 | 101 |
| 0821Qalqashandi.SubhAcsha | 1,616,289 | 5,387 |
| 0821ShihabDinQalqashandi.Maathir | 142,487 | 474 |
| 0825IbnQasimSabti.IkhtisarAkhbar | 5,839 | 19 |
| 0826IbnCiraqi.Mudallisin | 3,392 | 11 |
| 0826IbnCiraqi.TuhfaTahsil | 62,996 | 209 |
| 0832AbuTayyibFasi.DhaylTaqyid | 177,958 | 593 |
| 0832AbuTayyibFasi.ShifaGharam | 305,946 | 1,019 |
| 0833IbnJazari.GhayaNihaya | 338,862 | 1,129 |
| 0842IbnNasirDinDimashqi.RaddWafir | 26,176 | 87 |
| 0842IbnNasirDinDimashqi.TawdihMushtabih | 550,678 | 1,835 |
| 0845Maqrizi.Bayan | 31,900 | 106 |
| 0845Maqrizi.IqazHunafa | 185,230 | 617 |
| 0845Maqrizi.Mawaciz | 683,850 | 2,279 |
| 0845Maqrizi.MukhtasarKamil | 142,932 | 476 |
| 0845Maqrizi.Suluk | 826,074 | 2,753 |
| 0851IbnQadiShuhba.TabaqatShaficiya | 119,436 | 398 |
| 0852IbnHajarCasqalani.DurarKamina | 414,702 | 1,382 |
| 0852IbnHajarCasqalani.FathBari | 3,545,728 | 11,819 |
| 0852IbnHajarCasqalani.InbaGhumr | 410,739 | 1,369 |
| 0852IbnHajarCasqalani.IsabaFiTamyiz | 1,153,468 | 3,844 |
| 0852IbnHajarCasqalani.ItharBiMacrifa | 8,858 | 29 |
| 0852IbnHajarCasqalani.LisanMizan | 1,131,427 | 3,771 |
| 0852IbnHajarCasqalani.MucjamMufahras | 183,759 | 612 |
| 0852IbnHajarCasqalani.MucjamShaykhaMaryam | 4,980 | 16 |
| 0852IbnHajarCasqalani.NuzhaAlbab | 43,292 | 144 |
| 0852IbnHajarCasqalani.RafcCisr | 123,094 | 410 |
| 0852IbnHajarCasqalani.TabaqatMudallisin | 8,929 | 29 |
| 0852IbnHajarCasqalani.TabsirMuntabih | 209,171 | 697 |
| 0852IbnHajarCasqalani.TacjilManfaca | 127,930 | 426 |
| 0852IbnHajarCasqalani.TacrifAhlTaqbis | 8,687 | 28 |
| 0852IbnHajarCasqalani.TahdhibTahdhib | 1,415,254 | 4,717 |
| 0852IbnHajarCasqalani.TaqribTahdhib | 217,589 | 725 |
| 0854IbnCarabshah.CajaibMaqdur | 72,705 | 242 |
| 0854IbnDiyaMakki.TarikhMakka | 96,272 | 320 |
| 0855Cayni.CiqdJuman | 274,376 | 914 |
| 0855Cayni.CumdaQari | 4,680,632 | 15,602 |
| 0855Cayni.MaghaniAkhyar | 426,063 | 1,420 |
| 0862IbnMuhammadMujari.Barnamaj | 8,697 | 28 |
| 0871IbnFahdMakki.LahzAlhaz | 62,047 | 206 |
| 0874IbnTaghribirdi.HawadithDahriya | 32,505 | 108 |
| 0874IbnTaghribirdi.ManhalSafi | 368,687 | 1,228 |
| 0874IbnTaghribirdi.MawridLatafa | 59,510 | 198 |
| 0874IbnTaghribirdi.NujumZahira | 1,314,867 | 4,382 |
| 0879IbnQutlubugha.TajTarajim | 26,463 | 88 |
| 0879IbnQutlubugha.Thiqat | 473,854 | 1,579 |
| 0884IbnMuflih.MaqsidArshad | 123,777 | 412 |
| 0884SibtIbnCajami.Ightibat | 5,716 | 19 |
| 0884SibtIbnCajami.KashfHathith | 52,220 | 174 |
| 0884SibtIbnCajami.KunuzDhahab | 170,224 | 567 |
| 0884SibtIbnCajami.TabyinLiAsma | 6,877 | 22 |
| 0900AbuCabdAllahHimyari.RawdMictar | 322,499 | 1,074 |
| 0902Sakhawi.Buldaniyyat | 37,943 | 126 |
| 0902Sakhawi.DuLamic | 1,335,630 | 4,452 |
| 0902Sakhawi.ManhalCadhb | 28,425 | 94 |
| 0902Sakhawi.TuhfaLatifa | 394,353 | 1,314 |
| 0904Burayhi.TabaqatSulahaYaman | 74,213 | 247 |
| 0905Basrawi.Tarikh | 39,659 | 132 |
| 0909IbnMibradHanbali.BahrDamm | 55,202 | 184 |
| 0909IbnMibradHanbali.MucjamKutub | 14,490 | 48 |
| 0911Samhudi.KhulasaWafaWafa | 168,018 | 560 |
| 0911Samhudi.WafaWafa | 376,631 | 1,255 |
| 0911Suyuti.AsmaMudallisin | 306,751 | 1,022 |
| 0911Suyuti.AsmaMukhadramin | 3,736 | 12 |
| 0911Suyuti.BughyaWucat | 197,961 | 659 |
| 0911Suyuti.DhaylTabaqatHuffaz | 22,369 | 74 |
| 0911Suyuti.HusnMuhadara | 218,158 | 727 |
| 0911Suyuti.IscafMubatta | 16,433 | 54 |
| 0911Suyuti.ItmamDiraya | 54,179 | 180 |
| 0911Suyuti.LubbLubab | 57,394 | 191 |
| 0911Suyuti.NazmCiqyan | 31,489 | 104 |
| 0911Suyuti.RihNisrin | 795 | 2 |
| 0911Suyuti.Shamarikh | 3,874 | 12 |
| 0911Suyuti.TabaqatHuffaz | 73,614 | 245 |
| 0911Suyuti.TabaqatMufassirin | 11,806 | 39 |
| 0911Suyuti.TarikhKhulafa | 133,130 | 443 |
| 0922IbnShaykhTarabulusi.IscafAwqaf | 43,648 | 145 |
| 0923IbnCabdAllahKhazraji.KhulasaTahdhib | 328,135 | 1,093 |
| 0927Culaymi.UnsJalil | 218,375 | 727 |
| 0927Nucaymi.DarisFiMadaris | 224,568 | 748 |
| 0929IbnKayyal.KawakibNayyirat | 23,699 | 78 |
| 0938IbnCaliBalawi.Thabat | 61,539 | 205 |
| 0945ShamsDinDawudi.TabaqatMufassirin | 139,971 | 466 |
| 0953IbnTulun.MufakahaKhillan | 127,338 | 424 |
| 0966HusaynDiyarbakri.TarikhKhamis | 552,947 | 1,843 |
| 0968Tashkubruizadah.ShaqaiqNucmaniyya | 145,615 | 485 |
| 0973CabdWahhabShacrani.LawaqihAnwar | 232,710 | 775 |
| 0984BardDinGhazzi.MatalicBadriya | 46,951 | 156 |
| 1010TamimiDari.TabaqatSaniya | 161,681 | 538 |
| 1011SahibMacalim.TahrirTawusi | 157,260 | 524 |
| 1016MuhibbDinHamawi.HadiAzcan | 17,554 | 58 |
| 1037CabdQadirCaydarus.TarikhNurSafir | 113,966 | 379 |
| 1041BurhanDinMaliki.BahjaMahafil | 96,298 | 320 |
| 1041Maqarri.AzharRiyad | 185,770 | 619 |
| 1041Maqarri.NafhTib | 848,136 | 2,827 |
| 1051Cimadi.RawdaRayya | 4,849 | 16 |
| 1061NajmDinGhazzi.KawakibSaira | 242,384 | 807 |
| 1067HajjiKhalifa.KashfZunun | 580,572 | 1,935 |
| 1069ShihabDinKhafaji.RayhanaAlibba | 57,614 | 192 |
| 1070MuhammadKibrit.RihlaShita | 50,647 | 168 |
| 1078RiyadZadah.AsmaKutub | 33,076 | 110 |
| 1086IbnCajamiMisri.DhaylLubbLubab | 22,972 | 76 |
| 1089IbnCimad.Shadharat | 1,097,722 | 3,659 |
| 1100IbnMuhammadAdnahwi.TabaqatMufassirin | 40,783 | 135 |
| 1100MuhammadItlidi.IclamNas | 80,344 | 267 |
| 1100MustafaTafrishi.NaqdRijal | 500,280 | 1,667 |
| 1101MuhammadCaliArdabili.JamicRuwat | 614,459 | 2,048 |
| 1111Majlisi.BiharAnwar | 4,430,411 | 14,768 |
| 1111MuhammadAminMuhibbi.KhulasaAthr | 623,533 | 2,078 |
| 1119IbnMacsum.SulafaCasr | 165,783 | 552 |
| 1120CaliKhanMadani.DarajatRafica | 174,564 | 581 |
| 1126MuhammadHanbali.Mashyakha | 14,775 | 49 |
| 1147CabdAllahSancani.TarikhYaman | 69,040 | 230 |
| 1153IbnKannan.YawmiyyatShamiyya | 79,567 | 265 |
| 1167IbnCabrRahmanGhazzi.DiwanIslam | 55,685 | 185 |
| 1172IbnKhalifaMasakini.Fahrasa | 3,704 | 12 |
| 1174AbuBarakatSuwaydi.NafhaMiskiya | 71,961 | 239 |
| 1175AhmadBudayri.HawadithDimashq | 32,858 | 109 |
| 1175MuhammadKarabisi.IklilManhaj | 203,395 | 677 |
| 1187SulaymanMahasini.HululTacab | 2,064 | 6 |
| 1195CabdRahmanAnsari.Tuhfa | 68,557 | 228 |
| 1206Muradi.SilkDurar | 358,759 | 1,195 |
| 1212BahrCulum.FawaidRijaliya | 338,918 | 1,129 |
| 1218SalihFulani.QatfThamar | 16,905 | 56 |
| 1232IbnKhatibCumari.RawdaFayha | 63,383 | 211 |
| 1237Jabarti.CajaibAthar | 514,968 | 1,716 |
| 1246IbnHamadBassam.DurarMafakhir | 10,058 | 33 |
| 1250IbnCaliShaykani.BadrTalic | 192,663 | 642 |
| 1269CabdMalikCasimi.SamtNujum | 594,712 | 1,982 |
| 1270ShihabDinAlusi.GharaibIghtirab | 113,165 | 377 |
| 1277MuhammadTantawi.NashaNahw | 52,381 | 174 |
| 1285CabdRahmanTamimi.Maqamat | 7,256 | 24 |
| 1286IcjazHusaynKunturi.KashfHajb | 126,032 | 420 |
| 1307Qannawji.AbjadCulum | 274,005 | 913 |
| 1307Qannawji.HittaFiDhikr | 67,880 | 226 |
| 1307Qannawji.LuqtaCajlan | 59,600 | 198 |
| 1313Barujirdi.Taraif | 331,121 | 1,103 |
| 1313VanDyck.IktifaQunuc | 112,098 | 373 |
| 1315AbuMacaliKalbasi.RasailRijaliyya | 613,389 | 2,044 |
| 1315Salawi.IstiqsaLiAhkbar | 464,659 | 1,548 |
| 1318MuhammadSanusi.Musamarat | 266,110 | 887 |
| 1330IbnMusaTabrizi.MiratKutub | 88,818 | 296 |
| 1332ZaynabFawwaz.DurrManthur | 238,367 | 794 |
| 1335CabdRazzaqBaytar.HilyaBashar | 346,616 | 1,155 |
| 1338MuhammadFaridBey.Bahja | 59,305 | 197 |
| 1338MuhammadFaridBey.Tarikh | 155,747 | 519 |
| 1339IsmacilBashaBaghdadi.HadiyaCarifin | 412,771 | 1,375 |
| 1339IsmacilBashaBaghdadi.IdahMaknun | 288,661 | 962 |
| 1341CabdHayyTalibi.IclamBiMan | 634,469 | 2,114 |
| 1345IbnJacfarKattani.RisalaMustatrafa | 39,163 | 130 |
| 1346CbdQadirBadran.Munadama | 110,741 | 369 |
| 1347BashirYamut.Shacirat | 37,705 | 125 |
| 1351IbnHusaynGhazzi.NahrDhahab | 434,840 | 1,449 |
| 1351YusufIlyanSarkis.MucjamMatbucat | 401,654 | 1,338 |
| 1354HasanSadr.Takmila | 88,094 | 293 |
| 1354RashidRida.Manar | 29,042 | 96 |
| 1355AhmadTahtawi.TanbihWaIqaz | 32,723 | 109 |
| 1356AbuHudaKalbasi.SamaMaqal | 226,396 | 754 |
| 1359CabbasQummi.Kuna | 299,903 | 999 |
| 1360IbnQasimMakhluf.ShajaraNur | 299,618 | 998 |
| 1364IbnHamdMughiri.MuntakhabQabail | 42,407 | 141 |
| 1368HasanAmin.MustadrakatAcyanShica | 547,076 | 1,823 |
| 1371MuhsinCamili.AcyanShica | 4,675,215 | 15,584 |
| 1372KurdCali.KhitatSham | 414,117 | 1,380 |
| 1373AbuYaclaZuwawi.TarikhZuwawa | 34,902 | 116 |
| 1376CabdRahmanSacdi.Muallafat | 139,967 | 466 |
| 1376MuhammadHajwiThacalibi.FikrSami | 234,888 | 782 |
| 1381MuhammadSancani.MulhaqBadr | 51,442 | 171 |
| 1383CadbHayyKattani.FihrisFaharis | 295,736 | 985 |
| 1389AghaBuzurgTihrani.DharicaFiTasanifShica | 2,918,325 | 9,727 |
| 1389AghaBuzurgTihrani.DhaylKashfZunun | 30,484 | 101 |
| 1389AghaBuzurgTihrani.TASHAnwarSatica | 37,497 | 124 |
| 1389AghaBuzurgTihrani.TASHNawabighRuwat | 84,082 | 280 |
| 1396KhayrDinZirikli.Aclam | 1,634,967 | 5,449 |
| 1405CaliShahrudi.Mustadrakat | 1,015,230 | 3,384 |
| 1408CumarKahhala.MucjamMuallifin | 1,145,173 | 3,817 |
| 1408CumarKahhala.MucjamQabail | 467,206 | 1,557 |
| 1411SayyidKhui.MucjamRijal | 2,594,210 | 8,647 |
| 1411SayyidMarcashi.SharhIhqaq | 4,126,172 | 13,753 |
| 1414SalimIbadi.IscafAcyan | 25,921 | 86 |
| 1418SalihAhmadArkani.TihfaMajalis | 14,467 | 48 |
| 1419MahmudTanahi.MujizFiMarajic | 12,525 | 41 |
| 1421HamdJasir.MucjamQabailMCS | 67,689 | 225 |
| 1422IbnHadiWadici.RijalHakim | 152,657 | 508 |
| 1422MuhammadSalimMuhaysin.MucjamHuffazQuran | 169,932 | 566 |
| 1429BakrIbnCabdAllah.TabaqatNassabin | 23,042 | 76 |
| 1450AbuTayyibMansuri.Irshad | 144,616 | 482 |
| 1450AkramFaluji.MucjamSaghir | 251,265 | 837 |
| 1450CabdRahmanAlShaykh.Mashahir | 62,418 | 208 |
| 1450CadilNuwayhid.MucjamAclamJazair | 100,098 | 333 |
| 1450DarIftaMisriyya.FatawaDarIfta | 1,911,816 | 6,372 |
| 1450MajmacFikrIslami.MawsucaMuallifiImamiya | 249,154 | 830 |
| 1450MawsucaShicriya.MucjamShucara | 155,885 | 519 |
| 1450MuhammadHadiAmini.MucjamMatbicatNajafiya | 44,242 | 147 |
| 1450MuhammadKhayrRamadan.TakmilaMucjamMuallifin | 189,829 | 632 |
| 1450MuhammadSancani.NaylWatar | 150 | 0 |
| 1450Musannifun.MawsucaMujaza | 668,172 | 2,227 |
| 1450TarhibDawsari.MucjamMuallafatMalikiyya | 6,095 | 20 |
| 1450TarhibDawsari.MucjamMuallafatShaficiyya | 12,526 | 41 |
| 1450WizaraAwqafMisriyya.TarajimMujaza | 26,409 | 88 |



## Themes and Genres Report

### *ADAB* (608 texts, 50,829,080 words)

- ~~06th century CE: 0 titles, 0 words~~
- **07th century CE: 2 titles, 19,107 words**
- **08th century CE: 7 titles, 209,885 words**
- **09th century CE: 48 titles, 2,956,390 words**
- **10th century CE: 86 titles, 6,981,561 words**
- **11th century CE: 94 titles, 6,518,363 words**
- **12th century CE: 85 titles, 7,929,689 words**
- **13th century CE: 44 titles, 5,591,528 words**
- **14th century CE: 37 titles, 4,720,991 words**
- **15th century CE: 23 titles, 3,522,201 words**
- **16th century CE: 32 titles, 1,187,974 words**
- **17th century CE: 10 titles, 2,794,471 words**
- **18th century CE: 6 titles, 1,206,440 words**
- **19th century CE: 14 titles, 705,377 words**
- **20th century CE: 13 titles, 1,173,560 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 608 titles, 50,829,080 words**


### *ADHKAR* (219 texts, 11,924,910 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 1 titles, 16,317 words**
- **09th century CE: 10 titles, 348,180 words**
- **10th century CE: 15 titles, 775,222 words**
- **11th century CE: 14 titles, 492,787 words**
- **12th century CE: 33 titles, 2,606,490 words**
- **13th century CE: 15 titles, 1,178,644 words**
- **14th century CE: 16 titles, 996,909 words**
- **15th century CE: 6 titles, 331,299 words**
- **16th century CE: 12 titles, 378,561 words**
- **17th century CE: 2 titles, 21,449 words**
- **18th century CE: 4 titles, 905,376 words**
- **19th century CE: 4 titles, 234,025 words**
- **20th century CE: 2 titles, 112,685 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 219 titles, 11,924,910 words**


### *ADILLA* (38 texts, 2,636,056 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- **11th century CE: 1 titles, 136,752 words**
- **12th century CE: 2 titles, 128,589 words**
- **13th century CE: 1 titles, 16,475 words**
- **14th century CE: 1 titles, 43,380 words**
- **15th century CE: 2 titles, 189,442 words**
- **16th century CE: 3 titles, 126,760 words**
- **17th century CE: 3 titles, 686,112 words**
- **18th century CE: 1 titles, 3,496 words**
- **19th century CE: 5 titles, 516,437 words**
- **20th century CE: 2 titles, 318,891 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 38 titles, 2,636,056 words**


### *AFTER800* (88 texts, 39,439,017 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- **13th century CE: 1 titles, 175,751 words**
- **14th century CE: 17 titles, 8,139,313 words**
- **15th century CE: 4 titles, 767,493 words**
- **16th century CE: 15 titles, 6,948,799 words**
- **17th century CE: 9 titles, 1,326,327 words**
- **18th century CE: 5 titles, 5,594,799 words**
- **19th century CE: 25 titles, 14,269,454 words**
- **20th century CE: 12 titles, 2,217,081 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 88 titles, 39,439,017 words**


### *AHKAM* (37 texts, 14,448,347 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 9 titles, 423,425 words**
- **10th century CE: 8 titles, 5,606,230 words**
- **11th century CE: 2 titles, 63,885 words**
- **12th century CE: 7 titles, 2,234,182 words**
- **13th century CE: 1 titles, 2,068,218 words**
- **14th century CE: 6 titles, 2,261,621 words**
- **15th century CE: 1 titles, 44,444 words**
- ~~16th century CE: 0 titles, 0 words~~
- **17th century CE: 1 titles, 9,769 words**
- **18th century CE: 1 titles, 261,323 words**
- **19th century CE: 1 titles, 1,475,250 words**
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 37 titles, 14,448,347 words**


### *AHLAM* (9 texts, 931,763 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 1 titles, 211,445 words**
- **09th century CE: 1 titles, 24,681 words**
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- **13th century CE: 1 titles, 48,509 words**
- **14th century CE: 1 titles, 76,822 words**
- **15th century CE: 1 titles, 182,337 words**
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- **18th century CE: 1 titles, 254,104 words**
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 9 titles, 931,763 words**


### *AJZA* (666 texts, 8,995,458 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 21 titles, 289,272 words**
- **09th century CE: 105 titles, 1,422,088 words**
- **10th century CE: 187 titles, 2,499,231 words**
- **11th century CE: 124 titles, 1,833,468 words**
- **12th century CE: 72 titles, 989,705 words**
- **13th century CE: 75 titles, 947,485 words**
- **14th century CE: 35 titles, 501,890 words**
- **15th century CE: 29 titles, 363,667 words**
- **16th century CE: 11 titles, 43,891 words**
- ~~17th century CE: 0 titles, 0 words~~
- **18th century CE: 1 titles, 19,275 words**
- **19th century CE: 1 titles, 5,943 words**
- **20th century CE: 1 titles, 5,888 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 666 titles, 8,995,458 words**


### *AKHLAQ* (204 texts, 12,178,946 words)

- ~~06th century CE: 0 titles, 0 words~~
- **07th century CE: 2 titles, 123,285 words**
- **08th century CE: 3 titles, 171,423 words**
- **09th century CE: 58 titles, 1,050,123 words**
- **10th century CE: 27 titles, 1,453,988 words**
- **11th century CE: 23 titles, 734,655 words**
- **12th century CE: 18 titles, 1,703,041 words**
- **13th century CE: 11 titles, 2,664,007 words**
- **14th century CE: 38 titles, 3,268,872 words**
- **15th century CE: 2 titles, 28,166 words**
- **16th century CE: 9 titles, 336,228 words**
- **17th century CE: 1 titles, 16,342 words**
- **18th century CE: 3 titles, 59,116 words**
- **19th century CE: 5 titles, 299,708 words**
- **20th century CE: 1 titles, 109,344 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 204 titles, 12,178,946 words**


### *ALBANI* (19 texts, 1,377,404 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 4 titles, 79,862 words**
- **10th century CE: 1 titles, 786,888 words**
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- **13th century CE: 3 titles, 5,821 words**
- **14th century CE: 6 titles, 380,150 words**
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- **19th century CE: 1 titles, 20,581 words**
- **20th century CE: 2 titles, 13,303 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 19 titles, 1,377,404 words**


### *AMALI* (12 texts, 159,787 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 2 titles, 13,840 words**
- **10th century CE: 3 titles, 73,010 words**
- **11th century CE: 3 titles, 6,784 words**
- **12th century CE: 1 titles, 3,881 words**
- ~~13th century CE: 0 titles, 0 words~~
- ~~14th century CE: 0 titles, 0 words~~
- **15th century CE: 3 titles, 62,272 words**
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 12 titles, 159,787 words**


### *AMTHAL* (15 texts, 1,298,264 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 1 titles, 41,459 words**
- **09th century CE: 2 titles, 48,761 words**
- **10th century CE: 4 titles, 219,925 words**
- **11th century CE: 3 titles, 216,614 words**
- **12th century CE: 2 titles, 332,602 words**
- **13th century CE: 1 titles, 179,688 words**
- **14th century CE: 1 titles, 54,758 words**
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- **17th century CE: 1 titles, 204,457 words**
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 15 titles, 1,298,264 words**


### *ANDALUSI* (16 texts, 351,649 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- **10th century CE: 1 titles, 34,483 words**
- **11th century CE: 3 titles, 21,401 words**
- **12th century CE: 1 titles, 5,351 words**
- **13th century CE: 1 titles, 21,396 words**
- **14th century CE: 2 titles, 76,426 words**
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- **18th century CE: 1 titles, 58,380 words**
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 16 titles, 351,649 words**


### *ANSAB* (36 texts, 5,718,637 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 10 titles, 1,618,087 words**
- **10th century CE: 2 titles, 263,420 words**
- **11th century CE: 4 titles, 265,652 words**
- **12th century CE: 6 titles, 1,185,749 words**
- **13th century CE: 5 titles, 1,936,171 words**
- **14th century CE: 1 titles, 132,990 words**
- **15th century CE: 2 titles, 124,664 words**
- **16th century CE: 1 titles, 56,484 words**
- **17th century CE: 1 titles, 21,216 words**
- **18th century CE: 1 titles, 66,073 words**
- **19th century CE: 1 titles, 9,883 words**
- **20th century CE: 1 titles, 10,017 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 36 titles, 5,718,637 words**


### *ASHAB* (61 texts, 10,958,798 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 1 titles, 45,305 words**
- **09th century CE: 7 titles, 1,110,637 words**
- **10th century CE: 7 titles, 133,091 words**
- **11th century CE: 5 titles, 821,086 words**
- **12th century CE: 5 titles, 655,365 words**
- **13th century CE: 7 titles, 800,175 words**
- **14th century CE: 8 titles, 3,573,708 words**
- **15th century CE: 4 titles, 60,587 words**
- **16th century CE: 10 titles, 2,877,118 words**
- **17th century CE: 2 titles, 659,204 words**
- **18th century CE: 4 titles, 154,586 words**
- ~~19th century CE: 0 titles, 0 words~~
- **20th century CE: 1 titles, 67,936 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 61 titles, 10,958,798 words**


### *BALAGHA* (357 texts, 33,394,022 words)

- ~~06th century CE: 0 titles, 0 words~~
- **07th century CE: 2 titles, 19,107 words**
- **08th century CE: 6 titles, 193,568 words**
- **09th century CE: 35 titles, 2,455,107 words**
- **10th century CE: 61 titles, 4,238,596 words**
- **11th century CE: 75 titles, 5,205,739 words**
- **12th century CE: 49 titles, 4,911,336 words**
- **13th century CE: 27 titles, 3,174,857 words**
- **14th century CE: 20 titles, 3,650,248 words**
- **15th century CE: 15 titles, 2,999,855 words**
- **16th century CE: 16 titles, 592,089 words**
- **17th century CE: 6 titles, 2,335,652 words**
- **18th century CE: 2 titles, 301,064 words**
- **19th century CE: 10 titles, 471,352 words**
- **20th century CE: 11 titles, 1,060,875 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 357 titles, 33,394,022 words**


### *BEFORE800* (40 texts, 5,683,106 words)

- ~~06th century CE: 0 titles, 0 words~~
- **07th century CE: 1 titles, 30,942 words**
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- **10th century CE: 3 titles, 349,602 words**
- **11th century CE: 25 titles, 3,286,431 words**
- **12th century CE: 3 titles, 263,847 words**
- **13th century CE: 8 titles, 1,752,284 words**
- ~~14th century CE: 0 titles, 0 words~~
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 40 titles, 5,683,106 words**


### *BIB* (12 texts, 1,399,550 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- **11th century CE: 2 titles, 144,167 words**
- ~~12th century CE: 0 titles, 0 words~~
- ~~13th century CE: 0 titles, 0 words~~
- **14th century CE: 1 titles, 43,380 words**
- ~~15th century CE: 0 titles, 0 words~~
- **16th century CE: 2 titles, 73,707 words**
- **17th century CE: 2 titles, 590,059 words**
- ~~18th century CE: 0 titles, 0 words~~
- **19th century CE: 3 titles, 197,207 words**
- **20th century CE: 2 titles, 351,030 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 12 titles, 1,399,550 words**


### *BIO* (79 texts, 40,769,399 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 6 titles, 1,394,996 words**
- **10th century CE: 7 titles, 273,989 words**
- **11th century CE: 5 titles, 3,102,403 words**
- **12th century CE: 12 titles, 11,270,914 words**
- **13th century CE: 10 titles, 3,174,230 words**
- **14th century CE: 24 titles, 16,235,580 words**
- **15th century CE: 7 titles, 3,022,431 words**
- **16th century CE: 3 titles, 411,086 words**
- **17th century CE: 3 titles, 1,540,941 words**
- **18th century CE: 2 titles, 342,829 words**
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 79 titles, 40,769,399 words**


### *BUHUTH* (183 texts, 4,789,334 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 3 titles, 90,498 words**
- **09th century CE: 6 titles, 274,845 words**
- **10th century CE: 4 titles, 180,218 words**
- **11th century CE: 5 titles, 314,658 words**
- **12th century CE: 5 titles, 72,614 words**
- **13th century CE: 4 titles, 225,838 words**
- **14th century CE: 12 titles, 144,597 words**
- **15th century CE: 8 titles, 158,071 words**
- **16th century CE: 20 titles, 354,473 words**
- **17th century CE: 6 titles, 53,289 words**
- **18th century CE: 11 titles, 137,296 words**
- **19th century CE: 3 titles, 176,161 words**
- **20th century CE: 1 titles, 62,571 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 183 titles, 4,789,334 words**


### *BULDAN* (152 texts, 32,712,979 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 2 titles, 4,799 words**
- **09th century CE: 20 titles, 3,084,580 words**
- **10th century CE: 22 titles, 1,067,593 words**
- **11th century CE: 13 titles, 3,618,066 words**
- **12th century CE: 13 titles, 9,885,026 words**
- **13th century CE: 26 titles, 5,386,136 words**
- **14th century CE: 13 titles, 2,572,378 words**
- **15th century CE: 15 titles, 3,213,426 words**
- **16th century CE: 8 titles, 1,396,072 words**
- **17th century CE: 5 titles, 985,256 words**
- **18th century CE: 4 titles, 249,582 words**
- **19th century CE: 2 titles, 575,071 words**
- **20th century CE: 4 titles, 338,413 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 152 titles, 32,712,979 words**


### *CABBASI* (53 texts, 2,085,222 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 1 titles, 2,989 words**
- **09th century CE: 9 titles, 461,588 words**
- **10th century CE: 4 titles, 132,001 words**
- **11th century CE: 6 titles, 238,798 words**
- **12th century CE: 3 titles, 91,059 words**
- **13th century CE: 5 titles, 120,984 words**
- **14th century CE: 1 titles, 36,812 words**
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 53 titles, 2,085,222 words**


### *CAQAID* (519 texts, 28,190,335 words)

- ~~06th century CE: 0 titles, 0 words~~
- **07th century CE: 1 titles, 25,843 words**
- **08th century CE: 3 titles, 128,651 words**
- **09th century CE: 34 titles, 699,441 words**
- **10th century CE: 51 titles, 1,558,222 words**
- **11th century CE: 52 titles, 4,052,321 words**
- **12th century CE: 31 titles, 1,549,422 words**
- **13th century CE: 33 titles, 1,065,767 words**
- **14th century CE: 67 titles, 6,613,406 words**
- **15th century CE: 10 titles, 1,102,986 words**
- **16th century CE: 8 titles, 413,894 words**
- **17th century CE: 18 titles, 1,517,606 words**
- **18th century CE: 37 titles, 1,301,671 words**
- **19th century CE: 48 titles, 2,158,295 words**
- **20th century CE: 30 titles, 2,315,656 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 519 titles, 28,190,335 words**


### *CARUD* (9 texts, 1,958,412 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 1 titles, 68,578 words**
- **10th century CE: 2 titles, 136,376 words**
- **11th century CE: 2 titles, 82,279 words**
- **12th century CE: 2 titles, 88,931 words**
- **13th century CE: 1 titles, 77,618 words**
- ~~14th century CE: 0 titles, 0 words~~
- **15th century CE: 1 titles, 1,504,630 words**
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 9 titles, 1,958,412 words**


### *CENT00NO* (948 texts, 54,670,558 words)

- ~~06th century CE: 0 titles, 0 words~~
- **07th century CE: 18 titles, 181,447 words**
- **08th century CE: 14 titles, 254,232 words**
- **09th century CE: 13 titles, 544,634 words**
- **10th century CE: 14 titles, 769,075 words**
- **11th century CE: 14 titles, 241,550 words**
- **12th century CE: 11 titles, 616,402 words**
- **13th century CE: 11 titles, 278,704 words**
- **14th century CE: 7 titles, 407,123 words**
- **15th century CE: 2 titles, 222,358 words**
- **16th century CE: 5 titles, 51,275 words**
- **17th century CE: 5 titles, 433,555 words**
- **18th century CE: 4 titles, 886,882 words**
- **19th century CE: 5 titles, 495,091 words**
- **20th century CE: 7 titles, 596,608 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 948 titles, 54,670,558 words**


### *CENT0100* (10 texts, 1,008,751 words)

- ~~06th century CE: 0 titles, 0 words~~
- **07th century CE: 4 titles, 179,218 words**
- **08th century CE: 5 titles, 581,883 words**
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- ~~13th century CE: 0 titles, 0 words~~
- ~~14th century CE: 0 titles, 0 words~~
- **15th century CE: 1 titles, 247,650 words**
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 10 titles, 1,008,751 words**


### *CENT0200* (95 texts, 7,074,107 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 65 titles, 5,500,005 words**
- **09th century CE: 30 titles, 1,574,102 words**
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- ~~13th century CE: 0 titles, 0 words~~
- ~~14th century CE: 0 titles, 0 words~~
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 95 titles, 7,074,107 words**


### *CENT0300* (472 texts, 32,345,327 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 423 titles, 28,990,456 words**
- **10th century CE: 47 titles, 3,308,505 words**
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- ~~13th century CE: 0 titles, 0 words~~
- **14th century CE: 1 titles, 1,066 words**
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 472 titles, 32,345,327 words**


### *CENT0400* (655 texts, 60,871,538 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 2 titles, 57,898 words**
- **10th century CE: 580 titles, 55,947,125 words**
- **11th century CE: 70 titles, 4,767,379 words**
- **12th century CE: 1 titles, 7,946 words**
- ~~13th century CE: 0 titles, 0 words~~
- ~~14th century CE: 0 titles, 0 words~~
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 655 titles, 60,871,538 words**


### *CENT0500* (611 texts, 67,616,149 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 1 titles, 8,013 words**
- ~~09th century CE: 0 titles, 0 words~~
- **10th century CE: 2 titles, 51,680 words**
- **11th century CE: 585 titles, 65,540,489 words**
- **12th century CE: 20 titles, 1,414,600 words**
- ~~13th century CE: 0 titles, 0 words~~
- **14th century CE: 1 titles, 5,026 words**
- **15th century CE: 1 titles, 589,291 words**
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 611 titles, 67,616,149 words**


### *CENT0600* (478 texts, 55,069,161 words)

- ~~06th century CE: 0 titles, 0 words~~
- **07th century CE: 7 titles, 296,190 words**
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 2 titles, 6,524 words**
- **10th century CE: 1 titles, 21,305 words**
- **11th century CE: 1 titles, 5,795 words**
- **12th century CE: 430 titles, 51,086,173 words**
- **13th century CE: 34 titles, 2,813,319 words**
- **14th century CE: 2 titles, 745,098 words**
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 478 titles, 55,069,161 words**


### *CENT0700* (385 texts, 58,252,725 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- **12th century CE: 3 titles, 872,264 words**
- **13th century CE: 378 titles, 57,150,027 words**
- ~~14th century CE: 0 titles, 0 words~~
- **15th century CE: 1 titles, 79,286 words**
- **16th century CE: 2 titles, 124,269 words**
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 385 titles, 58,252,725 words**


### *CENT0800* (551 texts, 99,574,208 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- **13th century CE: 2 titles, 220,275 words**
- **14th century CE: 546 titles, 94,998,089 words**
- **15th century CE: 2 titles, 4,328,354 words**
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 551 titles, 99,574,208 words**


### *CENT0900* (311 texts, 72,147,880 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 1 titles, 2,287 words**
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- **11th century CE: 1 titles, 1,088,701 words**
- ~~12th century CE: 0 titles, 0 words~~
- **13th century CE: 1 titles, 66,666 words**
- **14th century CE: 9 titles, 1,258,306 words**
- **15th century CE: 296 titles, 69,245,448 words**
- **16th century CE: 1 titles, 1,815 words**
- ~~17th century CE: 0 titles, 0 words~~
- **18th century CE: 2 titles, 484,657 words**
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 311 titles, 72,147,880 words**


### *CENT1000* (258 texts, 53,725,455 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- ~~13th century CE: 0 titles, 0 words~~
- ~~14th century CE: 0 titles, 0 words~~
- **15th century CE: 23 titles, 3,725,601 words**
- **16th century CE: 235 titles, 49,999,854 words**
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 258 titles, 53,725,455 words**


### *CENT1100* (140 texts, 34,802,409 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- ~~13th century CE: 0 titles, 0 words~~
- ~~14th century CE: 0 titles, 0 words~~
- ~~15th century CE: 0 titles, 0 words~~
- **16th century CE: 10 titles, 5,772,985 words**
- **17th century CE: 130 titles, 29,029,424 words**
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 140 titles, 34,802,409 words**


### *CENT1200* (108 texts, 45,368,897 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- ~~13th century CE: 0 titles, 0 words~~
- ~~14th century CE: 0 titles, 0 words~~
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- **17th century CE: 25 titles, 24,085,446 words**
- **18th century CE: 83 titles, 21,283,451 words**
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 108 titles, 45,368,897 words**


### *CENT1300* (215 texts, 61,771,357 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- ~~13th century CE: 0 titles, 0 words~~
- ~~14th century CE: 0 titles, 0 words~~
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- **18th century CE: 64 titles, 11,665,897 words**
- **19th century CE: 149 titles, 50,031,610 words**
- **20th century CE: 1 titles, 31,773 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 215 titles, 61,771,357 words**


### *CENT1400* (170 texts, 34,131,920 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- ~~13th century CE: 0 titles, 0 words~~
- ~~14th century CE: 0 titles, 0 words~~
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- **19th century CE: 47 titles, 9,507,721 words**
- **20th century CE: 121 titles, 16,230,159 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 170 titles, 34,131,920 words**


### *CENT1500* (11 texts, 744,982 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 1 titles, 1,418 words**
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- ~~13th century CE: 0 titles, 0 words~~
- ~~14th century CE: 0 titles, 0 words~~
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 11 titles, 744,982 words**


### *CHR* (13 texts, 13,844,874 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- **10th century CE: 2 titles, 1,645,771 words**
- ~~11th century CE: 0 titles, 0 words~~
- **12th century CE: 1 titles, 1,414,449 words**
- **13th century CE: 1 titles, 1,377,588 words**
- **14th century CE: 6 titles, 6,747,646 words**
- **15th century CE: 2 titles, 1,646,674 words**
- ~~16th century CE: 0 titles, 0 words~~
- **17th century CE: 1 titles, 1,012,746 words**
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 13 titles, 13,844,874 words**


### *CHRONOMULTIPLE* (41 texts, 11,745,623 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 4 titles, 223,163 words**
- **09th century CE: 3 titles, 59,755 words**
- **10th century CE: 5 titles, 457,839 words**
- **11th century CE: 3 titles, 1,099,784 words**
- **12th century CE: 6 titles, 909,213 words**
- **13th century CE: 3 titles, 1,486,402 words**
- **14th century CE: 4 titles, 751,190 words**
- **15th century CE: 6 titles, 5,498,347 words**
- **16th century CE: 3 titles, 267,269 words**
- ~~17th century CE: 0 titles, 0 words~~
- **18th century CE: 2 titles, 484,657 words**
- **19th century CE: 1 titles, 476,231 words**
- **20th century CE: 1 titles, 31,773 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 41 titles, 11,745,623 words**


### *CILAL* (71 texts, 6,584,897 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 15 titles, 484,960 words**
- **10th century CE: 9 titles, 2,099,368 words**
- **11th century CE: 7 titles, 146,969 words**
- **12th century CE: 11 titles, 1,700,275 words**
- **13th century CE: 4 titles, 352,567 words**
- **14th century CE: 7 titles, 413,434 words**
- ~~15th century CE: 0 titles, 0 words~~
- **16th century CE: 4 titles, 649,219 words**
- **17th century CE: 3 titles, 65,752 words**
- **18th century CE: 2 titles, 276,756 words**
- **19th century CE: 3 titles, 57,089 words**
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 71 titles, 6,584,897 words**


### *CIRFAN* (7 texts, 3,487,980 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- **13th century CE: 2 titles, 1,870,333 words**
- ~~14th century CE: 0 titles, 0 words~~
- **15th century CE: 2 titles, 387,628 words**
- ~~16th century CE: 0 titles, 0 words~~
- **17th century CE: 3 titles, 1,230,019 words**
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 7 titles, 3,487,980 words**


### *COL* (78 texts, 45,261,680 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 4 titles, 1,099,770 words**
- **10th century CE: 5 titles, 1,738,117 words**
- **11th century CE: 4 titles, 3,014,033 words**
- **12th century CE: 22 titles, 13,109,092 words**
- **13th century CE: 11 titles, 4,623,803 words**
- **14th century CE: 17 titles, 15,749,228 words**
- **15th century CE: 7 titles, 3,284,070 words**
- **16th century CE: 4 titles, 632,777 words**
- **17th century CE: 3 titles, 1,730,558 words**
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- **20th century CE: 1 titles, 280,232 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 78 titles, 45,261,680 words**


### *CULUM* (427 texts, 64,867,950 words)

- ~~06th century CE: 0 titles, 0 words~~
- **07th century CE: 1 titles, 15,330 words**
- **08th century CE: 7 titles, 601,640 words**
- **09th century CE: 20 titles, 1,386,096 words**
- **10th century CE: 32 titles, 8,763,797 words**
- **11th century CE: 49 titles, 6,809,780 words**
- **12th century CE: 31 titles, 5,467,849 words**
- **13th century CE: 25 titles, 7,507,767 words**
- **14th century CE: 41 titles, 7,815,414 words**
- **15th century CE: 42 titles, 10,648,247 words**
- **16th century CE: 22 titles, 4,013,299 words**
- **17th century CE: 9 titles, 323,446 words**
- **18th century CE: 11 titles, 545,057 words**
- **19th century CE: 4 titles, 5,107,008 words**
- **20th century CE: 6 titles, 486,830 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 427 titles, 64,867,950 words**


### *CUTHMANI* (12 texts, 809,558 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- ~~13th century CE: 0 titles, 0 words~~
- **14th century CE: 2 titles, 221,371 words**
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- **17th century CE: 2 titles, 69,081 words**
- **18th century CE: 2 titles, 91,062 words**
- **19th century CE: 2 titles, 128,579 words**
- **20th century CE: 1 titles, 30,739 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 12 titles, 809,558 words**


### *DACIF* (44 texts, 4,118,004 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 6 titles, 313,864 words**
- **10th century CE: 5 titles, 1,149,393 words**
- **11th century CE: 1 titles, 4,804 words**
- **12th century CE: 8 titles, 1,228,988 words**
- **13th century CE: 3 titles, 58,198 words**
- **14th century CE: 7 titles, 116,023 words**
- **15th century CE: 1 titles, 154,496 words**
- **16th century CE: 3 titles, 581,473 words**
- **17th century CE: 3 titles, 65,752 words**
- **18th century CE: 2 titles, 276,756 words**
- **19th century CE: 5 titles, 168,257 words**
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 44 titles, 4,118,004 words**


### *DACWA* (86 texts, 2,317,706 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- **12th century CE: 2 titles, 29,281 words**
- ~~13th century CE: 0 titles, 0 words~~
- ~~14th century CE: 0 titles, 0 words~~
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- **20th century CE: 1 titles, 28,757 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 86 titles, 2,317,706 words**


### *DHB* (16 texts, 15,999,674 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 1 titles, 285,184 words**
- ~~10th century CE: 0 titles, 0 words~~
- **11th century CE: 2 titles, 3,133,874 words**
- **12th century CE: 2 titles, 2,248,461 words**
- **13th century CE: 1 titles, 661,178 words**
- **14th century CE: 10 titles, 9,670,977 words**
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 16 titles, 15,999,674 words**


### *FADAIL* (3 texts, 16,177 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- **10th century CE: 1 titles, 8,687 words**
- **11th century CE: 1 titles, 4,535 words**
- ~~12th century CE: 0 titles, 0 words~~
- ~~13th century CE: 0 titles, 0 words~~
- ~~14th century CE: 0 titles, 0 words~~
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- **18th century CE: 1 titles, 2,955 words**
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 3 titles, 16,177 words**


### *FAHARIS* (54 texts, 8,211,931 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- **10th century CE: 1 titles, 29,675 words**
- **11th century CE: 3 titles, 367,553 words**
- **12th century CE: 3 titles, 425,058 words**
- **13th century CE: 5 titles, 1,428,773 words**
- **14th century CE: 3 titles, 3,148,891 words**
- **15th century CE: 4 titles, 412,099 words**
- **16th century CE: 4 titles, 128,592 words**
- **17th century CE: 4 titles, 770,296 words**
- **18th century CE: 1 titles, 3,496 words**
- **19th century CE: 6 titles, 638,087 words**
- **20th century CE: 3 titles, 389,689 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 54 titles, 8,211,931 words**


### *FALSAFA* (93 texts, 4,909,218 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 1 titles, 1,748 words**
- **09th century CE: 32 titles, 482,392 words**
- **10th century CE: 35 titles, 386,348 words**
- **11th century CE: 13 titles, 496,423 words**
- **12th century CE: 2 titles, 24,519 words**
- **13th century CE: 3 titles, 1,878,480 words**
- ~~14th century CE: 0 titles, 0 words~~
- **15th century CE: 2 titles, 387,628 words**
- ~~16th century CE: 0 titles, 0 words~~
- **17th century CE: 3 titles, 1,230,019 words**
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- **20th century CE: 1 titles, 10,386 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 93 titles, 4,909,218 words**


### *FARQ* (8 texts, 460,423 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 2 titles, 88,948 words**
- **10th century CE: 1 titles, 96,387 words**
- **11th century CE: 1 titles, 8,825 words**
- ~~12th century CE: 0 titles, 0 words~~
- ~~13th century CE: 0 titles, 0 words~~
- ~~14th century CE: 0 titles, 0 words~~
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- **19th century CE: 1 titles, 5,529 words**
- **20th century CE: 1 titles, 106,644 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 8 titles, 460,423 words**


### *FASAHA* (39 texts, 4,652,773 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 5 titles, 340,543 words**
- **10th century CE: 7 titles, 478,820 words**
- **11th century CE: 15 titles, 835,623 words**
- **12th century CE: 5 titles, 430,128 words**
- **13th century CE: 4 titles, 1,518,949 words**
- ~~14th century CE: 0 titles, 0 words~~
- ~~15th century CE: 0 titles, 0 words~~
- **16th century CE: 2 titles, 73,513 words**
- **17th century CE: 1 titles, 975,197 words**
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 39 titles, 4,652,773 words**


### *FATAWA* (31 texts, 6,771,578 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- **13th century CE: 1 titles, 27,528 words**
- **14th century CE: 3 titles, 592,878 words**
- **15th century CE: 2 titles, 24,713 words**
- **16th century CE: 4 titles, 1,539,515 words**
- ~~17th century CE: 0 titles, 0 words~~
- **18th century CE: 2 titles, 244,948 words**
- **19th century CE: 14 titles, 2,154,716 words**
- **20th century CE: 1 titles, 147,609 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 31 titles, 6,771,578 words**


### *FAWAID* (14 texts, 203,216 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 1 titles, 1,423 words**
- **09th century CE: 1 titles, 7,761 words**
- **10th century CE: 2 titles, 4,018 words**
- **11th century CE: 6 titles, 153,804 words**
- **12th century CE: 2 titles, 27,690 words**
- ~~13th century CE: 0 titles, 0 words~~
- **14th century CE: 2 titles, 8,520 words**
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 14 titles, 203,216 words**


### *FIQH* (776 texts, 255,621,672 words)

- ~~06th century CE: 0 titles, 0 words~~
- **07th century CE: 1 titles, 30,942 words**
- **08th century CE: 9 titles, 1,894,834 words**
- **09th century CE: 56 titles, 10,572,765 words**
- **10th century CE: 71 titles, 12,379,338 words**
- **11th century CE: 86 titles, 25,601,998 words**
- **12th century CE: 51 titles, 12,593,546 words**
- **13th century CE: 65 titles, 20,924,847 words**
- **14th century CE: 101 titles, 35,792,813 words**
- **15th century CE: 47 titles, 25,348,530 words**
- **16th century CE: 70 titles, 27,005,289 words**
- **17th century CE: 34 titles, 9,589,355 words**
- **18th century CE: 41 titles, 22,371,227 words**
- **19th century CE: 65 titles, 35,370,893 words**
- **20th century CE: 27 titles, 4,773,862 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 776 titles, 255,621,672 words**


### *FIRAQ* (19 texts, 2,093,490 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- **10th century CE: 3 titles, 143,968 words**
- **11th century CE: 3 titles, 521,151 words**
- **12th century CE: 2 titles, 134,392 words**
- **13th century CE: 3 titles, 146,670 words**
- **14th century CE: 4 titles, 1,009,219 words**
- **15th century CE: 1 titles, 35,438 words**
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- **19th century CE: 1 titles, 8,499 words**
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 19 titles, 2,093,490 words**


### *GEN* (12 texts, 1,732,134 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 8 titles, 1,360,907 words**
- ~~10th century CE: 0 titles, 0 words~~
- **11th century CE: 1 titles, 22,410 words**
- **12th century CE: 1 titles, 22,125 words**
- **13th century CE: 1 titles, 193,702 words**
- **14th century CE: 1 titles, 132,990 words**
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 12 titles, 1,732,134 words**


### *GEO* (32 texts, 3,354,197 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- **10th century CE: 11 titles, 408,545 words**
- **11th century CE: 2 titles, 336,660 words**
- **12th century CE: 3 titles, 157,585 words**
- **13th century CE: 6 titles, 1,445,549 words**
- **14th century CE: 4 titles, 438,394 words**
- **15th century CE: 3 titles, 411,167 words**
- ~~16th century CE: 0 titles, 0 words~~
- **17th century CE: 2 titles, 67,554 words**
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 32 titles, 3,354,197 words**


### *GHARIB* (126 texts, 28,196,667 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 1 titles, 456,502 words**
- **09th century CE: 23 titles, 1,070,048 words**
- **10th century CE: 21 titles, 4,345,423 words**
- **11th century CE: 18 titles, 4,136,424 words**
- **12th century CE: 15 titles, 2,947,637 words**
- **13th century CE: 13 titles, 2,847,675 words**
- **14th century CE: 7 titles, 4,062,644 words**
- **15th century CE: 7 titles, 1,217,218 words**
- **16th century CE: 5 titles, 52,175 words**
- **17th century CE: 2 titles, 432,615 words**
- **18th century CE: 4 titles, 5,431,435 words**
- **19th century CE: 3 titles, 975,182 words**
- **20th century CE: 1 titles, 28,889 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 126 titles, 28,196,667 words**


### *GRAR* (150 texts, 2,385,551 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 1 titles, 1,748 words**
- **09th century CE: 39 titles, 617,499 words**
- **10th century CE: 35 titles, 386,348 words**
- **11th century CE: 20 titles, 570,655 words**
- **12th century CE: 2 titles, 24,519 words**
- **13th century CE: 24 titles, 535,632 words**
- **14th century CE: 16 titles, 128,573 words**
- **15th century CE: 8 titles, 40,897 words**
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- **20th century CE: 1 titles, 10,386 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 150 titles, 2,385,551 words**


### *HAD* (3 texts, 1,559,638 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 1 titles, 10,042 words**
- **10th century CE: 2 titles, 1,549,596 words**
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- ~~13th century CE: 0 titles, 0 words~~
- ~~14th century CE: 0 titles, 0 words~~
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 3 titles, 1,559,638 words**


### *HADITH* (1,999 texts, 224,854,392 words)

- ~~06th century CE: 0 titles, 0 words~~
- **07th century CE: 4 titles, 260,901 words**
- **08th century CE: 41 titles, 3,530,626 words**
- **09th century CE: 258 titles, 19,306,273 words**
- **10th century CE: 397 titles, 30,831,210 words**
- **11th century CE: 356 titles, 30,415,812 words**
- **12th century CE: 196 titles, 16,482,593 words**
- **13th century CE: 178 titles, 11,915,776 words**
- **14th century CE: 145 titles, 20,449,082 words**
- **15th century CE: 147 titles, 30,695,218 words**
- **16th century CE: 66 titles, 15,921,981 words**
- **17th century CE: 44 titles, 27,042,668 words**
- **18th century CE: 29 titles, 5,064,161 words**
- **19th century CE: 20 titles, 3,422,793 words**
- **20th century CE: 16 titles, 4,489,353 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 1,999 titles, 224,854,392 words**


### *HANAFI* (53 texts, 28,270,970 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 3 titles, 73,365 words**
- **09th century CE: 6 titles, 616,960 words**
- ~~10th century CE: 0 titles, 0 words~~
- **11th century CE: 3 titles, 2,659,560 words**
- **12th century CE: 6 titles, 2,122,393 words**
- **13th century CE: 5 titles, 3,538,249 words**
- **14th century CE: 7 titles, 4,583,455 words**
- **15th century CE: 3 titles, 3,422,672 words**
- **16th century CE: 3 titles, 3,457,828 words**
- **17th century CE: 7 titles, 1,360,431 words**
- **18th century CE: 1 titles, 334,180 words**
- **19th century CE: 5 titles, 4,148,500 words**
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 53 titles, 28,270,970 words**


### *HANBALI* (52 texts, 19,111,058 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 6 titles, 387,262 words**
- **10th century CE: 5 titles, 454,998 words**
- ~~11th century CE: 0 titles, 0 words~~
- **12th century CE: 2 titles, 32,913 words**
- **13th century CE: 5 titles, 2,548,949 words**
- **14th century CE: 8 titles, 7,025,324 words**
- **15th century CE: 3 titles, 2,248,171 words**
- **16th century CE: 3 titles, 532,703 words**
- **17th century CE: 6 titles, 2,016,521 words**
- **18th century CE: 8 titles, 845,866 words**
- **19th century CE: 1 titles, 1,063,300 words**
- **20th century CE: 1 titles, 112,736 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 52 titles, 19,111,058 words**


### *HIS* (2 texts, 98,467 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- **10th century CE: 1 titles, 12,993 words**
- ~~11th century CE: 0 titles, 0 words~~
- **12th century CE: 1 titles, 85,474 words**
- ~~13th century CE: 0 titles, 0 words~~
- ~~14th century CE: 0 titles, 0 words~~
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 2 titles, 98,467 words**


### *IBNABIDUNYA* (59 texts, 808,380 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 59 titles, 808,380 words**
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- ~~13th century CE: 0 titles, 0 words~~
- ~~14th century CE: 0 titles, 0 words~~
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 59 titles, 808,380 words**


### *IBNQAYYIM* (36 texts, 4,224,213 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- ~~13th century CE: 0 titles, 0 words~~
- **14th century CE: 36 titles, 4,224,213 words**
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 36 titles, 4,224,213 words**


### *IBNTAYMIYYA* (75 texts, 9,437,074 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- ~~13th century CE: 0 titles, 0 words~~
- **14th century CE: 75 titles, 9,437,074 words**
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 75 titles, 9,437,074 words**


### *ICRAB* (3 texts, 772,636 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- **10th century CE: 1 titles, 415,797 words**
- **11th century CE: 1 titles, 116,026 words**
- ~~12th century CE: 0 titles, 0 words~~
- **13th century CE: 1 titles, 240,813 words**
- ~~14th century CE: 0 titles, 0 words~~
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 3 titles, 772,636 words**


### *IMAM* (60 texts, 11,323,852 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 3 titles, 184,928 words**
- **09th century CE: 3 titles, 568,993 words**
- **10th century CE: 3 titles, 635,431 words**
- **11th century CE: 5 titles, 158,345 words**
- **12th century CE: 8 titles, 911,335 words**
- **13th century CE: 8 titles, 875,639 words**
- **14th century CE: 10 titles, 3,434,571 words**
- **15th century CE: 6 titles, 721,387 words**
- **16th century CE: 2 titles, 2,068,905 words**
- **17th century CE: 2 titles, 803,170 words**
- **18th century CE: 2 titles, 36,022 words**
- **19th century CE: 3 titles, 757,754 words**
- **20th century CE: 5 titles, 167,372 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 60 titles, 11,323,852 words**


### *ISLAMI* (3 texts, 12,212 words)

- ~~06th century CE: 0 titles, 0 words~~
- **07th century CE: 1 titles, 1,941 words**
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- ~~13th century CE: 0 titles, 0 words~~
- ~~14th century CE: 0 titles, 0 words~~
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 3 titles, 12,212 words**


### *JAHILI* (29 texts, 107,906 words)

- ~~06th century CE: 0 titles, 0 words~~
- **07th century CE: 14 titles, 74,537 words**
- **08th century CE: 1 titles, 3,145 words**
- **09th century CE: 1 titles, 629 words**
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- ~~13th century CE: 0 titles, 0 words~~
- ~~14th century CE: 0 titles, 0 words~~
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 29 titles, 107,906 words**


### *JUGHRAFIYA* (69 texts, 7,959,023 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 1 titles, 2,282 words**
- **10th century CE: 15 titles, 662,259 words**
- **11th century CE: 7 titles, 570,333 words**
- **12th century CE: 6 titles, 401,777 words**
- **13th century CE: 11 titles, 1,848,229 words**
- **14th century CE: 9 titles, 1,971,009 words**
- **15th century CE: 6 titles, 1,172,741 words**
- **16th century CE: 3 titles, 614,971 words**
- **17th century CE: 2 titles, 67,554 words**
- **18th century CE: 1 titles, 69,554 words**
- **19th century CE: 1 titles, 112,731 words**
- **20th century CE: 2 titles, 129,002 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 69 titles, 7,959,023 words**


### *KITABA* (9 texts, 1,958,412 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 1 titles, 68,578 words**
- **10th century CE: 2 titles, 136,376 words**
- **11th century CE: 2 titles, 82,279 words**
- **12th century CE: 2 titles, 88,931 words**
- **13th century CE: 1 titles, 77,618 words**
- ~~14th century CE: 0 titles, 0 words~~
- **15th century CE: 1 titles, 1,504,630 words**
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 9 titles, 1,958,412 words**


### *KUTUB* (45 texts, 3,153,519 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- **10th century CE: 1 titles, 29,675 words**
- **11th century CE: 2 titles, 144,167 words**
- **12th century CE: 2 titles, 128,589 words**
- **13th century CE: 2 titles, 126,710 words**
- **14th century CE: 2 titles, 46,408 words**
- **15th century CE: 3 titles, 364,104 words**
- **16th century CE: 3 titles, 126,760 words**
- **17th century CE: 3 titles, 686,112 words**
- **18th century CE: 1 titles, 3,496 words**
- **19th century CE: 6 titles, 638,087 words**
- **20th century CE: 3 titles, 389,689 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 45 titles, 3,153,519 words**


### *LUGHA* (69 texts, 15,148,642 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 1 titles, 456,502 words**
- **09th century CE: 6 titles, 603,726 words**
- **10th century CE: 7 titles, 182,480 words**
- **11th century CE: 8 titles, 1,440,823 words**
- **12th century CE: 4 titles, 171,372 words**
- **13th century CE: 10 titles, 2,073,783 words**
- **14th century CE: 5 titles, 3,750,454 words**
- **15th century CE: 1 titles, 579,698 words**
- **16th century CE: 6 titles, 239,767 words**
- **17th century CE: 1 titles, 586,354 words**
- **18th century CE: 2 titles, 4,350,401 words**
- **19th century CE: 2 titles, 116,582 words**
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 69 titles, 15,148,642 words**


### *MACAJIM* (173 texts, 38,507,742 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 2 titles, 476,460 words**
- **09th century CE: 40 titles, 5,686,476 words**
- **10th century CE: 41 titles, 8,277,379 words**
- **11th century CE: 23 titles, 4,546,279 words**
- **12th century CE: 15 titles, 3,266,102 words**
- **13th century CE: 16 titles, 3,465,350 words**
- **14th century CE: 6 titles, 3,630,088 words**
- **15th century CE: 7 titles, 1,217,218 words**
- **16th century CE: 5 titles, 52,175 words**
- **17th century CE: 3 titles, 990,090 words**
- **18th century CE: 4 titles, 5,431,435 words**
- **19th century CE: 4 titles, 1,247,001 words**
- **20th century CE: 1 titles, 28,889 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 173 titles, 38,507,742 words**


### *MAJALIS* (12 texts, 159,787 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 2 titles, 13,840 words**
- **10th century CE: 3 titles, 73,010 words**
- **11th century CE: 3 titles, 6,784 words**
- **12th century CE: 1 titles, 3,881 words**
- ~~13th century CE: 0 titles, 0 words~~
- ~~14th century CE: 0 titles, 0 words~~
- **15th century CE: 3 titles, 62,272 words**
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 12 titles, 159,787 words**


### *MAJALLAT* (6 texts, 9,765,526 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- **11th century CE: 1 titles, 65,541 words**
- ~~12th century CE: 0 titles, 0 words~~
- ~~13th century CE: 0 titles, 0 words~~
- **14th century CE: 1 titles, 313,586 words**
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- **19th century CE: 3 titles, 1,093,849 words**
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 6 titles, 9,765,526 words**


### *MAJMUCAT* (44 texts, 18,468,777 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 2 titles, 303,136 words**
- **09th century CE: 1 titles, 170,879 words**
- **10th century CE: 2 titles, 445,570 words**
- **11th century CE: 5 titles, 1,774,838 words**
- **12th century CE: 3 titles, 279,197 words**
- **13th century CE: 5 titles, 557,996 words**
- **14th century CE: 12 titles, 1,363,798 words**
- **15th century CE: 5 titles, 1,823,726 words**
- **16th century CE: 2 titles, 2,198,479 words**
- **17th century CE: 1 titles, 9,197 words**
- **18th century CE: 1 titles, 143,312 words**
- **19th century CE: 3 titles, 1,093,849 words**
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 44 titles, 18,468,777 words**


### *MAKHTUTAT* (300 texts, 1,975,198 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 2 titles, 11,989 words**
- **09th century CE: 16 titles, 74,770 words**
- **10th century CE: 57 titles, 257,661 words**
- **11th century CE: 88 titles, 476,913 words**
- **12th century CE: 66 titles, 571,884 words**
- **13th century CE: 28 titles, 286,314 words**
- **14th century CE: 14 titles, 94,675 words**
- **15th century CE: 20 titles, 91,423 words**
- **16th century CE: 7 titles, 60,617 words**
- ~~17th century CE: 0 titles, 0 words~~
- **18th century CE: 2 titles, 48,952 words**
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 300 titles, 1,975,198 words**


### *MALIKI* (44 texts, 24,962,848 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 2 titles, 1,151,308 words**
- **09th century CE: 1 titles, 6,087 words**
- **10th century CE: 5 titles, 2,091,441 words**
- **11th century CE: 3 titles, 2,766,621 words**
- **12th century CE: 5 titles, 4,011,653 words**
- **13th century CE: 2 titles, 1,325,252 words**
- **14th century CE: 4 titles, 561,759 words**
- **15th century CE: 3 titles, 763,044 words**
- **16th century CE: 4 titles, 1,509,129 words**
- **17th century CE: 3 titles, 3,197,848 words**
- **18th century CE: 3 titles, 2,150,734 words**
- **19th century CE: 5 titles, 4,911,364 words**
- **20th century CE: 1 titles, 177,397 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 44 titles, 24,962,848 words**


### *MANSUKH* (8 texts, 213,315 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 1 titles, 3,261 words**
- ~~09th century CE: 0 titles, 0 words~~
- **10th century CE: 1 titles, 90,849 words**
- **11th century CE: 2 titles, 25,121 words**
- **12th century CE: 2 titles, 70,568 words**
- ~~13th century CE: 0 titles, 0 words~~
- **14th century CE: 1 titles, 4,209 words**
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- **17th century CE: 1 titles, 19,307 words**
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 8 titles, 213,315 words**


### *MANTIQ* (7 texts, 3,487,980 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- **13th century CE: 2 titles, 1,870,333 words**
- ~~14th century CE: 0 titles, 0 words~~
- **15th century CE: 2 titles, 387,628 words**
- ~~16th century CE: 0 titles, 0 words~~
- **17th century CE: 3 titles, 1,230,019 words**
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 7 titles, 3,487,980 words**


### *MASAIL* (285 texts, 9,044,295 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 4 titles, 117,551 words**
- **09th century CE: 24 titles, 872,725 words**
- **10th century CE: 22 titles, 532,227 words**
- **11th century CE: 20 titles, 934,826 words**
- **12th century CE: 9 titles, 111,801 words**
- **13th century CE: 15 titles, 1,264,579 words**
- **14th century CE: 25 titles, 1,056,018 words**
- **15th century CE: 11 titles, 466,517 words**
- **16th century CE: 25 titles, 534,978 words**
- **17th century CE: 7 titles, 60,347 words**
- **18th century CE: 18 titles, 218,970 words**
- **19th century CE: 5 titles, 222,208 words**
- **20th century CE: 4 titles, 105,937 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 285 titles, 9,044,295 words**


### *MASANID* (39 texts, 8,094,316 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 1 titles, 19,958 words**
- **09th century CE: 15 titles, 3,322,911 words**
- **10th century CE: 20 titles, 4,575,089 words**
- **11th century CE: 3 titles, 176,358 words**
- ~~12th century CE: 0 titles, 0 words~~
- ~~13th century CE: 0 titles, 0 words~~
- ~~14th century CE: 0 titles, 0 words~~
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 39 titles, 8,094,316 words**


### *MAWDUC* (44 texts, 4,118,004 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 6 titles, 313,864 words**
- **10th century CE: 5 titles, 1,149,393 words**
- **11th century CE: 1 titles, 4,804 words**
- **12th century CE: 8 titles, 1,228,988 words**
- **13th century CE: 3 titles, 58,198 words**
- **14th century CE: 7 titles, 116,023 words**
- **15th century CE: 1 titles, 154,496 words**
- **16th century CE: 3 titles, 581,473 words**
- **17th century CE: 3 titles, 65,752 words**
- **18th century CE: 2 titles, 276,756 words**
- **19th century CE: 5 titles, 168,257 words**
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 44 titles, 4,118,004 words**


### *MILAL* (230 texts, 12,713,631 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 2 titles, 7,598 words**
- **09th century CE: 23 titles, 464,663 words**
- **10th century CE: 38 titles, 1,289,107 words**
- **11th century CE: 39 titles, 2,873,359 words**
- **12th century CE: 19 titles, 1,015,259 words**
- **13th century CE: 16 titles, 512,816 words**
- **14th century CE: 43 titles, 5,059,850 words**
- **15th century CE: 4 titles, 197,786 words**
- **16th century CE: 4 titles, 295,951 words**
- **17th century CE: 5 titles, 86,504 words**
- **18th century CE: 18 titles, 170,202 words**
- **19th century CE: 12 titles, 336,647 words**
- **20th century CE: 5 titles, 309,736 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 230 titles, 12,713,631 words**


### *MISC* (321 texts, 26,457,643 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 3 titles, 222,454 words**
- **09th century CE: 12 titles, 564,427 words**
- **10th century CE: 39 titles, 3,105,199 words**
- **11th century CE: 57 titles, 3,360,982 words**
- **12th century CE: 52 titles, 4,306,746 words**
- **13th century CE: 39 titles, 3,153,454 words**
- **14th century CE: 38 titles, 4,626,265 words**
- **15th century CE: 15 titles, 2,182,981 words**
- **16th century CE: 22 titles, 1,036,484 words**
- **17th century CE: 9 titles, 612,280 words**
- **18th century CE: 7 titles, 1,102,622 words**
- **19th century CE: 10 titles, 352,892 words**
- **20th century CE: 7 titles, 631,542 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 321 titles, 26,457,643 words**


### *MUDHAKKARAT* (11 texts, 955,128 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- **10th century CE: 5 titles, 167,892 words**
- ~~11th century CE: 0 titles, 0 words~~
- **12th century CE: 1 titles, 189,565 words**
- **13th century CE: 1 titles, 73,841 words**
- **14th century CE: 2 titles, 413,699 words**
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- **20th century CE: 1 titles, 21,388 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 11 titles, 955,128 words**


### *MUFASSIRUN* (3 texts, 146,094 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- ~~13th century CE: 0 titles, 0 words~~
- **14th century CE: 1 titles, 95,375 words**
- ~~15th century CE: 0 titles, 0 words~~
- **16th century CE: 1 titles, 11,388 words**
- **17th century CE: 1 titles, 39,331 words**
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 3 titles, 146,094 words**


### *MUKHADRAM* (8 texts, 75,727 words)

- ~~06th century CE: 0 titles, 0 words~~
- **07th century CE: 3 titles, 28,157 words**
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- ~~13th century CE: 0 titles, 0 words~~
- ~~14th century CE: 0 titles, 0 words~~
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 8 titles, 75,727 words**


### *MUSHKIL* (10 texts, 1,966,407 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 2 titles, 61,975 words**
- **10th century CE: 1 titles, 844,012 words**
- **11th century CE: 1 titles, 59,081 words**
- **12th century CE: 1 titles, 324,113 words**
- **13th century CE: 1 titles, 327,540 words**
- **14th century CE: 4 titles, 349,686 words**
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 10 titles, 1,966,407 words**


### *MUSTALAHAT* (224 texts, 31,919,937 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 1 titles, 456,502 words**
- **09th century CE: 25 titles, 1,196,381 words**
- **10th century CE: 34 titles, 3,760,800 words**
- **11th century CE: 36 titles, 5,761,202 words**
- **12th century CE: 25 titles, 2,604,002 words**
- **13th century CE: 19 titles, 2,986,962 words**
- **14th century CE: 14 titles, 4,030,913 words**
- **15th century CE: 25 titles, 2,251,075 words**
- **16th century CE: 15 titles, 583,057 words**
- **17th century CE: 6 titles, 620,121 words**
- **18th century CE: 8 titles, 5,788,532 words**
- **19th century CE: 6 titles, 1,295,648 words**
- **20th century CE: 4 titles, 391,942 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 224 titles, 31,919,937 words**


### *MUSTAQILLA* (6 texts, 2,465,091 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- **12th century CE: 1 titles, 308,981 words**
- ~~13th century CE: 0 titles, 0 words~~
- ~~14th century CE: 0 titles, 0 words~~
- **15th century CE: 2 titles, 484,386 words**
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- **18th century CE: 1 titles, 483,418 words**
- **19th century CE: 2 titles, 1,188,306 words**
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 6 titles, 2,465,091 words**


### *NABI* (60 texts, 11,323,852 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 3 titles, 184,928 words**
- **09th century CE: 3 titles, 568,993 words**
- **10th century CE: 3 titles, 635,431 words**
- **11th century CE: 5 titles, 158,345 words**
- **12th century CE: 8 titles, 911,335 words**
- **13th century CE: 8 titles, 875,639 words**
- **14th century CE: 10 titles, 3,434,571 words**
- **15th century CE: 6 titles, 721,387 words**
- **16th century CE: 2 titles, 2,068,905 words**
- **17th century CE: 2 titles, 803,170 words**
- **18th century CE: 2 titles, 36,022 words**
- **19th century CE: 3 titles, 757,754 words**
- **20th century CE: 5 titles, 167,372 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 60 titles, 11,323,852 words**


### *NAHW* (143 texts, 19,242,451 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 3 titles, 759,638 words**
- **09th century CE: 6 titles, 758,470 words**
- **10th century CE: 17 titles, 814,400 words**
- **11th century CE: 20 titles, 2,292,858 words**
- **12th century CE: 10 titles, 387,864 words**
- **13th century CE: 17 titles, 1,933,136 words**
- **14th century CE: 22 titles, 4,494,202 words**
- **15th century CE: 9 titles, 1,247,701 words**
- **16th century CE: 10 titles, 358,726 words**
- **17th century CE: 4 titles, 608,646 words**
- **18th century CE: 2 titles, 4,869,766 words**
- **19th century CE: 2 titles, 25,295 words**
- **20th century CE: 1 titles, 11,064 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 143 titles, 19,242,451 words**


### *NASIKH* (8 texts, 213,315 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 1 titles, 3,261 words**
- ~~09th century CE: 0 titles, 0 words~~
- **10th century CE: 1 titles, 90,849 words**
- **11th century CE: 2 titles, 25,121 words**
- **12th century CE: 2 titles, 70,568 words**
- ~~13th century CE: 0 titles, 0 words~~
- **14th century CE: 1 titles, 4,209 words**
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- **17th century CE: 1 titles, 19,307 words**
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 8 titles, 213,315 words**


### *NO_TAGS* (3 texts, 89,252 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- ~~13th century CE: 0 titles, 0 words~~
- ~~14th century CE: 0 titles, 0 words~~
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 3 titles, 89,252 words**


### *ONO* (4 texts, 1,237,148 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- **12th century CE: 1 titles, 834,012 words**
- **13th century CE: 2 titles, 381,920 words**
- ~~14th century CE: 0 titles, 0 words~~
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- **17th century CE: 1 titles, 21,216 words**
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 4 titles, 1,237,148 words**


### *POE* (14 texts, 2,583,148 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- **12th century CE: 12 titles, 1,293,728 words**
- **13th century CE: 2 titles, 1,289,420 words**
- ~~14th century CE: 0 titles, 0 words~~
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 14 titles, 2,583,148 words**


### *PPE* (566 texts, 125,456,930 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 2 titles, 4,799 words**
- **09th century CE: 56 titles, 7,322,706 words**
- **10th century CE: 79 titles, 11,288,076 words**
- **11th century CE: 54 titles, 10,756,698 words**
- **12th century CE: 89 titles, 16,891,272 words**
- **13th century CE: 54 titles, 12,631,314 words**
- **14th century CE: 87 titles, 30,102,054 words**
- **15th century CE: 63 titles, 21,062,952 words**
- **16th century CE: 28 titles, 3,259,782 words**
- **17th century CE: 20 titles, 5,750,029 words**
- **18th century CE: 10 titles, 1,404,678 words**
- **19th century CE: 13 titles, 2,943,760 words**
- **20th century CE: 9 titles, 1,923,188 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 566 titles, 125,456,930 words**


### *QADA* (51 texts, 3,726,081 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 1 titles, 4,667 words**
- ~~10th century CE: 0 titles, 0 words~~
- **11th century CE: 11 titles, 735,988 words**
- **12th century CE: 5 titles, 235,118 words**
- **13th century CE: 4 titles, 102,170 words**
- **14th century CE: 10 titles, 789,982 words**
- **15th century CE: 6 titles, 587,448 words**
- **16th century CE: 3 titles, 14,182 words**
- **17th century CE: 1 titles, 304,193 words**
- ~~18th century CE: 0 titles, 0 words~~
- **19th century CE: 1 titles, 521,964 words**
- **20th century CE: 3 titles, 88,639 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 51 titles, 3,726,081 words**


### *QAWACID* (119 texts, 16,819,321 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 2 titles, 177,679 words**
- **10th century CE: 2 titles, 326,081 words**
- **11th century CE: 17 titles, 2,028,529 words**
- **12th century CE: 9 titles, 606,748 words**
- **13th century CE: 16 titles, 1,942,257 words**
- **14th century CE: 19 titles, 4,224,042 words**
- **15th century CE: 6 titles, 3,375,310 words**
- **16th century CE: 7 titles, 1,093,651 words**
- **17th century CE: 2 titles, 447,605 words**
- **18th century CE: 6 titles, 155,300 words**
- **19th century CE: 4 titles, 790,876 words**
- **20th century CE: 3 titles, 295,227 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 119 titles, 16,819,321 words**


### *QIRAAT* (29 texts, 2,385,777 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 2 titles, 19,171 words**
- **10th century CE: 3 titles, 164,650 words**
- **11th century CE: 3 titles, 147,684 words**
- **12th century CE: 2 titles, 179,564 words**
- **13th century CE: 2 titles, 447,891 words**
- **14th century CE: 4 titles, 252,140 words**
- **15th century CE: 3 titles, 354,009 words**
- **16th century CE: 2 titles, 281,824 words**
- ~~17th century CE: 0 titles, 0 words~~
- **18th century CE: 2 titles, 316,791 words**
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 29 titles, 2,385,777 words**


### *QISAS* (54 texts, 6,175,973 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 5 titles, 357,438 words**
- **10th century CE: 11 titles, 1,684,315 words**
- **11th century CE: 10 titles, 657,055 words**
- **12th century CE: 11 titles, 1,212,778 words**
- **13th century CE: 1 titles, 59,132 words**
- **14th century CE: 4 titles, 374,109 words**
- **15th century CE: 5 titles, 910,745 words**
- **16th century CE: 4 titles, 432,793 words**
- **17th century CE: 2 titles, 256,916 words**
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 54 titles, 6,175,973 words**


### *QURAN* (306 texts, 64,746,401 words)

- ~~06th century CE: 0 titles, 0 words~~
- **07th century CE: 2 titles, 108,445 words**
- **08th century CE: 8 titles, 693,458 words**
- **09th century CE: 17 titles, 1,112,291 words**
- **10th century CE: 29 titles, 8,135,996 words**
- **11th century CE: 38 titles, 6,767,528 words**
- **12th century CE: 28 titles, 7,639,257 words**
- **13th century CE: 20 titles, 7,251,433 words**
- **14th century CE: 30 titles, 7,354,603 words**
- **15th century CE: 22 titles, 9,051,956 words**
- **16th century CE: 17 titles, 3,995,653 words**
- **17th century CE: 9 titles, 2,532,080 words**
- **18th century CE: 10 titles, 824,933 words**
- **19th century CE: 4 titles, 5,238,487 words**
- **20th century CE: 3 titles, 166,927 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 306 titles, 64,746,401 words**


### *RAQAIQ* (188 texts, 10,269,908 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 1 titles, 16,317 words**
- **09th century CE: 9 titles, 282,039 words**
- **10th century CE: 14 titles, 771,481 words**
- **11th century CE: 13 titles, 355,629 words**
- **12th century CE: 28 titles, 2,558,803 words**
- **13th century CE: 14 titles, 1,153,698 words**
- **14th century CE: 13 titles, 983,884 words**
- **15th century CE: 5 titles, 320,080 words**
- **16th century CE: 10 titles, 365,106 words**
- **17th century CE: 1 titles, 5,107 words**
- **18th century CE: 3 titles, 870,170 words**
- **19th century CE: 4 titles, 234,025 words**
- **20th century CE: 2 titles, 112,685 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 188 titles, 10,269,908 words**


### *RIHLAT* (70 texts, 7,980,411 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 1 titles, 2,282 words**
- **10th century CE: 15 titles, 662,259 words**
- **11th century CE: 7 titles, 570,333 words**
- **12th century CE: 6 titles, 401,777 words**
- **13th century CE: 11 titles, 1,848,229 words**
- **14th century CE: 9 titles, 1,971,009 words**
- **15th century CE: 6 titles, 1,172,741 words**
- **16th century CE: 3 titles, 614,971 words**
- **17th century CE: 2 titles, 67,554 words**
- **18th century CE: 1 titles, 69,554 words**
- **19th century CE: 1 titles, 112,731 words**
- **20th century CE: 3 titles, 150,390 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 70 titles, 7,980,411 words**


### *RUDUD* (65 texts, 4,134,417 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 1 titles, 1,418 words**
- **09th century CE: 3 titles, 97,763 words**
- **10th century CE: 3 titles, 142,666 words**
- **11th century CE: 5 titles, 112,094 words**
- **12th century CE: 5 titles, 288,531 words**
- **13th century CE: 1 titles, 21,700 words**
- **14th century CE: 14 titles, 1,785,050 words**
- **15th century CE: 3 titles, 161,610 words**
- **16th century CE: 3 titles, 187,172 words**
- **17th century CE: 4 titles, 105,933 words**
- **18th century CE: 4 titles, 46,843 words**
- **19th century CE: 6 titles, 94,066 words**
- **20th century CE: 10 titles, 842,402 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 65 titles, 4,134,417 words**


### *SAHIH* (10 texts, 4,806,999 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 2 titles, 1,090,940 words**
- **10th century CE: 3 titles, 1,188,183 words**
- **11th century CE: 3 titles, 1,730,031 words**
- ~~12th century CE: 0 titles, 0 words~~
- **13th century CE: 1 titles, 595,389 words**
- ~~14th century CE: 0 titles, 0 words~~
- **15th century CE: 1 titles, 202,456 words**
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 10 titles, 4,806,999 words**


### *SARF* (125 texts, 6,904,155 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 2 titles, 303,136 words**
- **09th century CE: 2 titles, 268,707 words**
- **10th century CE: 17 titles, 814,400 words**
- **11th century CE: 16 titles, 1,079,132 words**
- **12th century CE: 10 titles, 387,864 words**
- **13th century CE: 14 titles, 778,257 words**
- **14th century CE: 19 titles, 981,731 words**
- **15th century CE: 8 titles, 668,003 words**
- **16th century CE: 10 titles, 358,726 words**
- **17th century CE: 3 titles, 22,292 words**
- **18th century CE: 1 titles, 524,863 words**
- **19th century CE: 2 titles, 25,295 words**
- **20th century CE: 1 titles, 11,064 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 125 titles, 6,904,155 words**


### *SARH* (21 texts, 12,848,371 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 1 titles, 456,502 words**
- **09th century CE: 5 titles, 587,591 words**
- ~~10th century CE: 0 titles, 0 words~~
- **11th century CE: 4 titles, 1,213,726 words**
- ~~12th century CE: 0 titles, 0 words~~
- **13th century CE: 4 titles, 1,415,965 words**
- **14th century CE: 4 titles, 3,663,632 words**
- **15th century CE: 1 titles, 579,698 words**
- ~~16th century CE: 0 titles, 0 words~~
- **17th century CE: 1 titles, 586,354 words**
- **18th century CE: 1 titles, 4,344,903 words**
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 21 titles, 12,848,371 words**


### *SBS* (17 texts, 4,334,477 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 14 titles, 1,288,949 words**
- **10th century CE: 1 titles, 2,919,964 words**
- **11th century CE: 1 titles, 117,248 words**
- ~~12th century CE: 0 titles, 0 words~~
- ~~13th century CE: 0 titles, 0 words~~
- **14th century CE: 1 titles, 8,316 words**
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 17 titles, 4,334,477 words**


### *SHAFICI* (67 texts, 46,379,011 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 7 titles, 1,925,304 words**
- ~~10th century CE: 0 titles, 0 words~~
- **11th century CE: 7 titles, 5,704,498 words**
- **12th century CE: 5 titles, 1,907,928 words**
- **13th century CE: 7 titles, 6,324,457 words**
- **14th century CE: 3 titles, 483,862 words**
- **15th century CE: 4 titles, 484,155 words**
- **16th century CE: 21 titles, 12,761,665 words**
- **17th century CE: 1 titles, 590,267 words**
- **18th century CE: 3 titles, 6,606,897 words**
- **19th century CE: 5 titles, 3,947,008 words**
- **20th century CE: 1 titles, 186,843 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 67 titles, 46,379,011 words**


### *SHAMAIL* (89 texts, 16,634,819 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 1 titles, 79,120 words**
- **09th century CE: 5 titles, 742,916 words**
- **10th century CE: 2 titles, 168,433 words**
- **11th century CE: 7 titles, 1,701,532 words**
- **12th century CE: 5 titles, 948,938 words**
- **13th century CE: 5 titles, 555,467 words**
- **14th century CE: 8 titles, 3,323,030 words**
- **15th century CE: 7 titles, 1,618,141 words**
- **16th century CE: 9 titles, 3,339,882 words**
- **17th century CE: 3 titles, 1,511,000 words**
- **18th century CE: 5 titles, 572,406 words**
- **19th century CE: 1 titles, 146,888 words**
- **20th century CE: 2 titles, 120,102 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 89 titles, 16,634,819 words**


### *SHARH* (84 texts, 37,821,300 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 1 titles, 1,221,983 words**
- **09th century CE: 8 titles, 984,601 words**
- **10th century CE: 2 titles, 335,221 words**
- **11th century CE: 6 titles, 5,410,008 words**
- **12th century CE: 4 titles, 1,141,752 words**
- **13th century CE: 8 titles, 1,044,491 words**
- **14th century CE: 12 titles, 2,118,910 words**
- **15th century CE: 7 titles, 9,702,633 words**
- **16th century CE: 10 titles, 4,508,162 words**
- **17th century CE: 7 titles, 5,635,204 words**
- **18th century CE: 5 titles, 2,238,457 words**
- **19th century CE: 3 titles, 1,336,770 words**
- **20th century CE: 2 titles, 1,372,981 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 84 titles, 37,821,300 words**


### *SHC* (18 texts, 3,549,125 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- **10th century CE: 1 titles, 21,065 words**
- **11th century CE: 3 titles, 369,208 words**
- **12th century CE: 2 titles, 256,292 words**
- ~~13th century CE: 0 titles, 0 words~~
- **14th century CE: 3 titles, 280,267 words**
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- **17th century CE: 3 titles, 1,119,469 words**
- **18th century CE: 4 titles, 687,525 words**
- **19th century CE: 2 titles, 815,299 words**
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 18 titles, 3,549,125 words**


### *SHICI* (448 texts, 107,414,120 words)

- ~~06th century CE: 0 titles, 0 words~~
- **07th century CE: 6 titles, 317,686 words**
- **08th century CE: 8 titles, 607,856 words**
- **09th century CE: 10 titles, 1,098,703 words**
- **10th century CE: 45 titles, 6,607,596 words**
- **11th century CE: 89 titles, 9,608,844 words**
- **12th century CE: 25 titles, 5,006,848 words**
- **13th century CE: 47 titles, 4,541,156 words**
- **14th century CE: 35 titles, 9,506,644 words**
- **15th century CE: 16 titles, 3,289,582 words**
- **16th century CE: 20 titles, 7,263,281 words**
- **17th century CE: 48 titles, 25,919,253 words**
- **18th century CE: 25 titles, 8,778,817 words**
- **19th century CE: 44 titles, 18,941,125 words**
- **20th century CE: 30 titles, 5,926,729 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 448 titles, 107,414,120 words**


### *SHICR* (196 texts, 8,626,024 words)

- ~~06th century CE: 0 titles, 0 words~~
- **07th century CE: 19 titles, 107,439 words**
- **08th century CE: 14 titles, 238,833 words**
- **09th century CE: 14 titles, 728,032 words**
- **10th century CE: 12 titles, 432,001 words**
- **11th century CE: 20 titles, 1,846,674 words**
- **12th century CE: 9 titles, 399,309 words**
- **13th century CE: 11 titles, 674,105 words**
- **14th century CE: 6 titles, 523,335 words**
- ~~15th century CE: 0 titles, 0 words~~
- **16th century CE: 1 titles, 5,661 words**
- **17th century CE: 3 titles, 1,044,278 words**
- **18th century CE: 4 titles, 156,481 words**
- **19th century CE: 4 titles, 154,066 words**
- **20th century CE: 5 titles, 456,705 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 196 titles, 8,626,024 words**


### *SIRA* (166 texts, 24,328,846 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 4 titles, 230,233 words**
- **09th century CE: 11 titles, 1,564,212 words**
- **10th century CE: 11 titles, 870,331 words**
- **11th century CE: 13 titles, 1,881,774 words**
- **12th century CE: 14 titles, 2,067,885 words**
- **13th century CE: 17 titles, 1,744,136 words**
- **14th century CE: 15 titles, 4,168,796 words**
- **15th century CE: 13 titles, 2,339,528 words**
- **16th century CE: 15 titles, 4,154,291 words**
- **17th century CE: 5 titles, 1,672,794 words**
- **18th century CE: 8 titles, 635,786 words**
- **19th century CE: 4 titles, 904,642 words**
- **20th century CE: 7 titles, 287,474 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 166 titles, 24,328,846 words**


### *SIYASA* (66 texts, 5,383,972 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 1 titles, 11,433 words**
- **09th century CE: 5 titles, 238,423 words**
- ~~10th century CE: 0 titles, 0 words~~
- **11th century CE: 12 titles, 759,550 words**
- **12th century CE: 5 titles, 235,118 words**
- **13th century CE: 4 titles, 102,170 words**
- **14th century CE: 18 titles, 952,052 words**
- **15th century CE: 6 titles, 587,448 words**
- **16th century CE: 3 titles, 14,182 words**
- **17th century CE: 1 titles, 304,193 words**
- ~~18th century CE: 0 titles, 0 words~~
- **19th century CE: 2 titles, 1,749,034 words**
- **20th century CE: 3 titles, 88,639 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 66 titles, 5,383,972 words**


### *SUALAT* (64 texts, 4,517,643 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 16 titles, 515,025 words**
- **10th century CE: 10 titles, 1,292,035 words**
- **11th century CE: 5 titles, 83,084 words**
- **12th century CE: 10 titles, 1,376,162 words**
- **13th century CE: 3 titles, 25,027 words**
- **14th century CE: 3 titles, 100,309 words**
- ~~15th century CE: 0 titles, 0 words~~
- **16th century CE: 4 titles, 649,219 words**
- **17th century CE: 3 titles, 65,752 words**
- **18th century CE: 1 titles, 15,433 words**
- **19th century CE: 3 titles, 57,089 words**
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 64 titles, 4,517,643 words**


### *SULUK* (88 texts, 6,377,189 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 1 titles, 9,586 words**
- **09th century CE: 3 titles, 58,239 words**
- **10th century CE: 6 titles, 465,262 words**
- **11th century CE: 10 titles, 360,884 words**
- **12th century CE: 12 titles, 1,622,284 words**
- **13th century CE: 3 titles, 90,736 words**
- **14th century CE: 33 titles, 2,925,743 words**
- **15th century CE: 2 titles, 28,166 words**
- **16th century CE: 7 titles, 311,789 words**
- **17th century CE: 1 titles, 16,342 words**
- **18th century CE: 2 titles, 48,092 words**
- **19th century CE: 4 titles, 170,074 words**
- **20th century CE: 1 titles, 109,344 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 88 titles, 6,377,189 words**


### *SUNAN* (16 texts, 5,570,177 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 8 titles, 1,196,149 words**
- **10th century CE: 5 titles, 2,074,402 words**
- **11th century CE: 2 titles, 2,249,667 words**
- ~~12th century CE: 0 titles, 0 words~~
- ~~13th century CE: 0 titles, 0 words~~
- ~~14th century CE: 0 titles, 0 words~~
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 16 titles, 5,570,177 words**


### *SUNNI* (362 texts, 114,529,616 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 9 titles, 680,173 words**
- **09th century CE: 81 titles, 10,982,136 words**
- **10th century CE: 80 titles, 16,393,874 words**
- **11th century CE: 61 titles, 15,302,943 words**
- **12th century CE: 21 titles, 13,570,825 words**
- **13th century CE: 24 titles, 10,489,844 words**
- **14th century CE: 29 titles, 15,608,560 words**
- **15th century CE: 29 titles, 16,550,971 words**
- **16th century CE: 14 titles, 6,195,895 words**
- **17th century CE: 3 titles, 1,835,177 words**
- **18th century CE: 7 titles, 515,627 words**
- **19th century CE: 2 titles, 5,053,898 words**
- **20th century CE: 2 titles, 1,349,693 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 362 titles, 114,529,616 words**


### *TABAQAT* (351 texts, 74,811,081 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 2 titles, 4,799 words**
- **09th century CE: 40 titles, 4,219,795 words**
- **10th century CE: 58 titles, 4,677,487 words**
- **11th century CE: 39 titles, 8,638,308 words**
- **12th century CE: 28 titles, 11,997,906 words**
- **13th century CE: 29 titles, 6,812,821 words**
- **14th century CE: 50 titles, 20,599,483 words**
- **15th century CE: 40 titles, 10,494,696 words**
- **16th century CE: 20 titles, 1,786,368 words**
- **17th century CE: 12 titles, 1,916,318 words**
- **18th century CE: 6 titles, 597,271 words**
- **19th century CE: 4 titles, 522,964 words**
- **20th century CE: 5 titles, 1,509,023 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 351 titles, 74,811,081 words**


### *TAFSIR* (207 texts, 84,047,256 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 8 titles, 901,167 words**
- **09th century CE: 13 titles, 1,116,982 words**
- **10th century CE: 23 titles, 9,199,726 words**
- **11th century CE: 27 titles, 7,106,368 words**
- **12th century CE: 22 titles, 7,661,236 words**
- **13th century CE: 20 titles, 7,893,906 words**
- **14th century CE: 23 titles, 9,178,285 words**
- **15th century CE: 13 titles, 8,112,759 words**
- **16th century CE: 11 titles, 5,199,679 words**
- **17th century CE: 10 titles, 4,583,698 words**
- **18th century CE: 9 titles, 3,294,587 words**
- **19th century CE: 7 titles, 11,873,202 words**
- **20th century CE: 2 titles, 1,458,280 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 207 titles, 84,047,256 words**


### *TAJWID* (16 texts, 1,411,578 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 1 titles, 12,707 words**
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- **12th century CE: 1 titles, 165,640 words**
- ~~13th century CE: 0 titles, 0 words~~
- **14th century CE: 3 titles, 249,424 words**
- **15th century CE: 2 titles, 350,976 words**
- **16th century CE: 2 titles, 281,824 words**
- ~~17th century CE: 0 titles, 0 words~~
- **18th century CE: 1 titles, 128,954 words**
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 16 titles, 1,411,578 words**


### *TAKHRIJ* (77 texts, 25,299,880 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- **10th century CE: 2 titles, 230,094 words**
- **11th century CE: 1 titles, 457,750 words**
- **12th century CE: 3 titles, 612,516 words**
- **13th century CE: 3 titles, 1,680,962 words**
- **14th century CE: 16 titles, 4,402,122 words**
- **15th century CE: 25 titles, 10,037,751 words**
- **16th century CE: 6 titles, 4,832,402 words**
- **17th century CE: 4 titles, 499,033 words**
- **18th century CE: 1 titles, 261,323 words**
- **19th century CE: 4 titles, 488,002 words**
- **20th century CE: 1 titles, 51,274 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 77 titles, 25,299,880 words**


### *TARAIF* (54 texts, 6,175,973 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 5 titles, 357,438 words**
- **10th century CE: 11 titles, 1,684,315 words**
- **11th century CE: 10 titles, 657,055 words**
- **12th century CE: 11 titles, 1,212,778 words**
- **13th century CE: 1 titles, 59,132 words**
- **14th century CE: 4 titles, 374,109 words**
- **15th century CE: 5 titles, 910,745 words**
- **16th century CE: 4 titles, 432,793 words**
- **17th century CE: 2 titles, 256,916 words**
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 54 titles, 6,175,973 words**


### *TARAJIM* (768 texts, 151,346,090 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 14 titles, 413,129 words**
- **09th century CE: 103 titles, 12,645,847 words**
- **10th century CE: 164 titles, 17,829,604 words**
- **11th century CE: 94 titles, 17,576,228 words**
- **12th century CE: 63 titles, 15,815,884 words**
- **13th century CE: 51 titles, 11,670,393 words**
- **14th century CE: 83 titles, 24,375,733 words**
- **15th century CE: 71 titles, 25,405,455 words**
- **16th century CE: 39 titles, 7,659,816 words**
- **17th century CE: 26 titles, 9,400,189 words**
- **18th century CE: 17 titles, 2,861,595 words**
- **19th century CE: 11 titles, 1,509,853 words**
- **20th century CE: 9 titles, 2,934,168 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 768 titles, 151,346,090 words**


### *TARIKH* (310 texts, 74,474,408 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 2 titles, 4,799 words**
- **09th century CE: 37 titles, 4,344,252 words**
- **10th century CE: 41 titles, 5,260,659 words**
- **11th century CE: 29 titles, 4,737,481 words**
- **12th century CE: 37 titles, 14,997,022 words**
- **13th century CE: 30 titles, 7,831,288 words**
- **14th century CE: 40 titles, 18,840,746 words**
- **15th century CE: 33 titles, 9,489,822 words**
- **16th century CE: 16 titles, 1,705,260 words**
- **17th century CE: 12 titles, 3,894,897 words**
- **18th century CE: 7 titles, 395,846 words**
- **19th century CE: 4 titles, 1,174,238 words**
- **20th century CE: 5 titles, 812,131 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 310 titles, 74,474,408 words**


### *TASAWWUF* (9 texts, 2,412,869 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- **10th century CE: 3 titles, 421,781 words**
- **11th century CE: 1 titles, 113,883 words**
- **12th century CE: 3 titles, 44,938 words**
- **13th century CE: 1 titles, 1,826,396 words**
- **14th century CE: 1 titles, 5,871 words**
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 9 titles, 2,412,869 words**


### *TAZKIYA* (34 texts, 3,209,984 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- **13th century CE: 4 titles, 686,978 words**
- **14th century CE: 28 titles, 2,382,348 words**
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- **18th century CE: 1 titles, 11,024 words**
- **19th century CE: 1 titles, 129,634 words**
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 34 titles, 3,209,984 words**


### *THIQAT* (13 texts, 3,327,383 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 2 titles, 117,398 words**
- **10th century CE: 4 titles, 588,135 words**
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- ~~13th century CE: 0 titles, 0 words~~
- **14th century CE: 6 titles, 2,550,137 words**
- ~~15th century CE: 0 titles, 0 words~~
- **16th century CE: 1 titles, 71,713 words**
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 13 titles, 3,327,383 words**


### *TIBB* (77 texts, 5,223,263 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 10 titles, 708,510 words**
- **10th century CE: 2 titles, 1,294,196 words**
- **11th century CE: 8 titles, 787,810 words**
- ~~12th century CE: 0 titles, 0 words~~
- **13th century CE: 26 titles, 1,015,160 words**
- **14th century CE: 17 titles, 215,823 words**
- **15th century CE: 9 titles, 476,779 words**
- **16th century CE: 1 titles, 363,021 words**
- **17th century CE: 1 titles, 303,945 words**
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 77 titles, 5,223,263 words**


### *TOOLARGE* (1 texts, 11,672,533 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- ~~13th century CE: 0 titles, 0 words~~
- ~~14th century CE: 0 titles, 0 words~~
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- **17th century CE: 1 titles, 11,672,533 words**
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 1 titles, 11,672,533 words**


### *TWELVERS* (58 texts, 5,318,002 words)

- ~~06th century CE: 0 titles, 0 words~~
- **07th century CE: 1 titles, 25,843 words**
- **08th century CE: 1 titles, 121,053 words**
- **09th century CE: 2 titles, 50,166 words**
- **10th century CE: 6 titles, 160,864 words**
- **11th century CE: 5 titles, 454,119 words**
- **12th century CE: 2 titles, 84,876 words**
- **13th century CE: 6 titles, 330,135 words**
- **14th century CE: 9 titles, 846,798 words**
- **15th century CE: 2 titles, 139,488 words**
- **16th century CE: 1 titles, 52,433 words**
- **17th century CE: 6 titles, 1,316,857 words**
- **18th century CE: 5 titles, 541,320 words**
- **19th century CE: 4 titles, 394,232 words**
- **20th century CE: 8 titles, 799,818 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 58 titles, 5,318,002 words**


### *UMAWI* (21 texts, 254,022 words)

- ~~06th century CE: 0 titles, 0 words~~
- **07th century CE: 1 titles, 2,804 words**
- **08th century CE: 10 titles, 168,109 words**
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- ~~13th century CE: 0 titles, 0 words~~
- ~~14th century CE: 0 titles, 0 words~~
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 21 titles, 254,022 words**


### *USUL* (221 texts, 28,522,664 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 2 titles, 38,486 words**
- **09th century CE: 11 titles, 452,927 words**
- **10th century CE: 15 titles, 942,405 words**
- **11th century CE: 28 titles, 2,655,382 words**
- **12th century CE: 12 titles, 939,490 words**
- **13th century CE: 22 titles, 4,188,458 words**
- **14th century CE: 40 titles, 6,525,495 words**
- **15th century CE: 8 titles, 3,666,169 words**
- **16th century CE: 15 titles, 1,160,544 words**
- **17th century CE: 6 titles, 665,346 words**
- **18th century CE: 14 titles, 1,073,169 words**
- **19th century CE: 13 titles, 4,103,310 words**
- **20th century CE: 5 titles, 588,052 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 221 titles, 28,522,664 words**


### *USULIYYA* (23 texts, 1,295,289 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- **11th century CE: 6 titles, 92,816 words**
- **12th century CE: 1 titles, 17,517 words**
- **13th century CE: 5 titles, 906,339 words**
- **14th century CE: 2 titles, 38,781 words**
- ~~15th century CE: 0 titles, 0 words~~
- **16th century CE: 2 titles, 154,624 words**
- **17th century CE: 1 titles, 7,058 words**
- **18th century CE: 5 titles, 61,024 words**
- **19th century CE: 1 titles, 17,130 words**
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 23 titles, 1,295,289 words**


### *WAFAYAT* (29 texts, 11,154,222 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- **11th century CE: 1 titles, 67,697 words**
- **12th century CE: 1 titles, 326,827 words**
- **13th century CE: 2 titles, 913,713 words**
- **14th century CE: 6 titles, 4,960,098 words**
- **15th century CE: 11 titles, 3,118,996 words**
- **16th century CE: 3 titles, 257,154 words**
- **17th century CE: 3 titles, 975,284 words**
- ~~18th century CE: 0 titles, 0 words~~
- **19th century CE: 1 titles, 189,890 words**
- **20th century CE: 1 titles, 344,563 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 29 titles, 11,154,222 words**


### *ZAHIRI* (1 texts, 1,480,381 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- ~~09th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- **11th century CE: 1 titles, 1,480,381 words**
- ~~12th century CE: 0 titles, 0 words~~
- ~~13th century CE: 0 titles, 0 words~~
- ~~14th century CE: 0 titles, 0 words~~
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 1 titles, 1,480,381 words**


### *ZAYDI* (3 texts, 1,481,320 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- **08th century CE: 1 titles, 101,083 words**
- ~~09th century CE: 0 titles, 0 words~~
- **10th century CE: 1 titles, 225,391 words**
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- ~~13th century CE: 0 titles, 0 words~~
- ~~14th century CE: 0 titles, 0 words~~
- **15th century CE: 1 titles, 1,154,846 words**
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 3 titles, 1,481,320 words**


### *ZAYDIYYA* (5 texts, 85,596 words)

- ~~06th century CE: 0 titles, 0 words~~
- ~~07th century CE: 0 titles, 0 words~~
- ~~08th century CE: 0 titles, 0 words~~
- **09th century CE: 1 titles, 11,849 words**
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- **13th century CE: 1 titles, 8,291 words**
- ~~14th century CE: 0 titles, 0 words~~
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- **17th century CE: 1 titles, 20,815 words**
- **18th century CE: 1 titles, 8,956 words**
- ~~19th century CE: 0 titles, 0 words~~
- **20th century CE: 1 titles, 35,685 words**
- ~~21st century CE: 0 titles, 0 words~~
- **total CE: 5 titles, 85,596 words**

