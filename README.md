# OpenArabic Project (@ AvH Lehrstuhl für Digital Humanities, U Leipzig)

Arabic texts from different periods, collected and reformatted into machine-readable formats (mARkdown > CTS-compliant TEI XML > Perseus DL)

Currently uploaded texts are converted automatically into [*mARkdown*](http://maximromanov.github.io/mARkdown/) format and require further manual tagging of the structure; when manual tagging is complete they will be converted into CTS-compliant XML format.

For the list of added books, see below (Mostly premoderns chronicles, biographical collections, encyclopaedic dictionaries, gazetteers).

# Prospects and Progress
| *Texts* | *Status* |
|:--- | ------:|
| Total in the Collection | 10,393 |
| Unique texts | 7,802 |
| Scheduled texts __*__  | 523 |
| Scheduled top priority | 301 |
| To be rechecked | 263 |
| Excluded __**__ | 535 |
| Added texts (listed below) | 110 |
| Converted to mARkdown | _pending_ |
| Converted to TEI XML  | _pending_ |

__*__ : Predominantly historical, biographical, geographical, and bibliographical texts with ‘serialized data’ (plus, selected dictionaries and lexicons relevant to historical research).

__**__ : Either modern works, or irrelevant for current research purposes.

# Text Description Tags

Tags follow the URI of a text in the following format **(TAGS: TAG,TAG,TAG)**. Combinations of tags specify the description of the text, for example, **BIO** refers to 'a biographical text', but **BIO,COL** refers more specifically to 'a biographical collection'. 

* **BIB** : bibliographical
* **BIO** : biographical
* **CHR** : chronicle
* **COL** : collection, dictionary, anthology
* **GEN** : genealogical
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

# Preprocessed titles

## List of books by centuries (110 titles)

* **0100AH [[ [Re]generated on 2016-03-23 (20:34:17) ]]**

    * _no texts at the moment_

* **0200AH [[ [Re]generated on 2016-03-23 (20:34:17) ]]**

    * _no texts at the moment_

* **0300AH [[ [Re]generated on 2016-03-23 (20:34:17) ]]**

    * `0230IbnSacd.TabaqatKubra (TAGS: BIO,COL)`
    * `0240KhalifaIbnKhayyat.Tabaqat (TAGS: ...)`
    * `0240KhalifaIbnKhayyat.Tarikh (TAGS: ...)`

* **0400AH [[ [Re]generated on 2016-03-23 (20:34:17) ]]**

    * `0310Tabari.Tarikh (TAGS: CHR)`
    * `0347IbnYunusSadafi.Tarikh (TAGS: ...)`
    * `0354IbnHibban.Thiqat (TAGS: ...)`
    * `0385IbnNadim.Fihrist (TAGS: BIB)`

* **0500AH [[ [Re]generated on 2016-03-23 (20:34:17) ]]**

    * `0403IbnFaradi.TarikhCulamaAndalus (TAGS: ...)`
    * `0429AbuMansurThacalibi.YatimaDahr (TAGS: ...)`
    * `0430AbuNucaymIsbahani.TarikhIsbahan (TAGS: ...)`
    * `0463KhatibBaghdadi.TarikhBaghdad (TAGS: BIO,COL)`
    * `0475IbnMakula.IkmalFiRafcIrtiyab (TAGS: ...)`

* **0600AH [[ [Re]generated on 2016-03-23 (20:34:17) ]]**

    * `0521IbnAbiYacla.TabaqatHanabila (TAGS: BIO,COL)`
    * `0544CiyadIbnMusaYahsubi.TartibMadarik (TAGS: BIO,COL)`
    * `0561Samcani.Ansab (TAGS: ONO,COL)`
    * `0571IbnCasakir.TarikhDimashq (TAGS: BIO,COL)`
    * `0576IbnMuhammadSilafi.MucjamSafar (TAGS: BIO,COL)`
    * `0578IbnBashkuwal.Sila (TAGS: BIO,COL)`
    * `0597IbnJawzi.Muntazam (TAGS: BIO,COL,CHR)`
    * `0599IbnYahyaDabbi.BughyaMultamis (TAGS: ...)`

* **0700AH [[ [Re]generated on 2016-03-23 (20:34:17) ]]**

    * `0623Qazwini.Tadwin (TAGS: ...)`
    * `0626YaqutHamawi.MucjamUdaba (TAGS: BIO,COL,POE)`
    * `0629IbnNuqta.TakmilaIkmal (TAGS: ...)`
    * `0629IbnNuqta.TaqyidLiMacrifa (TAGS: BIO,COL)`
    * `0630IbnAthirCizzDin.Kamil (TAGS: CHR)`
    * `0630IbnAthirCizzDin.LubabFiTahdhibAnsab (TAGS: ...)`
    * `0637IbnMustafwi.TarikhIrbil (TAGS: ...)`
    * `0641Sarifini.Muntakhab (TAGS: ...)`
    * `0642IbnNajjar.DhaylTarikhBaghdad (TAGS: BIO,COL)`
    * `0646IbnQifti.InbahRuwat (TAGS: ...)`
    * `0658IbnAbbar.TakmilaLiSila (TAGS: BIO,COL)`
    * `0659SainDinNaccal.Mashyakha (TAGS: ...)`
    * `0660IbnCadim.BughyatTalib (TAGS: ...)`
    * `0681IbnKhallikan.WafayatAcyan (TAGS: BIO,COL)`
    * `0684IbnShaddad.AclaqKhatira (TAGS: ...)`

* **0800AH [[ [Re]generated on 2016-03-23 (20:34:17) ]]**

    * `0711IbnManzurIfriqi.MukhtasarTarikhDimashq (TAGS: BIO,COL)`
    * `0726Yunini.DhaylMiratZaman (TAGS: CHR,BIO,COL)`
    * `0732AbuFida.MukhtasarFiAkhbar (TAGS: ...)`
    * `0732IbnYacqubJanadi.SulukFiTabaqat (TAGS: BIO,COL)`
    * `0733Nuwayri.NihayaArab (TAGS: ...)`
    * `0742Mizzi.TahdhibKamal (TAGS: ...)`
    * `0748Dhahabi.CibarFiKhabar (TAGS: CHR)`
    * `0748Dhahabi.MacrifaQurraKibar (TAGS: BIO,COL)`
    * `0748Dhahabi.MizanIctidal (TAGS: ...)`
    * `0748Dhahabi.MucjamShuyukh (TAGS: BIO,COL)`
    * `0748Dhahabi.MukhtasarMinDubaythi (TAGS: ...)`
    * `0748Dhahabi.SiyarAclamNubala (TAGS: BIO,COL)`
    * `0748Dhahabi.TadhkiraHuffaz (TAGS: BIO,COL)`
    * `0748Dhahabi.TarikhIslam (TAGS: BIO,COL,CHR)`
    * `0749IbnWardi.Tarikh (TAGS: ...)`
    * `0762MughaltayIbnQalij.IkmalTahdhib (TAGS: ...)`
    * `0764IbnShakirKutubi.FawatWafayat (TAGS: ...)`
    * `0764Safadi.AcyanCasr (TAGS: BIO,COL)`
    * `0764Safadi.WafiBiWafayat (TAGS: BIO,COL)`
    * `0768Yafici.MiratJanan (TAGS: ...)`
    * `0771Subki.TabaqatShaficiyaKubra (TAGS: BIO,COL)`
    * `0774IbnKathir.Bidaya (TAGS: BIO,COL,CHR)`
    * `0774IbnKathir.TabaqatShaficiyyin (TAGS: BIO,COL)`
    * `0775IbnAbiWafa.JawahirMudiya (TAGS: BIO,COL)`
    * `0776LisanDinIbnKhatib.Ihata (TAGS: ...)`
    * `0795IbnRajabHanbali.DhaylTabaqatHanabila (TAGS: BIO,COL)`
    * `0799IbnFarhun.DibajMudhahhab (TAGS: ...)`

* **0900AH [[ [Re]generated on 2016-03-23 (20:34:17) ]]**

    * `0808IbnKhaldun.Muqaddima (TAGS: CHR)`
    * `0832AbuTayyibFasi.DhaylTaqyid (TAGS: ...)`
    * `0832AbuTayyibFasi.ShifaGharam (TAGS: ...)`
    * `0833IbnJazari.GhayaNihaya (TAGS: ...)`
    * `0842IbnNasirDinDimashqi.TawdihMushtabih (TAGS: ...)`
    * `0845Maqrizi.Mawaciz (TAGS: ...)`
    * `0845Maqrizi.Suluk (TAGS: ...)`
    * `0851IbnQadiShuhba.TabaqatShaficiya (TAGS: BIO,COL)`
    * `0852IbnHajarCasqalani.InbaGhumr (TAGS: ...)`
    * `0852IbnHajarCasqalani.IsabaFiTamyiz (TAGS: ...)`
    * `0852IbnHajarCasqalani.LisanMizan (TAGS: BIO,COL)`
    * `0852IbnHajarCasqalani.RafcCisr (TAGS: ...)`
    * `0852IbnHajarCasqalani.TahdhibTahdhib (TAGS: ...)`
    * `0852IbnHajarCasqalani.TaqribTahdhib (TAGS: ...)`
    * `0855Cayni.CumdaQari (TAGS: ...)`
    * `0855Cayni.MaghaniAkhyar (TAGS: ...)`
    * `0874IbnTaghribirdi.ManhalSafi (TAGS: ...)`
    * `0874IbnTaghribirdi.NujumZahira (TAGS: ...)`
    * `0879IbnQutlubugha.Thiqat (TAGS: ...)`
    * `0884IbnMuflih.MaqsidArshad (TAGS: ...)`

* **1000AH [[ [Re]generated on 2016-03-23 (20:34:17) ]]**

    * `0902Sakhawi.DuLamic (TAGS: BIO,COL)`
    * `0902Sakhawi.TuhfaLatifa (TAGS: ...)`
    * `0911Suyuti.BughyaWucat (TAGS: BIO,COL)`
    * `0911Suyuti.HusnMuhadara (TAGS: ...)`
    * `0911Suyuti.TabaqatHuffaz (TAGS: BIO,COL)`
    * `0911Suyuti.TabaqatMufassirin (TAGS: ...)`
    * `0923IbnCabdAllahKhazraji.KhulasaTahdhib (TAGS: ...)`
    * `0927Nucaymi.DarisFiMadaris (TAGS: COL)`
    * `0945ShamsDinDawudi.TabaqatMufassirin (TAGS: ...)`

* **1100AH [[ [Re]generated on 2016-03-23 (20:34:17) ]]**

    * `1010TamimiDari.TabaqatSaniya (TAGS: BIO,COL)`
    * `1061NajmDinGhazzi.KawakibSaira (TAGS: ...)`
    * `1067HajjiKhalifa.KashfZunun (TAGS: BIB,COL)`
    * `1089IbnCimad.Shadharat (TAGS: BIO,COL,CHR)`
    * `1100IbnMuhammadAdnahwi.TabaqatMufassirin (TAGS: ...)`

* **1200AH [[ [Re]generated on 2016-03-23 (20:34:17) ]]**

    * `1111MuhammadAminMuhibbi.KhulasaAthr (TAGS: ...)`

* **1300AH [[ [Re]generated on 2016-03-23 (20:34:17) ]]**

    * `1206Muradi.SilkDurar (TAGS: ...)`
    * `1250IbnCaliShaykani.BadrTalic (TAGS: ...)`
    * `1269CabdMalikCasimi.SamtNujum (TAGS: ...)`
    * `1286IcjazHusaynKunturi.KashfHajb (TAGS: BIB)`

* **1400AH [[ [Re]generated on 2016-03-23 (20:34:17) ]]**

    * `1315Salawi.IstiqsaLiAhkbar (TAGS: ...)`
    * `1318MuhammadSanusi.Musamarat (TAGS: ...)`
    * `1335CabdRazzaqBaytar.HilyaBashar (TAGS: ...)`
    * `1339IsmacilBashaBaghdadi.HadiyaCarifin (TAGS: BIO,BIB,COL)`
    * `1339IsmacilBashaBaghdadi.IdahMaknun (TAGS: BIB,COL)`
    * `1341CabdHayyTalibi.IclamBiMan (TAGS: ...)`
    * `1351IbnHusaynGhazzi.NahrDhahab (TAGS: ...)`
    * `1360IbnQasimMakhluf.ShajaraNur (TAGS: BIO,COL)`
    * `1389AghaBuzurgTihrani.DharicaFiTasanifShica (TAGS: BIB, ...)`

* **1500AH [[ [Re]generated on 2016-03-23 (20:34:17) ]]**

    * _no texts at the moment_
