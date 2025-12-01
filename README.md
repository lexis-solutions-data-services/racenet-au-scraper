# Racenet AU Horse Profile Scraper

![banner](https://i.ibb.co/CpMXLVM6/Screenshot-2025-11-16-at-8-14-48-PM.png)

This Actor scrapes detailed horse racing profiles from Racenet.com.au, extracting comprehensive information about horses including their statistics, breeding information, race history, and connections.

<p align="center">
  <img src="https://apify-image-uploads-prod.s3.us-east-1.amazonaws.com/DevbkY3adMTBuoECt-actor-fqOcgHaLpZ3pFAmFr-Ul7eUn1wPH-Screenshot_2025-11-23_at_12.40.03.png" alt="Racenet.com.au Scraper" style="height: 60px; margin-right: 15px;" /><a href="https://apify.com/lexis-solutions/racenet-au-scraper" target="_blank">
    <img src="https://img.shields.io/badge/Try%20it%20on-Apify-0066FF?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNDA4IiBoZWlnaHQ9IjQwOCIgdmlld0JveD0iMCAwIDQwOCA0MDgiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxnIGNsaXAtcGF0aD0idXJsKCNjbGlwMF8zNDFfNDE1NykiPgo8cGF0aCBkPSJNMjE4LjY5NSAxMDRIMzAwLjk3QzMwMi42NDMgMTA0IDMwNCAxMDUuMzU3IDMwNCAxMDcuMDNWMjMyLjc2NkMzMDQgMjM1Ljc3OCAzMDAuMDgzIDIzNi45NDUgMjk4LjQzNCAyMzQuNDI1TDIxNi4xNTkgMTA4LjY5QzIxNC44NDEgMTA2LjY3NCAyMTYuMjg3IDEwNCAyMTguNjk1IDEwNFoiIGZpbGw9IndoaXRlIi8+CjxwYXRoIGQ9Ik0xODkuMzA1IDEwNEgxMDcuMDNDMTA1LjM1NyAxMDQgMTA0IDEwNS4zNTcgMTA0IDEwNy4wM1YyMzIuNzY2QzEwNCAyMzUuNzc4IDEwNy45MTcgMjM2Ljk0NSAxMDkuNTY2IDIzNC40MjVMMTkxLjg0IDEwOC42OUMxOTMuMTU5IDEwNi42NzQgMTkxLjcxMyAxMDQgMTg5LjMwNSAxMDRaIiBmaWxsPSJ3aGl0ZSIvPgo8cGF0aCBkPSJNMjAyLjU5MSAyMDQuNjY4TDEwOS4xMjcgMjk4LjgzNUMxMDcuMjI5IDMwMC43NDcgMTA4LjU4MyAzMDQgMTExLjI3OCAzMDRIMjk2LjhDMjk5LjQ4MyAzMDQgMzAwLjg0MiAzMDAuNzcgMjk4Ljk2NyAyOTguODUyTDIwNi45MDggMjA0LjY4NUMyMDUuNzI2IDIwMy40NzUgMjAzLjc4MiAyMDMuNDY4IDIwMi41OTEgMjA0LjY2OFoiIGZpbGw9IndoaXRlIi8+CjwvZz4KPGRlZnM+CjxjbGlwUGF0aCBpZD0iY2xpcDBfMzQxXzQxNTciPgo8cmVjdCB3aWR0aD0iMjAwIiBoZWlnaHQ9IjIwMCIgZmlsbD0id2hpdGUiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDEwNCAxMDQpIi8+CjwvY2xpcFBhdGg+CjwvZGVmcz4KPC9zdmc+Cg==&logoColor=white" alt="Try it on Apify" style="border-radius: 12px; height: 60px;" />
  </a>
</p>



## 📊 Actor Stats

| Stat | Value |
|------|-------|
| **Version** | `0.0.1` |
| **Last Update** | Dec 1, 2025 |

---



## 💻 Integration Examples

This repository includes example code showing how to integrate the `racenet-au-scraper` actor into your projects.

You can find example implementations in the [`examples/`](./examples) folder:
- **TypeScript/JavaScript**: See [`examples/typescript/`](./examples/typescript) for a complete TypeScript example
- **Python**: See [`examples/python/`](./examples/python) for a complete Python example

Each example includes:
- Ready-to-use code templates
- Setup instructions
- Documentation links

---


## Features

- Horse profile data: id, name, slug, colour, sex, sexShort, age, country, imageUrl, silkImageUrl, foalDate, racingColours, etc.
- Breeding details: sire, sireCountry, dam, damCountry, breeder.
- Connections: owner, trainer, jockey.
- Performance stats: totalRuns, totalWins, totalSeconds, totalThirds, winPercentage, placePercentage, totalPrizeMoney.
- Previous runs: id, date, venue, eventName, eventDistance, finishPosition, totalStarters, jockey, and more.

## Input

The Actor accepts the following input parameters:

```json
{
    "startUrls": [
        {
            "url": "https://www.racenet.com.au/profiles/horse/briasa-aus"
        }
    ],
    "proxyConfiguration": {
        "useApifyProxy": false
    }
}
```

### Input Parameters

- **startUrls** (required) - Array of horse profile URLs to scrape
  - Format: `https://www.racenet.com.au/profiles/horse/{horse-slug}`
- **proxyConfiguration** (optional) - Proxy settings for the crawler

## Output

The Actor outputs structured data for each horse profile:

```json
{
    "url": "https://www.racenet.com.au/profiles/horse/briasa-aus",
    "scrapedAt": "2024-11-16T14:54:00.000Z",
    "horse": {
        "id": "12345",
        "name": "Briasa",
        "slug": "briasa-aus",
        "colour": "Bay",
        "sex": "Mare",
        "sexShort": "M",
        "age": 5,
        "country": "AUS",
        "imageUrl": "...",
        "silkImageUrl": "...",
        "foalDate": "2019-09-15",
        "racingColours": "..."
    },
    "breeding": {
        "sire": "Sire Name",
        "sireCountry": "AUS",
        "dam": "Dam Name",
        "damCountry": "AUS",
        "breeder": "Breeder Name"
    },
    "connections": {
        "owner": "Owner Name",
        "trainer": {
            "id": "67890",
            "name": "Trainer Name",
            "slug": "trainer-slug",
            "location": "Location"
        }
    },
    "stats": {
        "totalRuns": 15,
        "totalWins": 3,
        "totalSeconds": 4,
        "totalThirds": 2,
        "winPercentage": 20.0,
        "placePercentage": 60.0,
        "totalPrizeMoney": 150000
    },
    "previousRuns": [
        {
            "id": "run123",
            "date": "2024-10-15",
            "venue": "Flemington",
            "eventName": "Melbourne Cup",
            "eventDistance": 3200,
            "finishPosition": 1,
            "totalStarters": 24,
            "jockey": {
                "id": "jockey123",
                "name": "Jockey Name"
            }
        }
    ]
}
```

---

👀 p.s.

Got feedback or need an extension?

Lexis Solutions is a [certified Apify Partner](https://apify.com/partners/find). We can help you with custom solutions or data extraction projects.

Contact us over [Email](mailto:scraping@lexis.solutions) or [LinkedIn](https://www.linkedin.com/company/lexis-solutions)

## Support Our Work 💝

If you're happy with our work and scrapers, you're welcome to leave us a company review [here](https://apify.com/partners/find/lexis-solutions/review) and leave a review for the scrapers you're subscribed to. It will take you less than a minute but it will mean a lot to us!
