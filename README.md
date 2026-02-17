# 🏎️ F1 PERFORMANCE ARCHITECT  

---
##  Présentation du Projet

**F1 Performance Architect** est un projet d’analyse de données visant à isoler la performance humaine de la performance machine en Formule 1 durant l’ère du Budget Cap (2021–2025).

L’objectif est de concevoir une solution de Business Intelligence automatisée permettant d’évaluer :

- La performance réelle des pilotes indépendamment de leur monoplace  
- L’efficacité technique des écuries  
- Le retour sur investissement financier sous contrainte budgétaire  

---

##  Problématique Métier

Comment séparer statistiquement la performance du pilote de celle de la voiture afin d’identifier la véritable valeur compétitive des actifs humains et techniques ?

---

## Sources de Données

###  API REST F1 (Ergast compatible – Jolpica)
- Résultats de courses  
- Classements pilotes et constructeurs  
- Points, positions, tours  
   https://api.jolpi.ca/ergast/f1  

###  FastF1 – Télémétrie
- Vitesse  
- RPM  
- Activation DRS  
- Données tour par tour  

###  Données Financières (Web Scraping éthique)
- Salaires pilotes (2021–2025)  
- Modélisation proxy du Budget Cap  

Sources publiques utilisées :  
- https://racingnews365.com/formula-1-driver-salaries-2021  
- https://racingnews365.com/what-are-the-driver-salaries-for-2022  
- https://racingnews365.com/f1-driver-salaries-2023  
- https://www.nbcnewyork.com/news/sports/how-much-are-f1-drivers-paid-salaries-2024/5192874/  
- https://racingnews365.com/2025-f1-driver-salaries-how-much-do-f1-drivers-earn  

---

##  Pipeline Data

1. Extraction via API REST (Jolpica)  
2. Ingestion des données télémétriques (FastF1)  
3. Web scraping des données salariales  
4. Nettoyage et normalisation (Pandas)  
5. Consolidation des datasets  
6. Calcul des indicateurs de performance  
7. Intégration dans Power BI  

---

##  Indicateurs Clés (KPIs)

- Pace Advantage  
- Teammate Delta  
- Budget Efficiency  
- Driver ROI  
- Mechanical Reliability Score  
- Cost per Podium  

---

## Dashboards

- Vue Executive  
- Talent Pilote  
- Performance Machine  
- Finance & ROI  

---

##  Stack Technique

- Python (Pandas, NumPy, FastF1, Requests, BeautifulSoup)  
- Power BI  
- Git / GitHub  

---

##  Structure du Repository

📁 data/           <br>
   ├── raw/              → Données brutes (API, FastF1, Web Scraping) <br>
   ├── processed/        → Données nettoyées et prêtes pour analyse  <br>
📁 cache/                → Cache FastF1 (non versionné)  <br>
📁 scripts/              → Scripts d’extraction & génération des CSV  <br>
📁 notebooks/            → EDA, calcul des KPIs, analyses statistiques  <br>
📁 dashboards/           → Fichier Power BI (.pbix)  <br>
📄 Cahier_de_charge.docx → Documentation fonctionnelle  <br>
📄 README.md             → Présentation du projet  <br>


---

## Gestion de Projet & Documentation

###  Organisation du projet (Kanban)
Le suivi du projet a été réalisé via Trello selon une méthodologie agile .

🔗 Trello : <https://trello.com/invite/b/698dabb9950d7840343abecf/ATTI35a09675e9068139e94402fd91e3ba0e14763F3F/f1-performance-architect>

---

###  Documentation technique & fonctionnelle
La documentation détaillée (cadrage, architecture, décisions techniques, évolutions) est centralisée sur Confluence.

🔗 Confluence : <(https://imanelen25-1770646756973.atlassian.net/wiki/pages/resumedraft.action?draftId=557057&draftShareId=64e1f518-d0d7-481c-815f-32b6aff04291)>




