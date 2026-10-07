# Pulseman — Traducción al español

[![Invítame a un café en Ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/johanderohan)

Ficha del proyecto, capturas y más traducciones al castellano en **[Parches en Castellano](https://parchesencastellano.com/traducciones/mega-drive/pulseman)**.

Traducción al **español de España** de *Pulseman* (Mega Drive, 1994),
el juego de acción de Game Freak publicado por SEGA.

La traducción se distribuye como **parche**: necesitas tu propia copia de la
ROM japonesa original. Este repositorio contiene únicamente este README;
el parche está en **[Releases](../../releases)**.

## Estado

Última versión: **[v1.0 — Historia en castellano](../../releases/tag/v1.0)**.

Traducción nueva realizada directamente desde los textos japoneses de la ROM,
con biblia de términos y revisión del contexto. Incluye **22 mensajes narrativos
distintos**, además de **36 cadenas de interfaz y créditos** y el agradecimiento
final. Los subtítulos dibujados como gráficos están incluidos en el parche.

| Parte | Estado |
|---|---|
| Introducción | Sus siete cartelas, incluidas las copias del segundo banco gráfico |
| Selección de fase | Las siete descripciones y el aviso de caso resuelto |
| Intervención de Waruyama | Traducida, incluida la explicación de la debilidad al agua |
| Cartela de cierre y desenlace | Traducidos, incluida la respuesta de Pulseman |
| Interfaz y créditos | Menú principal, ajustes, mando, mensajes de acceso y cargos del equipo |
| Ortografía | Tildes, eñes y signos de apertura en los subtítulos; mayúsculas acentuadas en la interfaz |
| Revisión durante una partida | Parcial; pruebas dirigidas de escenas y de las siete fases |

**Se conservan el logotipo y los rótulos grandes de la identidad visual del
juego**, como STAGE SELECT y los grafismos de televisión. También permanecen
las voces japonesas, las marcas, los nombres originales del equipo y de las
piezas musicales, los nombres del globo, el marcador y los textos decorativos
de escenarios y pantallas informáticas. No se añade doblaje ni subtitulado
nuevo a voces que no tenían texto en el original.

### Comprobaciones y límites

Se han comprobado en **Genesis Plus GX** la introducción completa, las siete
descripciones de fase, los avisos de caso resuelto, la intervención de Waruyama,
la cartela de cierre, el desenlace, los créditos y el agradecimiento final.
También se han probado una partida nueva por los menús, el inicio y el movimiento
en las siete fases mediante pruebas dirigidas, y la demostración automática.

El parche se ha aplicado de nuevo sobre el original y el resultado coincide
**byte a byte** con la ROM preparada. Se verifican tamaño, checksum de Mega Drive,
punteros y límites de los gráficos. Las pruebas dirigidas usan cambios en la
memoria del emulador para acceder a escenas; **el parche no incluye esos atajos**.

Quedan pendientes una partida completa sin ayudas y la prueba en consola física.
La traducción y su revisión han contado con asistencia de IA; no es una
localización oficial ni una revisión profesional humana certificada.

## Biblia de términos y estilo

Castellano de España, con «ordenador», tuteo y una redacción que conserva el tono
de aventura tecnológica. La compañera del protagonista habla con cercanía;
la presentadora del final mantiene el tono de un informativo. Los subtítulos
conservan los tiempos y las áreas de presentación originales.

| Japonés / original | Castellano | Criterio |
|---|---|---|
| パルスマン | Pulseman | Nombre propio y título |
| パルス | Pulse | Apelativo de su compañera |
| 好山博士 | doctor Yoshiyama | Tratamiento y apellido del científico |
| ドク・ワルヤマ | Doc Waruyama | Nombre del antagonista |
| ギャラクシィ・ギャング / G・G | Galaxy Gang / G.G. | Nombre y sigla de la organización |
| 人工生命体 | forma de vida artificial | Se evita convertirla en un robot |
| 現実界 / コンピュータ空間 | mundo real / mundo digital | Terminología coherente en la introducción |
| 本部 | cuartel general | Igual en la misión y en el informativo |
| STAGE | fase | El gran rótulo gráfico STAGE SELECT se conserva |
| VOLTTECCER | VOLTTECCER | Nombre de la técnica, con la grafía del juego |

La fecha de la introducción sigue siendo **1999**, como en la ROM. El contexto
general y los nombres se han contrastado con la [ficha oficial de SEGA](https://vc.sega.jp/vc_pulseman/).

## Cómo aplicar el parche

1. Descarga **[Pulseman-es-ES-v1.0.xdelta](../../releases/download/v1.0/Pulseman-es-ES-v1.0.xdelta)**.
2. Comprueba que tienes la ROM japonesa **original, sin cabecera adicional y sin
   otros parches**:

   | Dato | Valor |
   |---|---|
   | Archivo de referencia | `Pulseman (Japan).md` |
   | Tamaño | 2.097.152 bytes (2 MiB) |
   | CRC32 | `138A104E` |
   | MD5 | `b0952bec44386411651ad944c67cf86c` |
   | SHA-256 | `0ae94742bc82f01374297e8dc06dae806d7a5e4ed5537e380446e50c1b63715c` |

3. Aplica el parche con **[Delta Patcher](https://github.com/marco-calautti/DeltaPatcher/releases)**
   o con `xdelta3`:

   ```bash
   xdelta3 -d -s "Pulseman (Japan).md" Pulseman-es-ES-v1.0.xdelta "Pulseman (es-ES).md"
   ```

4. La ROM resultante ocupa **4.194.304 bytes (4 MiB)**. Su MD5 debe ser
   `b17b3ac173b8925e899ab4edd6429b6e` y su SHA-256:
   `e72a0e0098c57b6dffa6d046a0c2a3caeab9f8369a8a1bdd60f380bddd3acd9a`.
5. Inicia una partida nueva con la consola/emulador configurado como
   **Mega Drive japonesa, NTSC a 60 Hz**. Se conserva la región y la protección
   regional del original; este parche no adapta el juego a PAL.

Aplica cada versión sobre el **original japonés**, no sobre una ROM traducida.
La extensión `.bin` o `.md` no cambia la compatibilidad: deben coincidir el
tamaño y el hash. No cargues un estado de emulador creado con otra versión
del juego para comprobar la traducción.

## Aviso

Proyecto de traducción por afición, sin ánimo de lucro y sin relación con
Game Freak ni SEGA. No se distribuye la ROM, solo un parche para una copia propia.
Se mantienen los nombres y créditos del equipo original.

Si eres titular de los derechos y quieres que lo retire, abre una incidencia.
