# portfolio.berry-secure.pl

Statyczne portfolio Michala Krzepkowskiego przygotowane pod Coolify.

## Lokalny podglad

```bash
cd portfolio-site
python3 -m http.server 4173
```

Adres lokalny:

```text
http://localhost:4173
```

## Docker

```bash
cd portfolio-site
docker build -t mk-portfolio .
docker run --rm -p 8080:80 mk-portfolio
```

## Coolify

1. Utworz nowy resource typu Dockerfile.
2. Jako build context wskaz katalog `portfolio-site`.
3. Ustaw public domain: `https://portfolio.berry-secure.pl`.
4. Port aplikacji: `80`.
5. W DNS dodaj rekord `A` albo `CNAME` subdomeny `portfolio.berry-secure.pl` na ten sam VPS, zgodnie z obecna konfiguracja Coolify.

Strona nie wymaga zmiennych srodowiskowych ani backendu.
