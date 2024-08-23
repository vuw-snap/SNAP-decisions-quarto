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
git clone https://github.com/vuw-snap/SNAP-decisions.git <br>
clone SNAP-decisions-quarto  <br>
git clone https://github.com/vuw-snap/SNAP-decisions-quarto.git <br>
alter the files in SNAP-decisions-quarto with your editor <br>
from within the quarto directory type <br>
quarto render (to produce the html) <br>
quarto preview (to produce a preview in your browser)<br>
<br>
NOTE:the html will be in directory "../SNAP-decisions" unless you point to another directory in _quarto.yml, you will want to change the following line in _quarto.yml<br>
output-dir: ../SNAP-decisions <br>
<br>
check that you like everything, if not make further changes in the quarto directory and visualise using preview <br>
once you are happy, send everything back to github <br>
for example from inside SNAP-decisions do the standard git stuff <br>
git init <br>
git add --all <br>
git commit -m "add multiple files" <br>
git push https://github.com/vuw-snap/SNAP-decisions-quarto.git main <br>
don't forget to repeat for SNAP-decision files!<br>
