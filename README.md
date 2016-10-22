# OpenArabic Project (@ AvH Lehrstuhl für Digital Humanities, U Leipzig, led and curated by Maxim Romanov)

<!--
**Short description**: a short description goes here — what, who, why, etc.

**Team**: ... 
-->


# Contents

- [General Description](#general-description)
- [Prospects and Progress](#prospects-and-progress)
- [Text Description Tags](#text-description-tags)
- [Preliminary Analysis of Categories of Texts](#preliminary-analysis-of-categories-of-texts)
- [Folder structure](#folder-structure)
- [General description of the workflow with mARkdown](#general-description-of-the-workflow-with-markdown)
- [Status Report](#status-report)
- [List of books by centuries (1329 titles)](#list-of-books-by-centuries-1329-titles)
- [Statistics on the corpus](#statistics-on-the-corpus)
- [Summary statistics on the lengths of texts in the corpus](#summary-statistics-on-the-lengths-of-texts-in-the-corpus)
- [Texts by length (duplicates excluded)](#texts-by-length-duplicates-excluded)
- [Texts in chronological order (duplicates excluded)](#texts-in-chronological-order-duplicates-excluded)
- [Chronological Distribution of Texts - up until 1930 (5,467 texts, 726,946,794 words)](#chronological-distribution-of-texts---up-until-1930-5467-texts-726946794-words)
- [Forms, Themes, Genres (provisional assessment)](#forms-themes-genres-provisional-assessment)




## General Description

The goal of OpenArabic is to build a machine-actionable corpus of premodern texts in Arabic to encourage computational analysis of the Arabic literary tradition. Currently, most of the texts are historical in nature (chronicles, biographical collections, geographical treatises and gazetteers, adab, and thematic dictionaries). If you are interested in having other genres and forms, please, get in touch with us.

Most of the texts derive from open-access online collections of premodern and modern Arabic texts such as [http://shamela.ws/](http://shamela.ws/) and [http://shiaonlinelibrary.com/](http://shiaonlinelibrary.com/) (These texts have `Shamela+NUMBER` and `Shia+NUMBER`; some texts are coming from _al-Jāmiʿ al-kabīr_, which has been published on an external HDD and is not available online (`JK+NUMBER`). Initial metadata from these collections is preserved at the beginning of each file.

Currently uploaded texts have been automatically converted from their initial formats into a `mARkdown` format—a flavor of `markdown` for tagging premodern Arabic text. All of our texts require further editing to properly tag their structures. A detailed description of the `mARkdown` scheme and the tagging workflow can be found at [http://maximromanov.github.io/mARkdown/](http://maximromanov.github.io/mARkdown/). When manual tagging is complete our texts will be converted into a CTS-compliant XML format.

For the list of books currently in our corpus, see below.

## Prospects and Progress

| *Texts* | *Status* |
|:--- | ------:|
| Total in the Collection | 10,393 |
| Unique texts | 7,781 |
| Added texts (listed below) | 1,329 |
| Orphans (no TXT) | 2 |

| *Texts* | *Status* |
|:--- | ------:|
| In Progress (`.inProgress`) | 26 |
| Tagged (`.completed`) | 44 |
| Vetted (`.mARkdown`) | 20 |
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

## Preliminary Analysis of Categories of Texts

Based on temporary tags derived from *The Coverage of the Arabic Collection* (the detailed statistics can be found at (https://github.com/OpenArabic/Annotation), in Sections: “Chronological Distribution of Texts” and “Forms, Themes, Genres (provisional assessment)”. Descriptive statistics numbers for “Forms, Themes, Genres (provisional assessment)” are overlapping as most books belong to multiple forms/genres/categories, and often cover multiple themes. At the moment we have *ca.* 7,700 unique Arabic texts with a smaller subset of *ca.* 5,500 unique texts written before 1930 CE (the year 1350 of the Islamic lunar calendar). This selection of texts covers most thoroughly the period from the 9th till 16th century CE (250–700 titles and 30–90 million words per century), but also offers a decent coverage of 7th–8th and 17th–early 20th centuries. Based on our provisional assessment of this collection using metadata that we were able to gather together with texts, the thematic coverage is quite broad broad and includes all major genres that flourished in the Arabic-Islamic written tradition: 

* The broad category of “fine literature”/belles-lettres (*adab*) includes ca. 600 texts, with over 50 million words; its subcategories—also quite broadly defined—cover such areas as “ethics,” (*aḫlāq*)—204 titles, with 12 million words; rhetoric (*balāġaŧ*)—357 texts, with 33,3 million words; poetic theory, or “science of versification” (*ʿarūḍ*)—9 texts, with 1,9 million words; poetic collections (*šiʿr*)—196 texts with 8,6 million words (collections of poetry, *dīwān*s, cover all major historical periods/regions: pre-Islamic, early Islamic, Umayyad, ʿAbbāsid, Andalusi, ʿUṯmānī/Ottoman); collections of sayings and proverbs (*amṯāl*)—15 texts, with 1,3 million words;
* Geographical texts and travelogues: general geographies (*buldān*/*juġrafīyaŧ*)—152 texts, with 32,7 million words; travelogues (*riḥlāt*)—70 texts, 7,9 million words;
* Historical texts and chronicles (*tawāriḫ*)—310 texts, 74,4 million words;
* Biographical texts and collections of biographies (*siyar*, *tarājim* and *ṭabaqāt*)—768 texts, with 151 million words;
* Administrative practice (*ṣināʿaŧ al-kitābaŧ*)— ... ; and governance (*siyāsaŧ*)—66 texts, with 5,3 million words; 
* Genealogical texts (*ansāb*)—36 texts, with 5,7 million words;
*  *Islamic religious texts I.* The Qurʾān and Qurʾānic sciences, which include: exegesis (*tafsīr*)—207 texts, 84 million words; *qiraʾāt*, recitations—29 texts, 2,4 million words; *tajwīd*, “art of recitation”—16 texts, 1,4 million words;
* *Islamic religious texts II.*—Tradition and traditionalist sciences (*ḥadīṯ*); collections of reliable transmitters (*ṯiqāt*)—13 texts, 3,3 million words; “analysis of sources” (*taḫrīj*)—77 texts, 25,3 million words;
* *Islamic religious texts IIIa.* Islamic law and legal sciences: legal theory (*fiqh*)—776 texts, with 255 million words; collections of legal decisions (*fatāwá*)—31 text, with 6,7 million words; *IIIb.* Teachings of different legal schools: Ḥanafīs—...; Mālikīs—...; Šāfiʿīs—67 texts, 46,3 words; Ḥanbalīs—...; Jaʿfarīs (“Twelvers”)—...; Ẓāhirīs—1 text, 1,5 million words; Zaydīs—3 texts, 1,5 million words;
* *Islamic religious texts IV.* Theological treatises and dogmatics (*ʿaqāʾid*): 519 texts, 28,2 million words;
* Doxographical texts: “religious communities” (*milal*)—230 texts, 12,7 million words; “religious divisions” (*firaq*)—19 texts, 2 million words; refutations (*rudūd*)—65 texts, 4,1 million words;
* Medical texts (*ṭibb*), including both Greek and Islamic traditions—77 texts, with 5,2 million words; (**NB**: Including a collection of texts prepared by Professor Peter Pormann and his team at U Manchester within the “Arabic Commentaries on the Hippocratic Aphorisms” project—64 texts, with *ca.* 1 million words);
* Texts by smaller religious communities: Twelver Shiʿites—58 texts, 5,3 million words; Zaydī Shiʿites—5 texts, *ca.* 85,000 words); Ṣūfī texts—9 texts, 2,4 million words; 
* Greek/Hellenistic tradition—altogether 150 texts, with 2,4 million words, including philosophical (*falsafaŧ*) and natural sciences texts—93 texts, 4,9 million words (**NB**: Including texts from “A Digital Corpus for Graeco-Arabic Studies” (http://www.graeco-arabic-studies.org/), whose Arabic section includes 77 texts, with *ca.* 1 million words);
* Bibliographical texts and collections (*fahāris*)—54 texts, with 8,2 million words;
* Arabic language: grammar (*naḥw*)—143 texts, with 19 million words; morphology (*ṣarf*)—143 texts, 19 million words; lexicons of rare words (*ġarīb*)—126 texts, with 28 million words;
* Early modern journals (*majallaŧ*): ...; 
* Memoires (*muḏakkarāt*)—11 texts, *ca.* 1 million words; 
* Reference books of different kind: technical terminology of various disciplines (*muṣṭalaḥāt*)—224 texts, 31,9 million words; 

**NB**: These categories based on the currently available metadata; creating detailed metadata on authors and their books, by the end of the project we will provide a very detailed and precise description of the coverage of this collection. 




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

**Adding PDFs:** Ideally, we need to start collecting PDFs on which our texts are based and rename them according to some clear pattern that will be appendable to the URI scheme: + `./print/Place_YEAR_XXX.pdff`, where `XXX` is the ordinal number of a volume (prepending zeros) and the extension is changed to `.pdff` since by default `*.pdf` files are excluded from repositories.



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
 
* 90 titles
* 57,561,691 words
* 277,944 logical units
* 56,798 bios

### `*.inProgress` (26 titles: 22,088,362 words; 83,793 units; 0 bios)

- `0230IbnSacd.TabaqatKubra (920,980 words; 6,386 units; 0 bios)`
- `0255Jahiz.Hayawan (456,584 words; 3,186 units; 0 bios)`
- `0256Bukhari.TarikhKabir (519,629 words; 15,061 units; 0 bios)`
- `0276IbnQutaybaDinawari.CuyunAkhbar (232,763 words; 310 units; 0 bios)`
- `0282AbuHanifaDinawari.AkhbarTiwal  (93,184 words; 858 units; 0 bios)`
- `0282AbuHanifaDinawari.AkhbarTiwal (93,182 words; 458 units; 0 bios)`
- `0306IbnHayyanDabbi.AkhbarQudat (237,236 words; 1,976 units; 0 bios)`
- `0310Tabari.JamicBayan (2,850,544 words; 0 units; 0 bios)`
- `0310Tabari.Tarikh (1,468,736 words; 577 units; 0 bios)`
- `0310Tabari.Tarikh (1,053,157 words; 417 units; 0 bios)`
- `0324Ashcari.MaqalatIslamiyyin (94,221 words; 5 units; 0 bios)`
- `0324Ashcari.MaqalatIslamiyyin (100,232 words; 2,635 units; 0 bios)`
- `0328IbnCabdRabbihi.CiqdFarid (562,475 words; 3,607 units; 0 bios)`
- `0335Suli.AkhbarRadi (165,915 words; 255 units; 0 bios)`
- `0346Istakhri.MasalikWaMamalik (75,617 words; 28 units; 0 bios)`
- `0365IbnFaqihHamadhani.Buldan (147,627 words; 74 units; 0 bios)`
- `0400IbnTahirMaqdisi.BadWaTarikh (197,351 words; 639 units; 0 bios)`
- `0421Miskawayh.Tajarib (679,938 words; 2,490 units; 0 bios)`
- `0421Miskawayh.Tajarib (244,209 words; 764 units; 0 bios)`
- `0646IbnQifti.IkhbarCulama (96,909 words; 85 units; 0 bios)`
- `0728IbnTaymiyya.MajmucFatawa (2,993,811 words; 0 units; 0 bios)`
- `0742Mizzi.TahdhibKamal (2,683,671 words; 12,446 units; 0 bios)`
- `0764Safadi.AcyanCasr (604,056 words; 2,408 units; 0 bios)`
- `0764Safadi.WafiBiWafayat (1,968,791 words; 11,211 units; 0 bios)`
- `0774IbnKathir.Bidaya (2,212,102 words; 3,465 units; 0 bios)`
- `0902Sakhawi.DuLamic (1,335,442 words; 14,452 units; 0 bios)`


### `*.completed` (44 titles: 26,448,505 words; 112,555 units; 1 bios)

- `0292Yacqubi.TarikhYacqubi (192,205 words; 139 units; 0 bios)`
- `0379MuhammadRabci.TarikhMawlidCulama (35,125 words; 338 units; 0 bios)`
- `0390Muqaddasi.AhsanTaqasim (103,553 words; 67 units; 0 bios)`
- `0412Sulami.TabaqatSufiya (68,554 words; 193 units; 0 bios)`
- `0430AbuNucaymIsbahani.HilyaAwliya (1,188,081 words; 678 units; 0 bios)`
- `0430AbuNucaymIsbahani.TarikhIsbahan (228,661 words; 1,959 units; 0 bios)`
- `0442Tanukhi.TarikhCulamaNahwiyyin (10,765 words; 95 units; 0 bios)`
- `0446AbuYaclaKhalili.IrshadFiMacrifaCulama (81,543 words; 994 units; 0 bios)`
- `0450Najashi.Rijal (88,987 words; 1,330 units; 0 bios)`
- `0458Bayhaqi.DalailNubuwwa (528,431 words; 678 units; 0 bios)`
- `0460ShaykhTusi.IkhtiyarMacrifaRijal (224,038 words; 416 units; 0 bios)`
- `0460ShaykhTusi.Rijal (75,644 words; 6,745 units; 0 bios)`
- `0463IbnCabdBarr.IsticabFiMacrifaAshab (397,653 words; 4,049 units; 1 bios)`
- `0463KhatibBaghdadi.TarikhBaghdad (1,883,359 words; 8,484 units; 0 bios)`
- `0463KhatibBaghdadi.TarikhBaghdad (2,621,786 words; 13,309 units; 0 bios)`
- `0466CabdAzizKattani.DhaylTarikhMawlidCulama (18,115 words; 463 units; 0 bios)`
- `0476AbuIshaqShirazi.TabaqatFuqaha (30,392 words; 508 units; 0 bios)`
- `0482AbuIshaqHabbal.WafayatMisriyyin (6,616 words; 497 units; 0 bios)`
- `0521IbnAbiYacla.TabaqatHanabila (169,947 words; 880 units; 0 bios)`
- `0524IbnAkfani.DhaylDhaylTarikhMawlidCulama (4,082 words; 84 units; 0 bios)`
- `0544CiyadIbnMusaYahsubi.TartibMadarik (320,968 words; 1,177 units; 0 bios)`
- `0555IbnQalanisi.Tarikh (120,986 words; 157 units; 0 bios)`
- `0565IbnZaydBayhaqi.TarikhBayhaq (121,031 words; 299 units; 0 bios)`
- `0571IbnCasakir.TarikhDimashq (8,193,674 words; 10,910 units; 0 bios)`
- `0577IbnAnbari.NuzhaAlibba (43,678 words; 183 units; 0 bios)`
- `0597IbnJawzi.Muntazam (1,529,901 words; 7,351 units; 0 bios)`
- `0600KatibMarrakushi.Istibsar (60,658 words; 200 units; 0 bios)`
- `0626YaqutHamawi.MucjamBuldan (1,273,690 words; 13,668 units; 0 bios)`
- `0658IbnAbbar.HullaSiyara (98,490 words; 228 units; 0 bios)`
- `0658IbnAbbar.TuhfaQadim (28,899 words; 114 units; 0 bios)`
- `0685IbnCibri.TarikhMukhtasarDuwal (97,240 words; 234 units; 0 bios)`
- `0711IbnManzurIfriqi.MukhtasarTarikhDimashq (2,408,342 words; 7,118 units; 0 bios)`
- `0748Dhahabi.CibarFiKhabar (270,948 words; 868 units; 0 bios)`
- `0748Dhahabi.Culuww (51,237 words; 777 units; 0 bios)`
- `0748Dhahabi.DhaylCibar (37,477 words; 161 units; 0 bios)`
- `0748Dhahabi.DhaylDiwanDucafa (12,664 words; 603 units; 0 bios)`
- `0748Dhahabi.DhikrAsmaManTakallama (9,038 words; 403 units; 0 bios)`
- `0748Dhahabi.DiwanDucafa (105,267 words; 6,009 units; 0 bios)`
- `0748Dhahabi.MucinFiTabaqatMuhaddithin (23,129 words; 2,455 units; 0 bios)`
- `0748Dhahabi.MucjamMuhaddithin (44,241 words; 422 units; 0 bios)`
- `0748Dhahabi.MukhtasarMinDubaythi (96,058 words; 1,641 units; 0 bios)`
- `0852IbnHajarCasqalani.TahdhibTahdhib (1,316,187 words; 13,415 units; 0 bios)`
- `0874IbnTaghribirdi.NujumZahira (1,129,443 words; 1,113 units; 0 bios)`
- `1089IbnCimad.Shadharat (1,097,722 words; 1,143 units; 0 bios)`


### `*.mARkdown` (20 titles: 9,024,824 words; 81,596 units; 56,797 bios)

- `0276IbnQutaybaDinawari.AdabKatib (69,366 words; 299 units; 0 bios)`
- `0355MuhammadKindi.QudatMisr (36,490 words; 101 units; 100 bios)`
- `0355MuhammadKindi.WulatMisr (50,998 words; 132 units; 128 bios)`
- `0369AbuShaykhIsbahani.TabaqatMuhaddithin (110,503 words; 701 units; 683 bios)`
- `0403IbnFaradi.TarikhCulamaAndalus (120,674 words; 1,987 units; 1,659 bios)`
- `0405HakimNaysaburi.TalkhisTarikhNaysabur (35,152 words; 2,519 units; 2,509 bios)`
- `0427HamzaJurjani.TarikhJurjan (107,903 words; 1,356 units; 1,193 bios)`
- `0561Samcani.Ansab (827,145 words; 4,951 units; 0 bios)`
- `0561Samcani.Ansab (879,572 words; 5,063 units; 0 bios)`
- `0578IbnBashkuwal.Sila (140,896 words; 1,725 units; 1,543 bios)`
- `0630IbnAthirCizzDin.LubabFiTahdhibAnsab (343,452 words; 5,169 units; 0 bios)`
- `0658IbnAbbar.TakmilaLiSila (306,871 words; 3,925 units; 3,580 bios)`
- `0681IbnKhallikan.WafayatAcyan (677,511 words; 1,528 units; 862 bios)`
- `0748Dhahabi.TarikhIslam (3,505,304 words; 33,719 units; 31,090 bios)`
- `0771Subki.TabaqatShaficiyaKubra (676,946 words; 1,428 units; 1,412 bios)`
- `0774IbnKathir.TabaqatShaficiyyin (181,807 words; 965 units; 919 bios)`
- `0900AbuCabdAllahHimyari.RawdMictar (323,710 words; 0 units; 0 bios)`
- `0911Suyuti.LubbLubab (51,027 words; 4,853 units; 0 bios)`
- `1339IsmacilBashaBaghdadi.HadiyaCarifin (421,313 words; 8,842 units; 8,814 bios)`
- `1450MawsucaShicriya.MucjamShucara (158,184 words; 2,333 units; 2,305 bios)`




# Text currently included in the Coprus

## List of books by centuries (1329 titles)


* **0100AH [[ [Re]generated on 2016-10-22 (17:14:35) ]]**

 * `0001HarithIbnHilliza.Diwan `
	- *TAGS: _CENT00NO, _SHICR_JAHILI, _SHICR*
 * `0001HatimTai.Diwan `
	- *TAGS: _CENT00NO, _SHICR_JAHILI, _SHICR*
 * `0001ImruQays.Diwan `
	- *TAGS: _CENT00NO, _SHICR_JAHILI, _SHICR*
 * `0001NabighaDhubyani.Diwan `
	- *TAGS: _CENT00NO, _SHICR_JAHILI, _SHICR*
 * `0001TarafaIbnCabd.Diwan `
	- *TAGS: CENT0100, _ADAB, _BALAGHA, _SHICR_JAHILI, _SHICR*
 * `0001TufaylGhanawi.Diwan `
	- *TAGS: _CENT00NO, _SHICR_JAHILI, _SHICR*
 * `0040CaliIbnAbiTalib.NahjBalagha `
	- *TAGS: CENT0100, _HADITH, _SHICI*
 * `0041LabidIbnRabica.Diwan `
	- *TAGS: CENT0100, _ADAB, _BALAGHA, _MUKHADRAM, _SHICR*
 * `0094ZaynCabidin.SahifaSajjadiya `
	- *TAGS: CENT0100, _HADITH, _SHICI*

* **0200AH [[ [Re]generated on 2016-10-22 (17:14:35) ]]**

 * `0104MujahidIbnJabr.Tafsir `
	- *TAGS: CENT0200, _CULUM, _QURAN, _SUNNI, _TAFSIR*
 * `0110HasanBasri.FadailMakka `
	- *TAGS: CENT0200, PPE, _AJZA, _BULDAN, _HADITH, _TABAQAT, _TARAJIM, _TARIKH*
 * `0110IbnSirin.MuntakhabKalamFiTafsirAhlam `
	- *TAGS: CENT0100, CENT0200, _AHLAM, _CHRONOMULTIPLE, _MISC, _TAFSIR*
 * `0117IbnDicamaSadusi.NasikhWaMansukh `
	- *TAGS: CENT0200, _CULUM, _MANSUKH, _NASIKH, _QURAN, _TAFSIR*
 * `0117IbnDicamaSadusi.NasikhWaMansukh `
	- *TAGS: CENT0200, _CULUM, _QURAN, _SUNNI, _TAFSIR*
 * `0122ZaydIbnCali.MusnadZayd `
	- *TAGS: CENT0200, _FIQH, _SHICI, _ZAYDI*
 * `0128IbnAbiHabibMisri.AhadithYazid `
	- *TAGS: CENT0200, _AJZA, _HADITH*
 * `0132HammamIbnMunabbih.Sahifa `
	- *TAGS: CENT0200, _AJZA, _HADITH, _TARAJIM*
 * `0132HammamIbnMunabbih.Sahifa `
	- *TAGS: CENT0200, _HADITH, _SUNNI*
 * `0150AbuHanifa.Musnad `
	- *TAGS: CENT0200, _HADITH*
 * `0150MuqatilIbnSulayman.TafsirMuqatil `
	- *TAGS: CENT0200, _CULUM, _QURAN, _SUNNI, _TAFSIR*
 * `0156IbnAbiCuruba.Manasik `
	- *TAGS: CENT0200, _AJZA, _BUHUTH, _HADITH, _MASAIL, _TARAJIM*
 * `0161SufyanThawri.Tafsir `
	- *TAGS: CENT0200, _CULUM, _HADITH, _QURAN, _SUNNI, _TAFSIR*
 * `0164MajishunMadani.Hajj `
	- *TAGS: CENT0200, _AJZA, _HADITH*
 * `0168IbnTahman.Mashyakha `
	- *TAGS: CENT0200, _AJZA, _HADITH, _TARAJIM*
 * `0168MufaddalDabbi.AmthalCarab `
	- *TAGS: CENT0200, _ADAB, _ADAB, _AMTHAL, _BALAGHA*
 * `0168MufaddalDabbi.AmthalCarab `
	- *TAGS: _ADAB, _BALAGHA, _CENT00NO*
 * `0168MufaddalDabbi.Mufaddaliyat `
	- *TAGS: CENT0200, _ADAB, _ADAB, _BALAGHA, _SHICR*
 * `0170AbuZaydQurashi.JamharaAshcarCarab `
	- *TAGS: CENT0200, _ADAB, _ADAB, _BALAGHA, _SHICR*
 * `0170KhalilFarahidi.Cayn `
	- *TAGS: CENT0200, _FIQH, _GHARIB, _LUGHA, _MACAJIM, _MUSTALAHAT, _NAHW, _SARF*
 * `0170KhalilFarahidi.JumalFiNahw `
	- *TAGS: CENT0200, _MAJMUCAT, _NAHW, _SARF*
 * `0175LaythIbnSacd.MajlisMinFawaid `
	- *TAGS: CENT0200, _AJZA, _FAWAID, _HADITH, _MISC, _TARAJIM*
 * `0179MalikIbnAnas.MudawwanaKubra `
	- *TAGS: CENT0200, _FIQH, _HADITH, _MALIKI*
 * `0179MalikIbnAnas.Muwatta `
	- *TAGS: CENT0200, _FIQH, _HADITH, _MALIKI, _TARAJIM*
 * `0180IbnJacfarAnsari.HadithIsmacil `
	- *TAGS: CENT0200, _AJZA, _HADITH, _TARAJIM*
 * `0180Sibawayh.KitabSibawayh `
	- *TAGS: CENT0200, _MAJMUCAT, _NAHW, _SARF*
 * `0181IbnMubarak.Jihad `
	- *TAGS: CENT0200, _AJZA, _FIQH, _HADITH, _MASAIL, _SUNNI, _TARAJIM, _USUL*
 * `0181IbnMubarak.Musnad `
	- *TAGS: CENT0200, _AJZA, _HADITH, _MACAJIM, _MASANID, _TARAJIM*
 * `0181IbnMubarak.Zuhd `
	- *TAGS: CENT0200, _AJZA, _AKHLAQ, _HADITH*
 * `0182AbuYusufYacqub.Athar `
	- *TAGS: CENT0200, _FIQH, _HADITH, _HANAFI*
 * `0182AbuYusufYacqub.IkhtilafAbiHanifa `
	- *TAGS: CENT0200, _FIQH, _HANAFI*
 * `0182AbuYusufYacqub.Kharaj `
	- *TAGS: CENT0200, _BUHUTH, _MASAIL*
 * `0182AbuYusufYacqub.RaddCalaSiyarAwzaci `
	- *TAGS: CENT0200, _BUHUTH, _FIQH, _HANAFI, _MASAIL, _SIYASA, _USUL*
 * `0188IbnMuhammadFazari.Siyar `
	- *TAGS: CENT0200, _SHAMAIL, _SIRA*
 * `0189MuhammadShaybani.Asl `
	- *TAGS: CENT0200, _FIQH, _HADITH, _HANAFI*
 * `0189MuhammadShaybani.Athar `
	- *TAGS: CENT0200, _FIQH, _HADITH, _HANAFI*
 * `0189MuhammadShaybani.HujjaCalaAhlMadina `
	- *TAGS: CENT0200, _FIQH, _HADITH, _HANAFI*
 * `0189MuhammadShaybani.JamicSaghir `
	- *TAGS: CENT0200, _FIQH, _HADITH, _HANAFI*
 * `0189MuhammadShaybani.Kasb `
	- *TAGS: CENT0200, _FIQH, _HANAFI*
 * `0189MuhammadShaybani.Siyar `
	- *TAGS: CENT0200, _FIQH, _HANAFI, _SIYASA*
 * `0191IbnQasimMisri.MajalisIbnQasim `
	- *TAGS: CENT0200, _FIQH, _MALIKI*
 * `0195IbnCamrSadusi.Amthal `
	- *TAGS: CENT0200, _ADAB, _AMTHAL, _BALAGHA*
 * `0195IbnFudaylDabbi.Duca `
	- *TAGS: CENT0200, _AJZA, _AKHLAQ, _HADITH*
 * `0195MuarrijSadusi.HadhfMinNasabQuraysh `
	- *TAGS: CENT0200, GEN, PPE, _ANSAB, _BULDAN, _TARIKH*
 * `0197IbnWahbQurashi.JamicFiHadith `
	- *TAGS: CENT0200, _HADITH, _SUNAN, _TARAJIM*
 * `0197IbnWahbQurashi.MuharabaMinMuwattaIbnWahb `
	- *TAGS: CENT0200, _AJZA, _HADITH*
 * `0197IbnWahbQurashi.MuwattaIbnWahb.Qitca `
	- *TAGS: CENT0200, _AJZA, _HADITH*
 * `0197IbnWahbQurashi.QadaMinMuwattaIbnWahb `
	- *TAGS: CENT0200, _AJZA, _HADITH*
 * `0197IbnWahbQurashi.Qadar `
	- *TAGS: CENT0200, _AJZA, _CAQAID, _HADITH, _MILAL*
 * `0197WakicIbnJarrah.NuskhaWakic `
	- *TAGS: CENT0200, _AJZA, _HADITH, _SUNNI, _TARAJIM*
 * `0198SufyanIbnCuyayna.JuzFihiHadith `
	- *TAGS: CENT0200, _AJZA, _HADITH, _TARAJIM*
 * `0198SufyanIbnCuyayna.JuzHadith `
	- *TAGS: CENT0200, _AJZA, _HADITH, _SUNNI*
 * `0200AbuShis.Diwan `
	- *TAGS: CENT0200, _SHICR_CABBASI, _SHICR*
 * `0200IbnCumarDabbi.Fitna `
	- *TAGS: CENT0200, PPE, _HADITH, _SUNNI, _TARIKH*

* **0300AH [[ [Re]generated on 2016-10-22 (17:14:35) ]]**

 * `0203IbnSulaymanGhazi.MusnadRida `
	- *TAGS: CENT0300, _HADITH, _SHICI*
 * `0203YahyaIbnAdam.Kharaj `
	- *TAGS: CENT0300, _AJZA, _FIQH, _HADITH, _MASAIL, _USUL*
 * `0204AbuDawudTayalisi.Musnad `
	- *TAGS: CENT0300, _HADITH, _MACAJIM, _MASANID, _SUNNI, _TARAJIM*
 * `0204HishamKalbi.Asnam `
	- *TAGS: CENT0300, _CAQAID, _MILAL*
 * `0204IbnKalbi.AnsabKhayl `
	- *TAGS: CENT0300, GEN, PPE, _ADAB, _BALAGHA, _GHARIB, _MACAJIM, _MUSTALAHAT*
 * `0204IbnKalbi.JamharaAnsab `
	- *TAGS: CENT0300, GEN, PPE, _ANSAB, _BULDAN, _TARIKH*
 * `0204IbnKalbi.NasabMacad `
	- *TAGS: CENT0300, GEN, PPE, _ANSAB, _BULDAN, _TARIKH*
 * `0204Shafici.AhkamQuran `
	- *TAGS: CENT0300, _AHKAM, _CULUM, _GHARIB, _HADITH, _QURAN, _SUNNI, _TAFSIR*
 * `0204Shafici.IkhtilafHadith `
	- *TAGS: CENT0300, _AHKAM, _CILAL, _FIQH, _HADITH, _MASAIL, _MUSHKIL, _SHARH, _SUNNI, _TARAJIM, _USUL*
 * `0204Shafici.JimacCilm `
	- *TAGS: CENT0300, _FIQH, _QAWACID, _SHAFICI, _USUL*
 * `0204Shafici.Musnad `
	- *TAGS: CENT0300, _FIQH, _HADITH, _SHAFICI, _SUNAN, _SUNNI, _TARAJIM*
 * `0204Shafici.Risala `
	- *TAGS: CENT0300, _FIQH, _QAWACID, _SHAFICI, _USUL*
 * `0204Shafici.Umm `
	- *TAGS: CENT0300, _FIQH, _HADITH, _SHAFICI*
 * `0206AbuMuhammadQutrub.Azmina `
	- *TAGS: CENT0300, _FIQH, _GHARIB, _MACAJIM, _MASAIL, _MUSTALAHAT*
 * `0206IbnMirarShaybani.Jim `
	- *TAGS: CENT0300, _FIQH, _GHARIB, _MACAJIM, _MUSTALAHAT*
 * `0207IbnZiyadFarra.MacaniQuran `
	- *TAGS: CENT0300, _CULUM, _QURAN*
 * `0207Waqidi.FutuhSham `
	- *TAGS: CENT0300, PPE, _BULDAN, _TARIKH*
 * `0207Waqidi.Maghazi `
	- *TAGS: CENT0300, PPE, _ASHAB, _SHAMAIL, _SIRA*
 * `0207Waqidi.Ridda `
	- *TAGS: CENT0300, PPE, _TARIKH*
 * `0209AbuCaliAshyabBaghdadi.JuzAshyab `
	- *TAGS: CENT0300, _AJZA, _HADITH, _TARAJIM*
 * `0209IbnMuthannaTaymi.Dibaj `
	- *TAGS: CENT0300, PPE, _GHARIB, _MACAJIM, _MUSTALAHAT, _TARIKH*
 * `0209MacmarIbnMuthanna.Khayl `
	- *TAGS: CENT0300, PPE, _ADAB, _BALAGHA, _GHARIB, _MACAJIM, _MUSTALAHAT*
 * `0211AbuCatahiya.Diwan `
	- *TAGS: CENT0300, _SHICR_CABBASI, _SHICR*
 * `0211CabdRazzakSancani.AmaliFiAthar `
	- *TAGS: CENT0300, _AJZA, _AMALI, _HADITH, _MAJALIS, _TARAJIM*
 * `0211CabdRazzakSancani.Musannaf `
	- *TAGS: CENT0300, _FIQH, _HADITH, _SUNNI, _TARAJIM*
 * `0211CabdRazzakSancani.Tafsir `
	- *TAGS: CENT0300, _CULUM, _HADITH, _QURAN, _SUNNI, _TAFSIR*
 * `0213IbnHisham.SiraNabawiyya `
	- *TAGS: BIO, CENT0300, DHB, PPE, _ASHAB, _IMAM, _NABI, _SHAMAIL, _SIRA*
 * `0213IbnHisham.Tijan `
	- *TAGS: CENT0300, PPE, _TARIKH*
 * `0214IbnCabdHakamMisri.SiraCumarIbnCabdCaziz `
	- *TAGS: CENT0300, PPE, _TABAQAT, _TARAJIM, _TARIKH*
 * `0215AkhfashAwsat.Qawafi `
	- *TAGS: CENT0300, _ADAB, _BALAGHA, _FASAHA*
 * `0216IbnQuraybAsmaci.Asmaciyat `
	- *TAGS: CENT0300, _ADAB, _ADAB, _BALAGHA, _SHICR*
 * `0216IbnQuraybAsmaci.Sha `
	- *TAGS: CENT0300, _FIQH, _GHARIB, _MACAJIM, _MUSTALAHAT*
 * `0219AbuNucaymIbnDykayn.Salat `
	- *TAGS: CENT0300, _AJZA, _HADITH, _TARAJIM*
 * `0219IbnZubayrHumaydi.Musnad `
	- *TAGS: CENT0300, _HADITH, _MACAJIM, _MASANID, _SUNNI, _TARAJIM*
 * `0222IbnBakkarDabi.AkhbarWafidat `
	- *TAGS: CENT0300, _TABAQAT, _TARAJIM, _TARIKH*
 * `0222IbnBakkarDabi.AkhbarWafidin `
	- *TAGS: CENT0300, _TABAQAT, _TARAJIM, _TARIKH*
 * `0224AbuCubaydIbnSallam.Amwal `
	- *TAGS: CENT0300, _BUHUTH, _FIQH, _MASAIL, _USUL*
 * `0224AbuCubaydIbnSallam.GharibHadith `
	- *TAGS: CENT0300, _FIQH, _GHARIB, _HADITH, _LUGHA, _MACAJIM, _MUSTALAHAT, _NAHW, _SARF*
 * `0224AbuCubaydIbnSallam.NasikhWaMansukh `
	- *TAGS: CENT0300, _CULUM, _QURAN*
 * `0224IbnSallamBaghdadi.Amthal `
	- *TAGS: CENT0300, _ADAB, _ADAB, _AMTHAL, _BALAGHA*
 * `0227IbnMansurKhurasani.Sunan `
	- *TAGS: CENT0300, _FIQH, _HADITH, _SUNAN, _TARAJIM*
 * `0227IbnMansurKhurasani.Sunan `
	- *TAGS: CENT0300, _HADITH, _SUNAN, _TARAJIM*
 * `0227IbnMansurKhurasani.TafsirMinSunanSacid `
	- *TAGS: CENT0300, _HADITH*
 * `0228IbnHammadKhuzaci.Fitan `
	- *TAGS: CENT0300, _AJZA, _CAQAID, _HADITH, _MILAL, _TARIKH*
 * `0230CaliIbnJacd.Musnad `
	- *TAGS: CENT0300, _HADITH, _MACAJIM, _MASANID, _SUNNI, _TARAJIM*
 * `0230IbnSacd.TabaqatKubra `
	- *TAGS: BIO, CENT0300, COL, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0231IbnSallamJumahi.TabaqatFuhulShucara `
	- *TAGS: CENT0300, PPE, _ADAB, _TABAQAT, _TARAJIM, _TARIKH*
 * `0231IbnZiyadAcrabi.AsmaKhayl `
	- *TAGS: CENT0300, _ADAB, _BALAGHA, _GHARIB, _MACAJIM, _MUSTALAHAT*
 * `0233YahyaIbnMacin.HadithYahya `
	- *TAGS: CENT0300, _AJZA, _FAWAID, _HADITH, _MISC, _TARAJIM*
 * `0233YahyaIbnMacin.MacrifaRijal `
	- *TAGS: CENT0300, PPE, _TABAQAT, _TARAJIM*
 * `0233YahyaIbnMacin.MinKalamFiRijal `
	- *TAGS: CENT0300, PPE, _CILAL, _HADITH, _SUALAT, _TARAJIM*
 * `0233YahyaIbnMacin.TarikhIbnMacin `
	- *TAGS: CENT0300, PPE, _HADITH, _SUALAT, _SUNNI, _TABAQAT, _TARAJIM*
 * `0234AbuHasanSacdi.TasmiyaManRuwiya `
	- *TAGS: CENT0300, PPE, _HADITH, _MISC, _TABAQAT, _TARAJIM*
 * `0234AbuKhaythamaNisai.Cilm `
	- *TAGS: CENT0300, _AJZA, _AKHLAQ, _FIQH, _HADITH, _MASAIL, _SUNNI, _USUL*
 * `0234CaliIbnMadini.Cilal `
	- *TAGS: CENT0300, _AHKAM, _CILAL, _DACIF, _HADITH, _MAWDUC, _SUALAT*
 * `0234CaliIbnMadini.SualatIbnAbiShayba `
	- *TAGS: CENT0300, _CILAL, _HADITH, _SUALAT, _TARAJIM*
 * `0234CaliIbnMadini.SualatIbnAbiShayba `
	- *TAGS: CENT0300, _HADITH, _SUNNI*
 * `0234IbnAbiShayba.Adab `
	- *TAGS: CENT0300, _AJZA, _HADITH, _TARAJIM*
 * `0234IbnAbiShayba.Musnad `
	- *TAGS: CENT0300, _HADITH, _MACAJIM, _MASANID, _TARAJIM*
 * `0236AbuCabdAllahZubayri.NasabQuraysh `
	- *TAGS: CENT0300, _ANSAB, _TARAJIM, _TARIKH*
 * `0238IbnHabibQurtubi.AdabNisa `
	- *TAGS: CENT0300, _AJZA, _HADITH*
 * `0238IbnHabibQurtubi.AshratSaca `
	- *TAGS: CENT0300, _AJZA, _HADITH*
 * `0238IbnHabibQurtubi.MukhtasarFiTibb `
	- *TAGS: CENT0300, _CULUM, _MISC, _TIBB*
 * `0238IbnRahawayh.Musnad `
	- *TAGS: CENT0300, _HADITH, _MACAJIM, _MASANID, _SUNNI, _TARAJIM*
 * `0238MuhammadBarjlani.KaramWaJawd `
	- *TAGS: CENT0300, _AJZA, _AKHLAQ, _HADITH*
 * `0238MuhammadBarjlani.KaramWaJawd `
	- *TAGS: CENT0300, _HADITH, _SUNNI*
 * `0240KhalifaIbnKhayyat.Tabaqat `
	- *TAGS: CENT0300, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0240KhalifaIbnKhayyat.Tarikh `
	- *TAGS: CENT0300, PPE, _HADITH, _SUNNI, _TARAJIM, _TARIKH*
 * `0241IbnHanbal.AsamiWaKuna `
	- *TAGS: CENT0300, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0241IbnHanbal.Ashriba `
	- *TAGS: CENT0300, _AJZA, _BUHUTH, _FIQH, _HANBALI, _MASAIL*
 * `0241IbnHanbal.CaqidaRiwayaKhallal `
	- *TAGS: CENT0300, _CAQAID, _HADITH, _MILAL*
 * `0241IbnHanbal.CilalWaMacrifa `
	- *TAGS: CENT0300, PPE, _AHKAM, _CILAL, _DACIF, _HADITH, _MAWDUC, _SUALAT, _SUNNI, _TARAJIM*
 * `0241IbnHanbal.FadailSahaba `
	- *TAGS: CENT0300, PPE, _ASHAB, _HADITH, _SIRA, _TABAQAT, _TARAJIM*
 * `0241IbnHanbal.MasailRiwayaIbnih `
	- *TAGS: CENT0300, _FIQH, _HANBALI*
 * `0241IbnHanbal.MasailRiwayaSalih `
	- *TAGS: CENT0300, _FIQH, _HANBALI*
 * `0241IbnHanbal.MinSualatIbnMuhammadAthram `
	- *TAGS: CENT0300, _CILAL, _SUALAT*
 * `0241IbnHanbal.Musnad `
	- *TAGS: CENT0300, _FIQH, _HADITH, _MACAJIM, _MASANID, _SUNNI, _TARAJIM*
 * `0241IbnHanbal.RaddCalaZanadiqa `
	- *TAGS: CENT0300, _AJZA, _CAQAID, _HADITH, _MILAL, _RUDUD*
 * `0241IbnHanbal.RaddCalaZanadiqa `
	- *TAGS: CENT0300, _CAQAID*
 * `0241IbnHanbal.SualatAbiDawudLiIbnHanbal `
	- *TAGS: CENT0300, _CILAL, _HADITH, _SUALAT, _TARAJIM*
 * `0241IbnHanbal.UsulSunna `
	- *TAGS: CENT0300, _AJZA, _CAQAID, _HADITH, _MILAL*
 * `0241IbnHanbal.Warac `
	- *TAGS: CENT0300, _AJZA, _AKHLAQ, _HADITH*
 * `0241IbnHanbal.Zuhd `
	- *TAGS: CENT0300, _AJZA, _AKHLAQ, _HADITH*
 * `0243HannadIbnSari.Zuhd `
	- *TAGS: CENT0300, _ADAB, _ADHKAR, _AJZA, _AKHLAQ, _HADITH, _RAQAIQ*
 * `0243HarithMuhasibi.AdabNufus `
	- *TAGS: CENT0300, _ADAB, _ADHKAR, _AKHLAQ, _MISC, _RAQAIQ, _SULUK*
 * `0243HarithMuhasibi.FahmQuran `
	- *TAGS: CENT0300, _CULUM, _QURAN, _TAFSIR*
 * `0243HarithMuhasibi.MahiyaCaql `
	- *TAGS: CENT0300, _CAQAID, _MILAL*
 * `0243HarithMuhasibi.Makasib `
	- *TAGS: CENT0300, _AJZA, _BUHUTH, _FIQH, _MASAIL*
 * `0243HarithMuhasibi.RisalaMustarshidin `
	- *TAGS: CENT0300, _ADAB, _ADHKAR, _AKHLAQ, _MISC, _RAQAIQ, _SULUK*
 * `0243IbnYahyaCadani.Iman `
	- *TAGS: CENT0300, _AJZA, _CAQAID, _HADITH, _MILAL, _SUNNI*
 * `0244IbnSikkit.KanzLughawi `
	- *TAGS: CENT0300, _FIQH, _GHARIB, _LUGHA, _MACAJIM, _MASAIL, _MUSTALAHAT, _NAHW, _SARF*
 * `0244IbnSikkit.QalbWaIbdal `
	- *TAGS: CENT0300, _LUGHA*
 * `0245DhuNunMisri.Hadith `
	- *TAGS: CENT0300, _HADITH, _MAKHTUTAT*
 * `0245LuwaynMissisi.JuzHadith `
	- *TAGS: CENT0300, _AJZA, _HADITH, _TARAJIM*
 * `0245MuhammadIbnHabib.Muhabbar `
	- *TAGS: CENT0300, _ADAB, _BALAGHA, _FASAHA, _TARIKH*
 * `0245MuhammadIbnHabib.MukhtalafQabail `
	- *TAGS: CENT0300, GEN, PPE, _ANSAB, _BULDAN, _TARIKH*
 * `0245MuhammadIbnHabib.MunammaqFiAkhbarQuraysh `
	- *TAGS: CENT0300, _BULDAN, _TARIKH*
 * `0246AhmadDawraqi.MusnadSacdIbnAbiWaqqas `
	- *TAGS: CENT0300, _AJZA, _HADITH, _MACAJIM, _MASANID, _SUNNI, _TARAJIM*
 * `0246DicbilKhuzaci.WasayaMuluk `
	- *TAGS: CENT0300, _ADAB, _BALAGHA, _SIYASA*
 * `0246HishamSulami.HadithHisham `
	- *TAGS: CENT0300, _AJZA, _HADITH, _MISC, _TARAJIM*
 * `0246HusaynMarwazi.BirrWaSila `
	- *TAGS: CENT0300, _AJZA, _AKHLAQ, _HADITH*
 * `0246IbnCumarDuri.JuzFihiQiraat `
	- *TAGS: CENT0300, _AJZA, _CULUM, _HADITH, _QIRAAT, _QURAN, _TAFSIR*
 * `0248AbuHatimSijistani.Farq `
	- *TAGS: CENT0300, _FIQH, _GHARIB, _MACAJIM, _MASAIL, _MUSTALAHAT*
 * `0248AbuHatimSijistani.FuhulaShucara `
	- *TAGS: CENT0300, _TARAJIM, _TARIKH*
 * `0248AbuHatimSijistani.Mucammarun `
	- *TAGS: CENT0300, _ADAB, _AKHLAQ, _BALAGHA, _MISC, _SULUK*
 * `0249Azraqi.AkhbarMakka `
	- *TAGS: CENT0300, PPE, _BULDAN, _HADITH, _TABAQAT, _TARAJIM, _TARIKH*
 * `0249CabdIbnHamid.MuntakhabMinMusnad `
	- *TAGS: CENT0300, _HADITH, _MACAJIM, _MASANID, _SUNNI, _TARAJIM*
 * `0251IbnMansurKawsaj.Masail `
	- *TAGS: CENT0300, _FIQH, _HANBALI*
 * `0251IbnZanjawayh.Amwal `
	- *TAGS: CENT0300, _FIQH, _HADITH, _MASAIL*
 * `0254MuammalIbnIhab.JuzMuammal `
	- *TAGS: CENT0300, _AJZA, _HADITH, _SUNNI, _TARAJIM*
 * `0255CabdAllahDarimi.Sunan `
	- *TAGS: CENT0300, _FIQH, _HADITH, _SUNAN, _SUNNI, _TARAJIM*
 * `0255IbnAhmadQurtubi.Hajj `
	- *TAGS: CENT0300, _AJZA, _HADITH*
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
 * `0256Bukhari.AdabMufrad `
	- *TAGS: CENT0300, _AJZA, _AKHLAQ, _HADITH, _SUNNI*
 * `0256Bukhari.Ducafa `
	- *TAGS: CENT0300, PPE, _TABAQAT, _TARAJIM*
 * `0256Bukhari.DucafaSaghir `
	- *TAGS: BIO, CENT0300, HAD, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0256Bukhari.KhalqAfcal `
	- *TAGS: CENT0300, _AJZA, _CAQAID, _HADITH, _MILAL, _SUNNI*
 * `0256Bukhari.QiraaKhalfaImam `
	- *TAGS: CENT0300, _FIQH, _HADITH, _MASAIL*
 * `0256Bukhari.QuraCaynanyn `
	- *TAGS: CENT0300, _AJZA, _FIQH, _HADITH, _MASAIL, _USUL*
 * `0256Bukhari.Sahih `
	- *TAGS: CENT0300, _FIQH, _HADITH, _SAHIH, _SUNNI, _TARAJIM*
 * `0256Bukhari.SharhKitabFitan `
	- *TAGS: CENT0300, _HADITH, _SHARH*
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
 * `0257IbnCurfaCabdi.AhadithCawali `
	- *TAGS: CENT0300, CENT0800, _AJZA, _CHRONOMULTIPLE, _HADITH, _TARAJIM*
 * `0258IbnYahyaNaysaburi.Juz `
	- *TAGS: CENT0300, _HADITH, _MAKHTUTAT*
 * `0259IbnYacqubJuzjani.AhwalRijal `
	- *TAGS: CENT0300, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0260IbnSahlTabari.FirdawsHikmaFiTibb `
	- *TAGS: CENT0300, _TIBB*
 * `0261AbuHasanCijli.MacrifaThiqat `
	- *TAGS: CENT0300, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM, _THIQAT*
 * `0261Muslim.KunaWaAsma `
	- *TAGS: CENT0300, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0261Muslim.Munfaridat `
	- *TAGS: CENT0300, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0261Muslim.Sahih `
	- *TAGS: CENT0300, _FIQH, _HADITH, _SAHIH, _SUNNI, _TARAJIM*
 * `0261Muslim.SharhKitabHajj `
	- *TAGS: CENT0300, _HADITH, _SHARH*
 * `0261Muslim.Tamyiz `
	- *TAGS: CENT0300, _AHKAM, _CILAL, _DACIF, _HADITH, _MAWDUC, _SUALAT*
 * `0262AbuZaydNumayri.TarikhMadina `
	- *TAGS: CENT0300, PPE, _BULDAN, _HADITH, _TABAQAT, _TARAJIM, _TARIKH*
 * `0262IbnCasimIsbahani.Juz `
	- *TAGS: CENT0300, _AJZA, _HADITH, _TARAJIM*
 * `0262YacqubIbnShayba.MusnadCumarIbnKhattab `
	- *TAGS: CENT0300, _AJZA, _HADITH, _MACAJIM, _MASANID, _TARAJIM*
 * `0264AbyZurca.Ducafa `
	- *TAGS: CENT0300, _HADITH, _SUALAT, _TARAJIM*
 * `0264IbnYahyaMuzani.Mukhtasar `
	- *TAGS: CENT0300, _FIQH, _SHAFICI*
 * `0264IbnYahyaMuzani.SharhSunna `
	- *TAGS: CENT0300, _CAQAID, _MILAL*
 * `0265IbnHarbMawsili.HadithSyfyanIbnCuyayna `
	- *TAGS: CENT0300, _HADITH, _MAKHTUTAT*
 * `0265SalihIbnHanbal.SiraImam `
	- *TAGS: CENT0300, _TABAQAT, _TARAJIM, _TARIKH*
 * `0270IbnCaffanKufi.AmaliWaQiraa `
	- *TAGS: CENT0300, _AJZA, _AMALI, _HADITH, _MAJALIS, _TARAJIM*
 * `0272Fakihi.AkhbarMakka `
	- *TAGS: CENT0300, PPE, _BULDAN, _HADITH, _TABAQAT, _TARAJIM, _TARIKH*
 * `0272IbnCassamIsbahani.JuzIbnCassam `
	- *TAGS: CENT0300, _AJZA, _HADITH, _TARAJIM*
 * `0272IbnIshaqFakihi.HadithFakihi `
	- *TAGS: CENT0300, _AJZA, _HADITH, _TARAJIM*
 * `0273AbuUmayyaTarsusi.MusnadCabdAllahIbnCumar `
	- *TAGS: CENT0300, _AJZA, _HADITH, _MACAJIM, _MASANID, _TARAJIM*
 * `0273IbnMaja.SharhMuqaddimaSunan `
	- *TAGS: CENT0300, _HADITH, _SHARH*
 * `0273IbnMaja.Sunan `
	- *TAGS: CENT0300, _FIQH, _HADITH, _SUNAN, _SUNNI, _TARAJIM*
 * `0274AhmadBarqi.Mahasin `
	- *TAGS: CENT0300, _HADITH, _SHICI*
 * `0275AbuDawud.Zuhd `
	- *TAGS: CENT0300, _AKHLAQ, _HADITH*
 * `0275AbuDawudSijistani.Marasil `
	- *TAGS: CENT0300, _AHKAM, _CILAL, _DACIF, _HADITH, _MAWDUC*
 * `0275AbuDawudSijistani.RisalaIlaAhlMakka `
	- *TAGS: CENT0300, _CULUM, _HADITH, _MISC, _MUSTALAHAT, _SUNNI*
 * `0275AbuDawudSijistani.Sunan `
	- *TAGS: CENT0300, _FIQH, _HADITH, _SUNAN, _SUNNI, _TARAJIM*
 * `0276IbnMukhalladQurtubi.MaRuwiyaFiHawd `
	- *TAGS: CENT0300, _AJZA, _CAQAID, _HADITH, _MILAL*
 * `0276IbnQutaybaDinawari.AdabKatib `
	- *TAGS: CENT0300, SBS, _ADAB, _ADAB, _BALAGHA, _CARUD, _KITABA*
 * `0276IbnQutaybaDinawari.AnwaFiMawasim `
	- *TAGS: CENT0300, _MISC*
 * `0276IbnQutaybaDinawari.AshribaWaIkhtilafFiha `
	- *TAGS: CENT0300, _BUHUTH, _FIQH, _MASAIL*
 * `0276IbnQutaybaDinawari.CuyunAkhbar `
	- *TAGS: CENT0300, _ADAB, _ADAB, _BALAGHA, _QISAS, _TARAIF*
 * `0276IbnQutaybaDinawari.GharibHadith `
	- *TAGS: CENT0300, _FIQH, _GHARIB, _HADITH, _LUGHA, _MACAJIM, _MUSTALAHAT, _NAHW, _SARF*
 * `0276IbnQutaybaDinawari.GharibQuran `
	- *TAGS: CENT0300, _CULUM, _QURAN*
 * `0276IbnQutaybaDinawari.IkhtilafFiLafz `
	- *TAGS: CENT0300, _AJZA, _HADITH*
 * `0276IbnQutaybaDinawari.ImamaWaSiyasa `
	- *TAGS: CENT0300, _IMAM, _NABI, _SIRA, _SIYASA*
 * `0276IbnQutaybaDinawari.Jarathim `
	- *TAGS: CENT0300, _FIQH, _GHARIB, _MACAJIM, _MUSTALAHAT*
 * `0276IbnQutaybaDinawari.MacaniKabir `
	- *TAGS: CENT0300, _ADAB, _BALAGHA, _GHARIB, _MACAJIM, _MASAIL, _MUSTALAHAT*
 * `0276IbnQutaybaDinawari.Macarif `
	- *TAGS: CENT0300, PPE, _ANSAB, _MACAJIM, _TARIKH*
 * `0276IbnQutaybaDinawari.RisalaKhatt `
	- *TAGS: CENT0300, _GHARIB, _MACAJIM, _MUSTALAHAT*
 * `0276IbnQutaybaDinawari.ShicrWaShucara `
	- *TAGS: CENT0300, _ADAB, _ADAB, _BALAGHA, _SHICR*
 * `0276IbnQutaybaDinawari.TawilMukhtalafHadith `
	- *TAGS: CENT0300, _HADITH, _MISC, _MUSTALAHAT, _SHARH, _SUNNI*
 * `0276IbnQutaybaDinawari.TawilMushkilQuran `
	- *TAGS: CENT0300, _CULUM, _QURAN*
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
 * `0279Tirmidhi.CilalSaghir `
	- *TAGS: CENT0300, PPE, _AHKAM, _CILAL, _HADITH, _MUSHKIL, _SUALAT, _SUNNI, _TARAJIM*
 * `0279Tirmidhi.JamicSahih `
	- *TAGS: CENT0300, CENT1500, _ALBANI, _CHRONOMULTIPLE, _FIQH, _HADITH, _SUNAN, _SUNNI, _TARAJIM*
 * `0279Tirmidhi.ShamailMuhammadiya `
	- *TAGS: CENT0300, _AJZA, _ASHAB, _HADITH, _SHAMAIL, _SIRA, _SUNNI*
 * `0280CuthmanIbnSacidDarimi.NaqdImam `
	- *TAGS: CENT0300, _CAQAID*
 * `0280IbnIsmacilKirmani.MasailHarb `
	- *TAGS: CENT0300, _BUHUTH, _MASAIL*
 * `0280IbnTayfur.Baghdad `
	- *TAGS: CENT0300, PPE, _BULDAN, _HADITH, _TABAQAT, _TARAJIM*
 * `0280IbnTayfur.BallaghatNisa `
	- *TAGS: CENT0300, CENT0400, _ADAB, _ADAB, _BALAGHA, _CHRONOMULTIPLE, _FASAHA, _TARIKH*
 * `0281AbuZurcaDimashqi.FawaidMucallala `
	- *TAGS: CENT0300, _CILAL, _SUALAT*
 * `0281AbuZurcaDimashqi.Tarikh `
	- *TAGS: CENT0300, PPE, _HADITH, _TARAJIM, _TARIKH*
 * `0281IbnAbiDunya.Ahwal `
	- *TAGS: CENT0300, _CAQAID, _IBNABIDUNYA, _MILAL*
 * `0281IbnAbiDunya.AmrBiMacruf `
	- *TAGS: CENT0300, _AKHLAQ, _IBNABIDUNYA*
 * `0281IbnAbiDunya.Awliya `
	- *TAGS: CENT0300, _AKHLAQ, _IBNABIDUNYA*
 * `0281IbnAbiDunya.CaqlWaFadluh `
	- *TAGS: CENT0300, _AKHLAQ, _HADITH, _IBNABIDUNYA, _SUNNI*
 * `0281IbnAbiDunya.Ciyal `
	- *TAGS: CENT0300, _AKHLAQ, _IBNABIDUNYA*
 * `0281IbnAbiDunya.CumrWaShayb `
	- *TAGS: CENT0300, _AKHLAQ, _IBNABIDUNYA*
 * `0281IbnAbiDunya.Cuzla `
	- *TAGS: CENT0300, _AKHLAQ, _IBNABIDUNYA*
 * `0281IbnAbiDunya.DhammBaghy `
	- *TAGS: CENT0300, _AKHLAQ, _IBNABIDUNYA*
 * `0281IbnAbiDunya.DhammGhiba `
	- *TAGS: CENT0300, _AKHLAQ, _IBNABIDUNYA*
 * `0281IbnAbiDunya.DhammMuskir `
	- *TAGS: CENT0300, _AKHLAQ, _FIQH, _IBNABIDUNYA, _MASAIL, _USUL*
 * `0281IbnAbiDunya.FadailRamadan `
	- *TAGS: CENT0300, _AJZA, _HADITH, _IBNABIDUNYA, _TARAJIM*
 * `0281IbnAbiDunya.FarajBacdaShidda `
	- *TAGS: CENT0300, _AKHLAQ, _IBNABIDUNYA*
 * `0281IbnAbiDunya.HammWaHuzn `
	- *TAGS: CENT0300, _AKHLAQ, _HADITH, _IBNABIDUNYA, _SUNNI*
 * `0281IbnAbiDunya.Hawatif `
	- *TAGS: CENT0300, _AKHLAQ, _CAQAID, _HADITH, _IBNABIDUNYA, _SUNNI*
 * `0281IbnAbiDunya.Hilm `
	- *TAGS: CENT0300, _AKHLAQ, _IBNABIDUNYA*
 * `0281IbnAbiDunya.HilmMucawiya `
	- *TAGS: CENT0300, _AJZA, _HADITH*
 * `0281IbnAbiDunya.HusnZannBiLlah `
	- *TAGS: CENT0300, _AKHLAQ, _CAQAID, _HADITH, _IBNABIDUNYA, _SUNNI*
 * `0281IbnAbiDunya.IctibarWaAcqab `
	- *TAGS: CENT0300, _AKHLAQ, _HADITH, _IBNABIDUNYA, _SUNNI*
 * `0281IbnAbiDunya.Ikhwan `
	- *TAGS: CENT0300, _AKHLAQ, _IBNABIDUNYA*
 * `0281IbnAbiDunya.IshrafFiManazil `
	- *TAGS: CENT0300, _AKHLAQ, _IBNABIDUNYA*
 * `0281IbnAbiDunya.IslahMal `
	- *TAGS: CENT0300, _AKHLAQ, _IBNABIDUNYA*
 * `0281IbnAbiDunya.MakarimAkhlaq `
	- *TAGS: CENT0300, _AKHLAQ, _HADITH, _IBNABIDUNYA, _SUNNI*
 * `0281IbnAbiDunya.ManCashaBacdaMawt `
	- *TAGS: CENT0300, _CAQAID, _HADITH, _IBNABIDUNYA, _MILAL*
 * `0281IbnAbiDunya.Manamat `
	- *TAGS: CENT0300, _AHLAM, _CAQAID, _HADITH, _IBNABIDUNYA*
 * `0281IbnAbiDunya.MaqtalCali `
	- *TAGS: CENT0300, _AJZA, _HADITH, _TARAJIM*
 * `0281IbnAbiDunya.MaqtalCali `
	- *TAGS: CENT0300, _IBNABIDUNYA*
 * `0281IbnAbiDunya.MaradWaKaffarat `
	- *TAGS: CENT0300, _AKHLAQ, _IBNABIDUNYA*
 * `0281IbnAbiDunya.MudaratNas `
	- *TAGS: CENT0300, _AKHLAQ, _IBNABIDUNYA*
 * `0281IbnAbiDunya.MuhasabaNafs `
	- *TAGS: CENT0300, _AKHLAQ, _IBNABIDUNYA*
 * `0281IbnAbiDunya.Muhtadirin `
	- *TAGS: CENT0300, _AKHLAQ, _IBNABIDUNYA, _MISC*
 * `0281IbnAbiDunya.MujabuDacwa `
	- *TAGS: CENT0300, _AKHLAQ, _IBNABIDUNYA*
 * `0281IbnAbiDunya.Mutammanin `
	- *TAGS: CENT0300, _AKHLAQ, _IBNABIDUNYA*
 * `0281IbnAbiDunya.QadaHawaij `
	- *TAGS: CENT0300, _AKHLAQ, _HADITH, _IBNABIDUNYA, _SUNNI*
 * `0281IbnAbiDunya.QasrAmal `
	- *TAGS: CENT0300, _AJZA, _HADITH, _IBNABIDUNYA, _TARAJIM*
 * `0281IbnAbiDunya.Rida `
	- *TAGS: CENT0300, _AKHLAQ, _CAQAID, _HADITH, _IBNABIDUNYA*
 * `0281IbnAbiDunya.SamtWaAdab `
	- *TAGS: CENT0300, _AKHLAQ, _HADITH, _IBNABIDUNYA, _SUNNI*
 * `0281IbnAbiDunya.Shukr `
	- *TAGS: CENT0300, _AKHLAQ, _IBNABIDUNYA*
 * `0281IbnAbiDunya.ShukrLiLlah `
	- *TAGS: CENT0300, _HADITH, _SUNNI*
 * `0281IbnAbiDunya.SifaJanna `
	- *TAGS: CENT0300, _CAQAID, _HADITH, _IBNABIDUNYA, _MILAL*
 * `0281IbnAbiDunya.SifaNar `
	- *TAGS: CENT0300, _CAQAID, _HADITH, _IBNABIDUNYA, _MILAL*
 * `0281IbnAbiDunya.TawaducWaKhumul `
	- *TAGS: CENT0300, _AKHLAQ, _HADITH, _IBNABIDUNYA, _SUNNI*
 * `0281IbnAbiDunya.Tawba `
	- *TAGS: CENT0300, _AKHLAQ, _IBNABIDUNYA*
 * `0281IbnAbiDunya.WajalWaTawaththuq `
	- *TAGS: CENT0300, _AKHLAQ, _IBNABIDUNYA*
 * `0281IbnAbiDunya.Warac `
	- *TAGS: CENT0300, _AKHLAQ, _IBNABIDUNYA*
 * `0281IbnAbiDunya.Warac `
	- *TAGS: CENT0300, _HADITH, _SUNNI*
 * `0281IbnAbiDunya.Yaqin `
	- *TAGS: CENT0300, _AKHLAQ, _IBNABIDUNYA*
 * `0281IbnAbiDunya.Zuhd `
	- *TAGS: CENT0300, _AKHLAQ, _IBNABIDUNYA*
 * `0282AbuHanifaDinawari.AkhbarTiwal `
	- *TAGS: CENT0300, PPE, _HADITH, _SUNNI, _TARAJIM, _TARIKH*
 * `0282HarithHaythami.BughyaBahith `
	- *TAGS: CENT0300, _HADITH, _MACAJIM, _MASANID, _SUNNI, _TARAJIM*
 * `0282IbnIshaqJahdami.FadlSalat `
	- *TAGS: CENT0300, _AJZA, _AKHLAQ, _ALBANI, _FIQH, _HADITH, _MASAIL, _SUNNI, _USUL*
 * `0285IbnYazidMubarrad.Fadil `
	- *TAGS: CENT0300, _ADAB, _ADAB, _BALAGHA, _FASAHA*
 * `0285IbnYazidMubarrad.Tacazi `
	- *TAGS: CENT0300, _ADAB, _ADAB, _BALAGHA, _SHICR*
 * `0285IbrahimHarbi.GharibHadith `
	- *TAGS: CENT0300, _FIQH, _GHARIB, _HADITH, _LUGHA, _MACAJIM, _MUSTALAHAT, _NAHW, _SARF*
 * `0285IbrahimHarbi.IkramDayf `
	- *TAGS: CENT0300, _AJZA, _AKHLAQ, _HADITH, _SUNNI*
 * `0286IbnWaddahQurtubi.Bidac `
	- *TAGS: CENT0300, _FIQH, _HADITH, _MASAIL*
 * `0286Mubarrad.NasabCadnan `
	- *TAGS: CENT0300, GEN, PPE, _ANSAB, _BULDAN, _TARIKH*
 * `0287Dahhak.AhadWaMathani `
	- *TAGS: CENT0300, PPE, _HADITH, _MACAJIM, _MASANID, _SUNNI, _TABAQAT, _TARAJIM*
 * `0287Dahhak.Awail `
	- *TAGS: CENT0300, _AJZA, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0287Dahhak.Diyat `
	- *TAGS: CENT0300, _BUHUTH, _FIQH, _MASAIL, _USUL*
 * `0287Dahhak.Jihad `
	- *TAGS: CENT0300, _AJZA, _FIQH, _HADITH, _MASAIL, _TARAJIM, _USUL*
 * `0287Dahhak.Mudhakkir `
	- *TAGS: CENT0300, _AJZA, _AKHLAQ, _HADITH, _SUNNI*
 * `0287Dahhak.Salat `
	- *TAGS: CENT0300, _AJZA, _HADITH*
 * `0287Dahhak.Sunna `
	- *TAGS: CENT0300, _AJZA, _CAQAID, _HADITH, _MILAL*
 * `0287Dahhak.Sunna `
	- *TAGS: CENT0300, _HADITH, _SUNNI*
 * `0287Dahhak.Zuhd `
	- *TAGS: CENT0300, _ADAB, _ADHKAR, _AJZA, _AKHLAQ, _HADITH, _RAQAIQ*
 * `0290IbnAhmadIbnHanbal.FadailCuthman `
	- *TAGS: CENT0300, _AJZA, _HADITH, _TARAJIM*
 * `0290IbnAhmadIbnHanbal.Sunna `
	- *TAGS: CENT0300, _CAQAID, _HADITH, _MILAL*
 * `0290IbnHasanSaffar.BasairDarajat `
	- *TAGS: CENT0300, _HADITH, _SHICI*
 * `0291IbnYahyaThaclab.Fasih `
	- *TAGS: CENT0300, _FIQH, _GHARIB, _MACAJIM, _MUSTALAHAT*
 * `0291IbnYahyaThaclab.MajalisThaclab `
	- *TAGS: CENT0300, _ADAB, _BALAGHA, _QISAS, _TARAIF*
 * `0291IbnYahyaThaclab.QawacidShicr `
	- *TAGS: CENT0300, _ADAB, _ADAB, _BALAGHA, _SHICR*
 * `0292AbuBakrBazzar.BahrZakhkhar `
	- *TAGS: CENT0300, _HADITH, _MACAJIM, _MASANID, _TARAJIM*
 * `0292Bahshal.TarikhWasit `
	- *TAGS: CENT0300, PPE, _BULDAN, _HADITH, _TABAQAT, _TARAJIM, _TARIKH*
 * `0292IbnCaliMarwazi.MusnadAbiBakr `
	- *TAGS: CENT0300, _AJZA, _HADITH, _MACAJIM, _MASANID, _TARAJIM*
 * `0292Yacqubi.Buldan `
	- *TAGS: CENT0300, PPE, _BULDAN, _JUGHRAFIYA, _RIHLAT, _TARIKH*
 * `0292Yacqubi.TarikhYacqubi `
	- *TAGS: CENT0300, PPE, _TARIKH*
 * `0294IbnNasrMarwazi.IkhtilafCulama `
	- *TAGS: CENT0300, _FIQH, _HADITH*
 * `0294IbnNasrMarwazi.Sunna `
	- *TAGS: CENT0300, _AJZA, _CAQAID, _HADITH, _MILAL*
 * `0294IbnNasrMarwazi.TaczimQadrSalat `
	- *TAGS: CENT0300, _FIQH, _HADITH, _MASAIL, _USUL*
 * `0296IbnMuctazz.Diwan `
	- *TAGS: CENT0300, _SHICR_CABBASI, _SHICR*
 * `0296IbnMuctazz.TabaqatShucara `
	- *TAGS: CENT0300, PPE, _TABAQAT, _TARAJIM*
 * `0296MuhammadIbnJarrah.ManIsmuhCamr `
	- *TAGS: CENT0300, _TABAQAT, _TARAJIM, _TARIKH*
 * `0297IbnAbiShayba.Carsh `
	- *TAGS: CENT0300, _AJZA, _CAQAID, _HADITH, _MILAL*
 * `0297IbnAbiShayba.Carsh `
	- *TAGS: CENT0300, _AJZA, _HADITH*
 * `0297IbnAbiShayba.Carsh `
	- *TAGS: CENT0300, _HADITH, _SUNNI*
 * `0297IbnAbuShayba.JuzFihiMasail `
	- *TAGS: CENT0300, _CILAL, _SUALAT*
 * `0297IbnDawudZahiri.Zahra `
	- *TAGS: CENT0300, _ADAB, _BALAGHA, _MISC*
 * `0300IbnJacfarHimyari.QurbIsnad `
	- *TAGS: CENT0300, _HADITH, _SHICI*
 * `0300IbnKhurdadhbih.MasalikWaMamalik `
	- *TAGS: CENT0300, GEO, PPE, _BULDAN, _JUGHRAFIYA, _MUDHAKKARAT, _RIHLAT, _TARIKH*
 * `0300IbnKhurdadhbih.MukhtarMinKitabLahw `
	- *TAGS: CENT0300, _ADAB, _BALAGHA, _MISC*
 * `0300IbnZakariyaHajari.Tacliqat `
	- *TAGS: CENT0300, _ADAB, _BALAGHA, _QISAS, _TARAIF*
 * `0300MuallifMajhul.AkhbarDawlaCabbasiya `
	- *TAGS: CENT0300, PPE, _TARIKH*

* **0400AH [[ [Re]generated on 2016-10-22 (17:14:35) ]]**

 * `0301AbuBakrFaryabi.DalailNubuwwa `
	- *TAGS: CENT0400, _AJZA, _ASHAB, _CAQAID, _HADITH, _SIRA, _TABAQAT, _TARAJIM*
 * `0301Bardiji.TabaqatAsma `
	- *TAGS: CENT0400, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0303Nasai.DhikrMudallisin `
	- *TAGS: CENT0400, PPE, _HADITH, _MUSTALAHAT, _TABAQAT, _TARAJIM*
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
 * `0307AbuYaclaMawsili.Mafarid `
	- *TAGS: CENT0400, _AJZA, _HADITH, _SUNNI, _TARAJIM*
 * `0307AbuYaclaMawsili.Mucjam `
	- *TAGS: CENT0400, _HADITH, _MACAJIM, _MASANID, _TARAJIM*
 * `0308IbnIbrahimJundi.FadailMadina `
	- *TAGS: CENT0400, _AJZA, _BULDAN, _HADITH, _TABAQAT, _TARAJIM, _TARIKH*
 * `0308IbnIbrahimJundi.FadailMadina `
	- *TAGS: CENT0400, _TARIKH*
 * `0309IbnFadlan.Rihla `
	- *TAGS: CENT0400, GEO, PPE, _BULDAN, _JUGHRAFIYA, _MUDHAKKARAT, _RIHLAT, _TARIKH*
 * `0309IbnMarzuban.DhammThuqala `
	- *TAGS: CENT0400, _AJZA, _AKHLAQ, _HADITH, _SUNNI*
 * `0309IbnMarzuban.FadlKilab `
	- *TAGS: CENT0400, _ADAB, _AJZA, _BALAGHA, _FIQH, _MASAIL, _USUL*
 * `0310IbnAhmadDulabi.Dhariyya `
	- *TAGS: CENT0400, PPE, _ASHAB, _HADITH, _SIRA, _SUNNI, _TABAQAT, _TARAJIM*
 * `0310IbnAhmadDulabi.KunaWaAsma `
	- *TAGS: CENT0400, PPE, _HADITH, _TARAJIM*
 * `0310Nawbakhti.FiraqShica `
	- *TAGS: CENT0400, _CAQAID, _FIRAQ, _MILAL*
 * `0310Tabari.IkhtilafFuqaha `
	- *TAGS: CENT0400, _FIQH*
 * `0310Tabari.JamicBayan `
	- *TAGS: CENT0400, SBS, _AHKAM, _CULUM, _HADITH, _QURAN, _SUNNI, _TAFSIR*
 * `0310Tabari.MuntakhabMinDhayl `
	- *TAGS: CENT0400, PPE, _MISC, _TABAQAT, _TARAJIM, _TARIKH*
 * `0310Tabari.SarihSunna `
	- *TAGS: CENT0400, _AJZA, _CAQAID, _HADITH, _MILAL, _SUNNI*
 * `0310Tabari.TabsirFiMacalimDin `
	- *TAGS: CENT0400, _AJZA, _HADITH*
 * `0310Tabari.TahdhibAthar `
	- *TAGS: CENT0400, _FIQH, _HADITH, _TARAJIM*
 * `0310Tabari.TahdhibAthar `
	- *TAGS: CENT0400, _FIQH, _HADITH, _TARAJIM*
 * `0310Tabari.TahdhibAthar `
	- *TAGS: CENT0400, _FIQH, _HADITH, _TARAJIM*
 * `0310Tabari.TahdhibAthar `
	- *TAGS: CENT0400, _FIQH, _HADITH, _TARAJIM*
 * `0310Tabari.Tarikh `
	- *TAGS: CENT0400, CHR, PPE, _TARIKH*
 * `0312IbnCaliTusi.MukhtasarAhkam `
	- *TAGS: CENT0400, _FIQH, _HADITH, _SUNAN, _TARAJIM*
 * `0312IbnMuhammadBaghandi.MusnadCumar `
	- *TAGS: CENT0400, _AJZA, _HADITH, _MACAJIM, _MASANID, _SUNNI, _TARAJIM*
 * `0313IbnIshaqSarraj.Musnad `
	- *TAGS: CENT0400, _HADITH, _MACAJIM, _MASANID, _TARAJIM*
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
 * `0324Ashcari.Ibana `
	- *TAGS: CENT0400, _CAQAID, _MILAL*
 * `0324Ashcari.MaqalatIslamiyyin `
	- *TAGS: CENT0400, _CAQAID, _FARQ, _FIRAQ, _MILAL, _RUDUD*
 * `0324Ashcari.RisalaIlaAhlThughr `
	- *TAGS: CENT0400, _CAQAID, _MILAL*
 * `0327IbnAbiHatimRazi.BayanKhataBukhari `
	- *TAGS: CENT0400, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0328IbnCabdRabbihi.CiqdFarid `
	- *TAGS: CENT0400, _ADAB, _ADAB, _BALAGHA, _QISAS, _TARAIF*
 * `0328IbnCabdRabbihi.Diwan `
	- *TAGS: _SHICR_ANDALUSI, _CENT00NO, _SHICR*
 * `0328IbnCabdRabbihi.TabaicNisa `
	- *TAGS: CENT0400, _ADAB, _ADAB, _BALAGHA, _QISAS, _TARAIF*
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
 * `0335Suli.AdabKuttab `
	- *TAGS: CENT0400, _ADAB, _ADAB, _BALAGHA, _CARUD, _KITABA*
 * `0335Suli.AkhbarAbiTamam `
	- *TAGS: CENT0400, _ADAB, _BALAGHA, _TARAJIM, _TARIKH*
 * `0335Suli.AkhbarRadi `
	- *TAGS: CENT0400, _ADAB, _BALAGHA, _TARAJIM, _TARIKH*
 * `0335Suli.AshcarAwladKhulafa `
	- *TAGS: CENT0400, _ADAB, _ADAB, _BALAGHA, _SHICR*
 * `0335Suli.JuzMinAhadith `
	- *TAGS: CENT0400, _AJZA, _HADITH*
 * `0337IbnIshaqZajjaji.Akhbar `
	- *TAGS: CENT0400, _NAHW, _SARF, _TARAJIM, _TARIKH*
 * `0337QudamaIbnJacfar.Kharaj `
	- *TAGS: CENT0400, _ADAB, _BUHUTH, _CARUD, _FIQH, _KITABA, _MASAIL, _USUL*
 * `0337QudamaIbnJacfar.NaqdShicr `
	- *TAGS: CENT0400, _ADAB, _BALAGHA*
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
 * `0360AbuBakrAjurri.AkhbarAbiHafs `
	- *TAGS: CENT0400, _TABAQAT, _TARAJIM, _TARIKH*
 * `0360Khawlani.TarikhDaraya `
	- *TAGS: CENT0400, HIS, PPE, _BULDAN, _HADITH, _TARIKH*
 * `0360Tabarani.Awail `
	- *TAGS: CENT0400, _AJZA, _HADITH, _TABAQAT, _TARAJIM*
 * `0360Tabarani.MucjamAwsat `
	- *TAGS: CENT0400, _HADITH, _MACAJIM, _MASANID, _SUNNI, _TARAJIM*
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
 * `0381AbuQasimJawhari.MusnadMuwatta `
	- *TAGS: CENT0400, _HADITH*
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
 * `0385IbnShahin.DhikrManIkhtalafaCulama `
	- *TAGS: CENT0400, _HADITH, _MISC, _TABAQAT, _TARAJIM*
 * `0385IbnShahin.TarikhAsmaDucafa `
	- *TAGS: CENT0400, PPE, _TABAQAT, _TARAJIM*
 * `0385IbnShahin.TarikhAsmaThiqat `
	- *TAGS: CENT0400, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM, _THIQAT*
 * `0386AbuTalibMakki.QutQulub `
	- *TAGS: CENT0300, CENT0400, _ADAB, _ADHKAR, _AKHLAQ, _CHRONOMULTIPLE, _RAQAIQ, _TASAWWUF*
 * `0387IbnSamcunBaghdadi.Amali `
	- *TAGS: CENT0400, _AJZA, _HADITH, _TARAJIM*
 * `0387KatibKhwarizmi.MafatihCulum `
	- *TAGS: CENT0400, _FAHARIS, _FIQH, _GHARIB, _KUTUB, _MACAJIM, _MUSTALAHAT*
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
 * `0400IbnCamashliqJacfari.JuzIbnCamashliq `
	- *TAGS: CENT0400, _AJZA, _HADITH, _TARAJIM*
 * `0400IbnTahirMaqdisi.BadWaTarikh `
	- *TAGS: CENT0600, PPE, _TARIKH*
 * `0400IshaqMunajjim.AkamMarjan `
	- *TAGS: CENT0400, _BULDAN, _JUGHRAFIYA, _RIHLAT*

* **0500AH [[ [Re]generated on 2016-10-22 (17:14:35) ]]**

 * `0402MuhammadSaydawi.MucjamShuyukh `
	- *TAGS: CENT0500, _HADITH, _MACAJIM, _MASANID, _TABAQAT, _TARAJIM*
 * `0403IbnFaradi.TarikhCulamaAndalus `
	- *TAGS: CENT0500, PPE, _BULDAN, _TABAQAT, _TARAJIM, _TARIKH*
 * `0405AbuFadlHarawi.MucjamFiMushtabah `
	- *TAGS: CENT0500, PPE, _HADITH, _MISC, _TABAQAT, _TARAJIM*
 * `0405HakimNaysaburi.MacrifatCulumHadith `
	- *TAGS: CENT0500, _FIQH, _HADITH, _MUSTALAHAT, _QAWACID, _SUNNI, _USUL*
 * `0405HakimNaysaburi.Mustadrak `
	- *TAGS: CENT0500, _FIQH, _HADITH, _SAHIH, _SUNNI, _TARAJIM*
 * `0405HakimNaysaburi.TalkhisTarikhNaysabur `
	- *TAGS: CENT0500, PPE, _TABAQAT, _TARAJIM*
 * `0405HakimNaysaburi.TasmiyaManAkhrajahum `
	- *TAGS: CENT0500, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0409CabdGhaniAzdi.KitabMutawarin `
	- *TAGS: CENT0500, _TARIKH*
 * `0410IbnMardawayh.ThalathaMajalis `
	- *TAGS: CENT0500, _AJZA, _AMALI, _HADITH, _MAJALIS, _TARAJIM*
 * `0412Sulami.TabaqatSufiya `
	- *TAGS: CENT0500, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `0413ShaykhMufid.AhkamNisa `
	- *TAGS: CENT0500, _BEFORE800, _FIQH, _SHICI*
 * `0413ShaykhMufid.Amali `
	- *TAGS: CENT0500, _HADITH, _SHICI*
 * `0413ShaykhMufid.Irshad `
	- *TAGS: CENT0500, _HADITH, _SHICI*
 * `0413ShaykhMufid.MasarShica `
	- *TAGS: CENT0500, _HADITH, _SHICI*
 * `0413ShaykhMufid.Muqnica `
	- *TAGS: CENT0500, _BEFORE800, _FIQH, _SHICI*
 * `0414AbuHayyanTawhidi.AkhlaqWazirayn `
	- *TAGS: CENT0400, _ADAB, _BALAGHA, _TARAJIM, _TARIKH*
 * `0414AbuHayyanTawhidi.Basair `
	- *TAGS: CENT0500, _ADAB, _ADAB, _BALAGHA, _QISAS, _TARAIF*
 * `0414AbuHayyanTawhidi.Imtac `
	- *TAGS: CENT0400, _ADAB, _ADAB, _BALAGHA, _QISAS, _TARAIF*
 * `0414AbuHayyanTawhidi.Muqabasat `
	- *TAGS: CENT0400, _ADAB, _BALAGHA*
 * `0414AbuHayyanTawhidi.Sadaqa `
	- *TAGS: CENT0400, _ADAB, _AKHLAQ, _BALAGHA, _MISC, _SULUK*
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
 * `0429AbuMansurThacalibi.AhsanMaSamictu `
	- *TAGS: CENT0500, _ADAB, _BALAGHA*
 * `0429AbuMansurThacalibi.Diwan `
	- *TAGS: _SHICR_CABBASI, _CENT00NO, _SHICR*
 * `0429AbuMansurThacalibi.DurarHikm `
	- *TAGS: CENT0500, _ADAB, _ADHKAR, _RAQAIQ*
 * `0429AbuMansurThacalibi.FiqhLugha `
	- *TAGS: CENT0500, _ADAB, _BALAGHA, _FASAHA, _LUGHA*
 * `0429AbuMansurThacalibi.IcjazWaIjaz `
	- *TAGS: CENT0500, _ADAB, _ADAB, _BALAGHA, _FASAHA*
 * `0429AbuMansurThacalibi.KhassKhass `
	- *TAGS: CENT0500, _ADAB, _ADAB, _BALAGHA, _FASAHA*
 * `0429AbuMansurThacalibi.LataifWaZaraif `
	- *TAGS: CENT0500, _ADAB, _BALAGHA*
 * `0429AbuMansurThacalibi.LubabAdab `
	- *TAGS: CENT0500, _ADAB, _ADAB, _BALAGHA, _FASAHA*
 * `0429AbuMansurThacalibi.Lutf `
	- *TAGS: CENT0500, _ADAB, _BALAGHA*
 * `0429AbuMansurThacalibi.ManGhabaCanhuMutrib `
	- *TAGS: CENT0500, _ADAB, _ADAB, _BALAGHA, _QISAS, _TARAIF*
 * `0429AbuMansurThacalibi.Muntahal `
	- *TAGS: CENT0500, _ADAB, _ADAB, _BALAGHA, _MISC*
 * `0429AbuMansurThacalibi.MutanabbiWaMaLahu `
	- *TAGS: CENT0500, _ADAB, _BALAGHA*
 * `0429AbuMansurThacalibi.Rasail `
	- *TAGS: CENT0500, _ADAB, _BALAGHA, _MISC*
 * `0429AbuMansurThacalibi.Shakwa `
	- *TAGS: CENT0500, _ADAB, _BALAGHA*
 * `0429AbuMansurThacalibi.SihrBalagha `
	- *TAGS: CENT0500, _ADAB, _ADAB, _BALAGHA, _FASAHA*
 * `0429AbuMansurThacalibi.TahsinQabih `
	- *TAGS: CENT0500, _ADAB, _ADAB, _BALAGHA, _QISAS, _TARAIF*
 * `0429AbuMansurThacalibi.Tamthil `
	- *TAGS: CENT0500, _ADAB, _ADAB, _BALAGHA, _QISAS, _TARAIF*
 * `0429AbuMansurThacalibi.ThimarQulub `
	- *TAGS: CENT0500, SBS, _ADAB, _ADAB, _AMTHAL, _BALAGHA*
 * `0429AbuMansurThacalibi.YatimaDahr `
	- *TAGS: CENT0500, PPE, _ADAB, _SHICR, _TABAQAT, _TARAJIM, _TARIKH*
 * `0430AbuNucaymIsbahani.DhikrManIsmuhuShucba `
	- *TAGS: CENT0500, PPE, _AJZA, _HADITH, _MISC, _TARAJIM*
 * `0430AbuNucaymIsbahani.Ducafa `
	- *TAGS: CENT0500, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0430AbuNucaymIsbahani.HilyaAwliya `
	- *TAGS: CENT0500, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0430AbuNucaymIsbahani.MacrifaSahaba `
	- *TAGS: CENT0500, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0430AbuNucaymIsbahani.MajlisMinAmali `
	- *TAGS: CENT0500, _AJZA, _AMALI, _HADITH, _MAJALIS, _TARAJIM*
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
	- *TAGS: CENT0500, _SHICR_CABBASI, _SHICR*
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
 * `0458Bayhaqi.AsmaWaSifat `
	- *TAGS: CENT0500, _CAQAID, _HADITH, _MILAL*
 * `0458Bayhaqi.DalailNubuwwa `
	- *TAGS: CENT0500, DHB, PPE, _ASHAB, _CAQAID, _HADITH, _SHAMAIL, _SIRA*
 * `0458Bayhaqi.Ictiqad `
	- *TAGS: CENT0500, _AJZA, _CAQAID, _HADITH, _MILAL*
 * `0460ShaykhTusi.IkhtiyarMacrifaRijal `
	- *TAGS: CENT0500, PPE, SHC, _HADITH, _SHICI, _TARAJIM*
 * `0460ShaykhTusi.Rijal `
	- *TAGS: CENT0500, PPE, SHC, _HADITH, _SHICI, _TARAJIM*
 * `0461IbnHusaynSughdi.NutafFifatawa `
	- *TAGS: CENT0500, _FIQH, _HANAFI*
 * `0463IbnCabdBarr.AdabMujalasa `
	- *TAGS: CENT0500, _ADAB, _ADHKAR, _AKHLAQ, _HADITH, _MISC, _RAQAIQ, _SUNNI*
 * `0463IbnCabdBarr.BahjatMajalis `
	- *TAGS: CENT0500, _ADAB, _ADHKAR*
 * `0463IbnCabdBarr.Durar `
	- *TAGS: CENT0500, PPE, _ASHAB, _HADITH, _SHAMAIL, _SIRA, _SUNNI*
 * `0463IbnCabdBarr.InbahCalaQabail `
	- *TAGS: CENT0500, _ANSAB, _HADITH, _SUNNI, _TARIKH*
 * `0463IbnCabdBarr.Insaf `
	- *TAGS: CENT0500, _BUHUTH, _FIQH, _MASAIL*
 * `0463IbnCabdBarr.IntiqaFiFadail `
	- *TAGS: CENT0500, PPE, _FIQH, _HADITH, _SUNNI, _TABAQAT, _TARAJIM, _TARIKH*
 * `0463IbnCabdBarr.IsticabFiMacrifaAshab `
	- *TAGS: BIO, CENT0500, COL, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0463IbnCabdBarr.IstidhkarJamic `
	- *TAGS: CENT0500, _FIQH, _HADITH, _MALIKI, _SHARH, _SUNNI*
 * `0463IbnCabdBarr.JamicBayan `
	- *TAGS: CENT0500, _AKHLAQ, _HADITH, _MISC, _SULUK, _SUNNI*
 * `0463IbnCabdBarr.KafiFiFiqh `
	- *TAGS: CENT0500, _FIQH, _HADITH, _MALIKI, _SUNNI*
 * `0463IbnCabdBarr.TamhidMuwatta `
	- *TAGS: CENT0500, _FIQH, _HADITH, _MALIKI, _SHARH, _SUNNI, _TARAJIM*
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
	- *TAGS: CENT0500, _BULDAN, _FAHARIS, _GHARIB, _JUGHRAFIYA, _LUGHA, _MACAJIM, _MUSTALAHAT, _NAHW, _RIHLAT, _SARF*
 * `0488IbnFutuhHumaydi.JadhwaMuqtabis `
	- *TAGS: CENT0500, PPE, _TABAQAT, _TARAJIM, _TARIKH*
 * `0498AbuCaliJayyani.AlqabSahaba `
	- *TAGS: CENT0500, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0498AbuCaliJayyani.TaqyidMuhmal `
	- *TAGS: CENT0500, PPE, _HADITH, _MISC, _TABAQAT, _TARAJIM*
 * `0499IbnHusaynJurjani.TartibAmali `
	- *TAGS: CENT0500, _AJZA, _HADITH, _TARAJIM*

* **0600AH [[ [Re]generated on 2016-10-22 (17:14:35) ]]**

 * `0505Ghazali.AsnafMaghrurin `
	- *TAGS: CENT0600, _ADAB, _ADHKAR, _AKHLAQ, _MISC, _RAQAIQ, _SULUK*
 * `0505Ghazali.BidayatHidaya `
	- *TAGS: CENT0600, _ADAB, _ADHKAR, _RAQAIQ*
 * `0505Ghazali.Fadaih `
	- *TAGS: CENT0600, _CAQAID, _MILAL, _RUDUD*
 * `0505Ghazali.IhyaCulumDin `
	- *TAGS: CENT0600, _ADAB, _ADHKAR, _AKHLAQ, _MISC, _RAQAIQ, _SULUK*
 * `0505Ghazali.Iqtisad `
	- *TAGS: CENT0600, _CAQAID, _MILAL*
 * `0505Ghazali.JawahirQuran `
	- *TAGS: CENT0600, _CAQAID, _CULUM, _QURAN, _TAFSIR*
 * `0505Ghazali.KimiyaSacada `
	- *TAGS: CENT0600, _ADAB, _ADHKAR, _RAQAIQ*
 * `0505Ghazali.MacarijQuds `
	- *TAGS: CENT0600, _CAQAID, _MILAL*
 * `0505Ghazali.MahkNazar `
	- *TAGS: CENT0600, _MISC*
 * `0505Ghazali.Mankhul `
	- *TAGS: CENT0600, _FIQH, _QAWACID, _SUNNI, _USUL*
 * `0505Ghazali.MaqsadAsna `
	- *TAGS: CENT0600, _CAQAID, _MILAL, _MISC*
 * `0505Ghazali.MicyarCilm `
	- *TAGS: CENT0600, _MISC*
 * `0505Ghazali.MishkatAnwar `
	- *TAGS: CENT0600, _AKHLAQ, _TASAWWUF, _ADAB, _ADHKAR, _RAQAIQ*
 * `0505Ghazali.MizanCamal `
	- *TAGS: CENT0600, _ADAB, _ADHKAR, _AKHLAQ, _MISC, _RAQAIQ, _SULUK*
 * `0505Ghazali.Munqidh `
	- *TAGS: CENT0600, _ADAB, _ADHKAR, _AKHLAQ, _RAQAIQ, _TASAWWUF*
 * `0505Ghazali.Mustasfa `
	- *TAGS: CENT0600, _FIQH, _QAWACID, _SUNNI, _USUL*
 * `0505Ghazali.QawaidCaqaid `
	- *TAGS: CENT0600, _CAQAID, _MILAL*
 * `0505Ghazali.SirrCalamin `
	- *TAGS: CENT0600, _AKHLAQ, _TASAWWUF*
 * `0505Ghazali.Tahafut `
	- *TAGS: CENT0600, _MISC*
 * `0505Ghazali.TibrMasbuk `
	- *TAGS: CENT0600, _QADA, _SIYASA*
 * `0505Ghazali.Wasit `
	- *TAGS: CENT0600, _FIQH, _SHAFICI*
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
 * `0538IbnCumarZamakhshari.FaiqFiGharib `
	- *TAGS: CENT0600, _FAHARIS, _FIQH, _GHARIB, _HADITH, _MACAJIM, _MUSTALAHAT, _SUNNI*
 * `0538MahmudZamakhshari.JibalWaAmkina `
	- *TAGS: CENT0600, GEO, PPE, _BULDAN, _JUGHRAFIYA, _RIHLAT*
 * `0540AbuMansurJawaliqi.SharhAdabKatib `
	- *TAGS: CENT0600, _ADAB, _ADAB, _BALAGHA, _CARUD, _KITABA*
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
 * `0571IbnCasakir.ArbacunaBuldaniyya `
	- *TAGS: CENT0600, _AJZA, _HADITH, _SUNNI, _TARAJIM*
 * `0571IbnCasakir.ArbacunaFiHathth `
	- *TAGS: CENT0600, _AJZA, _FIQH, _HADITH, _MASAIL, _TARAJIM, _USUL*
 * `0571IbnCasakir.KashfMughatta `
	- *TAGS: CENT0600, _CULUM, _HADITH, _MUSTALAHAT*
 * `0571IbnCasakir.MadhTawaduc `
	- *TAGS: CENT0600, _AJZA, _HADITH*
 * `0571IbnCasakir.MucjamShuyukh `
	- *TAGS: CENT0600, PPE, _HADITH*
 * `0571IbnCasakir.TabyinImtinan `
	- *TAGS: CENT0600, _AJZA, _HADITH*
 * `0571IbnCasakir.TabyinKadhb `
	- *TAGS: CENT0600, _CAQAID, _MILAL, _RUDUD*
 * `0571IbnCasakir.TacziyatMuslim `
	- *TAGS: CENT0600, _AJZA, _AKHLAQ, _HADITH, _SUNNI*
 * `0571IbnCasakir.TarikhDimashq `
	- *TAGS: BIO, CENT0600, COL, PPE, _BULDAN, _HADITH, _SUNNI, _TABAQAT, _TARAJIM, _TARIKH*
 * `0571IbnCasakir.TarjamatHasan `
	- *TAGS: CENT0600, _IMAM, _NABI, _SIRA*
 * `0571IbnCasakir.TarjamatHusayn `
	- *TAGS: CENT0600, _IMAM, _NABI, _SIRA*
 * `0571IbnCasakir.Tawba `
	- *TAGS: CENT0600, _AJZA, _AKHLAQ, _HADITH, _MISC, _SULUK*
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
 * `0578IbnBashkuwal.MaRuwiyaFiHawd `
	- *TAGS: CENT0300, CENT0600, _AJZA, _AKHLAQ, _CAQAID, _CHRONOMULTIPLE, _HADITH, _SUNNI*
 * `0578IbnBashkuwal.Sila `
	- *TAGS: BIO, CENT0600, COL, PPE, _TARAJIM, _TARIKH*
 * `0580IbnCimrani.InbaFiTarikhKhulafa `
	- *TAGS: CENT0600, HIS, PPE, _TARIKH*
 * `0581IbnCumarIsbahani.DhikrIbnAbiDunya `
	- *TAGS: CENT0600, _AJZA, _HADITH*
 * `0581IbnCumarIsbahani.DhikrIbnMandah `
	- *TAGS: CENT0600, _AJZA, _HADITH*
 * `0581IbnCumarIsbahani.KalamCalaHadithIstilqa `
	- *TAGS: CENT0600, _HADITH, _MAKHTUTAT*
 * `0581IbnCumarIsbahani.KhasaisMusnadAhmad `
	- *TAGS: CENT0600, _CULUM, _HADITH, _MISC, _MUSTALAHAT, _SUNNI*
 * `0581IbnCumarIsbahani.Lataif `
	- *TAGS: CENT0600, _CULUM, _HADITH, _MAKHTUTAT*
 * `0581IbnCumarIsbahani.MuntahaRaghabat `
	- *TAGS: CENT0600, _AJZA, _HADITH*
 * `0581IbnCumarIsbahani.NuzhatHuffaz `
	- *TAGS: CENT0600, _AJZA, _HADITH, _MUSTALAHAT*
 * `0581IbnCumarIsbahani.TiwalatAkhbar `
	- *TAGS: CENT0600, _HADITH, _MAKHTUTAT*
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
 * `0597IbnJawzi.Adhkiya `
	- *TAGS: CENT0600, _ADAB, _ADAB, _ADHKAR, _QISAS, _RAQAIQ, _TARAIF*
 * `0597IbnJawzi.AkhbarNisa `
	- *TAGS: CENT0600, _ADAB, _BALAGHA*
 * `0597IbnJawzi.BahrDumuc `
	- *TAGS: CENT0600, _ADAB, _ADHKAR, _RAQAIQ*
 * `0597IbnJawzi.BirrWaSila `
	- *TAGS: CENT0600, _ADAB, _ADHKAR, _RAQAIQ*
 * `0597IbnJawzi.BirrWalidayn `
	- *TAGS: CENT0600, _ADAB, _ADHKAR, _AKHLAQ, _MISC, _SULUK*
 * `0597IbnJawzi.BustanWacizin `
	- *TAGS: CENT0600, _ADAB, _ADAB, _ADHKAR, _MISC, _QISAS, _RAQAIQ, _TARAIF*
 * `0597IbnJawzi.CilalMutanahiyya `
	- *TAGS: CENT0600, _AHKAM, _CILAL, _DACIF, _FIQH, _HADITH, _MAWDUC, _SUALAT, _TAKHRIJ*
 * `0597IbnJawzi.DafcShubahTashbih `
	- *TAGS: CENT0600, _CAQAID, _MILAL*
 * `0597IbnJawzi.DafcShubahTashbih `
	- *TAGS: CENT0600, _HADITH, _SUNNI*
 * `0597IbnJawzi.DhammHawa `
	- *TAGS: CENT0600, _ADAB, _ADHKAR, _AKHLAQ, _MISC, _QISAS, _RAQAIQ, _SULUK, _TARAIF*
 * `0597IbnJawzi.DucafaWaMatrukin `
	- *TAGS: CENT0600, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0597IbnJawzi.FadailQuds `
	- *TAGS: CENT0600, _BULDAN, _JUGHRAFIYA, _RIHLAT, _TARIKH*
 * `0597IbnJawzi.FununAfnan `
	- *TAGS: CENT0600, _CULUM, _QURAN*
 * `0597IbnJawzi.GharibHadith `
	- *TAGS: CENT0600, _FIQH, _GHARIB, _HADITH, _MACAJIM, _MUSTALAHAT*
 * `0597IbnJawzi.HamqaWaMughallifin `
	- *TAGS: CENT0600, _ADAB, _ADAB, _BALAGHA, _QISAS, _TARAIF*
 * `0597IbnJawzi.Hathth `
	- *TAGS: CENT0600, _ADAB, _ADHKAR, _RAQAIQ*
 * `0597IbnJawzi.HifzCumr `
	- *TAGS: CENT0600, _ADAB, _ADHKAR, _RAQAIQ*
 * `0597IbnJawzi.IclamMacalim `
	- *TAGS: CENT0600, _CULUM, _HADITH*
 * `0597IbnJawzi.IkhbarAhlRusukh `
	- *TAGS: CENT0600, _HADITH, _SHARH*
 * `0597IbnJawzi.KashfMushkil `
	- *TAGS: CENT0600, _AHKAM, _CILAL, _HADITH, _MUSHKIL, _SHARH, _TARAJIM*
 * `0597IbnJawzi.Laali `
	- *TAGS: CENT0600, _ADAB, _ADHKAR, _MISC*
 * `0597IbnJawzi.Lataif `
	- *TAGS: CENT0600, _ADAB, _ADHKAR, _MISC*
 * `0597IbnJawzi.Manthur `
	- *TAGS: CENT0600, _ADAB, _ADHKAR, _QISAS, _TARAIF*
 * `0597IbnJawzi.Mashyakha `
	- *TAGS: BIO, CENT0600, PPE, _AJZA, _HADITH*
 * `0597IbnJawzi.Mawducat `
	- *TAGS: CENT0600, _CILAL, _DACIF, _HADITH, _MAWDUC, _SUALAT, _SUNNI, _TARAJIM*
 * `0597IbnJawzi.Mudhish `
	- *TAGS: CENT0600, _ADAB, _ADAB, _ADHKAR, _QISAS, _RAQAIQ, _TARAIF*
 * `0597IbnJawzi.Muntazam `
	- *TAGS: BIO, CENT0600, CHR, COL, DHB, PPE, _TARIKH*
 * `0597IbnJawzi.Muqliq `
	- *TAGS: CENT0600, _ADAB, _ADHKAR, _RAQAIQ*
 * `0597IbnJawzi.MusaffaBiAkuff `
	- *TAGS: CENT0600, _CULUM, _MANSUKH, _NASIKH, _QURAN, _TAFSIR*
 * `0597IbnJawzi.Musalsalat `
	- *TAGS: CENT0600, _HADITH, _MAKHTUTAT*
 * `0597IbnJawzi.MuthirGharam `
	- *TAGS: CENT0600, GEO, PPE, _BULDAN, _JUGHRAFIYA, _RIHLAT*
 * `0597IbnJawzi.NawasikhQuran `
	- *TAGS: CENT0600, _CULUM, _MANSUKH, _NASIKH, _QURAN, _SUNNI, _TAFSIR*
 * `0597IbnJawzi.NuzhatAcyun `
	- *TAGS: CENT0600, _FIQH, _QAWACID, _USUL*
 * `0597IbnJawzi.QussasWaMudhakkirin `
	- *TAGS: CENT0600, _CILAL, _DACIF, _HADITH, _MAWDUC, _SUALAT*
 * `0597IbnJawzi.SaydKhatir `
	- *TAGS: CENT0600, _ADAB, _ADAB, _ADHKAR, _QISAS, _RAQAIQ, _TARAIF*
 * `0597IbnJawzi.SifaSafwa `
	- *TAGS: BIO, CENT0600, COL, PPE, _ADAB, _ADHKAR, _FIQH, _MISC, _RAQAIQ, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `0597IbnJawzi.Tabsira `
	- *TAGS: CENT0600, _ADAB, _ADHKAR, _AKHLAQ, _MISC, _RAQAIQ, _SULUK*
 * `0597IbnJawzi.TaczimFutya `
	- *TAGS: CENT0600, _FIQH, _QAWACID, _USUL*
 * `0597IbnJawzi.TadhkiraFiWacz `
	- *TAGS: CENT0600, _ADAB, _ADHKAR, _AKHLAQ, _MISC, _RAQAIQ, _SULUK*
 * `0597IbnJawzi.TadhkiratArib `
	- *TAGS: CENT0600, _AHKAM, _GHARIB, _MACAJIM, _MUSTALAHAT, _QURAN, _TAFSIR*
 * `0597IbnJawzi.TahqiqFiAhadithKhilaf `
	- *TAGS: CENT0600, _FIQH, _HADITH, _TAKHRIJ, _TARAJIM*
 * `0597IbnJawzi.TalbisIblis `
	- *TAGS: CENT0600, _ADAB, _ADHKAR, _AKHLAQ, _CAQAID, _MISC, _RAQAIQ, _SULUK*
 * `0597IbnJawzi.TalqihFuhum `
	- *TAGS: CENT0600, PPE, _TARIKH*
 * `0597IbnJawzi.TanbihNaim `
	- *TAGS: CENT0600, _ADAB, _ADHKAR, _MISC, _RAQAIQ*
 * `0597IbnJawzi.TanwirGhabash `
	- *TAGS: CENT0600, _AJZA, _BUHUTH, _HADITH, _MASAIL, _TARAJIM*
 * `0597IbnJawzi.TarikhBaytMuqaddas `
	- *TAGS: CENT0600, PPE, _BULDAN, _TARIKH*
 * `0597IbnJawzi.ThibatCindaMamat `
	- *TAGS: CENT0600, _ADAB, _ADHKAR, _AKHLAQ, _CAQAID, _RAQAIQ*
 * `0597IbnJawzi.Yaquta `
	- *TAGS: CENT0600, _ADAB, _ADHKAR*
 * `0597IbnJawzi.ZadMasir `
	- *TAGS: CENT0600, _AHKAM, _CULUM, _QURAN, _SUNNI, _TAFSIR*
 * `0597IbnJawzi.ZirafWaMutamajinin `
	- *TAGS: CENT0600, _ADAB, _ADAB, _BALAGHA, _QISAS, _TARAIF*
 * `0599IbnYahyaDabbi.BughyaMultamis `
	- *TAGS: CENT0600, PPE, _TABAQAT, _TARAJIM*
 * `0600AbuBaqaHilli.ManaqibMazidiya `
	- *TAGS: CENT0600, _TARAJIM, _TARIKH*
 * `0600KatibMarrakushi.Istibsar `
	- *TAGS: CENT0600, _BULDAN, _JUGHRAFIYA, _RIHLAT*

* **0700AH [[ [Re]generated on 2016-10-22 (17:14:35) ]]**

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
 * `0635AbuMunajjaIbnLatti.Mashyakha `
	- *TAGS: CENT0700, _AJZA, _HADITH*
 * `0637IbnAthirDiyaDin.MathalSair `
	- *TAGS: CENT0700, _ADAB, _ADAB, _AMTHAL, _BALAGHA*
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
 * `0643IbnSalahShahrazuri.Fatawa `
	- *TAGS: CENT0700, _FIQH, _SHAFICI*
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
 * `0654SibtIbnJawzi.ItharInsaf `
	- *TAGS: CENT0700, _FIQH, _MASAIL, _QAWACID, _USUL, _USULIYYA*
 * `0656IbnAbiHadid.FalakDair `
	- *TAGS: CENT0700, _ADAB, _BALAGHA*
 * `0656IbnAbiHadid.RawdaMukhtara `
	- *TAGS: CENT0700, _IMAM, _NABI, _SIRA*
 * `0656IbnAbiHadid.SharhNahjBalagha `
	- *TAGS: CENT0700, _ADAB, _BALAGHA, _FASAHA, _HADITH, _SUNNI*
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
 * `0676Nawawi.AdabFatwa `
	- *TAGS: CENT0700, _FIQH, _MASAIL, _QAWACID, _USUL, _USULIYYA*
 * `0676Nawawi.Adhkar `
	- *TAGS: CENT0700, _ADAB, _ADHKAR, _AKHLAQ, _HADITH, _RAQAIQ, _SUNNI, _TAZKIYA*
 * `0676Nawawi.ArbacunaNawawiyya `
	- *TAGS: CENT0700, _ADAB, _ADHKAR, _RAQAIQ*
 * `0676Nawawi.BustanCarifin `
	- *TAGS: CENT0700, _ADAB, _ADHKAR, _AKHLAQ, _MISC, _RAQAIQ, _SULUK*
 * `0676Nawawi.DaqaiqMinhaj `
	- *TAGS: CENT0700, _FIQH, _SHAFICI*
 * `0676Nawawi.IctiqadSalafFiHuruf `
	- *TAGS: CENT0700, _CAQAID*
 * `0676Nawawi.IdahFiManasikHajj `
	- *TAGS: CENT0700, _FIQH*
 * `0676Nawawi.IjazFiSharhSunanAbiDawud `
	- *TAGS: CENT0700, _HADITH, _SHARH*
 * `0676Nawawi.KhulasatAhkam `
	- *TAGS: CENT0700, _HADITH, _TAKHRIJ, _TARAJIM*
 * `0676Nawawi.Majmuc `
	- *TAGS: CENT0700, _FIQH, _SHAFICI*
 * `0676Nawawi.MasailManthura `
	- *TAGS: CENT0700, _FATAWA*
 * `0676Nawawi.MinhajTalibin `
	- *TAGS: CENT0700, _FIQH, _SHAFICI*
 * `0676Nawawi.RawdatTalibin `
	- *TAGS: CENT0700, _FIQH, _SHAFICI*
 * `0676Nawawi.RiyadSalihin `
	- *TAGS: CENT0700, _ADAB, _ADHKAR, _AKHLAQ, _HADITH, _MAJMUCAT, _MISC, _RAQAIQ, _SUNNI, _TAZKIYA*
 * `0676Nawawi.RiyadSalihin `
	- *TAGS: CENT0700, _ALBANI*
 * `0676Nawawi.SharhArbacinaNawawi `
	- *TAGS: CENT0700, _HADITH, _SHARH, _TARAJIM*
 * `0676Nawawi.SharhMuslim `
	- *TAGS: CENT0700, _FIQH, _HADITH, _SHARH, _SUNNI, _TARAJIM*
 * `0676Nawawi.TahdhibAsma `
	- *TAGS: CENT0700, PPE, _GHARIB, _LUGHA, _MACAJIM, _MISC, _MUSTALAHAT, _TABAQAT, _TARAJIM*
 * `0676Nawawi.TahrirAlfaz `
	- *TAGS: CENT0700, _FIQH, _GHARIB, _LUGHA, _MACAJIM, _MUSTALAHAT*
 * `0676Nawawi.Taqrib `
	- *TAGS: CENT0700, _CULUM, _HADITH, _MUSTALAHAT*
 * `0676Nawawi.Tibyan `
	- *TAGS: CENT0700, _CULUM, _QURAN, _SUNNI, _TAFSIR*
 * `0676Nawawi.UsulWaDawabit `
	- *TAGS: CENT0700, _FIQH, _QAWACID, _USUL*
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
 * `0693IbnAbiFathIrbili.KashfGhumma `
	- *TAGS: CENT0700, PPE, _IMAM, _NABI, _SIRA*
 * `0694MuhibbDinTabari.Dhakhair `
	- *TAGS: CENT0700, PPE, _ASHAB, _HADITH, _SHAMAIL, _SHICI, _SIRA*
 * `0694MuhibbDinTabari.RiyadNadira `
	- *TAGS: CENT0700, PPE, _ASHAB, _SIRA, _TABAQAT, _TARAJIM*
 * `0695IbnCidhariMarrakushi.BayanMaghrib `
	- *TAGS: CENT0700, _BULDAN, _TARIKH*
 * `0696CumarSunami.NisabIhtisab `
	- *TAGS: CENT0800, _QADA, _SIYASA*
 * `0696Dabbagh.MacalimIman `
	- *TAGS: BIO, CENT0700, COL, ORPHAN, PPE*
 * `0696IbnZahiri.Mashyakha `
	- *TAGS: CENT0700, PPE, _AJZA, _HADITH, _TARAJIM*

* **0800AH [[ [Re]generated on 2016-10-22 (17:14:35) ]]**

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
 * `0728IbnTaymiyya.FatawaHamawiyya `
	- *TAGS: CENT0800, _IBNTAYMIYYA*
 * `0728IbnTaymiyya.FatawaKubra `
	- *TAGS: CENT0800, _FIQH, _HANBALI, _IBNTAYMIYYA*
 * `0728IbnTaymiyya.MajmucFatawa `
	- *TAGS: CENT0800, _FIQH, _HANBALI, _IBNTAYMIYYA*
 * `0728IbnTaymiyya.MustadrakCalaMajmucFatawa `
	- *TAGS: CENT0800, _IBNTAYMIYYA*
 * `0728IbnTaymiyya.RasHusayn `
	- *TAGS: CENT0800, _IBNTAYMIYYA, _IMAM, _NABI, _SIRA, _TARIKH*
 * `0728IbnTaymiyya.RasailWaFatawa `
	- *TAGS: CENT0800, _FIQH, _HANBALI, _CAQAID, _MILAL, _HADITH, _MUSTALAHAT*
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
 * `0734IbnQaddahHarawi.MulhaqFatawa `
	- *TAGS: CENT0800, _BUHUTH, _FIQH, _MASAIL*
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
 * `0748Dhahabi.AhadithMukhtaraMinMawducat `
	- *TAGS: CENT0800, _CILAL, _DACIF, _HADITH, _MAWDUC, _SUALAT*
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
 * `0748Dhahabi.TalkhisMawducatIbnJawzi `
	- *TAGS: CENT0800, _CILAL, _DACIF, _HADITH, _MAWDUC, _SUALAT*
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
 * `0751IbQayyimJawziyya.AclamMuwaqqicin `
	- *TAGS: CENT0800, _FIQH, _IBNQAYYIM, _USUL*
 * `0751IbQayyimJawziyya.AhkamAhlDhimma `
	- *TAGS: CENT0800, _FIQH, _IBNQAYYIM, _MASAIL, _USUL*
 * `0751IbQayyimJawziyya.AmthalFiQuran `
	- *TAGS: CENT0800, _CULUM, _IBNQAYYIM, _QURAN, _SUNNI, _TAFSIR*
 * `0751IbQayyimJawziyya.BadaicFawaid `
	- *TAGS: CENT0800, _AKHLAQ, _IBNQAYYIM, _SULUK, _TAZKIYA*
 * `0751IbQayyimJawziyya.CuddatSabirin `
	- *TAGS: CENT0800, _AKHLAQ, _IBNQAYYIM, _SULUK, _TAZKIYA*
 * `0751IbQayyimJawziyya.DaWaDawa `
	- *TAGS: CENT0800, _AKHLAQ, _IBNQAYYIM, _SULUK, _TAZKIYA*
 * `0751IbQayyimJawziyya.FaidaJalila `
	- *TAGS: CENT0800, _IBNQAYYIM*
 * `0751IbQayyimJawziyya.Fawaid `
	- *TAGS: CENT0800, _AKHLAQ, _IBNQAYYIM, _QISAS, _SULUK, _TARAIF, _TAZKIYA*
 * `0751IbQayyimJawziyya.Furusiyya `
	- *TAGS: CENT0800, _FIQH, _IBNQAYYIM, _MASAIL, _USUL*
 * `0751IbQayyimJawziyya.HadiArwah `
	- *TAGS: CENT0800, _AKHLAQ, _IBNQAYYIM, _SULUK, _TAZKIYA*
 * `0751IbQayyimJawziyya.HidayatHayara `
	- *TAGS: CENT0800, _CAQAID, _FIRAQ, _IBNQAYYIM, _MILAL*
 * `0751IbQayyimJawziyya.IghathatLahfan `
	- *TAGS: CENT0800, _AKHLAQ, _IBNQAYYIM, _SULUK, _TAZKIYA*
 * `0751IbQayyimJawziyya.IjtimacJuyush `
	- *TAGS: CENT0800, _CAQAID, _IBNQAYYIM, _MILAL, _RUDUD*
 * `0751IbQayyimJawziyya.JalaAfham `
	- *TAGS: CENT0800, _AKHLAQ, _IBNQAYYIM, _SULUK, _TAZKIYA*
 * `0751IbQayyimJawziyya.JawabFiSiyaghHamd `
	- *TAGS: CENT0800, _AKHLAQ, _IBNQAYYIM, _SULUK, _TAZKIYA*
 * `0751IbQayyimJawziyya.MadarijSalikin `
	- *TAGS: CENT0800, _AKHLAQ, _IBNQAYYIM, _SULUK, _TAZKIYA*
 * `0751IbQayyimJawziyya.ManarMunif `
	- *TAGS: CENT0800, _DACIF, _HADITH, _IBNQAYYIM, _MAWDUC*
 * `0751IbQayyimJawziyya.MatnQasidaNuniyya `
	- *TAGS: CENT0800, _IBNQAYYIM*
 * `0751IbQayyimJawziyya.MiftahDarSacada `
	- *TAGS: CENT0800, _AKHLAQ, _IBNQAYYIM, _SULUK, _TAZKIYA*
 * `0751IbQayyimJawziyya.MukhtasarSawaciqMursala `
	- *TAGS: CENT0800, _IBNQAYYIM*
 * `0751IbQayyimJawziyya.RawdatMuhibbin `
	- *TAGS: CENT0800, _AKHLAQ, _IBNQAYYIM, _SULUK, _TAZKIYA*
 * `0751IbQayyimJawziyya.RisalaIlaAhadIkhwan `
	- *TAGS: CENT0800, _IBNQAYYIM, _TARAJIM, _TARIKH*
 * `0751IbQayyimJawziyya.RisalaTabukiyya `
	- *TAGS: CENT0800, _AKHLAQ, _IBNQAYYIM, _SULUK, _TAZKIYA*
 * `0751IbQayyimJawziyya.RuhFiKalam `
	- *TAGS: CENT0800, _CAQAID, _IBNQAYYIM, _MILAL*
 * `0751IbQayyimJawziyya.Salat `
	- *TAGS: CENT0800, _IBNQAYYIM*
 * `0751IbQayyimJawziyya.SawaciqMursala `
	- *TAGS: CENT0800, _CAQAID, _IBNQAYYIM, _MILAL, _RUDUD*
 * `0751IbQayyimJawziyya.ShifaCalil `
	- *TAGS: CENT0800, _CAQAID, _IBNQAYYIM, _MILAL*
 * `0751IbQayyimJawziyya.SifatMunafiqin `
	- *TAGS: CENT0800, _IBNQAYYIM*
 * `0751IbQayyimJawziyya.TafsirQuran `
	- *TAGS: CENT0800, _TAFSIR*
 * `0751IbQayyimJawziyya.TariqHijratayn `
	- *TAGS: CENT0800, _AKHLAQ, _IBNQAYYIM, _SULUK, _TAZKIYA*
 * `0751IbQayyimJawziyya.TibbNabawi `
	- *TAGS: CENT0800, _ASHAB, _IBNQAYYIM, _SIRA, _TIBB*
 * `0751IbQayyimJawziyya.TibyanFiAqsamQuran `
	- *TAGS: CENT0800, _CULUM, _IBNQAYYIM, _QURAN, _TAFSIR*
 * `0751IbQayyimJawziyya.TuhfatMawdud `
	- *TAGS: CENT0800, _FIQH, _IBNQAYYIM, _MASAIL, _USUL*
 * `0751IbQayyimJawziyya.TuruqHukmiyya `
	- *TAGS: CENT0800, _FIQH, _IBNQAYYIM, _MASAIL, _SIYASA, _USUL*
 * `0751IbQayyimJawziyya.WabilSayyib `
	- *TAGS: CENT0800, _AKHLAQ, _HADITH, _IBNQAYYIM, _MAJMUCAT, _SULUK, _TAZKIYA*
 * `0751IbQayyimJawziyya.ZadMacad `
	- *TAGS: CENT0800, _ASHAB, _IBNQAYYIM, _SIRA*
 * `0751IbnQayyimJawziya.AsmaMuallafatIbnTaymiya `
	- *TAGS: CENT0800, _FAHARIS, _IBNTAYMIYYA, _KUTUB*
 * `0751IbnQayyimJawziyya.IghathaLahfan `
	- *TAGS: CENT0800, SBS, _FIQH, _IBNQAYYIM, _MASAIL, _USUL*
 * `0756TaqiDinSubki.Fatawa `
	- *TAGS: CENT0800, _FATAWA, _FIQH, _SHAFICI*
 * `0756TaqiDinSubki.Ibhaj `
	- *TAGS: CENT0800, _FIQH, _QAWACID, _USUL*
 * `0756TaqiDinSubki.IbrazHikam `
	- *TAGS: CENT0800, _HADITH, _SHARH, _TARAJIM*
 * `0761IbnKaykaldi.JamicTahsil `
	- *TAGS: CENT0800, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0761IbnKaykaldi.Mukhtalitin `
	- *TAGS: CENT0800, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0761IbnKaykaldiDimashqi.ItharatFawaid `
	- *TAGS: CENT0800, _AJZA, _HADITH*
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
 * `0774IbnKathir.AdabDukhulHammam `
	- *TAGS: CENT0800, _BUHUTH, _FIQH, _MASAIL, _MISC, _USUL*
 * `0774IbnKathir.Bidaya `
	- *TAGS: BIO, CENT0800, CHR, COL, PPE, _ASHAB, _IMAM, _NABI, _SHAMAIL, _SIRA, _TARIKH*
 * `0774IbnKathir.FadailQuran `
	- *TAGS: CENT0800, _CULUM, _QURAN, _TAFSIR*
 * `0774IbnKathir.FusulMinSira `
	- *TAGS: CENT0800, _ASHAB, _SHAMAIL, _SIRA*
 * `0774IbnKathir.IkhtisarCulumHadith `
	- *TAGS: CENT0800, _CULUM, _HADITH*
 * `0774IbnKathir.JamicMasanid `
	- *TAGS: CENT0800, _HADITH, _TAKHRIJ*
 * `0774IbnKathir.MusnadCumarIbnKhattab `
	- *TAGS: CENT0800, _HADITH*
 * `0774IbnKathir.NihayatFiFitan `
	- *TAGS: CENT0800, _ADAB, _ADHKAR, _CAQAID, _MILAL, _RAQAIQ*
 * `0774IbnKathir.QisasAnbiya `
	- *TAGS: CENT0800, _IMAM, _NABI, _SHAMAIL, _SIRA*
 * `0774IbnKathir.SharhIkhtisarCulumHadith `
	- *TAGS: CENT0800, _CULUM, _HADITH*
 * `0774IbnKathir.TabaqatShaficiyyin `
	- *TAGS: BIO, CENT0800, COL, PPE, _TABAQAT, _TARAJIM*
 * `0774IbnKathir.TafsirQuran `
	- *TAGS: CENT0800, _AHKAM, _CULUM, _HADITH, _QURAN, _SUNNI, _TAFSIR*
 * `0774IbnKathir.Takmil `
	- *TAGS: CENT0800, PPE, _TABAQAT, _TARAJIM*
 * `0774IbnKathir.TalkhisKitabIstighatha `
	- *TAGS: CENT0800, _CAQAID, _MILAL*
 * `0774IbnKathir.TuhfatTalib `
	- *TAGS: CENT0800, _FIQH, _HADITH, _TAKHRIJ, _TARAJIM*
 * `0774IbnKathir.TuhfatTalib `
	- *TAGS: CENT0800, _HADITH, _TAKHRIJ*
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
 * `0777BadrDinBacli.MukhtasarFatawaMisriyya `
	- *TAGS: CENT0800, _FATAWA, _FIQH, _HANBALI*
 * `0779IbnBattuta.Rihla `
	- *TAGS: CENT0800, GEO, PPE, _BULDAN, _JUGHRAFIYA, _MUDHAKKARAT, _RIHLAT, _TARIKH*
 * `0782IbnSallar.TabaqatQurra `
	- *TAGS: BIO, CENT0800, PPE, _QIRAAT, _QURAN, _TAJWID*
 * `0789IbnMuhammadKhuzaci.TakhrijDalalat `
	- *TAGS: CENT0800, _QADA, _SIYASA*
 * `0793AbuHasanMalaqi.TarikhQudat `
	- *TAGS: CENT0800, PPE, _TABAQAT, _TARAJIM, _TARIKH*
 * `0795IbnRajabHanbali.DhaylTabaqatHanabila `
	- *TAGS: BIO, CENT0800, COL, PPE, _TABAQAT, _TARAJIM, _TARIKH*
 * `0799IbnFarhun.DibajMudhahhab `
	- *TAGS: CENT0800, PPE, _FIQH, _TABAQAT, _TARAJIM, _TARIKH*

* **0900AH [[ [Re]generated on 2016-10-22 (17:14:35) ]]**

 * `0802IbnMusaAbnasi.ShadhaFayyah `
	- *TAGS: CENT0900, _CULUM, _HADITH, _MUSTALAHAT*
 * `0804IbnMulaqqin.BadrMunir `
	- *TAGS: CENT0900, _HADITH, _TAKHRIJ, _TARAJIM*
 * `0804IbnMulaqqin.TabaqatAwliya `
	- *TAGS: CENT0900, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `0804IbnMulaqqin.TuhfaMuhtaj `
	- *TAGS: CENT0900, _FIQH, _HADITH, _TAKHRIJ, _TARAJIM*
 * `0806IbnHusaynCiraqi.Alfiyya `
	- *TAGS: CENT0900, _CULUM, _HADITH*
 * `0806IbnHusaynCiraqi.AlfiyyatSira `
	- *TAGS: CENT0900, _SHAMAIL, _SIRA*
 * `0806IbnHusaynCiraqi.ArbacunaCushariyya `
	- *TAGS: CENT0900, _AJZA, _HADITH, _SUNNI, _TARAJIM*
 * `0806IbnHusaynCiraqi.DhaylMizan `
	- *TAGS: BIO, CENT0900, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0806IbnHusaynCiraqi.MustakhrajCalaMustadrak `
	- *TAGS: CENT0900, _AJZA, _HADITH, _MISC, _MUSTALAHAT, _SUNNI*
 * `0806IbnHusaynCiraqi.SharhAlfiyya `
	- *TAGS: CENT0900, _CULUM, _HADITH*
 * `0806IbnHusaynCiraqi.Taqyid `
	- *TAGS: CENT0700, CENT0900, _CHRONOMULTIPLE, _CULUM, _HADITH, _MUSTALAHAT, _SUNNI*
 * `0806IbnHusaynCiraqi.TarhTarthib `
	- *TAGS: CENT0900, _HADITH, _SHARH, _TARAJIM*
 * `0807IbnAhmarKhazraji.NafhaNisriniyya `
	- *TAGS: CENT0900, PPE, _BULDAN, _TARIKH*
 * `0807NurDinHaythami.GhayatMaqsad `
	- *TAGS: CENT0900, _HADITH, _TAKHRIJ*
 * `0807NurDinHaythami.KashfAstar `
	- *TAGS: CENT0900, _HADITH, _TAKHRIJ*
 * `0807NurDinHaythami.MaqsadAli `
	- *TAGS: CENT0900, _HADITH*
 * `0807NurDinHaythami.MawaridZaman `
	- *TAGS: CENT0900, _HADITH, _SAHIH, _SUNNI, _TARAJIM*
 * `0807NurDinHaythami.MucjamZawaid `
	- *TAGS: CENT0900, _FIQH, _HADITH, _MAJMUCAT, _SUNNI, _TAKHRIJ, _TARAJIM*
 * `0808IbnKhaldun.Rihla `
	- *TAGS: CENT0900, GEO, PPE, _BULDAN, _JUGHRAFIYA, _RIHLAT*
 * `0808IbnKhaldun.Tarikh `
	- *TAGS: CENT0900, CHR, PPE, _MISC, _TARIKH*
 * `0808MuhammadDamiri.HayatHayawanKubra `
	- *TAGS: CENT0900, _ADAB, _BALAGHA, _CULUM, _TIBB*
 * `0809IbnQunfudh.Wafayat `
	- *TAGS: CENT0900, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `0812CaliKhazraji.CuqudLuluiyya `
	- *TAGS: CENT0900, PPE, _TARIKH*
 * `0815IbnCabdAllahGhazuli.MatalicBudur `
	- *TAGS: CENT0900, _ADAB, _BALAGHA*
 * `0816AbuBakrMaraghi.Mashyakha `
	- *TAGS: CENT0900, PPE, _AJZA, _HADITH*
 * `0817Firuzabadi.QamusMuhit `
	- *TAGS: CENT0900, _FIQH, _GHARIB, _LUGHA, _MACAJIM, _MUSTALAHAT, _NAHW, _SARF*
 * `0817Firuzabadi.TanwirMiqbas `
	- *TAGS: CENT0100, CENT0900, _CHRONOMULTIPLE, _CULUM, _QURAN, _SUNNI, _TAFSIR*
 * `0817IbnYacqubFiruzabadi.BulghaFiTarajim `
	- *TAGS: CENT0900, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `0821Qalqashandi.Maathir `
	- *TAGS: CENT0900, _MISC, _QADA, _SIYASA*
 * `0821Qalqashandi.NihayaArab `
	- *TAGS: CENT0900, PPE, _ANSAB*
 * `0821Qalqashandi.QalaidJuman `
	- *TAGS: CENT0900, PPE, _ANSAB, _BULDAN, _TARIKH*
 * `0821Qalqashandi.SubhAcsha `
	- *TAGS: CENT0900, _ADAB, _ADAB, _BALAGHA, _CARUD, _KITABA*
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
 * `0833IbnJazari.Cawali `
	- *TAGS: CENT0900, _HADITH, _MAKHTUTAT*
 * `0833IbnJazari.DurraMudiyya `
	- *TAGS: CENT0900, _CULUM, _QIRAAT, _QURAN, _TAFSIR*
 * `0833IbnJazari.GhayaNihaya `
	- *TAGS: CENT0900, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `0833IbnJazari.ManaqibAsadGhalib `
	- *TAGS: CENT0900, _AJZA, _HADITH*
 * `0833IbnJazari.ManaqibAsadGhalib `
	- *TAGS: CENT0900, _MISC*
 * `0833IbnJazari.ManzumaJazariyya `
	- *TAGS: CENT0900, _CULUM, _QURAN*
 * `0833IbnJazari.MatnTayyibaNashr `
	- *TAGS: CENT0900, _CULUM, _QURAN*
 * `0833IbnJazari.MunjidMuqriyyin `
	- *TAGS: CENT0900, _CULUM, _QURAN*
 * `0833IbnJazari.Nashr `
	- *TAGS: CENT0900, _CULUM, _QURAN*
 * `0833IbnJazari.SharhTayyibaNashr `
	- *TAGS: CENT0900, _QIRAAT, _QURAN, _TAJWID*
 * `0833IbnJazari.TahbirTaysir `
	- *TAGS: CENT0900, _CULUM, _QURAN, _TAFSIR*
 * `0833IbnJazari.TamhidFiCulumTajwid `
	- *TAGS: CENT0900, _CULUM, _QURAN*
 * `0833IbnJazari.ZahrFaih `
	- *TAGS: CENT0900, PPE, _ADAB, _ADHKAR, _RAQAIQ, _TARAJIM, _TARIKH*
 * `0842IbnNasirDinDimashqi.RaddWafir `
	- *TAGS: CENT0900, PPE, _TABAQAT, _TARAJIM, _TARIKH*
 * `0842IbnNasirDinDimashqi.TawdihMushtabih `
	- *TAGS: CENT0900, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0845Maqrizi.Bayan `
	- *TAGS: CENT0900, _BULDAN, _TARIKH*
 * `0845Maqrizi.ImtacAsmac `
	- *TAGS: CENT0900, _SHAMAIL, _SIRA, _TARIKH*
 * `0845Maqrizi.IqazHunafa `
	- *TAGS: CENT0900, PPE, _BULDAN, _TARIKH*
 * `0845Maqrizi.Mawaciz `
	- *TAGS: CENT0900, PPE, _BULDAN, _JUGHRAFIYA, _RIHLAT*
 * `0845Maqrizi.MukhtasarKamil `
	- *TAGS: CENT0900, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0845Maqrizi.Suluk `
	- *TAGS: CENT0900, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `0848IbnSarrajAndalusi.Fatawa `
	- *TAGS: CENT0900, _FATAWA*
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
 * `0852IbnHajarCasqalani.MasailAjabaCanha `
	- *TAGS: CENT0900, _FATAWA*
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
 * `0855Cayni.SharhSunanAbiDawud `
	- *TAGS: CENT0900, _HADITH, _SHARH*
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
 * `0893IbnAbiBakrHadari.BahjatMahafil `
	- *TAGS: CENT0900, PPE, _SHAMAIL, _SIRA*
 * `0900AbuCabdAllahHimyari.RawdMictar `
	- *TAGS: CENT0900, COL, GEO, PPE, _BULDAN, _GHARIB, _JUGHRAFIYA, _MACAJIM, _MUSTALAHAT, _RIHLAT*

* **1000AH [[ [Re]generated on 2016-10-22 (17:14:35) ]]**

 * `0902Sakhawi.Buldaniyyat `
	- *TAGS: CENT1000, PPE, _AJZA, _HADITH, _MISC, _TARAJIM*
 * `0902Sakhawi.DuLamic `
	- *TAGS: BIO, CENT1000, COL, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `0902Sakhawi.FathMughith `
	- *TAGS: CENT1000, _CULUM, _HADITH, _MUSTALAHAT*
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
 * `0911Suyuti.Ashbah `
	- *TAGS: CENT1000, _FIQH, _MASAIL, _QAWACID, _USUL, _USULIYYA*
 * `0911Suyuti.AsmaMudallisin `
	- *TAGS: CENT1000, PPE, _HADITH, _MUSTALAHAT, _TABAQAT, _TARAJIM*
 * `0911Suyuti.AsmaMukhadramin `
	- *TAGS: CENT1000, PPE, _TARAJIM, _TARIKH*
 * `0911Suyuti.BastKaff `
	- *TAGS: CENT1000, _BUHUTH, _FIQH, _MASAIL, _USUL*
 * `0911Suyuti.BughyaWucat `
	- *TAGS: BIO, CENT1000, COL, PPE, _TABAQAT, _TARAJIM, _TARIKH*
 * `0911Suyuti.DafcTashnic `
	- *TAGS: CENT1000, _BUHUTH, _FIQH, _MASAIL, _USUL*
 * `0911Suyuti.DhaylTabaqatHuffaz `
	- *TAGS: CENT1000, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `0911Suyuti.DibajCalaMuslim `
	- *TAGS: CENT1000, _FIQH, _HADITH, _SHARH, _SUNNI, _TARAJIM*
 * `0911Suyuti.DurrManthur `
	- *TAGS: CENT1000, _CULUM, _HADITH, _QURAN, _SUNNI, _TAFSIR*
 * `0911Suyuti.FaddWica `
	- *TAGS: CENT1000, _BUHUTH, _FIQH, _MASAIL, _USUL*
 * `0911Suyuti.GhurarFiFadailCumar `
	- *TAGS: CENT1000, PPE, _ASHAB, _SIRA, _TABAQAT, _TARAJIM*
 * `0911Suyuti.HawiLiFatawa `
	- *TAGS: CENT1000, _FATAWA, _FIQH, _SHAFICI*
 * `0911Suyuti.HusnMuhadara `
	- *TAGS: CENT1000, PPE, _BULDAN, _TARIKH*
 * `0911Suyuti.IscafMubatta `
	- *TAGS: CENT1000, PPE, _HADITH, _TABAQAT, _TARAJIM*
 * `0911Suyuti.ItmamDiraya `
	- *TAGS: CENT1000, _ADILLA, _FAHARIS, _KUTUB*
 * `0911Suyuti.Itqan `
	- *TAGS: CENT1000, _CULUM, _QURAN, _SUNNI, _TAFSIR*
 * `0911Suyuti.KhasaisKubra `
	- *TAGS: CENT1000, _ASHAB, _SHAMAIL, _SIRA*
 * `0911Suyuti.LaaliMasnuca `
	- *TAGS: CENT1000, _CILAL, _DACIF, _HADITH, _MAWDUC, _SUALAT*
 * `0911Suyuti.LubabNuqul `
	- *TAGS: CENT1000, _CULUM, _QURAN, _SUNNI, _TAFSIR*
 * `0911Suyuti.LubbLubab `
	- *TAGS: CENT1000, PPE, _ANSAB, _TARAJIM, _TARIKH*
 * `0911Suyuti.LumacFiAsbabHadith `
	- *TAGS: CENT1000, _HADITH, _MISC, _MUSTALAHAT, _SHARH*
 * `0911Suyuti.LumcaFiKhasaisJumca `
	- *TAGS: CENT1000, _BUHUTH, _FIQH, _MASAIL, _USUL*
 * `0911Suyuti.ManahilSafa `
	- *TAGS: CENT1000, _HADITH, _TAKHRIJ*
 * `0911Suyuti.MiftahJanna `
	- *TAGS: CENT1000, _CULUM, _FIQH, _HADITH, _MASAIL, _MUSTALAHAT, _USUL*
 * `0911Suyuti.Muhadarat `
	- *TAGS: CENT1000, _ADAB, _BALAGHA*
 * `0911Suyuti.MuzhirFiCulumLugha `
	- *TAGS: CENT1000, _ADAB, _LUGHA, _MISC, _QISAS, _TARAIF*
 * `0911Suyuti.NawahidAbkar `
	- *TAGS: CENT1000, _TAFSIR*
 * `0911Suyuti.NazmCiqyan `
	- *TAGS: CENT1000, PPE, _TABAQAT, _TARAJIM, _TARIKH*
 * `0911Suyuti.NuzhatJulasa `
	- *TAGS: CENT1000, _ADAB, _ADAB, _BALAGHA, _SHICR*
 * `0911Suyuti.QutMughtadhi `
	- *TAGS: CENT1000, _HADITH, _SHARH*
 * `0911Suyuti.RawdAniqFiFadlSiddiq `
	- *TAGS: CENT0900, CENT1000, _ASHAB, _CHRONOMULTIPLE, _SIRA, _TABAQAT, _TARAJIM*
 * `0911Suyuti.RihNisrin `
	- *TAGS: CENT1000, PPE, _HADITH, _MISC, _TABAQAT, _TARAJIM*
 * `0911Suyuti.SababWadc `
	- *TAGS: CENT1000, _MISC, _NAHW, _SARF*
 * `0911Suyuti.ShamailSharifa `
	- *TAGS: CENT1000, _ASHAB, _SHAMAIL, _SIRA*
 * `0911Suyuti.Shamarikh `
	- *TAGS: CENT1000, _MISC, _TARIKH*
 * `0911Suyuti.SharhSudur `
	- *TAGS: CENT1000, _CAQAID, _MILAL*
 * `0911Suyuti.SharhSunanIbnMaja `
	- *TAGS: CENT1000, _HADITH, _SHARH, _TARAJIM*
 * `0911Suyuti.TabaqatHuffaz `
	- *TAGS: BIO, CENT1000, COL, PPE, _HADITH, _TABAQAT, _TARAJIM, _THIQAT*
 * `0911Suyuti.TabaqatMufassirin `
	- *TAGS: CENT1000, PPE, _MUFASSIRUN, _TABAQAT, _TARAJIM, _TARIKH*
 * `0911Suyuti.TadhkiratMutasi `
	- *TAGS: CENT1000, _CULUM, _HADITH, _MUSTALAHAT*
 * `0911Suyuti.TadribRawi `
	- *TAGS: CENT1000, _CULUM, _HADITH, _MUSTALAHAT*
 * `0911Suyuti.TafsirJalalayn `
	- *TAGS: CENT0900, CENT1000, _CHRONOMULTIPLE, _CULUM, _QURAN, _SUNNI, _TAFSIR*
 * `0911Suyuti.TahdhirKhawass `
	- *TAGS: CENT1000, _CILAL, _DACIF, _HADITH, _MAWDUC, _SUALAT*
 * `0911Suyuti.TakrirIstinad `
	- *TAGS: CENT1000, _FIQH, _MASAIL, _QAWACID, _USUL, _USULIYYA*
 * `0911Suyuti.TanwirHawalik `
	- *TAGS: CENT1000, _HADITH, _SHARH, _TARAJIM*
 * `0911Suyuti.TarikhKhulafa `
	- *TAGS: CENT1000, PPE, _BULDAN, _TARAJIM, _TARIKH*
 * `0911Suyuti.Tatrif `
	- *TAGS: CENT1000, _CULUM, _HADITH, _MISC, _MUSTALAHAT*
 * `0922IbnShaykhTarabulusi.IscafAwqaf `
	- *TAGS: CENT1000, PPE, _BUHUTH, _MASAIL*
 * `0923AhmadQastallani.IrshadSari `
	- *TAGS: CENT1000, _HADITH, _SHARH*
 * `0923IbnCabdAllahKhazraji.KhulasaTahdhib `
	- *TAGS: CENT1000, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0926ZakariyaAnsari.HududCaniqa `
	- *TAGS: CENT1000, _FAHARIS, _FIQH, _GHARIB, _MACAJIM, _MUSTALAHAT*
 * `0927Culaymi.UnsJalil `
	- *TAGS: CENT1000, PPE, _BULDAN, _TARIKH*
 * `0927Nucaymi.DarisFiMadaris `
	- *TAGS: CENT1000, COL, PPE, _MISC, _TARIKH*
 * `0929IbnKayyal.KawakibNayyirat `
	- *TAGS: CENT1000, PPE, _HADITH, _SUNNI, _TABAQAT, _TARAJIM*
 * `0938IbnCaliBalawi.Thabat `
	- *TAGS: BIB, CENT1000, PPE, _ADILLA, _FAHARIS, _KUTUB*
 * `0942IbnYusufShami.SubulHuda `
	- *TAGS: CENT1000, _ASHAB, _IMAM, _NABI, _SHAMAIL, _SIRA*
 * `0945ShamsDinDawudi.TabaqatMufassirin `
	- *TAGS: CENT1000, PPE, _TABAQAT, _TARAJIM*
 * `0953IbnTulun.MufakahaKhillan `
	- *TAGS: CENT1000, PPE, _BULDAN, _TARIKH*
 * `0957ShihabDinRamli.FatawaRamli `
	- *TAGS: CENT1000, _CHRONOMULTIPLE, _FATAWA, _FIQH, _SHAFICI*
 * `0966HusaynDiyarbakri.TarikhKhamis `
	- *TAGS: CENT1000, _SHAMAIL, _SIRA*
 * `0968Tashkubruizadah.ShaqaiqNucmaniyya `
	- *TAGS: BIO, CENT1000, COL, PPE, _FIQH, _TABAQAT, _TARAJIM, _TARIKH*
 * `0973CabdWahhabShacrani.LawaqihAnwar `
	- *TAGS: CENT1000, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `0973IbnHajarHaythami.FatawaHadithiyya `
	- *TAGS: CENT1000, _FATAWA, _FIQH, _SHAFICI*
 * `0973IbnHajarHaythami.FatawaKubra `
	- *TAGS: CENT1000, _FATAWA, _FIQH, _SHAFICI*
 * `0978QasimQunawi.AnisFuqaha `
	- *TAGS: CENT1000, _FIQH, _GHARIB, _LUGHA, _MACAJIM, _MUSTALAHAT*
 * `0984BardDinGhazzi.MatalicBadriya `
	- *TAGS: CENT1000, _BULDAN, _JUGHRAFIYA, _RIHLAT*

* **1100AH [[ [Re]generated on 2016-10-22 (17:14:35) ]]**

 * `1004ShamsDinRamli.FatawaRamli `
	- *TAGS: CENT1100, _CHRONOMULTIPLE, _FATAWA, _FIQH, _SHAFICI*
 * `1010TamimiDari.TabaqatSaniya `
	- *TAGS: BIO, CENT1100, COL, PPE, _TABAQAT, _TARAJIM, _TARIKH*
 * `1011SahibMacalim.TahrirTawusi `
	- *TAGS: CENT1100, PPE, SHC, _HADITH, _SHICI, _TARAJIM*
 * `1014IbnSultanHarawi.Adilla `
	- *TAGS: CENT1100, _CAQAID, _MILAL*
 * `1014IbnSultanHarawi.AhadithQudsiyya `
	- *TAGS: CENT1100, _HADITH, _TAKHRIJ*
 * `1014IbnSultanHarawi.AhadithQudsiyya `
	- *TAGS: CENT1100, _HADITH, _TAKHRIJ*
 * `1014IbnSultanHarawi.AsrarMarfuca `
	- *TAGS: CENT1100, _CILAL, _DACIF, _HADITH, _MAWDUC, _SUALAT*
 * `1014IbnSultanHarawi.FaydMucin `
	- *TAGS: CENT1100, _CULUM, _FIQH, _HANAFI, _QURAN*
 * `1014IbnSultanHarawi.JamcWasail `
	- *TAGS: CENT1100, _SHAMAIL, _SIRA*
 * `1014IbnSultanHarawi.MirqatMafatih `
	- *TAGS: CENT1100, _HADITH, _SHARH, _TARAJIM*
 * `1014IbnSultanHarawi.RaddCalaQailinBiWahdatWujud `
	- *TAGS: CENT1100, _CAQAID, _MILAL, _RUDUD*
 * `1014IbnSultanHarawi.ShammCawarid `
	- *TAGS: CENT1100, _CAQAID*
 * `1014IbnSultanHarawi.SharhMusnadAbiHanifa `
	- *TAGS: CENT1100, _HADITH, _SHARH, _SUNNI, _TARAJIM*
 * `1014IbnSultanHarawi.SharhShifa `
	- *TAGS: CENT1100, _SHAMAIL, _SIRA*
 * `1014IbnSultanHarawi.TasliyyatAcma `
	- *TAGS: CENT1100, _ADAB, _ADHKAR, _RAQAIQ*
 * `1016MuhibbDinHamawi.HadiAzcan `
	- *TAGS: CENT1100, GEO, PPE, _BULDAN, _JUGHRAFIYA, _MISC, _RIHLAT*
 * `1031CabdRaufMunawi.Tawqif `
	- *TAGS: CENT1100, _FAHARIS, _FIQH, _GHARIB, _MACAJIM, _MUSTALAHAT*
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
 * `1057IbnCallan.DalilFalihin `
	- *TAGS: CENT1100, _HADITH, _SHARH*
 * `1057IbnCallan.DalilFalihin `
	- *TAGS: CENT1100, _HADITH, _SHARH, _TARAJIM*
 * `1057IbnCallan.IthafFadil `
	- *TAGS: CENT1100, _MISC, _NAHW, _SARF*
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
 * `1090NizamDinBalkhi.FatawaHindiyya `
	- *TAGS: _CENT00NO, _FATAWA, _FIQH, _HANAFI*
 * `1093CabdQadirBaghdadi.KhizanatAdab `
	- *TAGS: CENT1100, _ADAB, _ADAB, _BALAGHA, _FASAHA, _SHICR*
 * `1100IbnMuhammadAdnahwi.TabaqatMufassirin `
	- *TAGS: CENT1100, PPE, _MUFASSIRUN, _TABAQAT, _TARAJIM, _TARIKH*
 * `1100MuhammadItlidi.IclamNas `
	- *TAGS: CENT1100, _BULDAN, _TARIKH*
 * `1100MustafaTafrishi.NaqdRijal `
	- *TAGS: BIO, CENT1100, PPE, SHC, _HADITH, _SHICI, _TARAJIM*

* **1200AH [[ [Re]generated on 2016-10-22 (17:14:35) ]]**

 * `1101MuhammadCaliArdabili.JamicRuwat `
	- *TAGS: CENT1200, PPE, SHC, _HADITH, _SHICI, _TARAJIM*
 * `1107HashimBahrani.GhayatMaram `
	- *TAGS: CENT1200, _CAQAID, _SHICI, _TWELVERS*
 * `1111MuhammadAminMuhibbi.KhulasaAthr `
	- *TAGS: CENT1200, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `1119IbnMacsum.SulafaCasr `
	- *TAGS: BIO, CENT1200, PPE, _TABAQAT, _TARAJIM, _TARIKH*
 * `1120CaliKhanMadani.DarajatRafica `
	- *TAGS: CENT1200, PPE, SHC, _HADITH, _SHICI, _TARAJIM*
 * `1122MuhammadZarqani.SharhCalaMawahib `
	- *TAGS: CENT1200, PPE, _SHAMAIL, _SIRA*
 * `1122MuhammadZarqani.SharhCalaMuwatta `
	- *TAGS: CENT1200, _FIQH, _HADITH, _MALIKI, _SHARH, _TARAJIM*
 * `1126MuhammadHanbali.Mashyakha `
	- *TAGS: CENT1200, PPE, _TABAQAT, _TARAJIM*
 * `1127IbnMustafaIstanbuli.RuhBayan `
	- *TAGS: CENT1200, _TAFSIR*
 * `1147CabdAllahSancani.TarikhYaman `
	- *TAGS: CENT1200, PPE, _BULDAN, _TARIKH*
 * `1147IbnSharafDinKhalili.FatawaKhalili `
	- *TAGS: CENT1200, _FATAWA*
 * `1153IbnKannan.YawmiyyatShamiyya `
	- *TAGS: CENT1200, PPE, _BULDAN, _TARIKH*
 * `1167IbnCabrRahmanGhazzi.DiwanIslam `
	- *TAGS: CENT1200, _SHICR_CUTHMANI, _SHICR, _TABAQAT, _TARAJIM*
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

* **1300AH [[ [Re]generated on 2016-10-22 (17:14:35) ]]**

 * `1204SulaymanJamal.Hashiya `
	- *TAGS: CENT1300, _FIQH, _SHAFICI*
 * `1204SulaymanJamal.Hashiya `
	- *TAGS: CENT1300, _FIQH, _SHAFICI*
 * `1205Zubaydi.TajCarus `
	- *TAGS: CENT1300, _FIQH, _GHARIB, _LUGHA, _MACAJIM, _MUSTALAHAT, _NAHW, _SARF*
 * `1206IbnCabdWahhab.Fatawa `
	- *TAGS: CENT1300, _FATAWA, _FIQH, _HANBALI*
 * `1206Muradi.SilkDurar `
	- *TAGS: CENT1300, PPE, _TABAQAT, _TARAJIM*
 * `1212BahrCulum.FawaidRijaliya `
	- *TAGS: CENT1300, PPE, SHC, _HADITH, _SHICI, _TARAJIM*
 * `1212BahrCulum.FawaidRijaliya `
	- *TAGS: CENT1300, PPE, SHC, _HADITH, _SHICI, _TARAJIM*
 * `1218SalihFulani.QatfThamar `
	- *TAGS: BIB, CENT1300, PPE, _ADILLA, _FAHARIS, _KUTUB*
 * `1225IbnNasirNajdi.MajmucatRasail `
	- *TAGS: CENT1300, _FATAWA*
 * `1225IbnNasirNajdi.RasailWaFatawa `
	- *TAGS: CENT1300, _FATAWA*
 * `1232IbnKhatibCumari.RawdaFayha `
	- *TAGS: CENT1300, PPE, _TABAQAT, _TARAJIM*
 * `1237Jabarti.CajaibAthar `
	- *TAGS: CENT1300, PPE, _TARIKH*
 * `1246IbnHamadBassam.DurarMafakhir `
	- *TAGS: CENT1300, _ANSAB, _TARAJIM, _TARIKH*
 * `1250IbnCaliShawkani.BadrTalic `
	- *TAGS: CENT1300, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `1250IbnCaliShawkani.FathBariMinFatawa `
	- *TAGS: CENT1300, _MAJALLAT, _MAJMUCAT, _FATAWA*
 * `1252IbnCabidinDimashqi.TanqihFatawa `
	- *TAGS: CENT1300, _FATAWA, _FIQH, _HANAFI*
 * `1258IbnCabdSalamTusuli.AjwibatTusuli `
	- *TAGS: CENT1300, _FATAWA*
 * `1269CabdMalikCasimi.SamtNujum `
	- *TAGS: CENT1200, PPE, _TARIKH*
 * `1270ShihabDinAlusi.GharaibIghtirab `
	- *TAGS: CENT1300, _BULDAN, _JUGHRAFIYA, _RIHLAT*
 * `1270ShihabDinAlusi.GharaibIghtirab `
	- *TAGS: CENT1400, _MISC*
 * `1277MuhammadTantawi.NashaNahw `
	- *TAGS: _ADILLA, _CENT00NO, _FAHARIS, _KUTUB*
 * `1282AbaButayn.RasailWaFatawa `
	- *TAGS: CENT1300, _FATAWA*
 * `1285CabdRahmanTamimi.Maqamat `
	- *TAGS: CENT1300, _TABAQAT, _TARAJIM*
 * `1285IbnHasanTamimi.RasailWaFatawa `
	- *TAGS: CENT1300, _FATAWA*
 * `1286IcjazHusaynKunturi.KashfHajb `
	- *TAGS: BIB, CENT1300, PPE, _FAHARIS, _KUTUB*
 * `1292IbnIbrahimMaghribi.QurratCaynBiFatawa `
	- *TAGS: CENT1300, _FATAWA*
 * `1293CabdLatifAlShaykh.CuyunRasailwaAjwiba `
	- *TAGS: CENT1300, _FATAWA*
 * `1299IbnCalishMaliki.FathCali `
	- *TAGS: CENT1300, _FATAWA*

* **1400AH [[ [Re]generated on 2016-10-22 (17:14:35) ]]**

 * `1307Qannawji.AbjadCulum `
	- *TAGS: CENT1400, PPE, _ADILLA, _FAHARIS, _KUTUB, _MACAJIM*
 * `1307Qannawji.BulghaFuUsulLugha `
	- *TAGS: CENT1400, _LUGHA*
 * `1307Qannawji.FathBayan `
	- *TAGS: CENT1400, _TAFSIR*
 * `1307Qannawji.HittaFiDhikr `
	- *TAGS: CENT1400, PPE, _ADILLA, _FAHARIS, _KUTUB*
 * `1307Qannawji.HusnUswa `
	- *TAGS: CENT1400, _BUHUTH, _FIQH, _MASAIL, _MISC, _USUL*
 * `1307Qannawji.LuqtaCajlan `
	- *TAGS: BIB, CENT1400, PPE, _ADILLA, _FAHARIS, _KUTUB*
 * `1307Qannawji.NashwatSakran `
	- *TAGS: CENT1400, _ADAB, _BALAGHA*
 * `1307Qannawji.NaylMaram `
	- *TAGS: CENT1400, _CULUM, _QURAN*
 * `1307Qannawji.QatfThamar `
	- *TAGS: CENT1400, _CAQAID, _MILAL*
 * `1307Qannawji.RawdaNadiyya `
	- *TAGS: CENT1400, _FIQH*
 * `1307Qannawji.Yaqza `
	- *TAGS: CENT1400, _ADAB, _ADHKAR, _AKHLAQ, _CAQAID, _MISC, _RAQAIQ, _SULUK*
 * `1310BakriDimyati.HashiyaIcanaTalibin `
	- *TAGS: CENT1400, _FIQH, _SHAFICI*
 * `1313Barujirdi.Taraif `
	- *TAGS: CENT1400, PPE, SHC, _HADITH, _SHICI, _TARAJIM*
 * `1313VanDyck.IktifaQunuc `
	- *TAGS: CENT1400, PPE, _ADILLA, _FAHARIS, _KUTUB*
 * `1315AbuMacaliKalbasi.RasailRijaliyya `
	- *TAGS: CENT1400, PPE, SHC, _HADITH, _SHICI, _TARAJIM*
 * `1315Salawi.IstiqsaLiAhkbar `
	- *TAGS: CENT1400, PPE, _BULDAN, _TARIKH*
 * `1318AhmadDimashqi.MucjamAsmaAshya `
	- *TAGS: CENT1400, _FIQH, _GHARIB, _MACAJIM, _MASAIL, _MUSTALAHAT*
 * `1318MuhammadSanusi.Musamarat `
	- *TAGS: CENT1400, PPE, _TABAQAT, _TARAJIM*
 * `1320NuriTabarsi.KhatimaMustadrak `
	- *TAGS: CENT1400, _HADITH, _SHICI*
 * `1320NuriTabarsi.MustadrakWasail `
	- *TAGS: CENT1400, _HADITH, _SHICI*
 * `1330IbnMusaTabrizi.MiratKutub `
	- *TAGS: BIB, CENT1400, PPE, _FAHARIS, _KUTUB*
 * `1332ZaynabFawwaz.DurrManthur `
	- *TAGS: CENT1400, PPE, _TABAQAT, _TARAJIM*
 * `1335CabdRazzaqBaytar.HilyaBashar `
	- *TAGS: CENT1400, PPE, _TABAQAT, _TARAJIM, _TARIKH, _WAFAYAT*
 * `1336CabdHamidThani.MudhakkaratiSiyasiya `
	- *TAGS: CENT1400, _MUDHAKKARAT, _QADA, _RIHLAT, _SIYASA*
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
 * `1353IbnCabdRahimMubarakfuri.TuhfatAhwadhi `
	- *TAGS: CENT1300, CENT1400, _CHRONOMULTIPLE, _FIQH, _HADITH, _SHARH, _SUNNI, _TARAJIM*
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
 * `1389MuhammadAlShaykh.FatawaWaRasail `
	- *TAGS: CENT1400, _FATAWA*
 * `1390MuhsinTabatabai.DalilNasik `
	- *TAGS: CENT1400, _FATAWA, _FIQH, _SHICI*
 * `1396KhayrDinZirikli.Aclam `
	- *TAGS: BIO, CENT1400, COL, PPE, _FAHARIS, _KUTUB, _TABAQAT, _TARAJIM*
 * `1400MuhammadBaqirSadr.FatawaWadiha `
	- *TAGS: CENT1400, _FATAWA, _FIQH, _SHICI*

* **1500AH [[ [Re]generated on 2016-10-22 (17:14:35) ]]**

 * `1405CaliShahrudi.Mustadrakat `
	- *TAGS: CENT1500, PPE, SHC, _HADITH, _SHICI, _TARAJIM*
 * `1408CumarKahhala.MucjamMuallifin `
	- *TAGS: BIB, BIO, CENT1500, COL, PPE, _FAHARIS, _KUTUB, _TABAQAT, _TARAJIM*
 * `1408CumarKahhala.MucjamQabail `
	- *TAGS: CENT1500, COL, GEN, PPE, _ANSAB, _MACAJIM*
 * `1409IbnSayyidCajamiMisri.HidayatQari `
	- *TAGS: CENT1500, _CULUM, _QURAN*
 * `1411SayyidMarcashi.SharhIhqaq `
	- *TAGS: CENT1500, _CAQAID, _SHICI, _TWELVERS*
 * `1413TajDinKhui.MinhajSalihin `
	- *TAGS: CENT1500, _FATAWA, _FIQH, _SHICI*
 * `1413TajDinKhui.MucjamRijal `
	- *TAGS: CENT1500, PPE, _HADITH, _SHICI, _TARAJIM*
 * `1413TajDinKhui.TakmilatMinhajSalihin `
	- *TAGS: CENT1500, _FATAWA, _FIQH, _SHICI*
 * `1414MuhammadRidaGulpayagani.HidayatCibad `
	- *TAGS: CENT1500, _FATAWA, _FIQH, _SHICI*
 * `1414MuhammadRidaGulpayagani.IrshadSail `
	- *TAGS: CENT1500, _FATAWA, _FIQH, _SHICI*
 * `1414MuhammadRidaGulpayagani.MukhtasarAhkam `
	- *TAGS: CENT1500, _FATAWA, _FIQH, _SHICI*
 * `1414SalimIbadi.IscafAcyan `
	- *TAGS: CENT1500, _ANSAB*
 * `1418MuhammadRuhani.ManasikHajj `
	- *TAGS: CENT1500, _FATAWA, _FIQH, _SHICI*
 * `1418MuhammadRuhani.MasailMuntakhaba `
	- *TAGS: CENT1500, _FATAWA, _FIQH, _SHICI*
 * `1418MuhammadRuhani.MinhajSalihin `
	- *TAGS: CENT1500, _FATAWA, _FIQH, _SHICI*
 * `1418SalihAhmadArkani.TihfaMajalis `
	- *TAGS: BIB, CENT1500, PPE, _FAHARIS, _KUTUB*
 * `1419MahmudTanahi.MujizFiMarajic `
	- *TAGS: BIB, CENT1500, PPE, _ADILLA, _FAHARIS, _KUTUB*
 * `1420IbnBaz.FatawaNurCalaDarb `
	- *TAGS: CENT1500, _FATAWA*
 * `1420IbnBaz.FatawaNurCalaDarb `
	- *TAGS: CENT1500, _FATAWA*
 * `1420IbnBaz.MajmucFatawa `
	- *TAGS: CENT1500, _FATAWA*
 * `1421HamdJasir.MucjamQabailMCS `
	- *TAGS: CENT1500, _ANSAB*
 * `1421MuhammadCuthaymin.FatawaArkanIslam `
	- *TAGS: CENT1500, _FATAWA*
 * `1421MuhammadCuthaymin.FatawaNurCalaDarb `
	- *TAGS: CENT1500, _FATAWA*
 * `1421MuhammadCuthaymin.MajmucFatawa `
	- *TAGS: CENT1500, _FATAWA*
 * `1422IbnHadiWadici.RijalHakim `
	- *TAGS: CENT1500, _TABAQAT, _TARAJIM*
 * `1422MuhammadSalimMuhaysin.MucjamHuffazQuran `
	- *TAGS: CENT1500, PPE, _TABAQAT, _TARAJIM*
 * `1422MuqbilWadici.TarajimRijal `
	- *TAGS: CENT1500, PPE, _TABAQAT, _TARAJIM*
 * `1424IhsanCabbas.ShadharatMinKutubMafquda `
	- *TAGS: CENT1500, PPE, _FAHARIS, _TARIKH*
 * `1429BakrIbnCabdAllah.TabaqatNassabin `
	- *TAGS: CENT1500, _TABAQAT, _TARAJIM*
 * `1430IbnJibrin.Fatawa `
	- *TAGS: _CENT00NO, _FATAWA*
 * `1450AbuTayyibMansuri.Irshad `
	- *TAGS: _CENT00NO, _TABAQAT, _TARAJIM*
 * `1450AkramFaluji.MucjamSaghir `
	- *TAGS: CENT1500, _TABAQAT, _TARAJIM*
 * `1450AkramFaluji.MucjamShuyukhTabari `
	- *TAGS: _CENT00NO, _TABAQAT, _TARAJIM*
 * `1450CabdRahmanAlShaykh.Mashahir `
	- *TAGS: CENT1500, PPE, _TABAQAT, _TARAJIM*
 * `1450CadilNuwayhid.MucjamAclamJazair `
	- *TAGS: _CENT00NO, _TABAQAT, _TARAJIM*
 * `1450CulamaNajd.DurarSaniyya `
	- *TAGS: _CENT00NO, _FATAWA*
 * `1450DarIftaMisriyya.FatawaDarIfta `
	- *TAGS: CENT1500, _FATAWA*
 * `1450JamicaIslamiyya.MajallaJIMN `
	- *TAGS: CENT1500, _MAJALLAT, _MAJMUCAT*
 * `1450LajnaDaima.Fatawa `
	- *TAGS: _CENT00NO, _FATAWA*
 * `1450Maghrawi.MawsucaMawaqifSalaf `
	- *TAGS: CENT1500, _CAQAID*
 * `1450MajmacFikrIslami.MawsucaMuallifiImamiya `
	- *TAGS: CENT1500, PPE, _FAHARIS, _KUTUB*
 * `1450MawqicIslam.Fatawa `
	- *TAGS: _CENT00NO, _FATAWA*
 * `1450MawsucaShicriya.MucjamShucara `
	- *TAGS: _CENT1500, _TABAQAT, _TARAJIM*
 * `1450Milani.NafahatAzhar `
	- *TAGS: CENT1500, _CAQAID, _SHICI, _TWELVERS*
 * `1450MuhammadAbtahi.TahdhibMaqal `
	- *TAGS: CENT1500, PPE, _HADITH, _SHICI, _TARAJIM*
 * `1450MuhammadHadiAmini.MucjamMatbicatNajafiya `
	- *TAGS: BIB, CENT1500, PPE, _FAHARIS, _KUTUB*
 * `1450MuhammadKhayrRamadan.TakmilaMucjamMuallifin `
	- *TAGS: BIB, CENT1500, COL, PPE, _TABAQAT, _TARAJIM*
 * `1450MuhammadSancani.NaylWatar `
	- *TAGS: BIO, CENT1500, COL, ORPHAN, PPE*
 * `1450MusaCaffana.Fatawa `
	- *TAGS: CENT1500, _FATAWA*
 * `1450Musannifun.MawsucaMujaza `
	- *TAGS: _CENT1500, _TARIKH*
 * `1450SadiqRuhani.ManasikHajj `
	- *TAGS: CENT1500, _FATAWA, _FIQH, _SHICI*
 * `1450SadiqRuhani.MasailMuntakhaba `
	- *TAGS: CENT1500, _FATAWA, _FIQH, _SHICI*
 * `1450SadiqRuhani.MinhajSalihin `
	- *TAGS: CENT1500, _FATAWA, _FIQH, _SHICI*
 * `1450SadiqRuhani.TakmilaMinhajSalihin `
	- *TAGS: CENT1500, _FATAWA, _FIQH, _SHICI*
 * `1450SalahMahmudKhaymi.FaharisCulumQuran `
	- *TAGS: _ADILLA, PPE, _CENT00NO, _FAHARIS, _KUTUB*
 * `1450SalihFawzan.MajmucFatawa `
	- *TAGS: _CENT00NO, _FATAWA*
 * `1450TarhibDawsari.MucjamMuallafatMalikiyya `
	- *TAGS: _ADILLA, _CENT00NO, _FAHARIS, _KUTUB*
 * `1450TarhibDawsari.MucjamMuallafatShaficiyya `
	- *TAGS: _ADILLA, _CENT00NO, _FAHARIS, _KUTUB*
 * `1450WahidKhurasani.MinhajSalihin `
	- *TAGS: CENT1500, _FATAWA, _FIQH, _SHICI*
 * `1450WizaraAwqafMisriyya.TarajimMujaza `
	- *TAGS: CENT1500, _TABAQAT, _TARAJIM*


## Statistics on the corpus

| **Category** | **Stats** |
|:--- | ------:|
| Number of text files | 2589 |
| Number of books      | 1305 |
| Number of authors    | 629 |
| Length in words (all)| 634,832,073 |
| Length in pages (300 w/p)| 2,116,106 |
| Length in words (unique) | 308,869,584 |
| Length in pages (300 w/p)| 1,029,565 |


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
| 2 | 1450JamicaIslamiyya.MajallaJIMN | 5,405,231 | 18,017 |
| 3 | 0855Cayni.CumdaQari | 4,680,632 | 15,602 |
| 4 | 1371MuhsinCamili.AcyanShica | 4,675,215 | 15,584 |
| 5 | 1205Zubaydi.TajCarus | 4,503,454 | 15,011 |
| 6 | 1111Majlisi.BiharAnwar | 4,430,411 | 14,768 |
| 7 | 1411SayyidMarcashi.SharhIhqaq | 4,126,172 | 13,753 |
| 8 | 0852IbnHajarCasqalani.FathBari | 3,545,728 | 11,819 |
| 9 | 0748Dhahabi.TarikhIslam | 3,437,381 | 11,457 |
| 10 | 0923AhmadQastallani.IrshadSari | 3,431,449 | 11,438 |
| 11 | 0748Dhahabi.SiyarAclamNubala | 3,145,544 | 10,485 |
| 12 | 0310Tabari.JamicBayan | 3,041,268 | 10,137 |
| 13 | 0728IbnTaymiyya.MajmucFatawa | 3,016,187 | 10,053 |
| 14 | 1389AghaBuzurgTihrani.DharicaFiTasanifShica | 2,918,325 | 9,727 |
| 15 | 0676Nawawi.Majmuc | 2,819,113 | 9,397 |
| 16 | 0742Mizzi.TahdhibKamal | 2,701,747 | 9,005 |
| 17 | 0463KhatibBaghdadi.TarikhBaghdad | 2,621,786 | 8,739 |
| 18 | 1450MawqicIslam.Fatawa | 2,607,138 | 8,690 |
| 19 | 1413TajDinKhui.MucjamRijal | 2,594,210 | 8,647 |
| 20 | 1014IbnSultanHarawi.MirqatMafatih | 2,481,715 | 8,272 |
| 21 | 0733Nuwayri.NihayaArab | 2,455,687 | 8,185 |
| 22 | 1127IbnMustafaIstanbuli.RuhBayan | 2,425,227 | 8,084 |
| 23 | 0711IbnManzurIfriqi.MukhtasarTarikhDimashq | 2,408,342 | 8,027 |
| 24 | 0774IbnKathir.Bidaya | 2,329,940 | 7,766 |
| 25 | 1204SulaymanJamal.Hashiya | 2,260,269 | 7,534 |
| 26 | 1420IbnBaz.MajmucFatawa | 2,038,258 | 6,794 |
| 27 | 1421MuhammadCuthaymin.MajmucFatawa | 2,025,627 | 6,752 |
| 28 | 1450LajnaDaima.Fatawa | 1,993,944 | 6,646 |
| 29 | 1320NuriTabarsi.MustadrakWasail | 1,983,623 | 6,612 |
| 30 | 0764Safadi.WafiBiWafayat | 1,978,264 | 6,594 |
| 31 | 1450DarIftaMisriyya.FatawaDarIfta | 1,911,816 | 6,372 |
| 32 | 0942IbnYusufShami.SubulHuda | 1,900,839 | 6,336 |
| 33 | 0845Maqrizi.ImtacAsmac | 1,802,668 | 6,008 |
| 34 | 0241IbnHanbal.Musnad | 1,778,094 | 5,926 |
| 35 | 0911Suyuti.DurrManthur | 1,732,784 | 5,775 |
| 36 | 1090NizamDinBalkhi.FatawaHindiyya | 1,729,192 | 5,763 |
| 37 | 0774IbnKathir.TafsirQuran | 1,696,932 | 5,656 |
| 38 | 1396KhayrDinZirikli.Aclam | 1,634,967 | 5,449 |
| 39 | 1420IbnBaz.FatawaNurCalaDarb | 1,627,900 | 5,426 |
| 40 | 0821Qalqashandi.SubhAcsha | 1,616,289 | 5,387 |
| 41 | 0310Tabari.Tarikh | 1,613,108 | 5,377 |
| 42 | 0808IbnKhaldun.Tarikh | 1,596,529 | 5,321 |
| 43 | 0360Tabarani.MucjamKabir | 1,590,311 | 5,301 |
| 44 | 1421MuhammadCuthaymin.FatawaNurCalaDarb | 1,572,869 | 5,242 |
| 45 | 0355AbuFarajIsbahani.Aghani | 1,537,021 | 5,123 |
| 46 | 0597IbnJawzi.Muntazam | 1,529,894 | 5,099 |
| 47 | 1307Qannawji.FathBayan | 1,522,217 | 5,074 |
| 48 | 1450Milani.NafahatAzhar | 1,517,206 | 5,057 |
| 49 | 0463IbnCabdBarr.TamhidMuwatta | 1,461,702 | 4,872 |
| 50 | 0656IbnAbiHadid.SharhNahjBalagha | 1,452,591 | 4,841 |
| 51 | 1450CulamaNajd.DurarSaniyya | 1,438,831 | 4,796 |
| 52 | 0852IbnHajarCasqalani.TahdhibTahdhib | 1,415,254 | 4,717 |
| 53 | 0630IbnAthirCizzDin.Kamil | 1,385,342 | 4,617 |
| 54 | 0660IbnCadim.BughyatTalib | 1,373,052 | 4,576 |
| 55 | 1353IbnCabdRahimMubarakfuri.TuhfatAhwadhi | 1,368,928 | 4,563 |
| 56 | 0902Sakhawi.DuLamic | 1,335,429 | 4,451 |
| 57 | 0874IbnTaghribirdi.NujumZahira | 1,314,867 | 4,382 |
| 58 | 0626YaqutHamawi.MucjamBuldan | 1,274,659 | 4,248 |
| 59 | 0211CabdRazzakSancani.Musannaf | 1,267,117 | 4,223 |
| 60 | 0204Shafici.Umm | 1,258,325 | 4,194 |
| 61 | 0728IbnTaymiyya.RasailWaFatawa | 1,258,070 | 4,193 |
| 62 | 0430AbuNucaymIsbahani.HilyaAwliya | 1,227,955 | 4,093 |
| 63 | 0807NurDinHaythami.MucjamZawaid | 1,222,016 | 4,073 |
| 64 | 0749ShihabDinCumari.MasalikAbsar | 1,182,722 | 3,942 |
| 65 | 0852IbnHajarCasqalani.IsabaFiTamyiz | 1,153,468 | 3,844 |
| 66 | 0463IbnCabdBarr.IstidhkarJamic | 1,147,942 | 3,826 |
| 67 | 1408CumarKahhala.MucjamMuallifin | 1,145,173 | 3,817 |
| 68 | 0852IbnHajarCasqalani.LisanMizan | 1,131,427 | 3,771 |
| 69 | 0279Baladhuri.AnsabAshraf | 1,128,932 | 3,763 |
| 70 | 0277AbuHatimRazi.JarhWaTacdil | 1,121,289 | 3,737 |
| 71 | 0676Nawawi.RawdatTalibin | 1,105,776 | 3,685 |
| 72 | 1089IbnCimad.Shadharat | 1,097,722 | 3,659 |
| 73 | 0774IbnKathir.JamicMasanid | 1,078,748 | 3,595 |
| 74 | 1405CaliShahrudi.Mustadrakat | 1,015,230 | 3,384 |
| 75 | 0505Ghazali.IhyaCulumDin | 996,434 | 3,321 |
| 76 | 1310BakriDimyati.HashiyaIcanaTalibin | 989,242 | 3,297 |
| 77 | 1093CabdQadirBaghdadi.KhizanatAdab | 981,595 | 3,271 |
| 78 | 1122MuhammadZarqani.SharhCalaMuwatta | 975,818 | 3,252 |
| 79 | 0804IbnMulaqqin.BadrMunir | 973,506 | 3,245 |
| 80 | 0630IbnAthirCizzDin.UsdGhaba | 963,485 | 3,211 |
| 81 | 0365IbnCadiJurjani.KamilFiDucafa | 962,139 | 3,207 |
| 82 | 1450Maghrawi.MawsucaMawaqifSalaf | 952,565 | 3,175 |
| 83 | 0179MalikIbnAnas.MudawwanaKubra | 948,401 | 3,161 |
| 84 | 0561Samcani.Ansab | 943,976 | 3,146 |
| 85 | 0230IbnSacd.TabaqatKubra | 921,111 | 3,070 |
| 86 | 1450MusaCaffana.Fatawa | 917,900 | 3,059 |
| 87 | 0728IbnTaymiyya.FatawaKubra | 910,627 | 3,035 |
| 88 | 0405HakimNaysaburi.Mustadrak | 886,412 | 2,954 |
| 89 | 0475IbnMakula.IkmalFiRafcIrtiyab | 868,430 | 2,894 |
| 90 | 0762MughaltayIbnQalij.IkmalTahdhib | 861,631 | 2,872 |
| 91 | 1107HashimBahrani.GhayatMaram | 854,344 | 2,847 |
| 92 | 1041Maqarri.NafhTib | 848,136 | 2,827 |
| 93 | 0973IbnHajarHaythami.FatawaKubra | 831,866 | 2,772 |
| 94 | 0845Maqrizi.Suluk | 826,074 | 2,753 |
| 95 | 1389MuhammadAlShaykh.FatawaWaRasail | 822,319 | 2,741 |
| 96 | 0597IbnJawzi.ZadMasir | 795,393 | 2,651 |
| 97 | 0626YaqutHamawi.MucjamUdaba | 794,903 | 2,649 |
| 98 | 0256Bukhari.TarikhKabir | 791,001 | 2,636 |
| 99 | 1250IbnCaliShawkani.FathBariMinFatawa | 787,019 | 2,623 |
| 100 | 0430AbuNucaymIsbahani.MacrifaSahaba | 785,050 | 2,616 |
| 101 | 0676Nawawi.SharhMuslim | 758,673 | 2,528 |
| 102 | 0292AbuBakrBazzar.BahrZakhkhar | 747,561 | 2,491 |
| 103 | 1320NuriTabarsi.KhatimaMustadrak | 731,187 | 2,437 |
| 104 | 0360Tabarani.MucjamAwsat | 728,810 | 2,429 |
| 105 | 0806IbnHusaynCiraqi.TarhTarthib | 712,047 | 2,373 |
| 106 | 0845Maqrizi.Mawaciz | 683,850 | 2,279 |
| 107 | 1057IbnCallan.DalilFalihin | 680,104 | 2,267 |
| 108 | 0421Miskawayh.Tajarib | 679,938 | 2,266 |
| 109 | 0681IbnKhallikan.WafayatAcyan | 677,482 | 2,258 |
| 110 | 0771Subki.TabaqatShaficiyaKubra | 676,807 | 2,256 |
| 111 | 1450Musannifun.MawsucaMujaza | 668,172 | 2,227 |
| 112 | 0855Cayni.SharhSunanAbiDawud | 663,495 | 2,211 |
| 113 | 0748Dhahabi.MizanIctidal | 649,090 | 2,163 |
| 114 | 1341CabdHayyTalibi.IclamBiMan | 634,469 | 2,114 |
| 115 | 0256Bukhari.Sahih | 628,978 | 2,096 |
| 116 | 1111MuhammadAminMuhibbi.KhulasaAthr | 623,533 | 2,078 |
| 117 | 1101MuhammadCaliArdabili.JamicRuwat | 614,459 | 2,048 |
| 118 | 1315AbuMacaliKalbasi.RasailRijaliyya | 613,389 | 2,044 |
| 119 | 1014IbnSultanHarawi.SharhShifa | 613,217 | 2,044 |
| 120 | 0764Safadi.AcyanCasr | 604,057 | 2,013 |
| 121 | 0458Bayhaqi.DalailNubuwwa | 602,949 | 2,009 |
| 122 | 1269CabdMalikCasimi.SamtNujum | 594,712 | 1,982 |
| 123 | 0542IbnBassamShantarini.Dhakhira | 593,086 | 1,976 |
| 124 | 0817Firuzabadi.QamusMuhit | 581,791 | 1,939 |
| 125 | 1067HajjiKhalifa.KashfZunun | 580,572 | 1,935 |
| 126 | 0751IbQayyimJawziyya.ZadMacad | 566,492 | 1,888 |
| 127 | 0328IbnCabdRabbihi.CiqdFarid | 562,475 | 1,874 |
| 128 | 0966HusaynDiyarbakri.TarikhKhamis | 552,947 | 1,843 |
| 129 | 0842IbnNasirDinDimashqi.TawdihMushtabih | 550,678 | 1,835 |
| 130 | 1368HasanAmin.MustadrakatAcyanShica | 547,076 | 1,823 |
| 131 | 0354IbnHibban.Thiqat | 535,985 | 1,786 |
| 132 | 0261Muslim.Sahih | 523,024 | 1,743 |
| 133 | 1237Jabarti.CajaibAthar | 514,968 | 1,716 |
| 134 | 0150MuqatilIbnSulayman.TafsirMuqatil | 501,772 | 1,672 |
| 135 | 1100MustafaTafrishi.NaqdRijal | 500,280 | 1,667 |
| 136 | 0170KhalilFarahidi.Cayn | 494,216 | 1,647 |
| 137 | 0879IbnQutlubugha.Thiqat | 473,854 | 1,579 |
| 138 | 1408CumarKahhala.MucjamQabail | 467,206 | 1,557 |
| 139 | 1450MuhammadAbtahi.TahdhibMaqal | 465,412 | 1,551 |
| 140 | 1315Salawi.IstiqsaLiAhkbar | 464,659 | 1,548 |
| 141 | 0776LisanDinIbnKhatib.Ihata | 462,435 | 1,541 |
| 142 | 0255Jahiz.Hayawan | 455,685 | 1,518 |
| 143 | 0751IbQayyimJawziyya.AclamMuwaqqicin | 450,649 | 1,502 |
| 144 | 0808MuhammadDamiri.HayatHayawanKubra | 441,392 | 1,471 |
| 145 | 1351IbnHusaynGhazzi.NahrDhahab | 434,840 | 1,449 |
| 146 | 0387IbnSamcunBaghdadi.Amali | 434,581 | 1,448 |
| 147 | 0855Cayni.MaghaniAkhyar | 426,063 | 1,420 |
| 148 | 0768Yafici.MiratJanan | 424,088 | 1,413 |
| 149 | 1122MuhammadZarqani.SharhCalaMawahib | 422,551 | 1,408 |
| 150 | 0756TaqiDinSubki.Fatawa | 418,947 | 1,396 |
| 151 | 0852IbnHajarCasqalani.DurarKamina | 414,702 | 1,382 |
| 152 | 1372KurdCali.KhitatSham | 414,117 | 1,380 |
| 153 | 0463IbnCabdBarr.IsticabFiMacrifaAshab | 413,421 | 1,378 |
| 154 | 0279Tirmidhi.JamicSahih | 413,385 | 1,377 |
| 155 | 1339IsmacilBashaBaghdadi.HadiyaCarifin | 412,771 | 1,375 |
| 156 | 0852IbnHajarCasqalani.InbaGhumr | 410,739 | 1,369 |
| 157 | 0275AbuDawudSijistani.Sunan | 407,350 | 1,357 |
| 158 | 0505Ghazali.Wasit | 404,624 | 1,348 |
| 159 | 1351YusufIlyanSarkis.MucjamMatbucat | 401,654 | 1,338 |
| 160 | 0893IbnAbiBakrHadari.BahjatMahafil | 401,485 | 1,338 |
| 161 | 1252IbnCabidinDimashqi.TanqihFatawa | 394,372 | 1,314 |
| 162 | 0902Sakhawi.TuhfaLatifa | 394,353 | 1,314 |
| 163 | 1450WahidKhurasani.MinhajSalihin | 392,908 | 1,309 |
| 164 | 0386AbuTalibMakki.QutQulub | 385,567 | 1,285 |
| 165 | 0637IbnMustafwi.TarikhIrbil | 385,144 | 1,283 |
| 166 | 0597CimadDinKatib.KharidaQasr | 385,025 | 1,283 |
| 167 | 0346Mascudi.MurujDhahab | 382,786 | 1,275 |
| 168 | 0751IbQayyimJawziyya.MadarijSalikin | 378,062 | 1,260 |
| 169 | 0806IbnHusaynCiraqi.SharhAlfiyya | 376,778 | 1,255 |
| 170 | 0911Samhudi.WafaWafa | 376,631 | 1,255 |
| 171 | 1299IbnCalishMaliki.FathCali | 372,373 | 1,241 |
| 172 | 0874IbnTaghribirdi.ManhalSafi | 368,687 | 1,228 |
| 173 | 0429AbuMansurThacalibi.YatimaDahr | 362,496 | 1,208 |
| 174 | 0900AbuCabdAllahHimyari.RawdMictar | 362,088 | 1,206 |
| 175 | 1206Muradi.SilkDurar | 358,759 | 1,195 |
| 176 | 0623Qazwini.Tadwin | 353,391 | 1,177 |
| 177 | 0676Nawawi.TahdhibAsma | 352,183 | 1,173 |
| 178 | 0262AbuZaydNumayri.TarikhMadina | 351,743 | 1,172 |
| 179 | 1335CabdRazzaqBaytar.HilyaBashar | 346,616 | 1,155 |
| 180 | 0630IbnAthirCizzDin.LubabFiTahdhibAnsab | 341,753 | 1,139 |
| 181 | 0277IbnSyfyanFasawi.MacrifaWaTarikh | 340,450 | 1,134 |
| 182 | 1212BahrCulum.FawaidRijaliya | 338,918 | 1,129 |
| 183 | 0833IbnJazari.GhayaNihaya | 338,862 | 1,129 |
| 184 | 0748Dhahabi.TadhkiraHuffaz | 337,969 | 1,126 |
| 185 | 0597IbnJawzi.KashfMushkil | 336,225 | 1,120 |
| 186 | 0807NurDinHaythami.GhayatMaqsad | 334,690 | 1,115 |
| 187 | 1313Barujirdi.Taraif | 331,121 | 1,103 |
| 188 | 0597IbnJawzi.SifaSafwa | 330,284 | 1,100 |
| 189 | 0923IbnCabdAllahKhazraji.KhulasaTahdhib | 328,135 | 1,093 |
| 190 | 0642IbnNajjar.DhaylTarikhBaghdad | 326,501 | 1,088 |
| 191 | 0372AbuSacidQayruwani.TahdhibMudawwana | 325,423 | 1,084 |
| 192 | 0726Yunini.DhaylMiratZaman | 323,810 | 1,079 |
| 193 | 0544CiyadIbnMusaYahsubi.TartibMadarik | 322,807 | 1,076 |
| 194 | 0189MuhammadShaybani.Asl | 319,253 | 1,064 |
| 195 | 0665AbuShama.Rawdatayn | 317,787 | 1,059 |
| 196 | 0732AbuFida.MukhtasarFiAkhbar | 316,828 | 1,056 |
| 197 | 1430IbnJibrin.Fatawa | 314,884 | 1,049 |
| 198 | 0817Firuzabadi.TanwirMiqbas | 314,570 | 1,048 |
| 199 | 0322AbuJacfarCuqayli.DucafaKabir | 314,435 | 1,048 |
| 200 | 0499IbnHusaynJurjani.TartibAmali | 313,911 | 1,046 |
| 201 | 0911Suyuti.LaaliMasnuca | 310,804 | 1,036 |
| 202 | 0693IbnAbiFathIrbili.KashfGhumma | 309,157 | 1,030 |
| 203 | 0414AbuHayyanTawhidi.Basair | 307,963 | 1,026 |
| 204 | 0911Suyuti.HawiLiFatawa | 306,937 | 1,023 |
| 205 | 0911Suyuti.AsmaMudallisin | 306,751 | 1,022 |
| 206 | 0832AbuTayyibFasi.ShifaGharam | 305,946 | 1,019 |
| 207 | 0658IbnAbbar.TakmilaLiSila | 303,591 | 1,011 |
| 208 | 1359CabbasQummi.Kuna | 299,903 | 999 |
| 209 | 1360IbnQasimMakhluf.ShajaraNur | 299,618 | 998 |
| 210 | 0538IbnCumarZamakhshari.FaiqFiGharib | 298,042 | 993 |
| 211 | 0646IbnQifti.InbahRuwat | 295,800 | 986 |
| 212 | 1383CadbHayyKattani.FihrisFaharis | 295,736 | 985 |
| 213 | 0213IbnHisham.SiraNabawiyya | 295,600 | 985 |
| 214 | 0902Sakhawi.FathMughith | 294,305 | 981 |
| 215 | 0273IbnMaja.Sunan | 293,138 | 977 |
| 216 | 0487AbuCubaydBakri.MucjamMaIstacjama | 291,075 | 970 |
| 217 | 1307Qannawji.RawdaNadiyya | 290,058 | 966 |
| 218 | 0911Suyuti.NawahidAbkar | 289,785 | 965 |
| 219 | 1339IsmacilBashaBaghdadi.IdahMaknun | 288,661 | 962 |
| 220 | 0764IbnShakirKutubi.FawatWafayat | 288,315 | 961 |
| 221 | 0807NurDinHaythami.KashfAstar | 284,395 | 947 |
| 222 | 0751IbQayyimJawziyya.BadaicFawaid | 284,235 | 947 |
| 223 | 0756TaqiDinSubki.Ibhaj | 284,031 | 946 |
| 224 | 0180Sibawayh.KitabSibawayh | 281,336 | 937 |
| 225 | 0855Cayni.CiqdJuman | 274,376 | 914 |
| 226 | 0833IbnJazari.Nashr | 274,215 | 914 |
| 227 | 1307Qannawji.AbjadCulum | 274,005 | 913 |
| 228 | 0732IbnYacqubJanadi.SulukFiTabaqat | 272,623 | 908 |
| 229 | 0748Dhahabi.CibarFiKhabar | 270,945 | 903 |
| 230 | 0272Fakihi.AkhbarMakka | 269,999 | 899 |
| 231 | 0779IbnBattuta.Rihla | 267,265 | 890 |
| 232 | 0911Suyuti.KhasaisKubra | 266,949 | 889 |
| 233 | 0911Suyuti.TafsirJalalayn | 266,662 | 888 |
| 234 | 1318MuhammadSanusi.Musamarat | 266,110 | 887 |
| 235 | 0287Dahhak.AhadWaMathani | 265,863 | 886 |
| 236 | 0207Waqidi.Maghazi | 264,920 | 883 |
| 237 | 0911Suyuti.Itqan | 263,388 | 877 |
| 238 | 0430AbuNucaymIsbahani.TarikhIsbahan | 260,298 | 867 |
| 239 | 0597IbnJawzi.Mawducat | 259,908 | 866 |
| 240 | 0179MalikIbnAnas.Muwatta | 259,815 | 866 |
| 241 | 1450SalahMahmudKhaymi.FaharisCulumQuran | 259,637 | 865 |
| 242 | 0774IbnKathir.Takmil | 255,916 | 853 |
| 243 | 0668IbnAbiUsaybica.CuyunAnba | 253,484 | 844 |
| 244 | 0749IbnWardi.Tarikh | 252,903 | 843 |
| 245 | 0274AhmadBarqi.Mahasin | 251,755 | 839 |
| 246 | 1450AkramFaluji.MucjamSaghir | 251,265 | 837 |
| 247 | 1014IbnSultanHarawi.JamcWasail | 250,690 | 835 |
| 248 | 0354IbnHibban.Majruhin | 250,389 | 834 |
| 249 | 0728IbnTaymiyya.MustadrakCalaMajmucFatawa | 249,305 | 831 |
| 250 | 1450MajmacFikrIslami.MawsucaMuallifiImamiya | 249,154 | 830 |
| 251 | 0207Waqidi.FutuhSham | 248,628 | 828 |
| 252 | 0261Muslim.SharhKitabHajj | 246,757 | 822 |
| 253 | 0207IbnZiyadFarra.MacaniQuran | 245,716 | 819 |
| 254 | 1061NajmDinGhazzi.KawakibSaira | 242,384 | 807 |
| 255 | 0751IbQayyimJawziyya.MiftahDarSacada | 240,583 | 801 |
| 256 | 1450AkramFaluji.MucjamShuyukhTabari | 240,016 | 800 |
| 257 | 1332ZaynabFawwaz.DurrManthur | 238,367 | 794 |
| 258 | 0807NurDinHaythami.MawaridZaman | 238,357 | 794 |
| 259 | 0957ShihabDinRamli.FatawaRamli | 238,093 | 793 |
| 260 | 1004ShamsDinRamli.FatawaRamli | 237,937 | 793 |
| 261 | 0306IbnHayyanDabbi.AkhbarQudat | 237,235 | 790 |
| 262 | 0748Dhahabi.Kashif | 235,822 | 786 |
| 263 | 1376MuhammadHajwiThacalibi.FikrSami | 234,888 | 782 |
| 264 | 0911Suyuti.SharhSunanIbnMaja | 233,491 | 778 |
| 265 | 0276IbnQutaybaDinawari.CuyunAkhbar | 232,763 | 775 |
| 266 | 0973CabdWahhabShacrani.LawaqihAnwar | 232,710 | 775 |
| 267 | 0629IbnNuqta.TakmilaIkmal | 231,460 | 771 |
| 268 | 0775IbnAbiWafa.JawahirMudiya | 230,720 | 769 |
| 269 | 0460ShaykhTusi.IkhtiyarMacrifaRijal | 227,637 | 758 |
| 270 | 1356AbuHudaKalbasi.SamaMaqal | 226,396 | 754 |
| 271 | 1147IbnSharafDinKhalili.FatawaKhalili | 225,290 | 750 |
| 272 | 0927Nucaymi.DarisFiMadaris | 224,568 | 748 |
| 273 | 0739SafiDinHanbali.Marasid | 220,179 | 733 |
| 274 | 0927Culaymi.UnsJalil | 218,375 | 727 |
| 275 | 0317AbuQasimBaghawi.MucjamSahaba | 218,356 | 727 |
| 276 | 0911Suyuti.HusnMuhadara | 218,158 | 727 |
| 277 | 0463KhatibBaghdadi.MuttafiqWaMuftariq | 218,096 | 726 |
| 278 | 0852IbnHajarCasqalani.TaqribTahdhib | 217,589 | 725 |
| 279 | 0241IbnHanbal.CilalWaMacrifa | 214,328 | 714 |
| 280 | 0795IbnRajabHanbali.DhaylTabaqatHanabila | 213,679 | 712 |
| 281 | 0110IbnSirin.MuntakhabKalamFiTafsirAhlam | 213,643 | 712 |
| 282 | 1414MuhammadRidaGulpayagani.HidayatCibad | 213,176 | 710 |
| 283 | 0597IbnJawzi.TahqiqFiAhadithKhilaf | 213,087 | 710 |
| 284 | 0255CabdAllahDarimi.Sunan | 209,282 | 697 |
| 285 | 0911Suyuti.DibajCalaMuslim | 209,180 | 697 |
| 286 | 0852IbnHajarCasqalani.TabsirMuntabih | 209,171 | 697 |
| 287 | 0560SharifIdrisi.NuzhaMushtaq | 207,532 | 691 |
| 288 | 0385Daruqutni.MutalifWaMukhtalif | 207,158 | 690 |
| 289 | 0694MuhibbDinTabari.RiyadNadira | 205,681 | 685 |
| 290 | 1175MuhammadKarabisi.IklilManhaj | 203,395 | 677 |
| 291 | 0224AbuCubaydIbnSallam.GharibHadith | 203,348 | 677 |
| 292 | 0251IbnMansurKawsaj.Masail | 200,411 | 668 |
| 293 | 0463IbnCabdBarr.KafiFiFiqh | 199,095 | 663 |
| 294 | 0911Suyuti.BughyaWucat | 197,961 | 659 |
| 295 | 0400IbnTahirMaqdisi.BadWaTarikh | 197,348 | 657 |
| 296 | 0571IbnCasakir.MucjamShuyukh | 195,776 | 652 |
| 297 | 0413ShaykhMufid.Muqnica | 195,606 | 652 |
| 298 | 0911Suyuti.MuzhirFiCulumLugha | 194,828 | 649 |
| 299 | 0645TilimsaniBurri.Jawhara | 194,697 | 648 |
| 300 | 0751IbQayyimJawziyya.IghathatLahfan | 193,281 | 644 |
| 301 | 0751IbQayyimJawziyya.SawaciqMursala | 193,235 | 644 |
| 302 | 0292Yacqubi.TarikhYacqubi | 193,018 | 643 |
| 303 | 1250IbnCaliShawkani.BadrTalic | 192,663 | 642 |
| 304 | 0751IbQayyimJawziyya.MukhtasarSawaciqMursala | 192,397 | 641 |
| 305 | 0347IbnYunusSadafi.Tarikh | 190,889 | 636 |
| 306 | 1450MuhammadKhayrRamadan.TakmilaMucjamMuallifin | 189,829 | 632 |
| 307 | 0561Samcani.Muntakhab | 188,251 | 627 |
| 308 | 0463KhatibBaghdadi.TalkhisMutashabih | 187,352 | 624 |
| 309 | 0310IbnAhmadDulabi.KunaWaAsma | 186,967 | 623 |
| 310 | 0597IbnJawzi.Tabsira | 186,643 | 622 |
| 311 | 1041Maqarri.AzharRiyad | 185,770 | 619 |
| 312 | 1413TajDinKhui.MinhajSalihin | 185,758 | 619 |
| 313 | 0789IbnMuhammadKhuzaci.TakhrijDalalat | 185,440 | 618 |
| 314 | 0845Maqrizi.IqazHunafa | 185,230 | 617 |
| 315 | 0774IbnKathir.QisasAnbiya | 183,993 | 613 |
| 316 | 0852IbnHajarCasqalani.MucjamMufahras | 183,759 | 612 |
| 317 | 0637IbnAthirDiyaDin.MathalSair | 183,732 | 612 |
| 318 | 0505Ghazali.Mustasfa | 183,605 | 612 |
| 319 | 0204Shafici.Risala | 183,244 | 610 |
| 320 | 0251IbnZanjawayh.Amwal | 183,217 | 610 |
| 321 | 0487AbuCubaydBakri.MasalikWaMamalik | 181,326 | 604 |
| 322 | 0597IbnJawzi.CilalMutanahiyya | 181,277 | 604 |
| 323 | 0774IbnKathir.TabaqatShaficiyyin | 180,884 | 602 |
| 324 | 0474IbnKhalafBaji.TacdilWaTakhrij | 180,381 | 601 |
| 325 | 0264IbnYahyaMuzani.Mukhtasar | 179,308 | 597 |
| 326 | 0832AbuTayyibFasi.DhaylTaqyid | 177,958 | 593 |
| 327 | 1450SadiqRuhani.MinhajSalihin | 177,800 | 592 |
| 328 | 0204AbuDawudTayalisi.Musnad | 177,566 | 591 |
| 329 | 0815IbnCabdAllahGhazuli.MatalicBudur | 175,305 | 584 |
| 330 | 0238IbnRahawayh.Musnad | 174,827 | 582 |
| 331 | 1120CaliKhanMadani.DarajatRafica | 174,564 | 581 |
| 332 | 0413ShaykhMufid.Irshad | 172,972 | 576 |
| 333 | 0751IbQayyimJawziyya.AhkamAhlDhimma | 172,395 | 574 |
| 334 | 0255Jahiz.Rasail | 172,282 | 574 |
| 335 | 0287Dahhak.Sunna | 172,108 | 573 |
| 336 | 0521IbnAbiYacla.TabaqatHanabila | 171,812 | 572 |
| 337 | 0508FattalNaysaburi.RawdaWacizin | 170,713 | 569 |
| 338 | 0255Jahiz.BayanWaTabyin | 170,368 | 567 |
| 339 | 0884SibtIbnCajami.KunuzDhahab | 170,224 | 567 |
| 340 | 1422MuhammadSalimMuhaysin.MucjamHuffazQuran | 169,932 | 566 |
| 341 | 0973IbnHajarHaythami.FatawaHadithiyya | 169,473 | 564 |
| 342 | 0911Samhudi.KhulasaWafaWafa | 168,018 | 560 |
| 343 | 0276IbnQutaybaDinawari.MacaniKabir | 168,017 | 560 |
| 344 | 0812CaliKhazraji.CuqudLuluiyya | 167,694 | 558 |
| 345 | 0615MuwaffaqDinShafici.MurshidZuwwar | 167,271 | 557 |
| 346 | 0911Suyuti.TadribRawi | 166,686 | 555 |
| 347 | 0335Suli.AkhbarRadi | 165,915 | 553 |
| 348 | 1119IbnMacsum.SulafaCasr | 165,783 | 552 |
| 349 | 0421IbnMuhammadMarzuqi.AzminaWaAmkina | 165,458 | 551 |
| 350 | 0751IbQayyimJawziyya.ShifaCalil | 165,000 | 550 |
| 351 | 0643IbnSalahShahrazuri.Fatawa | 164,681 | 548 |
| 352 | 0774IbnKathir.NihayatFiFitan | 162,376 | 541 |
| 353 | 0511SalmaSahari.Ansab | 162,120 | 540 |
| 354 | 0276IbnQutaybaDinawari.ImamaWaSiyasa | 162,038 | 540 |
| 355 | 1010TamimiDari.TabaqatSaniya | 161,681 | 538 |
| 356 | 0597IbnJawzi.TalqihFuhum | 160,269 | 534 |
| 357 | 1409IbnSayyidCajamiMisri.HidayatQari | 158,087 | 526 |
| 358 | 0458Bayhaqi.AsmaWaSifat | 157,931 | 526 |
| 359 | 0040CaliIbnAbiTalib.NahjBalagha | 157,597 | 525 |
| 360 | 0290IbnHasanSaffar.BasairDarajat | 157,407 | 524 |
| 361 | 1011SahibMacalim.TahrirTawusi | 157,260 | 524 |
| 362 | 1450MawsucaShicriya.MucjamShucara | 155,885 | 519 |
| 363 | 1338MuhammadFaridBey.Tarikh | 155,747 | 519 |
| 364 | 0676Nawawi.Adhkar | 155,669 | 518 |
| 365 | 0279IbnAbiKhaythama.TarikhKabir | 155,627 | 518 |
| 366 | 1418MuhammadRuhani.MinhajSalihin | 155,324 | 517 |
| 367 | 0535QawwamSunna.SiyarSalaf | 154,547 | 515 |
| 368 | 0695IbnCidhariMarrakushi.BayanMaghrib | 153,641 | 512 |
| 369 | 0748Dhahabi.MucjamShuyukh | 152,971 | 509 |
| 370 | 1422IbnHadiWadici.RijalHakim | 152,657 | 508 |
| 371 | 0260IbnSahlTabari.FirdawsHikmaFiTibb | 152,376 | 507 |
| 372 | 0276IbnQutaybaDinawari.GharibHadith | 151,462 | 504 |
| 373 | 0911Suyuti.Ashbah | 150,770 | 502 |
| 374 | 0777BadrDinBacli.MukhtasarFatawaMisriyya | 149,612 | 498 |
| 375 | 1292IbnIbrahimMaghribi.QurratCaynBiFatawa | 149,088 | 496 |
| 376 | 0802IbnMusaAbnasi.ShadhaFayyah | 148,038 | 493 |
| 377 | 0365IbnFaqihHamadhani.Buldan | 147,627 | 492 |
| 378 | 0682ZakariyaQazwini.AtharBilad | 146,837 | 489 |
| 379 | 0696IbnZahiri.Mashyakha | 146,557 | 488 |
| 380 | 0313IbnIshaqSarraj.Musnad | 146,495 | 488 |
| 381 | 0211CabdRazzakSancani.Tafsir | 145,718 | 485 |
| 382 | 0968Tashkubruizadah.ShaqaiqNucmaniyya | 145,615 | 485 |
| 383 | 0751IbQayyimJawziyya.TafsirQuran | 145,349 | 484 |
| 384 | 0597IbnJawzi.DhammHawa | 144,805 | 482 |
| 385 | 1450AbuTayyibMansuri.Irshad | 144,616 | 482 |
| 386 | 0774IbnKathir.SharhIkhtisarCulumHadith | 143,546 | 478 |
| 387 | 0845Maqrizi.MukhtasarKamil | 142,932 | 476 |
| 388 | 0821Qalqashandi.Maathir | 142,487 | 474 |
| 389 | 0807NurDinHaythami.MaqsadAli | 142,449 | 474 |
| 390 | 1390MuhsinTabatabai.DalilNasik | 142,329 | 474 |
| 391 | 0751IbQayyimJawziyya.TariqHijratayn | 142,292 | 474 |
| 392 | 0385IbnNadim.Fihrist | 141,796 | 472 |
| 393 | 0463IbnCabdBarr.JamicBayan | 141,492 | 471 |
| 394 | 0945ShamsDinDawudi.TabaqatMufassirin | 139,971 | 466 |
| 395 | 1376CabdRahmanSacdi.Muallafat | 139,967 | 466 |
| 396 | 0181IbnMubarak.Zuhd | 139,950 | 466 |
| 397 | 0351IbnQanic.MucjamSahaba | 139,882 | 466 |
| 398 | 0578IbnBashkuwal.Sila | 139,365 | 464 |
| 399 | 0709CaliCalawi.Majdi | 138,926 | 463 |
| 400 | 0276IbnQutaybaDinawari.ShicrWaShucara | 137,744 | 459 |
| 401 | 0463IbnCabdBarr.BahjatMajalis | 137,584 | 458 |
| 402 | 0249Azraqi.AkhbarMakka | 136,671 | 455 |
| 403 | 0676Nawawi.RiyadSalihin | 136,428 | 454 |
| 404 | 0576IbnMuhammadSilafi.MashyakhaBaghdadiyya | 135,363 | 451 |
| 405 | 0245MuhammadIbnHabib.MunammaqFiAkhbarQuraysh | 135,021 | 450 |
| 406 | 0703MuhammadMarrakushi.DhaylWaTakmila | 133,973 | 446 |
| 407 | 1450SalihFawzan.MajmucFatawa | 133,824 | 446 |
| 408 | 1293CabdLatifAlShaykh.CuyunRasailwaAjwiba | 133,775 | 445 |
| 409 | 0911Suyuti.TarikhKhulafa | 133,130 | 443 |
| 410 | 0241IbnHanbal.FadailSahaba | 132,367 | 441 |
| 411 | 0369AbuShaykhIsbahani.TabaqatMuhaddithin | 132,061 | 440 |
| 412 | 0461IbnHusaynSughdi.NutafFifatawa | 131,713 | 439 |
| 413 | 1307Qannawji.HusnUswa | 131,192 | 437 |
| 414 | 0456IbnHazm.JamharaAnsab | 130,859 | 436 |
| 415 | 0597IbnJawzi.TalbisIblis | 130,487 | 434 |
| 416 | 0227IbnMansurKhurasani.Sunan | 129,476 | 431 |
| 417 | 0224AbuCubaydIbnSallam.Amwal | 128,905 | 429 |
| 418 | 0189MuhammadShaybani.HujjaCalaAhlMadina | 128,781 | 429 |
| 419 | 0911Suyuti.Muhadarat | 128,274 | 427 |
| 420 | 0852IbnHajarCasqalani.TacjilManfaca | 127,930 | 426 |
| 421 | 0094ZaynCabidin.SahifaSajjadiya | 127,633 | 425 |
| 422 | 0953IbnTulun.MufakahaKhillan | 127,338 | 424 |
| 423 | 0230CaliIbnJacd.Musnad | 126,950 | 423 |
| 424 | 0597IbnJawzi.GharibHadith | 126,650 | 422 |
| 425 | 1286IcjazHusaynKunturi.KashfHajb | 126,032 | 420 |
| 426 | 0395IbnMandahMuhammad.FathBab | 124,908 | 416 |
| 427 | 0279Baladhuri.FutuhBuldan | 124,892 | 416 |
| 428 | 0414AbuHayyanTawhidi.Imtac | 124,775 | 415 |
| 429 | 0428IbnManjuwayhIsbahani.RijalSahihMuslim | 124,175 | 413 |
| 430 | 0367IbnHawqal.SuraArd | 123,793 | 412 |
| 431 | 0884IbnMuflih.MaqsidArshad | 123,777 | 412 |
| 432 | 0581IbnCumarIsbahani.Lataif | 123,597 | 411 |
| 433 | 0852IbnHajarCasqalani.RafcCisr | 123,094 | 410 |
| 434 | 0597IbnJawzi.SaydKhatir | 122,967 | 409 |
| 435 | 1422MuqbilWadici.TarajimRijal | 122,531 | 408 |
| 436 | 0310Tabari.TahdhibAthar | 122,442 | 408 |
| 437 | 0276IbnQutaybaDinawari.Macarif | 121,880 | 406 |
| 438 | 0294IbnNasrMarwazi.TaczimQadrSalat | 121,812 | 406 |
| 439 | 0206IbnMirarShaybani.Jim | 121,563 | 405 |
| 440 | 1014IbnSultanHarawi.SharhMusnadAbiHanifa | 121,419 | 404 |
| 441 | 0565IbnZaydBayhaqi.TarikhBayhaq | 121,037 | 403 |
| 442 | 0555IbnQalanisi.Tarikh | 120,986 | 403 |
| 443 | 0676Nawawi.SharhArbacinaNawawi | 120,803 | 402 |
| 444 | 1400MuhammadBaqirSadr.FatawaWadiha | 120,795 | 402 |
| 445 | 0449AbuCalaMacarri.Diwan | 120,379 | 401 |
| 446 | 0429AbuMansurThacalibi.ThimarQulub | 119,721 | 399 |
| 447 | 0228IbnHammadKhuzaci.Fitan | 119,494 | 398 |
| 448 | 0851IbnQadiShuhba.TabaqatShaficiya | 119,436 | 398 |
| 449 | 0297IbnDawudZahiri.Zahra | 119,436 | 398 |
| 450 | 0748Dhahabi.MughniFiDucafa | 119,182 | 397 |
| 451 | 0403IbnFaradi.TarikhCulamaAndalus | 118,911 | 396 |
| 452 | 0575IbnKhayrIshbili.Fahrasa | 117,769 | 392 |
| 453 | 0771Subki.MucjamShuyukh | 117,371 | 391 |
| 454 | 0599IbnYahyaDabbi.BughyaMultamis | 116,987 | 389 |
| 455 | 0684IbnShaddad.AclaqKhatira | 116,670 | 388 |
| 456 | 0257IbnCabdHakam.FutuhMisr | 116,282 | 387 |
| 457 | 0241IbnHanbal.Zuhd | 116,143 | 387 |
| 458 | 0189MuhammadShaybani.JamicSaghir | 115,609 | 385 |
| 459 | 0427HamzaJurjani.TarikhJurjan | 114,881 | 382 |
| 460 | 0676Nawawi.KhulasatAhkam | 114,612 | 382 |
| 461 | 0799IbnFarhun.DibajMudhahhab | 114,355 | 381 |
| 462 | 1037CabdQadirCaydarus.TarikhNurSafir | 113,966 | 379 |
| 463 | 1270ShihabDinAlusi.GharaibIghtirab | 113,165 | 377 |
| 464 | 0233YahyaIbnMacin.TarikhIbnMacin | 112,871 | 376 |
| 465 | 0629IbnNuqta.TaqyidLiMacrifa | 112,296 | 374 |
| 466 | 1313VanDyck.IktifaQunuc | 112,098 | 373 |
| 467 | 0774IbnKathir.MusnadCumarIbnKhattab | 112,095 | 373 |
| 468 | 0213IbnHisham.Tijan | 111,971 | 373 |
| 469 | 0300IbnJacfarHimyari.QurbIsnad | 111,668 | 372 |
| 470 | 0571IbnCasakir.TarjamatHusayn | 111,626 | 372 |
| 471 | 0440AbuRayhanBiruni.TahqiqMaLilHind | 111,411 | 371 |
| 472 | 0751IbQayyimJawziyya.HadiArwah | 110,951 | 369 |
| 473 | 1346CbdQadirBadran.Munadama | 110,741 | 369 |
| 474 | 0660IbnCadim.ZubdaHalab | 110,479 | 368 |
| 475 | 0578IbnBashkuwal.GhawamidAsma | 110,027 | 366 |
| 476 | 0354IbnHibban.Sira | 109,974 | 366 |
| 477 | 0285IbrahimHarbi.GharibHadith | 109,595 | 365 |
| 478 | 0561Samcani.Tahbir | 109,525 | 365 |
| 479 | 0685IbnSacidMaghribi.Mughrib | 109,402 | 364 |
| 480 | 0413ShaykhMufid.Amali | 109,089 | 363 |
| 481 | 0685IbnCibri.TarikhMukhtasarDuwal | 109,030 | 363 |
| 482 | 1421MuhammadCuthaymin.FatawaArkanIslam | 108,365 | 361 |
| 483 | 0240KhalifaIbnKhayyat.Tarikh | 108,050 | 360 |
| 484 | 0337QudamaIbnJacfar.Kharaj | 106,955 | 356 |
| 485 | 0726CallamaHilli.KhulasaAqwal | 106,878 | 356 |
| 486 | 0249CabdIbnHamid.MuntakhabMinMusnad | 106,574 | 355 |
| 487 | 0911Suyuti.TanwirHawalik | 106,252 | 354 |
| 488 | 0300MuallifMajhul.AkhbarDawlaCabbasiya | 106,130 | 353 |
| 489 | 0122ZaydIbnCali.MusnadZayd | 106,101 | 353 |
| 490 | 0748Dhahabi.DiwanDucafa | 105,284 | 350 |
| 491 | 0761IbnKaykaldiDimashqi.ItharatFawaid | 104,474 | 348 |
| 492 | 1307Qannawji.NaylMaram | 104,303 | 347 |
| 493 | 0911Suyuti.ShamailSharifa | 103,995 | 346 |
| 494 | 0571IbnCasakir.TarjamatHasan | 103,718 | 345 |
| 495 | 0748Dhahabi.MukhtasarMinDubaythi | 103,004 | 343 |
| 496 | 0240KhalifaIbnKhayyat.Tabaqat | 102,233 | 340 |
| 497 | 0911Suyuti.QutMughtadhi | 102,034 | 340 |
| 498 | 0597IbnJawzi.DucafaWaMatrukin | 100,991 | 336 |
| 499 | 0597IbnJawzi.Mudhish | 100,987 | 336 |
| 500 | 0204Shafici.Musnad | 100,909 | 336 |
| 501 | 0324Ashcari.MaqalatIslamiyyin | 100,191 | 333 |
| 502 | 1450CadilNuwayhid.MucjamAclamJazair | 100,098 | 333 |
| 503 | 0227IbnMansurKhurasani.TafsirMinSunanSacid | 99,781 | 332 |
| 504 | 0658IbnAbbar.HullaSiyara | 98,508 | 328 |
| 505 | 0390Muqaddasi.AhsanTaqasim | 98,198 | 327 |
| 506 | 0833IbnJazari.SharhTayyibaNashr | 98,149 | 327 |
| 507 | 0507AbuBakrShashi.HilyaCulama | 98,130 | 327 |
| 508 | 0282AbuHanifaDinawari.AkhbarTiwal | 97,880 | 326 |
| 509 | 0576IbnMuhammadSilafi.MucjamSafar | 97,869 | 326 |
| 510 | 0748Dhahabi.MacrifaQurraKibar | 97,714 | 325 |
| 511 | 0821Qalqashandi.NihayaArab | 97,039 | 323 |
| 512 | 0646IbnQifti.IkhbarCulama | 96,909 | 323 |
| 513 | 0641Sarifini.Muntakhab | 96,486 | 321 |
| 514 | 0575IbnBabawayh.Fihrist | 96,438 | 321 |
| 515 | 1041BurhanDinMaliki.BahjaMahafil | 96,298 | 320 |
| 516 | 0854IbnDiyaMakki.TarikhMakka | 96,272 | 320 |
| 517 | 0804IbnMulaqqin.TuhfaMuhtaj | 95,932 | 319 |
| 518 | 0448HilalSabi.TuhfaUmara | 95,725 | 319 |
| 519 | 0600AbuBaqaHilli.ManaqibMazidiya | 95,644 | 318 |
| 520 | 0280IbnIsmacilKirmani.MasailHarb | 95,312 | 317 |
| 521 | 0751IbQayyimJawziyya.RuhFiKalam | 94,694 | 315 |
| 522 | 0751IbQayyimJawziyya.RawdatMuhibbin | 94,055 | 313 |
| 523 | 0312IbnCaliTusi.MukhtasarAhkam | 93,252 | 310 |
| 524 | 0580IbnCimrani.InbaFiTarikhKhulafa | 92,814 | 309 |
| 525 | 0245MuhammadIbnHabib.Muhabbar | 91,282 | 304 |
| 526 | 0751IbQayyimJawziyya.TibbNabawi | 91,222 | 304 |
| 527 | 0282HarithHaythami.BughyaBahith | 91,203 | 304 |
| 528 | 0911Suyuti.SharhSudur | 90,965 | 303 |
| 529 | 0104MujahidIbnJabr.Tafsir | 90,882 | 302 |
| 530 | 0398AbuNasrKalabadhi.HidayaWaIrshad | 90,817 | 302 |
| 531 | 0395IbnMandahMuhammad.MacrifaSahaba | 90,565 | 301 |
| 532 | 0571IbnCasakir.TabyinKadhb | 90,478 | 301 |
| 533 | 0741KhatibTabrizi.Ikmal | 90,307 | 301 |
| 534 | 0236AbuCabdAllahZubayri.NasabQuraysh | 90,262 | 300 |
| 535 | 0450Najashi.Rijal | 90,256 | 300 |
| 536 | 1031CabdRaufMunawi.Tawqif | 90,082 | 300 |
| 537 | 0280CuthmanIbnSacidDarimi.NaqdImam | 89,633 | 298 |
| 538 | 0204IbnKalbi.NasabMacad | 88,977 | 296 |
| 539 | 1330IbnMusaTabrizi.MiratKutub | 88,818 | 296 |
| 540 | 0460ShaykhTusi.Rijal | 88,503 | 295 |
| 541 | 1354HasanSadr.Takmila | 88,094 | 293 |
| 542 | 0290IbnAhmadIbnHanbal.Sunna | 87,822 | 292 |
| 543 | 0751IbQayyimJawziyya.DaWaDawa | 87,602 | 292 |
| 544 | 0346Mascudi.TanbihWaIshraf | 87,579 | 291 |
| 545 | 1225IbnNasirNajdi.MajmucatRasail | 86,793 | 289 |
| 546 | 0256Bukhari.AdabMufrad | 86,503 | 288 |
| 547 | 0256Bukhari.TarikhSaghir | 86,362 | 287 |
| 548 | 0384IbnCimranMarzubani.MucjamShucara | 86,047 | 286 |
| 549 | 0597IbnJawzi.BustanWacizin | 85,753 | 285 |
| 550 | 0256ZubayrIbnBakkar.AkhbarMuwaffaqiyat | 85,750 | 285 |
| 551 | 0774IbnKathir.TalkhisKitabIstighatha | 85,496 | 284 |
| 552 | 1424IhsanCabbas.ShadharatMinKutubMafquda | 85,480 | 284 |
| 553 | 0255Jahiz.Cuthmaniya | 85,453 | 284 |
| 554 | 0488IbnFutuhHumaydi.JadhwaMuqtabis | 85,167 | 283 |
| 555 | 0751IbQayyimJawziyya.TuruqHukmiyya | 84,928 | 283 |
| 556 | 0597CimadDinKatib.BarqShami | 84,900 | 283 |
| 557 | 0219IbnZubayrHumaydi.Musnad | 84,690 | 282 |
| 558 | 0528FathIbnKhaqan.QalaidCiqyan | 84,437 | 281 |
| 559 | 1389AghaBuzurgTihrani.TASHNawabighRuwat | 84,082 | 280 |
| 560 | 0540AbuMansurJawaliqi.SharhAdabKatib | 83,991 | 279 |
| 561 | 0446AbuYaclaKhalili.IrshadFiMacrifaCulama | 82,456 | 274 |
| 562 | 0656IbnAbiHadid.FalakDair | 82,158 | 273 |
| 563 | 0694MuhibbDinTabari.Dhakhair | 81,328 | 271 |
| 564 | 0597IbnJawzi.MuthirGharam | 81,078 | 270 |
| 565 | 0273IbnMaja.SharhMuqaddimaSunan | 80,715 | 269 |
| 566 | 1100MuhammadItlidi.IclamNas | 80,344 | 267 |
| 567 | 0292Bahshal.TarikhWasit | 80,039 | 266 |
| 568 | 0806IbnHusaynCiraqi.Taqyid | 79,924 | 266 |
| 569 | 1153IbnKannan.YawmiyyatShamiyya | 79,567 | 265 |
| 570 | 0751IbQayyimJawziyya.TibyanFiAqsamQuran | 79,486 | 264 |
| 571 | 0276IbnQutaybaDinawari.TawilMukhtalafHadith | 79,395 | 264 |
| 572 | 0751IbQayyimJawziyya.CuddatSabirin | 78,339 | 261 |
| 573 | 1450SadiqRuhani.MasailMuntakhaba | 77,666 | 258 |
| 574 | 0182AbuYusufYacqub.Kharaj | 77,392 | 257 |
| 575 | 0676Nawawi.MinhajTalibin | 77,131 | 257 |
| 576 | 0748Dhahabi.Muqtana | 77,096 | 256 |
| 577 | 0261AbuHasanCijli.MacrifaThiqat | 76,492 | 254 |
| 578 | 0658IbnAbbar.MucjamAshab | 76,471 | 254 |
| 579 | 0761IbnKaykaldi.JamicTahsil | 76,460 | 254 |
| 580 | 0565IbnZaydBayhaqi.LubabAnsab | 76,424 | 254 |
| 581 | 0463IbnCabdBarr.Durar | 76,336 | 254 |
| 582 | 0749IbnWardi.KharidaCajaib | 75,947 | 253 |
| 583 | 0281AbuZurcaDimashqi.Tarikh | 75,765 | 252 |
| 584 | 0751IbQayyimJawziyya.JalaAfham | 75,694 | 252 |
| 585 | 0346Istakhri.MasalikWaMamalik | 75,599 | 251 |
| 586 | 0733IbnJamaca.Mashyakha | 75,126 | 250 |
| 587 | 0381AbuQasimJawhari.MusnadMuwatta | 74,413 | 248 |
| 588 | 0614IbnJubayr.Rihla | 74,329 | 247 |
| 589 | 0764Safadi.NaktHimyan | 74,306 | 247 |
| 590 | 0904Burayhi.TabaqatSulahaYaman | 74,213 | 247 |
| 591 | 0405HakimNaysaburi.MacrifatCulumHadith | 73,931 | 246 |
| 592 | 0751IbQayyimJawziyya.HidayatHayara | 73,901 | 246 |
| 593 | 0767Balawi.TajMafriq | 73,852 | 246 |
| 594 | 0911Suyuti.TabaqatHuffaz | 73,614 | 245 |
| 595 | 1418MuhammadRuhani.MasailMuntakhaba | 73,342 | 244 |
| 596 | 0241IbnHanbal.MasailRiwayaIbnih | 73,202 | 244 |
| 597 | 0535QawwamSunna.DalailNubuwwa | 72,728 | 242 |
| 598 | 0854IbnCarabshah.CajaibMaqdur | 72,705 | 242 |
| 599 | 0224AbuCubaydIbnSallam.NasikhWaMansukh | 72,201 | 240 |
| 600 | 1174AbuBarakatSuwaydi.NafhaMiskiya | 71,961 | 239 |
| 601 | 0723IbnFuwati.Hawadith | 71,739 | 239 |
| 602 | 0730MuhammadTujibi.Barnamaj | 71,375 | 237 |
| 603 | 0748Dhahabi.MukhtasarCuluww | 71,152 | 237 |
| 604 | 0334IbnHaikHamdani.SifaJaziraCarab | 70,929 | 236 |
| 605 | 0647CabdWahidMarrakushi.Mucjib | 70,871 | 236 |
| 606 | 0255Jahiz.MahasinWaAddad | 70,477 | 234 |
| 607 | 0333AbuCarabTamimi.Mihan | 70,365 | 234 |
| 608 | 0261Muslim.KunaWaAsma | 70,202 | 234 |
| 609 | 0243HannadIbnSari.Zuhd | 70,052 | 233 |
| 610 | 0296IbnMuctazz.TabaqatShucara | 69,665 | 232 |
| 611 | 0276IbnQutaybaDinawari.AdabKatib | 69,368 | 231 |
| 612 | 0597IbnJawzi.NawasikhQuran | 69,080 | 230 |
| 613 | 1147CabdAllahSancani.TarikhYaman | 69,040 | 230 |
| 614 | 0234IbnAbiShayba.Musnad | 68,957 | 229 |
| 615 | 0673AbuMahasinYaghmuri.NurQabas | 68,955 | 229 |
| 616 | 0750AbuHafsQazwini.Mashyakha | 68,872 | 229 |
| 617 | 0412Sulami.TabaqatSufiya | 68,774 | 229 |
| 618 | 1195CabdRahmanAnsari.Tuhfa | 68,557 | 228 |
| 619 | 0241IbnHanbal.MasailRiwayaSalih | 68,468 | 228 |
| 620 | 0740IbnDawudHilli.Rijal | 68,088 | 226 |
| 621 | 1307Qannawji.HittaFiDhikr | 67,880 | 226 |
| 622 | 1421HamdJasir.MucjamQabailMCS | 67,689 | 225 |
| 623 | 0281IbnAbiDunya.MaqtalCali | 67,018 | 223 |
| 624 | 0597IbnJawzi.DafcShubahTashbih | 66,255 | 220 |
| 625 | 0690IbnMujawirDimashqi.TarikhMustabsir | 65,633 | 218 |
| 626 | 0639AbuBakrMalaqi.MatlacAnwar | 65,139 | 217 |
| 627 | 0597IbnJawzi.Adhkiya | 65,051 | 216 |
| 628 | 0584IbnMusaHazimi.Amakin | 64,697 | 215 |
| 629 | 1307Qannawji.BulghaFuUsulLugha | 64,209 | 214 |
| 630 | 0816AbuBakrMaraghi.Mashyakha | 64,167 | 213 |
| 631 | 0346Mascudi.AkhbarZaman | 63,951 | 213 |
| 632 | 0291IbnYahyaThaclab.MajalisThaclab | 63,917 | 213 |
| 633 | 0911Suyuti.LubabNuqul | 63,669 | 212 |
| 634 | 1232IbnKhatibCumari.RawdaFayha | 63,383 | 211 |
| 635 | 0643IbnSalahShahrazuri.TabaqatFuqaha | 63,126 | 210 |
| 636 | 0597IbnJawzi.NuzhatAcyun | 63,056 | 210 |
| 637 | 0826IbnCiraqi.TuhfaTahsil | 62,996 | 209 |
| 638 | 0458Bayhaqi.Ictiqad | 62,880 | 209 |
| 639 | 1450CabdRahmanAlShaykh.Mashahir | 62,418 | 208 |
| 640 | 0871IbnFahdMakki.LahzAlhaz | 62,047 | 206 |
| 641 | 0793AbuHasanMalaqi.TarikhQudat | 62,043 | 206 |
| 642 | 0276IbnQutaybaDinawari.GharibQuran | 61,726 | 205 |
| 643 | 0938IbnCaliBalawi.Thabat | 61,539 | 205 |
| 644 | 0276IbnQutaybaDinawari.TawilMushkilQuran | 61,443 | 204 |
| 645 | 0774IbnRaficSallami.Wafayat | 61,135 | 203 |
| 646 | 0597IbnJawzi.TadhkiratArib | 60,775 | 202 |
| 647 | 0600KatibMarrakushi.Istibsar | 60,550 | 201 |
| 648 | 0310Tabari.IkhtilafFuqaha | 60,548 | 201 |
| 649 | 0521MuhammadHamadhani.TakmilaTarikhTabari | 60,016 | 200 |
| 650 | 0414AbuHayyanTawhidi.AkhlaqWazirayn | 59,746 | 199 |
| 651 | 1307Qannawji.LuqtaCajlan | 59,600 | 198 |
| 652 | 0874IbnTaghribirdi.MawridLatafa | 59,510 | 198 |
| 653 | 0414AbuHayyanTawhidi.Muqabasat | 59,313 | 197 |
| 654 | 1338MuhammadFaridBey.Bahja | 59,305 | 197 |
| 655 | 0714AhmadGhibrini.CunwanDiraya | 58,461 | 194 |
| 656 | 0751IbQayyimJawziyya.Furusiyya | 58,088 | 193 |
| 657 | 0395AbuHilalCaskari.Talkhis | 57,835 | 192 |
| 658 | 1069ShihabDinKhafaji.RayhanaAlibba | 57,614 | 192 |
| 659 | 0911Suyuti.LubbLubab | 57,394 | 191 |
| 660 | 0646IbnQifti.Muhammadun | 57,364 | 191 |
| 661 | 0255Jahiz.BursanWaCurjan | 57,316 | 191 |
| 662 | 0751IbQayyimJawziyya.MatnQasidaNuniyya | 57,221 | 190 |
| 663 | 0751IbQayyimJawziyya.IjtimacJuyush | 57,215 | 190 |
| 664 | 0204Shafici.IkhtilafHadith | 57,125 | 190 |
| 665 | 0276IbnQutaybaDinawari.Jarathim | 57,100 | 190 |
| 666 | 0256ZubayrIbnBakkar.JamharaNasabQuraysh | 56,650 | 188 |
| 667 | 0310Tabari.MuntakhabMinDhayl | 56,329 | 187 |
| 668 | 0429AbuMansurThacalibi.FiqhLugha | 56,313 | 187 |
| 669 | 0751IbQayyimJawziyya.Fawaid | 56,135 | 187 |
| 670 | 0808IbnKhaldun.Rihla | 55,833 | 186 |
| 671 | 1167IbnCabrRahmanGhazzi.DiwanIslam | 55,685 | 185 |
| 672 | 0909IbnMibradHanbali.BahrDamm | 55,202 | 184 |
| 673 | 0255Jahiz.Bukhala | 55,171 | 183 |
| 674 | 0475IbnMakula.TahdhibMustamirr | 55,129 | 183 |
| 675 | 0231IbnSallamJumahi.TabaqatFuhulShucara | 54,921 | 183 |
| 676 | 0776LisanDinIbnKhatib.KatibaKamina | 54,854 | 182 |
| 677 | 0804IbnMulaqqin.TabaqatAwliya | 54,595 | 181 |
| 678 | 0765AbuMahasinHusayni.IkmalLiRijal | 54,306 | 181 |
| 679 | 0505Ghazali.Mankhul | 54,192 | 180 |
| 680 | 0911Suyuti.ItmamDiraya | 54,179 | 180 |
| 681 | 0280IbnTayfur.BallaghatNisa | 53,601 | 178 |
| 682 | 1014IbnSultanHarawi.AsrarMarfuca | 52,534 | 175 |
| 683 | 1277MuhammadTantawi.NashaNahw | 52,381 | 174 |
| 684 | 0776LisanDinIbnKhatib.NafadaJirab | 52,268 | 174 |
| 685 | 0884SibtIbnCajami.KashfHathith | 52,220 | 174 |
| 686 | 0256Bukhari.SharhKitabFitan | 52,174 | 173 |
| 687 | 0300IbnZakariyaHajari.Tacliqat | 52,074 | 173 |
| 688 | 0748Dhahabi.Culuww | 51,813 | 172 |
| 689 | 0370IbnBishrAmidi.MutalifWaMukhtalif | 51,486 | 171 |
| 690 | 1381MuhammadSancani.MulhaqBadr | 51,442 | 171 |
| 691 | 0782IbnSallar.TabaqatQurra | 51,171 | 170 |
| 692 | 0296IbnMuctazz.Diwan | 51,131 | 170 |
| 693 | 1307Qannawji.Yaqza | 51,107 | 170 |
| 694 | 0606IbnMamati.LataifDhakhira | 51,074 | 170 |
| 695 | 0751IbQayyimJawziyya.TuhfatMawdud | 51,068 | 170 |
| 696 | 0355MuhammadKindi.WulatMisr | 50,996 | 169 |
| 697 | 1070MuhammadKibrit.RihlaShita | 50,647 | 168 |
| 698 | 0654SibtIbnJawzi.ItharInsaf | 50,626 | 168 |
| 699 | 0550AbuHajjajAshcari.TacrifBiAnsab | 50,496 | 168 |
| 700 | 0748Dhahabi.TalkhisMawducatIbnJawzi | 50,388 | 167 |
| 701 | 0748IbnDimyati.Mustafad | 50,153 | 167 |
| 702 | 0833IbnJazari.ManaqibAsadGhalib | 50,044 | 166 |
| 703 | 0429AbuMansurThacalibi.Tamthil | 49,580 | 165 |
| 704 | 0204Shafici.AhkamQuran | 49,550 | 165 |
| 705 | 0806IbnHusaynCiraqi.DhaylMizan | 49,484 | 164 |
| 706 | 0505Ghazali.Tahafut | 49,401 | 164 |
| 707 | 0505Ghazali.MicyarCilm | 49,099 | 163 |
| 708 | 0774IbnKathir.TuhfatTalib | 49,042 | 163 |
| 709 | 0280IbnTayfur.Baghdad | 48,570 | 161 |
| 710 | 0676Nawawi.IdahFiManasikHajj | 48,035 | 160 |
| 711 | 0505Ghazali.Fadaih | 47,692 | 158 |
| 712 | 0611SharafDinMuqaddasi.Arbacin | 47,514 | 158 |
| 713 | 0833IbnJazari.TahbirTaysir | 47,020 | 156 |
| 714 | 0569CumaraHakami.NukatCasriyya | 47,005 | 156 |
| 715 | 0984BardDinGhazzi.MatalicBadriya | 46,951 | 156 |
| 716 | 0414AbuHayyanTawhidi.Sadaqa | 46,821 | 156 |
| 717 | 0696CumarSunami.NisabIhtisab | 46,622 | 155 |
| 718 | 1258IbnCabdSalamTusuli.AjwibatTusuli | 46,225 | 154 |
| 719 | 0182AbuYusufYacqub.Athar | 45,995 | 153 |
| 720 | 0429AbuMansurThacalibi.Rasail | 45,809 | 152 |
| 721 | 0327IbnAbiHatimRazi.BayanKhataBukhari | 45,706 | 152 |
| 722 | 0751IbQayyimJawziyya.Salat | 45,614 | 152 |
| 723 | 0168MufaddalDabbi.AmthalCarab | 45,465 | 151 |
| 724 | 0354IbnHibban.MashahirCulamaAmsar | 45,365 | 151 |
| 725 | 0617MansurIbnShahanshah.MidmarHaqaiq | 45,270 | 150 |
| 726 | 0233YahyaIbnMacin.MacrifaRijal | 45,156 | 150 |
| 727 | 0749Wadiashi.Barnamaj | 44,950 | 149 |
| 728 | 0224IbnSallamBaghdadi.Amthal | 44,597 | 148 |
| 729 | 0297IbnAbiShayba.Carsh | 44,255 | 147 |
| 730 | 1450MuhammadHadiAmini.MucjamMatbicatNajafiya | 44,242 | 147 |
| 731 | 0748Dhahabi.MucjamMuhaddithin | 44,241 | 147 |
| 732 | 0751IbQayyimJawziyya.WabilSayyib | 44,173 | 147 |
| 733 | 0335Suli.AshcarAwladKhulafa | 44,151 | 147 |
| 734 | 0505Ghazali.Iqtisad | 43,770 | 145 |
| 735 | 0577IbnAnbari.NuzhaAlibba | 43,683 | 145 |
| 736 | 0922IbnShaykhTarabulusi.IscafAwqaf | 43,648 | 145 |
| 737 | 0429AbuMansurThacalibi.LataifWaZaraif | 43,612 | 145 |
| 738 | 0852IbnHajarCasqalani.NuzhaAlbab | 43,292 | 144 |
| 739 | 0285IbnYazidMubarrad.Tacazi | 42,980 | 143 |
| 740 | 0584IbnMunqidhShayzari.Ictibar | 42,824 | 142 |
| 741 | 0597IbnJawzi.BirrWaSila | 42,768 | 142 |
| 742 | 0507IbnQaysarani.AnsabMuttafiqa | 42,469 | 141 |
| 743 | 1364IbnHamdMughiri.MuntakhabQabail | 42,407 | 141 |
| 744 | 0429AbuMansurThacalibi.SihrBalagha | 42,361 | 141 |
| 745 | 0597IbnJawzi.AkhbarNisa | 42,278 | 140 |
| 746 | 0680IbnSabuni.TakmilaIkmalIkmal | 42,252 | 140 |
| 747 | 0244IbnSikkit.KanzLughawi | 41,978 | 139 |
| 748 | 0676Nawawi.TahrirAlfaz | 41,558 | 138 |
| 749 | 0300IbnKhurdadhbih.MasalikWaMamalik | 41,035 | 136 |
| 750 | 0436HusaynSaymari.AkhbarAbiHanifa | 41,024 | 136 |
| 751 | 0337IbnIshaqZajjaji.Akhbar | 40,895 | 136 |
| 752 | 1100IbnMuhammadAdnahwi.TabaqatMufassirin | 40,783 | 135 |
| 753 | 0335Suli.AdabKuttab | 40,702 | 135 |
| 754 | 0476AbuIshaqShirazi.TabaqatFuqaha | 40,668 | 135 |
| 755 | 1282AbaButayn.RasailWaFatawa | 39,985 | 133 |
| 756 | 0281IbnAbiDunya.SamtWaAdab | 39,899 | 132 |
| 757 | 0320CaribQurtubi.SilaTarikhTabari | 39,699 | 132 |
| 758 | 0774IbnKathir.FusulMinSira | 39,673 | 132 |
| 759 | 0905Basrawi.Tarikh | 39,659 | 132 |
| 760 | 0505Ghazali.MacarijQuds | 39,642 | 132 |
| 761 | 0429AbuMansurThacalibi.Muntahal | 39,453 | 131 |
| 762 | 0170AbuZaydQurashi.JamharaAshcarCarab | 39,365 | 131 |
| 763 | 0281IbnAbiDunya.Ciyal | 39,321 | 131 |
| 764 | 0203IbnSulaymanGhazi.MusnadRida | 39,283 | 130 |
| 765 | 1345IbnJacfarKattani.RisalaMustatrafa | 39,163 | 130 |
| 766 | 1414MuhammadRidaGulpayagani.IrshadSail | 39,093 | 130 |
| 767 | 0388Shabushti.Diyarat | 38,993 | 129 |
| 768 | 0294IbnNasrMarwazi.IkhtilafCulama | 38,921 | 129 |
| 769 | 0817IbnYacqubFiruzabadi.BulghaFiTarajim | 38,540 | 128 |
| 770 | 0281IbnAbiDunya.Zuhd | 38,461 | 128 |
| 771 | 0902Sakhawi.Buldaniyyat | 37,943 | 126 |
| 772 | 0207Waqidi.Ridda | 37,811 | 126 |
| 773 | 1347BashirYamut.Shacirat | 37,705 | 125 |
| 774 | 1389AghaBuzurgTihrani.TASHAnwarSatica | 37,497 | 124 |
| 775 | 0748Dhahabi.DhaylCibar | 37,477 | 124 |
| 776 | 0429AbuMansurThacalibi.KhassKhass | 37,474 | 124 |
| 777 | 0276IbnQutaybaDinawari.AnwaFiMawasim | 37,309 | 124 |
| 778 | 0463KhatibBaghdadi.SabiqWaLahiq | 37,301 | 124 |
| 779 | 0597IbnJawzi.HamqaWaMughallifin | 36,714 | 122 |
| 780 | 0463IbnCabdBarr.IntiqaFiFadail | 36,504 | 121 |
| 781 | 0774IbnKathir.FadailQuran | 36,176 | 120 |
| 782 | 0200IbnCumarDabbi.Fitna | 35,573 | 118 |
| 783 | 0685IbnSacidMaghribi.Jughrafiya | 35,291 | 117 |
| 784 | 0275AbuDawud.Zuhd | 35,250 | 117 |
| 785 | 0573NashwanHimyari.KhulasaSiyar | 35,216 | 117 |
| 786 | 0379MuhammadRabci.TarikhMawlidCulama | 35,176 | 117 |
| 787 | 0657IbnIbrahimIrbili.MudhakaraFiAlqab | 35,060 | 116 |
| 788 | 0597IbnJawzi.TadhkiraFiWacz | 34,984 | 116 |
| 789 | 1373AbuYaclaZuwawi.TarikhZuwawa | 34,902 | 116 |
| 790 | 0505Ghazali.MaqsadAsna | 34,718 | 115 |
| 791 | 1450SadiqRuhani.TakmilaMinhajSalihin | 34,593 | 115 |
| 792 | 1414MuhammadRidaGulpayagani.MukhtasarAhkam | 34,163 | 113 |
| 793 | 0161SufyanThawri.Tafsir | 33,688 | 112 |
| 794 | 0243HarithMuhasibi.FahmQuran | 33,600 | 112 |
| 795 | 0505Ghazali.JawahirQuran | 33,456 | 111 |
| 796 | 0197IbnWahbQurashi.JamicFiHadith | 33,382 | 111 |
| 797 | 1418MuhammadRuhani.ManasikHajj | 33,338 | 111 |
| 798 | 1450SadiqRuhani.ManasikHajj | 33,192 | 110 |
| 799 | 0505Ghazali.MizanCamal | 33,154 | 110 |
| 800 | 1078RiyadZadah.AsmaKutub | 33,076 | 110 |
| 801 | 1413TajDinKhui.TakmilatMinhajSalihin | 32,881 | 109 |
| 802 | 1175AhmadBudayri.HawadithDimashq | 32,858 | 109 |
| 803 | 0281IbnAbiDunya.MakarimAkhlaq | 32,838 | 109 |
| 804 | 1355AhmadTahtawi.TanbihWaIqaz | 32,723 | 109 |
| 805 | 0405HakimNaysaburi.TalkhisTarikhNaysabur | 32,674 | 108 |
| 806 | 0874IbnTaghribirdi.HawadithDahriya | 32,505 | 108 |
| 807 | 0626YaqutHamawi.Khazal | 32,504 | 108 |
| 808 | 0292Yacqubi.Buldan | 32,476 | 108 |
| 809 | 0189MuhammadShaybani.Siyar | 32,464 | 108 |
| 810 | 0385IbnShahin.TarikhAsmaThiqat | 31,929 | 106 |
| 811 | 0845Maqrizi.Bayan | 31,900 | 106 |
| 812 | 0911Suyuti.ManahilSafa | 31,678 | 105 |
| 813 | 0597IbnJawzi.TanwirGhabash | 31,590 | 105 |
| 814 | 0505Ghazali.TibrMasbuk | 31,540 | 105 |
| 815 | 0281IbnAbiDunya.IshrafFiManazil | 31,517 | 105 |
| 816 | 0911Suyuti.NazmCiqyan | 31,489 | 104 |
| 817 | 0429AbuMansurThacalibi.LubabAdab | 31,233 | 104 |
| 818 | 0597IbnJawzi.BahrDumuc | 31,132 | 103 |
| 819 | 0371AhmadJurjani.Mucjam | 31,101 | 103 |
| 820 | 0279Tirmidhi.ShamailMuhammadiya | 31,083 | 103 |
| 821 | 0676Nawawi.MasailManthura | 30,618 | 102 |
| 822 | 0821Qalqashandi.QalaidJuman | 30,592 | 101 |
| 823 | 1389AghaBuzurgTihrani.DhaylKashfZunun | 30,484 | 101 |
| 824 | 0387KatibKhwarizmi.MafatihCulum | 30,055 | 100 |
| 825 | 0328IbnCabdRabbihi.TabaicNisa | 30,047 | 100 |
| 826 | 0241IbnHanbal.Warac | 29,990 | 99 |
| 827 | 0248AbuHatimSijistani.Mucammarun | 29,938 | 99 |
| 828 | 0676Nawawi.IjazFiSharhSunanAbiDawud | 29,935 | 99 |
| 829 | 0203YahyaIbnAdam.Kharaj | 29,931 | 99 |
| 830 | 0214IbnCabdHakamMisri.SiraCumarIbnCabdCaziz | 29,897 | 99 |
| 831 | 0544CiyadIbnMusaYahsubi.Ghunya | 29,789 | 99 |
| 832 | 0168MufaddalDabbi.Mufaddaliyat | 29,565 | 98 |
| 833 | 0463KhatibBaghdadi.GhunyaMultamis | 29,514 | 98 |
| 834 | 1318AhmadDimashqi.MucjamAsmaAshya | 29,472 | 98 |
| 835 | 0611CaliHarawi.Isharat | 29,278 | 97 |
| 836 | 0197IbnWahbQurashi.MuwattaIbnWahb | 29,231 | 97 |
| 837 | 1354RashidRida.Manar | 29,042 | 96 |
| 838 | 0658IbnAbbar.TuhfaQadim | 28,899 | 96 |
| 839 | 0180IbnJacfarAnsari.HadithIsmacil | 28,810 | 96 |
| 840 | 0294IbnNasrMarwazi.Sunna | 28,589 | 95 |
| 841 | 0150AbuHanifa.Musnad | 28,573 | 95 |
| 842 | 0902Sakhawi.ManhalCadhb | 28,425 | 94 |
| 843 | 0333AbuCarabTamimi.TabaqatCulama | 28,320 | 94 |
| 844 | 0264AbyZurca.Ducafa | 28,257 | 94 |
| 845 | 0181IbnMubarak.Jihad | 27,914 | 93 |
| 846 | 0324Ashcari.RisalaIlaAhlThughr | 27,802 | 92 |
| 847 | 0334IbnHaikHamdani.Iklil | 27,740 | 92 |
| 848 | 0911Suyuti.LumcaFiKhasaisJumca | 27,412 | 91 |
| 849 | 0275AbuDawudSijistani.Marasil | 27,377 | 91 |
| 850 | 0650IbnNazifHamawi.TarikhMansuri | 27,313 | 91 |
| 851 | 0505Ghazali.MahkNazar | 26,750 | 89 |
| 852 | 0324Ashcari.Ibana | 26,624 | 88 |
| 853 | 0597IbnJawzi.QussasWaMudhakkirin | 26,592 | 88 |
| 854 | 0879IbnQutlubugha.TajTarajim | 26,463 | 88 |
| 855 | 1450WizaraAwqafMisriyya.TarajimMujaza | 26,409 | 88 |
| 856 | 0429AbuMansurThacalibi.IcjazWaIjaz | 26,325 | 87 |
| 857 | 0842IbnNasirDinDimashqi.RaddWafir | 26,176 | 87 |
| 858 | 0402MuhammadSaydawi.MucjamShuyukh | 26,156 | 87 |
| 859 | 0310IbnAhmadDulabi.Dhariyya | 26,063 | 86 |
| 860 | 1414SalimIbadi.IscafAcyan | 25,921 | 86 |
| 861 | 0597IbnJawzi.IclamMacalim | 25,913 | 86 |
| 862 | 0170KhalilFarahidi.JumalFiNahw | 25,879 | 86 |
| 863 | 0281IbnAbiDunya.Manamat | 25,799 | 85 |
| 864 | 0632IsmacilMarwazi.FakhriFiAnsab | 25,627 | 85 |
| 865 | 0597IbnJawzi.FununAfnan | 25,581 | 85 |
| 866 | 0255Jahiz.TajFiAkhlaq | 25,314 | 84 |
| 867 | 0256Bukhari.KhalqAfcal | 25,289 | 84 |
| 868 | 0281IbnAbiDunya.SifaJanna | 25,012 | 83 |
| 869 | 0978QasimQunawi.AnisFuqaha | 24,912 | 83 |
| 870 | 1014IbnSultanHarawi.RaddCalaQailinBiWahdatWujud | 24,574 | 81 |
| 871 | 1307Qannawji.QatfThamar | 24,292 | 80 |
| 872 | 0281IbnAbiDunya.Muhtadirin | 24,191 | 80 |
| 873 | 0676Nawawi.Tibyan | 24,167 | 80 |
| 874 | 0728IbnTaymiyya.FatawaHamawiyya | 24,002 | 80 |
| 875 | 0243HarithMuhasibi.AdabNufus | 23,958 | 79 |
| 876 | 0505Ghazali.SirrCalamin | 23,943 | 79 |
| 877 | 0748Dhahabi.MucinFiTabaqatMuhaddithin | 23,934 | 79 |
| 878 | 0929IbnKayyal.KawakibNayyirat | 23,699 | 78 |
| 879 | 1285IbnHasanTamimi.RasailWaFatawa | 23,607 | 78 |
| 880 | 0833IbnJazari.ZahrFaih | 23,508 | 78 |
| 881 | 0281IbnAbiDunya.IslahMal | 23,364 | 77 |
| 882 | 0188IbnMuhammadFazari.Siyar | 23,317 | 77 |
| 883 | 0584IbnMusaHazimi.CujalaMubtadi | 23,180 | 77 |
| 884 | 1429BakrIbnCabdAllah.TabaqatNassabin | 23,042 | 76 |
| 885 | 1086IbnCajamiMisri.DhaylLubbLubab | 22,972 | 76 |
| 886 | 0337QudamaIbnJacfar.NaqdShicr | 22,928 | 76 |
| 887 | 0576IbnMuhammadSilafi.Mashyakha | 22,872 | 76 |
| 888 | 0774IbnKathir.IkhtisarCulumHadith | 22,788 | 75 |
| 889 | 0662RashidAttar.NuzhatNazir | 22,772 | 75 |
| 890 | 0368AbuGhalibZurari.Risala | 22,769 | 75 |
| 891 | 0418WazirMaghribi.AdabKhawas | 22,658 | 75 |
| 892 | 0418WazirMaghribi.Inas | 22,614 | 75 |
| 893 | 0776LisanDinIbnKhatib.MicyarIkhtiyar | 22,471 | 74 |
| 894 | 0246DicbilKhuzaci.WasayaMuluk | 22,453 | 74 |
| 895 | 0209MacmarIbnMuthanna.Khayl | 22,392 | 74 |
| 896 | 0911Suyuti.DhaylTabaqatHuffaz | 22,369 | 74 |
| 897 | 0833IbnJazari.TamhidFiCulumTajwid | 22,299 | 74 |
| 898 | 0286IbnWaddahQurtubi.Bidac | 22,150 | 73 |
| 899 | 0640AbuHafsDunaysiri.TarikhDunaysir | 22,117 | 73 |
| 900 | 0285IbnYazidMubarrad.Fadil | 22,006 | 73 |
| 901 | 1336CabdHamidThani.MudhakkaratiSiyasiya | 21,875 | 72 |
| 902 | 0303Nasai.FadailSahaba | 21,802 | 72 |
| 903 | 0385IbnShahin.TarikhAsmaDucafa | 21,637 | 72 |
| 904 | 0238IbnHabibQurtubi.MukhtasarFiTibb | 21,535 | 71 |
| 905 | 0597IbnJawzi.ThibatCindaMamat | 21,524 | 71 |
| 906 | 0848IbnSarrajAndalusi.Fatawa | 21,504 | 71 |
| 907 | 0732AbuFida.Yawaqit | 21,381 | 71 |
| 908 | 0307AbuYaclaMawsili.Mucjam | 21,376 | 71 |
| 909 | 0330Sirafi.Rihla | 21,280 | 70 |
| 910 | 0281IbnAbiDunya.QasrAmal | 21,280 | 70 |
| 911 | 0429AbuMansurThacalibi.Shakwa | 21,139 | 70 |
| 912 | 0335Suli.AkhbarAbiTamam | 21,133 | 70 |
| 913 | 1206IbnCabdWahhab.Fatawa | 21,127 | 70 |
| 914 | 0204IbnKalbi.JamharaAnsab | 21,042 | 70 |
| 915 | 0182AbuYusufYacqub.IkhtilafAbiHanifa | 20,921 | 69 |
| 916 | 0287Dahhak.Jihad | 20,872 | 69 |
| 917 | 0181IbnMubarak.Musnad | 20,839 | 69 |
| 918 | 0287Dahhak.Diyat | 20,555 | 68 |
| 919 | 0281IbnAbiDunya.Hawatif | 20,452 | 68 |
| 920 | 0565IbnZaydBayhaqi.TatimmaSiwanHikma | 20,359 | 67 |
| 921 | 0833IbnJazari.MunjidMuqriyyin | 20,355 | 67 |
| 922 | 0515IbnQattac.DurraKhatira | 20,292 | 67 |
| 923 | 0238IbnHabibQurtubi.AdabNisa | 19,971 | 66 |
| 924 | 1307Qannawji.NashwatSakran | 19,854 | 66 |
| 925 | 0281IbnAbiDunya.Ahwal | 19,849 | 66 |
| 926 | 0385Daruqutni.DhikrAsmaTabicin | 19,767 | 65 |
| 927 | 0429AbuMansurThacalibi.MutanabbiWaMaLahu | 19,725 | 65 |
| 928 | 0656IbnAbiHadid.RawdaMukhtara | 19,714 | 65 |
| 929 | 0328IbnCabdRabbihi.Diwan | 19,627 | 65 |
| 930 | 0281IbnAbiDunya.ShukrLiLlah | 19,626 | 65 |
| 931 | 1014IbnSultanHarawi.ShammCawarid | 19,624 | 65 |
| 932 | 0241IbnHanbal.RaddCalaZanadiqa | 19,410 | 64 |
| 933 | 0748Dhahabi.DhikrAsmaManTakallama | 19,394 | 64 |
| 934 | 0505Ghazali.QawaidCaqaid | 19,315 | 64 |
| 935 | 0571IbnCasakir.ArbacunaBuldaniyya | 19,310 | 64 |
| 936 | 0380Muhallabi.MasalikWaMamalik | 18,868 | 62 |
| 937 | 0629IbnNuqta.IfadaWaIctibar | 18,784 | 62 |
| 938 | 0911Suyuti.LumacFiAsbabHadith | 18,722 | 62 |
| 939 | 0385Daruqutni.SualatBarqani | 18,719 | 62 |
| 940 | 0597IbnJawzi.ZirafWaMutamajinin | 18,698 | 62 |
| 941 | 0466CabdAzizKattani.DhaylTarikhMawlidCulama | 18,658 | 62 |
| 942 | 0463IbnCabdBarr.InbahCalaQabail | 18,464 | 61 |
| 943 | 0505Ghazali.MishkatAnwar | 18,447 | 61 |
| 944 | 0309IbnFadlan.Rihla | 18,416 | 61 |
| 945 | 0911Suyuti.TahdhirKhawass | 18,396 | 61 |
| 946 | 0189MuhammadShaybani.Kasb | 18,319 | 61 |
| 947 | 0255Jahiz.Bighal | 18,305 | 61 |
| 948 | 0677SahibTaji.HalbaFiAsmaKhayl | 18,268 | 60 |
| 949 | 0296MuhammadIbnJarrah.ManIsmuhCamr | 18,234 | 60 |
| 950 | 0272IbnIshaqFakihi.HadithFakihi | 18,015 | 60 |
| 951 | 0334IbnSacidQushayri.TarikhRaqqa | 17,955 | 59 |
| 952 | 0310Nawbakhti.FiraqShica | 17,929 | 59 |
| 953 | 0281IbnAbiDunya.Warac | 17,890 | 59 |
| 954 | 0290IbnAhmadIbnHanbal.FadailCuthman | 17,868 | 59 |
| 955 | 0676Nawawi.Taqrib | 17,766 | 59 |
| 956 | 0676Nawawi.BustanCarifin | 17,605 | 58 |
| 957 | 1016MuhibbDinHamawi.HadiAzcan | 17,554 | 58 |
| 958 | 0597IbnJawzi.Lataif | 17,506 | 58 |
| 959 | 0246HusaynMarwazi.BirrWaSila | 17,399 | 57 |
| 960 | 0597IbnJawzi.Mashyakha | 17,396 | 57 |
| 961 | 0469IbnHayyanQurtubi.Muqtabas | 17,127 | 57 |
| 962 | 0355AbuFarajIsbahani.Diyarat | 17,102 | 57 |
| 963 | 1014IbnSultanHarawi.AhadithQudsiyya | 17,034 | 56 |
| 964 | 0216IbnQuraybAsmaci.Asmaciyat | 16,956 | 56 |
| 965 | 0197IbnWahbQurashi.QadaMinMuwattaIbnWahb | 16,920 | 56 |
| 966 | 1218SalihFulani.QatfThamar | 16,905 | 56 |
| 967 | 0691IbnYusufLabli.Fihrist | 16,803 | 56 |
| 968 | 0635AbuMunajjaIbnLatti.Mashyakha | 16,784 | 55 |
| 969 | 0911Suyuti.IscafMubatta | 16,433 | 54 |
| 970 | 0751IbQayyimJawziyya.AmthalFiQuran | 16,339 | 54 |
| 971 | 0244IbnSikkit.QalbWaIbdal | 16,333 | 54 |
| 972 | 0498AbuCaliJayyani.TaqyidMuhmal | 16,017 | 53 |
| 973 | 0281IbnAbiDunya.Cuzla | 15,993 | 53 |
| 974 | 0806IbnHusaynCiraqi.AlfiyyatSira | 15,885 | 52 |
| 975 | 0405HakimNaysaburi.TasmiyaManAkhrajahum | 15,868 | 52 |
| 976 | 0456IbnHazm.FadailAndalus | 15,744 | 52 |
| 977 | 0685IbnSacidMaghribi.GhusunYanica | 15,713 | 52 |
| 978 | 0538MahmudZamakhshari.JibalWaAmkina | 15,676 | 52 |
| 979 | 0281IbnAbiDunya.SifaNar | 15,634 | 52 |
| 980 | 0189MuhammadShaybani.Athar | 15,601 | 52 |
| 981 | 0806IbnHusaynCiraqi.ArbacunaCushariyya | 15,498 | 51 |
| 982 | 0833IbnJazari.Cawali | 15,458 | 51 |
| 983 | 0281IbnAbiDunya.MaradWaKaffarat | 15,458 | 51 |
| 984 | 0751IbQayyimJawziyya.ManarMunif | 15,443 | 51 |
| 985 | 0765AbuMahasinHusayni.DhaylTadhkira | 15,407 | 51 |
| 986 | 0234IbnAbiShayba.Adab | 15,353 | 51 |
| 987 | 0429AbuMansurThacalibi.AhsanMaSamictu | 15,268 | 50 |
| 988 | 0256Bukhari.QiraaKhalfaImam | 14,995 | 49 |
| 989 | 0911Suyuti.MiftahJanna | 14,940 | 49 |
| 990 | 0292IbnCaliMarwazi.MusnadAbiBakr | 14,869 | 49 |
| 991 | 0276IbnQutaybaDinawari.AshribaWaIkhtilafFiha | 14,830 | 49 |
| 992 | 0209IbnMuthannaTaymi.Dibaj | 14,808 | 49 |
| 993 | 1126MuhammadHanbali.Mashyakha | 14,775 | 49 |
| 994 | 0281AbuZurcaDimashqi.FawaidMucallala | 14,744 | 49 |
| 995 | 0041LabidIbnRabica.Diwan | 14,717 | 49 |
| 996 | 0659SainDinNaccal.Mashyakha | 14,631 | 48 |
| 997 | 0505Ghazali.BidayatHidaya | 14,542 | 48 |
| 998 | 0909IbnMibradHanbali.MucjamKutub | 14,490 | 48 |
| 999 | 1418SalihAhmadArkani.TihfaMajalis | 14,467 | 48 |
| 1000 | 0246AhmadDawraqi.MusnadSacdIbnAbiWaqqas | 14,440 | 48 |
| 1001 | 0581IbnCumarIsbahani.MuntahaRaghabat | 14,322 | 47 |
| 1002 | 0430AbuNucaymIsbahani.Ducafa | 14,296 | 47 |
| 1003 | 0456IbnHazm.NaqtCarus | 14,078 | 46 |
| 1004 | 0265SalihIbnHanbal.SiraImam | 14,054 | 46 |
| 1005 | 0241IbnHanbal.SualatAbiDawudLiIbnHanbal | 13,820 | 46 |
| 1006 | 0360Khawlani.TarikhDaraya | 13,813 | 46 |
| 1007 | 0261Muslim.Munfaridat | 13,798 | 45 |
| 1008 | 0211AbuCatahiya.Diwan | 13,740 | 45 |
| 1009 | 0597IbnJawzi.Musalsalat | 13,511 | 45 |
| 1010 | 0281IbnAbiDunya.TawaducWaKhumul | 13,432 | 44 |
| 1011 | 0541IbnCatiyyaMuharibi.Fahrasa | 13,427 | 44 |
| 1012 | 0287Dahhak.Zuhd | 13,290 | 44 |
| 1013 | 0256Bukhari.Ducafa | 13,146 | 43 |
| 1014 | 0756TaqiDinSubki.IbrazHikam | 12,771 | 42 |
| 1015 | 0748Dhahabi.DhaylDiwanDucafa | 12,664 | 42 |
| 1016 | 0281IbnAbiDunya.MujabuDacwa | 12,654 | 42 |
| 1017 | 1450TarhibDawsari.MucjamMuallafatShaficiyya | 12,526 | 41 |
| 1018 | 1419MahmudTanahi.MujizFiMarajic | 12,525 | 41 |
| 1019 | 0676Nawawi.IctiqadSalafFiHuruf | 12,517 | 41 |
| 1020 | 0204Shafici.JimacCilm | 12,423 | 41 |
| 1021 | 0307AbuYaclaMawsili.Mafarid | 12,375 | 41 |
| 1022 | 0243HarithMuhasibi.Makasib | 12,299 | 40 |
| 1023 | 0281IbnAbiDunya.Awliya | 12,167 | 40 |
| 1024 | 0806IbnHusaynCiraqi.MustakhrajCalaMustadrak | 12,105 | 40 |
| 1025 | 0833IbnJazari.MatnTayyibaNashr | 12,067 | 40 |
| 1026 | 0429AbuMansurThacalibi.ManGhabaCanhuMutrib | 11,987 | 39 |
| 1027 | 0211CabdRazzakSancani.AmaliFiAthar | 11,952 | 39 |
| 1028 | 0429AbuMansurThacalibi.Lutf | 11,868 | 39 |
| 1029 | 0701SharafDinYunini.Mashyakha | 11,855 | 39 |
| 1030 | 0206AbuMuhammadQutrub.Azmina | 11,847 | 39 |
| 1031 | 0911Suyuti.TabaqatMufassirin | 11,806 | 39 |
| 1032 | 0285IbrahimHarbi.IkramDayf | 11,805 | 39 |
| 1033 | 0806IbnHusaynCiraqi.Alfiyya | 11,757 | 39 |
| 1034 | 0182AbuYusufYacqub.RaddCalaSiyarAwzaci | 11,742 | 39 |
| 1035 | 0281IbnAbiDunya.Tawba | 11,740 | 39 |
| 1036 | 0281IbnAbiDunya.Shukr | 11,617 | 38 |
| 1037 | 0234CaliIbnMadini.SualatIbnAbiShayba | 11,527 | 38 |
| 1038 | 0374IbnHusaynAzdi.Makhzun | 11,516 | 38 |
| 1039 | 0643DiyaDinMuqaddasi.FadailBaytMaqdis | 11,474 | 38 |
| 1040 | 0197IbnWahbQurashi.MuharabaMinMuwattaIbnWahb | 11,469 | 38 |
| 1041 | 0505Ghazali.Munqidh | 11,334 | 37 |
| 1042 | 0413ShaykhMufid.MasarShica | 11,320 | 37 |
| 1043 | 0281IbnAbiDunya.QadaHawaij | 11,251 | 37 |
| 1044 | 0281IbnAbiDunya.HusnZannBiLlah | 11,180 | 37 |
| 1045 | 0281IbnAbiDunya.HammWaHuzn | 11,128 | 37 |
| 1046 | 0385IbnShahin.DhikrManIkhtalafaCulama | 11,073 | 36 |
| 1047 | 0751IbQayyimJawziyya.RisalaTabukiyya | 11,072 | 36 |
| 1048 | 0310Tabari.TabsirFiMacalimDin | 11,022 | 36 |
| 1049 | 0576IbnMuhammadSilafi.Wajiz | 10,969 | 36 |
| 1050 | 0261Muslim.Tamyiz | 10,937 | 36 |
| 1051 | 1057IbnCallan.IthafFadil | 10,899 | 36 |
| 1052 | 0442Tanukhi.TarikhCulamaNahwiyyin | 10,863 | 36 |
| 1053 | 0195IbnFudaylDabbi.Duca | 10,827 | 36 |
| 1054 | 0168IbnTahman.Mashyakha | 10,822 | 36 |
| 1055 | 0597IbnJawzi.Muqliq | 10,803 | 36 |
| 1056 | 0256Bukhari.DucafaSaghir | 10,791 | 35 |
| 1057 | 0281IbnAbiDunya.FarajBacdaShidda | 10,784 | 35 |
| 1058 | 0241IbnHanbal.Ashriba | 10,784 | 35 |
| 1059 | 0287Dahhak.Awail | 10,752 | 35 |
| 1060 | 0444AbuFadlIbnMahdi.DhikrShuyukh | 10,738 | 35 |
| 1061 | 0215AkhfashAwsat.Qawafi | 10,645 | 35 |
| 1062 | 0400IshaqMunajjim.AkamMarjan | 10,606 | 35 |
| 1063 | 0463IbnCabdBarr.Insaf | 10,560 | 35 |
| 1064 | 0413ShaykhMufid.AhkamNisa | 10,517 | 35 |
| 1065 | 0117IbnDicamaSadusi.NasikhWaMansukh | 10,492 | 34 |
| 1066 | 0281IbnAbiDunya.IctibarWaAcqab | 10,485 | 34 |
| 1067 | 0628IbnCaliSanhaji.AkhbarMuluk | 10,423 | 34 |
| 1068 | 0255IbnAhmadQurtubi.Hajj | 10,408 | 34 |
| 1069 | 0571IbnCasakir.TacziyatMuslim | 10,396 | 34 |
| 1070 | 0405AbuFadlHarawi.MucjamFiMushtabah | 10,379 | 34 |
| 1071 | 0281IbnAbiDunya.Ikhwan | 10,356 | 34 |
| 1072 | 0728IbnTaymiyya.RasHusayn | 10,286 | 34 |
| 1073 | 0234CaliIbnMadini.Cilal | 10,252 | 34 |
| 1074 | 0368Sirafi.AkhbarNahwiyyin | 10,206 | 34 |
| 1075 | 0132HammamIbnMunabbih.Sahifa | 10,076 | 33 |
| 1076 | 1246IbnHamadBassam.DurarMafakhir | 10,058 | 33 |
| 1077 | 0246HishamSulami.HadithHisham | 9,959 | 33 |
| 1078 | 0281IbnAbiDunya.MuhasabaNafs | 9,949 | 33 |
| 1079 | 1014IbnSultanHarawi.Adilla | 9,893 | 32 |
| 1080 | 0374IbnHusaynAzdi.DhikrIsmKullAshab | 9,862 | 32 |
| 1081 | 0597IbnJawzi.Yaquta | 9,747 | 32 |
| 1082 | 0809IbnQunfudh.Wafayat | 9,725 | 32 |
| 1083 | 0245MuhammadIbnHabib.MukhtalafQabail | 9,630 | 32 |
| 1084 | 0429AbuMansurThacalibi.TahsinQabih | 9,612 | 32 |
| 1085 | 0774IbnKathir.AdabDukhulHammam | 9,495 | 31 |
| 1086 | 0498AbuCaliJayyani.AlqabSahaba | 9,492 | 31 |
| 1087 | 0281IbnAbiDunya.AmrBiMacruf | 9,329 | 31 |
| 1088 | 0219AbuNucaymIbnDykayn.Salat | 9,279 | 30 |
| 1089 | 0705SharafDinDimyatti.MucjamShuyukh | 9,252 | 30 |
| 1090 | 0281IbnAbiDunya.MudaratNas | 9,135 | 30 |
| 1091 | 0259IbnYacqubJuzjani.AhwalRijal | 9,088 | 30 |
| 1092 | 0195MuarrijSadusi.HadhfMinNasabQuraysh | 9,074 | 30 |
| 1093 | 0385Daruqutni.Ducafa | 9,054 | 30 |
| 1094 | 0282IbnIshaqJahdami.FadlSalat | 9,002 | 30 |
| 1095 | 0303Nasai.DhikrMudallisin | 8,949 | 29 |
| 1096 | 0852IbnHajarCasqalani.TabaqatMudallisin | 8,929 | 29 |
| 1097 | 0281IbnAbiDunya.DhammGhiba | 8,868 | 29 |
| 1098 | 0852IbnHajarCasqalani.ItharBiMacrifa | 8,858 | 29 |
| 1099 | 0245LuwaynMissisi.JuzHadith | 8,853 | 29 |
| 1100 | 0238MuhammadBarjlani.KaramWaJawd | 8,800 | 29 |
| 1101 | 0747MuhyiDinYunini.Mashyakha | 8,748 | 29 |
| 1102 | 0862IbnMuhammadMujari.Barnamaj | 8,697 | 28 |
| 1103 | 0262YacqubIbnShayba.MusnadCumarIbnKhattab | 8,689 | 28 |
| 1104 | 0852IbnHajarCasqalani.TacrifAhlTaqbis | 8,687 | 28 |
| 1105 | 0511IbnMandahYahya.MacrifaAsamiArdaf | 8,637 | 28 |
| 1106 | 0751IbnQayyimJawziyya.IghathaLahfan | 8,563 | 28 |
| 1107 | 0233YahyaIbnMacin.HadithYahya | 8,505 | 28 |
| 1108 | 0281IbnAbiDunya.Mutammanin | 8,481 | 28 |
| 1109 | 0281IbnAbiDunya.ManCashaBacdaMawt | 8,481 | 28 |
| 1110 | 0911Suyuti.Tatrif | 8,473 | 28 |
| 1111 | 0597IbnJawzi.Hathth | 8,462 | 28 |
| 1112 | 0318AbuCurubaHarrani.MuntaqaMinTabaqat | 8,422 | 28 |
| 1113 | 0676Nawawi.AdabFatwa | 8,353 | 27 |
| 1114 | 0385Daruqutni.SualatNaysaburi | 8,317 | 27 |
| 1115 | 0276IbnQutaybaDinawari.IkhtilafFiLafz | 8,312 | 27 |
| 1116 | 0597IbnJawzi.FadailQuds | 8,290 | 27 |
| 1117 | 0303Nasai.DucafaWaMatrukin | 8,237 | 27 |
| 1118 | 0301AbuBakrFaryabi.DalailNubuwwa | 8,230 | 27 |
| 1119 | 0291IbnYahyaThaclab.Fasih | 8,223 | 27 |
| 1120 | 0581IbnCumarIsbahani.DhikrIbnMandah | 7,923 | 26 |
| 1121 | 0001NabighaDhubyani.Diwan | 7,877 | 26 |
| 1122 | 0597IbnJawzi.Laali | 7,874 | 26 |
| 1123 | 0256Bukhari.QuraCaynanyn | 7,777 | 25 |
| 1124 | 0456IbnHazm.RisalaFiMaratibCulum | 7,743 | 25 |
| 1125 | 0312IbnMuhammadBaghandi.MusnadCumar | 7,742 | 25 |
| 1126 | 0365IbnCadiJurjani.AsamiManRawaCanhum | 7,679 | 25 |
| 1127 | 0234AbuHasanSacdi.TasmiyaManRuwiya | 7,575 | 25 |
| 1128 | 0308IbnIbrahimJundi.FadailMadina | 7,557 | 25 |
| 1129 | 0807IbnAhmarKhazraji.NafhaNisriniyya | 7,528 | 25 |
| 1130 | 0748Dhahabi.Radd | 7,489 | 24 |
| 1131 | 0281IbnAbiDunya.Rida | 7,481 | 24 |
| 1132 | 0255Jahiz.MukhtarFiRaddCalaNasara | 7,481 | 24 |
| 1133 | 0255Jahiz.AmilWaMamul | 7,425 | 24 |
| 1134 | 0243IbnYahyaCadani.Iman | 7,415 | 24 |
| 1135 | 0222IbnBakkarDabi.AkhbarWafidat | 7,319 | 24 |
| 1136 | 0597IbnJawzi.BirrWalidayn | 7,265 | 24 |
| 1137 | 1285CabdRahmanTamimi.Maqamat | 7,256 | 24 |
| 1138 | 1225IbnNasirNajdi.RasailWaFatawa | 7,178 | 23 |
| 1139 | 0355MuhammadKindi.FadailMisr | 7,140 | 23 |
| 1140 | 0256ZubayrIbnBakkar.Muntakhab | 7,125 | 23 |
| 1141 | 0191IbnQasimMisri.MajalisIbnQasim | 7,054 | 23 |
| 1142 | 0246IbnCumarDuri.JuzFihiQiraat | 7,050 | 23 |
| 1143 | 0482AbuIshaqHabbal.WafayatMisriyyin | 7,037 | 23 |
| 1144 | 0429AbuMansurThacalibi.DurarHikm | 6,924 | 23 |
| 1145 | 0884SibtIbnCajami.TabyinLiAsma | 6,877 | 22 |
| 1146 | 0581IbnCumarIsbahani.NuzhatHuffaz | 6,829 | 22 |
| 1147 | 0300IbnKhurdadhbih.MukhtarMinKitabLahw | 6,793 | 22 |
| 1148 | 0204HishamKalbi.Asnam | 6,772 | 22 |
| 1149 | 0676Nawawi.DaqaiqMinhaj | 6,752 | 22 |
| 1150 | 0258IbnYahyaNaysaburi.Juz | 6,744 | 22 |
| 1151 | 0281IbnAbiDunya.CaqlWaFadluh | 6,691 | 22 |
| 1152 | 0456IbnHazm.AsmaKhulafa | 6,660 | 22 |
| 1153 | 0309IbnMarzuban.DhammThuqala | 6,660 | 22 |
| 1154 | 0774IbnRaficSallami.MashyakhaBayani | 6,654 | 22 |
| 1155 | 0360AbuBakrAjurri.AkhbarAbiHafs | 6,629 | 22 |
| 1156 | 0301Bardiji.TabaqatAsma | 6,594 | 21 |
| 1157 | 0231IbnZiyadAcrabi.AsmaKhayl | 6,594 | 21 |
| 1158 | 0505Ghazali.AsnafMaghrurin | 6,558 | 21 |
| 1159 | 0204IbnKalbi.AnsabKhayl | 6,506 | 21 |
| 1160 | 0265IbnHarbMawsili.HadithSyfyanIbnCuyayna | 6,491 | 21 |
| 1161 | 0409CabdGhaniAzdi.KitabMutawarin | 6,452 | 21 |
| 1162 | 0597IbnJawzi.TarikhBaytMuqaddas | 6,394 | 21 |
| 1163 | 0309IbnMarzuban.FadlKilab | 6,359 | 21 |
| 1164 | 0281IbnAbiDunya.Hilm | 6,310 | 21 |
| 1165 | 0001TarafaIbnCabd.Diwan | 6,233 | 20 |
| 1166 | 0001ImruQays.Diwan | 6,224 | 20 |
| 1167 | 0303Nasai.TasmiyaShuyukh | 6,216 | 20 |
| 1168 | 0597IbnJawzi.Manthur | 6,211 | 20 |
| 1169 | 0571IbnCasakir.ArbacunaFiHathth | 6,196 | 20 |
| 1170 | 0287Dahhak.Salat | 6,159 | 20 |
| 1171 | 1450TarhibDawsari.MucjamMuallafatMalikiyya | 6,095 | 20 |
| 1172 | 0156IbnAbiCuruba.Manasik | 6,092 | 20 |
| 1173 | 0234AbuKhaythamaNisai.Cilm | 6,063 | 20 |
| 1174 | 0748Dhahabi.AhadithMukhtaraMinMawducat | 6,040 | 20 |
| 1175 | 0597IbnJawzi.MusaffaBiAkuff | 6,019 | 20 |
| 1176 | 0632AbyHafsSuhrawardi.Mashyakha | 6,008 | 20 |
| 1177 | 0241IbnHanbal.AsamiWaKuna | 5,950 | 19 |
| 1178 | 0911Suyuti.NuzhatJulasa | 5,898 | 19 |
| 1179 | 0825IbnQasimSabti.IkhtisarAkhbar | 5,839 | 19 |
| 1180 | 0198SufyanIbnCuyayna.JuzHadith | 5,786 | 19 |
| 1181 | 1014IbnSultanHarawi.TasliyyatAcma | 5,757 | 19 |
| 1182 | 0279Tirmidhi.CilalSaghir | 5,725 | 19 |
| 1183 | 0884SibtIbnCajami.Ightibat | 5,716 | 19 |
| 1184 | 0360Tabarani.Awail | 5,704 | 19 |
| 1185 | 0597IbnJawzi.HifzCumr | 5,669 | 18 |
| 1186 | 0463IbnCabdBarr.AdabMujalasa | 5,634 | 18 |
| 1187 | 0233YahyaIbnMacin.MinKalamFiRijal | 5,551 | 18 |
| 1188 | 0276IbnMukhalladQurtubi.MaRuwiyaFiHawd | 5,506 | 18 |
| 1189 | 0578IbnBashkuwal.MaRuwiyaFiHawd | 5,490 | 18 |
| 1190 | 0128IbnAbiHabibMisri.AhadithYazid | 5,422 | 18 |
| 1191 | 0243HarithMuhasibi.RisalaMustarshidin | 5,299 | 17 |
| 1192 | 0222IbnBakkarDabi.AkhbarWafidin | 5,286 | 17 |
| 1193 | 0248AbuHatimSijistani.Farq | 5,212 | 17 |
| 1194 | 0273AbuUmayyaTarsusi.MusnadCabdAllahIbnCumar | 5,144 | 17 |
| 1195 | 0597IbnJawzi.TaczimFutya | 5,050 | 16 |
| 1196 | 0281IbnAbiDunya.WajalWaTawaththuq | 5,029 | 16 |
| 1197 | 0197IbnWahbQurashi.Qadar | 5,009 | 16 |
| 1198 | 0852IbnHajarCasqalani.MucjamShaykhaMaryam | 4,980 | 16 |
| 1199 | 0238IbnHabibQurtubi.AshratSaca | 4,965 | 16 |
| 1200 | 0281IbnAbiDunya.DhammMuskir | 4,948 | 16 |
| 1201 | 0195IbnCamrSadusi.Amthal | 4,863 | 16 |
| 1202 | 1051Cimadi.RawdaRayya | 4,849 | 16 |
| 1203 | 0429AbuMansurThacalibi.Diwan | 4,829 | 16 |
| 1204 | 0911Suyuti.TakrirIstinad | 4,810 | 16 |
| 1205 | 0281IbnAbiDunya.CumrWaShayb | 4,768 | 15 |
| 1206 | 0281IbnAbiDunya.FadailRamadan | 4,673 | 15 |
| 1207 | 0751IbQayyimJawziyya.JawabFiSiyaghHamd | 4,621 | 15 |
| 1208 | 0243HarithMuhasibi.MahiyaCaql | 4,606 | 15 |
| 1209 | 0001TufaylGhanawi.Diwan | 4,570 | 15 |
| 1210 | 0751IbQayyimJawziyya.RisalaIlaAhadIkhwan | 4,567 | 15 |
| 1211 | 0200AbuShis.Diwan | 4,549 | 15 |
| 1212 | 0571IbnCasakir.MadhTawaduc | 4,490 | 14 |
| 1213 | 0751IbQayyimJawziyya.FaidaJalila | 4,424 | 14 |
| 1214 | 0410IbnMardawayh.ThalathaMajalis | 4,414 | 14 |
| 1215 | 0286Mubarrad.NasabCadnan | 4,412 | 14 |
| 1216 | 0241IbnHanbal.CaqidaRiwayaKhallal | 4,380 | 14 |
| 1217 | 0001HatimTai.Diwan | 4,359 | 14 |
| 1218 | 0571IbnCasakir.KashfMughatta | 4,241 | 14 |
| 1219 | 0262IbnCasimIsbahani.Juz | 4,197 | 13 |
| 1220 | 0524IbnAkfani.DhaylDhaylTarikhMawlidCulama | 4,178 | 13 |
| 1221 | 0852IbnHajarCasqalani.MasailAjabaCanha | 4,143 | 13 |
| 1222 | 0911Suyuti.FaddWica | 4,136 | 13 |
| 1223 | 0395IbnMandahMuhammad.Asami | 4,056 | 13 |
| 1224 | 0776LisanDinIbnKhatib.KhatraTayf | 3,992 | 13 |
| 1225 | 0911Suyuti.Shamarikh | 3,874 | 12 |
| 1226 | 0281IbnAbiDunya.DhammBaghy | 3,863 | 12 |
| 1227 | 0291IbnYahyaThaclab.QawacidShicr | 3,822 | 12 |
| 1228 | 0322KatibBaghdadi.TarikhAimma | 3,821 | 12 |
| 1229 | 0317AbuQasimBaghawi.TarikhWafatShuyukh | 3,802 | 12 |
| 1230 | 0911Suyuti.AsmaMukhadramin | 3,736 | 12 |
| 1231 | 0751IbnQayyimJawziya.AsmaMuallafatIbnTaymiya | 3,722 | 12 |
| 1232 | 0676Nawawi.ArbacunaNawawiyya | 3,714 | 12 |
| 1233 | 1172IbnKhalifaMasakini.Fahrasa | 3,704 | 12 |
| 1234 | 0374IbnHusaynAzdi.KunaLiManLaYucrafLahuIsm | 3,572 | 11 |
| 1235 | 0833IbnJazari.DurraMudiyya | 3,546 | 11 |
| 1236 | 0209AbuCaliAshyabBaghdadi.JuzAshyab | 3,426 | 11 |
| 1237 | 0505Ghazali.KimiyaSacada | 3,404 | 11 |
| 1238 | 0826IbnCiraqi.Mudallisin | 3,392 | 11 |
| 1239 | 0748Dhahabi.RuwatThiqat | 3,391 | 11 |
| 1240 | 0198SufyanIbnCuyayna.JuzFihiHadith | 3,380 | 11 |
| 1241 | 0751IbQayyimJawziyya.SifatMunafiqin | 3,344 | 11 |
| 1242 | 0761IbnKaykaldi.Mukhtalitin | 3,340 | 11 |
| 1243 | 0110HasanBasri.FadailMakka | 3,334 | 11 |
| 1244 | 0567IbnKhashshabBaghdadi.TarikhMawalidAimma | 3,254 | 10 |
| 1245 | 0281IbnAbiDunya.HilmMucawiya | 3,207 | 10 |
| 1246 | 0297IbnAbuShayba.JuzFihiMasail | 3,192 | 10 |
| 1247 | 0382IbnCabdAllahCaskari.AkhbarMusahhifin | 3,184 | 10 |
| 1248 | 0281IbnAbiDunya.Yaqin | 3,118 | 10 |
| 1249 | 0430AbuNucaymIsbahani.DhikrManIsmuhuShucba | 3,082 | 10 |
| 1250 | 0241IbnHanbal.MinSualatIbnMuhammadAthram | 3,020 | 10 |
| 1251 | 0581IbnCumarIsbahani.DhikrIbnAbiDunya | 2,998 | 9 |
| 1252 | 0571IbnCasakir.TabyinImtinan | 2,994 | 9 |
| 1253 | 0254MuammalIbnIhab.JuzMuammal | 2,965 | 9 |
| 1254 | 0310Tabari.SarihSunna | 2,940 | 9 |
| 1255 | 0287Dahhak.Mudhakkir | 2,938 | 9 |
| 1256 | 0581IbnCumarIsbahani.KhasaisMusnadAhmad | 2,908 | 9 |
| 1257 | 0270IbnCaffanKufi.AmaliWaQiraa | 2,804 | 9 |
| 1258 | 0400IbnCamashliqJacfari.JuzIbnCamashliq | 2,684 | 8 |
| 1259 | 0248AbuHatimSijistani.FuhulaShucara | 2,637 | 8 |
| 1260 | 0430AbuNucaymIsbahani.TasmiyaMaIntahaIlayna | 2,501 | 8 |
| 1261 | 0255Jahiz.TabsiraBiTijara | 2,497 | 8 |
| 1262 | 0597IbnJawzi.TanbihNaim | 2,463 | 8 |
| 1263 | 0216IbnQuraybAsmaci.Sha | 2,403 | 8 |
| 1264 | 0197WakicIbnJarrah.NuskhaWakic | 2,403 | 8 |
| 1265 | 0374IbnHusaynAzdi.AsmaManYucrafBiKunya | 2,362 | 7 |
| 1266 | 0276IbnQutaybaDinawari.RisalaKhatt | 2,337 | 7 |
| 1267 | 1014IbnSultanHarawi.FaydMucin | 2,321 | 7 |
| 1268 | 0597IbnJawzi.IkhbarAhlRusukh | 2,241 | 7 |
| 1269 | 0456IbnHazm.RisalaFiFutuhIslam | 2,234 | 7 |
| 1270 | 0911Suyuti.TadhkiratMutasi | 2,144 | 7 |
| 1271 | 0303Nasai.TasmiyaManLamYarwi | 2,100 | 7 |
| 1272 | 0911Suyuti.GhurarFiFadailCumar | 2,071 | 6 |
| 1273 | 1187SulaymanMahasini.HululTacab | 2,064 | 6 |
| 1274 | 0164MajishunMadani.Hajj | 2,034 | 6 |
| 1275 | 0926ZakariyaAnsari.HududCaniqa | 2,027 | 6 |
| 1276 | 0581IbnCumarIsbahani.TiwalatAkhbar | 2,004 | 6 |
| 1277 | 0643DiyaDinMuqaddasi.JuzAwham | 2,001 | 6 |
| 1278 | 0911Suyuti.RawdAniqFiFadlSiddiq | 1,983 | 6 |
| 1279 | 0911Suyuti.BastKaff | 1,961 | 6 |
| 1280 | 0571IbnCasakir.Tawba | 1,946 | 6 |
| 1281 | 0335Suli.JuzMinAhadith | 1,892 | 6 |
| 1282 | 0911Suyuti.SababWadc | 1,883 | 6 |
| 1283 | 0430AbuNucaymIsbahani.MajlisMinAmali | 1,871 | 6 |
| 1284 | 0241IbnHanbal.UsulSunna | 1,854 | 6 |
| 1285 | 0734IbnQaddahHarawi.MulhaqFatawa | 1,839 | 6 |
| 1286 | 0349IbnCumarMuqri.AkhbarNahwiyyin | 1,790 | 5 |
| 1287 | 0374IbnHusaynAzdi.ManWafaqaIsmuhuIsmAbihi | 1,753 | 5 |
| 1288 | 0676Nawawi.UsulWaDawabit | 1,716 | 5 |
| 1289 | 0175LaythIbnSacd.MajlisMinFawaid | 1,638 | 5 |
| 1290 | 0264IbnYahyaMuzani.SharhSunna | 1,602 | 5 |
| 1291 | 0245DhuNunMisri.Hadith | 1,513 | 5 |
| 1292 | 0275AbuDawudSijistani.RisalaIlaAhlMakka | 1,391 | 4 |
| 1293 | 0257IbnCurfaCabdi.AhadithCawali | 1,322 | 4 |
| 1294 | 0833IbnJazari.ManzumaJazariyya | 1,270 | 4 |
| 1295 | 0303Nasai.TasmiyaFuqaha | 1,162 | 3 |
| 1296 | 0001HarithIbnHilliza.Diwan | 1,148 | 3 |
| 1297 | 0911Suyuti.DafcTashnic | 1,129 | 3 |
| 1298 | _female_names_in_0902Sakhawi.DuLamic | 941 | 3 |
| 1299 | 0911Suyuti.RihNisrin | 795 | 2 |
| 1300 | 0272IbnCassamIsbahani.JuzIbnCassam | 739 | 2 |
| 1301 | 0456IbnHazm.UmmahatKhulafa | 693 | 2 |
| 1302 | 0303Nasai.Tabaqat | 612 | 2 |
| 1303 | 0581IbnCumarIsbahani.KalamCalaHadithIstilqa | 392 | 1 |
| 1304 | 0696Dabbagh.MacalimIman | 187 | 0 |
| 1305 | 1450MuhammadSancani.NaylWatar | 150 | 0 |


## Texts in chronological order (duplicates excluded)

| TextGroup URI | Words  | Pages (300 w/p) |
|:--- | ------:| -----:|
| 0001HarithIbnHilliza.Diwan | 1,148 | 3 |
| 0001HatimTai.Diwan | 4,359 | 14 |
| 0001ImruQays.Diwan | 6,224 | 20 |
| 0001NabighaDhubyani.Diwan | 7,877 | 26 |
| 0001TarafaIbnCabd.Diwan | 6,233 | 20 |
| 0001TufaylGhanawi.Diwan | 4,570 | 15 |
| 0040CaliIbnAbiTalib.NahjBalagha | 157,597 | 525 |
| 0041LabidIbnRabica.Diwan | 14,717 | 49 |
| 0094ZaynCabidin.SahifaSajjadiya | 127,633 | 425 |
| 0104MujahidIbnJabr.Tafsir | 90,882 | 302 |
| 0110HasanBasri.FadailMakka | 3,334 | 11 |
| 0110IbnSirin.MuntakhabKalamFiTafsirAhlam | 213,643 | 712 |
| 0117IbnDicamaSadusi.NasikhWaMansukh | 10,492 | 34 |
| 0122ZaydIbnCali.MusnadZayd | 106,101 | 353 |
| 0128IbnAbiHabibMisri.AhadithYazid | 5,422 | 18 |
| 0132HammamIbnMunabbih.Sahifa | 10,076 | 33 |
| 0150AbuHanifa.Musnad | 28,573 | 95 |
| 0150MuqatilIbnSulayman.TafsirMuqatil | 501,772 | 1,672 |
| 0156IbnAbiCuruba.Manasik | 6,092 | 20 |
| 0161SufyanThawri.Tafsir | 33,688 | 112 |
| 0164MajishunMadani.Hajj | 2,034 | 6 |
| 0168IbnTahman.Mashyakha | 10,822 | 36 |
| 0168MufaddalDabbi.AmthalCarab | 45,465 | 151 |
| 0168MufaddalDabbi.Mufaddaliyat | 29,565 | 98 |
| 0170AbuZaydQurashi.JamharaAshcarCarab | 39,365 | 131 |
| 0170KhalilFarahidi.Cayn | 494,216 | 1,647 |
| 0170KhalilFarahidi.JumalFiNahw | 25,879 | 86 |
| 0175LaythIbnSacd.MajlisMinFawaid | 1,638 | 5 |
| 0179MalikIbnAnas.MudawwanaKubra | 948,401 | 3,161 |
| 0179MalikIbnAnas.Muwatta | 259,815 | 866 |
| 0180IbnJacfarAnsari.HadithIsmacil | 28,810 | 96 |
| 0180Sibawayh.KitabSibawayh | 281,336 | 937 |
| 0181IbnMubarak.Jihad | 27,914 | 93 |
| 0181IbnMubarak.Musnad | 20,839 | 69 |
| 0181IbnMubarak.Zuhd | 139,950 | 466 |
| 0182AbuYusufYacqub.Athar | 45,995 | 153 |
| 0182AbuYusufYacqub.IkhtilafAbiHanifa | 20,921 | 69 |
| 0182AbuYusufYacqub.Kharaj | 77,392 | 257 |
| 0182AbuYusufYacqub.RaddCalaSiyarAwzaci | 11,742 | 39 |
| 0188IbnMuhammadFazari.Siyar | 23,317 | 77 |
| 0189MuhammadShaybani.Asl | 319,253 | 1,064 |
| 0189MuhammadShaybani.Athar | 15,601 | 52 |
| 0189MuhammadShaybani.HujjaCalaAhlMadina | 128,781 | 429 |
| 0189MuhammadShaybani.JamicSaghir | 115,609 | 385 |
| 0189MuhammadShaybani.Kasb | 18,319 | 61 |
| 0189MuhammadShaybani.Siyar | 32,464 | 108 |
| 0191IbnQasimMisri.MajalisIbnQasim | 7,054 | 23 |
| 0195IbnCamrSadusi.Amthal | 4,863 | 16 |
| 0195IbnFudaylDabbi.Duca | 10,827 | 36 |
| 0195MuarrijSadusi.HadhfMinNasabQuraysh | 9,074 | 30 |
| 0197IbnWahbQurashi.JamicFiHadith | 33,382 | 111 |
| 0197IbnWahbQurashi.MuharabaMinMuwattaIbnWahb | 11,469 | 38 |
| 0197IbnWahbQurashi.MuwattaIbnWahb | 29,231 | 97 |
| 0197IbnWahbQurashi.QadaMinMuwattaIbnWahb | 16,920 | 56 |
| 0197IbnWahbQurashi.Qadar | 5,009 | 16 |
| 0197WakicIbnJarrah.NuskhaWakic | 2,403 | 8 |
| 0198SufyanIbnCuyayna.JuzFihiHadith | 3,380 | 11 |
| 0198SufyanIbnCuyayna.JuzHadith | 5,786 | 19 |
| 0200AbuShis.Diwan | 4,549 | 15 |
| 0200IbnCumarDabbi.Fitna | 35,573 | 118 |
| 0203IbnSulaymanGhazi.MusnadRida | 39,283 | 130 |
| 0203YahyaIbnAdam.Kharaj | 29,931 | 99 |
| 0204AbuDawudTayalisi.Musnad | 177,566 | 591 |
| 0204HishamKalbi.Asnam | 6,772 | 22 |
| 0204IbnKalbi.AnsabKhayl | 6,506 | 21 |
| 0204IbnKalbi.JamharaAnsab | 21,042 | 70 |
| 0204IbnKalbi.NasabMacad | 88,977 | 296 |
| 0204Shafici.AhkamQuran | 49,550 | 165 |
| 0204Shafici.IkhtilafHadith | 57,125 | 190 |
| 0204Shafici.JimacCilm | 12,423 | 41 |
| 0204Shafici.Musnad | 100,909 | 336 |
| 0204Shafici.Risala | 183,244 | 610 |
| 0204Shafici.Umm | 1,258,325 | 4,194 |
| 0206AbuMuhammadQutrub.Azmina | 11,847 | 39 |
| 0206IbnMirarShaybani.Jim | 121,563 | 405 |
| 0207IbnZiyadFarra.MacaniQuran | 245,716 | 819 |
| 0207Waqidi.FutuhSham | 248,628 | 828 |
| 0207Waqidi.Maghazi | 264,920 | 883 |
| 0207Waqidi.Ridda | 37,811 | 126 |
| 0209AbuCaliAshyabBaghdadi.JuzAshyab | 3,426 | 11 |
| 0209IbnMuthannaTaymi.Dibaj | 14,808 | 49 |
| 0209MacmarIbnMuthanna.Khayl | 22,392 | 74 |
| 0211AbuCatahiya.Diwan | 13,740 | 45 |
| 0211CabdRazzakSancani.AmaliFiAthar | 11,952 | 39 |
| 0211CabdRazzakSancani.Musannaf | 1,267,117 | 4,223 |
| 0211CabdRazzakSancani.Tafsir | 145,718 | 485 |
| 0213IbnHisham.SiraNabawiyya | 295,600 | 985 |
| 0213IbnHisham.Tijan | 111,971 | 373 |
| 0214IbnCabdHakamMisri.SiraCumarIbnCabdCaziz | 29,897 | 99 |
| 0215AkhfashAwsat.Qawafi | 10,645 | 35 |
| 0216IbnQuraybAsmaci.Asmaciyat | 16,956 | 56 |
| 0216IbnQuraybAsmaci.Sha | 2,403 | 8 |
| 0219AbuNucaymIbnDykayn.Salat | 9,279 | 30 |
| 0219IbnZubayrHumaydi.Musnad | 84,690 | 282 |
| 0222IbnBakkarDabi.AkhbarWafidat | 7,319 | 24 |
| 0222IbnBakkarDabi.AkhbarWafidin | 5,286 | 17 |
| 0224AbuCubaydIbnSallam.Amwal | 128,905 | 429 |
| 0224AbuCubaydIbnSallam.GharibHadith | 203,348 | 677 |
| 0224AbuCubaydIbnSallam.NasikhWaMansukh | 72,201 | 240 |
| 0224IbnSallamBaghdadi.Amthal | 44,597 | 148 |
| 0227IbnMansurKhurasani.Sunan | 129,476 | 431 |
| 0227IbnMansurKhurasani.TafsirMinSunanSacid | 99,781 | 332 |
| 0228IbnHammadKhuzaci.Fitan | 119,494 | 398 |
| 0230CaliIbnJacd.Musnad | 126,950 | 423 |
| 0230IbnSacd.TabaqatKubra | 921,111 | 3,070 |
| 0231IbnSallamJumahi.TabaqatFuhulShucara | 54,921 | 183 |
| 0231IbnZiyadAcrabi.AsmaKhayl | 6,594 | 21 |
| 0233YahyaIbnMacin.HadithYahya | 8,505 | 28 |
| 0233YahyaIbnMacin.MacrifaRijal | 45,156 | 150 |
| 0233YahyaIbnMacin.MinKalamFiRijal | 5,551 | 18 |
| 0233YahyaIbnMacin.TarikhIbnMacin | 112,871 | 376 |
| 0234AbuHasanSacdi.TasmiyaManRuwiya | 7,575 | 25 |
| 0234AbuKhaythamaNisai.Cilm | 6,063 | 20 |
| 0234CaliIbnMadini.Cilal | 10,252 | 34 |
| 0234CaliIbnMadini.SualatIbnAbiShayba | 11,527 | 38 |
| 0234IbnAbiShayba.Adab | 15,353 | 51 |
| 0234IbnAbiShayba.Musnad | 68,957 | 229 |
| 0236AbuCabdAllahZubayri.NasabQuraysh | 90,262 | 300 |
| 0238IbnHabibQurtubi.AdabNisa | 19,971 | 66 |
| 0238IbnHabibQurtubi.AshratSaca | 4,965 | 16 |
| 0238IbnHabibQurtubi.MukhtasarFiTibb | 21,535 | 71 |
| 0238IbnRahawayh.Musnad | 174,827 | 582 |
| 0238MuhammadBarjlani.KaramWaJawd | 8,800 | 29 |
| 0240KhalifaIbnKhayyat.Tabaqat | 102,233 | 340 |
| 0240KhalifaIbnKhayyat.Tarikh | 108,050 | 360 |
| 0241IbnHanbal.AsamiWaKuna | 5,950 | 19 |
| 0241IbnHanbal.Ashriba | 10,784 | 35 |
| 0241IbnHanbal.CaqidaRiwayaKhallal | 4,380 | 14 |
| 0241IbnHanbal.CilalWaMacrifa | 214,328 | 714 |
| 0241IbnHanbal.FadailSahaba | 132,367 | 441 |
| 0241IbnHanbal.MasailRiwayaIbnih | 73,202 | 244 |
| 0241IbnHanbal.MasailRiwayaSalih | 68,468 | 228 |
| 0241IbnHanbal.MinSualatIbnMuhammadAthram | 3,020 | 10 |
| 0241IbnHanbal.Musnad | 1,778,094 | 5,926 |
| 0241IbnHanbal.RaddCalaZanadiqa | 19,410 | 64 |
| 0241IbnHanbal.SualatAbiDawudLiIbnHanbal | 13,820 | 46 |
| 0241IbnHanbal.UsulSunna | 1,854 | 6 |
| 0241IbnHanbal.Warac | 29,990 | 99 |
| 0241IbnHanbal.Zuhd | 116,143 | 387 |
| 0243HannadIbnSari.Zuhd | 70,052 | 233 |
| 0243HarithMuhasibi.AdabNufus | 23,958 | 79 |
| 0243HarithMuhasibi.FahmQuran | 33,600 | 112 |
| 0243HarithMuhasibi.MahiyaCaql | 4,606 | 15 |
| 0243HarithMuhasibi.Makasib | 12,299 | 40 |
| 0243HarithMuhasibi.RisalaMustarshidin | 5,299 | 17 |
| 0243IbnYahyaCadani.Iman | 7,415 | 24 |
| 0244IbnSikkit.KanzLughawi | 41,978 | 139 |
| 0244IbnSikkit.QalbWaIbdal | 16,333 | 54 |
| 0245DhuNunMisri.Hadith | 1,513 | 5 |
| 0245LuwaynMissisi.JuzHadith | 8,853 | 29 |
| 0245MuhammadIbnHabib.Muhabbar | 91,282 | 304 |
| 0245MuhammadIbnHabib.MukhtalafQabail | 9,630 | 32 |
| 0245MuhammadIbnHabib.MunammaqFiAkhbarQuraysh | 135,021 | 450 |
| 0246AhmadDawraqi.MusnadSacdIbnAbiWaqqas | 14,440 | 48 |
| 0246DicbilKhuzaci.WasayaMuluk | 22,453 | 74 |
| 0246HishamSulami.HadithHisham | 9,959 | 33 |
| 0246HusaynMarwazi.BirrWaSila | 17,399 | 57 |
| 0246IbnCumarDuri.JuzFihiQiraat | 7,050 | 23 |
| 0248AbuHatimSijistani.Farq | 5,212 | 17 |
| 0248AbuHatimSijistani.FuhulaShucara | 2,637 | 8 |
| 0248AbuHatimSijistani.Mucammarun | 29,938 | 99 |
| 0249Azraqi.AkhbarMakka | 136,671 | 455 |
| 0249CabdIbnHamid.MuntakhabMinMusnad | 106,574 | 355 |
| 0251IbnMansurKawsaj.Masail | 200,411 | 668 |
| 0251IbnZanjawayh.Amwal | 183,217 | 610 |
| 0254MuammalIbnIhab.JuzMuammal | 2,965 | 9 |
| 0255CabdAllahDarimi.Sunan | 209,282 | 697 |
| 0255IbnAhmadQurtubi.Hajj | 10,408 | 34 |
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
| 0256Bukhari.AdabMufrad | 86,503 | 288 |
| 0256Bukhari.Ducafa | 13,146 | 43 |
| 0256Bukhari.DucafaSaghir | 10,791 | 35 |
| 0256Bukhari.KhalqAfcal | 25,289 | 84 |
| 0256Bukhari.QiraaKhalfaImam | 14,995 | 49 |
| 0256Bukhari.QuraCaynanyn | 7,777 | 25 |
| 0256Bukhari.Sahih | 628,978 | 2,096 |
| 0256Bukhari.SharhKitabFitan | 52,174 | 173 |
| 0256Bukhari.TarikhKabir | 791,001 | 2,636 |
| 0256Bukhari.TarikhSaghir | 86,362 | 287 |
| 0256ZubayrIbnBakkar.AkhbarMuwaffaqiyat | 85,750 | 285 |
| 0256ZubayrIbnBakkar.JamharaNasabQuraysh | 56,650 | 188 |
| 0256ZubayrIbnBakkar.Muntakhab | 7,125 | 23 |
| 0257IbnCabdHakam.FutuhMisr | 116,282 | 387 |
| 0257IbnCurfaCabdi.AhadithCawali | 1,322 | 4 |
| 0258IbnYahyaNaysaburi.Juz | 6,744 | 22 |
| 0259IbnYacqubJuzjani.AhwalRijal | 9,088 | 30 |
| 0260IbnSahlTabari.FirdawsHikmaFiTibb | 152,376 | 507 |
| 0261AbuHasanCijli.MacrifaThiqat | 76,492 | 254 |
| 0261Muslim.KunaWaAsma | 70,202 | 234 |
| 0261Muslim.Munfaridat | 13,798 | 45 |
| 0261Muslim.Sahih | 523,024 | 1,743 |
| 0261Muslim.SharhKitabHajj | 246,757 | 822 |
| 0261Muslim.Tamyiz | 10,937 | 36 |
| 0262AbuZaydNumayri.TarikhMadina | 351,743 | 1,172 |
| 0262IbnCasimIsbahani.Juz | 4,197 | 13 |
| 0262YacqubIbnShayba.MusnadCumarIbnKhattab | 8,689 | 28 |
| 0264AbyZurca.Ducafa | 28,257 | 94 |
| 0264IbnYahyaMuzani.Mukhtasar | 179,308 | 597 |
| 0264IbnYahyaMuzani.SharhSunna | 1,602 | 5 |
| 0265IbnHarbMawsili.HadithSyfyanIbnCuyayna | 6,491 | 21 |
| 0265SalihIbnHanbal.SiraImam | 14,054 | 46 |
| 0270IbnCaffanKufi.AmaliWaQiraa | 2,804 | 9 |
| 0272Fakihi.AkhbarMakka | 269,999 | 899 |
| 0272IbnCassamIsbahani.JuzIbnCassam | 739 | 2 |
| 0272IbnIshaqFakihi.HadithFakihi | 18,015 | 60 |
| 0273AbuUmayyaTarsusi.MusnadCabdAllahIbnCumar | 5,144 | 17 |
| 0273IbnMaja.SharhMuqaddimaSunan | 80,715 | 269 |
| 0273IbnMaja.Sunan | 293,138 | 977 |
| 0274AhmadBarqi.Mahasin | 251,755 | 839 |
| 0275AbuDawud.Zuhd | 35,250 | 117 |
| 0275AbuDawudSijistani.Marasil | 27,377 | 91 |
| 0275AbuDawudSijistani.RisalaIlaAhlMakka | 1,391 | 4 |
| 0275AbuDawudSijistani.Sunan | 407,350 | 1,357 |
| 0276IbnMukhalladQurtubi.MaRuwiyaFiHawd | 5,506 | 18 |
| 0276IbnQutaybaDinawari.AdabKatib | 69,368 | 231 |
| 0276IbnQutaybaDinawari.AnwaFiMawasim | 37,309 | 124 |
| 0276IbnQutaybaDinawari.AshribaWaIkhtilafFiha | 14,830 | 49 |
| 0276IbnQutaybaDinawari.CuyunAkhbar | 232,763 | 775 |
| 0276IbnQutaybaDinawari.GharibHadith | 151,462 | 504 |
| 0276IbnQutaybaDinawari.GharibQuran | 61,726 | 205 |
| 0276IbnQutaybaDinawari.IkhtilafFiLafz | 8,312 | 27 |
| 0276IbnQutaybaDinawari.ImamaWaSiyasa | 162,038 | 540 |
| 0276IbnQutaybaDinawari.Jarathim | 57,100 | 190 |
| 0276IbnQutaybaDinawari.MacaniKabir | 168,017 | 560 |
| 0276IbnQutaybaDinawari.Macarif | 121,880 | 406 |
| 0276IbnQutaybaDinawari.RisalaKhatt | 2,337 | 7 |
| 0276IbnQutaybaDinawari.ShicrWaShucara | 137,744 | 459 |
| 0276IbnQutaybaDinawari.TawilMukhtalafHadith | 79,395 | 264 |
| 0276IbnQutaybaDinawari.TawilMushkilQuran | 61,443 | 204 |
| 0277AbuHatimRazi.JarhWaTacdil | 1,121,289 | 3,737 |
| 0277IbnSyfyanFasawi.MacrifaWaTarikh | 340,450 | 1,134 |
| 0279Baladhuri.AnsabAshraf | 1,128,932 | 3,763 |
| 0279Baladhuri.FutuhBuldan | 124,892 | 416 |
| 0279IbnAbiKhaythama.TarikhKabir | 155,627 | 518 |
| 0279Tirmidhi.CilalSaghir | 5,725 | 19 |
| 0279Tirmidhi.JamicSahih | 413,385 | 1,377 |
| 0279Tirmidhi.ShamailMuhammadiya | 31,083 | 103 |
| 0280CuthmanIbnSacidDarimi.NaqdImam | 89,633 | 298 |
| 0280IbnIsmacilKirmani.MasailHarb | 95,312 | 317 |
| 0280IbnTayfur.Baghdad | 48,570 | 161 |
| 0280IbnTayfur.BallaghatNisa | 53,601 | 178 |
| 0281AbuZurcaDimashqi.FawaidMucallala | 14,744 | 49 |
| 0281AbuZurcaDimashqi.Tarikh | 75,765 | 252 |
| 0281IbnAbiDunya.Ahwal | 19,849 | 66 |
| 0281IbnAbiDunya.AmrBiMacruf | 9,329 | 31 |
| 0281IbnAbiDunya.Awliya | 12,167 | 40 |
| 0281IbnAbiDunya.CaqlWaFadluh | 6,691 | 22 |
| 0281IbnAbiDunya.Ciyal | 39,321 | 131 |
| 0281IbnAbiDunya.CumrWaShayb | 4,768 | 15 |
| 0281IbnAbiDunya.Cuzla | 15,993 | 53 |
| 0281IbnAbiDunya.DhammBaghy | 3,863 | 12 |
| 0281IbnAbiDunya.DhammGhiba | 8,868 | 29 |
| 0281IbnAbiDunya.DhammMuskir | 4,948 | 16 |
| 0281IbnAbiDunya.FadailRamadan | 4,673 | 15 |
| 0281IbnAbiDunya.FarajBacdaShidda | 10,784 | 35 |
| 0281IbnAbiDunya.HammWaHuzn | 11,128 | 37 |
| 0281IbnAbiDunya.Hawatif | 20,452 | 68 |
| 0281IbnAbiDunya.Hilm | 6,310 | 21 |
| 0281IbnAbiDunya.HilmMucawiya | 3,207 | 10 |
| 0281IbnAbiDunya.HusnZannBiLlah | 11,180 | 37 |
| 0281IbnAbiDunya.IctibarWaAcqab | 10,485 | 34 |
| 0281IbnAbiDunya.Ikhwan | 10,356 | 34 |
| 0281IbnAbiDunya.IshrafFiManazil | 31,517 | 105 |
| 0281IbnAbiDunya.IslahMal | 23,364 | 77 |
| 0281IbnAbiDunya.MakarimAkhlaq | 32,838 | 109 |
| 0281IbnAbiDunya.ManCashaBacdaMawt | 8,481 | 28 |
| 0281IbnAbiDunya.Manamat | 25,799 | 85 |
| 0281IbnAbiDunya.MaqtalCali | 67,018 | 223 |
| 0281IbnAbiDunya.MaradWaKaffarat | 15,458 | 51 |
| 0281IbnAbiDunya.MudaratNas | 9,135 | 30 |
| 0281IbnAbiDunya.MuhasabaNafs | 9,949 | 33 |
| 0281IbnAbiDunya.Muhtadirin | 24,191 | 80 |
| 0281IbnAbiDunya.MujabuDacwa | 12,654 | 42 |
| 0281IbnAbiDunya.Mutammanin | 8,481 | 28 |
| 0281IbnAbiDunya.QadaHawaij | 11,251 | 37 |
| 0281IbnAbiDunya.QasrAmal | 21,280 | 70 |
| 0281IbnAbiDunya.Rida | 7,481 | 24 |
| 0281IbnAbiDunya.SamtWaAdab | 39,899 | 132 |
| 0281IbnAbiDunya.Shukr | 11,617 | 38 |
| 0281IbnAbiDunya.ShukrLiLlah | 19,626 | 65 |
| 0281IbnAbiDunya.SifaJanna | 25,012 | 83 |
| 0281IbnAbiDunya.SifaNar | 15,634 | 52 |
| 0281IbnAbiDunya.TawaducWaKhumul | 13,432 | 44 |
| 0281IbnAbiDunya.Tawba | 11,740 | 39 |
| 0281IbnAbiDunya.WajalWaTawaththuq | 5,029 | 16 |
| 0281IbnAbiDunya.Warac | 17,890 | 59 |
| 0281IbnAbiDunya.Yaqin | 3,118 | 10 |
| 0281IbnAbiDunya.Zuhd | 38,461 | 128 |
| 0282AbuHanifaDinawari.AkhbarTiwal | 97,880 | 326 |
| 0282HarithHaythami.BughyaBahith | 91,203 | 304 |
| 0282IbnIshaqJahdami.FadlSalat | 9,002 | 30 |
| 0285IbnYazidMubarrad.Fadil | 22,006 | 73 |
| 0285IbnYazidMubarrad.Tacazi | 42,980 | 143 |
| 0285IbrahimHarbi.GharibHadith | 109,595 | 365 |
| 0285IbrahimHarbi.IkramDayf | 11,805 | 39 |
| 0286IbnWaddahQurtubi.Bidac | 22,150 | 73 |
| 0286Mubarrad.NasabCadnan | 4,412 | 14 |
| 0287Dahhak.AhadWaMathani | 265,863 | 886 |
| 0287Dahhak.Awail | 10,752 | 35 |
| 0287Dahhak.Diyat | 20,555 | 68 |
| 0287Dahhak.Jihad | 20,872 | 69 |
| 0287Dahhak.Mudhakkir | 2,938 | 9 |
| 0287Dahhak.Salat | 6,159 | 20 |
| 0287Dahhak.Sunna | 172,108 | 573 |
| 0287Dahhak.Zuhd | 13,290 | 44 |
| 0290IbnAhmadIbnHanbal.FadailCuthman | 17,868 | 59 |
| 0290IbnAhmadIbnHanbal.Sunna | 87,822 | 292 |
| 0290IbnHasanSaffar.BasairDarajat | 157,407 | 524 |
| 0291IbnYahyaThaclab.Fasih | 8,223 | 27 |
| 0291IbnYahyaThaclab.MajalisThaclab | 63,917 | 213 |
| 0291IbnYahyaThaclab.QawacidShicr | 3,822 | 12 |
| 0292AbuBakrBazzar.BahrZakhkhar | 747,561 | 2,491 |
| 0292Bahshal.TarikhWasit | 80,039 | 266 |
| 0292IbnCaliMarwazi.MusnadAbiBakr | 14,869 | 49 |
| 0292Yacqubi.Buldan | 32,476 | 108 |
| 0292Yacqubi.TarikhYacqubi | 193,018 | 643 |
| 0294IbnNasrMarwazi.IkhtilafCulama | 38,921 | 129 |
| 0294IbnNasrMarwazi.Sunna | 28,589 | 95 |
| 0294IbnNasrMarwazi.TaczimQadrSalat | 121,812 | 406 |
| 0296IbnMuctazz.Diwan | 51,131 | 170 |
| 0296IbnMuctazz.TabaqatShucara | 69,665 | 232 |
| 0296MuhammadIbnJarrah.ManIsmuhCamr | 18,234 | 60 |
| 0297IbnAbiShayba.Carsh | 44,255 | 147 |
| 0297IbnAbuShayba.JuzFihiMasail | 3,192 | 10 |
| 0297IbnDawudZahiri.Zahra | 119,436 | 398 |
| 0300IbnJacfarHimyari.QurbIsnad | 111,668 | 372 |
| 0300IbnKhurdadhbih.MasalikWaMamalik | 41,035 | 136 |
| 0300IbnKhurdadhbih.MukhtarMinKitabLahw | 6,793 | 22 |
| 0300IbnZakariyaHajari.Tacliqat | 52,074 | 173 |
| 0300MuallifMajhul.AkhbarDawlaCabbasiya | 106,130 | 353 |
| 0301AbuBakrFaryabi.DalailNubuwwa | 8,230 | 27 |
| 0301Bardiji.TabaqatAsma | 6,594 | 21 |
| 0303Nasai.DhikrMudallisin | 8,949 | 29 |
| 0303Nasai.DucafaWaMatrukin | 8,237 | 27 |
| 0303Nasai.FadailSahaba | 21,802 | 72 |
| 0303Nasai.Tabaqat | 612 | 2 |
| 0303Nasai.TasmiyaFuqaha | 1,162 | 3 |
| 0303Nasai.TasmiyaManLamYarwi | 2,100 | 7 |
| 0303Nasai.TasmiyaShuyukh | 6,216 | 20 |
| 0306IbnHayyanDabbi.AkhbarQudat | 237,235 | 790 |
| 0307AbuYaclaMawsili.Mafarid | 12,375 | 41 |
| 0307AbuYaclaMawsili.Mucjam | 21,376 | 71 |
| 0308IbnIbrahimJundi.FadailMadina | 7,557 | 25 |
| 0309IbnFadlan.Rihla | 18,416 | 61 |
| 0309IbnMarzuban.DhammThuqala | 6,660 | 22 |
| 0309IbnMarzuban.FadlKilab | 6,359 | 21 |
| 0310IbnAhmadDulabi.Dhariyya | 26,063 | 86 |
| 0310IbnAhmadDulabi.KunaWaAsma | 186,967 | 623 |
| 0310Nawbakhti.FiraqShica | 17,929 | 59 |
| 0310Tabari.IkhtilafFuqaha | 60,548 | 201 |
| 0310Tabari.JamicBayan | 3,041,268 | 10,137 |
| 0310Tabari.MuntakhabMinDhayl | 56,329 | 187 |
| 0310Tabari.SarihSunna | 2,940 | 9 |
| 0310Tabari.TabsirFiMacalimDin | 11,022 | 36 |
| 0310Tabari.TahdhibAthar | 122,442 | 408 |
| 0310Tabari.Tarikh | 1,613,108 | 5,377 |
| 0312IbnCaliTusi.MukhtasarAhkam | 93,252 | 310 |
| 0312IbnMuhammadBaghandi.MusnadCumar | 7,742 | 25 |
| 0313IbnIshaqSarraj.Musnad | 146,495 | 488 |
| 0317AbuQasimBaghawi.MucjamSahaba | 218,356 | 727 |
| 0317AbuQasimBaghawi.TarikhWafatShuyukh | 3,802 | 12 |
| 0318AbuCurubaHarrani.MuntaqaMinTabaqat | 8,422 | 28 |
| 0320CaribQurtubi.SilaTarikhTabari | 39,699 | 132 |
| 0322AbuJacfarCuqayli.DucafaKabir | 314,435 | 1,048 |
| 0322KatibBaghdadi.TarikhAimma | 3,821 | 12 |
| 0324Ashcari.Ibana | 26,624 | 88 |
| 0324Ashcari.MaqalatIslamiyyin | 100,191 | 333 |
| 0324Ashcari.RisalaIlaAhlThughr | 27,802 | 92 |
| 0327IbnAbiHatimRazi.BayanKhataBukhari | 45,706 | 152 |
| 0328IbnCabdRabbihi.CiqdFarid | 562,475 | 1,874 |
| 0328IbnCabdRabbihi.Diwan | 19,627 | 65 |
| 0328IbnCabdRabbihi.TabaicNisa | 30,047 | 100 |
| 0330Sirafi.Rihla | 21,280 | 70 |
| 0333AbuCarabTamimi.Mihan | 70,365 | 234 |
| 0333AbuCarabTamimi.TabaqatCulama | 28,320 | 94 |
| 0334IbnHaikHamdani.Iklil | 27,740 | 92 |
| 0334IbnHaikHamdani.SifaJaziraCarab | 70,929 | 236 |
| 0334IbnSacidQushayri.TarikhRaqqa | 17,955 | 59 |
| 0335Suli.AdabKuttab | 40,702 | 135 |
| 0335Suli.AkhbarAbiTamam | 21,133 | 70 |
| 0335Suli.AkhbarRadi | 165,915 | 553 |
| 0335Suli.AshcarAwladKhulafa | 44,151 | 147 |
| 0335Suli.JuzMinAhadith | 1,892 | 6 |
| 0337IbnIshaqZajjaji.Akhbar | 40,895 | 136 |
| 0337QudamaIbnJacfar.Kharaj | 106,955 | 356 |
| 0337QudamaIbnJacfar.NaqdShicr | 22,928 | 76 |
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
| 0355MuhammadKindi.WulatMisr | 50,996 | 169 |
| 0360AbuBakrAjurri.AkhbarAbiHafs | 6,629 | 22 |
| 0360Khawlani.TarikhDaraya | 13,813 | 46 |
| 0360Tabarani.Awail | 5,704 | 19 |
| 0360Tabarani.MucjamAwsat | 728,810 | 2,429 |
| 0360Tabarani.MucjamKabir | 1,590,311 | 5,301 |
| 0365IbnCadiJurjani.AsamiManRawaCanhum | 7,679 | 25 |
| 0365IbnCadiJurjani.KamilFiDucafa | 962,139 | 3,207 |
| 0365IbnFaqihHamadhani.Buldan | 147,627 | 492 |
| 0367IbnHawqal.SuraArd | 123,793 | 412 |
| 0368AbuGhalibZurari.Risala | 22,769 | 75 |
| 0368Sirafi.AkhbarNahwiyyin | 10,206 | 34 |
| 0369AbuShaykhIsbahani.TabaqatMuhaddithin | 132,061 | 440 |
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
| 0381AbuQasimJawhari.MusnadMuwatta | 74,413 | 248 |
| 0382IbnCabdAllahCaskari.AkhbarMusahhifin | 3,184 | 10 |
| 0384IbnCimranMarzubani.MucjamShucara | 86,047 | 286 |
| 0385Daruqutni.DhikrAsmaTabicin | 19,767 | 65 |
| 0385Daruqutni.Ducafa | 9,054 | 30 |
| 0385Daruqutni.MutalifWaMukhtalif | 207,158 | 690 |
| 0385Daruqutni.SualatBarqani | 18,719 | 62 |
| 0385Daruqutni.SualatNaysaburi | 8,317 | 27 |
| 0385IbnNadim.Fihrist | 141,796 | 472 |
| 0385IbnShahin.DhikrManIkhtalafaCulama | 11,073 | 36 |
| 0385IbnShahin.TarikhAsmaDucafa | 21,637 | 72 |
| 0385IbnShahin.TarikhAsmaThiqat | 31,929 | 106 |
| 0386AbuTalibMakki.QutQulub | 385,567 | 1,285 |
| 0387IbnSamcunBaghdadi.Amali | 434,581 | 1,448 |
| 0387KatibKhwarizmi.MafatihCulum | 30,055 | 100 |
| 0388Shabushti.Diyarat | 38,993 | 129 |
| 0390Muqaddasi.AhsanTaqasim | 98,198 | 327 |
| 0395AbuHilalCaskari.Talkhis | 57,835 | 192 |
| 0395IbnMandahMuhammad.Asami | 4,056 | 13 |
| 0395IbnMandahMuhammad.FathBab | 124,908 | 416 |
| 0395IbnMandahMuhammad.MacrifaSahaba | 90,565 | 301 |
| 0398AbuNasrKalabadhi.HidayaWaIrshad | 90,817 | 302 |
| 0400IbnCamashliqJacfari.JuzIbnCamashliq | 2,684 | 8 |
| 0400IbnTahirMaqdisi.BadWaTarikh | 197,348 | 657 |
| 0400IshaqMunajjim.AkamMarjan | 10,606 | 35 |
| 0402MuhammadSaydawi.MucjamShuyukh | 26,156 | 87 |
| 0403IbnFaradi.TarikhCulamaAndalus | 118,911 | 396 |
| 0405AbuFadlHarawi.MucjamFiMushtabah | 10,379 | 34 |
| 0405HakimNaysaburi.MacrifatCulumHadith | 73,931 | 246 |
| 0405HakimNaysaburi.Mustadrak | 886,412 | 2,954 |
| 0405HakimNaysaburi.TalkhisTarikhNaysabur | 32,674 | 108 |
| 0405HakimNaysaburi.TasmiyaManAkhrajahum | 15,868 | 52 |
| 0409CabdGhaniAzdi.KitabMutawarin | 6,452 | 21 |
| 0410IbnMardawayh.ThalathaMajalis | 4,414 | 14 |
| 0412Sulami.TabaqatSufiya | 68,774 | 229 |
| 0413ShaykhMufid.AhkamNisa | 10,517 | 35 |
| 0413ShaykhMufid.Amali | 109,089 | 363 |
| 0413ShaykhMufid.Irshad | 172,972 | 576 |
| 0413ShaykhMufid.MasarShica | 11,320 | 37 |
| 0413ShaykhMufid.Muqnica | 195,606 | 652 |
| 0414AbuHayyanTawhidi.AkhlaqWazirayn | 59,746 | 199 |
| 0414AbuHayyanTawhidi.Basair | 307,963 | 1,026 |
| 0414AbuHayyanTawhidi.Imtac | 124,775 | 415 |
| 0414AbuHayyanTawhidi.Muqabasat | 59,313 | 197 |
| 0414AbuHayyanTawhidi.Sadaqa | 46,821 | 156 |
| 0418WazirMaghribi.AdabKhawas | 22,658 | 75 |
| 0418WazirMaghribi.Inas | 22,614 | 75 |
| 0421IbnMuhammadMarzuqi.AzminaWaAmkina | 165,458 | 551 |
| 0421Miskawayh.Tajarib | 679,938 | 2,266 |
| 0427HamzaJurjani.TarikhJurjan | 114,881 | 382 |
| 0428IbnManjuwayhIsbahani.RijalSahihMuslim | 124,175 | 413 |
| 0429AbuMansurThacalibi.AhsanMaSamictu | 15,268 | 50 |
| 0429AbuMansurThacalibi.Diwan | 4,829 | 16 |
| 0429AbuMansurThacalibi.DurarHikm | 6,924 | 23 |
| 0429AbuMansurThacalibi.FiqhLugha | 56,313 | 187 |
| 0429AbuMansurThacalibi.IcjazWaIjaz | 26,325 | 87 |
| 0429AbuMansurThacalibi.KhassKhass | 37,474 | 124 |
| 0429AbuMansurThacalibi.LataifWaZaraif | 43,612 | 145 |
| 0429AbuMansurThacalibi.LubabAdab | 31,233 | 104 |
| 0429AbuMansurThacalibi.Lutf | 11,868 | 39 |
| 0429AbuMansurThacalibi.ManGhabaCanhuMutrib | 11,987 | 39 |
| 0429AbuMansurThacalibi.Muntahal | 39,453 | 131 |
| 0429AbuMansurThacalibi.MutanabbiWaMaLahu | 19,725 | 65 |
| 0429AbuMansurThacalibi.Rasail | 45,809 | 152 |
| 0429AbuMansurThacalibi.Shakwa | 21,139 | 70 |
| 0429AbuMansurThacalibi.SihrBalagha | 42,361 | 141 |
| 0429AbuMansurThacalibi.TahsinQabih | 9,612 | 32 |
| 0429AbuMansurThacalibi.Tamthil | 49,580 | 165 |
| 0429AbuMansurThacalibi.ThimarQulub | 119,721 | 399 |
| 0429AbuMansurThacalibi.YatimaDahr | 362,496 | 1,208 |
| 0430AbuNucaymIsbahani.DhikrManIsmuhuShucba | 3,082 | 10 |
| 0430AbuNucaymIsbahani.Ducafa | 14,296 | 47 |
| 0430AbuNucaymIsbahani.HilyaAwliya | 1,227,955 | 4,093 |
| 0430AbuNucaymIsbahani.MacrifaSahaba | 785,050 | 2,616 |
| 0430AbuNucaymIsbahani.MajlisMinAmali | 1,871 | 6 |
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
| 0458Bayhaqi.AsmaWaSifat | 157,931 | 526 |
| 0458Bayhaqi.DalailNubuwwa | 602,949 | 2,009 |
| 0458Bayhaqi.Ictiqad | 62,880 | 209 |
| 0460ShaykhTusi.IkhtiyarMacrifaRijal | 227,637 | 758 |
| 0460ShaykhTusi.Rijal | 88,503 | 295 |
| 0461IbnHusaynSughdi.NutafFifatawa | 131,713 | 439 |
| 0463IbnCabdBarr.AdabMujalasa | 5,634 | 18 |
| 0463IbnCabdBarr.BahjatMajalis | 137,584 | 458 |
| 0463IbnCabdBarr.Durar | 76,336 | 254 |
| 0463IbnCabdBarr.InbahCalaQabail | 18,464 | 61 |
| 0463IbnCabdBarr.Insaf | 10,560 | 35 |
| 0463IbnCabdBarr.IntiqaFiFadail | 36,504 | 121 |
| 0463IbnCabdBarr.IsticabFiMacrifaAshab | 413,421 | 1,378 |
| 0463IbnCabdBarr.IstidhkarJamic | 1,147,942 | 3,826 |
| 0463IbnCabdBarr.JamicBayan | 141,492 | 471 |
| 0463IbnCabdBarr.KafiFiFiqh | 199,095 | 663 |
| 0463IbnCabdBarr.TamhidMuwatta | 1,461,702 | 4,872 |
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
| 0499IbnHusaynJurjani.TartibAmali | 313,911 | 1,046 |
| 0505Ghazali.AsnafMaghrurin | 6,558 | 21 |
| 0505Ghazali.BidayatHidaya | 14,542 | 48 |
| 0505Ghazali.Fadaih | 47,692 | 158 |
| 0505Ghazali.IhyaCulumDin | 996,434 | 3,321 |
| 0505Ghazali.Iqtisad | 43,770 | 145 |
| 0505Ghazali.JawahirQuran | 33,456 | 111 |
| 0505Ghazali.KimiyaSacada | 3,404 | 11 |
| 0505Ghazali.MacarijQuds | 39,642 | 132 |
| 0505Ghazali.MahkNazar | 26,750 | 89 |
| 0505Ghazali.Mankhul | 54,192 | 180 |
| 0505Ghazali.MaqsadAsna | 34,718 | 115 |
| 0505Ghazali.MicyarCilm | 49,099 | 163 |
| 0505Ghazali.MishkatAnwar | 18,447 | 61 |
| 0505Ghazali.MizanCamal | 33,154 | 110 |
| 0505Ghazali.Munqidh | 11,334 | 37 |
| 0505Ghazali.Mustasfa | 183,605 | 612 |
| 0505Ghazali.QawaidCaqaid | 19,315 | 64 |
| 0505Ghazali.SirrCalamin | 23,943 | 79 |
| 0505Ghazali.Tahafut | 49,401 | 164 |
| 0505Ghazali.TibrMasbuk | 31,540 | 105 |
| 0505Ghazali.Wasit | 404,624 | 1,348 |
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
| 0538IbnCumarZamakhshari.FaiqFiGharib | 298,042 | 993 |
| 0538MahmudZamakhshari.JibalWaAmkina | 15,676 | 52 |
| 0540AbuMansurJawaliqi.SharhAdabKatib | 83,991 | 279 |
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
| 0571IbnCasakir.ArbacunaBuldaniyya | 19,310 | 64 |
| 0571IbnCasakir.ArbacunaFiHathth | 6,196 | 20 |
| 0571IbnCasakir.KashfMughatta | 4,241 | 14 |
| 0571IbnCasakir.MadhTawaduc | 4,490 | 14 |
| 0571IbnCasakir.MucjamShuyukh | 195,776 | 652 |
| 0571IbnCasakir.TabyinImtinan | 2,994 | 9 |
| 0571IbnCasakir.TabyinKadhb | 90,478 | 301 |
| 0571IbnCasakir.TacziyatMuslim | 10,396 | 34 |
| 0571IbnCasakir.TarikhDimashq | 10,412,929 | 34,709 |
| 0571IbnCasakir.TarjamatHasan | 103,718 | 345 |
| 0571IbnCasakir.TarjamatHusayn | 111,626 | 372 |
| 0571IbnCasakir.Tawba | 1,946 | 6 |
| 0573NashwanHimyari.KhulasaSiyar | 35,216 | 117 |
| 0575IbnBabawayh.Fihrist | 96,438 | 321 |
| 0575IbnKhayrIshbili.Fahrasa | 117,769 | 392 |
| 0576IbnMuhammadSilafi.Mashyakha | 22,872 | 76 |
| 0576IbnMuhammadSilafi.MashyakhaBaghdadiyya | 135,363 | 451 |
| 0576IbnMuhammadSilafi.MucjamSafar | 97,869 | 326 |
| 0576IbnMuhammadSilafi.Wajiz | 10,969 | 36 |
| 0577IbnAnbari.NuzhaAlibba | 43,683 | 145 |
| 0578IbnBashkuwal.GhawamidAsma | 110,027 | 366 |
| 0578IbnBashkuwal.MaRuwiyaFiHawd | 5,490 | 18 |
| 0578IbnBashkuwal.Sila | 139,365 | 464 |
| 0580IbnCimrani.InbaFiTarikhKhulafa | 92,814 | 309 |
| 0581IbnCumarIsbahani.DhikrIbnAbiDunya | 2,998 | 9 |
| 0581IbnCumarIsbahani.DhikrIbnMandah | 7,923 | 26 |
| 0581IbnCumarIsbahani.KalamCalaHadithIstilqa | 392 | 1 |
| 0581IbnCumarIsbahani.KhasaisMusnadAhmad | 2,908 | 9 |
| 0581IbnCumarIsbahani.Lataif | 123,597 | 411 |
| 0581IbnCumarIsbahani.MuntahaRaghabat | 14,322 | 47 |
| 0581IbnCumarIsbahani.NuzhatHuffaz | 6,829 | 22 |
| 0581IbnCumarIsbahani.TiwalatAkhbar | 2,004 | 6 |
| 0584IbnMunqidhShayzari.Ictibar | 42,824 | 142 |
| 0584IbnMusaHazimi.Amakin | 64,697 | 215 |
| 0584IbnMusaHazimi.CujalaMubtadi | 23,180 | 77 |
| 0597CimadDinKatib.BarqShami | 84,900 | 283 |
| 0597CimadDinKatib.KharidaQasr | 385,025 | 1,283 |
| 0597IbnJawzi.Adhkiya | 65,051 | 216 |
| 0597IbnJawzi.AkhbarNisa | 42,278 | 140 |
| 0597IbnJawzi.BahrDumuc | 31,132 | 103 |
| 0597IbnJawzi.BirrWaSila | 42,768 | 142 |
| 0597IbnJawzi.BirrWalidayn | 7,265 | 24 |
| 0597IbnJawzi.BustanWacizin | 85,753 | 285 |
| 0597IbnJawzi.CilalMutanahiyya | 181,277 | 604 |
| 0597IbnJawzi.DafcShubahTashbih | 66,255 | 220 |
| 0597IbnJawzi.DhammHawa | 144,805 | 482 |
| 0597IbnJawzi.DucafaWaMatrukin | 100,991 | 336 |
| 0597IbnJawzi.FadailQuds | 8,290 | 27 |
| 0597IbnJawzi.FununAfnan | 25,581 | 85 |
| 0597IbnJawzi.GharibHadith | 126,650 | 422 |
| 0597IbnJawzi.HamqaWaMughallifin | 36,714 | 122 |
| 0597IbnJawzi.Hathth | 8,462 | 28 |
| 0597IbnJawzi.HifzCumr | 5,669 | 18 |
| 0597IbnJawzi.IclamMacalim | 25,913 | 86 |
| 0597IbnJawzi.IkhbarAhlRusukh | 2,241 | 7 |
| 0597IbnJawzi.KashfMushkil | 336,225 | 1,120 |
| 0597IbnJawzi.Laali | 7,874 | 26 |
| 0597IbnJawzi.Lataif | 17,506 | 58 |
| 0597IbnJawzi.Manthur | 6,211 | 20 |
| 0597IbnJawzi.Mashyakha | 17,396 | 57 |
| 0597IbnJawzi.Mawducat | 259,908 | 866 |
| 0597IbnJawzi.Mudhish | 100,987 | 336 |
| 0597IbnJawzi.Muntazam | 1,529,894 | 5,099 |
| 0597IbnJawzi.Muqliq | 10,803 | 36 |
| 0597IbnJawzi.MusaffaBiAkuff | 6,019 | 20 |
| 0597IbnJawzi.Musalsalat | 13,511 | 45 |
| 0597IbnJawzi.MuthirGharam | 81,078 | 270 |
| 0597IbnJawzi.NawasikhQuran | 69,080 | 230 |
| 0597IbnJawzi.NuzhatAcyun | 63,056 | 210 |
| 0597IbnJawzi.QussasWaMudhakkirin | 26,592 | 88 |
| 0597IbnJawzi.SaydKhatir | 122,967 | 409 |
| 0597IbnJawzi.SifaSafwa | 330,284 | 1,100 |
| 0597IbnJawzi.Tabsira | 186,643 | 622 |
| 0597IbnJawzi.TaczimFutya | 5,050 | 16 |
| 0597IbnJawzi.TadhkiraFiWacz | 34,984 | 116 |
| 0597IbnJawzi.TadhkiratArib | 60,775 | 202 |
| 0597IbnJawzi.TahqiqFiAhadithKhilaf | 213,087 | 710 |
| 0597IbnJawzi.TalbisIblis | 130,487 | 434 |
| 0597IbnJawzi.TalqihFuhum | 160,269 | 534 |
| 0597IbnJawzi.TanbihNaim | 2,463 | 8 |
| 0597IbnJawzi.TanwirGhabash | 31,590 | 105 |
| 0597IbnJawzi.TarikhBaytMuqaddas | 6,394 | 21 |
| 0597IbnJawzi.ThibatCindaMamat | 21,524 | 71 |
| 0597IbnJawzi.Yaquta | 9,747 | 32 |
| 0597IbnJawzi.ZadMasir | 795,393 | 2,651 |
| 0597IbnJawzi.ZirafWaMutamajinin | 18,698 | 62 |
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
| 0635AbuMunajjaIbnLatti.Mashyakha | 16,784 | 55 |
| 0637IbnAthirDiyaDin.MathalSair | 183,732 | 612 |
| 0637IbnMustafwi.TarikhIrbil | 385,144 | 1,283 |
| 0639AbuBakrMalaqi.MatlacAnwar | 65,139 | 217 |
| 0640AbuHafsDunaysiri.TarikhDunaysir | 22,117 | 73 |
| 0641Sarifini.Muntakhab | 96,486 | 321 |
| 0642IbnNajjar.DhaylTarikhBaghdad | 326,501 | 1,088 |
| 0643DiyaDinMuqaddasi.FadailBaytMaqdis | 11,474 | 38 |
| 0643DiyaDinMuqaddasi.JuzAwham | 2,001 | 6 |
| 0643IbnSalahShahrazuri.Fatawa | 164,681 | 548 |
| 0643IbnSalahShahrazuri.TabaqatFuqaha | 63,126 | 210 |
| 0645TilimsaniBurri.Jawhara | 194,697 | 648 |
| 0646IbnQifti.IkhbarCulama | 96,909 | 323 |
| 0646IbnQifti.InbahRuwat | 295,800 | 986 |
| 0646IbnQifti.Muhammadun | 57,364 | 191 |
| 0647CabdWahidMarrakushi.Mucjib | 70,871 | 236 |
| 0650IbnNazifHamawi.TarikhMansuri | 27,313 | 91 |
| 0654SibtIbnJawzi.ItharInsaf | 50,626 | 168 |
| 0656IbnAbiHadid.FalakDair | 82,158 | 273 |
| 0656IbnAbiHadid.RawdaMukhtara | 19,714 | 65 |
| 0656IbnAbiHadid.SharhNahjBalagha | 1,452,591 | 4,841 |
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
| 0676Nawawi.AdabFatwa | 8,353 | 27 |
| 0676Nawawi.Adhkar | 155,669 | 518 |
| 0676Nawawi.ArbacunaNawawiyya | 3,714 | 12 |
| 0676Nawawi.BustanCarifin | 17,605 | 58 |
| 0676Nawawi.DaqaiqMinhaj | 6,752 | 22 |
| 0676Nawawi.IctiqadSalafFiHuruf | 12,517 | 41 |
| 0676Nawawi.IdahFiManasikHajj | 48,035 | 160 |
| 0676Nawawi.IjazFiSharhSunanAbiDawud | 29,935 | 99 |
| 0676Nawawi.KhulasatAhkam | 114,612 | 382 |
| 0676Nawawi.Majmuc | 2,819,113 | 9,397 |
| 0676Nawawi.MasailManthura | 30,618 | 102 |
| 0676Nawawi.MinhajTalibin | 77,131 | 257 |
| 0676Nawawi.RawdatTalibin | 1,105,776 | 3,685 |
| 0676Nawawi.RiyadSalihin | 136,428 | 454 |
| 0676Nawawi.SharhArbacinaNawawi | 120,803 | 402 |
| 0676Nawawi.SharhMuslim | 758,673 | 2,528 |
| 0676Nawawi.TahdhibAsma | 352,183 | 1,173 |
| 0676Nawawi.TahrirAlfaz | 41,558 | 138 |
| 0676Nawawi.Taqrib | 17,766 | 59 |
| 0676Nawawi.Tibyan | 24,167 | 80 |
| 0676Nawawi.UsulWaDawabit | 1,716 | 5 |
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
| 0693IbnAbiFathIrbili.KashfGhumma | 309,157 | 1,030 |
| 0694MuhibbDinTabari.Dhakhair | 81,328 | 271 |
| 0694MuhibbDinTabari.RiyadNadira | 205,681 | 685 |
| 0695IbnCidhariMarrakushi.BayanMaghrib | 153,641 | 512 |
| 0696CumarSunami.NisabIhtisab | 46,622 | 155 |
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
| 0728IbnTaymiyya.FatawaHamawiyya | 24,002 | 80 |
| 0728IbnTaymiyya.FatawaKubra | 910,627 | 3,035 |
| 0728IbnTaymiyya.MajmucFatawa | 3,016,187 | 10,053 |
| 0728IbnTaymiyya.MustadrakCalaMajmucFatawa | 249,305 | 831 |
| 0728IbnTaymiyya.RasHusayn | 10,286 | 34 |
| 0728IbnTaymiyya.RasailWaFatawa | 1,258,070 | 4,193 |
| 0730MuhammadTujibi.Barnamaj | 71,375 | 237 |
| 0732AbuFida.MukhtasarFiAkhbar | 316,828 | 1,056 |
| 0732AbuFida.Yawaqit | 21,381 | 71 |
| 0732IbnYacqubJanadi.SulukFiTabaqat | 272,623 | 908 |
| 0733IbnJamaca.Mashyakha | 75,126 | 250 |
| 0733Nuwayri.NihayaArab | 2,455,687 | 8,185 |
| 0734IbnQaddahHarawi.MulhaqFatawa | 1,839 | 6 |
| 0739SafiDinHanbali.Marasid | 220,179 | 733 |
| 0740IbnDawudHilli.Rijal | 68,088 | 226 |
| 0741KhatibTabrizi.Ikmal | 90,307 | 301 |
| 0742Mizzi.TahdhibKamal | 2,701,747 | 9,005 |
| 0747MuhyiDinYunini.Mashyakha | 8,748 | 29 |
| 0748Dhahabi.AhadithMukhtaraMinMawducat | 6,040 | 20 |
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
| 0748Dhahabi.TalkhisMawducatIbnJawzi | 50,388 | 167 |
| 0748Dhahabi.TarikhIslam | 3,437,381 | 11,457 |
| 0748IbnDimyati.Mustafad | 50,153 | 167 |
| 0749IbnWardi.KharidaCajaib | 75,947 | 253 |
| 0749IbnWardi.Tarikh | 252,903 | 843 |
| 0749ShihabDinCumari.MasalikAbsar | 1,182,722 | 3,942 |
| 0749Wadiashi.Barnamaj | 44,950 | 149 |
| 0750AbuHafsQazwini.Mashyakha | 68,872 | 229 |
| 0751IbQayyimJawziyya.AclamMuwaqqicin | 450,649 | 1,502 |
| 0751IbQayyimJawziyya.AhkamAhlDhimma | 172,395 | 574 |
| 0751IbQayyimJawziyya.AmthalFiQuran | 16,339 | 54 |
| 0751IbQayyimJawziyya.BadaicFawaid | 284,235 | 947 |
| 0751IbQayyimJawziyya.CuddatSabirin | 78,339 | 261 |
| 0751IbQayyimJawziyya.DaWaDawa | 87,602 | 292 |
| 0751IbQayyimJawziyya.FaidaJalila | 4,424 | 14 |
| 0751IbQayyimJawziyya.Fawaid | 56,135 | 187 |
| 0751IbQayyimJawziyya.Furusiyya | 58,088 | 193 |
| 0751IbQayyimJawziyya.HadiArwah | 110,951 | 369 |
| 0751IbQayyimJawziyya.HidayatHayara | 73,901 | 246 |
| 0751IbQayyimJawziyya.IghathatLahfan | 193,281 | 644 |
| 0751IbQayyimJawziyya.IjtimacJuyush | 57,215 | 190 |
| 0751IbQayyimJawziyya.JalaAfham | 75,694 | 252 |
| 0751IbQayyimJawziyya.JawabFiSiyaghHamd | 4,621 | 15 |
| 0751IbQayyimJawziyya.MadarijSalikin | 378,062 | 1,260 |
| 0751IbQayyimJawziyya.ManarMunif | 15,443 | 51 |
| 0751IbQayyimJawziyya.MatnQasidaNuniyya | 57,221 | 190 |
| 0751IbQayyimJawziyya.MiftahDarSacada | 240,583 | 801 |
| 0751IbQayyimJawziyya.MukhtasarSawaciqMursala | 192,397 | 641 |
| 0751IbQayyimJawziyya.RawdatMuhibbin | 94,055 | 313 |
| 0751IbQayyimJawziyya.RisalaIlaAhadIkhwan | 4,567 | 15 |
| 0751IbQayyimJawziyya.RisalaTabukiyya | 11,072 | 36 |
| 0751IbQayyimJawziyya.RuhFiKalam | 94,694 | 315 |
| 0751IbQayyimJawziyya.Salat | 45,614 | 152 |
| 0751IbQayyimJawziyya.SawaciqMursala | 193,235 | 644 |
| 0751IbQayyimJawziyya.ShifaCalil | 165,000 | 550 |
| 0751IbQayyimJawziyya.SifatMunafiqin | 3,344 | 11 |
| 0751IbQayyimJawziyya.TafsirQuran | 145,349 | 484 |
| 0751IbQayyimJawziyya.TariqHijratayn | 142,292 | 474 |
| 0751IbQayyimJawziyya.TibbNabawi | 91,222 | 304 |
| 0751IbQayyimJawziyya.TibyanFiAqsamQuran | 79,486 | 264 |
| 0751IbQayyimJawziyya.TuhfatMawdud | 51,068 | 170 |
| 0751IbQayyimJawziyya.TuruqHukmiyya | 84,928 | 283 |
| 0751IbQayyimJawziyya.WabilSayyib | 44,173 | 147 |
| 0751IbQayyimJawziyya.ZadMacad | 566,492 | 1,888 |
| 0751IbnQayyimJawziya.AsmaMuallafatIbnTaymiya | 3,722 | 12 |
| 0751IbnQayyimJawziyya.IghathaLahfan | 8,563 | 28 |
| 0756TaqiDinSubki.Fatawa | 418,947 | 1,396 |
| 0756TaqiDinSubki.Ibhaj | 284,031 | 946 |
| 0756TaqiDinSubki.IbrazHikam | 12,771 | 42 |
| 0761IbnKaykaldi.JamicTahsil | 76,460 | 254 |
| 0761IbnKaykaldi.Mukhtalitin | 3,340 | 11 |
| 0761IbnKaykaldiDimashqi.ItharatFawaid | 104,474 | 348 |
| 0762MughaltayIbnQalij.IkmalTahdhib | 861,631 | 2,872 |
| 0764IbnShakirKutubi.FawatWafayat | 288,315 | 961 |
| 0764Safadi.AcyanCasr | 604,057 | 2,013 |
| 0764Safadi.NaktHimyan | 74,306 | 247 |
| 0764Safadi.WafiBiWafayat | 1,978,264 | 6,594 |
| 0765AbuMahasinHusayni.DhaylTadhkira | 15,407 | 51 |
| 0765AbuMahasinHusayni.IkmalLiRijal | 54,306 | 181 |
| 0767Balawi.TajMafriq | 73,852 | 246 |
| 0768Yafici.MiratJanan | 424,088 | 1,413 |
| 0771Subki.MucjamShuyukh | 117,371 | 391 |
| 0771Subki.TabaqatShaficiyaKubra | 676,807 | 2,256 |
| 0774IbnKathir.AdabDukhulHammam | 9,495 | 31 |
| 0774IbnKathir.Bidaya | 2,329,940 | 7,766 |
| 0774IbnKathir.FadailQuran | 36,176 | 120 |
| 0774IbnKathir.FusulMinSira | 39,673 | 132 |
| 0774IbnKathir.IkhtisarCulumHadith | 22,788 | 75 |
| 0774IbnKathir.JamicMasanid | 1,078,748 | 3,595 |
| 0774IbnKathir.MusnadCumarIbnKhattab | 112,095 | 373 |
| 0774IbnKathir.NihayatFiFitan | 162,376 | 541 |
| 0774IbnKathir.QisasAnbiya | 183,993 | 613 |
| 0774IbnKathir.SharhIkhtisarCulumHadith | 143,546 | 478 |
| 0774IbnKathir.TabaqatShaficiyyin | 180,884 | 602 |
| 0774IbnKathir.TafsirQuran | 1,696,932 | 5,656 |
| 0774IbnKathir.Takmil | 255,916 | 853 |
| 0774IbnKathir.TalkhisKitabIstighatha | 85,496 | 284 |
| 0774IbnKathir.TuhfatTalib | 49,042 | 163 |
| 0774IbnRaficSallami.MashyakhaBayani | 6,654 | 22 |
| 0774IbnRaficSallami.Wafayat | 61,135 | 203 |
| 0775IbnAbiWafa.JawahirMudiya | 230,720 | 769 |
| 0776LisanDinIbnKhatib.Ihata | 462,435 | 1,541 |
| 0776LisanDinIbnKhatib.KatibaKamina | 54,854 | 182 |
| 0776LisanDinIbnKhatib.KhatraTayf | 3,992 | 13 |
| 0776LisanDinIbnKhatib.MicyarIkhtiyar | 22,471 | 74 |
| 0776LisanDinIbnKhatib.NafadaJirab | 52,268 | 174 |
| 0777BadrDinBacli.MukhtasarFatawaMisriyya | 149,612 | 498 |
| 0779IbnBattuta.Rihla | 267,265 | 890 |
| 0782IbnSallar.TabaqatQurra | 51,171 | 170 |
| 0789IbnMuhammadKhuzaci.TakhrijDalalat | 185,440 | 618 |
| 0793AbuHasanMalaqi.TarikhQudat | 62,043 | 206 |
| 0795IbnRajabHanbali.DhaylTabaqatHanabila | 213,679 | 712 |
| 0799IbnFarhun.DibajMudhahhab | 114,355 | 381 |
| 0802IbnMusaAbnasi.ShadhaFayyah | 148,038 | 493 |
| 0804IbnMulaqqin.BadrMunir | 973,506 | 3,245 |
| 0804IbnMulaqqin.TabaqatAwliya | 54,595 | 181 |
| 0804IbnMulaqqin.TuhfaMuhtaj | 95,932 | 319 |
| 0806IbnHusaynCiraqi.Alfiyya | 11,757 | 39 |
| 0806IbnHusaynCiraqi.AlfiyyatSira | 15,885 | 52 |
| 0806IbnHusaynCiraqi.ArbacunaCushariyya | 15,498 | 51 |
| 0806IbnHusaynCiraqi.DhaylMizan | 49,484 | 164 |
| 0806IbnHusaynCiraqi.MustakhrajCalaMustadrak | 12,105 | 40 |
| 0806IbnHusaynCiraqi.SharhAlfiyya | 376,778 | 1,255 |
| 0806IbnHusaynCiraqi.Taqyid | 79,924 | 266 |
| 0806IbnHusaynCiraqi.TarhTarthib | 712,047 | 2,373 |
| 0807IbnAhmarKhazraji.NafhaNisriniyya | 7,528 | 25 |
| 0807NurDinHaythami.GhayatMaqsad | 334,690 | 1,115 |
| 0807NurDinHaythami.KashfAstar | 284,395 | 947 |
| 0807NurDinHaythami.MaqsadAli | 142,449 | 474 |
| 0807NurDinHaythami.MawaridZaman | 238,357 | 794 |
| 0807NurDinHaythami.MucjamZawaid | 1,222,016 | 4,073 |
| 0808IbnKhaldun.Rihla | 55,833 | 186 |
| 0808IbnKhaldun.Tarikh | 1,596,529 | 5,321 |
| 0808MuhammadDamiri.HayatHayawanKubra | 441,392 | 1,471 |
| 0809IbnQunfudh.Wafayat | 9,725 | 32 |
| 0812CaliKhazraji.CuqudLuluiyya | 167,694 | 558 |
| 0815IbnCabdAllahGhazuli.MatalicBudur | 175,305 | 584 |
| 0816AbuBakrMaraghi.Mashyakha | 64,167 | 213 |
| 0817Firuzabadi.QamusMuhit | 581,791 | 1,939 |
| 0817Firuzabadi.TanwirMiqbas | 314,570 | 1,048 |
| 0817IbnYacqubFiruzabadi.BulghaFiTarajim | 38,540 | 128 |
| 0821Qalqashandi.Maathir | 142,487 | 474 |
| 0821Qalqashandi.NihayaArab | 97,039 | 323 |
| 0821Qalqashandi.QalaidJuman | 30,592 | 101 |
| 0821Qalqashandi.SubhAcsha | 1,616,289 | 5,387 |
| 0825IbnQasimSabti.IkhtisarAkhbar | 5,839 | 19 |
| 0826IbnCiraqi.Mudallisin | 3,392 | 11 |
| 0826IbnCiraqi.TuhfaTahsil | 62,996 | 209 |
| 0832AbuTayyibFasi.DhaylTaqyid | 177,958 | 593 |
| 0832AbuTayyibFasi.ShifaGharam | 305,946 | 1,019 |
| 0833IbnJazari.Cawali | 15,458 | 51 |
| 0833IbnJazari.DurraMudiyya | 3,546 | 11 |
| 0833IbnJazari.GhayaNihaya | 338,862 | 1,129 |
| 0833IbnJazari.ManaqibAsadGhalib | 50,044 | 166 |
| 0833IbnJazari.ManzumaJazariyya | 1,270 | 4 |
| 0833IbnJazari.MatnTayyibaNashr | 12,067 | 40 |
| 0833IbnJazari.MunjidMuqriyyin | 20,355 | 67 |
| 0833IbnJazari.Nashr | 274,215 | 914 |
| 0833IbnJazari.SharhTayyibaNashr | 98,149 | 327 |
| 0833IbnJazari.TahbirTaysir | 47,020 | 156 |
| 0833IbnJazari.TamhidFiCulumTajwid | 22,299 | 74 |
| 0833IbnJazari.ZahrFaih | 23,508 | 78 |
| 0842IbnNasirDinDimashqi.RaddWafir | 26,176 | 87 |
| 0842IbnNasirDinDimashqi.TawdihMushtabih | 550,678 | 1,835 |
| 0845Maqrizi.Bayan | 31,900 | 106 |
| 0845Maqrizi.ImtacAsmac | 1,802,668 | 6,008 |
| 0845Maqrizi.IqazHunafa | 185,230 | 617 |
| 0845Maqrizi.Mawaciz | 683,850 | 2,279 |
| 0845Maqrizi.MukhtasarKamil | 142,932 | 476 |
| 0845Maqrizi.Suluk | 826,074 | 2,753 |
| 0848IbnSarrajAndalusi.Fatawa | 21,504 | 71 |
| 0851IbnQadiShuhba.TabaqatShaficiya | 119,436 | 398 |
| 0852IbnHajarCasqalani.DurarKamina | 414,702 | 1,382 |
| 0852IbnHajarCasqalani.FathBari | 3,545,728 | 11,819 |
| 0852IbnHajarCasqalani.InbaGhumr | 410,739 | 1,369 |
| 0852IbnHajarCasqalani.IsabaFiTamyiz | 1,153,468 | 3,844 |
| 0852IbnHajarCasqalani.ItharBiMacrifa | 8,858 | 29 |
| 0852IbnHajarCasqalani.LisanMizan | 1,131,427 | 3,771 |
| 0852IbnHajarCasqalani.MasailAjabaCanha | 4,143 | 13 |
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
| 0855Cayni.SharhSunanAbiDawud | 663,495 | 2,211 |
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
| 0893IbnAbiBakrHadari.BahjatMahafil | 401,485 | 1,338 |
| 0900AbuCabdAllahHimyari.RawdMictar | 362,088 | 1,206 |
| 0902Sakhawi.Buldaniyyat | 37,943 | 126 |
| 0902Sakhawi.DuLamic | 1,335,429 | 4,451 |
| 0902Sakhawi.FathMughith | 294,305 | 981 |
| 0902Sakhawi.ManhalCadhb | 28,425 | 94 |
| 0902Sakhawi.TuhfaLatifa | 394,353 | 1,314 |
| 0904Burayhi.TabaqatSulahaYaman | 74,213 | 247 |
| 0905Basrawi.Tarikh | 39,659 | 132 |
| 0909IbnMibradHanbali.BahrDamm | 55,202 | 184 |
| 0909IbnMibradHanbali.MucjamKutub | 14,490 | 48 |
| 0911Samhudi.KhulasaWafaWafa | 168,018 | 560 |
| 0911Samhudi.WafaWafa | 376,631 | 1,255 |
| 0911Suyuti.Ashbah | 150,770 | 502 |
| 0911Suyuti.AsmaMudallisin | 306,751 | 1,022 |
| 0911Suyuti.AsmaMukhadramin | 3,736 | 12 |
| 0911Suyuti.BastKaff | 1,961 | 6 |
| 0911Suyuti.BughyaWucat | 197,961 | 659 |
| 0911Suyuti.DafcTashnic | 1,129 | 3 |
| 0911Suyuti.DhaylTabaqatHuffaz | 22,369 | 74 |
| 0911Suyuti.DibajCalaMuslim | 209,180 | 697 |
| 0911Suyuti.DurrManthur | 1,732,784 | 5,775 |
| 0911Suyuti.FaddWica | 4,136 | 13 |
| 0911Suyuti.GhurarFiFadailCumar | 2,071 | 6 |
| 0911Suyuti.HawiLiFatawa | 306,937 | 1,023 |
| 0911Suyuti.HusnMuhadara | 218,158 | 727 |
| 0911Suyuti.IscafMubatta | 16,433 | 54 |
| 0911Suyuti.ItmamDiraya | 54,179 | 180 |
| 0911Suyuti.Itqan | 263,388 | 877 |
| 0911Suyuti.KhasaisKubra | 266,949 | 889 |
| 0911Suyuti.LaaliMasnuca | 310,804 | 1,036 |
| 0911Suyuti.LubabNuqul | 63,669 | 212 |
| 0911Suyuti.LubbLubab | 57,394 | 191 |
| 0911Suyuti.LumacFiAsbabHadith | 18,722 | 62 |
| 0911Suyuti.LumcaFiKhasaisJumca | 27,412 | 91 |
| 0911Suyuti.ManahilSafa | 31,678 | 105 |
| 0911Suyuti.MiftahJanna | 14,940 | 49 |
| 0911Suyuti.Muhadarat | 128,274 | 427 |
| 0911Suyuti.MuzhirFiCulumLugha | 194,828 | 649 |
| 0911Suyuti.NawahidAbkar | 289,785 | 965 |
| 0911Suyuti.NazmCiqyan | 31,489 | 104 |
| 0911Suyuti.NuzhatJulasa | 5,898 | 19 |
| 0911Suyuti.QutMughtadhi | 102,034 | 340 |
| 0911Suyuti.RawdAniqFiFadlSiddiq | 1,983 | 6 |
| 0911Suyuti.RihNisrin | 795 | 2 |
| 0911Suyuti.SababWadc | 1,883 | 6 |
| 0911Suyuti.ShamailSharifa | 103,995 | 346 |
| 0911Suyuti.Shamarikh | 3,874 | 12 |
| 0911Suyuti.SharhSudur | 90,965 | 303 |
| 0911Suyuti.SharhSunanIbnMaja | 233,491 | 778 |
| 0911Suyuti.TabaqatHuffaz | 73,614 | 245 |
| 0911Suyuti.TabaqatMufassirin | 11,806 | 39 |
| 0911Suyuti.TadhkiratMutasi | 2,144 | 7 |
| 0911Suyuti.TadribRawi | 166,686 | 555 |
| 0911Suyuti.TafsirJalalayn | 266,662 | 888 |
| 0911Suyuti.TahdhirKhawass | 18,396 | 61 |
| 0911Suyuti.TakrirIstinad | 4,810 | 16 |
| 0911Suyuti.TanwirHawalik | 106,252 | 354 |
| 0911Suyuti.TarikhKhulafa | 133,130 | 443 |
| 0911Suyuti.Tatrif | 8,473 | 28 |
| 0922IbnShaykhTarabulusi.IscafAwqaf | 43,648 | 145 |
| 0923AhmadQastallani.IrshadSari | 3,431,449 | 11,438 |
| 0923IbnCabdAllahKhazraji.KhulasaTahdhib | 328,135 | 1,093 |
| 0926ZakariyaAnsari.HududCaniqa | 2,027 | 6 |
| 0927Culaymi.UnsJalil | 218,375 | 727 |
| 0927Nucaymi.DarisFiMadaris | 224,568 | 748 |
| 0929IbnKayyal.KawakibNayyirat | 23,699 | 78 |
| 0938IbnCaliBalawi.Thabat | 61,539 | 205 |
| 0942IbnYusufShami.SubulHuda | 1,900,839 | 6,336 |
| 0945ShamsDinDawudi.TabaqatMufassirin | 139,971 | 466 |
| 0953IbnTulun.MufakahaKhillan | 127,338 | 424 |
| 0957ShihabDinRamli.FatawaRamli | 238,093 | 793 |
| 0966HusaynDiyarbakri.TarikhKhamis | 552,947 | 1,843 |
| 0968Tashkubruizadah.ShaqaiqNucmaniyya | 145,615 | 485 |
| 0973CabdWahhabShacrani.LawaqihAnwar | 232,710 | 775 |
| 0973IbnHajarHaythami.FatawaHadithiyya | 169,473 | 564 |
| 0973IbnHajarHaythami.FatawaKubra | 831,866 | 2,772 |
| 0978QasimQunawi.AnisFuqaha | 24,912 | 83 |
| 0984BardDinGhazzi.MatalicBadriya | 46,951 | 156 |
| 1004ShamsDinRamli.FatawaRamli | 237,937 | 793 |
| 1010TamimiDari.TabaqatSaniya | 161,681 | 538 |
| 1011SahibMacalim.TahrirTawusi | 157,260 | 524 |
| 1014IbnSultanHarawi.Adilla | 9,893 | 32 |
| 1014IbnSultanHarawi.AhadithQudsiyya | 17,034 | 56 |
| 1014IbnSultanHarawi.AsrarMarfuca | 52,534 | 175 |
| 1014IbnSultanHarawi.FaydMucin | 2,321 | 7 |
| 1014IbnSultanHarawi.JamcWasail | 250,690 | 835 |
| 1014IbnSultanHarawi.MirqatMafatih | 2,481,715 | 8,272 |
| 1014IbnSultanHarawi.RaddCalaQailinBiWahdatWujud | 24,574 | 81 |
| 1014IbnSultanHarawi.ShammCawarid | 19,624 | 65 |
| 1014IbnSultanHarawi.SharhMusnadAbiHanifa | 121,419 | 404 |
| 1014IbnSultanHarawi.SharhShifa | 613,217 | 2,044 |
| 1014IbnSultanHarawi.TasliyyatAcma | 5,757 | 19 |
| 1016MuhibbDinHamawi.HadiAzcan | 17,554 | 58 |
| 1031CabdRaufMunawi.Tawqif | 90,082 | 300 |
| 1037CabdQadirCaydarus.TarikhNurSafir | 113,966 | 379 |
| 1041BurhanDinMaliki.BahjaMahafil | 96,298 | 320 |
| 1041Maqarri.AzharRiyad | 185,770 | 619 |
| 1041Maqarri.NafhTib | 848,136 | 2,827 |
| 1051Cimadi.RawdaRayya | 4,849 | 16 |
| 1057IbnCallan.DalilFalihin | 680,104 | 2,267 |
| 1057IbnCallan.IthafFadil | 10,899 | 36 |
| 1061NajmDinGhazzi.KawakibSaira | 242,384 | 807 |
| 1067HajjiKhalifa.KashfZunun | 580,572 | 1,935 |
| 1069ShihabDinKhafaji.RayhanaAlibba | 57,614 | 192 |
| 1070MuhammadKibrit.RihlaShita | 50,647 | 168 |
| 1078RiyadZadah.AsmaKutub | 33,076 | 110 |
| 1086IbnCajamiMisri.DhaylLubbLubab | 22,972 | 76 |
| 1089IbnCimad.Shadharat | 1,097,722 | 3,659 |
| 1090NizamDinBalkhi.FatawaHindiyya | 1,729,192 | 5,763 |
| 1093CabdQadirBaghdadi.KhizanatAdab | 981,595 | 3,271 |
| 1100IbnMuhammadAdnahwi.TabaqatMufassirin | 40,783 | 135 |
| 1100MuhammadItlidi.IclamNas | 80,344 | 267 |
| 1100MustafaTafrishi.NaqdRijal | 500,280 | 1,667 |
| 1101MuhammadCaliArdabili.JamicRuwat | 614,459 | 2,048 |
| 1107HashimBahrani.GhayatMaram | 854,344 | 2,847 |
| 1111Majlisi.BiharAnwar | 4,430,411 | 14,768 |
| 1111MuhammadAminMuhibbi.KhulasaAthr | 623,533 | 2,078 |
| 1119IbnMacsum.SulafaCasr | 165,783 | 552 |
| 1120CaliKhanMadani.DarajatRafica | 174,564 | 581 |
| 1122MuhammadZarqani.SharhCalaMawahib | 422,551 | 1,408 |
| 1122MuhammadZarqani.SharhCalaMuwatta | 975,818 | 3,252 |
| 1126MuhammadHanbali.Mashyakha | 14,775 | 49 |
| 1127IbnMustafaIstanbuli.RuhBayan | 2,425,227 | 8,084 |
| 1147CabdAllahSancani.TarikhYaman | 69,040 | 230 |
| 1147IbnSharafDinKhalili.FatawaKhalili | 225,290 | 750 |
| 1153IbnKannan.YawmiyyatShamiyya | 79,567 | 265 |
| 1167IbnCabrRahmanGhazzi.DiwanIslam | 55,685 | 185 |
| 1172IbnKhalifaMasakini.Fahrasa | 3,704 | 12 |
| 1174AbuBarakatSuwaydi.NafhaMiskiya | 71,961 | 239 |
| 1175AhmadBudayri.HawadithDimashq | 32,858 | 109 |
| 1175MuhammadKarabisi.IklilManhaj | 203,395 | 677 |
| 1187SulaymanMahasini.HululTacab | 2,064 | 6 |
| 1195CabdRahmanAnsari.Tuhfa | 68,557 | 228 |
| 1204SulaymanJamal.Hashiya | 2,260,269 | 7,534 |
| 1205Zubaydi.TajCarus | 4,503,454 | 15,011 |
| 1206IbnCabdWahhab.Fatawa | 21,127 | 70 |
| 1206Muradi.SilkDurar | 358,759 | 1,195 |
| 1212BahrCulum.FawaidRijaliya | 338,918 | 1,129 |
| 1218SalihFulani.QatfThamar | 16,905 | 56 |
| 1225IbnNasirNajdi.MajmucatRasail | 86,793 | 289 |
| 1225IbnNasirNajdi.RasailWaFatawa | 7,178 | 23 |
| 1232IbnKhatibCumari.RawdaFayha | 63,383 | 211 |
| 1237Jabarti.CajaibAthar | 514,968 | 1,716 |
| 1246IbnHamadBassam.DurarMafakhir | 10,058 | 33 |
| 1250IbnCaliShawkani.BadrTalic | 192,663 | 642 |
| 1250IbnCaliShawkani.FathBariMinFatawa | 787,019 | 2,623 |
| 1252IbnCabidinDimashqi.TanqihFatawa | 394,372 | 1,314 |
| 1258IbnCabdSalamTusuli.AjwibatTusuli | 46,225 | 154 |
| 1269CabdMalikCasimi.SamtNujum | 594,712 | 1,982 |
| 1270ShihabDinAlusi.GharaibIghtirab | 113,165 | 377 |
| 1277MuhammadTantawi.NashaNahw | 52,381 | 174 |
| 1282AbaButayn.RasailWaFatawa | 39,985 | 133 |
| 1285CabdRahmanTamimi.Maqamat | 7,256 | 24 |
| 1285IbnHasanTamimi.RasailWaFatawa | 23,607 | 78 |
| 1286IcjazHusaynKunturi.KashfHajb | 126,032 | 420 |
| 1292IbnIbrahimMaghribi.QurratCaynBiFatawa | 149,088 | 496 |
| 1293CabdLatifAlShaykh.CuyunRasailwaAjwiba | 133,775 | 445 |
| 1299IbnCalishMaliki.FathCali | 372,373 | 1,241 |
| 1307Qannawji.AbjadCulum | 274,005 | 913 |
| 1307Qannawji.BulghaFuUsulLugha | 64,209 | 214 |
| 1307Qannawji.FathBayan | 1,522,217 | 5,074 |
| 1307Qannawji.HittaFiDhikr | 67,880 | 226 |
| 1307Qannawji.HusnUswa | 131,192 | 437 |
| 1307Qannawji.LuqtaCajlan | 59,600 | 198 |
| 1307Qannawji.NashwatSakran | 19,854 | 66 |
| 1307Qannawji.NaylMaram | 104,303 | 347 |
| 1307Qannawji.QatfThamar | 24,292 | 80 |
| 1307Qannawji.RawdaNadiyya | 290,058 | 966 |
| 1307Qannawji.Yaqza | 51,107 | 170 |
| 1310BakriDimyati.HashiyaIcanaTalibin | 989,242 | 3,297 |
| 1313Barujirdi.Taraif | 331,121 | 1,103 |
| 1313VanDyck.IktifaQunuc | 112,098 | 373 |
| 1315AbuMacaliKalbasi.RasailRijaliyya | 613,389 | 2,044 |
| 1315Salawi.IstiqsaLiAhkbar | 464,659 | 1,548 |
| 1318AhmadDimashqi.MucjamAsmaAshya | 29,472 | 98 |
| 1318MuhammadSanusi.Musamarat | 266,110 | 887 |
| 1320NuriTabarsi.KhatimaMustadrak | 731,187 | 2,437 |
| 1320NuriTabarsi.MustadrakWasail | 1,983,623 | 6,612 |
| 1330IbnMusaTabrizi.MiratKutub | 88,818 | 296 |
| 1332ZaynabFawwaz.DurrManthur | 238,367 | 794 |
| 1335CabdRazzaqBaytar.HilyaBashar | 346,616 | 1,155 |
| 1336CabdHamidThani.MudhakkaratiSiyasiya | 21,875 | 72 |
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
| 1353IbnCabdRahimMubarakfuri.TuhfatAhwadhi | 1,368,928 | 4,563 |
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
| 1389MuhammadAlShaykh.FatawaWaRasail | 822,319 | 2,741 |
| 1390MuhsinTabatabai.DalilNasik | 142,329 | 474 |
| 1396KhayrDinZirikli.Aclam | 1,634,967 | 5,449 |
| 1400MuhammadBaqirSadr.FatawaWadiha | 120,795 | 402 |
| 1405CaliShahrudi.Mustadrakat | 1,015,230 | 3,384 |
| 1408CumarKahhala.MucjamMuallifin | 1,145,173 | 3,817 |
| 1408CumarKahhala.MucjamQabail | 467,206 | 1,557 |
| 1409IbnSayyidCajamiMisri.HidayatQari | 158,087 | 526 |
| 1411SayyidMarcashi.SharhIhqaq | 4,126,172 | 13,753 |
| 1413TajDinKhui.MinhajSalihin | 185,758 | 619 |
| 1413TajDinKhui.MucjamRijal | 2,594,210 | 8,647 |
| 1413TajDinKhui.TakmilatMinhajSalihin | 32,881 | 109 |
| 1414MuhammadRidaGulpayagani.HidayatCibad | 213,176 | 710 |
| 1414MuhammadRidaGulpayagani.IrshadSail | 39,093 | 130 |
| 1414MuhammadRidaGulpayagani.MukhtasarAhkam | 34,163 | 113 |
| 1414SalimIbadi.IscafAcyan | 25,921 | 86 |
| 1418MuhammadRuhani.ManasikHajj | 33,338 | 111 |
| 1418MuhammadRuhani.MasailMuntakhaba | 73,342 | 244 |
| 1418MuhammadRuhani.MinhajSalihin | 155,324 | 517 |
| 1418SalihAhmadArkani.TihfaMajalis | 14,467 | 48 |
| 1419MahmudTanahi.MujizFiMarajic | 12,525 | 41 |
| 1420IbnBaz.FatawaNurCalaDarb | 1,627,900 | 5,426 |
| 1420IbnBaz.MajmucFatawa | 2,038,258 | 6,794 |
| 1421HamdJasir.MucjamQabailMCS | 67,689 | 225 |
| 1421MuhammadCuthaymin.FatawaArkanIslam | 108,365 | 361 |
| 1421MuhammadCuthaymin.FatawaNurCalaDarb | 1,572,869 | 5,242 |
| 1421MuhammadCuthaymin.MajmucFatawa | 2,025,627 | 6,752 |
| 1422IbnHadiWadici.RijalHakim | 152,657 | 508 |
| 1422MuhammadSalimMuhaysin.MucjamHuffazQuran | 169,932 | 566 |
| 1422MuqbilWadici.TarajimRijal | 122,531 | 408 |
| 1424IhsanCabbas.ShadharatMinKutubMafquda | 85,480 | 284 |
| 1429BakrIbnCabdAllah.TabaqatNassabin | 23,042 | 76 |
| 1430IbnJibrin.Fatawa | 314,884 | 1,049 |
| 1450AbuTayyibMansuri.Irshad | 144,616 | 482 |
| 1450AkramFaluji.MucjamSaghir | 251,265 | 837 |
| 1450AkramFaluji.MucjamShuyukhTabari | 240,016 | 800 |
| 1450CabdRahmanAlShaykh.Mashahir | 62,418 | 208 |
| 1450CadilNuwayhid.MucjamAclamJazair | 100,098 | 333 |
| 1450CulamaNajd.DurarSaniyya | 1,438,831 | 4,796 |
| 1450DarIftaMisriyya.FatawaDarIfta | 1,911,816 | 6,372 |
| 1450JamicaIslamiyya.MajallaJIMN | 5,405,231 | 18,017 |
| 1450LajnaDaima.Fatawa | 1,993,944 | 6,646 |
| 1450Maghrawi.MawsucaMawaqifSalaf | 952,565 | 3,175 |
| 1450MajmacFikrIslami.MawsucaMuallifiImamiya | 249,154 | 830 |
| 1450MawqicIslam.Fatawa | 2,607,138 | 8,690 |
| 1450MawsucaShicriya.MucjamShucara | 155,885 | 519 |
| 1450Milani.NafahatAzhar | 1,517,206 | 5,057 |
| 1450MuhammadAbtahi.TahdhibMaqal | 465,412 | 1,551 |
| 1450MuhammadHadiAmini.MucjamMatbicatNajafiya | 44,242 | 147 |
| 1450MuhammadKhayrRamadan.TakmilaMucjamMuallifin | 189,829 | 632 |
| 1450MuhammadSancani.NaylWatar | 150 | 0 |
| 1450MusaCaffana.Fatawa | 917,900 | 3,059 |
| 1450Musannifun.MawsucaMujaza | 668,172 | 2,227 |
| 1450SadiqRuhani.ManasikHajj | 33,192 | 110 |
| 1450SadiqRuhani.MasailMuntakhaba | 77,666 | 258 |
| 1450SadiqRuhani.MinhajSalihin | 177,800 | 592 |
| 1450SadiqRuhani.TakmilaMinhajSalihin | 34,593 | 115 |
| 1450SalahMahmudKhaymi.FaharisCulumQuran | 259,637 | 865 |
| 1450SalihFawzan.MajmucFatawa | 133,824 | 446 |
| 1450TarhibDawsari.MucjamMuallafatMalikiyya | 6,095 | 20 |
| 1450TarhibDawsari.MucjamMuallafatShaficiyya | 12,526 | 41 |
| 1450WahidKhurasani.MinhajSalihin | 392,908 | 1,309 |
| 1450WizaraAwqafMisriyya.TarajimMujaza | 26,409 | 88 |
| _female_names_in_0902Sakhawi.DuLamic | 941 | 3 |


## Chronological Distribution of Texts - up until 1930 (5,467 texts, 726,946,794 words)

- ~~6th century CE: 0 titles, 0 words~~
- **7th century CE: 29 titles, 656,855 words**
- **8th century CE: 84 titles, 6,126,423 words**
- **9th century CE: 506 titles, 31,731,358 words**
- **10th century CE: 674 titles, 60,026,199 words**
- **11th century CE: 688 titles, 71,114,785 words**
- **12th century CE: 461 titles, 53,112,691 words**
- **13th century CE: 447 titles, 59,578,221 words**
- **14th century CE: 578 titles, 96,792,091 words**
- **15th century CE: 328 titles, 72,980,538 words**
- **16th century CE: 251 titles, 59,867,783 words**
- **17th century CE: 160 titles, 53,548,425 words**
- **18th century CE: 151 titles, 33,836,230 words**
- **19th century CE: 200 titles, 59,558,191 words**
- **20th century CE: 129 titles, 16,837,153 words**
- ~~21st century CE: 0 titles, 0 words~~
- **TOTAL: 5,467 titles, 726,946,794 words**



## Forms, Themes, Genres (provisional assessment)

### *ADAB* (596 texts, 49,379,852 words)

- ~~6th century CE: 0 titles, 0 words~~
- **7th century CE: 2 titles, 19,107 words**
- **8th century CE: 7 titles, 209,885 words**
- **9th century CE: 48 titles, 2,956,390 words**
- **10th century CE: 86 titles, 6,981,561 words**
- **11th century CE: 94 titles, 6,518,363 words**
- **12th century CE: 86 titles, 7,939,889 words**
- **13th century CE: 44 titles, 5,591,528 words**
- **14th century CE: 37 titles, 4,720,991 words**
- **15th century CE: 23 titles, 3,522,201 words**
- **16th century CE: 32 titles, 1,187,974 words**
- **17th century CE: 10 titles, 2,794,471 words**
- **18th century CE: 6 titles, 1,206,440 words**
- **19th century CE: 14 titles, 705,377 words**
- **20th century CE: 13 titles, 1,173,560 words**
- ~~21st century CE: 0 titles, 0 words~~
- **TOTAL: 596 titles, 49,379,852 words**


### *ADHKAR* (210 texts, 10,840,197 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 1 titles, 16,317 words**
- **9th century CE: 10 titles, 348,180 words**
- **10th century CE: 15 titles, 775,222 words**
- **11th century CE: 14 titles, 492,787 words**
- **12th century CE: 34 titles, 2,616,690 words**
- **13th century CE: 15 titles, 1,178,644 words**
- **14th century CE: 16 titles, 996,909 words**
- **15th century CE: 6 titles, 331,299 words**
- **16th century CE: 12 titles, 378,561 words**
- **17th century CE: 2 titles, 21,449 words**
- **18th century CE: 4 titles, 905,376 words**
- **19th century CE: 4 titles, 234,025 words**
- **20th century CE: 2 titles, 112,685 words**
- ~~21st century CE: 0 titles, 0 words~~
- **TOTAL: 210 titles, 10,840,197 words**


### *ADILLA* (37 texts, 2,626,920 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 37 titles, 2,626,920 words**


### *AHKAM* (36 texts, 13,887,262 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 9 titles, 423,425 words**
- **10th century CE: 8 titles, 5,606,230 words**
- **11th century CE: 2 titles, 63,885 words**
- **12th century CE: 7 titles, 2,234,182 words**
- **13th century CE: 1 titles, 2,068,218 words**
- **14th century CE: 5 titles, 1,700,536 words**
- **15th century CE: 1 titles, 44,444 words**
- ~~16th century CE: 0 titles, 0 words~~
- **17th century CE: 1 titles, 9,769 words**
- **18th century CE: 1 titles, 261,323 words**
- **19th century CE: 1 titles, 1,475,250 words**
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **TOTAL: 36 titles, 13,887,262 words**


### *AHLAM* (9 texts, 931,763 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 1 titles, 211,445 words**
- **9th century CE: 1 titles, 24,681 words**
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
- **TOTAL: 9 titles, 931,763 words**


### *AJZA* (667 texts, 9,020,525 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 22 titles, 314,339 words**
- **9th century CE: 105 titles, 1,422,088 words**
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
- **TOTAL: 667 titles, 9,020,525 words**


### *AKHLAQ* (204 texts, 12,191,718 words)

- ~~6th century CE: 0 titles, 0 words~~
- **7th century CE: 2 titles, 123,285 words**
- **8th century CE: 3 titles, 171,423 words**
- **9th century CE: 57 titles, 1,044,919 words**
- **10th century CE: 27 titles, 1,453,988 words**
- **11th century CE: 23 titles, 734,655 words**
- **12th century CE: 19 titles, 1,721,017 words**
- **13th century CE: 11 titles, 2,664,007 words**
- **14th century CE: 38 titles, 3,268,872 words**
- **15th century CE: 2 titles, 28,166 words**
- **16th century CE: 9 titles, 336,228 words**
- **17th century CE: 1 titles, 16,342 words**
- **18th century CE: 3 titles, 59,116 words**
- **19th century CE: 5 titles, 299,708 words**
- **20th century CE: 1 titles, 109,344 words**
- ~~21st century CE: 0 titles, 0 words~~
- **TOTAL: 204 titles, 12,191,718 words**


### *ALBANI* (19 texts, 1,377,404 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 4 titles, 79,862 words**
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
- **TOTAL: 19 titles, 1,377,404 words**


### *AMALI* (12 texts, 159,787 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 2 titles, 13,840 words**
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
- **TOTAL: 12 titles, 159,787 words**


### *AMTHAL* (15 texts, 1,298,264 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 1 titles, 41,459 words**
- **9th century CE: 2 titles, 48,761 words**
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
- **TOTAL: 15 titles, 1,298,264 words**


### *ANSAB* (36 texts, 5,718,637 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 10 titles, 1,618,087 words**
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
- **TOTAL: 36 titles, 5,718,637 words**


### *ASHAB* (61 texts, 10,958,798 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 1 titles, 45,305 words**
- **9th century CE: 7 titles, 1,110,637 words**
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
- **TOTAL: 61 titles, 10,958,798 words**


### *BALAGHA* (354 texts, 33,029,507 words)

- ~~6th century CE: 0 titles, 0 words~~
- **7th century CE: 2 titles, 19,107 words**
- **8th century CE: 6 titles, 193,568 words**
- **9th century CE: 35 titles, 2,455,107 words**
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
- **TOTAL: 354 titles, 33,029,507 words**


### *BIB* (12 texts, 1,399,550 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 12 titles, 1,399,550 words**


### *BIO* (79 texts, 40,769,399 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 6 titles, 1,394,996 words**
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
- **TOTAL: 79 titles, 40,769,399 words**


### *BUHUTH* (175 texts, 4,638,412 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 3 titles, 90,498 words**
- **9th century CE: 6 titles, 274,845 words**
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
- **TOTAL: 175 titles, 4,638,412 words**


### *BULDAN* (151 texts, 32,709,465 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 2 titles, 4,799 words**
- **9th century CE: 20 titles, 3,084,580 words**
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
- **TOTAL: 151 titles, 32,709,465 words**


### *CAQAID* (517 texts, 29,879,440 words)

- ~~6th century CE: 0 titles, 0 words~~
- **7th century CE: 1 titles, 25,843 words**
- **8th century CE: 3 titles, 128,651 words**
- **9th century CE: 34 titles, 699,441 words**
- **10th century CE: 51 titles, 1,558,222 words**
- **11th century CE: 52 titles, 4,052,321 words**
- **12th century CE: 32 titles, 1,581,247 words**
- **13th century CE: 33 titles, 1,065,767 words**
- **14th century CE: 70 titles, 8,480,261 words**
- **15th century CE: 10 titles, 1,102,986 words**
- **16th century CE: 8 titles, 413,894 words**
- **17th century CE: 18 titles, 1,517,606 words**
- **18th century CE: 37 titles, 1,301,671 words**
- **19th century CE: 48 titles, 2,158,295 words**
- **20th century CE: 30 titles, 2,315,656 words**
- ~~21st century CE: 0 titles, 0 words~~
- **TOTAL: 517 titles, 29,879,440 words**


### *CARUD* (9 texts, 1,958,412 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 1 titles, 68,578 words**
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
- **TOTAL: 9 titles, 1,958,412 words**


### *CHR* (13 texts, 13,844,874 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 13 titles, 13,844,874 words**


### *CILAL* (69 texts, 6,380,949 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 15 titles, 484,960 words**
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
- **TOTAL: 69 titles, 6,380,949 words**


### *CIRFAN* (7 texts, 3,487,980 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 7 titles, 3,487,980 words**


### *COL* (78 texts, 45,261,680 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 4 titles, 1,099,770 words**
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
- **TOTAL: 78 titles, 45,261,680 words**


### *CULUM* (412 texts, 63,414,383 words)

- ~~6th century CE: 0 titles, 0 words~~
- **7th century CE: 1 titles, 15,330 words**
- **8th century CE: 7 titles, 601,640 words**
- **9th century CE: 20 titles, 1,386,096 words**
- **10th century CE: 32 titles, 8,763,797 words**
- **11th century CE: 49 titles, 6,809,780 words**
- **12th century CE: 31 titles, 5,467,849 words**
- **13th century CE: 25 titles, 7,507,767 words**
- **14th century CE: 40 titles, 7,254,329 words**
- **15th century CE: 41 titles, 10,058,956 words**
- **16th century CE: 22 titles, 4,013,299 words**
- **17th century CE: 9 titles, 323,446 words**
- **18th century CE: 11 titles, 545,057 words**
- **19th century CE: 4 titles, 5,107,008 words**
- **20th century CE: 6 titles, 486,830 words**
- ~~21st century CE: 0 titles, 0 words~~
- **TOTAL: 412 titles, 63,414,383 words**


### *DACIF* (44 texts, 4,118,004 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 6 titles, 313,864 words**
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
- **TOTAL: 44 titles, 4,118,004 words**


### *DACWA* (81 texts, 2,288,511 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 81 titles, 2,288,511 words**


### *FADAIL* (3 texts, 16,177 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 3 titles, 16,177 words**


### *FAHARIS* (53 texts, 8,202,795 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 53 titles, 8,202,795 words**


### *FALSAFA* (93 texts, 4,909,218 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 1 titles, 1,748 words**
- **9th century CE: 32 titles, 482,392 words**
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
- **TOTAL: 93 titles, 4,909,218 words**


### *FARQ* (8 texts, 460,423 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 2 titles, 88,948 words**
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
- **TOTAL: 8 titles, 460,423 words**


### *FASAHA* (39 texts, 4,652,773 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 5 titles, 340,543 words**
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
- **TOTAL: 39 titles, 4,652,773 words**


### *FATAWA* (32 texts, 7,530,433 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- **13th century CE: 1 titles, 27,528 words**
- **14th century CE: 3 titles, 592,878 words**
- **15th century CE: 2 titles, 24,713 words**
- **16th century CE: 4 titles, 1,539,515 words**
- ~~17th century CE: 0 titles, 0 words~~
- **18th century CE: 2 titles, 244,948 words**
- **19th century CE: 15 titles, 2,913,571 words**
- **20th century CE: 1 titles, 147,609 words**
- ~~21st century CE: 0 titles, 0 words~~
- **TOTAL: 32 titles, 7,530,433 words**


### *FAWAID* (14 texts, 203,216 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 1 titles, 1,423 words**
- **9th century CE: 1 titles, 7,761 words**
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
- **TOTAL: 14 titles, 203,216 words**


### *FIQH* (777 texts, 256,439,692 words)

- ~~6th century CE: 0 titles, 0 words~~
- **7th century CE: 1 titles, 30,942 words**
- **8th century CE: 10 titles, 2,133,322 words**
- **9th century CE: 56 titles, 10,572,765 words**
- **10th century CE: 71 titles, 12,379,338 words**
- **11th century CE: 86 titles, 25,601,998 words**
- **12th century CE: 51 titles, 12,593,546 words**
- **13th century CE: 65 titles, 20,924,847 words**
- **14th century CE: 105 titles, 36,497,661 words**
- **15th century CE: 47 titles, 25,348,530 words**
- **16th century CE: 71 titles, 31,190,143 words**
- **17th century CE: 34 titles, 9,589,355 words**
- **18th century CE: 41 titles, 22,371,227 words**
- **19th century CE: 65 titles, 35,370,893 words**
- **20th century CE: 27 titles, 4,773,862 words**
- ~~21st century CE: 0 titles, 0 words~~
- **TOTAL: 777 titles, 256,439,692 words**


### *FIRAQ* (19 texts, 2,093,490 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 19 titles, 2,093,490 words**


### *GEN* (12 texts, 1,732,134 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 8 titles, 1,360,907 words**
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
- **TOTAL: 12 titles, 1,732,134 words**


### *GEO* (32 texts, 3,354,197 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 32 titles, 3,354,197 words**


### *GHARIB* (124 texts, 27,626,205 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 1 titles, 456,502 words**
- **9th century CE: 23 titles, 1,070,048 words**
- **10th century CE: 21 titles, 4,345,423 words**
- **11th century CE: 18 titles, 4,136,424 words**
- **12th century CE: 15 titles, 2,947,637 words**
- **13th century CE: 13 titles, 2,847,675 words**
- **14th century CE: 6 titles, 3,501,559 words**
- **15th century CE: 7 titles, 1,217,218 words**
- **16th century CE: 5 titles, 52,175 words**
- **17th century CE: 2 titles, 432,615 words**
- **18th century CE: 4 titles, 5,431,435 words**
- **19th century CE: 3 titles, 975,182 words**
- **20th century CE: 1 titles, 28,889 words**
- ~~21st century CE: 0 titles, 0 words~~
- **TOTAL: 124 titles, 27,626,205 words**


### *GRAR* (150 texts, 2,385,551 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 1 titles, 1,748 words**
- **9th century CE: 39 titles, 617,499 words**
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
- **TOTAL: 150 titles, 2,385,551 words**


### *HAD* (3 texts, 1,559,638 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 1 titles, 10,042 words**
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
- **TOTAL: 3 titles, 1,559,638 words**


### *HADITH* (1,992 texts, 226,471,036 words)

- ~~6th century CE: 0 titles, 0 words~~
- **7th century CE: 4 titles, 260,901 words**
- **8th century CE: 41 titles, 3,530,626 words**
- **9th century CE: 258 titles, 19,306,273 words**
- **10th century CE: 397 titles, 30,831,210 words**
- **11th century CE: 356 titles, 30,415,812 words**
- **12th century CE: 196 titles, 16,482,593 words**
- **13th century CE: 178 titles, 11,915,776 words**
- **14th century CE: 149 titles, 22,334,930 words**
- **15th century CE: 147 titles, 30,695,218 words**
- **16th century CE: 66 titles, 15,921,981 words**
- **17th century CE: 44 titles, 27,042,668 words**
- **18th century CE: 29 titles, 5,064,161 words**
- **19th century CE: 20 titles, 3,422,793 words**
- **20th century CE: 16 titles, 4,489,353 words**
- ~~21st century CE: 0 titles, 0 words~~
- **TOTAL: 1,992 titles, 226,471,036 words**


### *HANAFI* (53 texts, 28,270,970 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 3 titles, 73,365 words**
- **9th century CE: 6 titles, 616,960 words**
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
- **TOTAL: 53 titles, 28,270,970 words**


### *HANBALI* (56 texts, 19,815,906 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 6 titles, 387,262 words**
- **10th century CE: 5 titles, 454,998 words**
- ~~11th century CE: 0 titles, 0 words~~
- **12th century CE: 2 titles, 32,913 words**
- **13th century CE: 5 titles, 2,548,949 words**
- **14th century CE: 12 titles, 7,730,172 words**
- **15th century CE: 3 titles, 2,248,171 words**
- **16th century CE: 3 titles, 532,703 words**
- **17th century CE: 6 titles, 2,016,521 words**
- **18th century CE: 8 titles, 845,866 words**
- **19th century CE: 1 titles, 1,063,300 words**
- **20th century CE: 1 titles, 112,736 words**
- ~~21st century CE: 0 titles, 0 words~~
- **TOTAL: 56 titles, 19,815,906 words**


### *HIS* (2 texts, 98,467 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 2 titles, 98,467 words**


### *IBNABIDUNYA* (59 texts, 808,380 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 59 titles, 808,380 words**
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
- **TOTAL: 59 titles, 808,380 words**


### *IBNQAYYIM* (36 texts, 4,224,213 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 36 titles, 4,224,213 words**


### *IBNTAYMIYYA* (75 texts, 9,437,074 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 75 titles, 9,437,074 words**


### *ICRAB* (3 texts, 772,636 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 3 titles, 772,636 words**


### *IMAM* (60 texts, 11,323,852 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 3 titles, 184,928 words**
- **9th century CE: 3 titles, 568,993 words**
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
- **TOTAL: 60 titles, 11,323,852 words**


### *JUGHRAFIYA* (68 texts, 7,955,509 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 1 titles, 2,282 words**
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
- **TOTAL: 68 titles, 7,955,509 words**


### *KITABA* (9 texts, 1,958,412 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 1 titles, 68,578 words**
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
- **TOTAL: 9 titles, 1,958,412 words**


### *KUTUB* (44 texts, 3,144,383 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 44 titles, 3,144,383 words**


### *LUGHA* (68 texts, 15,104,707 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 1 titles, 456,502 words**
- **9th century CE: 6 titles, 603,726 words**
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
- **TOTAL: 68 titles, 15,104,707 words**


### *MACAJIM* (172 texts, 38,498,365 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 2 titles, 476,460 words**
- **9th century CE: 40 titles, 5,686,476 words**
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
- **TOTAL: 172 titles, 38,498,365 words**


### *MAJALIS* (12 texts, 159,787 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 2 titles, 13,840 words**
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
- **TOTAL: 12 titles, 159,787 words**


### *MAJALLAT* (6 texts, 9,765,526 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 6 titles, 9,765,526 words**


### *MAJMUCAT* (44 texts, 18,468,777 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 2 titles, 303,136 words**
- **9th century CE: 1 titles, 170,879 words**
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
- **TOTAL: 44 titles, 18,468,777 words**


### *MAKHTUTAT* (300 texts, 1,975,198 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 2 titles, 11,989 words**
- **9th century CE: 16 titles, 74,770 words**
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
- **TOTAL: 300 titles, 1,975,198 words**


### *MALIKI* (44 texts, 25,105,006 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 3 titles, 1,389,796 words**
- **9th century CE: 1 titles, 6,087 words**
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
- **TOTAL: 44 titles, 25,105,006 words**


### *MANSUKH* (8 texts, 213,315 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 1 titles, 3,261 words**
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 8 titles, 213,315 words**


### *MANTIQ* (7 texts, 3,487,980 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 7 titles, 3,487,980 words**


### *MASAIL* (277 texts, 8,893,373 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 4 titles, 117,551 words**
- **9th century CE: 24 titles, 872,725 words**
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
- **TOTAL: 277 titles, 8,893,373 words**


### *MASANID* (39 texts, 8,094,316 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 1 titles, 19,958 words**
- **9th century CE: 15 titles, 3,322,911 words**
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
- **TOTAL: 39 titles, 8,094,316 words**


### *MAWDUC* (44 texts, 4,118,004 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 6 titles, 313,864 words**
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
- **TOTAL: 44 titles, 4,118,004 words**


### *MILAL* (234 texts, 14,585,690 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 2 titles, 7,598 words**
- **9th century CE: 24 titles, 469,867 words**
- **10th century CE: 38 titles, 1,289,107 words**
- **11th century CE: 39 titles, 2,873,359 words**
- **12th century CE: 19 titles, 1,015,259 words**
- **13th century CE: 16 titles, 512,816 words**
- **14th century CE: 46 titles, 6,926,705 words**
- **15th century CE: 4 titles, 197,786 words**
- **16th century CE: 4 titles, 295,951 words**
- **17th century CE: 5 titles, 86,504 words**
- **18th century CE: 18 titles, 170,202 words**
- **19th century CE: 12 titles, 336,647 words**
- **20th century CE: 5 titles, 309,736 words**
- ~~21st century CE: 0 titles, 0 words~~
- **TOTAL: 234 titles, 14,585,690 words**


### *MISC* (320 texts, 26,285,719 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 3 titles, 222,454 words**
- **9th century CE: 12 titles, 564,427 words**
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
- **TOTAL: 320 titles, 26,285,719 words**


### *MUDHAKKARAT* (11 texts, 955,128 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 11 titles, 955,128 words**


### *MUFASSIRUN* (3 texts, 146,094 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 3 titles, 146,094 words**


### *MUKHADRAM* (8 texts, 75,727 words)

- ~~6th century CE: 0 titles, 0 words~~
- **7th century CE: 3 titles, 28,157 words**
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 8 titles, 75,727 words**


### *MUSHKIL* (10 texts, 1,966,407 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 2 titles, 61,975 words**
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
- **TOTAL: 10 titles, 1,966,407 words**


### *MUSTALAHAT* (227 texts, 33,796,408 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 1 titles, 456,502 words**
- **9th century CE: 25 titles, 1,196,381 words**
- **10th century CE: 34 titles, 3,760,800 words**
- **11th century CE: 36 titles, 5,761,202 words**
- **12th century CE: 25 titles, 2,604,002 words**
- **13th century CE: 19 titles, 2,986,962 words**
- **14th century CE: 18 titles, 5,916,761 words**
- **15th century CE: 25 titles, 2,251,075 words**
- **16th century CE: 15 titles, 583,057 words**
- **17th century CE: 6 titles, 620,121 words**
- **18th century CE: 8 titles, 5,788,532 words**
- **19th century CE: 6 titles, 1,295,648 words**
- **20th century CE: 4 titles, 391,942 words**
- ~~21st century CE: 0 titles, 0 words~~
- **TOTAL: 227 titles, 33,796,408 words**


### *MUSTAQILLA* (6 texts, 2,465,091 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 6 titles, 2,465,091 words**


### *NABI* (60 texts, 11,323,852 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 3 titles, 184,928 words**
- **9th century CE: 3 titles, 568,993 words**
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
- **TOTAL: 60 titles, 11,323,852 words**


### *NAHW* (141 texts, 19,160,223 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 3 titles, 759,638 words**
- **9th century CE: 6 titles, 758,470 words**
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
- **TOTAL: 141 titles, 19,160,223 words**


### *NASIKH* (8 texts, 213,315 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 1 titles, 3,261 words**
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 8 titles, 213,315 words**


### *NO_TAGS* (4 texts, 678,543 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
- ~~10th century CE: 0 titles, 0 words~~
- ~~11th century CE: 0 titles, 0 words~~
- ~~12th century CE: 0 titles, 0 words~~
- ~~13th century CE: 0 titles, 0 words~~
- ~~14th century CE: 0 titles, 0 words~~
- **15th century CE: 1 titles, 589,291 words**
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **TOTAL: 4 titles, 678,543 words**


### *ONO* (4 texts, 1,237,148 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 4 titles, 1,237,148 words**


### *POE* (14 texts, 2,583,148 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 14 titles, 2,583,148 words**


### *QADA* (50 texts, 3,702,180 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 1 titles, 4,667 words**
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
- **TOTAL: 50 titles, 3,702,180 words**


### *QAWACID* (117 texts, 16,799,712 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 2 titles, 177,679 words**
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
- **TOTAL: 117 titles, 16,799,712 words**


### *QIRAAT* (29 texts, 2,385,777 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 2 titles, 19,171 words**
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
- **TOTAL: 29 titles, 2,385,777 words**


### *QISAS* (54 texts, 6,175,973 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 5 titles, 357,438 words**
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
- **TOTAL: 54 titles, 6,175,973 words**


### *QURAN* (299 texts, 63,485,456 words)

- ~~6th century CE: 0 titles, 0 words~~
- **7th century CE: 2 titles, 108,445 words**
- **8th century CE: 8 titles, 693,458 words**
- **9th century CE: 17 titles, 1,112,291 words**
- **10th century CE: 29 titles, 8,135,996 words**
- **11th century CE: 38 titles, 6,767,528 words**
- **12th century CE: 28 titles, 7,639,257 words**
- **13th century CE: 20 titles, 7,251,433 words**
- **14th century CE: 29 titles, 6,793,518 words**
- **15th century CE: 21 titles, 8,462,665 words**
- **16th century CE: 17 titles, 3,995,653 words**
- **17th century CE: 9 titles, 2,532,080 words**
- **18th century CE: 10 titles, 824,933 words**
- **19th century CE: 4 titles, 5,238,487 words**
- **20th century CE: 3 titles, 166,927 words**
- ~~21st century CE: 0 titles, 0 words~~
- **TOTAL: 299 titles, 63,485,456 words**


### *RAQAIQ* (183 texts, 10,119,943 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 1 titles, 16,317 words**
- **9th century CE: 9 titles, 282,039 words**
- **10th century CE: 14 titles, 771,481 words**
- **11th century CE: 13 titles, 355,629 words**
- **12th century CE: 29 titles, 2,569,003 words**
- **13th century CE: 14 titles, 1,153,698 words**
- **14th century CE: 13 titles, 983,884 words**
- **15th century CE: 5 titles, 320,080 words**
- **16th century CE: 10 titles, 365,106 words**
- **17th century CE: 1 titles, 5,107 words**
- **18th century CE: 3 titles, 870,170 words**
- **19th century CE: 4 titles, 234,025 words**
- **20th century CE: 2 titles, 112,685 words**
- ~~21st century CE: 0 titles, 0 words~~
- **TOTAL: 183 titles, 10,119,943 words**


### *RIHLAT* (69 texts, 7,976,897 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 1 titles, 2,282 words**
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
- **TOTAL: 69 titles, 7,976,897 words**


### *RUDUD* (65 texts, 4,134,417 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 1 titles, 1,418 words**
- **9th century CE: 3 titles, 97,763 words**
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
- **TOTAL: 65 titles, 4,134,417 words**


### *SAHIH* (10 texts, 4,806,999 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 2 titles, 1,090,940 words**
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
- **TOTAL: 10 titles, 4,806,999 words**


### *SARF* (141 texts, 19,160,223 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 3 titles, 759,638 words**
- **9th century CE: 6 titles, 758,470 words**
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
- **TOTAL: 141 titles, 19,160,223 words**


### *SHAFICI* (67 texts, 46,379,011 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 7 titles, 1,925,304 words**
- ~~10th century CE: 0 titles, 0 words~~
- **11th century CE: 7 titles, 5,704,498 words**
- **12th century CE: 5 titles, 1,907,928 words**
- **13th century CE: 7 titles, 6,324,457 words**
- **14th century CE: 3 titles, 483,862 words**
- **15th century CE: 4 titles, 484,155 words**
- **16th century CE: 22 titles, 16,946,519 words**
- **17th century CE: 1 titles, 590,267 words**
- **18th century CE: 3 titles, 6,606,897 words**
- **19th century CE: 5 titles, 3,947,008 words**
- **20th century CE: 1 titles, 186,843 words**
- ~~21st century CE: 0 titles, 0 words~~
- **TOTAL: 67 titles, 46,379,011 words**


### *SHAMAIL* (88 texts, 16,572,274 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 1 titles, 79,120 words**
- **9th century CE: 5 titles, 742,916 words**
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
- **TOTAL: 88 titles, 16,572,274 words**


### *SHARH* (83 texts, 37,817,466 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 1 titles, 1,221,983 words**
- **9th century CE: 8 titles, 984,601 words**
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
- **TOTAL: 83 titles, 37,817,466 words**


### *SHC* (18 texts, 3,549,125 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 18 titles, 3,549,125 words**


### *SHICI* (448 texts, 107,414,120 words)

- ~~6th century CE: 0 titles, 0 words~~
- **7th century CE: 6 titles, 317,686 words**
- **8th century CE: 8 titles, 607,856 words**
- **9th century CE: 10 titles, 1,098,703 words**
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
- **TOTAL: 448 titles, 107,414,120 words**


### *SHICR* (196 texts, 8,626,024 words)

- ~~6th century CE: 0 titles, 0 words~~
- **7th century CE: 19 titles, 107,439 words**
- **8th century CE: 14 titles, 238,833 words**
- **9th century CE: 14 titles, 728,032 words**
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
- **TOTAL: 196 titles, 8,626,024 words**


### *SHICRANDALUSI* (16 texts, 351,649 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 16 titles, 351,649 words**


### *SHICRCABBASI* (53 texts, 2,085,222 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 1 titles, 2,989 words**
- **9th century CE: 9 titles, 461,588 words**
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
- **TOTAL: 53 titles, 2,085,222 words**


### *SHICRCUTHMANI* (12 texts, 809,558 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 12 titles, 809,558 words**


### *SHICRISLAMI* (3 texts, 12,212 words)

- ~~6th century CE: 0 titles, 0 words~~
- **7th century CE: 1 titles, 1,941 words**
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 3 titles, 12,212 words**


### *SHICRJAHILI* (29 texts, 107,906 words)

- ~~6th century CE: 0 titles, 0 words~~
- **7th century CE: 14 titles, 74,537 words**
- **8th century CE: 1 titles, 3,145 words**
- **9th century CE: 1 titles, 629 words**
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
- **TOTAL: 29 titles, 107,906 words**


### *SHICRUMAWI* (21 texts, 254,022 words)

- ~~6th century CE: 0 titles, 0 words~~
- **7th century CE: 1 titles, 2,804 words**
- **8th century CE: 10 titles, 168,109 words**
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 21 titles, 254,022 words**


### *SIRA* (165 texts, 24,266,301 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 4 titles, 230,233 words**
- **9th century CE: 11 titles, 1,564,212 words**
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
- **TOTAL: 165 titles, 24,266,301 words**


### *SIYASA* (65 texts, 5,360,071 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 1 titles, 11,433 words**
- **9th century CE: 5 titles, 238,423 words**
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
- **TOTAL: 65 titles, 5,360,071 words**


### *SUALAT* (62 texts, 4,313,695 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 16 titles, 515,025 words**
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
- **TOTAL: 62 titles, 4,313,695 words**


### *SULUK* (88 texts, 6,377,189 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 1 titles, 9,586 words**
- **9th century CE: 3 titles, 58,239 words**
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
- **TOTAL: 88 titles, 6,377,189 words**


### *SUNAN* (15 texts, 5,517,153 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 7 titles, 1,143,125 words**
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
- **TOTAL: 15 titles, 5,517,153 words**


### *SUNNI* (360 texts, 113,935,121 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 9 titles, 680,173 words**
- **9th century CE: 80 titles, 10,976,932 words**
- **10th century CE: 80 titles, 16,393,874 words**
- **11th century CE: 61 titles, 15,302,943 words**
- **12th century CE: 21 titles, 13,570,825 words**
- **13th century CE: 24 titles, 10,489,844 words**
- **14th century CE: 29 titles, 15,608,560 words**
- **15th century CE: 28 titles, 15,961,680 words**
- **16th century CE: 14 titles, 6,195,895 words**
- **17th century CE: 3 titles, 1,835,177 words**
- **18th century CE: 7 titles, 515,627 words**
- **19th century CE: 2 titles, 5,053,898 words**
- **20th century CE: 2 titles, 1,349,693 words**
- ~~21st century CE: 0 titles, 0 words~~
- **TOTAL: 360 titles, 113,935,121 words**


### *TABAQAT* (351 texts, 74,811,081 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 2 titles, 4,799 words**
- **9th century CE: 40 titles, 4,219,795 words**
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
- **TOTAL: 351 titles, 74,811,081 words**


### *TAFSIR* (205 texts, 82,926,235 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 8 titles, 901,167 words**
- **9th century CE: 13 titles, 1,116,982 words**
- **10th century CE: 23 titles, 9,199,726 words**
- **11th century CE: 27 titles, 7,106,368 words**
- **12th century CE: 23 titles, 7,693,061 words**
- **13th century CE: 20 titles, 7,893,906 words**
- **14th century CE: 22 titles, 8,617,200 words**
- **15th century CE: 12 titles, 7,523,468 words**
- **16th century CE: 11 titles, 5,199,679 words**
- **17th century CE: 10 titles, 4,583,698 words**
- **18th century CE: 9 titles, 3,294,587 words**
- **19th century CE: 7 titles, 11,873,202 words**
- **20th century CE: 2 titles, 1,458,280 words**
- ~~21st century CE: 0 titles, 0 words~~
- **TOTAL: 205 titles, 82,926,235 words**


### *TAJWID* (16 texts, 1,411,578 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 1 titles, 12,707 words**
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
- **TOTAL: 16 titles, 1,411,578 words**


### *TAKHRIJ* (75 texts, 25,227,132 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 75 titles, 25,227,132 words**


### *TARAIF* (54 texts, 6,175,973 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 5 titles, 357,438 words**
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
- **TOTAL: 54 titles, 6,175,973 words**


### *TARAJIM* (768 texts, 151,531,554 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 15 titles, 651,617 words**
- **9th century CE: 102 titles, 12,592,823 words**
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
- **TOTAL: 768 titles, 151,531,554 words**


### *TARIKH* (310 texts, 74,474,408 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 2 titles, 4,799 words**
- **9th century CE: 37 titles, 4,344,252 words**
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
- **TOTAL: 310 titles, 74,474,408 words**


### *TASAWWUF* (10 texts, 2,430,845 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
- **10th century CE: 3 titles, 421,781 words**
- **11th century CE: 1 titles, 113,883 words**
- **12th century CE: 4 titles, 62,914 words**
- **13th century CE: 1 titles, 1,826,396 words**
- **14th century CE: 1 titles, 5,871 words**
- ~~15th century CE: 0 titles, 0 words~~
- ~~16th century CE: 0 titles, 0 words~~
- ~~17th century CE: 0 titles, 0 words~~
- ~~18th century CE: 0 titles, 0 words~~
- ~~19th century CE: 0 titles, 0 words~~
- ~~20th century CE: 0 titles, 0 words~~
- ~~21st century CE: 0 titles, 0 words~~
- **TOTAL: 10 titles, 2,430,845 words**


### *TAZKIYA* (34 texts, 3,209,984 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 34 titles, 3,209,984 words**


### *THIQAT* (13 texts, 3,327,383 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 2 titles, 117,398 words**
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
- **TOTAL: 13 titles, 3,327,383 words**


### *TIBB* (77 texts, 5,223,263 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 10 titles, 708,510 words**
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
- **TOTAL: 77 titles, 5,223,263 words**


### *TWELVERS* (58 texts, 5,318,002 words)

- ~~6th century CE: 0 titles, 0 words~~
- **7th century CE: 1 titles, 25,843 words**
- **8th century CE: 1 titles, 121,053 words**
- **9th century CE: 2 titles, 50,166 words**
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
- **TOTAL: 58 titles, 5,318,002 words**


### *USUL* (219 texts, 28,503,055 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 2 titles, 38,486 words**
- **9th century CE: 11 titles, 452,927 words**
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
- **TOTAL: 219 titles, 28,503,055 words**


### *USULIYYA* (23 texts, 1,295,289 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 23 titles, 1,295,289 words**


### *WAFAYAT* (29 texts, 11,154,222 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 29 titles, 11,154,222 words**


### *ZAHIRI* (1 texts, 1,480,381 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 1 titles, 1,480,381 words**


### *ZAYDI* (3 texts, 1,481,320 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- **8th century CE: 1 titles, 101,083 words**
- ~~9th century CE: 0 titles, 0 words~~
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
- **TOTAL: 3 titles, 1,481,320 words**


### *ZAYDIYYA* (5 texts, 85,596 words)

- ~~6th century CE: 0 titles, 0 words~~
- ~~7th century CE: 0 titles, 0 words~~
- ~~8th century CE: 0 titles, 0 words~~
- **9th century CE: 1 titles, 11,849 words**
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
- **TOTAL: 5 titles, 85,596 words**

