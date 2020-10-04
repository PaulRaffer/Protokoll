****************************************************************
* Protokoll-Template Anleitung                                 *
****************************************************************

Um ein Protokoll mit dem Protokoll-Template zu erstellen müssen Folgende Schritte durchgeführt werden:

1.) MiKTeX herunterladen und installieren:
	https://miktex.org/download

	Nun kann ein LaTeX-File mit dem Befehl pdflatex <Filename> zu einem PDF-File kompiliert werden.
	
2.) Notepad++ Shortcut einrichten
	* Notepad++ öffnen
	* Plugins/Plugins Admin... öffnen
	* Häkchen bei NppExec setzen
	* Install klicken
	* F6 drücken
	* Folgenden Text eingeben:
	
		cd "$(CURRENT_DIRECTORY)"
		pdflatex -output-directory "./out/" "$(FILE_NAME)"


	* Save... klicken
	* Script Name: "LaTeX" eingeben
	* Save
	
	Nun kann ein LaTeX-File durch drücken von F6 und danach Enter zu einem PDF-File kompiliert werden.
	
Die ersten beiden schritte müssen nur beim ersten Mal durchgeführt werden!
Schritt 3 muss jedes Mal gemacht werden wenn man ein Protokoll schreiben will.


3.) Protokoll erstellen

	* Wenn man das Template noch nicht auf seinem Rechner hat kann man es mit dem git Befehl
		git clone https://github.com/PaulRaffer/Protokoll.git
	herunterladen. (Nicht vergessen vorher mit cd <path> in den gewünschten Ordner zu wechseln)
	* File "LA_[Uebungsnummer] - [Uebungstitel]_[jjjj-mm-dd]_[Vorname] [Nachname], [Lfd.Nr.] [Klasse]_Protokoll_[Version].tex" umbenennen und eigene Daten statt [...] einsetzen.
	* Alle Files im Ordner "./src" in einem Editor (am beseten Notepad++) öffnen
	* Eigene Daten ins File "macros.tex" eintragen
	* Protokoll im File "content.tex" schreiben (LaTeX-Tutorial: https://www.latex-tutorial.com/tutorials/ )
	* Die Files "LA_[Uebungsnummer] - [Uebungstitel]_[jjjj-mm-dd]_[Vorname] [Nachname], [Lfd.Nr.] [Klasse]_Protokoll_[Version].tex" und "titlepage.tex" müssen im Normalfall nicht verändert werden
	  AUSSNAHME: Vor dem letzten Kompilieren muss das "%" am begin der Zeile 15 im File "titlepage.tex" entfernt werden. Dies inkludiert das HTL-Logo. Die Zeile ist auskommentiert, da das kompilieren sonst zu lange dauern würde
	* Messprotokoll einscannen und unter ./res/doc/Messprotokoll.pdf abspeichern ODER Zeile 33 in "macros.tex" und Zeile 53 in "content.tex" entfernen und das original Messprotokoll nach dem Ausdrucken zum Protokoll dazuheften
	* Inventarliste unter ./res/doc/Inventarliste.pdf abspeichern
	* File "LA_[Uebungsnummer] - [Uebungstitel]_[jjjj-mm-dd]_[Vorname] [Nachname], [Lfd.Nr.] [Klasse]_Protokoll_[Version].tex" kompilieren (Notepad++: F6 und danach ENTER klicken)
	
	FERTIG! Ein PDF-File ("LA_[Uebungsnummer] - [Uebungstitel]_[jjjj-mm-dd]_[Vorname] [Nachname], [Lfd.Nr.] [Klasse]_Protokoll_[Version].pdf") wurde generiert
	ACHTUNG! DIE SEITENZAHLEN STIMMEN NOCH NICHT! LÖSUNG: ZWEITES MAL KOMPILIEREN
	NUN STIMMEN DIE SEITENZAHLEN, BIS AUF DIE VOM ANHANG! LÖSUNG: DIE SEITENZAHLEN MÜSSEN MANUELL INM FILE
	"LA_[Uebungsnummer] - [Uebungstitel]_[jjjj-mm-dd]_[Vorname] [Nachname], [Lfd.Nr.] [Klasse]_Protokoll_[Version].toc"
	ANGEPASST WERDEN! (Dazu muss der Wert in den letzten geschwungenen Klammern der Zeile verändert werden)
	ANSCHLIESSEND MUSS DIE DATEI GESPEICHERT UND DAS PROTOKOLL NEU KOMPILIERT WERDEN
