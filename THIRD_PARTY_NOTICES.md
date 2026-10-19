# Drittanbieter-Software in der Roto-App

Die Roto-App bündelt folgende Software. Die jeweiligen Lizenzen gelten unverändert.

## MatAnyone 2 (Modell und Code) – **nur nicht-kommerziell**

- Quelle: https://github.com/pq-yang/MatAnyone2 (Peiqing Yang u. a., S-Lab, Nanyang Technological University)
- Lizenz: **S-Lab License 1.0**, siehe `LICENSE-MatAnyone2.txt`
- Weitergabe und Nutzung **nur für nicht-kommerzielle Zwecke**. Für kommerzielle Nutzung ist die
  Zustimmung der Rechteinhaber nötig.
- Änderungen in dieser App: eigener Modell-Lader (ohne ImageNet-Download), eigene
  Streaming-Pipeline vorwärts/rückwärts. Der Modellcode selbst ist unverändert.

## FFmpeg (über imageio-ffmpeg)

- Statisch gebautes FFmpeg 7.1 für Apple Silicon, mitgeliefert vom Python-Paket `imageio-ffmpeg`.
- Dieser Build ist mit `--enable-gpl` erstellt (u. a. libx264, libx265) und steht damit unter der
  **GNU GPL v2 oder neuer**. Quellcode: https://ffmpeg.org/download.html,
  Build-Skripte: https://github.com/imageio/imageio-binaries
- Die Roto-App ruft FFmpeg als eigenständiges Programm auf (keine Verlinkung).

## Python und Pakete

| Komponente | Lizenz |
|---|---|
| Python 3.11 (python-build-standalone) | PSF License |
| PyTorch, torchvision | BSD-3-Clause |
| NumPy | BSD-3-Clause |
| OpenCV (opencv-python-headless) | Apache 2.0 (enthält FFmpeg-Bibliotheken, LGPL) |
| Hydra, OmegaConf | MIT / BSD-3-Clause |
| einops | MIT |
| FastAPI, Starlette, Uvicorn, Pydantic | MIT / BSD-3-Clause |
| Pillow | MIT-CMU (HPND) |
| huggingface_hub, tqdm, imageio | Apache 2.0 / MPL-2.0 und MIT / BSD-2-Clause |

## Oberfläche

| Komponente | Lizenz |
|---|---|
| Electron | MIT |
| React, React DOM | MIT |
| Radix UI | MIT |
| Tailwind CSS | MIT |
| lucide-react (Symbole) | ISC |
| Zustand, Zod, clsx, tailwind-merge | MIT |
| Inter (Schrift, @fontsource-variable/inter) | SIL Open Font License 1.1 |

## Apple Vision

Die automatische Personen-Maske nutzt das in macOS eingebaute Vision-Framework
(`VNGeneratePersonSegmentationRequest`). Es wird nichts davon mitgeliefert.
