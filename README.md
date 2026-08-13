# Autonomes Spurführungs-Fahrzeug (Induktive Leitdrahtverfolgung)

![Status](https://img.shields.io/badge/Status-Completed-success)
![Focus](https://img.shields.io/badge/Focus-Embedded%20Systems%20%26%20Sensorik-blue)
![University](https://img.shields.io/badge/TU%20Braunschweig-Modellfahrzeugbau-red)

Dieses Projekt entstand im Rahmen des akademischen Projektkurses **Modellfahrzeugbau** an der **Technischen Universität Braunschweig**. Ziel war die Entwicklung eines autonomen Modellfahrzeugs, das mithilfe induktiver Sensorik und digitaler Signalverarbeitung einem im Boden verlegten Wechselstrom-Leitdraht präzise folgt.

---

## 📸 Galerie & Einblicke

> *Hinweis: Ordne deine Bilder im Repository z. B. in einem Ordner `/assets` an und verlinke sie hier.*

| Hardware & Aufbau | Sensorik & Test |
| :---: | :---: |
| ![Fahrzeug-Hardware](assets/fahrzeug_gesamt.jpg) | ![Sensorik/Messung](assets/sensorik_aufbau.jpg) |
| *Gesamtaufbau des Modellfahrzeugs* | *Induktive Sensoranordnung an der Front* |

---

## 🎯 Kernthemen & Meine Aufgaben

In diesem Projekt lag mein Schwerpunkt auf der **Konzeption der Sensorik, der analogen Signalverarbeitung sowie der Regelungstechnik**:

- **Induktive Sensorik:** Auslegung und Platzierung von Induktionsspulen zur Erfassung des magnetischen Wechselfelds des Leitdrahts.
- **Analoge Signalaufbereitung:** Filterung (Bandpass) und Verstärkung der schwachen Induktionssignale zur Rauschunterdrückung und ADC-Vorbereitung.
- **Signalverarbeitung & Regelung:** Normalisierung der Differenzsignale zur Berechnung der Querablage sowie Implementierung eines Regelungsalgorithmus (PID) zur präzisen Ansteuerung des Lenkservos.

---

## 🛠 Eingesetzte Technologien & Tools

- **Hardware & Hardware-Nah:** Induktionsspulen, Operationsverstärker (OPVs), Bandpassfilter, ADC, PWM-Servoansteuerung.
- **Software & Entwicklung:** Embedded C/C++, Signalverarbeitung, PID-Regelung.
- **Methodik:** Mess- und Prüfaufbau zur Validierung der Signalqualität bei unterschiedlichen Abständen und Winkeln zum Leitdraht.

---

## 💡 Funktionsprinzip (Kurzübersicht)

1. **Erfassung:** Ein Wechselstrom im Leitdraht erzeugt ein kreisförmiges Magnetfeld.
2. **Messung:** Zwei symmetrisch an der Front montierte Spulen induzieren eine spannungsabhängige Amplitude basierend auf dem Abstand zum Draht.
3. **Auswertung:**
   $$\text{Querablagefehler} = \frac{V_{\text{links}} - V_{\text{rechts}}}{V_{\text{links}} + V_{\text{rechts}}}$$
4. **Regelung:** Der berechnete Fehler dient dem Regler als Eingangsgröße, um den Servo-Lenkwinkel kontinuierlich nachzuführen.
