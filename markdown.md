# Dokumentation Modul 346

## KN01 Virtualisierung

#### A)
In dieser Aufgabe arbeite ich mit der VMWare Workstation Pro, da ich schon einige Erfahrungen gemacht habe mit diesem Programm. Das VMWare Workstation Pro Programm ist ein Virtualisierungssoftware.

#### B)
Nachdem ich die VMWare Workstation Pro auf dem Laptop installiert habe, konnte ich mit der aufgabe B starten. In Aufgabe B geht es darum Ubuntu auf einer VM zu installieren.
Zuerst musste ich die konfigurationen machen in der VMWare Workstation Pro, um später die **ISO Image Datei** in die VM einbinde.

![VMWare Workstation Pro](KN01/vmware.png)

>Nachdem ich alles fertig konfiguriert habe, konnte ich nun die **ISO Image Datei** in die VM einbinden.

![ISO Image Datei](KN01/ISOimagefile.png)

#### Problemen
1. Fehlermeldung: Nicht genügend RAM um die Virtuelle Maschiene zu betreiben.
   Grund:   Maximal 32GB RAM sind erlaubt, mehr nicht.

#### C)
Dieses Kapitel war ein kurzer Einstieg für das Modul 346. Hier zum einstieg mussten wir die Ressourcezuteilung von der neu erstellten VM überprüfen.

![Relative](KN01/CPU_weniger.png)
>Weniger CPU als Hostsystem

![Relative](KN01/CPU_mehr.png)
>Mehr CPU als Hostsystem

![Relative](KN01/RAM_weniger.png)
>Weniger RAM als Hostsystem

![Relative](KN01/RAM_mehr.png)
>Mehr RAM als Hostsystem

***

## KN02 IaaS - Virtuelle Server


#### A) AWS Kurs
Wir arbeiten hauptsächlich mit AWS (Amazon Web Services), da AWS extra für Lernende ein Lerner Lab zur verfügung stellt und dazu 100$ zum Ausprobieren. Nachdem die 100$ abgelaufen sind, muss man selber zahlen, wenn man weiter machen möchte. Aber das gute daran ist, die 100$ werden sehr langsam verbraucht.

#### a) Lab 4.1 - EC2
Bei dieser Aufgabe musste ich eine Instanz erstellen über den AWS Academy. Das Ziel dabei ist, dass man eine HTML Seite hochlädt und sie anschliessend über den Browser mit dem URL Code über den AWS abruft.

![Relative](KN02/Lab%204.1%20-%20EC2/Inbound.png)
>Hier ist ein Beispiel was ich einstellen musste, damit ich meine HTML Datei auf den Webserver abrufen kann. Bei der Sicherheitsgruppe habe ich für den ausgehenden Datenverkehr eine hinzugefügt, damit meine HTML Seite nicht blockiert wird.

![Relative](KN02/Lab%204.1%20-%20EC2/Instance.png)
>Da kann man einige Informationen über die Instanz herauslesen.

![Relative](KN02/Lab%204.1%20-%20EC2/EC2-Instance.png)
>Hier ist meine neu erstellte Instanz, wie man sehen kann, gibt es viele Einstellungen die man Benutzerdefiniert einstellen kann. Und wenn ich jetzt auf die Öffentliche IPv4-Adresse klicke, öffnet sich die HTML Seite in einem neuen Browsertag.

![Relative](KN02/Lab%204.1%20-%20EC2/HTML-Site.png)
>Das ist das Endergebnis, wenn man alles korrekt gemacht hat.

***

#### b) Lab 4.2 - S3

Bei dieser Aufgabe geht es darum ein Bucket zu erstellen. 

![Relative](KN02/Lab%204.2%20-%20S3/BlockPublicAccess.png)
>Als erstes musste ich die Blockierung vom öffentlichen Zugang beheben. Dazu musste ich in der *Edit Block public access* in allen Checkboxen abwählen und anschliessend Speichern.

![Relative](KN02/Lab%204.2%20-%20S3/Bucket_policy.png)
>Nachdem ich die die Blockierung aufbehoben habe, fügte ich unter der *Bucket policy* ein JSON Code ein.

![Relative](KN02/Lab%204.2%20-%20S3/StaticWebsiteHosting.png)

![Relative](KN02/Lab%204.2%20-%20S3/StaticWebsiteHostingIndex.png)
>Hier wird das ausgewählte Bild im *Index document* eingetragen

#### B) Zugriff mit SSH-Key

#### C) Installation von Web- und Datenbankserver

***

## KN03: Cloud-init und AWS

#### A) Cloud-init Datei Verstehen
Ich habe ein YAML-File abgelegt in diesem Ordner. Der name des Files lautet "cloud-init.yaml"

#### B) SHH-Key und Cloud-init

Beim generieren der beiden Public Keys hatte ich ein problem. Ich konnte keine Public Keys aus den Private Keys generieren, weil mein Rechner blockiert es. Deshalb musste ich es auf einen anderen Rechner probieren (PC von zuhause) und dort hat es funktioniert.

![erster Publickey]()
![zweiter Publickey]()

#### C) Template

Nachdem ich die Public Keys generiert hatte, fügte ich den in mein yml File ein. Dazu fügte ich den Publickey von unserer Lehrperson ebenso ein, damit beide Benutzer (Ich, Lehrperson) Zugriff haben.

## KN04

#### A) Bild erstellen und auf S3 hosten

In dieser Aufgabe wird das gleiche Konzept wie in KN02 gemacht. Als erstes müssen wir ein neuen *Bucket* erstellen, welches wieder mit einem Bild gehostet wird.

#### B) Web-Server mit PHP-Seite hinzufügen



#### C) Elastic Block Storage (EBS) hinzufügen

Die Zeitzonen müssen miteinander stimmen, sonst funktioniert es nicht.
