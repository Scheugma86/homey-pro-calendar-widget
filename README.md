
<body>

<h1>Homey Seasonal Calendar Widget</h1>

<blockquote>
    <p>English below · Deutsche Beschreibung unten</p>
</blockquote>

<h2>🇩🇪 Deutsch</h2>

<p>
    Ein kompakter Kalender-Widget mit saisonalen Animationen, deutschen Feiertagen und Spezialtagen
    für Beziehungen und Geburtstage. Ideal für Tablets oder Smart-Home-Displays
    (z. B. Homey-Wandtablet).
</p>

<h3>Features</h3>

<ul>
    <li>
        🎄 <strong>Weihnachten</strong>
        <ul>
            <li>Zeitraum: 26 Tage vor bis 2 Tage nach Weihnachten</li>
            <li>Schneeflocken, Schnee-Boden mit Glitzereffekt, animierter 🎄</li>
            <li>Intensität steigt, je näher der 24./25. kommt</li>
        </ul>
    </li>
    <li>
        🐰 <strong>Ostern</strong>
        <ul>
            <li>Zeitraum: 26 Tage vor bis 2 Tage nach Ostersonntag</li>
            <li>Fallende Eier/Frühlings-Symbole, Wiesenboden, animierter 🐰</li>
            <li>Ostersonntag wird per Algorithmus automatisch berechnet</li>
        </ul>
    </li>
    <li>
        💕 <strong>Spezialtage</strong>
        <ul>
            <li>Hochzeitstag: 💍-Animation, goldene Hervorhebung</li>
            <li>Geburtstage: 🎂-Animation, Konfetti, spezielles Event-Styling</li>
            <li>Monatliche „Anniversary Days“: dezente Herz-Animation</li>
        </ul>
    </li>
    <li>
        🇩🇪 <strong>Deutsche Feiertage</strong>
        <ul>
            <li>Automatische Berechnung der wichtigsten bundesweiten Feiertage</li>
            <li>Einschließlich beweglicher Feiertage (Karfreitag, Ostern, Himmelfahrt, Pfingsten)</li>
            <li>Feiertage erscheinen automatisch im Kalender mit speziellen Badges</li>
        </ul>
    </li>
    <li>
        🎨 <strong>UI &amp; Layout</strong>
        <ul>
            <li>Kompakte, gut lesbare Event-Karten (Heute / Morgen)</li>
            <li>Dark-/Light-Mode via <code>prefers-color-scheme</code></li>
            <li>Footer mit „Tap-to-Refresh“ statt Floating-Button</li>
            <li>Boden-Effekte (Schnee, Wiese, etc.) ohne das Event-Layout zu stören</li>
        </ul>
    </li>
    <li>
        🧪 <strong>Testmodus</strong>
        <ul>
            <li>Über <code>?testdate=YYYY-MM-DD</code> kann ein beliebiges Datum simuliert werden</li>
            <li>Beispiel: <code>?testdate=2024-12-24</code> für Heiligabend</li>
        </ul>
    </li>
</ul>

<h3>Konfiguration</h3>

<h4>1. Spezialdaten anpassen</h4>

<pre><code>const SPECIAL_DATES = {
    // Monatlicher Beziehungs-/Anniversary-Tag (Tag im Monat)
    anniversaryDay: 22,

    // Hochzeitstag
    weddingDay: { day: 1, month: 7, year: 2017 },

    // Geburtstage
    birthdays: [
        { name: "Partner 1", day: 3, month: 8, year: 1993 },
        { name: "Partner 2", day: 23, month: 10, year: 1986 }
    ]
};
</code></pre>

<h4>2. Kalender-URLs eintragen</h4>

<pre><code>const calendars = [
    {
        name: "Work",
        url: "https://YOUR_WORK_ICS_URL",
        color: "#3b82f6",
        class: "partner2"
    },
    {
        name: "Personal",
        url: "https://YOUR_PERSONAL_ICS_URL",
        color: "#ec4899",
        class: "partner1"
    },
    {
        name: "Shared",
        url: "https://YOUR_SHARED_ICS_URL",
        color: "#38bdf8",
        class: "shared"
    }
];
</code></pre>

<p>
    Unterstützt werden z. B. iCloud-, Google- oder andere ICS-Public-Links.
</p>

<h4>3. Home-Location für Fahrzeiten</h4>

<pre><code>const HOME_LAT = 48.1351;  // Deine Breitengrad
const HOME_LON = 11.5820;  // Dein Längengrad
</code></pre>

<p>
    Damit berechnet das Widget einfache Fahrzeiten zum Termin-Ort und zeigt an,
    wann du losfahren solltest.
</p>

