---
# try also 'default' to start simple
theme: default
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://cover.sli.dev
# some information about your slides (markdown enabled)
title: Title
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# apply UnoCSS classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
# duration of the presentation
duration: 35min
---

# Journée des métiers

Présentation de parcours RIM - Pierre Cochard

Université Jean Monnet, 13 Février 2026

<div @click="$slidev.nav.next" class="mt-12 py-1" hover:bg="white op-10">
  <carbon:arrow-right />
</div>

<div class="abs-br m-6 text-xl">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="slidev-icon-btn">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
transition: fade-out
---

# Sommaire

<!-- <style> ul li {font-size: 30px} </style> -->

<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/features/slide-scope-style
-->

<Toc text-sm minDepth="1" maxDepth="1" />


<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

<!--
Here is another comment.
-->

---
transition: fade-out
---

# **Parcours personnel initial**

<br>

<v-clicks>

- **Licence Médiation Culturelle & Communication**
  - *ICT Toulouse, 2010*
- **Master Expertise des Professions et Institutions de la Culture**
  - Université de Nantes, 2011-2012

</v-clicks>

<br>

<v-clicks>

- ***Autodidacte***, pas de formation musicale académique (Conservatoire, Université)
- Pratique instrumentale amateur (guitare, claviers)
- Pratique **MAO** (**Cubase**), **Max/MSP** (v5), **NI Reaktor**, ...
- Composition musique électronique/électroacoustique, 
- Animation émission de radio (Nantes, JetFM)

</v-clicks>

<style> ul li {font-size: 22px} </style>

---
transition: fade-out
---

# **Master RIM (2013-2014)**

<br>

- Entrée sur dossier, entretien (L. Pottier, Y. Orlarey)
- Etudiants avec **parcours très variés**
- Programme **très complet** (et très dense) : 
  - **Techniques/ingénierie du son**
  - **Langages de programmation** (Faust, Max, Csound, C, Lisp, ...)
  - **Composition, formation musicale**
  - **Ethnomusicologie, histoire de la musique** 
  - *etc.*
- **Projets personnels**
- **Stages**

<!-- Ajouter autres slides avec screenshots de projets faits pendant le master -->

<style> ul li {font-size: 21px} </style>

---
transition: fade-out
layout: image
image: media/master-rim/la-marche-des-anges.png
backgroundSize: 75%
---

---
transition: fade-out
layout: image
image: media/master-rim/selvanscapes.png
backgroundSize: 75%
---

---
transition: fade-out
layout: two-cols-header
# image: 
# backgroundSize: 90%
---

<!-- ![](./media/master-rim/organisation-synthese.jpg) -->
<!-- <div class="absolute left-10px "> -->

# Hello

::left::

<div class="absolute left--260px top--100px">
<img src="./media/master-rim/selvanscapes.png" scale="45%" />
</div>

::right::

<div class="absolute right--360px top--570px">
<img src="./media/master-rim/organisation-synthese.jpg" scale="40%" />
</div>

<style>
.two-cols-header {
  column-gap: 10px; /* Adjust the gap size as needed */
}
</style>

<!-- </div> -->

---
transition: fade-out
layout: image
image: media/master-rim/selvanScapes-chronologie-projet.jpg
backgroundSize: 75%
---

---
transition: fade-out
layout: image-right
image: media/master-rim/birds.png
backgroundSize: 75%
---

## **Projet Faust, 'birds'**

<br>

```js
/*:
- Bird singing generator.
- Head = Reverberation, birds heard from far away.
- Bottom = Maximum proximity of the birds.
- Right = maximum speed of whistles.
- Left = minimum speed, birds rarely heard.
*/

process = hgroup("Birds", 
    mainOsc(
        noteTrig 
      : rdm(72,94) 
      : mtof, noteTrig) 
      * envWrapper(noteTrig, ampEnv, amp_xp(2510)) 
      : fi.lowpass(1, 2000) *(0.8) 
      <: _,_, (rdmPanner : panSte) 
      : panConnect 
      : *,* 
      : reverb
);

// ...
```


---
transition: fade-out
---

# **Stages**

<br>

<v-clicks>

## **Décembre-Janvier 2014 - APO33 (Nantes)**

 <br>

> -  Réalisation d'une interface **Qt5** (*C++*) pour logiciel de streaming open-source (*IceStream*)

</v-clicks>

<br>

<v-clicks>

## **Mai-Août 2014 - SCRIME-LaBRI (Bordeaux)**

<br>

> - **Assistant RIM** (J. Larralde)
> - **Embauche dès la fin du stage** \o/

</v-clicks>

<style> ul li {font-size: 22px} </style>

---
transition: fade-out
---

# **Réalisateur en informatique musicale, SCRIME-LaBRI (Bordeaux, 2014-2017)**

<br>

## **Opérateur studio, maintenance des équipements**

<br>

<v-clicks>

