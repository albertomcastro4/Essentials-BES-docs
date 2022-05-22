# Combates contra salvajes
## Tabla de contenidos
1. [Encuentros salvajes](#wild)
2. [Encuentros de evento](#event)
3. [Pokémon errantes](#roaming)

## **Encuentros salvajes** <a name="wild"></a>

Los encuentros salvajes se dan de forma aleatoria en determinadas situaciones. Estos encuentros se definen o bien desde la opción `Setear encuentros` del menú de Debug una vez ingame, o desde el PBS `encounters.txt`. 

```
039 # Ruta 4
25,10,10
Land
SHELLOS,12,15
SHELLOS,12,15
SHELLOS,12,15
GRIMER,13,15
GRIMER,13,15
GRIMER,13,15
GRIMER,13,15
GRIMER,13,15
MURKROW,12,14
MURKROW,12,14
MURKROW,12,14
MURKROW,12,14
```
<text font="2">Ejemplo de PBS de encuentros.</font>

Para definir los encuentros de un mapa, se escribe la ID del mapa seguida de tres números separados por comas, que representan la frecuencia o densidad de encuentro en el mapa para los distintos tipos de salvajes: 

- Densidad en hierba.
- Densidad en cueva.
- Densidad en agua (`Surf`).

Cuanto más alto sea este número, más frecuentes serán los encuentros de ese tipo. Los valores por defecto son `25, 10, 10`.

Hay varios tipos de encuentro, y las probabilidades y número de Pokémon permitidos dependen de estos. Cada tipo de encuentro tiene un número de slots predeterminado al que se le asigna un porcentaje de aparición.

|Encuentro|Descripción|Porcentajes|
|-|-|-
|Land|Encuentros de hierba alta normal.<br>Se generan al andar en tiles con [Terrain Tag](../maps/TerrainTags.md) 2.| 20, 20, 10, 10, 10, 10, 5, 5, 4, 4, 1, 1
|LandMorning|Encuentros de hierba alta normal por la mañana.<br>Se generan al andar en tiles con [Terrain Tag](../maps/TerrainTags.md) 2.| 20, 20, 10, 10, 10, 10, 5, 5, 4, 4, 1, 1
LandDay|Encuentros de hierba alta normal por el día.<br>Se generan al andar en tiles con [Terrain Tag](../maps/TerrainTags.md) 2.| 20, 20, 10, 10, 10, 10, 5, 5, 4, 4, 1, 1
LandNight|Encuentros de hierba alta normal por la noche.<br>Se generan al andar en tiles con [Terrain Tag](../maps/TerrainTags.md) 2.| 20, 20, 10, 10, 10, 10, 5, 5, 4, 4, 1, 1
Cave|Encuentros de cueva.| 20, 20, 10, 10, 10, 10, 5, 5, 4, 4, 1, 1
BugContest|Encuentros durante un concurso de cazar bichos.| 20, 20, 10, 10, 10, 10, 5, 5, 4, 4, 1, 1
Water|Encuentros al usar `Surf`| 60, 30, 5, 4, 1
OldRoad|Encuentros al usar `Caña Vieja` | 	70, 30
GoodRod|Encuentros al usar `Caña Buena` | 60, 20, 20
SuperRod|Encuentros al usar `Super Caña`|40, 40, 15, 4, 1
RockSmash|Encuentros al usar `Golpe Roca`|	60, 30, 5, 4, 1
HeadbuttLow|Encuentros al usar `Cabezazo`|30, 25, 20, 10, 5, 5, 4, 1
HeadbuttHigh|Encuentros al usar `Cabezazo`|30, 25, 20, 10, 5, 5, 4, 1

Para configurarlos, se escribe el nombre del encuentro seguido de los Pokémon que ocuparán cada slot, seguidos de su nível mínimo y máximo.
Si un Pokémon aparece en varios slots, se suman los porcentajes.

```
031 # Ruta 3
25,10,10
Land
NIDORANfE,12,15
NIDORANmA,12,15
NIDORANfE,12,15
NIDORANmA,12,15
PIKACHU,14,17
PIKACHU,14,17
PONYTA,13,15
PONYTA,13,15
EEVEE,15
EEVEE,15
EEVEE,15
EEVEE,15
Water
SURSKIT,13,14
LOTAD,14
LOTAD,14
LOTAD,15
LOTAD,15
RockSmash
NOSEPASS,13,14
GEODUDE,12,15
GEODUDE,12,15
GEODUDE,12,15
GEODUDE,12,15
OldRod
MAGIKARP,6,11
MAGIKARP,10,17
```
<text font="2">Ejemplo con varios encuentros definidos</text>

## **Encuentros de evento** <a name="event"></a>
