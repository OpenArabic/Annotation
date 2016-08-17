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
			* after you changed/added files, run `git add .` (pediod/punkt/point at the end); this command adds all new files to the repository
			* `git commit -m "MESSAGE"` saves the current status of the repository to the git versioning system; MESSAGE contains your own human readable description of what you have done. For example, if you finished tagging 3 volumes in the book that has 10, you can do `git commit -m "Finished tagging first 3 volumes"`. These messages will be visible in github repository online and help tracking progress. Also, you can roll back to the committed stage, if something wrong goes with the repository.
			* `git push origin master` will upload your changes to the online repository. If somebody else has already updated the same repository, you may need to run `git pull origin master`.  
1. Clone repositories.
2. Work from earliest to latest.
3. Make sure that nobody else is editing the text that you chose; to avoid that keep me posted on text you are planning to work with. (**NB**: if there is a file with extension `.mARkdown`, it means that somebody is working on that text!)
4. In most cases there are multiple versions of the same text; you need to identify relevant editions and do a preliminary evaluation.
5. Ideally,  you should be able to find a text that corresponds to an edition,  which you can access (scans of most editions can be found online; links to some editions can be found in the PDF folder in text repositories; if there are links in `urls.txt`, they can be downloaded in batch using `wget`). 
6. It is likely that there will be more than one text based on the same edition. `Shamela` texts are often improved versions of `JK` texts (with more tags already in place);  it makes sense to compare the number of tags already in place and choose the text that will require less time to finish. Keep in mind that there is no solid rule about which text is likely to be better; you need to evaluate them all.
7. Only one text should be converted into `mARkdown`—the text that according to your evaluation is of better/best available quality. Make sure to record your observations on each text file into a `README.md` file in the folder with the text group you are working on (answer the questions that are in the `README.md` file).
 		* **NB**: If your research focuses on specific texts, you may want having multiple editions converted into `mARkdown`; this will allow to compare how editions are different from each other.
8. When you selected the text that you will be converting to `mARkdown`, work with the copy of that text file. The file name of that copy should retain the `URI` + `.mARkdown` (period + mARkdown,  where the second and third letters are capitalized!). For example, `0310Tabari.Tarikh.JK000157-ara1` > `0310Tabari.Tarikh.JK000157-ara1.mARkdown`
		* **NB** by default, Windows hides file extensions, so you will need to change some settings so that they are displayed. *How to do that*: 1) Open `File explorer` (Win+E); 2) press `F10` to see the menu; 3) in the menu: `Tools` > `Folder options`; then choose tab `View`; then uncheck `Hide extensions for known file types`; 4) Click `Apply to Folders`, then `Ok`.
9. Keep in mind that you need to tag only the structure of a book you are working with,  which includes tagging chapter headers (`### |`, `### ||`, `### |||`, etc.) and major information units, like biographies (`### $`, `### $$`, `### $$$`, etc.) or lexicon items (these we should discuss before you start). Please, do not tag anything else—at least without consulting first with me.
10. **NB!** Do not delete anything from the text! At this point we do not know what is valuable and what is not (things like numbers, random characters, punctuation, stray HTML tags, etc.). Your goal is **to provide the structure** to texts, **not to edit** them. If you think something should be deleted, please, consult me first. Time is the most valuable asset at the moment and we cannot afford to spend it on fixing messed-up texts; we want to invest it into tagging new texts.
10. Make commits to relevant github repositories after each working session. In addition to saving/backing up your work, this will also allow me to check periodically on your progress and make suggestions along the way.
11. In the same `README.md` file add the number of hours it took you to process the file. We are trying to get estimates on how much time it is going to take to process the entire corpus; we also know at the moment that the amount of time is not proportional to the length of a text, since what matters most is how much structural information is preserved in the initial file and that differs drastically from text to text.

These are the major steps.  Please, do not hesitate to contact the me if you have any questions, no matter how insignificant they may seem to you.

