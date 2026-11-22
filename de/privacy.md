---
title: Datenschutzerklärung von Budgetplaner
lang: de
---

# Datenschutzerklärung von Savings Challenge & Budget

*Dies ist eine Übersetzung. Weicht sie von der [englischen Fassung](../privacy) ab, ist die englische Fassung maßgeblich.*

Gültig ab: 2026-11-22

Diese Erklärung beschreibt, wie Savings Challenge & Budget (auf dem Home-Bildschirm „Budgetplaner“, die „App“), entwickelt von Stanislau Malchanau („wir“, „uns“), mit Ihren Informationen umgeht. Kurz gesagt: **Wir erheben, verkaufen oder teilen Ihre personenbezogenen Daten nicht. Ihr Budget bleibt auf Ihrem Gerät und in Ihrem eigenen iCloud-Account. Die App verwahrt und überweist kein Geld, ist mit keiner Bank verbunden und gibt keine Finanzberatung.**

## 1. Von der App gespeicherte Daten

Die App speichert Folgendes auf Ihrem Gerät: Ihre Ausgaben, Einnahmen und Erstattungen (den Betrag, seine Währung und den verwendeten Wechselkurs, die Kategorie, eine Notiz, Datum, Uhrzeit und Zeitzone sowie die Art, wie der Eintrag hinzugefügt wurde, zum Beispiel eingetippt, von einem Kassenbon oder über Apple Pay), Ihre Kategorien und deren Limits, Ihr Monatsbudget und seine Einstellungen (den Tag, an dem Ihr Monat beginnt, und ob der Rest übertragen wird), Ihre regelmäßigen Zahlungen, Ihre Sparziele mit dem, was Sie zurückgelegt und entnommen haben, Ihre Spar-Challenges, die Wechselkurse, die Sie selbst eingegeben haben, das gemeinsame Budget, das Sie mit einer von Ihnen eingeladenen Person führen (Abschnitt 3), Ihre Antworten auf die Fragen beim ersten Start und Ihre Einstellungen (die Uhrzeit der Erinnerung, die Face ID-Sperre, Töne und Vibration). Gelöschte Einträge bleiben 30 Tage lang unter „Zuletzt gelöscht“, damit Sie sie zurückholen können.

Diese Aufzeichnungen beschreiben, wie Sie Geld ausgeben und sparen, und manche Gesetze behandeln solche Informationen als finanzielle oder sensible Daten. Diese Daten verlassen nie Ihr Gerät und Ihren iCloud-Account (Abschnitte 2 und 3). Wir betreiben keine Server, die Ihre Aufzeichnungen empfangen, wir haben keinen Zugriff darauf, und die App sendet Ihre Einträge nie an einen Online-KI-Dienst oder an sonst jemanden. Der einzige kleine Server, den wir betreiben (Abschnitt 6), liefert Wechselkurse und signiert Rabattangebote; Ihre Aufzeichnungen erhält er nie.

## 2. iCloud-Synchronisierung

