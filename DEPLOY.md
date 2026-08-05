# KvizOpoly PWA: objava in preverjanje

## Najlažja objava: Cloudflare Pages Direct Upload

1. Razširi ZIP paket.
2. V Cloudflare odpri **Workers & Pages** in izberi ustvarjanje aplikacije Pages.
3. Izberi **Direct Upload**.
4. Naloži mapo, v kateri so neposredno datoteke `index.html`, `manifest.webmanifest`, `sw.js`, `offline.html`, `_headers` in mapa `icons`.
5. Odpri dodeljeni HTTPS naslov.

Pomembno: ne naloži zunanje mape, v kateri je še ena podmapa projekta. `index.html` mora biti v korenu objave.

## Namestitev na iPhone

1. Objavljeni HTTPS naslov odpri v Safariju.
2. Tapni gumb **Deli**.
3. Izberi **Dodaj na začetni zaslon**.
4. Potrdi **Dodaj**.
5. Aplikacijo nato odpri z ikono delfina na začetnem zaslonu.

## Obvezni preizkus po objavi

- Odpri `/manifest.webmanifest` in preveri, da se prikaže JSON.
- Odpri `/icons/apple-touch-icon.png` in preveri ikono delfina.
- Namesti aplikacijo na začetni zaslon.
- Ustvari testni kviz, zapri aplikacijo in jo znova odpri. Kviz mora ostati shranjen.
- Vklopi letalski način in znova odpri nameščeno aplikacijo. Domov, shranjeni kvizi in učenje morajo delovati.
- Uvoz Word dokumenta prvič preizkusi s povezavo, ker uporablja knjižnico Mammoth. Po prvem uspešnem nalaganju jo Service Worker shrani v runtime cache.
- Preizkusi beli in temni način.
- Preizkusi animacijo delfina in nastavitev Reduce Motion.

## Posodobitve

Ob vsaki novi izdaji spremeni ime cachea v `sw.js` in znova naloži vse datoteke. Ta paket uporablja `kvizopoly-v16`.
