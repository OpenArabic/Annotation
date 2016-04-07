# OpenArabic Project (@ AvH Lehrstuhl für Digital Humanities, U Leipzig)

Arabic texts from different periods, collected and reformatted into machine-readable formats (mARkdown > CTS-compliant TEI XML > Perseus DL).

Most of the texts are coming from open online collections of premodern and modern Arabic texts, such as [http://shamela.ws/](http://shamela.ws/) and [http://shiaonlinelibrary.com/](http://shiaonlinelibrary.com/) (These texts have `Shamela+NUMBER` and `Shia+NUMBER`; some texts are coming from _al-Jāmiʿ al-kabīr_, which is not available online (`JK+NUMBER`). Initial metadata from these collections is preserved in the beginning of each file.

Currently uploaded texts are converted automatically into [*mARkdown*](http://maximromanov.github.io/mARkdown/) format and require further manual tagging of the structure; when manual tagging is complete they will be converted into CTS-compliant XML format.

For the list of added books, see below (Mostly premodern chronicles, biographical collections, encyclopaedic dictionaries, gazetteers).

# Prospects and Progress
| *Texts* | *Status* |
|:--- | ------:|
| Total in the Collection | 10,395 |
| Unique texts | 7,793 |
| Scheduled texts __*__  | 340 |
| Scheduled top priority | 237 |
| To be rechecked | 251 |
| Excluded __**__ | 557 |
| Added texts (listed below) | 300 |
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

## List of books by centuries (300 titles)

* **0100AH [[ [Re]generated on 2016-04-07 (08:25:57) ]]**

    * _no texts at the moment_

* **0200AH [[ [Re]generated on 2016-04-07 (08:25:57) ]]**

    * _no texts at the moment_

* **0300AH [[ [Re]generated on 2016-04-07 (08:25:57) ]]**

    * `0230IbnSacd.TabaqatKubra (TAGS: BIO,COL)`
    * `0231IbnSallamJumahi.TabaqatFuhulShucara (TAGS: ...)`
    * `0233YahyaIbnMacin.MinKalamFiRijal (TAGS: ...)`
    * `0233YahyaIbnMacin.TarikhIbnMacin (TAGS: ...)`
    * `0234AbuHasanSacdi.TasmiyaManRuwiya  (TAGS: ...)`
    * `0240KhalifaIbnKhayyat.Tabaqat (TAGS: ...)`
    * `0240KhalifaIbnKhayyat.Tarikh (TAGS: ...)`
    * `0241IbnHanbal.AsamiWaKuna (TAGS: ...)`
    * `0249Azraqi.AkhbarMakka (TAGS: ...)`
    * `0256Bukhari.DucafaSaghir (TAGS: HAD,BIO)`
    * `0256Bukhari.TarikhKabir (TAGS: ...)`
    * `0256Bukhari.TarikhSaghir (TAGS: ...)`
    * `0257IbnCabdHakam.FutuhMisr (TAGS: ...)`
    * `0259IbnYacqubJuzjani.AhwalRijal (TAGS: ...)`
    * `0261AbuHasanCijli.MacrifaThiqat (TAGS: ...)`
    * `0261Muslim.KunaWaAsma (TAGS: ...)`
    * `0261Muslim.Munfaridat (TAGS: ...)`
    * `0262AbuZaydNumayri.TarikhMadina (TAGS: ...)`
    * `0272Fakihi.AkhbarMakka (TAGS: ...)`
    * `0277AbuHatimRazi.JarhWaTacdil (TAGS: ...)`
    * `0277IbnSyfyanFasawi.MacrifaWaTarikh (TAGS: ...)`
    * `0279Baladhuri.AnsabAshraf (TAGS: GEN)`
    * `0279Baladhuri.FutuhBuldan (TAGS: ...)`
    * `0281AbuZurcaDimashqi.Tarikh (TAGS: ...)`
    * `0292Bahshal.TarikhWasit (TAGS: ...)`
    * `0292Yacqubi.TarikhYacqubi (TAGS: ...)`
    * `0300IbnKhurdadhbih.MasalikWaMamalik (TAGS: GEO)`

* **0400AH [[ [Re]generated on 2016-04-07 (08:25:57) ]]**

    * `0301Bardiji.TabaqatAsma (TAGS: ...)`
    * `0303Nasai.DucafaWaMatrukin (TAGS: ...)`
    * `0303Nasai.FadailSahaba (TAGS: ...)`
    * `0303Nasai.Tabaqat (TAGS: ...)`
    * `0303Nasai.TasmiyaFuqaha (TAGS: ...)`
    * `0303Nasai.TasmiyaManLamYarwi (TAGS: ...)`
    * `0306IbnHayyanDabbi.AkhbarQudat (TAGS: ...)`
    * `0310IbnAhmadDulabi.KunaWaAsma (TAGS: ...)`
    * `0310Tabari.Tarikh (TAGS: CHR)`
    * `0322AbuJacfarCuqayli.DucafaKabir (TAGS: ...)`
    * `0346Istakhri.MasalikWaMamalik (TAGS: GEO)`
    * `0346Mascudi.MurujDhahab (TAGS: ...)`
    * `0347IbnYunusSadafi.Tarikh (TAGS: ...)`
    * `0351IbnQanic.MucjamSahaba (TAGS: ...)`
    * `0354IbnHibban.Majruhin (TAGS: ...)`
    * `0354IbnHibban.MashahirCulamaAmsar (TAGS: ...)`
    * `0354IbnHibban.Thiqat (TAGS: ...)`
    * `0355AbuFarajIsbahani.Aghani (TAGS: ...)`
    * `0355MuhammadKindi.FadailMisr (TAGS: ...)`
    * `0355MuhammadKindi.WulatMisr (TAGS: BIO,COL)`
    * `0360Tabarani.MucjamKabir (TAGS: HAD,COLL)`
    * `0365IbnCadiJurjani.AsamiManRawaCanhum (TAGS: ...)`
    * `0365IbnCadiJurjani.KamilFiDucafa (TAGS: ...)`
    * `0369IbnHayyanAnsari.TabaqatMuhaddithin (TAGS: ...)`
    * `0374AbuFathAzdi.Makhzun (TAGS: HAD,...)`
    * `0374IbnHusaynAzdi.AsmaManYucrafBiKunya (TAGS: ...)`
    * `0379MuhammadRabci.TarikhMawlidCulama (TAGS: BIO,COL)`
    * `0385Daruqutni.DhikrAsmaTabicin (TAGS: ...)`
    * `0385Daruqutni.Sualat (TAGS: ...)`
    * `0385IbnNadim.Fihrist (TAGS: BIB)`
    * `0385IbnShahin.AsmaThiqat (TAGS: ...)`
    * `0390Muqaddasi.AhsanTaqasim (TAGS: GEO)`
    * `0395IbnMandah.FathBab (TAGS: ...)`
    * `0398AbuNasrKalabadhi.HidayaWaIrshad (TAGS: ...)`
    * `0400IbnTahirMaqdisi.BadWaTarikh (TAGS: ...)`

* **0500AH [[ [Re]generated on 2016-04-07 (08:25:57) ]]**

    * `0403IbnFaradi.TarikhCulamaAndalus (TAGS: ...)`
    * `0405AbuFadlHarawi.MucjamFiMushtabah (TAGS: ...)`
    * `0412Sulami.TabaqatSufiya (TAGS: ...)`
    * `0421Miskawayh.Tajarib (TAGS: ...)`
    * `0427HamzaJurjani.TarikhJurjan (TAGS: ...)`
    * `0428IbnManjuwayhIsbahani.RijalSahihMuslim (TAGS: ...)`
    * `0429AbuMansurThacalibi.YatimaDahr (TAGS: ...)`
    * `0430AbuNucaymIsbahani.DhikrManIsmuhuShucba (TAGS: ...)`
    * `0430AbuNucaymIsbahani.Ducafa (TAGS: ...)`
    * `0430AbuNucaymIsbahani.HilyaAwliya (TAGS: ...)`
    * `0430AbuNucaymIsbahani.MacrifaSahaba (TAGS: ...)`
    * `0430AbuNucaymIsbahani.TarikhIsbahan (TAGS: ...)`
    * `0446AbuYaclaKhalili.IrshadFiMacrifaCulama (TAGS: ...)`
    * `0456IbnHazm.AsmaKhulafa (TAGS: ...)`
    * `0456IbnHazm.FadailAndalus (TAGS: ...)`
    * `0456IbnHazm.JamharaAnsab (TAGS: ...)`
    * `0458Bayhaqi.DalailNubuwwa (TAGS: DHB)`
    * `0463IbnCabdBarr.IsticabFiMacrifaAshab (TAGS: BIO,COL)`
    * `0463KhatibBaghdadi.GhunyaMultamis  (TAGS: ...)`
    * `0463KhatibBaghdadi.MuttafiqWaMuftariq (TAGS: ...)`
    * `0463KhatibBaghdadi.TarikhBaghdad (TAGS: BIO,COL,DHB)`
    * `0466CabdAzizKattani.DhaylTarikhMawlidCulama (TAGS: ...)`
    * `0474IbnKhalafBaji.TacdilWaTakhrij (TAGS: ...)`
    * `0475IbnMakula.IkmalFiRafcIrtiyab (TAGS: ...)`
    * `0475IbnMakula.TahdhibMustamirr (TAGS: ...)`
    * `0476AbuIshaqShirazi.TabaqatFuqaha (TAGS: BIO,COL)`
    * `0482AbuIshaqHabbal.WafayatMisriyyin (TAGS: ...)`
    * `0487AbuCubaydBakri.MasalikWaMamalik (TAGS: GEO)`
    * `0488IbnFutuhHumaydi.JadhwaMuqtabis (TAGS: ...)`

* **0600AH [[ [Re]generated on 2016-04-07 (08:25:57) ]]**

    * `0507AbuBakrShashi.HilyaCulama (TAGS: ...)`
    * `0507IbnQaysarani.AnsabMuttafiqa`
    * `0521IbnAbiYacla.TabaqatHanabila (TAGS: BIO,COL)`
    * `0524IbnAkfani.DhaylDhaylTarikhMawlidCulama (TAGS: ...)`
    * `0541IbnCatiyyaMuharibi.Fahrasa (TAGS: ...)`
    * `0542IbnBassamShantarini.Dhakhira (TAGS: ...)`
    * `0544CiyadIbnMusaYahsubi.TartibMadarik (TAGS: BIO,COL)`
    * `0561Samcani.Ansab (TAGS: ONO,COL,DHB)`
    * `0561Samcani.Muntakhab (TAGS: ...)`
    * `0561Samcani.Tahbir (TAGS: ...)`
    * `0565IbnZaydBayhaqi.LubabAnsab (TAGS: ...)`
    * `0565IbnZaydBayhaqi.TarikhBayhaq (TAGS: ...)`
    * `0571IbnCasakir.MucjamShuyukh (TAGS: ...)`
    * `0571IbnCasakir.TarikhDimashq (TAGS: BIO,COL)`
    * `0575IbnKhayrIshbili.Fahrasa (TAGS: ...)`
    * `0576IbnMuhammadSilafi.MucjamSafar (TAGS: BIO,COL)`
    * `0578IbnBashkuwal.Sila (TAGS: BIO,COL)`
    * `0597CimadDinKatib.BarqShami (TAGS: ...)`
    * `0597CimadDinKatib.KharidaQasr (TAGS: POE,COL)`
    * `0597IbnJawzi.DucafaWaMatrukin (TAGS: ...)`
    * `0597IbnJawzi.Muntazam (TAGS: BIO,COL,CHR,DHB)`
    * `0597IbnJawzi.SifaSafwa (TAGS: BIO,COL)`
    * `0599IbnYahyaDabbi.BughyaMultamis (TAGS: ...)`

* **0700AH [[ [Re]generated on 2016-04-07 (08:25:57) ]]**

    * `0623Qazwini.Tadwin (TAGS: ...)`
    * `0626YaqutHamawi.MucjamBuldan (TAGS: GEO,COL)`
    * `0626YaqutHamawi.MucjamUdaba (TAGS: BIO,COL,POE)`
    * `0629IbnNuqta.TakmilaIkmal (TAGS: ...)`
    * `0629IbnNuqta.TaqyidLiMacrifa (TAGS: BIO,COL)`
    * `0630IbnAthirCizzDin.Kamil (TAGS: CHR)`
    * `0630IbnAthirCizzDin.LubabFiTahdhibAnsab (TAGS: ONO,COL)`
    * `0630IbnAthirCizzDin.UsdGhaba (TAGS: ...)`
    * `0637IbnMustafwi.TarikhIrbil (TAGS: ...)`
    * `0641Sarifini.Muntakhab (TAGS: ...)`
    * `0642IbnNajjar.DhaylTarikhBaghdad (TAGS: BIO,COL)`
    * `0643IbnSalahShahrazuri.TabaqatFuqaha (TAGS: BIO,COL)`
    * `0646.IbnQifti.IkhbarCulama (TAGS: ...)`
    * `0646IbnQifti.InbahRuwat (TAGS: ...)`
    * `0646IbnQifti.Muhammadun (TAGS: ...)`
    * `0647CabdWahidMarrakushi.Mucjib (TAGS: ...)`
    * `0658IbnAbbar.HullaSiyara (TAGS: ...)`
    * `0658IbnAbbar.TakmilaLiSila (TAGS: BIO,COL)`
    * `0659SainDinNaccal.Mashyakha (TAGS: ...)`
    * `0660IbnCadim.BughyatTalib (TAGS: ...)`
    * `0660IbnCadim.ZubdaHalab (TAGS: ...)`
    * `0665AbuShama.Rawdatayn (TAGS: ...)`
    * `0668IbnAbiUsaybica.CuyunAnba (TAGS: BIO,COL)`
    * `0680IbnSabuni.TakmilaIkmalIkmal (TAGS: ONO,...)`
    * `0681IbnKhallikan.WafayatAcyan (TAGS: BIO,COL,DHB)`
    * `0684IbnShaddad.AclaqKhatira (TAGS: ...)`
    * `0685IbnCibri.TarikhMukhtasarDuwal (TAGS: ...)`
    * `0685IbnSacidMaghribi.Mughrib (TAGS: ...)`
    * `0694MuhibbDinTabari.Dhakhair (TAGS: ...)`
    * `0694MuhibbDinTabari.RiyadNadira`
    * `0696Dabbagh.MacalimIman (TAGS: NOT,BIO,COL)`

* **0800AH [[ [Re]generated on 2016-04-07 (08:25:57) ]]**

    * `0703Marakishi.DhaylWaTakmila (TAGS: ...)`
    * `0711IbnManzurIfriqi.MukhtasarTarikhDimashq (TAGS: BIO,COL)`
    * `0726Yunini.DhaylMiratZaman (TAGS: CHR,BIO,COL)`
    * `0732AbuFida.MukhtasarFiAkhbar (TAGS: ...)`
    * `0732IbnYacqubJanadi.SulukFiTabaqat (TAGS: BIO,COL)`
    * `0733Nuwayri.NihayaArab (TAGS: ...)`
    * `0742Mizzi.TahdhibKamal (TAGS: DHB)`
    * `0748Dhahabi.CibarFiKhabar (TAGS: CHR)`
    * `0748Dhahabi.DhaylCibar (TAGS: ...)`
    * `0748Dhahabi.DhaylDiwanDucafa (TAGS: ...)`
    * `0748Dhahabi.DhikrAsmaManTakallama (TAGS: DHB)`
    * `0748Dhahabi.DiwanDucafa (TAGS: ...)`
    * `0748Dhahabi.Kashif (TAGS: ...)`
    * `0748Dhahabi.MacrifaQurraKibar (TAGS: BIO,COL)`
    * `0748Dhahabi.MizanIctidal (TAGS: ...)`
    * `0748Dhahabi.MucinFiTabaqatMuhaddithin (TAGS: ...)`
    * `0748Dhahabi.MucjamMuhaddithin  (TAGS: ...)`
    * `0748Dhahabi.MucjamShuyukh (TAGS: BIO,COL)`
    * `0748Dhahabi.MughniFiDucafa (TAGS: DHB)`
    * `0748Dhahabi.MukhtasarMinDubaythi (TAGS: ...)`
    * `0748Dhahabi.Muqtana (TAGS: DHB)`
    * `0748Dhahabi.RuwatThiqat (TAGS: DHB)`
    * `0748Dhahabi.SiyarAclamNubala (TAGS: BIO,COL,DHB)`
    * `0748Dhahabi.TadhkiraHuffaz (TAGS: BIO,COL)`
    * `0748Dhahabi.TarikhIslam (TAGS: BIO,COL,CHR,DHB)`
    * `0748IbnDimyati.Mustafad (TAGS: ...)`
    * `0749IbnWardi.Tarikh (TAGS: ...)`
    * `0749Wadiashi.Barnamaj (TAGS: BIB)`
    * `0761IbnKaykaldi.JamicTahsil (TAGS: ...)`
    * `0762MughaltayIbnQalij.IkmalTahdhib (TAGS: ...)`
    * `0764IbnShakirKutubi.FawatWafayat (TAGS: ...)`
    * `0764Safadi.AcyanCasr (TAGS: BIO,COL)`
    * `0764Safadi.NaktHimyan (TAGS: ...)`
    * `0764Safadi.WafiBiWafayat (TAGS: BIO,COL)`
    * `0765AbuMahasinHusayni.DhaylTadhkira (TAGS: ...)`
    * `0765AbuMahasinHusayni.IkmalLiRijal (TAGS: ...)`
    * `0767Balawi.TajMafriq (TAGS: ...)`
    * `0768Yafici.MiratJanan (TAGS: ...)`
    * `0771Subki.MucjamShuyukh (TAGS: ...)`
    * `0771Subki.TabaqatShaficiyaKubra (TAGS: BIO,COL)`
    * `0774IbnKathir.Bidaya (TAGS: BIO,COL,CHR)`
    * `0774IbnKathir.TabaqatShaficiyyin (TAGS: BIO,COL)`
    * `0774IbnRaficSallami.Wafayat (TAGS: ...)`
    * `0775IbnAbiWafa.JawahirMudiya (TAGS: BIO,COL)`
    * `0776LisanDinIbnKhatib.Ihata (TAGS: ...)`
    * `0793AbuHasanMalaqi.TarikhQudat (TAGS: ...)`
    * `0795IbnRajabHanbali.DhaylTabaqatHanabila (TAGS: BIO,COL)`
    * `0799IbnFarhun.DibajMudhahhab (TAGS: ...)`

* **0900AH [[ [Re]generated on 2016-04-07 (08:25:57) ]]**

    * `0804IbnMulaqqin.TabaqatAwliya (TAGS: ...)`
    * `0808IbnKhaldun.Tarikh (TAGS: CHR)`
    * `0809IbnQunfudh.Wafayat (TAGS: ...)`
    * `0812CaliKhazraji.CuqudLuluiyya (TAGS: ...)`
    * `0817IbnYacqubFiruzabadi.BulghaFiTarajim (TAGS: ...)`
    * `0826IbnCiraqi.TuhfaTahsil (TAGS: ...)`
    * `0832AbuTayyibFasi.DhaylTaqyid (TAGS: ...)`
    * `0832AbuTayyibFasi.ShifaGharam (TAGS: ...)`
    * `0833IbnJazari.GhayaNihaya (TAGS: ...)`
    * `0842IbnNasirDinDimashqi.TawdihMushtabih (TAGS: ...)`
    * `0845Maqrizi.IqazHunafa (TAGS: ...)`
    * `0845Maqrizi.Mawaciz (TAGS: ...)`
    * `0845Maqrizi.MukhtasarKamil (TAGS: ...)`
    * `0845Maqrizi.Suluk (TAGS: ...)`
    * `0851IbnQadiShuhba.TabaqatShaficiya (TAGS: BIO,COL)`
    * `0852IbnHajarCasqalani.DurarKamina (TAGS: BIO,COL)`
    * `0852IbnHajarCasqalani.InbaGhumr (TAGS: ...)`
    * `0852IbnHajarCasqalani.IsabaFiTamyiz (TAGS: ...)`
    * `0852IbnHajarCasqalani.ItharBiMacrifa`
    * `0852IbnHajarCasqalani.LisanMizan (TAGS: BIO,COL)`
    * `0852IbnHajarCasqalani.NuzhaAlbab (TAGS: ...)`
    * `0852IbnHajarCasqalani.RafcCisr (TAGS: ...)`
    * `0852IbnHajarCasqalani.TabaqatMudallisin (TAGS: BIO,COL)`
    * `0852IbnHajarCasqalani.TacjilManfaca (TAGS: ...)`
    * `0852IbnHajarCasqalani.TahdhibTahdhib (TAGS: ...)`
    * `0852IbnHajarCasqalani.TaqribTahdhib (TAGS: ...)`
    * `0855Cayni.CiqdJuman (TAGS: ...)`
    * `0855Cayni.CumdaQari (TAGS: ...)`
    * `0855Cayni.MaghaniAkhyar (TAGS: ...)`
    * `0871IbnFahdMakki.LahzAlhaz (TAGS: BIO,...)`
    * `0874IbnTaghribirdi.ManhalSafi (TAGS: ...)`
    * `0874IbnTaghribirdi.MawridLatafa (TAGS: ...)`
    * `0874IbnTaghribirdi.NujumZahira (TAGS: ...)`
    * `0879IbnQutlubugha.TajTarajim (TAGS: ...)`
    * `0879IbnQutlubugha.Thiqat (TAGS: ...)`
    * `0881SibtIbnCajami.KashfHathith (TAGS: ...)`
    * `0884IbnMuflih.MaqsidArshad (TAGS: ...)`
    * `0884SibtIbnCajami.Ightibat (TAGS: ...)`
    * `0884SibtIbnCajami.KunuzDhahab (TAGS: ...)`
    * `0884SibtIbnCajami.TabyinLiAsma (TAGS: ...)`
    * `0900AbuCabdAllahHimyari.RawdMictar (TAGS: GEO,COL)`

* **1000AH [[ [Re]generated on 2016-04-07 (08:25:57) ]]**

    * `0902Sakhawi.DuLamic (TAGS: BIO,COL)`
    * `0902Sakhawi.TuhfaLatifa (TAGS: ...)`
    * `0904Burayhi.TabaqatSulahaYaman (TAGS: ...)`
    * `0905Basrawi.Tarikh (TAGS: ...)`
    * `0909IbnMibradHanbali.MucjamKutub (TAGS: BIB,...)`
    * `0911Suyuti.AsmaMukhadramin (TAGS: ...)`
    * `0911Suyuti.BughyaWucat (TAGS: BIO,COL)`
    * `0911Suyuti.DhaylTabaqatHuffaz (TAGS: ...)`
    * `0911Suyuti.HusnMuhadara (TAGS: ...)`
    * `0911Suyuti.IscafMubatta (TAGS: ...)`
    * `0911Suyuti.LubbLubab (TAGS: ...)`
    * `0911Suyuti.NazmCiqyan (TAGS: ...)`
    * `0911Suyuti.RihNisrin (TAGS: ...)`
    * `0911Suyuti.TabaqatHuffaz (TAGS: BIO,COL)`
    * `0911Suyuti.TabaqatMufassirin (TAGS: ...)`
    * `0911Suyuti.TarikhKhulafa (TAGS: ...)`
    * `0923IbnCabdAllahKhazraji.KhulasaTahdhib (TAGS: ...)`
    * `0927Culaymi.UnsJalil (TAGS: ...)`
    * `0927Nucaymi.DarisFiMadaris (TAGS: COL)`
    * `0929IbnKayyal.KawakibNayyirat (TAGS: ...)`
    * `0945ShamsDinDawudi.TabaqatMufassirin (TAGS: ...)`
    * `0968Tashkubruizadah.ShaqaiqNucmaniyya (TAGS: BIO,COL)`
    * `0973CabdWahhabShacrani.LawaqihAnwar (TAGS: ...)`

* **1100AH [[ [Re]generated on 2016-04-07 (08:25:57) ]]**

    * `1010TamimiDari.TabaqatSaniya (TAGS: BIO,COL)`
    * `1037CabdQadirCaydarus.TarikhNurSafir (TAGS: ...)`
    * `1041Maqarri.NafhTib (TAGS: ...)`
    * `1051Cimadi.RawdaRayya (TAGS: ...)`
    * `1061NajmDinGhazzi.KawakibSaira (TAGS: ...)`
    * `1067HajjiKhalifa.KashfZunun (TAGS: BIB,COL)`
    * `1078RiyadZadah.AsmaKutub (TAGS: BIB)`
    * `1089IbnCimad.Shadharat (TAGS: BIO,COL,CHR)`
    * `1100IbnMuhammadAdnahwi.TabaqatMufassirin (TAGS: ...)`

* **1200AH [[ [Re]generated on 2016-04-07 (08:25:57) ]]**

    * `1111MuhammadAminMuhibbi.KhulasaAthr (TAGS: ...)`
    * `1120CaliKhanMadani.DarajatRafica (TAGS: SHC,...)`

* **1300AH [[ [Re]generated on 2016-04-07 (08:25:57) ]]**

    * `1206Muradi.SilkDurar (TAGS: ...)`
    * `1212BahrCulum.FawaidRijaliya (TAGS: SHC)`
    * `1232IbnKhatibCumari.RawdaFayha (TAGS: ...)`
    * `1237Jabarti.CajaibAthar (TAGS: ...)`
    * `1250IbnCaliShaykani.BadrTalic (TAGS: ...)`
    * `1269CabdMalikCasimi.SamtNujum (TAGS: ...)`
    * `1286IcjazHusaynKunturi.KashfHajb (TAGS: BIB)`

* **1400AH [[ [Re]generated on 2016-04-07 (08:25:57) ]]**

    * `1307Qannawji.AbjadCulum (TAGS: ...)`
    * `1307Qannawji.HittaFiDhikr (TAG: BIB,...)`
    * `1307Qannawji.LuqtaCajlan (TAGS: BIB,...)`
    * `1313VanDyck.IktifaQunuc (TAGS: ...)`
    * `1315Salawi.IstiqsaLiAhkbar (TAGS: ...)`
    * `1318MuhammadSanusi.Musamarat (TAGS: ...)`
    * `1335CabdRazzaqBaytar.HilyaBashar (TAGS: ...)`
    * `1338MuhammadFaridBey.Tarikh (TAGS: ...)`
    * `1339IsmacilBashaBaghdadi.HadiyaCarifin (TAGS: BIO,BIB,COL)`
    * `1339IsmacilBashaBaghdadi.IdahMaknun (TAGS: BIB,COL)`
    * `1341CabdHayyTalibi.IclamBiMan (TAGS: ...)`
    * `1345IbnJacfarKattani.RisalaMustatrafa`
    * `1351IbnHusaynGhazzi.NahrDhahab (TAGS: ...)`
    * `1360IbnQasimMakhluf.ShajaraNur (TAGS: BIO,COL)`
    * `1368HasanAmin.MustadrakatAcyanShica (TAGS: ...)`
    * `1371MuhsinCamili.AcyanShica (TAGS: ...)`
    * `1381MuhammadSancani.MulhaqBadr (TAGS: ...)`
    * `1383CadbHayyKattani.FihrisFaharis (TAGS: BIB)`
    * `1389AghaBuzurgTihrani.DharicaFiTasanifShica (TAGS: BIB)`
    * `1389AghaBuzurgTihrani.DhaylKashfZunun (TAGS: BIB)`
    * `1389AghaBuzurgTihrani.TASHAnwarSatica (TAGS: ...)`
    * `1389AghaBuzurgTihrani.TASHNawabighRuwat (TAGS: ...)`

* **1500AH [[ [Re]generated on 2016-04-07 (08:25:57) ]]**

    * `1411SayyidKhui.MucjamRijal (TAGS: ...)`
    * `1418SalihAhmadArkani.TihfaMajalis (TAGS: BIB)`
    * `1450MuhammadSancani.NaylWatar (TAGS: NOT,BIO,COL)`
