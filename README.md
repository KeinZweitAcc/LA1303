# Projekt-Dokumentation

## 1 Informieren

### 1.1 User Stories

| US-№ | Verbindlichkeit | Typ  | Beschreibung                       |
| ---- | --------------- | ---- | ---------------------------------- |
| 1    | Muss            | Funktional | Als Benutzer möchte ich Zahlen an eine API schicken, um danach mit den Zahlen zu rechnen. |
| 2    | Muss            | Funktional | Als Benutzer möchte ich, dass die eingegebenen Zahlen mit Hilfe der Mitternachtsformel berechnet werden, um das Ergebnis der Gleichung angezeigt zu bekommen. |
| 3    | Muss            | Qualität | Als Benutzer möchte ich eine andere Nachricht erhalten, wenn die Gleichung nur eine Lösung anstatt zwei hat, um das Ergebnis besser nachvollziehen zu können. |
| 4    | Muss            | Qualität | Als Benutzer möchte ich dass das Ergebnis gerundet wird, um das Ergebnis besser Lösen zu können. |
| 5    | Muss            | Qualität | Als Benutzer möchte ich eine Nachricht erhalten, wenn die Gleichung nicht lösbar ist, um zu verstehen, wieso ich keine Rückgabe erhalten habe. |
| 6    | Muss            | Qualität | Als Benutzer möchte ich, dass wenn ich eine ungültige Eingabe tätige ich eine Rückmeldung erhalte, um zu verstehen, wieso ich keine Rückgabe erhalten habe. |
| 7    | Muss            | Qualität | Als Benutzer möchte ich, eine Nachricht erhalten, wenn der Parameter a 0 beträgt, um besser zu verstehen, wieso die Gleichung nicht lösbar ist. |



### 1.2 Testfälle

| TC-№ | Ausgangslage | Eingabe | Erwartete Ausgabe |
| ----- | ------------ | ------- | ----------------- |
| 1.1  | Applikation wurde gestartet | JSON-Eingabe: { "argumentA":"1", "argumentB":"2", "argumentC":"1" } | Die Gleichung ist mit dem Wert -1 als x lösbar |
| 2.1  | Applikation wurde gestartet | JSON-Eingabe: { "argumentA":"1", "argumentB":"2", "argumentC":"1" } | Die Gleichung ist mit dem Wert -1 als x lösbar |
| 3.1  | Applikation wurde gestartet | JSON-Eingabe: { "argumentA":"4", "argumentB":"16", "argumentC":"-3" } | Die Gleichung ist mit den Werten 0.1.. und -4.1.. als x lösbar |
| 4.1  | Applikation wurde gestartet | JSON-Eingabe: { "argumentA":"10", "argumentB":"1", "argumentC":"4" } | Die Gleichung ist mit den Werten -0.41742 und -9.58258 als x lösbar |
| 5.1  | Applikation wurde gestartet | JSON-Eingabe: { "argumentA":"10", "argumentB":"1", "argumentC":"40" } | Die gegebene Gleichung ist nicht lösbar |
| 6.1  | Applikation wurde gestartet | JSON-Eingabe: { "argumentA":"100", "argumentB":"B", "argumentC":"C" } | Die Eingabe muss aus drei Zahlen bestehen |
| 7.1  | Applikation wurde gestartet | JSON-Eingabe: { "argumentA":"0", "argumentB":"2", "argumentC":"1" } | Der Parameter a darf nicht 0 sein |


## 2 Planen

# Arbeitspakete

| AP-№ | Frist | Zuständig | Beschreibung | Geplante Zeit |
| ---- | ----- | --------- | ------------ | ------------- |
| 0.A  | 23.02.24 | Greub | Projektdokumentation erstellen | 360 Min |
| 1.A  | 23.02.24 | Greub | API gibt Wert zurück | 120 Min |
| 1.B  | 23.02.24 | Greub | API reagiert auf Eingabe | 180 Min |
| 2.A  | 23.02.24 | Greub | Ergebnis wird korrekt berechnet und dem Benutzer geschickt | 300 Min |
| 3.A  | 23.02.24 | Greub | Beide Lösungen werden berechnet und dem Benutzer geschickt | 240 Min |
| 4.A  | 23.02.24 | Greub | Ergebnis wird gerundet | 30 Min |
| 5.A  | 23.02.24 | Greub | Nicht lösbare abfangen | 120 Min |
| 6.A  | 23.02.24 | Greub | Ungültige Eingaben abfangen | 30 Min |
| 7.A  | 23.02.24 | Greub | Parameter a als 0 abfangen | 30 Min |
| 0.B  | 01.03.24 | Greub | Mahara Eintrag schreiben | 300 Min |




## 3 Entscheiden

Ich habe überlegt, ob ich zusätzlich zu dem Backend noch ein Frontend erstellen sollte, welches die Zahlen und die Mitternachtsformel anzeigt. Ich habe mich schlussendlich jedoch dagegen entschieden, da ich mich mehr auf die Umsetzung des Backends konzentrieren wollte.

## 4 Realisieren


| AP-№ | Datum | Zuständig | geplante Zeit | tatsächliche Zeit |
| ---- | ----- | --------- | ------------ | ------------- |
| 0.A  | 12.01.24 | Greub |  360 Min | 300 Min | 
| 1.A  | 19.01.24 | Greub |  120 Min | 240 Min |
| 1.B  | 19.01.24 | Greub |  180 Min | 120 Min |
| 2.A  | 26.01.24 | Greub |  300 Min | 240 Min |
| 3.A  | 02.02.24 | Greub |  240 Min | 180 Min |
| 4.A  | 23.02.24 | Greub |  30 Min | 30 Min |
| 5.A  | 23.02.24 | Greub |  120 Min | 180 Min |
| 6.A  | 23.02.24 | Greub |  30 Min | 20 Min |
| 7.A  | 23.02.24 | Greub |  30 Min | 15 Min |
| 0.B  | 01.03.24 | Greub |  300 Min | 360 Min |



## 5 Kontrollieren

### 5.1 Testprotokoll

Die API-Schnittstelle wurde mit Hilfe von Swagger ausführlich getestet. 

| TC-№ | Datum | Resultat | Tester |
| ---- | ----- | -------- | ------ |
| 1.1  | 01.03.24      |  OK        | Greub       |
| 2.1  | 01.03.24      |  OK        | Greub       |
| 3.1  | 01.03.24      |  OK        | Greub       |
| 4.1  | 01.03.24      |  OK        | Greub       |
| 5.1  | 01.03.24      |  OK        | Greub       |
| 6.1  | 01.03.24      |  OK        | Greub       |
| 7.1  | 01.03.24      |  OK        | Greub       |

Die gesetzten Ziele konnten alle im Rahmen des Projektes umgesetzt werden.

