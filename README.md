# Developpement-d-un-OCR-Optical-Character-Recognition-
## Description du projet : 
Cet outil permettra de déchiffrer les documents officiels, vérifier leur 
authenticité et extraire les données 
## Objectif : 
Développer un outil OCR capable de : 
1. Déchiffrer automatiquement le contenu textuel des documents officiels 
(PDF, image…) 
2. Extraire les données pertinentes 
3. Vérifier l’authenticité des documents 
## Fonctionnalités : 
1. Téléversement de documents 
• Upload de documents en formats : PDF, JPEG, PNG, TIFF 
• Drag & drop ou sélection manuelle 
• Interface intuitive pour charger plusieurs fichiers 
2. Reconnaissance de texte (OCR) 
• Lecture automatique du texte contenu dans les documents : 
• Imprimés (passeports, CIN, contrats, certificats…) 
• Manuscrits (optionnel si applicable) 
• Utilisation d’un moteur OCR : Tesseract, Google Vision, ou EasyOCR 
• Reconnaissance multilingue (Français, Arabe…) 
3. Extraction de données structurées 
• Détection et extraction automatique des champs spécifiques : 
➢ Nom, prénom, date de naissance, numéro CIN, adresse, etc. 
• Conversion en format exploitable : JSON, CSV, base de données 
• Support de modèles prédéfinis par type de document 
4. Vérification de l’authenticité 
• Vérification des éléments de sécurité visuels (filigrane, cachet, mise en 
page…) 
• Validation des formats et cohérences des données 
➢ Exemple : date de délivrance > date de naissance 
• Comparaison avec une base de documents de référence (si disponible) 
5. Interface utilisateur 
• Visualisation du document original + texte reconnu côte à côte 
• Zones de texte surlignées dans l’image avec contenu reconnu 
• Edition manuelle des champs extraits si erreur 
6. Export et intégration 
• Export des données extraites en PDF, Excel, CSV, JSON 
• Intégration vers d'autres systèmes (API REST, base de données centrale) 
• Génération d’un rapport de vérification 
7. Historique et traçabilité 
• Sauvegarde des documents analysés 
• Journalisation des vérifications et extractions 
• Possibilité de reconsulter les résultats 
8. Sécurité et confidentialité 
• Traitement local ou sur serveur sécurisé 
• Chiffrement des fichiers sensibles 
• Authentification des utilisateurs et gestion des rôles




## Sprints détaillés (proposition : 6 sprints)

✅ Sprint 1 : Mise en place (1 semaine)

Installer environnement Python (FastAPI, Tesseract, EasyOCR, Streamlit).

Créer repo projet + structure de dossiers.

Implémenter upload basique (FastAPI ou Streamlit).

Objectif : Uploader un document et afficher son contenu brut en texte via OCR.

✅ Sprint 2 : OCR multilingue (1 semaine)

Intégrer Tesseract FR/AR (gestion sens RTL pour l’arabe).

Tester sur plusieurs types de documents (PDF, JPEG).

Ajouter pré-traitement simple (rotation, contraste).

Objectif : OCR robuste FR/AR sur plusieurs formats.

✅ Sprint 3 : Extraction de données (2 semaines)

Implémenter regex pour CIN, dates, numéros, etc.

Développer pipeline d’extraction → sortie JSON structurée.

Ajouter NER (spaCy FR) pour noms/adresses.

Objectif : Extraire au moins 4 champs (nom, prénom, CIN, date naissance) avec bonne précision.

✅ Sprint 4 : Vérification authenticité basique (1-2 semaines)

Règles de cohérence (ex: date délivrance > date naissance).

Vérifier format du CIN et dates.

Détecter présence cachet/logo par template matching (OpenCV).

Objectif : Rapport de vérification simple (cohérence + flag authentique/non).

✅ Sprint 5 : Interface et exports (1 semaine)

Démo avec Streamlit :

Upload doc → affichage document + texte reconnu.

Visualisation JSON + possibilité de télécharger CSV.

Objectif : Interface fonctionnelle utilisable par un non-technique.

✅ Sprint 6 : Finalisation & rapport (1 semaine)

Sauvegarde historique (fichiers + résultats JSON).

Export complet (CSV, JSON, PDF rapport).

Rédiger rapport technique (pipeline, résultats, limites).

Objectif : Projet complet + prêt pour soutenance/démo.



