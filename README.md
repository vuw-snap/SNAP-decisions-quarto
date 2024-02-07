the main depository for the VUW-SNAP website.<br>

we use Quarto to create the website documents <br>
https://quarto.org/docs/get-started/hello/text-editor.html <br>
https://quarto.org/docs/guide/ <br>

basic structure is <br>
_quarto.yml : sets out framework of website <br>
various xxx.qmd files contain markdown versions of the final .html files <br>
styles.css where you control some of formatting in the form of  <br>
the index.qmd file will be the opening page <br>

basic instructions: <br>
clone SNAP-decisions  <br>
clone SNAP-decisions-quarto  <br>
git clone git clone https://github.com/vuw-snap/SNAP-decisions.git <br>
git clone git clone https://github.com/vuw-snap/SNAP-decisions-quarto.git <br>
alter the files in SNAP-decisions-quarto with your editor <br>
from outside of your directory type  <br>
     quarto preview SNAP-decisions-quarto <br>
this will generate the html <br>
the html will be in directory "_site" only unless you point to another directory in _quarto.yml  <br>
for example I point to the SNAP-decisions directory by adding the following line in _quarto.yml <br>
output-dir: /Users/tricia/Documents/GitHub_snap/SNAP-decisions <br>
check that you like everything, if not make further changes in the quarto directory and visualise using preview <br>
once you are happy, send everything back to github <br>
for example from inside SNAP-decisions do the standard git stuff <br>
git init <br>
git add --all <br>
git commit -m "add multiple files" <br>
git push https://github.com/vuw-snap/SNAP-decisions.git main <br>
