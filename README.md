# [33176](https://www.pierron.fr/microcontroleur-arduinotm-son-et-lumiere-pb200-6451.html)-Module_son_et_lumière_pour_ARDUINO_PB200

<p align='center' width="100%">
    <img width="50%" src="https://github.com/pierron-asco-celda/33176-Module_son_et_lumiere_pour_ARDUINO_PB200/blob/main/33176.jpg">
</p>

<div align='justify'>

Cette maquette permet aux élèves de programmer l’émission de signaux sonores et lumineux. Elle dispose de 4 boutons-poussoirs pouvant piloter 4 LED de couleurs et un buzzer. La séance de base consiste à reproduire les sirènes des différents véhicules de secours. Polyvalente, elle pourra être utilisée autant par des collégiens que par des lycéens. L’accessibilité au microcontrôleur de la maquette permet à l’élève d’augmenter le potentiel pédagogique du dispositif en ajoutant LED, buzzer ou autre actionneur, en plus de ceux déjà précâblés. L’élève est ainsi acteur de ses apprentissages en réalisant les connexions de base d’un microcontrôleur, en programmant son dispositif augmenté et en créant éventuellement un mini projet “son et lumière” personnalisé.

</div>

## Caractéristiques techniques :

- Compatible Arduino™ Nano*

- 4 diodes électroluminescente

- 4 boutons poussoir

- 1 Buzzer

\*L'utilisation d'une carte non officielle peut altérer et restreindre l'expérience d'utilisation de la maquette !

## Ressources à télécharger

- Arduino IDE : [Télécharger](https://www.arduino.cc/en/software)

- mBlock : [Télécharger](https://mblock.cc/pages/downloads)

- Documentation : [Télécharger](https://github.com/pierron-asco-celda/33176-Module_son_et_lumiere_pour_ARDUINO_PB200/blob/main/MODULE%20SON%20ET%20LUMI%C3%88RE%20POUR%20ARDUINO%20PB200.txt)

## Programme de démonstration

```cpp
/*
   "MICROCONTRÔLEUR ARDUINO SON ET LUMIÈRE PB200" Pierron référence 33176
   Programme V1.0 : "Programme"
   Rédacteur : M. PAUL Pierre 2024

   *L'utilisation d'une carte non officielle nécessite la configuration "Old Booltloader" !
*/

// Déclarations des entrées et sorties.
#define DEL_VERTE 11
#define DEL_JAUNE 10
#define DEL_ROUGE 9
#define DEL_BLEUE 8
#define BOUTON_POUSSOIR_VERT 2
#define BOUTON_POUSSOIR_JAUNE 3
#define BOUTON_POUSSOIR_ROUGE 4
#define BOUTON_POUSSOIR_BLEU 5
#define BUZZER 12

void setup() {
  // Définition des entées et des sorties de la carte Arduino NANO.
  pinMode(DEL_VERTE, OUTPUT);
  pinMode(DEL_JAUNE, OUTPUT);
  pinMode(DEL_ROUGE, OUTPUT);
  pinMode(DEL_BLEUE, OUTPUT);
  pinMode(BOUTON_POUSSOIR_VERT, INPUT);
  pinMode(BOUTON_POUSSOIR_JAUNE, INPUT);
  pinMode(BOUTON_POUSSOIR_ROUGE, INPUT);
  pinMode(BOUTON_POUSSOIR_BLEU, INPUT);
  pinMode(BUZZER, OUTPUT);
}

void loop() {
  // Programme de démonstration.
  if (digitalRead(BOUTON_POUSSOIR_VERT) == HIGH)
  {
    digitalWrite(DEL_VERTE, HIGH);
    tone(BUZZER, 250);
    delay(250);
    noTone(BUZZER);
  }
  else
  {
    digitalWrite(DEL_VERTE, LOW);
  }
  if (digitalRead(BOUTON_POUSSOIR_JAUNE) == HIGH)
  {
    digitalWrite(DEL_JAUNE, HIGH);
    tone(BUZZER, 500);
    delay(250);
    noTone(BUZZER);
  }
  else
  {
    digitalWrite(DEL_JAUNE, LOW);
  }
    if (digitalRead(BOUTON_POUSSOIR_ROUGE) == HIGH)
  {
    digitalWrite(DEL_ROUGE, HIGH);
    tone(BUZZER, 750);
    delay(250);
    noTone(BUZZER);
  }
  else
  {
    digitalWrite(DEL_ROUGE, LOW);
  }
    if (digitalRead(BOUTON_POUSSOIR_BLEU) == HIGH)
  {
    digitalWrite(DEL_BLEUE, HIGH);
    tone(BUZZER, 1000);
    delay(250);
    noTone(BUZZER);
  }
  else
  {
    digitalWrite(DEL_BLEUE, LOW);
  }
}
```

#### À propos :
<div align='center'>

© [PIERRON - ASCO & CELDA](https://www.pierron.fr) 2024 - 62 rue de Siltzheim - 57200 RÉMELFING - France

</div>
