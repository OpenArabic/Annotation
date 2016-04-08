# OpenArabic Project (@ AvH Lehrstuhl für Digital Humanities, U Leipzig)

Arabic texts from different periods, collected and reformatted into machine-readable formats (mARkdown > CTS-compliant TEI XML > Perseus DL).

Most of the texts are coming from open online collections of premodern and modern Arabic texts, such as [http://shamela.ws/](http://shamela.ws/) and [http://shiaonlinelibrary.com/](http://shiaonlinelibrary.com/) (These texts have `Shamela+NUMBER` and `Shia+NUMBER`; some texts are coming from _al-Jāmiʿ al-kabīr_, which is not available online (`JK+NUMBER`). Initial metadata from these collections is preserved in the beginning of each file.

Currently uploaded texts are converted automatically into [*mARkdown*](http://maximromanov.github.io/mARkdown/) format and require further manual tagging of the structure; when manual tagging is complete they will be converted into CTS-compliant XML format.

For the list of added books, see below (Mostly premodern chronicles, biographical collections, encyclopaedic dictionaries, gazetteers).

# Prospects and Progress
| *Texts* | *Status* |
|:--- | ------:|
| Total in the Collection | 10,394 |
| Unique texts | 7,790 |
| Scheduled texts __*__  | 260 |
| Scheduled top priority | 201 |
| To be rechecked | 256 |
| Excluded __**__ | 551 |
| Added texts (listed below) | 382 |
| Orphans (no TXT) | 2 |
| Converted to mARkdown | _pending_ |
| Converted to TEI XML  | _pending_ |

__*__ : Predominantly historical, biographical, geographical, and bibliographical texts with ‘serialized data’ (plus, selected dictionaries and lexicons relevant to historical research).

__**__ : Either modern works, or irrelevant for current research purposes.

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
* `NOT` : _no text_, orphan

# Project/Folder structure

- everything is divided into centuries
- each century includes `data` folder
- `data` folder includes `author` folders
- `author` folders include `title` folders
- `title` folders include:
	- texts (often different versions)
	- `arc` folder, where texts are preserved in their pre-formatted form
	- `PDF` folder, which include:
		- **urls.txt** with links to PDFs for about 125 books (usually on [archive.org](archive.org)), which can be downloaded with `wget -i urls.txt` (on 'command line' or 'Terminal')
			- on Mac/Linux all PDFs can be also downloaded with `make` command
			- `wget` must be installed on Windows (Macs usually have it)
		- to save space, PDFs are ignored in this GitHub repositories 
		- if you find new PDFs, add urls (one per line) into a new file **urls_additional.txt**. PDFs can be found via Google, most commonly on:
			- [http://waqfeya.com/](http://waqfeya.com/), with most links lead to [archive.org](archive.org)); other useful sites are:
			- [http://kt-b.com/](http://kt-b.com/) (books are often bulked into large collections, but the selection seems to be larger than on [http://waqfeya.com/](http://waqfeya.com/));
			- [http://bib-alex.com/](http://bib-alex.com/), which has scanned books from the Bibliotheca Alexandrina (unfortunately, most files are stored on file-sharing services and lots of links are already dead)
			- [http://wqf.me/](http://wqf.me/) for manuscripts (search is rather complicated though); most links lead to [archive.org](archive.org) as well.

# Preprocessed titles

## List of books by centuries (382 titles)

* **0100AH [[ [Re]generated on 2016-04-08 (17:51:53) ]]**

    * _no texts at the moment_

* **0200AH [[ [Re]generated on 2016-04-08 (17:51:53) ]]**

    * `0110HasanBasri.FadailMakka (TAGS: ...,PPE)`

* **0300AH [[ [Re]generated on 2016-04-08 (17:51:53) ]]**

    * `0207Waqidi.FutuhSham (TAGS: ...,PPE)`
    * `0207Waqidi.Maghazi (TAGS: ...,PPE)`
    * `0209MacmarIbnMuthanna.Khayl (TAGS: ...,PPE)`
    * `0213IbnHisham.SiraNabawiyya (TAGS: BIO,DHB,PPE)`
    * `0230IbnSacd.TabaqatKubra (TAGS: BIO,COL,PPE)`
    * `0231IbnSallamJumahi.TabaqatFuhulShucara (TAGS: ...,PPE)`
    * `0233YahyaIbnMacin.MinKalamFiRijal (TAGS: ...,PPE)`
    * `0233YahyaIbnMacin.TarikhIbnMacin (TAGS: ...,PPE)`
    * `0234AbuHasanSacdi.TasmiyaManRuwiya  (TAGS: ...,PPE)`
    * `0240KhalifaIbnKhayyat.Tabaqat (TAGS: ...,PPE)`
    * `0240KhalifaIbnKhayyat.Tarikh (TAGS: ...,PPE)`
    * `0241IbnHanbal.AsamiWaKuna (TAGS: ...,PPE)`
    * `0241IbnHanbal.CilalWaMacrifa (TAGS: ...,PPE)`
    * `0249Azraqi.AkhbarMakka (TAGS: ...,PPE)`
    * `0256Bukhari.DucafaSaghir (TAGS: HAD,BIO,PPE)`
    * `0256Bukhari.TarikhKabir (TAGS: ...,PPE)`
    * `0256Bukhari.TarikhSaghir (TAGS: ...,PPE)`
    * `0256ZubayrIbnBakkar.AkhbarMuwaffaqiyat (TAGS: ...,PPE)`
    * `0256ZubayrIbnBakkar.JamharaNasabQuraysh (TAGS: PPE,...)`
    * `0256ZubayrIbnBakkar.Muntakhab (TAGS: ...,PPE)`
    * `0257IbnCabdHakam.FutuhMisr (TAGS: ...,PPE)`
    * `0259IbnYacqubJuzjani.AhwalRijal (TAGS: ...,PPE)`
    * `0261AbuHasanCijli.MacrifaThiqat (TAGS: ...,PPE)`
    * `0261Muslim.KunaWaAsma (TAGS: ...,PPE)`
    * `0261Muslim.Munfaridat (TAGS: ...,PPE)`
    * `0262AbuZaydNumayri.TarikhMadina (TAGS: ...,PPE)`
    * `0272Fakihi.AkhbarMakka (TAGS: ...,PPE)`
    * `0276IbnQutayba.Macarif (TAGS: ...,PPE)`
    * `0277AbuHatimRazi.JarhWaTacdil (TAGS: ...,PPE)`
    * `0277IbnSyfyanFasawi.MacrifaWaTarikh (TAGS: ...,PPE)`
    * `0279Baladhuri.AnsabAshraf (TAGS: GEN,PPE)`
    * `0279Baladhuri.FutuhBuldan (TAGS: ...,PPE)`
    * `0279IbnAbiKhaythama.TarikhKabir (TAGS: ...,PPE)`
    * `0281AbuZurcaDimashqi.Tarikh (TAGS: ...,PPE)`
    * `0282AbuHanifaDinawari.AkhbarTiwal (TAGS: ...,PPE)`
    * `0287Dahhak.AhadWaMathani (TAGS: ...,PPE)`
    * `0292Bahshal.TarikhWasit (TAGS: ...,PPE)`
    * `0292Yacqubi.TarikhYacqubi (TAGS: ...,PPE)`
    * `0300IbnKhurdadhbih.MasalikWaMamalik (TAGS: GEO,PPE)`

* **0400AH [[ [Re]generated on 2016-04-08 (17:51:53) ]]**

    * `0301Bardiji.TabaqatAsma (TAGS: ...,PPE)`
    * `0303Nasai.DucafaWaMatrukin (TAGS: ...,PPE)`
    * `0303Nasai.FadailSahaba (TAGS: ...,PPE)`
    * `0303Nasai.Tabaqat (TAGS: ...,PPE)`
    * `0303Nasai.TasmiyaFuqaha (TAGS: ...,PPE)`
    * `0303Nasai.TasmiyaManLamYarwi (TAGS: ...,PPE)`
    * `0306IbnHayyanDabbi.AkhbarQudat (TAGS: ...,PPE)`
    * `0310IbnAhmadDulabi.Dhariyya (TAGS: ...,PPE)`
    * `0310IbnAhmadDulabi.KunaWaAsma (TAGS: ...,PPE)`
    * `0310Tabari.Tarikh (TAGS: CHR,PPE)`
    * `0317AbuQasimBaghawi.MucjamSahaba (TAGS: ...,PPE)`
    * `0322AbuJacfarCuqayli.DucafaKabir (TAGS: ...,PPE)`
    * `0346Istakhri.MasalikWaMamalik (TAGS: GEO,PPE)`
    * `0346Mascudi.MurujDhahab (TAGS: ...,PPE)`
    * `0347IbnYunusSadafi.Tarikh (TAGS: ...,PPE)`
    * `0349IbnCumarMuqri.AkhbarNahwiyyin (TAGS: ...,PPE)`
    * `0351IbnQanic.MucjamSahaba (TAGS: ...,PPE)`
    * `0354IbnHibban.Majruhin (TAGS: ...,PPE)`
    * `0354IbnHibban.MashahirCulamaAmsar (TAGS: ...,PPE)`
    * `0354IbnHibban.Sira (TAGS: ...,PPE)`
    * `0354IbnHibban.Thiqat (TAGS: ...,PPE)`
    * `0355AbuFarajIsbahani.Aghani (TAGS: ...,PPE)`
    * `0355MuhammadKindi.FadailMisr (TAGS: ...,PPE)`
    * `0355MuhammadKindi.WulatMisr (TAGS: BIO,COL,PPE)`
    * `0360Tabarani.MucjamKabir (TAGS: HAD,COLL,PPE)`
    * `0365IbnCadiJurjani.AsamiManRawaCanhum (TAGS: ...,PPE)`
    * `0365IbnCadiJurjani.KamilFiDucafa (TAGS: ...,PPE)`
    * `0369IbnHayyanAnsari.TabaqatMuhaddithin (TAGS: ...,PPE)`
    * `0370IbnBishrAmidi.MutalifWaMukhtalif (TAGS: ...,BIO,PPE)`
    * `0374IbnHusaynAzdi.AsmaManYucrafBiKunya (TAGS: ...,PPE)`
    * `0374IbnHusaynAzdi.Makhzun (TAGS: HAD,...,PPE)`
    * `0374IbnHusaynAzdi.ManWafaqaIsmuhuIsmAbihi (TAGS: PPE,...)`
    * `0379MuhammadRabci.TarikhMawlidCulama (TAGS: BIO,COL,PPE)`
    * `0382IbnCabdAllahCaskari.AkhbarMusahhifin (TAGS: ...,PPE)`
    * `0385Daruqutni.DhikrAsmaTabicin (TAGS: ...,PPE)`
    * `0385Daruqutni.MutalifWaMukhtalif (TAGS: ...,PPE)`
    * `0385Daruqutni.SualatBarqani (TAGS: ...,PPE)`
    * `0385Daruqutni.SualatNaysaburi (TAGS: ...,PPE)`
    * `0385IbnNadim.Fihrist (TAGS: BIB,PPE)`
    * `0385IbnShahin.TarikhAsmaDucafa (TAGS: ...,PPE)`
    * `0385IbnShahin.TarikhAsmaThiqat (TAGS: ...,PPE)`
    * `0390Muqaddasi.AhsanTaqasim (TAGS: GEO,PPE)`
    * `0395IbnMandahMuhammad.Asami (TAGS: ...,PPE)`
    * `0395IbnMandahMuhammad.FathBab (TAGS: ...,PPE)`
    * `0395IbnMandahMuhammad.MacrifaSahaba (TAGS: ...)`
    * `0398AbuNasrKalabadhi.HidayaWaIrshad (TAGS: ...,PPE)`
    * `0400IbnTahirMaqdisi.BadWaTarikh (TAGS: ...,PPE)`

* **0500AH [[ [Re]generated on 2016-04-08 (17:51:53) ]]**

    * `0403IbnFaradi.TarikhCulamaAndalus (TAGS: ...,PPE)`
    * `0405AbuFadlHarawi.MucjamFiMushtabah (TAGS: ...,PPE)`
    * `0405HakimNaysaburi.TalkhisTarikhNaysabur (TAGS: ...,PPE)`
    * `0405HakimNaysaburi.TasmiyaManAkhrajahum (TAGS: ...,PPE)`
    * `0412Sulami.TabaqatSufiya (TAGS: ...,PPE)`
    * `0421IbnMuhammadMarzuqi.AzminaWaAmkina (TAGS: ...,GEO,PPE)`
    * `0421Miskawayh.Tajarib (TAGS: ...,PPE)`
    * `0427HamzaJurjani.TarikhJurjan (TAGS: ...,PPE)`
    * `0428IbnManjuwayhIsbahani.RijalSahihMuslim (TAGS: ...,PPE)`
    * `0429AbuMansurThacalibi.YatimaDahr (TAGS: ...,PPE)`
    * `0430AbuNucaymIsbahani.DhikrManIsmuhuShucba (TAGS: ...,PPE)`
    * `0430AbuNucaymIsbahani.Ducafa (TAGS: ...,PPE)`
    * `0430AbuNucaymIsbahani.HilyaAwliya (TAGS: ...,PPE)`
    * `0430AbuNucaymIsbahani.MacrifaSahaba (TAGS: ...,PPE)`
    * `0430AbuNucaymIsbahani.TarikhIsbahan (TAGS: ...,PPE)`
    * `0430AbuNucaymIsbahani.TasmiyaMaIntahaIlayna (TAGS: ...,PPE)`
    * `0442Tanukhi.TarikhCulamaNahwiyyin (TAGS: ...,PPE)`
    * `0446AbuYaclaKhalili.IrshadFiMacrifaCulama (TAGS: ...,PPE)`
    * `0448HilalSabi.TuhfaUmara (TAGS: ...,PPE)`
    * `0450Najashi.Rijal (TAGS: ...,BIO,SHC,PPE)`
    * `0456IbnHazm.AsmaKhulafa (TAGS: ...,PPE)`
    * `0456IbnHazm.FadailAndalus (TAGS: ...,PPE)`
    * `0456IbnHazm.JamharaAnsab (TAGS: ...,PPE)`
    * `0458Bayhaqi.DalailNubuwwa (TAGS: DHB,PPE)`
    * `0460ShaykhTusi.Rijal (TAGS: SHC,...,PPE)`
    * `0463IbnCabdBarr.IsticabFiMacrifaAshab (TAGS: BIO,COL,PPE)`
    * `0463KhatibBaghdadi.GhunyaMultamis  (TAGS: ...,PPE)`
    * `0463KhatibBaghdadi.MuttafiqWaMuftariq (TAGS: ...,PPE)`
    * `0463KhatibBaghdadi.TarikhBaghdad (TAGS: BIO,COL,DHB,PPE)`
    * `0466CabdAzizKattani.DhaylTarikhMawlidCulama (TAGS: ...,PPE)`
    * `0474IbnKhalafBaji.TacdilWaTakhrij (TAGS: ...,PPE)`
    * `0475IbnMakula.IkmalFiRafcIrtiyab (TAGS: ...,PPE)`
    * `0475IbnMakula.TahdhibMustamirr (TAGS: ...,PPE)`
    * `0476AbuIshaqShirazi.TabaqatFuqaha (TAGS: BIO,COL,PPE)`
    * `0482AbuIshaqHabbal.WafayatMisriyyin (TAGS: ...,PPE)`
    * `0487AbuCubaydBakri.MasalikWaMamalik (TAGS: GEO,PPE)`
    * `0488IbnFutuhHumaydi.JadhwaMuqtabis (TAGS: ...,PPE)`
    * `0498AbuCaliJayyani.AlqabSahaba (TAGS: ...,PPE)`
    * `0498AbuCaliJayyani.TaqyidMuhmal`

* **0600AH [[ [Re]generated on 2016-04-08 (17:51:53) ]]**

    * `0507AbuBakrShashi.HilyaCulama (TAGS: ...,PPE)`
    * `0507IbnQaysarani.AnsabMuttafiqa (TAGS: PPE)`
    * `0511IbnMandahYahya.MacrifaAsamiArdaf (TAGS: ...)`
    * `0521IbnAbiYacla.TabaqatHanabila (TAGS: BIO,COL,PPE)`
    * `0521MuhammadHamadhani.TakmilaTarikhTabari (TAGS: ...)`
    * `0524IbnAkfani.DhaylDhaylTarikhMawlidCulama (TAGS: ...,PPE)`
    * `0535QawwamSunna.SiyarSalaf (TAGS: ...,BIO,PPE)`
    * `0541IbnCatiyyaMuharibi.Fahrasa (TAGS: ...,PPE)`
    * `0542IbnBassamShantarini.Dhakhira (TAGS: ...,PPE)`
    * `0544CiyadIbnMusaYahsubi.TartibMadarik (TAGS: BIO,COL,PPE)`
    * `0555IbnQalanisi.Tarikh (TAGS: ...,BIO,PPE)`
    * `0561Samcani.Ansab (TAGS: ONO,COL,DHB,PPE)`
    * `0561Samcani.Muntakhab (TAGS: ...,PPE)`
    * `0561Samcani.Tahbir (TAGS: ...,PPE)`
    * `0565IbnZaydBayhaqi.LubabAnsab (TAGS: ...,PPE)`
    * `0565IbnZaydBayhaqi.TarikhBayhaq (TAGS: ...,PPE)`
    * `0571IbnCasakir.MucjamShuyukh (TAGS: ...,PPE)`
    * `0571IbnCasakir.TarikhDimashq (TAGS: BIO,COL,PPE)`
    * `0575IbnKhayrIshbili.Fahrasa (TAGS: ...,PPE)`
    * `0576IbnMuhammadSilafi.MashyakhaBaghdadiyya (TAGS: ...,PPE)`
    * `0576IbnMuhammadSilafi.MucjamSafar (TAGS: BIO,COL,PPE)`
    * `0577IbnAnbari.NuzhaAlibba (TAGS: ...,PPE)`
    * `0578IbnBashkuwal.GhawamidAsma (TAGS: ...,PPE)`
    * `0578IbnBashkuwal.Sila (TAGS: BIO,COL,PPE)`
    * `0584IbnMusaHazimi.Amakin (TAGS: ...,PPE,GEO)`
    * `0597CimadDinKatib.BarqShami (TAGS: ...,PPE)`
    * `0597CimadDinKatib.KharidaQasr (TAGS: POE,COL,PPE)`
    * `0597IbnJawzi.DucafaWaMatrukin (TAGS: ...,PPE)`
    * `0597IbnJawzi.Muntazam (TAGS: BIO,COL,CHR,DHB,PPE)`
    * `0597IbnJawzi.SifaSafwa (TAGS: BIO,COL,PPE)`
    * `0599IbnYahyaDabbi.BughyaMultamis (TAGS: ...,PPE)`

* **0700AH [[ [Re]generated on 2016-04-08 (17:51:53) ]]**

    * `0611SharafDinMuqaddasi.Arbacin (TAGS: ...,PPE)`
    * `0615MuwaffaqDinShafici.MurshidZuwwar (TAGS: ...,PPE,GEO)`
    * `0623Qazwini.Tadwin (TAGS: ...,PPE)`
    * `0626YaqutHamawi.Khazal (TAGS: ...,GEO,PPE)`
    * `0626YaqutHamawi.MucjamBuldan (TAGS: GEO,COL,PPE)`
    * `0626YaqutHamawi.MucjamUdaba (TAGS: BIO,COL,POE,PPE)`
    * `0629IbnNuqta.TakmilaIkmal (TAGS: ...,PPE)`
    * `0629IbnNuqta.TaqyidLiMacrifa (TAGS: BIO,COL,PPE)`
    * `0630IbnAthirCizzDin.Kamil (TAGS: CHR,PPE)`
    * `0630IbnAthirCizzDin.LubabFiTahdhibAnsab (TAGS: ONO,COL,PPE)`
    * `0630IbnAthirCizzDin.UsdGhaba (TAGS: ...,PPE)`
    * `0637IbnMustafwi.TarikhIrbil (TAGS: ...,PPE)`
    * `0639AbuBakrMalaqi.MatlacAnwar (TAGS: ...,PPE)`
    * `0640AbuHafsDunaysiri.TarikhDunaysir (TAGS: ...)`
    * `0641Sarifini.Muntakhab (TAGS: ...,PPE)`
    * `0642IbnNajjar.DhaylTarikhBaghdad (TAGS: BIO,COL,PPE)`
    * `0643IbnSalahShahrazuri.TabaqatFuqaha (TAGS: BIO,COL,PPE)`
    * `0646IbnQifti.IkhbarCulama (TAGS: ...,PPE)`
    * `0646IbnQifti.InbahRuwat (TAGS: ...,PPE)`
    * `0646IbnQifti.Muhammadun (TAGS: ...,PPE)`
    * `0647CabdWahidMarrakushi.Mucjib (TAGS: ...,PPE)`
    * `0658IbnAbbar.HullaSiyara (TAGS: ...,PPE)`
    * `0658IbnAbbar.MucjamAshab (TAGS: PPE)`
    * `0658IbnAbbar.TakmilaLiSila (TAGS: BIO,COL,PPE)`
    * `0658IbnAbbar.TuhfaQadim (TAGS: ...)`
    * `0659SainDinNaccal.Mashyakha (TAGS: ...,PPE)`
    * `0660IbnCadim.BughyatTalib (TAGS: ...,PPE)`
    * `0660IbnCadim.ZubdaHalab (TAGS: ...,PPE)`
    * `0665AbuShama.Rawdatayn (TAGS: ...,PPE)`
    * `0668IbnAbiUsaybica.CuyunAnba (TAGS: BIO,COL,PPE)`
    * `0673AbuMahasinYaghmuri.NurQabas (TAGS: ...,PPE)`
    * `0676Nawawi.TahdhibAsma (TAGS: ...,PPE)`
    * `0680IbnSabuni.TakmilaIkmalIkmal (TAGS: ONO,...,PPE)`
    * `0681IbnKhallikan.WafayatAcyan (TAGS: BIO,COL,DHB,PPE)`
    * `0682ZakariyaQazwini.AtharBilad (TAGS: ...,PPE)`
    * `0684IbnShaddad.AclaqKhatira (TAGS: ...,PPE)`
    * `0685IbnCibri.TarikhMukhtasarDuwal (TAGS: ...,PPE)`
    * `0685IbnSacidMaghribi.Jughrafiya (TAGS: ...,GEO,PPE)`
    * `0685IbnSacidMaghribi.Mughrib (TAGS: ...,PPE)`
    * `0690IbnMujawirDimashqi.TarikhMustabsir (TAGS: ...,PPE)`
    * `0694MuhibbDinTabari.Dhakhair (TAGS: ...,PPE)`
    * `0694MuhibbDinTabari.RiyadNadira`
    * `0696Dabbagh.MacalimIman (TAGS: NOT,BIO,COL,PPE)`

* **0800AH [[ [Re]generated on 2016-04-08 (17:51:53) ]]**

    * `0703Marakishi.DhaylWaTakmila (TAGS: ...,PPE)`
    * `0709CaliCalawi.Majdi (TAGS: ...,GEN,SHC,PPE)`
    * `0711IbnManzurIfriqi.MukhtasarTarikhDimashq (TAGS: BIO,COL,PPE)`
    * `0714AhmadGhibrini.CunwanDiraya (TAGS: ...,BIO,PPE)`
    * `0726Yunini.DhaylMiratZaman (TAGS: CHR,BIO,COL,PPE)`
    * `0732AbuFida.MukhtasarFiAkhbar (TAGS: ...,PPE)`
    * `0732IbnYacqubJanadi.SulukFiTabaqat (TAGS: BIO,COL,PPE)`
    * `0733IbnJamaca.Mashyakha (TAGS: ...,BIO,PPE)`
    * `0733Nuwayri.NihayaArab (TAGS: ...,PPE)`
    * `0742Mizzi.TahdhibKamal (TAGS: DHB,PPE)`
    * `0748Dhahabi.CibarFiKhabar (TAGS: CHR,PPE)`
    * `0748Dhahabi.DhaylCibar (TAGS: ...,PPE)`
    * `0748Dhahabi.DhaylDiwanDucafa (TAGS: ...,PPE)`
    * `0748Dhahabi.DhikrAsmaManTakallama (TAGS: DHB,PPE)`
    * `0748Dhahabi.DiwanDucafa (TAGS: ...,PPE)`
    * `0748Dhahabi.Kashif (TAGS: ...,PPE)`
    * `0748Dhahabi.MacrifaQurraKibar (TAGS: BIO,COL,PPE)`
    * `0748Dhahabi.MizanIctidal (TAGS: ...,PPE)`
    * `0748Dhahabi.MucinFiTabaqatMuhaddithin (TAGS: ...,PPE)`
    * `0748Dhahabi.MucjamMuhaddithin  (TAGS: ...,PPE)`
    * `0748Dhahabi.MucjamShuyukh (TAGS: BIO,COL,PPE)`
    * `0748Dhahabi.MughniFiDucafa (TAGS: DHB,PPE)`
    * `0748Dhahabi.MukhtasarMinDubaythi (TAGS: ...,PPE)`
    * `0748Dhahabi.Muqtana (TAGS: DHB,PPE)`
    * `0748Dhahabi.RuwatThiqat (TAGS: DHB,PPE)`
    * `0748Dhahabi.SiyarAclamNubala (TAGS: BIO,COL,DHB,PPE)`
    * `0748Dhahabi.TadhkiraHuffaz (TAGS: BIO,COL,PPE)`
    * `0748Dhahabi.TarikhIslam (TAGS: BIO,COL,CHR,DHB,PPE)`
    * `0748IbnDimyati.Mustafad (TAGS: ...,PPE)`
    * `0749IbnWardi.Tarikh (TAGS: ...,PPE)`
    * `0749ShihabDinCumari.MasalikAbsar (TAGS: ...,PPE)`
    * `0749Wadiashi.Barnamaj (TAGS: BIB,PPE)`
    * `0761IbnKaykaldi.JamicTahsil (TAGS: ...,PPE)`
    * `0761IbnKaykaldi.Mukhtalitin (TAGS: ...,PPE)`
    * `0762MughaltayIbnQalij.IkmalTahdhib (TAGS: ...,PPE)`
    * `0764IbnShakirKutubi.FawatWafayat (TAGS: ...,PPE)`
    * `0764Safadi.AcyanCasr (TAGS: BIO,COL,PPE)`
    * `0764Safadi.NaktHimyan (TAGS: ...,PPE)`
    * `0764Safadi.WafiBiWafayat (TAGS: BIO,COL,PPE)`
    * `0765AbuMahasinHusayni.DhaylTadhkira (TAGS: ...,PPE)`
    * `0765AbuMahasinHusayni.IkmalLiRijal (TAGS: ...,PPE)`
    * `0767Balawi.TajMafriq (TAGS: ...,PPE)`
    * `0768Yafici.MiratJanan (TAGS: ...,PPE)`
    * `0771Subki.MucjamShuyukh (TAGS: ...,PPE)`
    * `0771Subki.TabaqatShaficiyaKubra (TAGS: BIO,COL,PPE)`
    * `0774IbnKathir.Bidaya (TAGS: BIO,COL,CHR,PPE)`
    * `0774IbnKathir.TabaqatShaficiyyin (TAGS: BIO,COL,PPE)`
    * `0774IbnKathir.Takmil (TAGS: ...,PPE)`
    * `0774IbnRaficSallami.Wafayat (TAGS: ...,PPE)`
    * `0775IbnAbiWafa.JawahirMudiya (TAGS: BIO,COL,PPE)`
    * `0776LisanDinIbnKhatib.Ihata (TAGS: ...,PPE)`
    * `0776LisanDinIbnKhatib.KatibaKamina (TAGS: ...,PPE)`
    * `0776LisanDinIbnKhatib.KhatraTayf (TAGS: ...,GEO,PPE)`
    * `0793AbuHasanMalaqi.TarikhQudat (TAGS: ...,PPE)`
    * `0795IbnRajabHanbali.DhaylTabaqatHanabila (TAGS: BIO,COL,PPE)`
    * `0799IbnFarhun.DibajMudhahhab (TAGS: ...,PPE)`

* **0900AH [[ [Re]generated on 2016-04-08 (17:51:53) ]]**

    * `0804IbnMulaqqin.TabaqatAwliya (TAGS: ...,PPE)`
    * `0808IbnKhaldun.Tarikh (TAGS: CHR,PPE)`
    * `0809IbnQunfudh.Wafayat (TAGS: ...,PPE)`
    * `0812CaliKhazraji.CuqudLuluiyya (TAGS: ...,PPE)`
    * `0817IbnYacqubFiruzabadi.BulghaFiTarajim (TAGS: ...,PPE)`
    * `0826IbnCiraqi.TuhfaTahsil (TAGS: ...,PPE)`
    * `0832AbuTayyibFasi.DhaylTaqyid (TAGS: ...,PPE)`
    * `0832AbuTayyibFasi.ShifaGharam (TAGS: ...,PPE)`
    * `0833IbnJazari.GhayaNihaya (TAGS: ...,PPE)`
    * `0842IbnNasirDinDimashqi.RaddWafir (TAGS: ...,PPE)`
    * `0842IbnNasirDinDimashqi.TawdihMushtabih (TAGS: ...,PPE)`
    * `0845Maqrizi.IqazHunafa (TAGS: ...,PPE)`
    * `0845Maqrizi.Mawaciz (TAGS: ...,PPE)`
    * `0845Maqrizi.MukhtasarKamil (TAGS: ...,PPE)`
    * `0845Maqrizi.Suluk (TAGS: ...,PPE)`
    * `0851IbnQadiShuhba.TabaqatShaficiya (TAGS: BIO,COL,PPE)`
    * `0852IbnHajarCasqalani.DurarKamina (TAGS: BIO,COL,PPE)`
    * `0852IbnHajarCasqalani.InbaGhumr (TAGS: ...,PPE)`
    * `0852IbnHajarCasqalani.IsabaFiTamyiz (TAGS: ...,PPE)`
    * `0852IbnHajarCasqalani.ItharBiMacrifa`
    * `0852IbnHajarCasqalani.LisanMizan (TAGS: BIO,COL,PPE)`
    * `0852IbnHajarCasqalani.NuzhaAlbab (TAGS: ...,PPE)`
    * `0852IbnHajarCasqalani.RafcCisr (TAGS: ...,PPE)`
    * `0852IbnHajarCasqalani.TabaqatMudallisin (TAGS: BIO,COL,PPE)`
    * `0852IbnHajarCasqalani.TabsirMuntabih (TAGS: ...,PPE)`
    * `0852IbnHajarCasqalani.TacjilManfaca (TAGS: ...,PPE)`
    * `0852IbnHajarCasqalani.TahdhibTahdhib (TAGS: ...,PPE)`
    * `0852IbnHajarCasqalani.TaqribTahdhib (TAGS: ...,PPE)`
    * `0855Cayni.CiqdJuman (TAGS: ...,PPE)`
    * `0855Cayni.CumdaQari (TAGS: ...,PPE)`
    * `0855Cayni.MaghaniAkhyar (TAGS: ...,PPE)`
    * `0871IbnFahdMakki.LahzAlhaz (TAGS: BIO,...,PPE)`
    * `0874IbnTaghribirdi.ManhalSafi (TAGS: ...,PPE)`
    * `0874IbnTaghribirdi.MawridLatafa (TAGS: ...,PPE)`
    * `0874IbnTaghribirdi.NujumZahira (TAGS: ...,PPE)`
    * `0879IbnQutlubugha.TajTarajim (TAGS: ...,PPE)`
    * `0879IbnQutlubugha.Thiqat (TAGS: ...,PPE)`
    * `0884IbnMuflih.MaqsidArshad (TAGS: ...,PPE)`
    * `0884SibtIbnCajami.Ightibat (TAGS: ...,PPE)`
    * `0884SibtIbnCajami.KashfHathith (TAGS: ...,PPE)`
    * `0884SibtIbnCajami.KunuzDhahab (TAGS: ...,PPE)`
    * `0884SibtIbnCajami.TabyinLiAsma (TAGS: ...,PPE)`
    * `0900AbuCabdAllahHimyari.RawdMictar (TAGS: GEO,COL,PPE)`

* **1000AH [[ [Re]generated on 2016-04-08 (17:51:53) ]]**

    * `0902Sakhawi.DuLamic (TAGS: BIO,COL,PPE)`
    * `0902Sakhawi.TuhfaLatifa (TAGS: ...,PPE)`
    * `0904Burayhi.TabaqatSulahaYaman (TAGS: ...,PPE)`
    * `0905Basrawi.Tarikh (TAGS: ...,PPE)`
    * `0909IbnMibradHanbali.MucjamKutub (TAGS: BIB,...,PPE)`
    * `0911Suyuti.AsmaMukhadramin (TAGS: ...,PPE)`
    * `0911Suyuti.BughyaWucat (TAGS: BIO,COL,PPE)`
    * `0911Suyuti.DhaylTabaqatHuffaz (TAGS: ...,PPE)`
    * `0911Suyuti.HusnMuhadara (TAGS: ...,PPE)`
    * `0911Suyuti.IscafMubatta (TAGS: ...,PPE)`
    * `0911Suyuti.LubbLubab (TAGS: ...,PPE)`
    * `0911Suyuti.NazmCiqyan (TAGS: ...,PPE)`
    * `0911Suyuti.RihNisrin (TAGS: ...,PPE)`
    * `0911Suyuti.TabaqatHuffaz (TAGS: BIO,COL,PPE)`
    * `0911Suyuti.TabaqatMufassirin (TAGS: ...,PPE)`
    * `0911Suyuti.TarikhKhulafa (TAGS: ...,PPE)`
    * `0923IbnCabdAllahKhazraji.KhulasaTahdhib (TAGS: ...,PPE)`
    * `0927Culaymi.UnsJalil (TAGS: ...,PPE)`
    * `0927Nucaymi.DarisFiMadaris (TAGS: COL,PPE)`
    * `0929IbnKayyal.KawakibNayyirat (TAGS: ...,PPE)`
    * `0938IbnCaliBalawi.Thabat (TAGS: BIB,PPE)`
    * `0945ShamsDinDawudi.TabaqatMufassirin (TAGS: ...,PPE)`
    * `0968Tashkubruizadah.ShaqaiqNucmaniyya (TAGS: BIO,COL,PPE)`
    * `0973CabdWahhabShacrani.LawaqihAnwar (TAGS: ...,PPE)`

* **1100AH [[ [Re]generated on 2016-04-08 (17:51:53) ]]**

    * `1010TamimiDari.TabaqatSaniya (TAGS: BIO,COL,PPE)`
    * `1037CabdQadirCaydarus.TarikhNurSafir (TAGS: ...,PPE)`
    * `1041BurhanDinMaliki.BahjaMahafil (TAGS: ...,PPE)`
    * `1041Maqarri.NafhTib (TAGS: ...,PPE)`
    * `1051Cimadi.RawdaRayya (TAGS: ...,PPE)`
    * `1061NajmDinGhazzi.KawakibSaira (TAGS: ...,PPE)`
    * `1067HajjiKhalifa.KashfZunun (TAGS: BIB,COL,PPE)`
    * `1078RiyadZadah.AsmaKutub (TAGS: BIB,PPE)`
    * `1089IbnCimad.Shadharat (TAGS: BIO,COL,CHR,PPE)`
    * `1100IbnMuhammadAdnahwi.TabaqatMufassirin (TAGS: ...,PPE)`
    * `1100MustafaTafrishi.NaqdRijal (TAGS: ...,BIO,SHC,PPE)`

* **1200AH [[ [Re]generated on 2016-04-08 (17:51:53) ]]**

    * `1111MuhammadAminMuhibbi.KhulasaAthr (TAGS: ...,PPE)`
    * `1119IbnMacsum.SulafaCasr (TAGS: ...,BIO,PPE)`
    * `1120CaliKhanMadani.DarajatRafica (TAGS: SHC,...,PPE)`
    * `1126MuhammadHanbali.Mashyakha (TAGS: ...,PPE)`
    * `1147CabdAllahSancani.TarikhYaman (TAGS: ...,PPE)`
    * `1175MuhammadKarabisi.IklilManhaj (TAGS: ...,BIO,SHC,PPE)`

* **1300AH [[ [Re]generated on 2016-04-08 (17:51:53) ]]**

    * `1206Muradi.SilkDurar (TAGS: ...,PPE)`
    * `1212BahrCulum.FawaidRijaliya (TAGS: SHC,...,PPE)`
    * `1212BahrCulum.FawaidRijaliya (TAGS: SHC,PPE)`
    * `1232IbnKhatibCumari.RawdaFayha (TAGS: ...,PPE)`
    * `1237Jabarti.CajaibAthar (TAGS: ...,PPE)`
    * `1250IbnCaliShaykani.BadrTalic (TAGS: ...,PPE)`
    * `1269CabdMalikCasimi.SamtNujum (TAGS: ...,PPE)`
    * `1286IcjazHusaynKunturi.KashfHajb (TAGS: BIB,PPE)`

* **1400AH [[ [Re]generated on 2016-04-08 (17:51:53) ]]**

    * `1307Qannawji.AbjadCulum (TAGS: ...,PPE)`
    * `1307Qannawji.HittaFiDhikr (TAG: BIB,...)`
    * `1307Qannawji.LuqtaCajlan (TAGS: BIB,...,PPE)`
    * `1313Barujirdi.Taraif (TAGS: ...,SHC,PPE)`
    * `1313VanDyck.IktifaQunuc (TAGS: ...,PPE)`
    * `1315Salawi.IstiqsaLiAhkbar (TAGS: ...,PPE)`
    * `1318MuhammadSanusi.Musamarat (TAGS: ...,PPE)`
    * `1330IbnMusaTabrizi.MiratKutub (TAGS: ...,BIB,PPE)`
    * `1335CabdRazzaqBaytar.HilyaBashar (TAGS: ...,PPE)`
    * `1338MuhammadFaridBey.Tarikh (TAGS: ...,PPE)`
    * `1339IsmacilBashaBaghdadi.HadiyaCarifin (TAGS: BIO,BIB,COL,PPE)`
    * `1339IsmacilBashaBaghdadi.IdahMaknun (TAGS: BIB,COL,PPE)`
    * `1341CabdHayyTalibi.IclamBiMan (TAGS: ...,PPE)`
    * `1345IbnJacfarKattani.RisalaMustatrafa (TAGS: ...,PPE)`
    * `1346CbdQadirBadran.Munadama (TAGS: ...,PPE)`
    * `1351IbnHusaynGhazzi.NahrDhahab (TAGS: ...,PPE)`
    * `1355AhmadTahtawi.TanbihWaIqaz (TAGS: ...,BIO,PPE)`
    * `1360IbnQasimMakhluf.ShajaraNur (TAGS: BIO,COL,PPE)`
    * `1368HasanAmin.MustadrakatAcyanShica (TAGS: ...,PPE)`
    * `1371MuhsinCamili.AcyanShica (TAGS: ...,PPE)`
    * `1372KurdCali.KhitatSham (TAGS: ...,PPE)`
    * `1381MuhammadSancani.MulhaqBadr (TAGS: ...,PPE)`
    * `1383CadbHayyKattani.FihrisFaharis (TAGS: BIB,PPE)`
    * `1389AghaBuzurgTihrani.DharicaFiTasanifShica (TAGS: BIB,PPE)`
    * `1389AghaBuzurgTihrani.DhaylKashfZunun (TAGS: BIB,PPE)`
    * `1389AghaBuzurgTihrani.TASHAnwarSatica (TAGS: ...,PPE)`
    * `1389AghaBuzurgTihrani.TASHNawabighRuwat (TAGS: ...,PPE)`
    * `1396KhayrDinZirikli.Aclam (TAGS: PPE,BIO,COL)`

* **1500AH [[ [Re]generated on 2016-04-08 (17:51:53) ]]**

    * `1405CaliShahrudi.Mustadrakat (TAGS: ...,SHC,PPE)`
    * `1408CumarKahhala.MucjamMuallifin (TAGS: ...,BIB,BIO,COL,PPE)`
    * `1411SayyidKhui.MucjamRijal (TAGS: ...,PPE)`
    * `1418SalihAhmadArkani.TihfaMajalis (TAGS: BIB,PPE)`
    * `1422MuhammadSalimMuhaysin.MucjamHuffazQuran (TAGS: ...,PPE)`
    * `1450MuhammadSancani.NaylWatar (TAGS: NOT,BIO,COL,PPE)`
