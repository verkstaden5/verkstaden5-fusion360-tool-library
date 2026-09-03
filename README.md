# Verkstaden 5 — verktygsbibliotek för Fusion 360

Officiellt verktygsbibliotek från [Verkstaden 5](https://verkstaden5.com) för
Autodesk Fusion. 113 hårdmetallfräsar med skärparametrar för nio material.
Fungerar med både Personal och kommersiell licens.

## Ladda ner

Hämta senaste versionen under [Releases](https://github.com/verkstaden5/verkstaden5-fusion360-tool-library/releases/latest).
Välj profil efter din maskin:

| Fil | Passar |
|---|---|
| `verkstaden5-fusion360-hobby.tools` | Skruv- eller remdriven maskin, trimfräs eller spindel upp till 1,5 kW |
| `verkstaden5-fusion360-industriell.tools` | Styv portalfräs med servodrift och spindel från 2,2 kW |

Osäker? Börja med **hobby** och gå upp. En för låg startpunkt kostar tid, en
för hög kostar frässtål.

Hobbyprofilen sänker skärdjup och stegbredd, kapar matningen vid 2 500 mm/min
och sänker varvtalet om chiploaden skulle hamna så lågt att verktyget gnider i
stället för att skära.

## Installera

1. Ladda ner `.tools`-filen och spara den på datorn.
2. Öppna Autodesk Fusion och gå till **Manufacture**-workspacet.
3. Klicka **Manage → Tool Library**.
4. Högerklicka på mappen **Local** (eller **Cloud**), välj **Import Library**
   och peka ut filen.

## Vad ingår

**Verktyg:** uppåt-, nedåt-, kompressions- och notfräsar, kulfräsar, V-bitar,
koniska radiefräsar, plan- och avrundningsfräsar, kopierfräs och PCB-fräsar.

**Material:** hårt trä, mjukt träslag/plywood, MDF/spånskiva, melamin, akryl,
hård plast, mjuk plast, aluminium och FR4/PCB.

Varje verktyg har ett preset per material med chipload, varvtal, matning och
dykhastighet. Skaftdiametern är korrekt angiven, så Fusions kollisionskontroll
mot uppspänning och fixturer fungerar som den ska.

## Om värdena

Detta är **startvärden för provfräsning**, inte facit. Justera efter din
maskin, uppspänning och material.

Ändringar per version finns i [CHANGELOG.md](CHANGELOG.md).

**Har du sparade verktygsbanor med `V-D6.0-TD0.1-60°-F5` behöver de räknas om
efter uppdatering till 2.0.0.** Spetsvinkeln var felaktigt angiven i tidigare
versioner av Vectric-databasen och värdet är nu enhetligt i båda programmen.

## Kul att veta

Biblioteket genereras ur en gemensam källa tillsammans med vår
[Vectric-databas](https://github.com/verkstaden5/verkstaden5-vectric-database).
Samma verktyg får därför identiska värden i båda programmen — det kontrolleras
automatiskt vid varje release.

## Om Verkstaden 5

Din svenska partner för CNC-tillbehör. Vi fokuserar på frässtål som håller
längre och ger bättre resultat.

[verkstaden5.com](https://verkstaden5.com) · [Frässtål](https://verkstaden5.com/collections/frasverktyg) · [Verktygsdatabaser](https://verkstaden5.com/pages/verktygsdatabaser)

Sponsra gärna arbetet: https://github.com/sponsors/verkstaden5
