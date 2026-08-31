# ShopFlow – analiza danych e-commerce

## Narzędzia

- PostgreSQL
- DBeaver
- SQL
- Microsoft Excel
- Copilot

## Opis projektu

Dane pochodzą z symulowanego sklepu internetowego **ShopFlow**, działającego na rynku polskim w branży e-commerce, obejmującej m.in.:

- modę,
- elektronikę,
- dom i wnętrza,
- urodę.

Zbiór obejmuje około **85 000 rekordów** w 5 powiązanych tabelach:

- klienci – ok. 5 000 rekordów,
- produkty – ok. 2 000 rekordów,
- zamówienia – ok. 20 000 rekordów,
- pozycje zamówień – ok. 49 000 rekordów,
- stany magazynowe – 2 000 rekordów.

Dane obejmują **24 miesiące historii sprzedaży** i celowo zawierają typowe problemy jakości danych spotykane w rzeczywistych systemach, takie jak:

- duplikaty,
- braki danych,
- niespójne formaty,
- wartości odstające.

Problemy te zostały wykryte i naprawione w ramach projektu.

## Kontekst biznesowy

ShopFlow to sklep internetowy działający na polskim rynku e-commerce i sprzedający produkty w 8 kategoriach:

- moda damska,
- moda męska,
- dom i wnętrza,
- elektronika,
- uroda,
- sport,
- dziecko,
- akcesoria.

Dane sprzedażowe obejmują **24 miesiące działalności firmy**.

W danych widoczna jest sezonowość sprzedaży, m.in.:

- wysoka sprzedaż na przełomie listopada i grudnia związana z Black Friday i okresem świątecznym,
- spadki sprzedaży w styczniu.

## Struktura danych

Model relacyjny składa się z 5 tabel:

| Tabela | Liczba rekordów | Zawartość |
|---|---:|---|
| `customers` | ~5 000 | Dane klientów: lokalizacja, kanał pozyskania, data rejestracji, udział w programie lojalnościowym |
| `products` | ~2 000 | Katalog produktowy: kategoria, marka, cena, koszt, data wprowadzenia do oferty |
| `orders` | ~20 000 | Nagłówki zamówień: klient, data, status, metoda płatności, wartość, kanał marketingowy |
| `order_items` | ~49 000 | Pozycje zamówień: produkt, ilość, cena w momencie zakupu, rabat |
| `inventory` | 2 000 | Stany magazynowe: ilość na stanie, próg uzupełnienia, lokalizacja w magazynie |

## Charakterystyka danych

Zbiór został zaprojektowany tak, aby odzwierciedlać jakość danych spotykaną w realnych systemach transakcyjnych.

Obejmuje m.in.:

- duplikaty rekordów klientów i zamówień,
- braki danych,
- niespójne formaty dat,
- niespójne formaty numerów telefonów,
- niespójne kody pocztowe,
- niespójne nazwy miast i kategorii,
- wartości odstające w cenach,
- osierocone klucze obce.

Wszystkie te problemy zostały zidentyfikowane i naprawione w ramach projektu przy użyciu **SQL i PostgreSQL**, przed rozpoczęciem właściwej analizy danych.

## Zakres czasowy

**24 miesiące** danych historycznych, aktualnych na moment pobrania.
