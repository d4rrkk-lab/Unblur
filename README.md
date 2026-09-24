# UNBLUR — wersja z backendem

Ta wersja naprawia problem `Failed to fetch`: przeglądarka NIE łączy się bezpośrednio z Replicate.
Frontend wysyła zdjęcie do `/api/deblur`, a funkcja serwerowa wywołuje Replicate.

## Uruchomienie lokalne

1. Zainstaluj Node.js.
2. W katalogu projektu:
   npm install
3. Ustaw zmienną:
   REPLICATE_API_TOKEN=r8_...
4. Uruchom:
   npx vercel dev
5. Otwórz adres podany przez Vercel.

## Wdrożenie

Wrzuć ten projekt do Vercel i w Settings → Environment Variables dodaj:
REPLICATE_API_TOKEN = Twój token Replicate

Nie wkładaj tokena do `public/index.html`.

Model: codeslake/ifan-defocus-deblur.