- **Studio octophonique** (8x Genelec 1030 + 2x Genelec 1037)
- Devenu '**Dôme 3D**' en 2017 (18 Genelec 8030 6'5)
- Salle de conférence, studio concert '**Hémicyclia**' 
  - **Acousmonium** modulaire (24 HP)
- Pilotage **Pro Tools** (avec contrôleur dédié)
- Gestion et maintenance du parc informatique (*macOS*)

</v-clicks>

<style> ul li {font-size: 22px} </style>

<!--  Ajouter screenshots studios -->

---
transition: fade-out
---

## **Studio Elise**

<br>

<!-- <img src="/home/pierre/Repositories/presentations/ujm-journee-metiers-2026/media/studios-scrime/scrime-studio-elise-new.jpg"  width="300" height="300"> -->


<style> ul li {font-size: 22px} </style>

---
transition: fade-out
---

## **Salle *Hémicyclia***

<br>

<!-- <img src="/home/pierre/Repositories/presentations/ujm-journee-metiers-2026/media/studios-scrime/scrime-studio-elise-new.jpg"  width="300" height="300"> -->


<style> ul li {font-size: 22px} </style>

---
transition: fade-out
---

## **Opérateur studio, maintenance des équipements**

<br>

- Former les utilisateurs au fonctionnement opérationnel des différents studios
  - Câblage, sécurité, ...
  - Prêt de matériel pour prises de son 
  - Bancs de montage audionumériques (Pro Tools, Reaper, Ableton Live)
    - Plugins de spatialisation

<br>

- Adapter les moyens techniques aux besoins des compositeurs
  - Disposition des haut-parleurs (Acousmonium *Hémicyclia*)

<!-- Schéma du patch Neutrik par ex.  -->

<style> ul li {font-size: 22px} </style>

---
transition: fade-out
---

## **Technicien/ingénieur son pour concerts et évènements**
<br>

<v-clicks>

- **Concerts-lecture** avec compositeur invité (Forum de Talence) ~ *1x/mois*
  - Concerts spatialisés (*>= octophonie*)
  - *projetés* en direct par les compositeurs eux-mêmes
- **Concerts thématiques**
  - *Piano Day*, *Hommage à Xenakis*, *Autechre*, *Raster-Noton*, *etc.*
- **Sorties de résidence**

<br>

- **Installations sonores**

<br>

- **Conférences** scientifiques/musique ou mixtes, workshops
  - Colloque *Chowning-Risset*

<br>

</v-clicks>

<style> ul li {font-size: 22px} </style>

---
transition: fade-out
---

## **Développement, *beta-testing* du logiciel *i-score* (ANR OSSIA)**

<br>

- Réalisation de démos
- Debugging, *bug reporting*
- Documentation, promotion
- Développement d'outils d'intégration avec d'autres environnements ou matériel audionumériques (Faust, SuperCollider, Max, Pure Data, etc.)

<!-- Ajouter présentation d'i-score avec screenshots, voire carrément vidéo -->
<!-- Block de code OSSIA-SuperCollider -->

<style> ul li {font-size: 22px} </style>

---
transition: fade-out
---

## **Accompagnement d'artistes en résidence de création**

<br>

- Expérimentations autour du logiciel *i-score* et spatialisation sonore :
  - **G. Gagneré** - *L'ombre*, d'Andersen (suivi de lecture)
  - **A. Bonardi** - *Pianotronics III*
  - **D. Garnier** - *L'arbre intégral*
  - **P. Cochard** - *quarrè (v1.0)*
- Accompagnement technique studio, acousmonium, programmation, création, sound-design, etc.
- Accompagnement pour sorties de résidence extérieures (tournée Arbre intégral)
- Feedback et support sur le logiciel *i-score*

<!-- Pas toujours évident avec des logiciels en développement, sachant que le spectacle vivant est un contexte plutôt critique -->

<!-- Ajouter media pour illustrer les différents projets -->

<style> ul li {font-size: 22px} </style>

---
transition: fade-out
---

## Activités universitaires, académiques (recherche, formation)

<br>

- Ateliers pour scolaires (Semaine du Son)
- Intervention des compositeurs dans les écoles/collèges/lycées
- Ateliers avec les étudiants de l'Université (Ableton Live)
- Workshops avec les élèves du Conservatoire (électroacoustique)
- Encadrement régulier de stagiaires

<br>

- Activités de recherche, écriture d'articles scientifiques


<style> ul li {font-size: 22px} </style>

---
transition: fade-out
---

# **Ingénieur projet Arts et Sciences, IdEx Bordeaux (2015-2016)**

- Faire le lien entre Arts et Sciences en invitant des artistes à collaborer avec des scientifiques de l'Université de Bordeaux.
- Gestion et suivi de projets, accompagnement sur aspects techniques, etc.

<!-- <SlidevVideo v-click autoplay controls> -->
  <!-- Anything that can go in an HTML video element. -->
  <!-- <source src="/myMovie.mp4" type="video/mp4" /> -->
  <!-- <source src="/myMovie.webm" type="video/webm" /> -->
  <!-- <p>
    Your browser does not support videos. You may download it
    <a href="/myMovie.mp4">here</a>.
  </p>
</SlidevVideo> -->


<style> ul li {font-size: 22px} </style>

---
transition: fade-out
---

# **Réalisateur en informatique musicale (freelance, Nantes, 2017-2020)**

- projet *quarrè*, installation sonore immersive et interactive
  - soutenu par le SCRIME, le CRNA (Cultures Connectées)
  - utilisation d'OSSIA score
  - 1 an d'écriture/programmation
  - Restitutions multiples

<style> ul li {font-size: 22px} </style>

---
transition: fade-out
---

# **Développeur C++ (PULSALYS, GRAME, 2020-2021)**

<style> ul li {font-size: 22px} </style>

---
transition: fade-out
---

# **Ingénieur de recherche, Equipe Emeraude, Inria, INSA-Lyon (Villeurbanne, 2022-2027)**

<style> ul li {font-size: 22px} </style>


---

<PoweredBySlidev mt-10/>