Wenn Sie bei iCloud angemeldet sind, synchronisiert die App Ihr Budget über CloudKit von Apple in der privaten Datenbank Ihres eigenen iCloud-Accounts, damit es auf einem neuen iPhone und nach einer Neuinstallation da ist. Diese Daten werden von Apple gemäß der Datenschutzrichtlinie von Apple (https://www.apple.com/legal/privacy/) gespeichert und geschützt. Wir können sie weder sehen noch lesen noch exportieren. Wenn sich in iCloud etwas ändert, kann der Push-Dienst von Apple die App wecken, damit sie die Änderung abruft; diese Mitteilung enthält keine Ihrer Aufzeichnungen. Sie können die Synchronisierung in iOS unter Einstellungen > [Ihr Name] > iCloud ausschalten; Ihr Budget bleibt dann nur auf diesem iPhone.

## 3. Das gemeinsame Budget

Sie können eine Person zu einem Budget einladen, das Sie gemeinsam führen. Die Einladung ist ein iCloud-Link, den Sie selbst versenden, und das gemeinsame Budget wird von Apple in einer freigegebenen CloudKit-Zone gespeichert, die nur Sie beide öffnen können. Was einer von Ihnen darin einträgt, sieht die andere Person, und bei jedem Eintrag ist zu sehen, wer ihn hinzugefügt hat; Ihr eigenes Budget wird nie geteilt. Wenn Sie einen Namen für das gemeinsame Budget eingeben, sieht die andere Person ihn bei Ihren Einträgen; er wird mit Ihrem Budget in Ihrem iCloud-Account und in der freigegebenen Zone gespeichert. Die App teilt der eingeladenen Person mit, ob Ihr Abonnement aktiv ist, damit sie kostenlos Einträge im gemeinsamen Budget hinzufügen kann (Abschnitt 2 der Nutzungsbedingungen). Jeder von Ihnen beiden kann das gemeinsame Budget in der App jederzeit verlassen oder schließen. Wenn Sie die Freigabe beenden, kann die andere Person eine schreibgeschützte Kopie dessen behalten, was bis dahin im gemeinsamen Budget stand. Wenn Apple der App mitteilt, dass die andere Person etwas hinzugefügt hat, läuft die Mitteilung über den Push-Dienst von Apple.

## 4. Der Bon-Scanner und die Kamera

Die App verwendet die Kamera nur, wenn Sie den Bon-Scanner öffnen, und iOS fragt beim ersten Mal nach Ihrer Erlaubnis. Das Foto des Kassenbons wird auf Ihrem iPhone gelesen: Das Vision-Framework von Apple findet seinen Text und einen etwaigen QR-Code, und auf iPhones mit Apple Intelligence hilft das Sprachmodell von Apple auf dem Gerät, den Gesamtbetrag, die Währung und den Namen des Geschäfts zu finden. Das Foto und der erkannte Text bleiben nur im Arbeitsspeicher des iPhone, solange sie gelesen werden, und werden direkt danach gelöscht. Beides wird nie gespeichert, nie hochgeladen und nie an uns oder an einen Online-Dienst gesendet. Gespeichert wird nur die Ausgabe, die Sie danach sichern (ihr Betrag, ihre Währung, ihr Datum und der Name des Geschäfts in der Notiz), wie jeder andere Eintrag.

## 5. Apple Pay über Kurzbefehle

Die App greift weder auf Wallet noch auf Ihre Karten oder Ihre Bank zu. Wenn Sie in der App „Kurzbefehle“ von Apple eine persönliche Automation mit dem Auslöser „Transaktion“ einrichten, übergibt „Kurzbefehle“ jedes Mal, wenn Sie in einem Geschäft mit Apple Pay bezahlen, auf demselben iPhone den Betrag und den Namen des Händlers an die Aktion der App zum Hinzufügen einer Ausgabe, und die App erfasst daraus eine Ausgabe. Nichts davon wird an uns gesendet; der Eintrag wird wie jeder andere gespeichert und synchronisiert (Abschnitte 1 und 2). Es passiert nichts, solange Sie die Automation nicht selbst einrichten, und Sie können sie jederzeit in „Kurzbefehle“ ändern oder löschen.

## 6. Wechselkurse und Rabattangebote (unser Server)

Wir betreiben einen kleinen Server auf Cloudflare Workers für zwei Aufgaben. Keine davon erhält Ihre Aufzeichnungen.

- **Wechselkurse.** Wenn eine Ausgabe in einer anderen Währung als Ihrer Hauptwährung erfasst wird oder Sie Ihre Hauptwährung ändern, fragt die App den Server nach den Kursen dieses Tages. Die Anfrage enthält nur das Datum: keinen Betrag, keine Währung und nichts über Sie. Der Server bezieht die Referenzkurse des Tages von der Europäischen Zentralbank und, für Währungen, die die Bank nicht veröffentlicht, Kurse von Zentralbanken, die der offene Dienst Frankfurter sammelt, und sendet die ganze Tabelle für diesen Tag zurück; Ihr iPhone wählt den Kurs aus, den es braucht. Ausgaben in Ihrer Hauptwährung brauchen den Server nie.
- **Rabattangebote.** Wenn Sie die Verlängerung ausschalten, kann Ihnen die App einen niedrigeren Preis für Ihren nächsten Zeitraum anbieten (Abschnitt 2 der Nutzungsbedingungen). Apple verlangt, dass ein solches Angebot von uns signiert wird; deshalb sendet die App dem Server direkt vor dem Kauf nur die eigene Kennung der App, die Kennungen des Plans und des Angebots und, wo Apple sie verlangt, die App Store-Nummer Ihres aktuellen Abonnementkaufs. Der Server fügt eine zufällige Einmalnummer hinzu, signiert die Angaben, antwortet und speichert nichts. Er erfährt nichts darüber, wer Sie sind: keinen Namen, keinen Apple Account und keine Ihrer Aufzeichnungen.

Wie jeder Server sieht auch unserer die IP-Adresse einer Anfrage, um sie zu beantworten. Er bewahrt diese Adresse nirgends auf und verknüpft Anfragen nicht mit einer Person. Cloudflare, das den Server betreibt, kann kurzlebige technische Protokolle von Anfragen zu Sicherheits- und Zuverlässigkeitszwecken gemäß seiner eigenen Datenschutzrichtlinie (https://www.cloudflare.com/privacypolicy/) aufbewahren.

## 7. Mitteilungen und Widgets

Die abendliche Erinnerung wird auf Ihrem iPhone geplant, und nur, wenn Sie Mitteilungen erlauben. Um sie zuzustellen, werden keine Daten an uns gesendet. Widgets lesen Ihr Budget auf Ihrem Gerät.

## 8. Face ID-Sperre

Wenn Sie die Sperre einschalten, bittet die App iOS, Ihre Face ID oder Ihren Code zu prüfen. Face ID wird vollständig von iOS verarbeitet: Die App sieht Ihre Gesichtsdaten nie und erfährt nur, ob die Prüfung erfolgreich war.

## 9. Käufe

Abonnements werden von Apple über den App Store verkauft und abgewickelt. Wir erhalten Ihre Zahlungsdaten nicht. Apple teilt der App mit, ob Ihr Abonnement aktiv ist, welchen Plan Sie gewählt haben, mit seinem Preis, ob die Verlängerung eingeschaltet ist und ob für Ihren Apple Account ein Angebot verfügbar ist; Abschnitt 10 beschreibt, was davon an unsere Nutzungsanalyse geht.

## 10. Nutzungsanalyse und Absturzberichte

Um zu erfahren, welche Funktionen helfen und wo die App im Weg steht, sendet die App anonyme Nutzungssignale an TelemetryDeck, einen Analysedienst der TelemetryDeck GmbH (Augsburg, Deutschland) mit Servern in der EU. Der Code von TelemetryDeck ist der einzige Code in der App, der nicht von Apple oder von uns stammt. Ein Signal benennt eine Aktion in der App: zum Beispiel, dass ein Schritt des ersten Starts abgeschlossen und welche seiner Auswahlantworten gewählt wurde (was Ihnen früher im Weg stand, ob Sie ein Monatsbudget festgelegt haben, an welchem Tag Ihr Monat beginnt, die Art Ihres ersten Ziels aus der Liste und in wie vielen Monaten es erreicht sein soll), wie lange die erste Ausgabe gedauert hat, dass eine Ausgabe oder Einnahme hinzugefügt wurde und wie (eingetippt, über ein Widget, einen Kassenbon, Apple Pay oder eine Datei) und ob sie in Ihrer Hauptwährung war, dass ein Ziel angelegt wurde (seine Art aus der Liste und ob es ein Datum hat), dass Geld zurückgelegt, eine Challenge begonnen oder ein Feld abgehakt wurde, dass eine Ansicht geöffnet oder eine Datei importiert wurde (mit einer ungefähren Zahl ihrer Zeilen), dass der Abo-Bildschirm oder ein Angebot angezeigt, ein Plan gewählt oder ein Abonnement abgeschlossen, verlängert oder wiederhergestellt wurde, dass die App um eine Bewertung gebeten hat, oder, als kurzer Fehlercode, dass etwas nicht funktioniert hat, etwa dass der App Store nicht antwortete. Es enthält einen auf die Stunde gerundeten Zeitstempel und allgemeine technische Angaben: die Versionen der App und von iOS, das Gerätemodell, die Sprache, die Region und die Zeitzone sowie Anzeige- und Bedienungshilfen-Einstellungen wie den Dunkelmodus oder die Textgröße. Wenn ein Abonnement beginnt oder sich verlängert, enthält sein Signal außerdem den Plan, seinen in US-Dollar umgerechneten Preis, die Währung und das Land Ihres App Stores, damit wir sehen, welche Pläne gewählt werden.

Ein Signal enthält nie Ihre Beträge, Salden oder Budgetzahlen, Ihre Kategorien, Notizen oder Zielnamen, Namen von Geschäften oder Händlern, Fotos von Kassenbons oder deren Text, die von Ihnen eingegebenen Wechselkurse, Ihren Namen, Ihre E-Mail-Adresse, Ihren Apple Account oder Ihren Standort und auch nichts über die Person, mit der Sie ein Budget teilen. Ihre Installation wird nur durch eine zufällige Kennung erkannt, die die App vor dem Senden mit einem Salt versieht und hasht, sodass die Signale nicht auf Sie zurückgeführt oder über Apps hinweg verfolgt werden können. TelemetryDeck speichert keine IP-Adressen und verwendet keine Cookies. Wir betrachten diese Signale nur als Statistik, um die App zu verbessern; wir verkaufen sie nicht, geben sie nicht an Werbetreibende weiter und nutzen sie nicht, um Sie zu verfolgen. Die App enthält keinen Werbe- oder Tracking-Code und verfolgt Sie nicht über andere Apps oder Websites hinweg.

Unabhängig davon kann Apple uns zusammengefasste, anonyme Nutzungsstatistiken und Absturzberichte zur Verfügung stellen, wenn Sie sich in iOS unter Einstellungen > Datenschutz & Sicherheit > Analyse & Verbesserungen dafür entscheiden, Analysedaten mit App-Entwicklern zu teilen. Diese lassen keinen Rückschluss auf Sie zu.

## 11. Game Center

Wenn Sie bei Game Center angemeldet sind, werden Erfolge für Ihre Spar-Meilensteine unter Ihrem Game Center-Account an Game Center von Apple gemeldet und gemäß der Datenschutzrichtlinie von Apple behandelt. Ein Erfolg sagt nur, dass ein Meilenstein erreicht wurde; Ihre Einträge, Notizen und Zielnamen werden nicht gesendet. Ihre Game Center-Identität erhalten wir nicht.

## 12. Import und Export

Ein Export Ihrer Ausgaben und Einnahmen als CSV-Datei und der Import einer CSV-Datei aus einer anderen Budget-App erfolgen auf Ihrem Gerät. Die App liest nur die Datei, die Sie auswählen, und eine exportierte Datei geht nur dorthin, wohin Sie sie über das Teilen-Menü senden.

## 13. Was die App nicht tut

Die App verwahrt, überweist, investiert und verleiht kein Geld, ist mit keiner Bank, keiner Karte und keinem Zahlungskonto verbunden und gibt keine Finanz-, Steuer- oder Anlageberatung. Die App greift nicht auf Wallet, Ihren Standort, Ihre Kontakte, Ihre Fotomediathek oder Ihr Mikrofon zu und hat kein Konto, keine Anmeldung, keine Werbung, keinen Chat und keinen öffentlichen Feed.

## 14. Kinder

Die App ist für alle Altersgruppen geeignet (Altersfreigabe 4+) und erhebt wissentlich keine personenbezogenen Informationen von irgendjemandem, auch nicht von Kindern unter 13 Jahren (oder dem entsprechenden Alter in Ihrem Land).

## 15. Aufbewahrung und Löschung von Daten

Die Daten bleiben, solange Sie sie behalten. Sie können einen Eintrag in der App jederzeit löschen; er wartet 30 Tage unter „Zuletzt gelöscht“ und ist dann weg. Alles löschen Sie, indem Sie die App löschen und, für synchronisierte Daten, in iOS unter Einstellungen > [Ihr Name] > iCloud > Accountspeicher verwalten > Budgetplaner. Was Sie einem gemeinsamen Budget hinzugefügt haben, bleibt dort für die andere Person, bis einer von Ihnen es löscht oder das gemeinsame Budget geschlossen wird. Da wir keine Kopie haben, gibt es für uns nichts weiter zu löschen. Nutzungssignale sind anonym und können Ihnen nicht zugeordnet werden, und unser Server speichert nichts über Sie, daher gibt es von beidem keinen persönlichen Datensatz, den man nachschlagen oder löschen könnte.

## 16. Ihre Rechte

Je nachdem, wo Sie leben (zum Beispiel nach der DSGVO in der EU, der UK GDPR, dem CCPA/CPRA in Kalifornien, dem APPI in Japan, dem PIPA in Korea oder dem LGPD in Brasilien), haben Sie möglicherweise das Recht auf Auskunft, Berichtigung, Löschung und Übertragbarkeit Ihrer personenbezogenen Daten sowie das Recht, der Verarbeitung zu widersprechen oder sie einschränken zu lassen. Da wir Ihre Daten nicht besitzen, können Sie diese Rechte direkt auf Ihrem Gerät und in iCloud wie oben beschrieben ausüben; der CSV-Export in den Einstellungen gibt Ihnen alle Ihre Ausgaben und Einnahmen in einer Datei. Sie können sich mit jeder Anfrage oder Frage auch an uns wenden und sich bei Ihrer örtlichen Datenschutzbehörde beschweren.

Wir verkaufen oder teilen keine personenbezogenen Informationen im Sinne des CCPA/CPRA.

## 17. Änderungen

Wenn sich diese Erklärung ändert, aktualisieren wir das Datum oben und informieren Sie bei wesentlichen Änderungen in der App.

## 18. Kontakt

Stanislau Malchanau, Belarus
E-Mail: 7tam.official@gmail.com
