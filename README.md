Vaja 7 CubeMX

2.
b) V level Pinout oknu razširite nabor možnosti za Timers ter za časovnik TIM1. Clock source nastavite kot Internal Clock.
   Prvi kanal aktivirajte kot PWM Generation CH1. Kateri pin ste omogočili? Kaj se izpiše poleg pina?
   - Omogočili smo pin "PA8". Poleg pina se izpiše "TIM1_CH1".

d) V oknu Configuration kliknemo za TIM1. Vrednost Prescaler v zavihku Counter settings določite tako, da bo časovnik delal s frekvenco 1 MHz. Koliko je vrednost Prescaler?
   - Vrednost Prescaler je 16.

e) Parameter Counter Period nastavimo na 100 in s tem še dodatno znižamo takt časovnika. Koliko znaša sedaj?
   - Sedaj znaša 10 kHz.

f) V PWM Generation Channel nastavite Pulse (16 bits value) na 50. Kaj pomeni ta parameter?
  - Ta parameter pomeni vrednost širine pulza. V tem primeru je 50-odstotna.


3.
c) Poiščite prenastavljeni parameter Pulse (ki je 50) v vaši kodi in prepišite ukaz, ki ga je generiral CubeMX.
   - Parameter je sConfigOC.Pulse = 50;


5.
a) V kodi spremenite vrednost širine pulza na 25%. Zapišite popravljeni ukaz v kodi.
   - sConfigOC.Pulse = 25;

c) Zapišite, kaj počnejo ukazi v 1., 2. in 3. vrstici.
   - a) Na začetku zanke se nastavi htim1.Instance - CCR1 na vrednost dutyCycla.

     b) Ko program izvede loop skozi to vrstico, doda spremenljivki 10 dutyCycla.

     c) Preveri, če je vrednost dutyCycla večja od 90, če je, nastavimo dutyCycle nazaj na 10 in zanka je neskončna.
  
