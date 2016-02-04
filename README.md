# OpenArabic Project (@ AvH Lehrstuhl für Digital Humanities, U Leipzig)

Arabic texts from different periods, collected and reformatted into machine-readable formats (mARkdown > CTS-compliant TEI XML > Perseus DL)

# List of added books (45 at the moment)

Mostly premoderns chronicles, biographical collections, encyclopaedic dictionaries, gazetteers.

[Ordered by the number of date statements (descending): with the assumption that texts with a lot of date statements are historical texts]* 0902Sakhawi.DuLamic* 0748Dhahabi.TarikhIslam* 0571IbnCasakir.TarikhDimashq* 0463KhatibBaghdadi.TarikhBaghdad* 0764Safadi.WafiBiWafayat* 1067HajjiKhalifa.KashfZunun* 0748Dhahabi.SiyarAclamNubala* 1339IsmacilBashaBaghdadi.HadiyaCarifin* 1339IsmacilBashaBaghdadi.IdahMaknun* 0561Samcani.Ansab* 0733Nuwayri.NihayaArab* 0711IbnManzurIfriqi.MukhtasarTarikhDimashq* 1089IbnCimad.Shadharat* 0764Safadi.AcyanCasr* 0874IbnTaghribirdi.NujumZahira* 0762MughaltayIbnQalij.IkmalTahdhib* 0681IbnKhallikan.WafayatAcyan* 0874IbnTaghribirdi.ManhalSafi* 0845Maqrizi.Mawaciz* 0902Sakhawi.TuhfaLatifa* 0630IbnAthirCizzDin.LubabFiTahdhibAnsab* 0597IbnJawzi.Muntazam* 0927Nucaymi.DarisFiMadaris* 1111MuhammadAminMuhibbi.KhulasaAthr* 0774IbnKathir.Bidaya* 0660IbnCadim.BughyatTalib* 0630IbnAthirCizzDin.Kamil* 0833IbnJazari.GhayaNihaya* 0911Suyuti.HusnMuhadara* 0623Qazwini.Tadwin* 0658IbnAbbar.TakmilaLiSila* 0748Dhahabi.MukhtasarMinDubaythi* 0771Subki.TabaqatShaficiyaKubra* 0775IbnAbiWafa.JawahirMudiya* 1061NajmDinGhazzi.KawakibSaira* 0578IbnBashkuwal.Sila* 1206Muradi.SilkDurar* 0851IbnQadiShuhba.TabaqatShaficiya* 0748Dhahabi.CibarFiKhabar* 0732IbnYacqubJanadi.SulukFiTabaqat* 0230IbnSacd.TabaqatKubra* 0795IbnRajabHanbali.DhaylTabaqatHanabila* 0544CiyadIbnMusaYahsubi.TartibMadarik* 0642IbnNajjar.DhaylTarikhBaghdad* 0521IbnAbiYacla.TabaqatHanabila

# Priorities

* 0230IbnSacd.TabaqatKubra* 0463KhatibBaghdadi.TarikhBaghdad* 0521IbnAbiYacla.TabaqatHanabila* 0544CiyadIbnMusaYahsubi.TartibMadarik* 0578IbnBashkuwal.Sila* 0597IbnJawzi.Muntazam* 0630IbnAthirCizzDin.Kamil* 0630IbnAthirCizzDin.LubabFiTahdhibAnsab* 0642IbnNajjar.DhaylTarikhBaghdad* 0658IbnAbbar.TakmilaLiSila* 0660IbnCadim.BughyatTalib* 0681IbnKhallikan.WafayatAcyan* 0711IbnManzurIfriqi.MukhtasarTarikhDimashq* 0732IbnYacqubJanadi.SulukFiTabaqat* 0748Dhahabi.CibarFiKhabar* 0748Dhahabi.MukhtasarMinDubaythi* 0748Dhahabi.SiyarAclamNubala* 0764Safadi.AcyanCasr* 0764Safadi.WafiBiWafayat* 0771Subki.TabaqatShaficiyaKubra* 0774IbnKathir.Bidaya* 0775IbnAbiWafa.JawahirMudiya* 0795IbnRajabHanbali.DhaylTabaqatHanabila* 0833IbnJazari.GhayaNihaya* 0851IbnQadiShuhba.TabaqatShaficiya* 0874IbnTaghribirdi.NujumZahira* 0911Suyuti.HusnMuhadara* 0927Nucaymi.DarisFiMadaris* 1061NajmDinGhazzi.KawakibSaira* 1067HajjiKhalifa.KashfZunun* 1089IbnCimad.Shadharat* 1111MuhammadAminMuhibbi.KhulasaAthr* 1206Muradi.SilkDurar* 1339IsmacilBashaBaghdadi.IdahMaknun

# Building a CTS-compliant corpus

- `data` has subfolders by authors, which have subfolders by titles
- each title subfolder has `PDF` subfolder:
	- **urls.txt**: includes links to PDFs of a book (usually on archive.org)
	- on Mac/Linux all PDFs can be downloaded by typing `make` in Terminal/CommandLine
	- on Windows: `wget` must be installed; then run `wget -i urls.txt`
	- to save space, PDFs are ignored in this GitHub repository 
	- if you find new PDFs, add urls (one per line) to **urls_additional.txt**
