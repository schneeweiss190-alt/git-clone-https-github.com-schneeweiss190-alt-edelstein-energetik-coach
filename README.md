
# This script prepares a Flutter project scaffold as text files (not executing Flutter tooling).
# It writes a set of source files into a local folder structure so the assistant can echo them back in the chat.

from pathlib import Path

project_root = Path('edelstein_energetik_coach')
files = {}

def add(path, content):
    p = project_root / path
    files[str(p)] = content

# README in German
add('README_de.md', r'''# Edelstein‑Energetik Coach – Flutter Projekt (Deutsch)

Dieses Grundgerüst ist vollständig auf **Deutsch** und enthält:
- Navigations‑Screens (Start, Coach, Scanner, Bibliothek, Shop)
- Datenmodelle (Stein, Produkt, Thema)
- Services (Firestore, Empfehlungen, Platzhalter für KI‑Coach)
- Deutsche Lokalisierung (`de`) und App‑Theming
- Beispiel‑Assets‑Einbindung (Logo)

## Schnellstart
1. Flutter installieren und Projekt erstellen/klonen.
2. Firebase initialisieren:
   ```bash
   flutter pub add firebase_core firebase_auth cloud_firestore firebase_storage
   flutterfire configure
flutter pub add google_mlkit_image_labeling image_picker
flutter run
