# PDF-Editor (eingebettet in die Leckortungs-App)

Angepasste Kopie des PDF-Editors (flojaeger-ai/pdf-editor, Version 7; pdf.js Apache-2.0, pdf-lib MIT).
Änderungen gegenüber dem Original:
- läuft nur im iframe der Leckortungs-App; Export/Öffnen per postMessage (Export über `saveFiles` der App)
- KEINE dauerhafte Speicherung: keine Unterschriften-Liste, kein Auto-Speichern (weder localStorage noch IndexedDB)
- eigener Service Worker / Manifest entfernt, Dateisystem-Zugriff (FSA) aus
- Speicher-Präfixe getrennt (`lkpdfed.*`), Farbschema an die App angepasst
