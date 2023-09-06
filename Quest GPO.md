# 1. Créer un objet dans le Gestion des stratégies de groupe

<br>

1 - Outil > Gestion des stratégies de groupe

![Gestion de stratégies de groupe](https://github.com/Fairskip/Quest_GPO/blob/main/Gestion%20de%20strategie%20de%20groupe.png)

<br>

2 - Gestion de stratégies de groupe > Forêt : wilders.lan > Domaines > wilders.lan > Wilders => Clic droit, Créer un objet GPO dans ce domaine et le lier ici...
 
![creation gpo1](https://github.com/Fairskip/Quest_GPO/blob/main/Creation%20GPO%201.png)

<br>

3 -  Nouvel objet GPO : 
  * Nom => wilders
  * Objet Starter GPO source : defaut, ok
 
![creation gpo2](https://github.com/Fairskip/Quest_GPO/blob/main/Creation%20GPO%202.png)

<br>

  * Le GPO est automatiquement activé
 
![creation gpo3](https://github.com/Fairskip/Quest_GPO/blob/main/Creation%20GPO%203%20wilders%20lien%20active.png)

<br>

# 2. Modifier la GPO

<br>

* Gestion de stratégies de groupe > Forêt : wilders > Domaines > wilders.lan _(domaine)_ > Wilders _(OU)_ > Wilders _(objet GPO)_ => Clic droit, Modifier

![Modif GPO1](https://github.com/Fairskip/Quest_GPO/blob/main/Modifier%20GPO%201.png)

<br>

### 1. Dans l'Editeur de gestion des stratégies de groupe

* Stratégie Wilders [SRV-QuestWIN.Wilders.LAN] > Configuration utilisateur > Stratégies > Modèles d'administration : définitions de stratégies... > Panneau de configuration > **Interdire l'accès  au Panneau de configuration et à l'application Paramètres du PC** => Clic droit, modifier.

![Modif GPO2](https://github.com/Fairskip/Quest_GPO/blob/main/Modifier%20GPO%202.png)

<br>

* Interdire l'accès  au Panneau de configuration et à l'application Paramètres du PC => Activé, Ok
 
![Modif GPO3](https://github.com/Fairskip/Quest_GPO/blob/main/Modifier%20GPO%203.png)

<br>
  
![Modif GPO4](https://github.com/Fairskip/Quest_GPO/blob/main/Modifier%20GPO%204.png)

<br>

### 2. Retour au Gestion de stratégies de groupe   

* Forêt : wilders > Domaines > wilders.lan > Wilders > Wilders => Clic droit, Appliqué, Ok

![gpo active & appliqué](https://github.com/Fairskip/Quest_GPO/blob/main/GPO%20Wilders%20applique%20et%20active.png)

<br>

### 3. Retour au Gestion de stratégies de groupe   

Sur l'invite de commandes, typer : 

```
gpupdate /force
```

![gpo force](https://github.com/Fairskip/Quest_GPO/blob/main/GPO_commande%20apr%C3%A8s%20chaque%20modif%20du%20GSG.png)

<br>

# 3. Tester la GPO

Sur un PC host lié au domaine : 

* Barre de recherche => Panneau de configuration.

![test panneau de config 1](https://github.com/Fairskip/Quest_GPO/blob/main/GPO%20test%20Panneau%20de%20config%201.png)

* Cliquer dessus pour le lancer.

![test panneau de config 1](https://github.com/Fairskip/Quest_GPO/blob/main/GPO%20test%20Panneau%20de%20config%202.png)
