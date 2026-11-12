# Ore Glow (Fabric, Minecraft 26.2) - UNGETESTET

Erze leuchten wie Lichtbloecke. Einstellungen im Spiel mit dem Befehl `/oreglow`.

## Bauen
1. JDK 25 installieren.
2. Einfachster Weg: Fabric-Template fuer 26.2 erzeugen (https://fabricmc.net/develop/template/)
   und die Ordner `src/` sowie `build.gradle`, `gradle.properties` aus diesem Projekt hineinkopieren.
   (Alternativ: Gradle 9.x installieren und in diesem Ordner `gradle wrapper` ausfuehren.)
3. `./gradlew build`  ->  fertige Mod: `build/libs/oreglow-1.0.0.jar`

## Benutzen
- Mods-Ordner: oreglow-1.0.0.jar + Fabric API + YACL (Yet Another Config Lib).
- Im Spiel `/oreglow` eingeben, Erze einstellen, "Fertig" klicken.
- Es wird ein Resource Pack "OreGlow" in `resourcepacks/` erzeugt:
  einmal aktivieren, danach nach jeder Aenderung F3+T druecken.
- Fuer das optische Leuchten der Texturen: Iris oder OptiFine.
- Helligkeit gilt nach Neuladen der Chunks (Welt neu betreten); bereits gespeicherte
  Chunks behalten ggf. ihr altes Licht, bis dort ein Lichtupdate passiert.

## Wenn der Build Fehler meldet
Das Projekt wurde ohne Compiler geschrieben. Kandidaten fuer Namensaenderungen in 26.x:
`ClientCommands`, `BlockStateBase.getLightEmission`, YACL-Imports. Fehlermeldung schicken -> ich korrigiere.
