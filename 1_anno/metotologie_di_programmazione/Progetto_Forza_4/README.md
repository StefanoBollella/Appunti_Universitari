# Come compilare ed eseguire il progetto Forza 4 su console

Dato l'elevato numero di file sorgente da compilare viene utilizzata l'opzione 
@filename sulla riga di comando. 
È stato creato un file apposito che elenca tutti i nomi dei file sorgente da compilare, chiamato argumentFiles.txt presente nella cartella del progetto.
Questo file viene passato nell'opzione di input per javac.

1) Occorre posizionarsi nella directory del progetto Forza4 e eseguire il comando: 
  
    javac -d build @argumentFiles.txt

2) successivamente bisogna spostarsi nella cartella build del progetto.

Dopo aver compilato tutti i file necessari occorre creare un file jar.
Al momento della sua creazione bisogna indicare qual è il punto di ingresso dell'applicazione. Per questo motivo è stato creato un file Manifest.txt
con all'interno l'intestazione Main-Class: seguita dal nome della classe.
Il file è stato salvato all'interno della cartella build.

3) È possibile creare il file jar eseguendo il comando : 
    
    jar cfm forza4.jar Manifest.txt  *

4) successivamente è possibile lanciare l'applicazione.
  Passando come argomento sulla linea di comando  il percorso 
  assoluto del file di testo saveGames.txt presente all'interno della     
  cartella build, ecco un esempio : 
 
    java -jar forza4.jar  /User/Desktop/Forza_4/build/saveGames.txt 
 
 