<blockquote>
    Hinweis: Die Reisezeit basiert auf einer groben Distanz-Schätzung und
    OpenStreetMap Nominatim. Für produktiven Einsatz sind Caching / eigener Proxy sinnvoll.
</blockquote>

<h4>Nutzung</h4>

<ol>
    <li>Repository klonen oder ZIP herunterladen</li>
    <li><code>calendar.html</code> im Browser öffnen</li>
    <li>Optional per lokalem Webserver auf einem Wand-Tablet im Kioskmodus anzeigen</li>
</ol>

<hr>

<h2>🇬🇧 English</h2>

<p>
    A compact calendar widget with seasonal animations, German public holidays and
    relationship-related special days (birthdays, wedding anniversary, monthly anniversaries).
    Designed for tablets or smart-home displays (e.g. a Homey wall tablet).
</p>

<h3>Features</h3>

<ul>
    <li>
        🎄 <strong>Christmas</strong>
        <ul>
            <li>Active from 26 days before to 2 days after Christmas</li>
            <li>Falling snow, snowy ground with sparkles, animated 🎄 accent</li>
            <li>Animation intensity increases as you get closer to Christmas</li>
        </ul>
    </li>
    <li>
        🐰 <strong>Easter</strong>
        <ul>
            <li>Active from 26 days before to 2 days after Easter Sunday</li>
            <li>Falling eggs/spring symbols, meadow ground, animated 🐰 accent</li>
            <li>Easter Sunday is calculated automatically via algorithm</li>
        </ul>
    </li>
    <li>
        💕 <strong>Special days</strong>
        <ul>
            <li>Wedding anniversary: 💍 animation, golden styling</li>
            <li>Birthdays: 🎂 animation, confetti, special event styling</li>
            <li>Monthly anniversary day: subtle heart animation</li>
        </ul>
    </li>
    <li>
        🇩🇪 <strong>German public holidays</strong>
        <ul>
            <li>Automatic calculation of major German public holidays</li>
            <li>Includes Easter-related holidays (Good Friday, Easter, Ascension, Pentecost)</li>
            <li>Holidays appear automatically with special badges</li>
        </ul>
    </li>
    <li>
        🎨 <strong>UI &amp; layout</strong>
        <ul>
            <li>Clean, compact event cards (today / tomorrow)</li>
            <li>Dark/light mode via <code>prefers-color-scheme</code></li>
            <li>Footer with clickable “refresh” instead of a floating button</li>
            <li>Seasonal ground effects that don’t interfere with event content</li>
        </ul>
    </li>
    <li>
        🧪 <strong>Test mode</strong>
        <ul>
            <li>Use <code>?testdate=YYYY-MM-DD</code> to simulate any date</li>
            <li>Example: <code>?testdate=2024-12-24</code> for Christmas Eve</li>
        </ul>
    </li>
</ul>

<h3>Configuration</h3>

<h4>1. Special dates</h4>

<pre><code>const SPECIAL_DATES = {
    anniversaryDay: 22, // Monthly relationship anniversary

    weddingDay: { day: 1, month: 7, year: 2017 }, // Wedding date

    birthdays: [
        { name: "Partner 1", day: 3, month: 8, year: 1993 },
        { name: "Partner 2", day: 23, month: 10, year: 1986 }
    ]
};
</code></pre>

<h4>2. Calendar URLs</h4>

<pre><code>const calendars = [
    {
        name: "Work",
        url: "https://YOUR_WORK_ICS_URL",
        color: "#3b82f6",
        class: "partner2"
    },
    {
        name: "Personal",
        url: "https://YOUR_PERSONAL_ICS_URL",
        color: "#ec4899",
        class: "partner1"
    },
    {
        name: "Shared",
        url: "https://YOUR_SHARED_ICS_URL",
        color: "#38bdf8",
        class: "shared"
    }
];
</code></pre>

<p>
    You can use iCloud, Google or any other public ICS feed.
</p>

<h4>3. Home coordinates for travel time</h4>

<pre><code>const HOME_LAT = 48.1351;  // Your latitude
const HOME_LON = 11.5820;  // Your longitude
</code></pre>

<p>
    The widget estimates travel time and shows when you should leave for an appointment.
</p>

<blockquote>
    Note: Travel time is a simple approximation based on distance and OpenStreetMap Nominatim.
    For production use, consider caching or your own proxy.
</blockquote>

<h4>Usage</h4>

<ol>
    <li>Clone the repository or download the ZIP</li>
    <li>Open <code>calendar.html</code> in your browser</li>
    <li>Optionally serve it via a local web server and display it on a wall tablet in kiosk mode</li>
</ol>

<h2>License</h2>

<p>
    This project is licensed under the MIT License. See the <code>LICENSE</code> file for details.
</p>

</body>
</html>
