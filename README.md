# Thermomètre Numérique Connecté

![STM32](https://img.shields.io/badge/STM32-03234B?style=flat&logo=stmicroelectronics&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white)

Projet ENSEA — Thermomètre numérique connecté avec interface web, stockage cloud et connectivité sans fil.

---

## Architecture

```
┌─────────────────┐
│ Capteur T°      │
└────────┬────────┘
         │
┌────────▼────────┐   BLE (config)
│ Microcontrôleur │ ─────────────►  Provisioning WiFi
│ (STM32 / ESP32) │   WiFi (données)
└────────┬────────┘
         │ HTTP
┌────────▼────────┐      ┌──────────────┐
│ API REST        │ ───► │ MongoDB       │
│ (Node / Python) │      │ (historique)  │
└────────┬────────┘      └──────────────┘
         │
┌────────▼────────┐
│ Dashboard React │  courbes · stats · alertes seuil
└─────────────────┘
```

---

## Fonctionnalités

- Acquisition de la température en temps réel
- Transmission sans fil : **BLE** (configuration) + **WiFi** (envoi des données)
- API REST pour l'historique et la gestion des alertes
- Interface web React : courbes, statistiques, alertes de seuil
- Stockage cloud (MongoDB)

---

## Stack technique

| Couche | Technologie |
|--------|-------------|
| Embarqué | STM32 / ESP32 · BLE · WiFi |
| Backend | API REST · Node.js / Python · MongoDB |
| Frontend | React · Chart.js |
| Cloud | MongoDB · déploiement distant |

---

## Rapport

`Rapport_Thermometre_Numerique.pdf` — Rapport technique complet (57 pages)

---

Auteurs : LENARD Dunstan Kishor & ROBINSAN Kiritheepan — Étudiants ingénieurs à l'ENSEA
