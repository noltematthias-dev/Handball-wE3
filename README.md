Versionsbeschreibung: wE-Jugend Handball App

Update: 10.02.2024 - Optimierung der Benutzererfahrung (UX)

Heute wurden gezielte Verbesserungen am Interaktionsmodell vorgenommen, um die Bedienung auf mobilen Geräten (Smartphones) flüssiger und intuitiver zu gestalten.

1. Intelligente Scroll-Logik im Overlay

Das Hauptproblem war bisher, dass das Scrollen durch lange Listen (z. B. Torschützen oder Team-Spielpläne) oft dazu führte, dass sich das Fenster versehentlich schloss.

Kontext-Sensitivität: Das Skript erkennt nun, ob du dich am Anfang der Liste befindest oder bereits nach unten gescrollt hast.

Scroll-Schutz: Solange du innerhalb der Liste nach unten oder oben scrollst, bleibt das Overlay stabil geöffnet.

Swipe-to-Close: Die Schließ-Geste (Wischen nach unten) wird nur noch dann aktiviert, wenn die Liste bereits ganz oben (scrollTop === 0) ist.

2. Visuelles Feedback beim Wischen

Um die Bedienung natürlicher wirken zu lassen, wurde ein direktes haptisch-visuelles Feedback eingebaut:

Mitgezogenes Fenster: Wenn du das Overlay am oberen Rand nach unten ziehst, folgt das Fenster nun aktiv deinem Finger ("Rubber-Banding"-Effekt), anstatt sofort hart zu schließen.

Dynamische Transitionen: Die Animationen wurden so angepasst, dass sie beim manuellen Ziehen deaktiviert sind (für direkte Reaktion) und beim Loslassen sanft zurückschnappen oder das Fenster schließen.

3. Schwellenwert für Schließ-Aktion

Es wurde eine Hysterese von 120 Pixeln implementiert. Das bedeutet, das Fenster schließt sich erst, wenn eine bewusste Abwärtsbewegung über diese Distanz erfolgt. Kleinere Zitterer oder kurzes Anscrollen führen nicht mehr zum Abbruch.

4. Automatische Reset-Funktion

Beim Öffnen eines neuen Teams oder der Torschützenliste wird der Scroll-Status des Fensters nun immer automatisch auf den Anfang gesetzt. Das verhindert, dass ein neues Fenster "mitten in der Liste" startet, wenn man vorher ein anderes Team betrachtet hat.

Status: Die App ist nun deutlich robuster gegen Fehlbedienungen während der Nutzung in der Halle oder unterwegs.
