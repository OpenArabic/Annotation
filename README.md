# OpenArabic Project (@ AvH Lehrstuhl für Digital Humanities, U Leipzig, led and curated by Maxim Romanov)

**Contents**:
- [General Description](#general-description)
- [Prospects and Progress](#prospects-and-progress)
- [Text Description Tags](#text-description-tags)
- [Project/Folder Structure](#projectfolder-structure)
- [General Description of the Workflow with `mARkdown`](#general-description-of-the-workflow-with-markdown)
- [Status Report](#status-report)
- [Text Included in the Coprus](#text-currently-included-in-the-coprus)
- [Statistics on the Corpus](#statistics-on-the-corpus)

# General Description

The goal of the project is to build a machine-actionable corpus of premodern texts in Arabic to encourage computational analysis of Arabic literary tradition. Currently, most of the text are historical texts (chronicles, biographical collections, geographical treatises and gazetteers, thematic dictionaries); if you are interested in having other genres and forms, please, get in touch with us.

Most of the texts are coming from open online collections of premodern and modern Arabic texts, such as [http://shamela.ws/](http://shamela.ws/) and [http://shiaonlinelibrary.com/](http://shiaonlinelibrary.com/) (These texts have `Shamela+NUMBER` and `Shia+NUMBER`; some texts are coming from _al-Jāmiʿ al-kabīr_, which has been published on an external HDD and is not available online (`JK+NUMBER`). Initial metadata from these collections is preserved in the beginning of each file.

Currently uploaded have been automatically converted from their initial formats into `mARkdown` format—a flavor of `markdown` for tagging premodern Arabic text; they all require further editing, so that the structure of each text is tagged properly; the detailed description of `mARkdown` scheme and the tagging workflow can be found [http://maximromanov.github.io/mARkdown/](http://maximromanov.github.io/mARkdown/). When manual tagging is complete text will be converted into CTS-compliant XML format.

For the list of added books, see below (Mostly premodern chronicles, biographical collections, encyclopaedic dictionaries, gazetteers).

# Prospects and Progress

| *Texts* | *Status* |
|:--- | ------:|
| Total in the Collection | 10,393 |
| Unique texts | 7,781 |
| Added texts (listed below) | 607 |
| Orphans (no TXT) | 2 |

| *Texts* | *Status* |
|:--- | ------:|
| In Progress (`.inProgress`) | 5 |
| Completed (`.completed`) | 38 |
| Vetted (`.mARkdown`) | 2 |
| Converted to TEI XML  (`.xml`) | _pending_ |

# Text Description Tags

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

# Project/Folder structure

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

<!-- AUTOGENERATED CONTENT -->

# General description of the workflow with mARkdown

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
			* `git commit -m "MESSAGE"` saves the current status of the repository to the git versioning system; MESSAGE contains your own human readable description of what you have done. For example, if you finished tagging 3 volumes in the book that has 10, you can do `git commit -m "Finished tagging first 3 volumes"`. These messages will be visible in github repository online and help tracking progress. Also, you can roll back to the committed stage, if something wrong goes with the repository.
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
	* `git commit -m "Started working on the file"` (message does not have to be exactly the same)
	* `git push origin master`
	* **NB:** Before you start a new text, make sure to pull the latest changes to the repository, i.e., run `git pull origin master`
9. Keep in mind that you need to tag only the structure of a book you are working with,  which includes tagging chapter headers (`### |`, `### ||`, `### |||`, etc.) and major information units, like biographies (`### $`, `### $$`, `### $$$`, etc.) or lexicon items (these we should discuss before you start). Please, do not tag anything else—at least without consulting with me first.
10. **IMPORTANT!** Do not delete anything from the text! At this point we do not know what is valuable and what is not (things like numbers, random characters, punctuation, stray HTML tags, etc.). **Your goal is to provide the structure to texts, not to edit them**. If you think something should be deleted, please, consult me first. Time is the most valuable asset at the moment and we cannot afford to spend it on fixing messed-up texts; we want to invest it into tagging logical units of as many new texts as possible.
10. Make commits to relevant github repositories after each working session. In addition to saving/backing up your work, this will also allow me to check periodically on your progress and make suggestions along the way.
11. When you have finished tagging a text, change its extension from `.inProgress` to `.completed`; then push your changes to the online repository.\* After that I will review the tagging and if everything is fine, I will change the extension to `.mARkdown`, which will indicate that the tagging of the file has been complete and vetted.
	* Git commands:
		* `git add .`
		* `git commit -m "tagging is complete"`
		* `git push origin master`
	* **NB:** The extensions are important as they allow everyone to see at which stage the files are; they are also used to generate the progress report, which will be included into the `README.md` file of each repository. 
11. Into the `README.md` which is in the same folder as the text file you are working on, please add the number of hours it took you to process the file. We are trying to get estimates on how much time it is going to take to process the entire corpus; we also know at the moment that the amount of time is not proportional to the length of a text, since what matters most is how much structural information is preserved in the initial file and that differs drastically from text to text.

These are the major steps.  Please, do not hesitate to contact the me if you have any questions, no matter how insignificant they may seem to you.

# Status Report

## In Progress (5)

- `0230IbnSacd.TabaqatKubra.Shamela0001686-ara1.inProgress`
- `0256Bukhari.TarikhKabir.Shamela0000956-ara1.inProgress`
- `0310Tabari.Tarikh.Shamela0009783-ara1.inProgress`
- `0310Tabari.Tarikh.Shia003474Vols-ara1.inProgress`
- `1339IsmacilBashaBaghdadi.HadiyaCarifin.Shia003362Vols-ara1.inProgress`

## Completed (38)

- `0276IbnQutaybaDinawari.AdabKatib.Shamela0026349-ara1.completed`
- `0355MuhammadKindi.WulatMisr.JK010325-ara1.completed`
- `0369AbuShaykhIsbahani.TabaqatMuhaddithin.Shamela0004182-ara1.completed`
- `0379MuhammadRabci.TarikhMawlidCulama.JK000651-ara1.completed`
- `0390Muqaddasi.AhsanTaqasim.Shamela0023696-ara1.completed`
- `0403IbnFaradi.TarikhCulamaAndalus.JK001462-ara1.completed`
- `0405HakimNaysaburi.TalkhisTarikhNaysabur.Shamela0004017-ara1.completed`
- `0412Sulami.TabaqatSufiya.Shamela0006686-ara1.completed`
- `0427HamzaJurjani.TarikhJurjan.Shamela0011077-ara1.completed`
- `0430AbuNucaymIsbahani.HilyaAwliya.JK000022-ara1.completed`
- `0430AbuNucaymIsbahani.TarikhIsbahan.Shia003488Vols-ara1.completed`
- `0442Tanukhi.TarikhCulamaNahwiyyin.Shamela0001386-ara1.completed`
- `0446AbuYaclaKhalili.IrshadFiMacrifaCulama.JK000732-ara1.completed`
- `0450Najashi.Rijal.Shia002931-ara1.completed`
- `0458Bayhaqi.DalailNubuwwa.JK006838-ara1.completed`
- `0460ShaykhTusi.IkhtiyarMacrifaRijal.Shia002932Vols-ara1.completed`
- `0460ShaykhTusi.Rijal.Shia002935-ara1.completed`
- `0463IbnCabdBarr.IsticabFiMacrifaAshab.JK000778-ara1.completed`
- `0463KhatibBaghdadi.TarikhBaghdad.Shamela0000736-ara1.completed`
- `0466CabdAzizKattani.DhaylTarikhMawlidCulama.JK000770-ara1.completed`
- `0476AbuIshaqShirazi.TabaqatFuqaha.Shamela0001031-ara1.completed`
- `0482AbuIshaqHabbal.WafayatMisriyyin.JK000712-ara1.completed`
- `0521IbnAbiYacla.TabaqatHanabila.JK000213-ara1.completed`
- `0524IbnAkfani.DhaylDhaylTarikhMawlidCulama.JK000695-ara1.completed`
- `0544CiyadIbnMusaYahsubi.TartibMadarik.Shamela0031215-ara1.completed`
- `0555IbnQalanisi.Tarikh.Shamela0022799-ara1.completed`
- `0565IbnZaydBayhaqi.TarikhBayhaq.Shamela0011758-ara1.completed`
- `0571IbnCasakir.TarikhDimashq.JK000916-ara1.completed`
- `0577IbnAnbari.NuzhaAlibba.Shamela0003583-ara1.completed`
- `0578IbnBashkuwal.Sila.Shamela0022788-ara1.completed`
- `0597IbnJawzi.Muntazam.Shamela0012406-ara1.completed`
- `0600KatibMarrakushi.Istibsar.Shamela0011684-ara1.completed`
- `0626YaqutHamawi.MucjamBuldan.Shamela0023735-ara1.completed`
- `0630IbnAthirCizzDin.LubabFiTahdhibAnsab.Shamela0005793-ara1.completed`
- `0658IbnAbbar.HullaSiyara.Shamela0006630-ara1.completed`
- `0658IbnAbbar.TakmilaLiSila.JK001319-ara1.completed`
- `0774IbnKathir.TabaqatShaficiyyin.Shamela0012860-ara1.completed`
- `0900AbuCabdAllahHimyari.RawdMictar.Shamela0001043-ara1.completed`

## Vetted (2)

- `0310Tabari.Tarikh.Shia003474Vols-ara1.mARkdown`
- `0658IbnAbbar.TuhfaQadim.Shamela0026108-ara1.mARkdown`

# Text currently included in the Coprus

## List of books by centuries (607 titles)

* **0100AH [[ [Re]generated on 2016-08-21 (20:32:00) ]]**

    * _no texts at the moment_

* **0200AH [[ [Re]generated on 2016-08-21 (20:32:00) ]]**

    * `0110HasanBasri.FadailMakka `
    * `0195MuarrijSadusi.HadhfMinNasabQuraysh `
    * `0200AbuShis.Diwan `

* **0300AH [[ [Re]generated on 2016-08-21 (20:32:00) ]]**

    * `0204IbnKalbi.AnsabKhayl `
    * `0204IbnKalbi.JamharaAnsab `
    * `0204IbnKalbi.NasabMacad `
    * `0207Waqidi.FutuhSham `
    * `0207Waqidi.Maghazi `
    * `0207Waqidi.Ridda `
    * `0209MacmarIbnMuthanna.Khayl `
    * `0211AbuCatahiya.Diwan `
    * `0213IbnHisham.SiraNabawiyya `
    * `0213IbnHisham.Tijan `
    * `0222IbnBakkarDabi.AkhbarWafidat `
    * `0222IbnBakkarDabi.AkhbarWafidin `
    * `0228IbnHammadKhuzaci.Fitan `
    * `0230IbnSacd.TabaqatKubra `
    * `0231IbnSallamJumahi.TabaqatFuhulShucara `
    * `0233YahyaIbnMacin.MacrifaRijal `
    * `0233YahyaIbnMacin.MinKalamFiRijal `
    * `0233YahyaIbnMacin.TarikhIbnMacin `
    * `0234AbuHasanSacdi.TasmiyaManRuwiya `
    * `0236AbuCabdAllahZubayri.NasabQuraysh `
    * `0240KhalifaIbnKhayyat.Tabaqat `
    * `0240KhalifaIbnKhayyat.Tarikh `
    * `0241IbnHanbal.AsamiWaKuna `
    * `0241IbnHanbal.CilalWaMacrifa `
    * `0241IbnHanbal.FadailSahaba `
    * `0245MuhammadIbnHabib.MukhtalafQabail `
    * `0245MuhammadIbnHabib.MunammaqFiAkhbarQuraysh `
    * `0248AbuHatimSijistani.FuhulaShucara `
    * `0249Azraqi.AkhbarMakka `
    * `0255Jahiz.AmilWaMamul `
    * `0255Jahiz.BayanWaTabyin `
    * `0255Jahiz.Bighal `
    * `0255Jahiz.Bukhala `
    * `0255Jahiz.BursanWaCurjan `
    * `0255Jahiz.Cuthmaniya `
    * `0255Jahiz.Hayawan `
    * `0255Jahiz.MahasinWaAddad `
    * `0255Jahiz.MukhtarFiRaddCalaNasara `
    * `0255Jahiz.Rasail `
    * `0255Jahiz.TabsiraBiTijara `
    * `0255Jahiz.TajFiAkhlaq `
    * `0256Bukhari.Ducafa `
    * `0256Bukhari.DucafaSaghir `
    * `0256Bukhari.TarikhKabir `
    * `0256Bukhari.TarikhSaghir `
    * `0256ZubayrIbnBakkar.AkhbarMuwaffaqiyat `
    * `0256ZubayrIbnBakkar.JamharaNasabQuraysh `
    * `0256ZubayrIbnBakkar.Muntakhab `
    * `0257IbnCabdHakam.FutuhMisr `
    * `0259IbnYacqubJuzjani.AhwalRijal `
    * `0261AbuHasanCijli.MacrifaThiqat `
    * `0261Muslim.KunaWaAsma `
    * `0261Muslim.Munfaridat `
    * `0262AbuZaydNumayri.TarikhMadina `
    * `0264AbyZurca.Ducafa `
    * `0272Fakihi.AkhbarMakka `
    * `0276IbnQutaybaDinawari.AdabKatib `
    * `0276IbnQutaybaDinawari.Macarif `
    * `0277AbuHatimRazi.JarhWaTacdil `
    * `0277IbnSyfyanFasawi.MacrifaWaTarikh `
    * `0279Baladhuri.AnsabAshraf `
    * `0279Baladhuri.FutuhBuldan `
    * `0279IbnAbiKhaythama.TarikhKabir `
    * `0280IbnTayfur.Baghdad `
    * `0280IbnTayfur.BallaghatNisa `
    * `0281AbuZurcaDimashqi.Tarikh `
    * `0282AbuHanifaDinawari.AkhbarTiwal `
    * `0286Mubarrad.NasabCadnan `
    * `0287Dahhak.AhadWaMathani `
    * `0292Bahshal.TarikhWasit `
    * `0292Yacqubi.Buldan `
    * `0292Yacqubi.TarikhYacqubi `
    * `0296IbnMuctazz.Diwan `
    * `0296IbnMuctazz.TabaqatShucara `
    * `0296MuhammadIbnJarrah.ManIsmuhCamr `
    * `0300IbnKhurdadhbih.MasalikWaMamalik `
    * `0300MuallifMajhul.AkhbarDawlaCabbasiya `

* **0400AH [[ [Re]generated on 2016-08-21 (20:32:00) ]]**

    * `0301Bardiji.TabaqatAsma `
    * `0303Nasai.DucafaWaMatrukin `
    * `0303Nasai.FadailSahaba `
    * `0303Nasai.Tabaqat `
    * `0303Nasai.TasmiyaFuqaha `
    * `0303Nasai.TasmiyaManLamYarwi `
    * `0303Nasai.TasmiyaShuyukh `
    * `0306IbnHayyanDabbi.AkhbarQudat `
    * `0308IbnIbrahimJundi.FadailMadina `
    * `0308IbnIbrahimJundi.FadailMadina `
    * `0309IbnFadlan.Rihla `
    * `0310IbnAhmadDulabi.Dhariyya `
    * `0310IbnAhmadDulabi.KunaWaAsma `
    * `0310Tabari.JamicBayan `
    * `0310Tabari.MuntakhabMinDhayl `
    * `0310Tabari.Tarikh `
    * `0317AbuQasimBaghawi.MucjamSahaba `
    * `0317AbuQasimBaghawi.TarikhWafatShuyukh `
    * `0318AbuCurubaHarrani.MuntaqaMinTabaqat `
    * `0320CaribQurtubi.SilaTarikhTabari `
    * `0322AbuJacfarCuqayli.DucafaKabir `
    * `0322KatibBaghdadi.TarikhAimma `
    * `0330Sirafi.Rihla `
    * `0333AbuCarabTamimi.Mihan `
    * `0333AbuCarabTamimi.TabaqatCulama `
    * `0334IbnHaikHamdani.Iklil `
    * `0334IbnHaikHamdani.SifaJaziraCarab `
    * `0334IbnSacidQushayri.TarikhRaqqa `
    * `0337IbnIshaqZajjaji.Akhbar `
    * `0346Istakhri.MasalikWaMamalik `
    * `0346Mascudi.AkhbarZaman `
    * `0346Mascudi.MurujDhahab `
    * `0346Mascudi.TanbihWaIshraf `
    * `0347IbnYunusSadafi.Tarikh `
    * `0349IbnCumarMuqri.AkhbarNahwiyyin `
    * `0351IbnQanic.MucjamSahaba `
    * `0354IbnHibban.Majruhin `
    * `0354IbnHibban.MashahirCulamaAmsar `
    * `0354IbnHibban.Sira `
    * `0354IbnHibban.Thiqat `
    * `0355AbuFarajIsbahani.Aghani `
    * `0355AbuFarajIsbahani.Diyarat `
    * `0355MuhammadKindi.FadailMisr `
    * `0355MuhammadKindi.WulatMisr `
    * `0360Khawlani.TarikhDaraya `
    * `0360Tabarani.MucjamKabir `
    * `0365IbnCadiJurjani.AsamiManRawaCanhum `
    * `0365IbnCadiJurjani.KamilFiDucafa `
    * `0365IbnFaqihHamadhani.Buldan `
    * `0367IbnHawqal.SuraArd `
    * `0368AbuGhalibZurari.Risala `
    * `0368Sirafi.AkhbarNahwiyyin `
    * `0369AbuShaykhIsbahani.TabaqatMuhaddithin `
    * `0370IbnBishrAmidi.MutalifWaMukhtalif `
    * `0371AhmadJurjani.Mucjam `
    * `0374IbnHusaynAzdi.AsmaManYucrafBiKunya `
    * `0374IbnHusaynAzdi.DhikrIsmKullAshab `
    * `0374IbnHusaynAzdi.KunaLiManLaYucrafLahuIsm `
    * `0374IbnHusaynAzdi.Makhzun `
    * `0374IbnHusaynAzdi.ManWafaqaIsmuhuIsmAbihi `
    * `0379MuhammadRabci.TarikhMawlidCulama `
    * `0380Muhallabi.MasalikWaMamalik `
    * `0382IbnCabdAllahCaskari.AkhbarMusahhifin `
    * `0384IbnCimranMarzubani.MucjamShucara `
    * `0385Daruqutni.DhikrAsmaTabicin `
    * `0385Daruqutni.Ducafa `
    * `0385Daruqutni.MutalifWaMukhtalif `
    * `0385Daruqutni.SualatBarqani `
    * `0385Daruqutni.SualatNaysaburi `
    * `0385IbnNadim.Fihrist `
    * `0385IbnShahin.TarikhAsmaDucafa `
    * `0385IbnShahin.TarikhAsmaThiqat `
    * `0388Shabushti.Diyarat `
    * `0390Muqaddasi.AhsanTaqasim `
    * `0395AbuHilalCaskari.Talkhis `
    * `0395IbnMandahMuhammad.Asami `
    * `0395IbnMandahMuhammad.FathBab `
    * `0395IbnMandahMuhammad.MacrifaSahaba `
    * `0398AbuNasrKalabadhi.HidayaWaIrshad `
    * `0400IbnTahirMaqdisi.BadWaTarikh `
    * `0400IshaqMunajjim.AkamMarjan `

* **0500AH [[ [Re]generated on 2016-08-21 (20:32:00) ]]**

    * `0402MuhammadSaydawi.MucjamShuyukh `
    * `0403IbnFaradi.TarikhCulamaAndalus `
    * `0405AbuFadlHarawi.MucjamFiMushtabah `
    * `0405HakimNaysaburi.TalkhisTarikhNaysabur `
    * `0405HakimNaysaburi.TasmiyaManAkhrajahum `
    * `0409CabdGhaniAzdi.KitabMutawarin `
    * `0412Sulami.TabaqatSufiya `
    * `0418WazirMaghribi.AdabKhawas `
    * `0418WazirMaghribi.Inas `
    * `0421IbnMuhammadMarzuqi.AzminaWaAmkina `
    * `0421Miskawayh.Tajarib `
    * `0427HamzaJurjani.TarikhJurjan `
    * `0428IbnManjuwayhIsbahani.RijalSahihMuslim `
    * `0429AbuMansurThacalibi.YatimaDahr `
    * `0429Thacalibi.ThimarQulub `
    * `0430AbuNucaymIsbahani.DhikrManIsmuhuShucba `
    * `0430AbuNucaymIsbahani.Ducafa `
    * `0430AbuNucaymIsbahani.HilyaAwliya `
    * `0430AbuNucaymIsbahani.MacrifaSahaba `
    * `0430AbuNucaymIsbahani.TarikhIsbahan `
    * `0430AbuNucaymIsbahani.TasmiyaMaIntahaIlayna `
    * `0436HusaynSaymari.AkhbarAbiHanifa `
    * `0440AbuRayhanBiruni.TahqiqMaLilHind `
    * `0442Tanukhi.TarikhCulamaNahwiyyin `
    * `0446AbuYaclaKhalili.IrshadFiMacrifaCulama `
    * `0448HilalSabi.TuhfaUmara `
    * `0449AbuCalaMacarri.Diwan `
    * `0450Najashi.Rijal `
    * `0456IbnHazm.AsmaKhulafa `
    * `0456IbnHazm.FadailAndalus `
    * `0456IbnHazm.JamharaAnsab `
    * `0456IbnHazm.NaqtCarus `
    * `0456IbnHazm.RisalaFiFutuhIslam `
    * `0456IbnHazm.RisalaFiMaratibCulum `
    * `0456IbnHazm.UmmahatKhulafa `
    * `0458Bayhaqi.DalailNubuwwa `
    * `0460ShaykhTusi.IkhtiyarMacrifaRijal `
    * `0460ShaykhTusi.Rijal `
    * `0463IbnCabdBarr.InbahCalaQabail `
    * `0463IbnCabdBarr.IsticabFiMacrifaAshab `
    * `0463KhatibBaghdadi.GhunyaMultamis `
    * `0463KhatibBaghdadi.MuttafiqWaMuftariq `
    * `0463KhatibBaghdadi.TalkhisMutashabih `
    * `0463KhatibBaghdadi.TarikhBaghdad `
    * `0466CabdAzizKattani.DhaylTarikhMawlidCulama `
    * `0469IbnHayyanQurtubi.Muqtabas `
    * `0474IbnKhalafBaji.TacdilWaTakhrij `
    * `0475IbnMakula.IkmalFiRafcIrtiyab `
    * `0475IbnMakula.TahdhibMustamirr `
    * `0476AbuIshaqShirazi.TabaqatFuqaha `
    * `0482AbuIshaqHabbal.WafayatMisriyyin `
    * `0487AbuCubaydBakri.MasalikWaMamalik `
    * `0487AbuCubaydBakri.MucjamMaIstacjama `
    * `0488IbnFutuhHumaydi.JadhwaMuqtabis `
    * `0498AbuCaliJayyani.AlqabSahaba `
    * `0498AbuCaliJayyani.TaqyidMuhmal `

* **0600AH [[ [Re]generated on 2016-08-21 (20:32:00) ]]**

    * `0507AbuBakrShashi.HilyaCulama `
    * `0507IbnQaysarani.AnsabMuttafiqa `
    * `0508FattalNaysaburi.RawdaWacizin `
    * `0511IbnMandahYahya.MacrifaAsamiArdaf `
    * `0511SalmaSahari.Ansab `
    * `0515IbnQattac.DurraKhatira `
    * `0521IbnAbiYacla.TabaqatHanabila `
    * `0521MuhammadHamadhani.TakmilaTarikhTabari `
    * `0524IbnAkfani.DhaylDhaylTarikhMawlidCulama `
    * `0528FathIbnKhaqan.QalaidCiqyan `
    * `0535QawwamSunna.DalailNubuwwa `
    * `0535QawwamSunna.SiyarSalaf `
    * `0538MahmudZamakhshari.JibalWaAmkina `
    * `0541IbnCatiyyaMuharibi.Fahrasa `
    * `0542IbnBassamShantarini.Dhakhira `
    * `0544CiyadIbnMusaYahsubi.Ghunya `
    * `0544CiyadIbnMusaYahsubi.TartibMadarik `
    * `0550AbuHajjajAshcari.TacrifBiAnsab `
    * `0555IbnQalanisi.Tarikh `
    * `0560SharifIdrisi.NuzhaMushtaq `
    * `0561Samcani.Ansab `
    * `0561Samcani.Muntakhab `
    * `0561Samcani.Tahbir `
    * `0565IbnZaydBayhaqi.LubabAnsab `
    * `0565IbnZaydBayhaqi.TarikhBayhaq `
    * `0565IbnZaydBayhaqi.TatimmaSiwanHikma `
    * `0567IbnKhashshabBaghdadi.TarikhMawalidAimma `
    * `0569CumaraHakami.NukatCasriyya `
    * `0571IbnCasakir.MucjamShuyukh `
    * `0571IbnCasakir.TarikhDimashq `
    * `0573NashwanHimyari.KhulasaSiyar `
    * `0575IbnBabawayh.Fihrist `
    * `0575IbnKhayrIshbili.Fahrasa `
    * `0576IbnMuhammadSilafi.Mashyakha `
    * `0576IbnMuhammadSilafi.MashyakhaBaghdadiyya `
    * `0576IbnMuhammadSilafi.MucjamSafar `
    * `0576IbnMuhammadSilafi.Wajiz `
    * `0577IbnAnbari.NuzhaAlibba `
    * `0578IbnBashkuwal.GhawamidAsma `
    * `0578IbnBashkuwal.Sila `
    * `0580IbnCimrani.InbaFiTarikhKhulafa `
    * `0584IbnMunqidhShayzari.Ictibar `
    * `0584IbnMusaHazimi.Amakin `
    * `0584IbnMusaHazimi.CujalaMubtadi `
    * `0597CimadDinKatib.BarqShami `
    * `0597CimadDinKatib.KharidaQasr `
    * `0597IbnJawzi.DucafaWaMatrukin `
    * `0597IbnJawzi.FadailQuds `
    * `0597IbnJawzi.Mashyakha `
    * `0597IbnJawzi.Muntazam `
    * `0597IbnJawzi.MuthirGharam `
    * `0597IbnJawzi.SifaSafwa `
    * `0597IbnJawzi.TalqihFuhum `
    * `0597IbnJawzi.TarikhBaytMuqaddas `
    * `0599IbnYahyaDabbi.BughyaMultamis `
    * `0600AbuBaqaHilli.ManaqibMazidiya `
    * `0600KatibMarrakushi.Istibsar `

* **0700AH [[ [Re]generated on 2016-08-21 (20:32:00) ]]**

    * `0606IbnMamati.LataifDhakhira `
    * `0611CaliHarawi.Isharat `
    * `0611SharafDinMuqaddasi.Arbacin `
    * `0614IbnJubayr.Rihla `
    * `0615MuwaffaqDinShafici.MurshidZuwwar `
    * `0617MansurIbnShahanshah.MidmarHaqaiq `
    * `0623Qazwini.Tadwin `
    * `0626YaqutHamawi.Khazal `
    * `0626YaqutHamawi.MucjamBuldan `
    * `0626YaqutHamawi.MucjamUdaba `
    * `0628IbnCaliSanhaji.AkhbarMuluk `
    * `0629IbnNuqta.IfadaWaIctibar `
    * `0629IbnNuqta.TakmilaIkmal `
    * `0629IbnNuqta.TaqyidLiMacrifa `
    * `0630IbnAthirCizzDin.Kamil `
    * `0630IbnAthirCizzDin.LubabFiTahdhibAnsab `
    * `0630IbnAthirCizzDin.UsdGhaba `
    * `0632AbyHafsSuhrawardi.Mashyakha `
    * `0632IsmacilMarwazi.FakhriFiAnsab `
    * `0637IbnMustafwi.TarikhIrbil `
    * `0639AbuBakrMalaqi.MatlacAnwar `
    * `0640AbuHafsDunaysiri.TarikhDunaysir `
    * `0641Sarifini.Muntakhab `
    * `0642IbnNajjar.DhaylTarikhBaghdad `
    * `0643DiyaDinMuqaddasi.FadailBaytMaqdis `
    * `0643DiyaDinMuqaddasi.JuzAwham `
    * `0643IbnSalahShahrazuri.TabaqatFuqaha `
    * `0645TilimsaniBurri.Jawhara `
    * `0646IbnQifti.IkhbarCulama `
    * `0646IbnQifti.InbahRuwat `
    * `0646IbnQifti.Muhammadun `
    * `0647CabdWahidMarrakushi.Mucjib `
    * `0650IbnNazifHamawi.TarikhMansuri `
    * `0657IbnIbrahimIrbili.MudhakaraFiAlqab `
    * `0658IbnAbbar.HullaSiyara `
    * `0658IbnAbbar.MucjamAshab `
    * `0658IbnAbbar.TakmilaLiSila `
    * `0658IbnAbbar.TuhfaQadim `
    * `0659SainDinNaccal.Mashyakha `
    * `0660IbnCadim.BughyatTalib `
    * `0660IbnCadim.ZubdaHalab `
    * `0665AbuShama.Rawdatayn `
    * `0668IbnAbiUsaybica.CuyunAnba `
    * `0673AbuMahasinYaghmuri.NurQabas `
    * `0676Nawawi.TahdhibAsma `
    * `0677SahibTaji.HalbaFiAsmaKhayl `
    * `0680IbnSabuni.TakmilaIkmalIkmal `
    * `0681IbnKhallikan.WafayatAcyan `
    * `0682ZakariyaQazwini.AtharBilad `
    * `0684IbnShaddad.AclaqKhatira `
    * `0685IbnCibri.TarikhMukhtasarDuwal `
    * `0685IbnSacidMaghribi.GhusunYanica `
    * `0685IbnSacidMaghribi.Jughrafiya `
    * `0685IbnSacidMaghribi.Mughrib `
    * `0690IbnMujawirDimashqi.TarikhMustabsir `
    * `0691IbnYusufLabli.Fihrist `
    * `0694MuhibbDinTabari.Dhakhair `
    * `0694MuhibbDinTabari.RiyadNadira `
    * `0695IbnCidhariMarrakushi.BayanMaghrib `
    * `0696Dabbagh.MacalimIman `
    * `0696IbnZahiri.Mashyakha `

* **0800AH [[ [Re]generated on 2016-08-21 (20:32:00) ]]**

    * `0701SharafDinYunini.Mashyakha `
    * `0703MuhammadMarrakushi.DhaylWaTakmila `
    * `0705SharafDinDimyatti.MucjamShuyukh `
    * `0709CaliCalawi.Majdi `
    * `0711IbnManzurIfriqi.MukhtasarTarikhDimashq `
    * `0714AhmadGhibrini.CunwanDiraya `
    * `0723IbnFuwati.Hawadith `
    * `0726CallamaHilli.KhulasaAqwal `
    * `0726Yunini.DhaylMiratZaman `
    * `0730MuhammadTujibi.Barnamaj `
    * `0732AbuFida.MukhtasarFiAkhbar `
    * `0732AbuFida.Yawaqit `
    * `0732IbnYacqubJanadi.SulukFiTabaqat `
    * `0733IbnJamaca.Mashyakha `
    * `0733Nuwayri.NihayaArab `
    * `0739SafiDinHanbali.Marasid `
    * `0740IbnDawudHilli.Rijal `
    * `0741KhatibTabrizi.Ikmal `
    * `0742Mizzi.TahdhibKamal `
    * `0747MuhyiDinYunini.Mashyakha `
    * `0748Dhahabi.CibarFiKhabar `
    * `0748Dhahabi.Culuww `
    * `0748Dhahabi.DhaylCibar `
    * `0748Dhahabi.DhaylDiwanDucafa `
    * `0748Dhahabi.DhikrAsmaManTakallama `
    * `0748Dhahabi.DiwanDucafa `
    * `0748Dhahabi.Kashif `
    * `0748Dhahabi.MacrifaQurraKibar `
    * `0748Dhahabi.MizanIctidal `
    * `0748Dhahabi.MucinFiTabaqatMuhaddithin `
    * `0748Dhahabi.MucjamMuhaddithin `
    * `0748Dhahabi.MucjamShuyukh `
    * `0748Dhahabi.MughniFiDucafa `
    * `0748Dhahabi.MukhtasarCuluww `
    * `0748Dhahabi.MukhtasarMinDubaythi `
    * `0748Dhahabi.Muqtana `
    * `0748Dhahabi.RuwatThiqat `
    * `0748Dhahabi.SiyarAclamNubala `
    * `0748Dhahabi.TadhkiraHuffaz `
    * `0748Dhahabi.TarikhIslam `
    * `0748IbnDimyati.Mustafad `
    * `0749IbnWardi.KharidaCajaib `
    * `0749IbnWardi.Tarikh `
    * `0749ShihabDinCumari.MasalikAbsar `
    * `0749Wadiashi.Barnamaj `
    * `0750AbuHafsQazwini.Mashyakha `
    * `0751IbnQayyimJawziyya.IghathaLahfan `
    * `0761IbnKaykaldi.JamicTahsil `
    * `0761IbnKaykaldi.Mukhtalitin `
    * `0762MughaltayIbnQalij.IkmalTahdhib `
    * `0764IbnShakirKutubi.FawatWafayat `
    * `0764Safadi.AcyanCasr `
    * `0764Safadi.NaktHimyan `
    * `0764Safadi.WafiBiWafayat `
    * `0765AbuMahasinHusayni.DhaylTadhkira `
    * `0765AbuMahasinHusayni.IkmalLiRijal `
    * `0767Balawi.TajMafriq `
    * `0768Yafici.MiratJanan `
    * `0771Subki.MucjamShuyukh `
    * `0771Subki.TabaqatShaficiyaKubra `
    * `0774IbnKathir.Bidaya `
    * `0774IbnKathir.TabaqatShaficiyyin `
    * `0774IbnKathir.Takmil `
    * `0774IbnRaficSallami.MashyakhaBayani `
    * `0774IbnRaficSallami.Wafayat `
    * `0775IbnAbiWafa.JawahirMudiya `
    * `0776LisanDinIbnKhatib.Ihata `
    * `0776LisanDinIbnKhatib.KatibaKamina `
    * `0776LisanDinIbnKhatib.KhatraTayf `
    * `0776LisanDinIbnKhatib.MicyarIkhtiyar `
    * `0776LisanDinIbnKhatib.NafadaJirab `
    * `0779IbnBattuta.Rihla `
    * `0782IbnSallar.TabaqatQurra `
    * `0793AbuHasanMalaqi.TarikhQudat `
    * `0795IbnRajabHanbali.DhaylTabaqatHanabila `
    * `0799IbnFarhun.DibajMudhahhab `

* **0900AH [[ [Re]generated on 2016-08-21 (20:32:00) ]]**

    * `0804IbnMulaqqin.TabaqatAwliya `
    * `0806IbnHusaynCiraqi.DhaylMizan `
    * `0807IbnAhmarKhazraji.NafhaNisriniyya `
    * `0808IbnKhaldun.Rihla `
    * `0808IbnKhaldun.Tarikh `
    * `0809IbnQunfudh.Wafayat `
    * `0812CaliKhazraji.CuqudLuluiyya `
    * `0816AbuBakrMaraghi.Mashyakha `
    * `0817IbnYacqubFiruzabadi.BulghaFiTarajim `
    * `0821Qalqashandi.NihayaArab `
    * `0821Qalqashandi.QalaidJuman `
    * `0821Qalqashandi.SubhAcsha `
    * `0821ShihabDinQalqashandi.Maathir `
    * `0825IbnQasimSabti.IkhtisarAkhbar `
    * `0826IbnCiraqi.Mudallisin `
    * `0826IbnCiraqi.TuhfaTahsil `
    * `0832AbuTayyibFasi.DhaylTaqyid `
    * `0832AbuTayyibFasi.ShifaGharam `
    * `0833IbnJazari.GhayaNihaya `
    * `0842IbnNasirDinDimashqi.RaddWafir `
    * `0842IbnNasirDinDimashqi.TawdihMushtabih `
    * `0845Maqrizi.Bayan `
    * `0845Maqrizi.IqazHunafa `
    * `0845Maqrizi.Mawaciz `
    * `0845Maqrizi.MukhtasarKamil `
    * `0845Maqrizi.Suluk `
    * `0851IbnQadiShuhba.TabaqatShaficiya `
    * `0852IbnHajarCasqalani.DurarKamina `
    * `0852IbnHajarCasqalani.FathBari `
    * `0852IbnHajarCasqalani.InbaGhumr `
    * `0852IbnHajarCasqalani.IsabaFiTamyiz `
    * `0852IbnHajarCasqalani.ItharBiMacrifa `
    * `0852IbnHajarCasqalani.LisanMizan `
    * `0852IbnHajarCasqalani.MucjamMufahras `
    * `0852IbnHajarCasqalani.NuzhaAlbab `
    * `0852IbnHajarCasqalani.RafcCisr `
    * `0852IbnHajarCasqalani.TabaqatMudallisin `
    * `0852IbnHajarCasqalani.TabsirMuntabih `
    * `0852IbnHajarCasqalani.TacjilManfaca `
    * `0852IbnHajarCasqalani.TacrifAhlTaqbis `
    * `0852IbnHajarCasqalani.TahdhibTahdhib `
    * `0852IbnHajarCasqalani.TaqribTahdhib `
    * `0854IbnCarabshah.CajaibMaqdur `
    * `0854IbnDiyaMakki.TarikhMakka `
    * `0855Cayni.CiqdJuman `
    * `0855Cayni.CumdaQari `
    * `0855Cayni.MaghaniAkhyar `
    * `0862IbnMuhammadMujari.Barnamaj `
    * `0871IbnFahdMakki.LahzAlhaz `
    * `0874IbnTaghribirdi.HawadithDahriya `
    * `0874IbnTaghribirdi.ManhalSafi `
    * `0874IbnTaghribirdi.MawridLatafa `
    * `0874IbnTaghribirdi.NujumZahira `
    * `0879IbnQutlubugha.TajTarajim `
    * `0879IbnQutlubugha.Thiqat `
    * `0884IbnMuflih.MaqsidArshad `
    * `0884SibtIbnCajami.Ightibat `
    * `0884SibtIbnCajami.KashfHathith `
    * `0884SibtIbnCajami.KunuzDhahab `
    * `0884SibtIbnCajami.TabyinLiAsma `
    * `0900AbuCabdAllahHimyari.RawdMictar `

* **1000AH [[ [Re]generated on 2016-08-21 (20:32:00) ]]**

    * `0902Sakhawi.Buldaniyyat `
    * `0902Sakhawi.DuLamic `
    * `0902Sakhawi.ManhalCadhb `
    * `0902Sakhawi.TuhfaLatifa `
    * `0904Burayhi.TabaqatSulahaYaman `
    * `0905Basrawi.Tarikh `
    * `0909IbnMibradHanbali.BahrDamm `
    * `0909IbnMibradHanbali.MucjamKutub `
    * `0911Samhudi.KhulasaWafaWafa `
    * `0911Samhudi.WafaWafa `
    * `0911Suyuti.AsmaMudallisin `
    * `0911Suyuti.AsmaMukhadramin `
    * `0911Suyuti.BughyaWucat `
    * `0911Suyuti.DhaylTabaqatHuffaz `
    * `0911Suyuti.HusnMuhadara `
    * `0911Suyuti.IscafMubatta `
    * `0911Suyuti.ItmamDiraya `
    * `0911Suyuti.LubbLubab `
    * `0911Suyuti.NazmCiqyan `
    * `0911Suyuti.RihNisrin `
    * `0911Suyuti.Shamarikh `
    * `0911Suyuti.TabaqatHuffaz `
    * `0911Suyuti.TabaqatMufassirin `
    * `0911Suyuti.TarikhKhulafa `
    * `0923IbnCabdAllahKhazraji.KhulasaTahdhib `
    * `0927Culaymi.UnsJalil `
    * `0927Nucaymi.DarisFiMadaris `
    * `0929IbnKayyal.KawakibNayyirat `
    * `0938IbnCaliBalawi.Thabat `
    * `0945ShamsDinDawudi.TabaqatMufassirin `
    * `0953IbnTulun.MufakahaKhillan `
    * `0968Tashkubruizadah.ShaqaiqNucmaniyya `
    * `0973CabdWahhabShacrani.LawaqihAnwar `
    * `0984BardDinGhazzi.MatalicBadriya `

* **1100AH [[ [Re]generated on 2016-08-21 (20:32:00) ]]**

    * `1010TamimiDari.TabaqatSaniya `
    * `1011SahibMacalim.TahrirTawusi `
    * `1016MuhibbDinHamawi.HadiAzcan `
    * `1037CabdQadirCaydarus.TarikhNurSafir `
    * `1041BurhanDinMaliki.BahjaMahafil `
    * `1041Maqarri.AzharRiyad `
    * `1041Maqarri.NafhTib `
    * `1051Cimadi.RawdaRayya `
    * `1061NajmDinGhazzi.KawakibSaira `
    * `1067HajjiKhalifa.KashfZunun `
    * `1069ShihabDinKhafaji.RayhanaAlibba `
    * `1070MuhammadKibrit.RihlaShita `
    * `1078RiyadZadah.AsmaKutub `
    * `1086IbnCajamiMisri.DhaylLubbLubab `
    * `1089IbnCimad.Shadharat `
    * `1100IbnMuhammadAdnahwi.TabaqatMufassirin `
    * `1100MuhammadItlidi.IclamNas `
    * `1100MustafaTafrishi.NaqdRijal `

* **1200AH [[ [Re]generated on 2016-08-21 (20:32:00) ]]**

    * `1101MuhammadCaliArdabili.JamicRuwat `
    * `1111MuhammadAminMuhibbi.KhulasaAthr `
    * `1119IbnMacsum.SulafaCasr `
    * `1120CaliKhanMadani.DarajatRafica `
    * `1126MuhammadHanbali.Mashyakha `
    * `1147CabdAllahSancani.TarikhYaman `
    * `1153IbnKannan.YawmiyyatShamiyya `
    * `1172IbnKhalifaMasakini.Fahrasa `
    * `1174AbuBarakatSuwaydi.NafhaMiskiya `
    * `1175AhmadBudayri.HawadithDimashq `
    * `1175MuhammadKarabisi.IklilManhaj `
    * `1187SulaymanMahasini.HululTacab `
    * `1195CabdRahmanAnsari.Tuhfa `

* **1300AH [[ [Re]generated on 2016-08-21 (20:32:00) ]]**

    * `1206Muradi.SilkDurar `
    * `1212BahrCulum.FawaidRijaliya `
    * `1212BahrCulum.FawaidRijaliya `
    * `1218SalihFulani.QatfThamar `
    * `1232IbnKhatibCumari.RawdaFayha `
    * `1237Jabarti.CajaibAthar `
    * `1246IbnHamadBassam.DurarMafakhir `
    * `1250IbnCaliShaykani.BadrTalic `
    * `1269CabdMalikCasimi.SamtNujum `
    * `1270ShihabDinAlusi.GharaibIghtirab `
    * `1277MuhammadTantawi.NashaNahw `
    * `1285CabdRahmanTamimi.Maqamat `
    * `1286IcjazHusaynKunturi.KashfHajb `

* **1400AH [[ [Re]generated on 2016-08-21 (20:32:00) ]]**

    * `1307Qannawji.AbjadCulum `
    * `1307Qannawji.HittaFiDhikr `
    * `1307Qannawji.LuqtaCajlan `
    * `1313Barujirdi.Taraif `
    * `1313VanDyck.IktifaQunuc `
    * `1315AbuMacaliKalbasi.RasailRijaliyya `
    * `1315Salawi.IstiqsaLiAhkbar `
    * `1318MuhammadSanusi.Musamarat `
    * `1330IbnMusaTabrizi.MiratKutub `
    * `1332ZaynabFawwaz.DurrManthur `
    * `1335CabdRazzaqBaytar.HilyaBashar `
    * `1338MuhammadFaridBey.Bahja `
    * `1338MuhammadFaridBey.Tarikh `
    * `1339IsmacilBashaBaghdadi.HadiyaCarifin `
    * `1339IsmacilBashaBaghdadi.IdahMaknun `
    * `1341CabdHayyTalibi.IclamBiMan `
    * `1345IbnJacfarKattani.RisalaMustatrafa `
    * `1346CbdQadirBadran.Munadama `
    * `1347BashirYamut.Shacirat `
    * `1351IbnHusaynGhazzi.NahrDhahab `
    * `1351YusufIlyanSarkis.MucjamMatbucat `
    * `1354HasanSadr.Takmila `
    * `1354RashidRida.Manar `
    * `1355AhmadTahtawi.TanbihWaIqaz `
    * `1356AbuHudaKalbasi.SamaMaqal `
    * `1359CabbasQummi.Kuna `
    * `1360IbnQasimMakhluf.ShajaraNur `
    * `1364IbnHamdMughiri.MuntakhabQabail `
    * `1368HasanAmin.MustadrakatAcyanShica `
    * `1371MuhsinCamili.AcyanShica `
    * `1372KurdCali.KhitatSham `
    * `1373AbuYaclaZuwawi.TarikhZuwawa `
    * `1376CabdRahmanSacdi.Muallafat `
    * `1381MuhammadSancani.MulhaqBadr `
    * `1383CadbHayyKattani.FihrisFaharis `
    * `1389AghaBuzurgTihrani.DharicaFiTasanifShica `
    * `1389AghaBuzurgTihrani.DhaylKashfZunun `
    * `1389AghaBuzurgTihrani.TASHAnwarSatica `
    * `1389AghaBuzurgTihrani.TASHNawabighRuwat `
    * `1396KhayrDinZirikli.Aclam `

* **1500AH [[ [Re]generated on 2016-08-21 (20:32:00) ]]**

    * `1405CaliShahrudi.Mustadrakat `
    * `1408CumarKahhala.MucjamMuallifin `
    * `1408CumarKahhala.MucjamQabail `
    * `1411SayyidKhui.MucjamRijal `
    * `1411SayyidMarcashi.SharhIhqaq `
    * `1414SalimIbadi.IscafAcyan `
    * `1418SalihAhmadArkani.TihfaMajalis `
    * `1419MahmudTanahi.MujizFiMarajic `
    * `1421HamdJasir.MucjamQabailMCS `
    * `1422MuhammadSalimMuhaysin.MucjamHuffazQuran `
    * `1429BakrIbnCabdAllah.TabaqatNassabin `
    * `1450AkramFaluji.MucjamSaghir `
    * `1450CabdRahmanAlShaykh.Mashahir `
    * `1450MajmacFikrIslami.MawsucaMuallifiImamiya `
    * `1450MuhammadHadiAmini.MucjamMatbicatNajafiya `
    * `1450MuhammadKhayrRamadan.TakmilaMucjamMuallifin `
    * `1450MuhammadSancani.NaylWatar `

# Statistics on the corpus

| **Category** | **Stats** |
|:--- | ------:|
| Number of text files | 1234 |
| Number of books      | 606 |
| Number of authors    | 392 |
| Length in words (all)| 374,476,761 |
| Length in pages (300 w/p)| 1,248,255 |
| Length in words (unique) | 169,904,911 |
| Length in pages (300 w/p)| 566,349 |

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
| 18 | 1396KhayrDinZirikli.Aclam | 1,634,967 | 5,449 |
| 19 | 0821Qalqashandi.SubhAcsha | 1,616,289 | 5,387 |
| 20 | 0310Tabari.Tarikh | 1,613,108 | 5,377 |
| 21 | 0808IbnKhaldun.Tarikh | 1,596,529 | 5,321 |
| 22 | 0360Tabarani.MucjamKabir | 1,590,311 | 5,301 |
| 23 | 0355AbuFarajIsbahani.Aghani | 1,537,021 | 5,123 |
| 24 | 0597IbnJawzi.Muntazam | 1,529,894 | 5,099 |
| 25 | 0852IbnHajarCasqalani.TahdhibTahdhib | 1,415,254 | 4,717 |
| 26 | 0630IbnAthirCizzDin.Kamil | 1,385,342 | 4,617 |
| 27 | 0660IbnCadim.BughyatTalib | 1,373,052 | 4,576 |
| 28 | 0902Sakhawi.DuLamic | 1,335,630 | 4,452 |
| 29 | 0874IbnTaghribirdi.NujumZahira | 1,314,867 | 4,382 |
| 30 | 0626YaqutHamawi.MucjamBuldan | 1,274,659 | 4,248 |
| 31 | 0430AbuNucaymIsbahani.HilyaAwliya | 1,227,955 | 4,093 |
| 32 | 0749ShihabDinCumari.MasalikAbsar | 1,182,722 | 3,942 |
| 33 | 0852IbnHajarCasqalani.IsabaFiTamyiz | 1,153,468 | 3,844 |
| 34 | 1408CumarKahhala.MucjamMuallifin | 1,145,173 | 3,817 |
| 35 | 0852IbnHajarCasqalani.LisanMizan | 1,131,427 | 3,771 |
| 36 | 0279Baladhuri.AnsabAshraf | 1,128,932 | 3,763 |
| 37 | 0277AbuHatimRazi.JarhWaTacdil | 1,121,289 | 3,737 |
| 38 | 1089IbnCimad.Shadharat | 1,097,722 | 3,659 |
| 39 | 1405CaliShahrudi.Mustadrakat | 1,015,230 | 3,384 |
| 40 | 0630IbnAthirCizzDin.UsdGhaba | 963,485 | 3,211 |
| 41 | 0365IbnCadiJurjani.KamilFiDucafa | 962,139 | 3,207 |
| 42 | 0561Samcani.Ansab | 943,976 | 3,146 |
| 43 | 0230IbnSacd.TabaqatKubra | 921,111 | 3,070 |
| 44 | 0475IbnMakula.IkmalFiRafcIrtiyab | 868,430 | 2,894 |
| 45 | 0762MughaltayIbnQalij.IkmalTahdhib | 861,631 | 2,872 |
| 46 | 1041Maqarri.NafhTib | 848,136 | 2,827 |
| 47 | 0845Maqrizi.Suluk | 826,074 | 2,753 |
| 48 | 0626YaqutHamawi.MucjamUdaba | 794,903 | 2,649 |
| 49 | 0256Bukhari.TarikhKabir | 791,001 | 2,636 |
| 50 | 0430AbuNucaymIsbahani.MacrifaSahaba | 785,050 | 2,616 |
| 51 | 0845Maqrizi.Mawaciz | 683,850 | 2,279 |
| 52 | 0421Miskawayh.Tajarib | 679,990 | 2,266 |
| 53 | 0681IbnKhallikan.WafayatAcyan | 677,482 | 2,258 |
| 54 | 0771Subki.TabaqatShaficiyaKubra | 676,731 | 2,255 |
| 55 | 0748Dhahabi.MizanIctidal | 649,090 | 2,163 |
| 56 | 1341CabdHayyTalibi.IclamBiMan | 634,469 | 2,114 |
| 57 | 1111MuhammadAminMuhibbi.KhulasaAthr | 623,533 | 2,078 |
| 58 | 1101MuhammadCaliArdabili.JamicRuwat | 614,459 | 2,048 |
| 59 | 1315AbuMacaliKalbasi.RasailRijaliyya | 613,389 | 2,044 |
| 60 | 0764Safadi.AcyanCasr | 604,057 | 2,013 |
| 61 | 0458Bayhaqi.DalailNubuwwa | 602,949 | 2,009 |
| 62 | 1269CabdMalikCasimi.SamtNujum | 594,712 | 1,982 |
| 63 | 0542IbnBassamShantarini.Dhakhira | 593,086 | 1,976 |
| 64 | 1067HajjiKhalifa.KashfZunun | 580,572 | 1,935 |
| 65 | 0842IbnNasirDinDimashqi.TawdihMushtabih | 550,678 | 1,835 |
| 66 | 1368HasanAmin.MustadrakatAcyanShica | 547,076 | 1,823 |
| 67 | 0354IbnHibban.Thiqat | 535,985 | 1,786 |
| 68 | 1237Jabarti.CajaibAthar | 514,968 | 1,716 |
| 69 | 1100MustafaTafrishi.NaqdRijal | 500,280 | 1,667 |
| 70 | 0879IbnQutlubugha.Thiqat | 473,854 | 1,579 |
| 71 | 1408CumarKahhala.MucjamQabail | 467,206 | 1,557 |
| 72 | 1315Salawi.IstiqsaLiAhkbar | 464,659 | 1,548 |
| 73 | 0776LisanDinIbnKhatib.Ihata | 462,435 | 1,541 |
| 74 | 0255Jahiz.Hayawan | 455,685 | 1,518 |
| 75 | 1351IbnHusaynGhazzi.NahrDhahab | 434,840 | 1,449 |
| 76 | 0855Cayni.MaghaniAkhyar | 426,063 | 1,420 |
| 77 | 0768Yafici.MiratJanan | 424,088 | 1,413 |
| 78 | 0852IbnHajarCasqalani.DurarKamina | 414,702 | 1,382 |
| 79 | 1372KurdCali.KhitatSham | 414,117 | 1,380 |
| 80 | 0463IbnCabdBarr.IsticabFiMacrifaAshab | 413,421 | 1,378 |
| 81 | 1339IsmacilBashaBaghdadi.HadiyaCarifin | 412,771 | 1,375 |
| 82 | 0852IbnHajarCasqalani.InbaGhumr | 410,739 | 1,369 |
| 83 | 1351YusufIlyanSarkis.MucjamMatbucat | 401,654 | 1,338 |
| 84 | 0902Sakhawi.TuhfaLatifa | 394,353 | 1,314 |
| 85 | 0637IbnMustafwi.TarikhIrbil | 385,144 | 1,283 |
| 86 | 0597CimadDinKatib.KharidaQasr | 385,025 | 1,283 |
| 87 | 0346Mascudi.MurujDhahab | 382,786 | 1,275 |
| 88 | 0911Samhudi.WafaWafa | 376,631 | 1,255 |
| 89 | 0874IbnTaghribirdi.ManhalSafi | 368,687 | 1,228 |
| 90 | 0429AbuMansurThacalibi.YatimaDahr | 362,496 | 1,208 |
| 91 | 1206Muradi.SilkDurar | 358,759 | 1,195 |
| 92 | 0623Qazwini.Tadwin | 353,391 | 1,177 |
| 93 | 0676Nawawi.TahdhibAsma | 352,183 | 1,173 |
| 94 | 0262AbuZaydNumayri.TarikhMadina | 351,743 | 1,172 |
| 95 | 1335CabdRazzaqBaytar.HilyaBashar | 346,616 | 1,155 |
| 96 | 0630IbnAthirCizzDin.LubabFiTahdhibAnsab | 341,753 | 1,139 |
| 97 | 0277IbnSyfyanFasawi.MacrifaWaTarikh | 340,450 | 1,134 |
| 98 | 1212BahrCulum.FawaidRijaliya | 338,918 | 1,129 |
| 99 | 0833IbnJazari.GhayaNihaya | 338,862 | 1,129 |
| 100 | 0748Dhahabi.TadhkiraHuffaz | 337,969 | 1,126 |
| 101 | 1313Barujirdi.Taraif | 331,121 | 1,103 |
| 102 | 0597IbnJawzi.SifaSafwa | 330,284 | 1,100 |
| 103 | 0923IbnCabdAllahKhazraji.KhulasaTahdhib | 328,135 | 1,093 |
| 104 | 0642IbnNajjar.DhaylTarikhBaghdad | 326,501 | 1,088 |
| 105 | 0726Yunini.DhaylMiratZaman | 323,810 | 1,079 |
| 106 | 0544CiyadIbnMusaYahsubi.TartibMadarik | 322,807 | 1,076 |
| 107 | 0900AbuCabdAllahHimyari.RawdMictar | 322,499 | 1,074 |
| 108 | 0665AbuShama.Rawdatayn | 317,787 | 1,059 |
| 109 | 0732AbuFida.MukhtasarFiAkhbar | 316,828 | 1,056 |
| 110 | 0322AbuJacfarCuqayli.DucafaKabir | 314,435 | 1,048 |
| 111 | 0911Suyuti.AsmaMudallisin | 306,751 | 1,022 |
| 112 | 0832AbuTayyibFasi.ShifaGharam | 305,946 | 1,019 |
| 113 | 0658IbnAbbar.TakmilaLiSila | 303,591 | 1,011 |
| 114 | 1359CabbasQummi.Kuna | 299,903 | 999 |
| 115 | 1360IbnQasimMakhluf.ShajaraNur | 299,618 | 998 |
| 116 | 0646IbnQifti.InbahRuwat | 295,800 | 986 |
| 117 | 1383CadbHayyKattani.FihrisFaharis | 295,736 | 985 |
| 118 | 0213IbnHisham.SiraNabawiyya | 295,600 | 985 |
| 119 | 0487AbuCubaydBakri.MucjamMaIstacjama | 291,075 | 970 |
| 120 | 1339IsmacilBashaBaghdadi.IdahMaknun | 288,661 | 962 |
| 121 | 0764IbnShakirKutubi.FawatWafayat | 288,315 | 961 |
| 122 | 0855Cayni.CiqdJuman | 274,376 | 914 |
| 123 | 1307Qannawji.AbjadCulum | 274,005 | 913 |
| 124 | 0732IbnYacqubJanadi.SulukFiTabaqat | 272,623 | 908 |
| 125 | 0748Dhahabi.CibarFiKhabar | 270,945 | 903 |
| 126 | 0272Fakihi.AkhbarMakka | 269,999 | 899 |
| 127 | 0779IbnBattuta.Rihla | 267,265 | 890 |
| 128 | 1318MuhammadSanusi.Musamarat | 266,110 | 887 |
| 129 | 0287Dahhak.AhadWaMathani | 265,863 | 886 |
| 130 | 0207Waqidi.Maghazi | 264,920 | 883 |
| 131 | 0430AbuNucaymIsbahani.TarikhIsbahan | 260,298 | 867 |
| 132 | 0774IbnKathir.Takmil | 255,916 | 853 |
| 133 | 0668IbnAbiUsaybica.CuyunAnba | 253,484 | 844 |
| 134 | 0749IbnWardi.Tarikh | 252,903 | 843 |
| 135 | 1450AkramFaluji.MucjamSaghir | 251,265 | 837 |
| 136 | 0354IbnHibban.Majruhin | 250,389 | 834 |
| 137 | 1450MajmacFikrIslami.MawsucaMuallifiImamiya | 249,154 | 830 |
| 138 | 0207Waqidi.FutuhSham | 248,628 | 828 |
| 139 | 1061NajmDinGhazzi.KawakibSaira | 242,384 | 807 |
| 140 | 1332ZaynabFawwaz.DurrManthur | 238,367 | 794 |
| 141 | 0306IbnHayyanDabbi.AkhbarQudat | 237,235 | 790 |
| 142 | 0748Dhahabi.Kashif | 235,822 | 786 |
| 143 | 0973CabdWahhabShacrani.LawaqihAnwar | 232,710 | 775 |
| 144 | 0629IbnNuqta.TakmilaIkmal | 231,460 | 771 |
| 145 | 0775IbnAbiWafa.JawahirMudiya | 230,720 | 769 |
| 146 | 0460ShaykhTusi.IkhtiyarMacrifaRijal | 227,637 | 758 |
| 147 | 1356AbuHudaKalbasi.SamaMaqal | 226,396 | 754 |
| 148 | 0927Nucaymi.DarisFiMadaris | 224,568 | 748 |
| 149 | 0739SafiDinHanbali.Marasid | 220,179 | 733 |
| 150 | 0927Culaymi.UnsJalil | 218,375 | 727 |
| 151 | 0317AbuQasimBaghawi.MucjamSahaba | 218,356 | 727 |
| 152 | 0911Suyuti.HusnMuhadara | 218,158 | 727 |
| 153 | 0463KhatibBaghdadi.MuttafiqWaMuftariq | 218,096 | 726 |
| 154 | 0852IbnHajarCasqalani.TaqribTahdhib | 217,589 | 725 |
| 155 | 0241IbnHanbal.CilalWaMacrifa | 214,328 | 714 |
| 156 | 0795IbnRajabHanbali.DhaylTabaqatHanabila | 213,679 | 712 |
| 157 | 0852IbnHajarCasqalani.TabsirMuntabih | 209,171 | 697 |
| 158 | 0560SharifIdrisi.NuzhaMushtaq | 207,532 | 691 |
| 159 | 0385Daruqutni.MutalifWaMukhtalif | 207,158 | 690 |
| 160 | 0694MuhibbDinTabari.RiyadNadira | 205,681 | 685 |
| 161 | 1175MuhammadKarabisi.IklilManhaj | 203,395 | 677 |
| 162 | 0911Suyuti.BughyaWucat | 197,961 | 659 |
| 163 | 0400IbnTahirMaqdisi.BadWaTarikh | 197,348 | 657 |
| 164 | 0571IbnCasakir.MucjamShuyukh | 195,776 | 652 |
| 165 | 0645TilimsaniBurri.Jawhara | 194,697 | 648 |
| 166 | 0292Yacqubi.TarikhYacqubi | 193,018 | 643 |
| 167 | 1250IbnCaliShaykani.BadrTalic | 192,663 | 642 |
| 168 | 0347IbnYunusSadafi.Tarikh | 190,889 | 636 |
| 169 | 1450MuhammadKhayrRamadan.TakmilaMucjamMuallifin | 189,829 | 632 |
| 170 | 0561Samcani.Muntakhab | 188,251 | 627 |
| 171 | 0463KhatibBaghdadi.TalkhisMutashabih | 187,352 | 624 |
| 172 | 0310IbnAhmadDulabi.KunaWaAsma | 186,967 | 623 |
| 173 | 1041Maqarri.AzharRiyad | 185,770 | 619 |
| 174 | 0845Maqrizi.IqazHunafa | 185,230 | 617 |
| 175 | 0852IbnHajarCasqalani.MucjamMufahras | 183,759 | 612 |
| 176 | 0487AbuCubaydBakri.MasalikWaMamalik | 181,326 | 604 |
| 177 | 0774IbnKathir.TabaqatShaficiyyin | 180,884 | 602 |
| 178 | 0474IbnKhalafBaji.TacdilWaTakhrij | 180,381 | 601 |
| 179 | 0832AbuTayyibFasi.DhaylTaqyid | 177,958 | 593 |
| 180 | 1120CaliKhanMadani.DarajatRafica | 174,564 | 581 |
| 181 | 0255Jahiz.Rasail | 172,282 | 574 |
| 182 | 0521IbnAbiYacla.TabaqatHanabila | 171,812 | 572 |
| 183 | 0508FattalNaysaburi.RawdaWacizin | 170,713 | 569 |
| 184 | 0255Jahiz.BayanWaTabyin | 170,368 | 567 |
| 185 | 0884SibtIbnCajami.KunuzDhahab | 170,224 | 567 |
| 186 | 1422MuhammadSalimMuhaysin.MucjamHuffazQuran | 169,932 | 566 |
| 187 | 0911Samhudi.KhulasaWafaWafa | 168,018 | 560 |
| 188 | 0812CaliKhazraji.CuqudLuluiyya | 167,694 | 558 |
| 189 | 0615MuwaffaqDinShafici.MurshidZuwwar | 167,271 | 557 |
| 190 | 1119IbnMacsum.SulafaCasr | 165,783 | 552 |
| 191 | 0421IbnMuhammadMarzuqi.AzminaWaAmkina | 165,458 | 551 |
| 192 | 0511SalmaSahari.Ansab | 162,120 | 540 |
| 193 | 1010TamimiDari.TabaqatSaniya | 161,681 | 538 |
| 194 | 0597IbnJawzi.TalqihFuhum | 160,269 | 534 |
| 195 | 1011SahibMacalim.TahrirTawusi | 157,260 | 524 |
| 196 | 1338MuhammadFaridBey.Tarikh | 155,747 | 519 |
| 197 | 0279IbnAbiKhaythama.TarikhKabir | 155,627 | 518 |
| 198 | 0535QawwamSunna.SiyarSalaf | 154,547 | 515 |
| 199 | 0695IbnCidhariMarrakushi.BayanMaghrib | 153,641 | 512 |
| 200 | 0748Dhahabi.MucjamShuyukh | 152,971 | 509 |
| 201 | 0365IbnFaqihHamadhani.Buldan | 147,644 | 492 |
| 202 | 0682ZakariyaQazwini.AtharBilad | 146,837 | 489 |
| 203 | 0696IbnZahiri.Mashyakha | 146,557 | 488 |
| 204 | 0968Tashkubruizadah.ShaqaiqNucmaniyya | 145,615 | 485 |
| 205 | 0845Maqrizi.MukhtasarKamil | 142,932 | 476 |
| 206 | 0821ShihabDinQalqashandi.Maathir | 142,487 | 474 |
| 207 | 0385IbnNadim.Fihrist | 141,796 | 472 |
| 208 | 0945ShamsDinDawudi.TabaqatMufassirin | 139,971 | 466 |
| 209 | 1376CabdRahmanSacdi.Muallafat | 139,967 | 466 |
| 210 | 0351IbnQanic.MucjamSahaba | 139,882 | 466 |
| 211 | 0578IbnBashkuwal.Sila | 139,365 | 464 |
| 212 | 0709CaliCalawi.Majdi | 138,926 | 463 |
| 213 | 0249Azraqi.AkhbarMakka | 136,671 | 455 |
| 214 | 0576IbnMuhammadSilafi.MashyakhaBaghdadiyya | 135,363 | 451 |
| 215 | 0245MuhammadIbnHabib.MunammaqFiAkhbarQuraysh | 135,021 | 450 |
| 216 | 0703MuhammadMarrakushi.DhaylWaTakmila | 133,973 | 446 |
| 217 | 0911Suyuti.TarikhKhulafa | 133,130 | 443 |
| 218 | 0241IbnHanbal.FadailSahaba | 132,367 | 441 |
| 219 | 0369AbuShaykhIsbahani.TabaqatMuhaddithin | 132,063 | 440 |
| 220 | 0456IbnHazm.JamharaAnsab | 130,859 | 436 |
| 221 | 0852IbnHajarCasqalani.TacjilManfaca | 127,930 | 426 |
| 222 | 0953IbnTulun.MufakahaKhillan | 127,338 | 424 |
| 223 | 1286IcjazHusaynKunturi.KashfHajb | 126,032 | 420 |
| 224 | 0395IbnMandahMuhammad.FathBab | 124,908 | 416 |
| 225 | 0279Baladhuri.FutuhBuldan | 124,892 | 416 |
| 226 | 0428IbnManjuwayhIsbahani.RijalSahihMuslim | 124,175 | 413 |
| 227 | 0367IbnHawqal.SuraArd | 123,793 | 412 |
| 228 | 0884IbnMuflih.MaqsidArshad | 123,777 | 412 |
| 229 | 0852IbnHajarCasqalani.RafcCisr | 123,094 | 410 |
| 230 | 0276IbnQutaybaDinawari.Macarif | 121,880 | 406 |
| 231 | 0565IbnZaydBayhaqi.TarikhBayhaq | 121,037 | 403 |
| 232 | 0555IbnQalanisi.Tarikh | 120,986 | 403 |
| 233 | 0449AbuCalaMacarri.Diwan | 120,379 | 401 |
| 234 | 0429Thacalibi.ThimarQulub | 119,721 | 399 |
| 235 | 0228IbnHammadKhuzaci.Fitan | 119,494 | 398 |
| 236 | 0851IbnQadiShuhba.TabaqatShaficiya | 119,436 | 398 |
| 237 | 0748Dhahabi.MughniFiDucafa | 119,182 | 397 |
| 238 | 0403IbnFaradi.TarikhCulamaAndalus | 118,911 | 396 |
| 239 | 0575IbnKhayrIshbili.Fahrasa | 117,769 | 392 |
| 240 | 0771Subki.MucjamShuyukh | 117,371 | 391 |
| 241 | 0599IbnYahyaDabbi.BughyaMultamis | 116,987 | 389 |
| 242 | 0684IbnShaddad.AclaqKhatira | 116,670 | 388 |
| 243 | 0257IbnCabdHakam.FutuhMisr | 116,282 | 387 |
| 244 | 0427HamzaJurjani.TarikhJurjan | 114,881 | 382 |
| 245 | 0799IbnFarhun.DibajMudhahhab | 114,355 | 381 |
| 246 | 1037CabdQadirCaydarus.TarikhNurSafir | 113,966 | 379 |
| 247 | 1270ShihabDinAlusi.GharaibIghtirab | 113,165 | 377 |
| 248 | 0233YahyaIbnMacin.TarikhIbnMacin | 112,871 | 376 |
| 249 | 0629IbnNuqta.TaqyidLiMacrifa | 112,296 | 374 |
| 250 | 1313VanDyck.IktifaQunuc | 112,098 | 373 |
| 251 | 0213IbnHisham.Tijan | 111,971 | 373 |
| 252 | 0440AbuRayhanBiruni.TahqiqMaLilHind | 111,411 | 371 |
| 253 | 1346CbdQadirBadran.Munadama | 110,741 | 369 |
| 254 | 0660IbnCadim.ZubdaHalab | 110,479 | 368 |
| 255 | 0578IbnBashkuwal.GhawamidAsma | 110,027 | 366 |
| 256 | 0354IbnHibban.Sira | 109,974 | 366 |
| 257 | 0561Samcani.Tahbir | 109,525 | 365 |
| 258 | 0685IbnSacidMaghribi.Mughrib | 109,402 | 364 |
| 259 | 0685IbnCibri.TarikhMukhtasarDuwal | 109,030 | 363 |
| 260 | 0240KhalifaIbnKhayyat.Tarikh | 108,050 | 360 |
| 261 | 0726CallamaHilli.KhulasaAqwal | 106,878 | 356 |
| 262 | 0300MuallifMajhul.AkhbarDawlaCabbasiya | 106,130 | 353 |
| 263 | 0748Dhahabi.DiwanDucafa | 105,284 | 350 |
| 264 | 0748Dhahabi.MukhtasarMinDubaythi | 103,004 | 343 |
| 265 | 0240KhalifaIbnKhayyat.Tabaqat | 102,233 | 340 |
| 266 | 0597IbnJawzi.DucafaWaMatrukin | 100,991 | 336 |
| 267 | 0658IbnAbbar.HullaSiyara | 98,508 | 328 |
| 268 | 0390Muqaddasi.AhsanTaqasim | 98,198 | 327 |
| 269 | 0507AbuBakrShashi.HilyaCulama | 98,130 | 327 |
| 270 | 0282AbuHanifaDinawari.AkhbarTiwal | 97,880 | 326 |
| 271 | 0576IbnMuhammadSilafi.MucjamSafar | 97,869 | 326 |
| 272 | 0748Dhahabi.MacrifaQurraKibar | 97,714 | 325 |
| 273 | 0821Qalqashandi.NihayaArab | 97,039 | 323 |
| 274 | 0646IbnQifti.IkhbarCulama | 96,909 | 323 |
| 275 | 0641Sarifini.Muntakhab | 96,486 | 321 |
| 276 | 0575IbnBabawayh.Fihrist | 96,438 | 321 |
| 277 | 1041BurhanDinMaliki.BahjaMahafil | 96,298 | 320 |
| 278 | 0854IbnDiyaMakki.TarikhMakka | 96,272 | 320 |
| 279 | 0448HilalSabi.TuhfaUmara | 95,725 | 319 |
| 280 | 0600AbuBaqaHilli.ManaqibMazidiya | 95,644 | 318 |
| 281 | 0580IbnCimrani.InbaFiTarikhKhulafa | 92,814 | 309 |
| 282 | 0398AbuNasrKalabadhi.HidayaWaIrshad | 90,817 | 302 |
| 283 | 0395IbnMandahMuhammad.MacrifaSahaba | 90,565 | 301 |
| 284 | 0741KhatibTabrizi.Ikmal | 90,307 | 301 |
| 285 | 0236AbuCabdAllahZubayri.NasabQuraysh | 90,262 | 300 |
| 286 | 0450Najashi.Rijal | 90,256 | 300 |
| 287 | 0204IbnKalbi.NasabMacad | 88,977 | 296 |
| 288 | 1330IbnMusaTabrizi.MiratKutub | 88,818 | 296 |
| 289 | 0460ShaykhTusi.Rijal | 88,503 | 295 |
| 290 | 1354HasanSadr.Takmila | 88,094 | 293 |
| 291 | 0346Mascudi.TanbihWaIshraf | 87,579 | 291 |
| 292 | 0355MuhammadKindi.WulatMisr | 86,621 | 288 |
| 293 | 0256Bukhari.TarikhSaghir | 86,362 | 287 |
| 294 | 0384IbnCimranMarzubani.MucjamShucara | 86,047 | 286 |
| 295 | 0256ZubayrIbnBakkar.AkhbarMuwaffaqiyat | 85,750 | 285 |
| 296 | 0255Jahiz.Cuthmaniya | 85,453 | 284 |
| 297 | 0488IbnFutuhHumaydi.JadhwaMuqtabis | 85,167 | 283 |
| 298 | 0597CimadDinKatib.BarqShami | 84,900 | 283 |
| 299 | 0528FathIbnKhaqan.QalaidCiqyan | 84,437 | 281 |
| 300 | 1389AghaBuzurgTihrani.TASHNawabighRuwat | 84,082 | 280 |
| 301 | 0446AbuYaclaKhalili.IrshadFiMacrifaCulama | 82,456 | 274 |
| 302 | 0694MuhibbDinTabari.Dhakhair | 81,328 | 271 |
| 303 | 0597IbnJawzi.MuthirGharam | 81,078 | 270 |
| 304 | 1100MuhammadItlidi.IclamNas | 80,344 | 267 |
| 305 | 0292Bahshal.TarikhWasit | 80,039 | 266 |
| 306 | 1153IbnKannan.YawmiyyatShamiyya | 79,567 | 265 |
| 307 | 0748Dhahabi.Muqtana | 77,096 | 256 |
| 308 | 0261AbuHasanCijli.MacrifaThiqat | 76,492 | 254 |
| 309 | 0658IbnAbbar.MucjamAshab | 76,471 | 254 |
| 310 | 0761IbnKaykaldi.JamicTahsil | 76,460 | 254 |
| 311 | 0565IbnZaydBayhaqi.LubabAnsab | 76,424 | 254 |
| 312 | 0749IbnWardi.KharidaCajaib | 75,947 | 253 |
| 313 | 0281AbuZurcaDimashqi.Tarikh | 75,765 | 252 |
| 314 | 0346Istakhri.MasalikWaMamalik | 75,599 | 251 |
| 315 | 0733IbnJamaca.Mashyakha | 75,126 | 250 |
| 316 | 0614IbnJubayr.Rihla | 74,329 | 247 |
| 317 | 0764Safadi.NaktHimyan | 74,306 | 247 |
| 318 | 0904Burayhi.TabaqatSulahaYaman | 74,213 | 247 |
| 319 | 0767Balawi.TajMafriq | 73,852 | 246 |
| 320 | 0911Suyuti.TabaqatHuffaz | 73,614 | 245 |
| 321 | 0535QawwamSunna.DalailNubuwwa | 72,728 | 242 |
| 322 | 0854IbnCarabshah.CajaibMaqdur | 72,705 | 242 |
| 323 | 1174AbuBarakatSuwaydi.NafhaMiskiya | 71,961 | 239 |
| 324 | 0723IbnFuwati.Hawadith | 71,739 | 239 |
| 325 | 0730MuhammadTujibi.Barnamaj | 71,375 | 237 |
| 326 | 0748Dhahabi.MukhtasarCuluww | 71,152 | 237 |
| 327 | 0334IbnHaikHamdani.SifaJaziraCarab | 70,929 | 236 |
| 328 | 0647CabdWahidMarrakushi.Mucjib | 70,871 | 236 |
| 329 | 0255Jahiz.MahasinWaAddad | 70,477 | 234 |
| 330 | 0333AbuCarabTamimi.Mihan | 70,365 | 234 |
| 331 | 0261Muslim.KunaWaAsma | 70,202 | 234 |
| 332 | 0296IbnMuctazz.TabaqatShucara | 69,665 | 232 |
| 333 | 0276IbnQutaybaDinawari.AdabKatib | 69,368 | 231 |
| 334 | 1147CabdAllahSancani.TarikhYaman | 69,040 | 230 |
| 335 | 0673AbuMahasinYaghmuri.NurQabas | 68,955 | 229 |
| 336 | 0750AbuHafsQazwini.Mashyakha | 68,872 | 229 |
| 337 | 0412Sulami.TabaqatSufiya | 68,774 | 229 |
| 338 | 1195CabdRahmanAnsari.Tuhfa | 68,557 | 228 |
| 339 | 0740IbnDawudHilli.Rijal | 68,088 | 226 |
| 340 | 1307Qannawji.HittaFiDhikr | 67,880 | 226 |
| 341 | 1421HamdJasir.MucjamQabailMCS | 67,689 | 225 |
| 342 | 0690IbnMujawirDimashqi.TarikhMustabsir | 65,633 | 218 |
| 343 | 0639AbuBakrMalaqi.MatlacAnwar | 65,139 | 217 |
| 344 | 0584IbnMusaHazimi.Amakin | 64,697 | 215 |
| 345 | 0816AbuBakrMaraghi.Mashyakha | 64,167 | 213 |
| 346 | 0346Mascudi.AkhbarZaman | 63,951 | 213 |
| 347 | 1232IbnKhatibCumari.RawdaFayha | 63,383 | 211 |
| 348 | 0643IbnSalahShahrazuri.TabaqatFuqaha | 63,126 | 210 |
| 349 | 0826IbnCiraqi.TuhfaTahsil | 62,996 | 209 |
| 350 | 1450CabdRahmanAlShaykh.Mashahir | 62,418 | 208 |
| 351 | 0871IbnFahdMakki.LahzAlhaz | 62,047 | 206 |
| 352 | 0793AbuHasanMalaqi.TarikhQudat | 62,043 | 206 |
| 353 | 0938IbnCaliBalawi.Thabat | 61,539 | 205 |
| 354 | 0774IbnRaficSallami.Wafayat | 61,135 | 203 |
| 355 | 0600KatibMarrakushi.Istibsar | 60,550 | 201 |
| 356 | 0521MuhammadHamadhani.TakmilaTarikhTabari | 60,016 | 200 |
| 357 | 1307Qannawji.LuqtaCajlan | 59,600 | 198 |
| 358 | 0874IbnTaghribirdi.MawridLatafa | 59,510 | 198 |
| 359 | 1338MuhammadFaridBey.Bahja | 59,305 | 197 |
| 360 | 0714AhmadGhibrini.CunwanDiraya | 58,461 | 194 |
| 361 | 0395AbuHilalCaskari.Talkhis | 57,835 | 192 |
| 362 | 1069ShihabDinKhafaji.RayhanaAlibba | 57,614 | 192 |
| 363 | 0911Suyuti.LubbLubab | 57,394 | 191 |
| 364 | 0646IbnQifti.Muhammadun | 57,364 | 191 |
| 365 | 0255Jahiz.BursanWaCurjan | 57,316 | 191 |
| 366 | 0256ZubayrIbnBakkar.JamharaNasabQuraysh | 56,650 | 188 |
| 367 | 0310Tabari.MuntakhabMinDhayl | 56,329 | 187 |
| 368 | 0808IbnKhaldun.Rihla | 55,833 | 186 |
| 369 | 0909IbnMibradHanbali.BahrDamm | 55,202 | 184 |
| 370 | 0255Jahiz.Bukhala | 55,171 | 183 |
| 371 | 0475IbnMakula.TahdhibMustamirr | 55,129 | 183 |
| 372 | 0231IbnSallamJumahi.TabaqatFuhulShucara | 54,921 | 183 |
| 373 | 0776LisanDinIbnKhatib.KatibaKamina | 54,854 | 182 |
| 374 | 0804IbnMulaqqin.TabaqatAwliya | 54,595 | 181 |
| 375 | 0765AbuMahasinHusayni.IkmalLiRijal | 54,306 | 181 |
| 376 | 0911Suyuti.ItmamDiraya | 54,179 | 180 |
| 377 | 0280IbnTayfur.BallaghatNisa | 53,601 | 178 |
| 378 | 1277MuhammadTantawi.NashaNahw | 52,381 | 174 |
| 379 | 0776LisanDinIbnKhatib.NafadaJirab | 52,268 | 174 |
| 380 | 0884SibtIbnCajami.KashfHathith | 52,220 | 174 |
| 381 | 0748Dhahabi.Culuww | 51,813 | 172 |
| 382 | 0370IbnBishrAmidi.MutalifWaMukhtalif | 51,486 | 171 |
| 383 | 1381MuhammadSancani.MulhaqBadr | 51,442 | 171 |
| 384 | 0782IbnSallar.TabaqatQurra | 51,171 | 170 |
| 385 | 0296IbnMuctazz.Diwan | 51,131 | 170 |
| 386 | 0606IbnMamati.LataifDhakhira | 51,074 | 170 |
| 387 | 1070MuhammadKibrit.RihlaShita | 50,647 | 168 |
| 388 | 0550AbuHajjajAshcari.TacrifBiAnsab | 50,496 | 168 |
| 389 | 0748IbnDimyati.Mustafad | 50,153 | 167 |
| 390 | 0806IbnHusaynCiraqi.DhaylMizan | 49,484 | 164 |
| 391 | 0280IbnTayfur.Baghdad | 48,570 | 161 |
| 392 | 0611SharafDinMuqaddasi.Arbacin | 47,514 | 158 |
| 393 | 0569CumaraHakami.NukatCasriyya | 47,005 | 156 |
| 394 | 0984BardDinGhazzi.MatalicBadriya | 46,951 | 156 |
| 395 | 0354IbnHibban.MashahirCulamaAmsar | 45,365 | 151 |
| 396 | 0617MansurIbnShahanshah.MidmarHaqaiq | 45,270 | 150 |
| 397 | 0233YahyaIbnMacin.MacrifaRijal | 45,156 | 150 |
| 398 | 0749Wadiashi.Barnamaj | 44,950 | 149 |
| 399 | 1450MuhammadHadiAmini.MucjamMatbicatNajafiya | 44,242 | 147 |
| 400 | 0748Dhahabi.MucjamMuhaddithin | 44,241 | 147 |
| 401 | 0577IbnAnbari.NuzhaAlibba | 43,683 | 145 |
| 402 | 0852IbnHajarCasqalani.NuzhaAlbab | 43,292 | 144 |
| 403 | 0584IbnMunqidhShayzari.Ictibar | 42,824 | 142 |
| 404 | 0507IbnQaysarani.AnsabMuttafiqa | 42,469 | 141 |
| 405 | 1364IbnHamdMughiri.MuntakhabQabail | 42,407 | 141 |
| 406 | 0680IbnSabuni.TakmilaIkmalIkmal | 42,252 | 140 |
| 407 | 0300IbnKhurdadhbih.MasalikWaMamalik | 41,035 | 136 |
| 408 | 0436HusaynSaymari.AkhbarAbiHanifa | 41,024 | 136 |
| 409 | 0337IbnIshaqZajjaji.Akhbar | 40,895 | 136 |
| 410 | 1100IbnMuhammadAdnahwi.TabaqatMufassirin | 40,783 | 135 |
| 411 | 0476AbuIshaqShirazi.TabaqatFuqaha | 40,668 | 135 |
| 412 | 0320CaribQurtubi.SilaTarikhTabari | 39,699 | 132 |
| 413 | 0905Basrawi.Tarikh | 39,659 | 132 |
| 414 | 1345IbnJacfarKattani.RisalaMustatrafa | 39,163 | 130 |
| 415 | 0388Shabushti.Diyarat | 38,993 | 129 |
| 416 | 0817IbnYacqubFiruzabadi.BulghaFiTarajim | 38,540 | 128 |
| 417 | 0902Sakhawi.Buldaniyyat | 37,943 | 126 |
| 418 | 0207Waqidi.Ridda | 37,811 | 126 |
| 419 | 1347BashirYamut.Shacirat | 37,705 | 125 |
| 420 | 1389AghaBuzurgTihrani.TASHAnwarSatica | 37,497 | 124 |
| 421 | 0748Dhahabi.DhaylCibar | 37,477 | 124 |
| 422 | 0685IbnSacidMaghribi.Jughrafiya | 35,291 | 117 |
| 423 | 0573NashwanHimyari.KhulasaSiyar | 35,216 | 117 |
| 424 | 0379MuhammadRabci.TarikhMawlidCulama | 35,176 | 117 |
| 425 | 0657IbnIbrahimIrbili.MudhakaraFiAlqab | 35,060 | 116 |
| 426 | 1373AbuYaclaZuwawi.TarikhZuwawa | 34,902 | 116 |
| 427 | 1078RiyadZadah.AsmaKutub | 33,076 | 110 |
| 428 | 1175AhmadBudayri.HawadithDimashq | 32,858 | 109 |
| 429 | 1355AhmadTahtawi.TanbihWaIqaz | 32,723 | 109 |
| 430 | 0405HakimNaysaburi.TalkhisTarikhNaysabur | 32,674 | 108 |
| 431 | 0874IbnTaghribirdi.HawadithDahriya | 32,505 | 108 |
| 432 | 0626YaqutHamawi.Khazal | 32,504 | 108 |
| 433 | 0292Yacqubi.Buldan | 32,476 | 108 |
| 434 | 0385IbnShahin.TarikhAsmaThiqat | 31,929 | 106 |
| 435 | 0845Maqrizi.Bayan | 31,900 | 106 |
| 436 | 0911Suyuti.NazmCiqyan | 31,489 | 104 |
| 437 | 0371AhmadJurjani.Mucjam | 31,101 | 103 |
| 438 | 0821Qalqashandi.QalaidJuman | 30,592 | 101 |
| 439 | 1389AghaBuzurgTihrani.DhaylKashfZunun | 30,484 | 101 |
| 440 | 0544CiyadIbnMusaYahsubi.Ghunya | 29,789 | 99 |
| 441 | 0463KhatibBaghdadi.GhunyaMultamis | 29,514 | 98 |
| 442 | 0611CaliHarawi.Isharat | 29,278 | 97 |
| 443 | 1354RashidRida.Manar | 29,042 | 96 |
| 444 | 0658IbnAbbar.TuhfaQadim | 28,899 | 96 |
| 445 | 0902Sakhawi.ManhalCadhb | 28,425 | 94 |
| 446 | 0333AbuCarabTamimi.TabaqatCulama | 28,320 | 94 |
| 447 | 0264AbyZurca.Ducafa | 28,257 | 94 |
| 448 | 0334IbnHaikHamdani.Iklil | 27,740 | 92 |
| 449 | 0650IbnNazifHamawi.TarikhMansuri | 27,313 | 91 |
| 450 | 0879IbnQutlubugha.TajTarajim | 26,463 | 88 |
| 451 | 0842IbnNasirDinDimashqi.RaddWafir | 26,176 | 87 |
| 452 | 0402MuhammadSaydawi.MucjamShuyukh | 26,156 | 87 |
| 453 | 0310IbnAhmadDulabi.Dhariyya | 26,063 | 86 |
| 454 | 1414SalimIbadi.IscafAcyan | 25,921 | 86 |
| 455 | 0632IsmacilMarwazi.FakhriFiAnsab | 25,627 | 85 |
| 456 | 0255Jahiz.TajFiAkhlaq | 25,314 | 84 |
| 457 | 0748Dhahabi.MucinFiTabaqatMuhaddithin | 23,934 | 79 |
| 458 | 0929IbnKayyal.KawakibNayyirat | 23,699 | 78 |
| 459 | 0584IbnMusaHazimi.CujalaMubtadi | 23,180 | 77 |
| 460 | 1429BakrIbnCabdAllah.TabaqatNassabin | 23,042 | 76 |
| 461 | 1086IbnCajamiMisri.DhaylLubbLubab | 22,972 | 76 |
| 462 | 0576IbnMuhammadSilafi.Mashyakha | 22,872 | 76 |
| 463 | 0368AbuGhalibZurari.Risala | 22,769 | 75 |
| 464 | 0418WazirMaghribi.AdabKhawas | 22,658 | 75 |
| 465 | 0418WazirMaghribi.Inas | 22,614 | 75 |
| 466 | 0776LisanDinIbnKhatib.MicyarIkhtiyar | 22,471 | 74 |
| 467 | 0209MacmarIbnMuthanna.Khayl | 22,392 | 74 |
| 468 | 0911Suyuti.DhaylTabaqatHuffaz | 22,369 | 74 |
| 469 | 0640AbuHafsDunaysiri.TarikhDunaysir | 22,117 | 73 |
| 470 | 0303Nasai.FadailSahaba | 21,802 | 72 |
| 471 | 0385IbnShahin.TarikhAsmaDucafa | 21,637 | 72 |
| 472 | 0732AbuFida.Yawaqit | 21,381 | 71 |
| 473 | 0330Sirafi.Rihla | 21,280 | 70 |
| 474 | 0204IbnKalbi.JamharaAnsab | 21,042 | 70 |
| 475 | 0565IbnZaydBayhaqi.TatimmaSiwanHikma | 20,359 | 67 |
| 476 | 0515IbnQattac.DurraKhatira | 20,292 | 67 |
| 477 | 0385Daruqutni.DhikrAsmaTabicin | 19,767 | 65 |
| 478 | 0748Dhahabi.DhikrAsmaManTakallama | 19,394 | 64 |
| 479 | 0380Muhallabi.MasalikWaMamalik | 18,868 | 62 |
| 480 | 0629IbnNuqta.IfadaWaIctibar | 18,784 | 62 |
| 481 | 0385Daruqutni.SualatBarqani | 18,719 | 62 |
| 482 | 0466CabdAzizKattani.DhaylTarikhMawlidCulama | 18,658 | 62 |
| 483 | 0463IbnCabdBarr.InbahCalaQabail | 18,464 | 61 |
| 484 | 0309IbnFadlan.Rihla | 18,416 | 61 |
| 485 | 0255Jahiz.Bighal | 18,305 | 61 |
| 486 | 0677SahibTaji.HalbaFiAsmaKhayl | 18,268 | 60 |
| 487 | 0296MuhammadIbnJarrah.ManIsmuhCamr | 18,234 | 60 |
| 488 | 0334IbnSacidQushayri.TarikhRaqqa | 17,955 | 59 |
| 489 | 1016MuhibbDinHamawi.HadiAzcan | 17,554 | 58 |
| 490 | 0597IbnJawzi.Mashyakha | 17,396 | 57 |
| 491 | 0469IbnHayyanQurtubi.Muqtabas | 17,127 | 57 |
| 492 | 0355AbuFarajIsbahani.Diyarat | 17,102 | 57 |
| 493 | 1218SalihFulani.QatfThamar | 16,905 | 56 |
| 494 | 0691IbnYusufLabli.Fihrist | 16,803 | 56 |
| 495 | 0911Suyuti.IscafMubatta | 16,433 | 54 |
| 496 | 0498AbuCaliJayyani.TaqyidMuhmal | 16,017 | 53 |
| 497 | 0405HakimNaysaburi.TasmiyaManAkhrajahum | 15,868 | 52 |
| 498 | 0456IbnHazm.FadailAndalus | 15,744 | 52 |
| 499 | 0685IbnSacidMaghribi.GhusunYanica | 15,713 | 52 |
| 500 | 0538MahmudZamakhshari.JibalWaAmkina | 15,676 | 52 |
| 501 | 0765AbuMahasinHusayni.DhaylTadhkira | 15,407 | 51 |
| 502 | 1126MuhammadHanbali.Mashyakha | 14,775 | 49 |
| 503 | 0659SainDinNaccal.Mashyakha | 14,631 | 48 |
| 504 | 0909IbnMibradHanbali.MucjamKutub | 14,490 | 48 |
| 505 | 1418SalihAhmadArkani.TihfaMajalis | 14,467 | 48 |
| 506 | 0430AbuNucaymIsbahani.Ducafa | 14,296 | 47 |
| 507 | 0456IbnHazm.NaqtCarus | 14,078 | 46 |
| 508 | 0360Khawlani.TarikhDaraya | 13,813 | 46 |
| 509 | 0261Muslim.Munfaridat | 13,798 | 45 |
| 510 | 0211AbuCatahiya.Diwan | 13,740 | 45 |
| 511 | 0541IbnCatiyyaMuharibi.Fahrasa | 13,427 | 44 |
| 512 | 0256Bukhari.Ducafa | 13,146 | 43 |
| 513 | 0748Dhahabi.DhaylDiwanDucafa | 12,664 | 42 |
| 514 | 1419MahmudTanahi.MujizFiMarajic | 12,525 | 41 |
| 515 | 0701SharafDinYunini.Mashyakha | 11,855 | 39 |
| 516 | 0911Suyuti.TabaqatMufassirin | 11,806 | 39 |
| 517 | 0374IbnHusaynAzdi.Makhzun | 11,516 | 38 |
| 518 | 0643DiyaDinMuqaddasi.FadailBaytMaqdis | 11,474 | 38 |
| 519 | 0576IbnMuhammadSilafi.Wajiz | 10,969 | 36 |
| 520 | 0442Tanukhi.TarikhCulamaNahwiyyin | 10,863 | 36 |
| 521 | 0256Bukhari.DucafaSaghir | 10,791 | 35 |
| 522 | 0400IshaqMunajjim.AkamMarjan | 10,606 | 35 |
| 523 | 0628IbnCaliSanhaji.AkhbarMuluk | 10,423 | 34 |
| 524 | 0405AbuFadlHarawi.MucjamFiMushtabah | 10,379 | 34 |
| 525 | 0368Sirafi.AkhbarNahwiyyin | 10,206 | 34 |
| 526 | 1246IbnHamadBassam.DurarMafakhir | 10,058 | 33 |
| 527 | 0374IbnHusaynAzdi.DhikrIsmKullAshab | 9,862 | 32 |
| 528 | 0809IbnQunfudh.Wafayat | 9,725 | 32 |
| 529 | 0245MuhammadIbnHabib.MukhtalafQabail | 9,630 | 32 |
| 530 | 0498AbuCaliJayyani.AlqabSahaba | 9,492 | 31 |
| 531 | 0705SharafDinDimyatti.MucjamShuyukh | 9,252 | 30 |
| 532 | 0259IbnYacqubJuzjani.AhwalRijal | 9,088 | 30 |
| 533 | 0195MuarrijSadusi.HadhfMinNasabQuraysh | 9,074 | 30 |
| 534 | 0385Daruqutni.Ducafa | 9,054 | 30 |
| 535 | 0852IbnHajarCasqalani.TabaqatMudallisin | 8,929 | 29 |
| 536 | 0852IbnHajarCasqalani.ItharBiMacrifa | 8,858 | 29 |
| 537 | 0747MuhyiDinYunini.Mashyakha | 8,748 | 29 |
| 538 | 0862IbnMuhammadMujari.Barnamaj | 8,697 | 28 |
| 539 | 0852IbnHajarCasqalani.TacrifAhlTaqbis | 8,687 | 28 |
| 540 | 0511IbnMandahYahya.MacrifaAsamiArdaf | 8,637 | 28 |
| 541 | 0751IbnQayyimJawziyya.IghathaLahfan | 8,563 | 28 |
| 542 | 0318AbuCurubaHarrani.MuntaqaMinTabaqat | 8,422 | 28 |
| 543 | 0385Daruqutni.SualatNaysaburi | 8,317 | 27 |
| 544 | 0597IbnJawzi.FadailQuds | 8,290 | 27 |
| 545 | 0303Nasai.DucafaWaMatrukin | 8,237 | 27 |
| 546 | 0456IbnHazm.RisalaFiMaratibCulum | 7,743 | 25 |
| 547 | 0365IbnCadiJurjani.AsamiManRawaCanhum | 7,679 | 25 |
| 548 | 0234AbuHasanSacdi.TasmiyaManRuwiya | 7,575 | 25 |
| 549 | 0308IbnIbrahimJundi.FadailMadina | 7,557 | 25 |
| 550 | 0807IbnAhmarKhazraji.NafhaNisriniyya | 7,528 | 25 |
| 551 | 0255Jahiz.MukhtarFiRaddCalaNasara | 7,481 | 24 |
| 552 | 0255Jahiz.AmilWaMamul | 7,425 | 24 |
| 553 | 0222IbnBakkarDabi.AkhbarWafidat | 7,319 | 24 |
| 554 | 1285CabdRahmanTamimi.Maqamat | 7,256 | 24 |
| 555 | 0355MuhammadKindi.FadailMisr | 7,140 | 23 |
| 556 | 0256ZubayrIbnBakkar.Muntakhab | 7,125 | 23 |
| 557 | 0482AbuIshaqHabbal.WafayatMisriyyin | 7,037 | 23 |
| 558 | 0884SibtIbnCajami.TabyinLiAsma | 6,877 | 22 |
| 559 | 0456IbnHazm.AsmaKhulafa | 6,660 | 22 |
| 560 | 0774IbnRaficSallami.MashyakhaBayani | 6,654 | 22 |
| 561 | 0301Bardiji.TabaqatAsma | 6,594 | 21 |
| 562 | 0204IbnKalbi.AnsabKhayl | 6,506 | 21 |
| 563 | 0409CabdGhaniAzdi.KitabMutawarin | 6,452 | 21 |
| 564 | 0597IbnJawzi.TarikhBaytMuqaddas | 6,394 | 21 |
| 565 | 0303Nasai.TasmiyaShuyukh | 6,216 | 20 |
| 566 | 0632AbyHafsSuhrawardi.Mashyakha | 6,008 | 20 |
| 567 | 0241IbnHanbal.AsamiWaKuna | 5,950 | 19 |
| 568 | 0825IbnQasimSabti.IkhtisarAkhbar | 5,839 | 19 |
| 569 | 0884SibtIbnCajami.Ightibat | 5,716 | 19 |
| 570 | 0233YahyaIbnMacin.MinKalamFiRijal | 5,551 | 18 |
| 571 | 0222IbnBakkarDabi.AkhbarWafidin | 5,286 | 17 |
| 572 | 1051Cimadi.RawdaRayya | 4,849 | 16 |
| 573 | 0200AbuShis.Diwan | 4,549 | 15 |
| 574 | 0286Mubarrad.NasabCadnan | 4,412 | 14 |
| 575 | 0524IbnAkfani.DhaylDhaylTarikhMawlidCulama | 4,178 | 13 |
| 576 | 0395IbnMandahMuhammad.Asami | 4,056 | 13 |
| 577 | 0776LisanDinIbnKhatib.KhatraTayf | 3,992 | 13 |
| 578 | 0911Suyuti.Shamarikh | 3,874 | 12 |
| 579 | 0322KatibBaghdadi.TarikhAimma | 3,821 | 12 |
| 580 | 0317AbuQasimBaghawi.TarikhWafatShuyukh | 3,802 | 12 |
| 581 | 0911Suyuti.AsmaMukhadramin | 3,736 | 12 |
| 582 | 1172IbnKhalifaMasakini.Fahrasa | 3,704 | 12 |
| 583 | 0374IbnHusaynAzdi.KunaLiManLaYucrafLahuIsm | 3,572 | 11 |
| 584 | 0826IbnCiraqi.Mudallisin | 3,392 | 11 |
| 585 | 0748Dhahabi.RuwatThiqat | 3,391 | 11 |
| 586 | 0761IbnKaykaldi.Mukhtalitin | 3,340 | 11 |
| 587 | 0110HasanBasri.FadailMakka | 3,334 | 11 |
| 588 | 0567IbnKhashshabBaghdadi.TarikhMawalidAimma | 3,254 | 10 |
| 589 | 0382IbnCabdAllahCaskari.AkhbarMusahhifin | 3,184 | 10 |
| 590 | 0430AbuNucaymIsbahani.DhikrManIsmuhuShucba | 3,082 | 10 |
| 591 | 0248AbuHatimSijistani.FuhulaShucara | 2,637 | 8 |
| 592 | 0430AbuNucaymIsbahani.TasmiyaMaIntahaIlayna | 2,501 | 8 |
| 593 | 0255Jahiz.TabsiraBiTijara | 2,497 | 8 |
| 594 | 0374IbnHusaynAzdi.AsmaManYucrafBiKunya | 2,362 | 7 |
| 595 | 0456IbnHazm.RisalaFiFutuhIslam | 2,234 | 7 |
| 596 | 0303Nasai.TasmiyaManLamYarwi | 2,100 | 7 |
| 597 | 1187SulaymanMahasini.HululTacab | 2,064 | 6 |
| 598 | 0643DiyaDinMuqaddasi.JuzAwham | 2,001 | 6 |
| 599 | 0349IbnCumarMuqri.AkhbarNahwiyyin | 1,790 | 5 |
| 600 | 0374IbnHusaynAzdi.ManWafaqaIsmuhuIsmAbihi | 1,753 | 5 |
| 601 | 0303Nasai.TasmiyaFuqaha | 1,162 | 3 |
| 602 | 0911Suyuti.RihNisrin | 795 | 2 |
| 603 | 0456IbnHazm.UmmahatKhulafa | 693 | 2 |
| 604 | 0303Nasai.Tabaqat | 612 | 2 |
| 605 | 0696Dabbagh.MacalimIman | 187 | 0 |
| 606 | 1450MuhammadSancani.NaylWatar | 150 | 0 |

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
| 0923IbnCabdAllahKhazraji.KhulasaTahdhib | 328,135 | 1,093 |
| 0927Culaymi.UnsJalil | 218,375 | 727 |
| 0927Nucaymi.DarisFiMadaris | 224,568 | 748 |
| 0929IbnKayyal.KawakibNayyirat | 23,699 | 78 |
| 0938IbnCaliBalawi.Thabat | 61,539 | 205 |
| 0945ShamsDinDawudi.TabaqatMufassirin | 139,971 | 466 |
| 0953IbnTulun.MufakahaKhillan | 127,338 | 424 |
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
| 1422MuhammadSalimMuhaysin.MucjamHuffazQuran | 169,932 | 566 |
| 1429BakrIbnCabdAllah.TabaqatNassabin | 23,042 | 76 |
| 1450AkramFaluji.MucjamSaghir | 251,265 | 837 |
| 1450CabdRahmanAlShaykh.Mashahir | 62,418 | 208 |
| 1450MajmacFikrIslami.MawsucaMuallifiImamiya | 249,154 | 830 |
| 1450MuhammadHadiAmini.MucjamMatbicatNajafiya | 44,242 | 147 |
| 1450MuhammadKhayrRamadan.TakmilaMucjamMuallifin | 189,829 | 632 |
| 1450MuhammadSancani.NaylWatar | 150 | 0 |

