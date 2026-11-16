# Orbweaver
Razer Orbweaver Silicon

# Orbweaver Bridge for macOS
# Download im release

**Deutsch** · [English](#english)

Eine native macOS-App zur Nutzung des **Razer Orbweaver Chroma** mit eigenen Tastenbelegungen, Makros, Profilen und RGB-Effekten.

Entwickelt und bisher getestet mit **macOS 27 auf Apple Silicon**. Die App ist ein unabhängiges Projekt und steht in keiner Verbindung zu Razer.

## Funktionen

- **Tastenbelegungen:** 20 Haupttasten, beide Daumentasten und alle Richtungen des Daumenpads.
- **Makros:** Tastensequenzen mit aufgezeichneten Zeitabständen.
- **Profile:** Lokales Speichern und Verknüpfen mit Spielen oder Programmen.
- **Automatischer Profilwechsel:** Optional passend zum aktiven Programm.
- **Spielesuche:** Erkennung von Spielebibliotheken; weitere Programme über die macOS-Dateiauswahl hinzufügen.
- **RGB-Beleuchtung:** Eigene Grundfarbe für jede Haupttaste.
- **Tasteneffekte:** Atmen, Reaktiv und Wechsel zwischen zwei Farben – einzeln oder für mehrere ausgewählte Tasten.
- **Menüleistenbetrieb:** Das rote Fensterkreuz blendet die Oberfläche aus; die Bridge läuft weiter.
- **Sprachen:** Deutsch und Englisch, während der Nutzung umschaltbar.

## Unterstütztes Gerät

**Razer Orbweaver Chroma — USB-ID `1532:0207`**

Andere Razer-Geräte wurden mit dieser App bisher nicht geprüft.

## Einrichtung

1. Die App öffnen.
2. Unter **Systemeinstellungen → Datenschutz & Sicherheit** die benötigten Freigaben für **Orbweaver Bridge** erteilen:
   - **Eingabeüberwachung** zum Erkennen der Orbweaver-Tasten.
   - **Bedienungshilfen** zum Auslösen eigener Tastenkürzel und Makros.
3. Falls macOS dazu auffordert, die App vollständig beenden und erneut öffnen.
4. Tastenbelegungen einstellen und **„Bridge-Profil aktiv“** einschalten.

Die Freigaben ermöglichen technisch weitreichenden Eingabe- und Steuerungszugriff. Die Geräteerkennung der Bridge ist auf den Orbweaver Chroma begrenzt. Normale Tastatureingaben werden für die Kürzel- und Makroaufnahme nur im eigenen App-Fenster erfasst.

## Verwendung

### Tasten und Makros

Unter **Anpassen** eine Taste in der Geräteansicht auswählen. Anschließend ein Tastenkürzel oder Makro aufnehmen.

- Kürzel können bis zum Loslassen der Orbweaver-Taste gehalten werden.
- Makros werden einmal pro Tastendruck abgespielt.
- **Esc** verwirft eine laufende Aufnahme.
- Makroaufnahmen sind auf 30 Sekunden beziehungsweise 512 aufgezeichnete Ereignisse begrenzt.

### Beleuchtung

Unter **Chroma RGB** die Grundfarben der einzelnen Tasten einstellen.

Für zusätzliche Effekte:

1. Gewünschte Tasten per Häkchen auswählen.
2. Effekt, Farben und Geschwindigkeit einstellen.
3. **„Effekt der Auswahl zuweisen“** wählen.
4. **„Anwenden & speichern“** anklicken.

**„Grundfarbe nutzen“** lässt ausgewählte Tasten jeweils in ihrer eigenen Grundfarbe atmen. Reaktive Effekte können eine Taste hervorheben und anschließend zu ihrer Grundfarbe zurückblenden.

Die zusätzlichen Tasteneffekte und die stufenlos regelbaren Animationen benötigen die laufende App.

### Spiele und Profile

Unter **Spiele & Profile** ein Spiel auswählen und ein eigenes Profil anlegen oder ein bestehendes verknüpfen. Andere Programme lassen sich über **„Hinzufügen …“** auswählen.

Die optionale Profilautomatik folgt dem Programm im Vordergrund. Für Programme ohne Verknüpfung kann ein Rückfallprofil festgelegt werden.

Die Suche berücksichtigt Steam-Bibliotheken, bekannte Spieleordner weiterer Anbieter sowie unterstützte Installationskataloge. Die Erkennung aller Anbieter und Installationsvarianten ist noch nicht vollständig praktisch geprüft.

### Menüleiste

- **Rotes ×:** Fenster ausblenden und im Hintergrund weiterlaufen.
- **Menüleistensymbol:** Fenster öffnen, Bridge-Profil aktivieren oder stoppen.
- **„Orbweaver Bridge beenden“:** App vollständig beenden.

Während ein Bridge-Profil aktiv ist, leuchten **alle drei Profillichter**. Beim Stoppen wird die vorherige Lampenkombination wiederhergestellt.

## Speicherung und Grenzen

Profile werden **auf dem Mac** gespeichert:

```text
~/Library/Application Support/Orbweaver Bridge/
```

Ein dauerhaftes Schreiben eigener Tastenbelegungen in den Gerätespeicher ist **nicht implementiert**. Die drei Profillichter sind keine bestätigten drei internen Speicherplätze.

Weitere aktuelle Grenzen:

- Mausaktionen werden nicht als Makros aufgenommen.
- Automatische Tastenwiederholung beim Halten einer Taste ist noch nicht ergänzt.
- Spiele innerhalb eines gemeinsamen Emulators oder Launchers können eine manuelle Profilwahl erfordern.
- Vollständige Funktionsgleichheit mit Razer Synapse wird nicht zugesichert.

## Entwicklungsstand

Aktuelle Vorschau: **0.17**

Tastenbelegungen, Makros, Profilspeicherung und verschiedene Beleuchtungsfunktionen wurden am angeschlossenen Gerät geprüft. Zusätzliche automatische Prüfungen decken unter anderem Profilzuordnung, RGB-Zuordnung, Effektberechnung und das Freigeben gehaltener Ausgabetasten ab.

Die App ist lokal signiert und nicht von Apple notarisiert. Nach Aktualisierungen können macOS-Freigaben erneut erforderlich sein.

## Aus dem Quellcode bauen

Benötigt werden die Apple Command Line Tools. Im Quellcodeordner:

```sh
zsh build.sh
```

Das Skript erstellt die App, signiert sie lokal und führt die enthaltenen Selbsttests aus.

---

# English

A native macOS app for using the **Razer Orbweaver Chroma** with custom key assignments, macros, profiles and RGB effects.

Developed and tested so far on **macOS 27 with Apple Silicon**. This is an independent project and is not affiliated with Razer.

## Features

- **Key assignments:** 20 main keys, both thumb buttons and all thumbpad directions.
- **Macros:** Keyboard sequences with recorded timing.
- **Profiles:** Local storage and links to games or applications.
- **Automatic profile switching:** Optionally follows the active application.
- **Game discovery:** Scans game libraries; other applications can be added through the macOS file picker.
- **RGB lighting:** An independent base color for each main key.
- **Per-key effects:** Breathing, reactive highlights and two-color cycling for individual keys or selected groups.
- **Menu bar operation:** Closing the window keeps the Bridge running.
- **Languages:** German and English, switchable without restarting.

## Supported device

**Razer Orbweaver Chroma — USB ID `1532:0207`**

Other Razer devices have not been tested with this app.

## Setup

1. Open the app.
2. Grant the required permissions to **Orbweaver Bridge** under **System Settings → Privacy & Security**:
   - **Input Monitoring** to detect Orbweaver key presses.
   - **Accessibility** to send custom shortcuts and macros.
3. Quit and reopen the app if macOS requests it.
4. Configure your assignments and enable **“Bridge profile active.”**

These permissions technically allow broad input and control access. The Bridge’s device matching is limited to the Orbweaver Chroma. Regular keyboard input used for shortcut and macro recording is captured only within the app’s own window.

## Usage

### Keys and macros

Select a key in the device diagram under **Customize**, then record a shortcut or macro.

- Shortcuts can remain held until the Orbweaver key is released.
- Macros play once per key press.
- **Esc** discards an active recording.
- Macro recordings are limited to 30 seconds or 512 recorded events.

### Lighting

Set each key’s base color under **Chroma RGB**.

To add effects:

1. Select the desired keys using their checkboxes.
2. Choose an effect, colors and speed.
3. Click **“Assign effect to selection.”**
4. Click **“Apply & save.”**

**“Use base color”** lets selected keys breathe in their individual base colors. Reactive effects can highlight a pressed key and then fade back to its base color.

Additional per-key effects and continuously adjustable animations require the app to remain running.

### Games and profiles

Under **Games & Profiles**, select a game and create a dedicated profile or link an existing one. Use **“Add …”** for other applications.

Optional automatic switching follows the foreground application. A fallback profile can be selected for applications without a linked profile.

Discovery covers Steam libraries, known game folders from other providers and supported installation catalogs. Detection across every provider and installation layout has not yet been fully tested.

### Menu bar

- **Red ×:** Hide the window and keep running in the background.
- **Menu bar icon:** Open the window or enable/stop the Bridge profile.
- **“Quit Orbweaver Bridge”:** Exit the app completely.

**All three profile indicators** light up while a Bridge profile is active. Stopping restores the previous indicator combination.

## Storage and limitations

Profiles are stored **on the Mac**:

```text
~/Library/Application Support/Orbweaver Bridge/
```

Writing custom key assignments permanently to the device’s onboard memory is **not implemented**. The three indicator LEDs do not establish the existence of three onboard profile slots.

Other current limitations:

- Mouse actions are not recorded as macros.
- Automatic key repeat while holding a key has not yet been added.
- Games running inside a shared emulator or launcher may require manual profile selection.
- Full feature parity with Razer Synapse is not guaranteed.

## Development status

Current preview: **0.17**

Key assignments, macros, profile storage and several lighting functions have been tested on the connected device. Additional automated checks cover areas including profile matching, RGB mapping, effect rendering and releasing held output keys.

The app is locally signed and is not notarized by Apple. macOS permissions may need to be renewed after updates.

## Build from source

Apple Command Line Tools are required. From the source directory:

```sh
zsh build.sh
```

The script builds the app, signs it locally and runs the included self-tests.
