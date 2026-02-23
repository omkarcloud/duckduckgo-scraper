![DuckDuckGo Scraper Featured Image](https://raw.githubusercontent.com/omkarcloud/duckduckgo-scraper/master/duckduckgo-scraper-featured-image.png)

# DuckDuckGo Scraper API

Get real-time DuckDuckGo search results as structured JSON — organic results, knowledge panels, sponsored links, and related queries in one call. No headless browsers, no HTML parsing. 5,000 free requests/month.

## Key Features

- Search DuckDuckGo by keyword or with operators (`site:`, `inurl:`, `intitle:`)
- Get organic results with rank, title, URL, description, icon, dates, and sub-links
- Knowledge panels with descriptions, images, attributes, and social links
- Sponsored links with domains and sub-links
- Related queries for keyword research
- Limit/start pagination with built-in `next`/`previous` URLs
- **5,000 requests/month on free tier**
- Example Response:
```json
{
    "rank": 1,
    "title": "Mango: Nutrition, Health Benefits, and How to Eat It",
    "url": "https://www.healthline.com/nutrition/mango",
    "description": "Learn about the nutrients, antioxidants, and potential health benefits of mango, a tropical fruit with a low calorie density. Find out how to enjoy mango in various ways, such as smoothies, salads, or desserts.",
    "icon": "https://external-content.duckduckgo.com/ip3/www.healthline.com.ico",
    "date_text": "Jun 2, 2025",
    "published_at": "2025-06-02T00:00:00.0000000"
}
```

## Get API Key

Create an account at [omkar.cloud](https://www.omkar.cloud/auth/sign-up?redirect=/api-key) to get your API key.

It takes just 2 minutes to sign up. You get 5,000 free requests every month — more than enough for most developers to get their job done without paying a dime.

This is a well built product, and your search for the best DuckDuckGo Scraper API ends right here.


## Quick Start

```bash
curl -X GET "https://duckduckgo-scraper.omkar.cloud/duckduckgo/search?query=mango" \
  -H "API-Key: YOUR_API_KEY"
```

```json
{
  "result_count": 10,
  "limit": 10,
  "start": 0,
  "next": "https://duckduckgo-scraper.omkar.cloud/duckduckgo/search?query=mango&start=10&limit=10",
  "previous": null,
  "results": [
    {
      "rank": 1,
      "title": "Mango USA - Sale | Online fashion",
      "url": "https://shop.mango.com/us/en",
      "description": "SALE - Discover the latest in fashion, footwear and accessories at Mango.",
      "icon": "https://external-content.duckduckgo.com/ip3/shop.mango.com.ico"
    }
  ]
}
```

## Quick Start (Python)

```bash
pip install requests
```

```python
import requests

response = requests.get(
    "https://duckduckgo-scraper.omkar.cloud/duckduckgo/search",
    params={"query": "mango", "limit": 10},
    headers={"API-Key": "YOUR_API_KEY"}
)

print(response.json())
```


## API Reference

### Web Search

```
GET https://duckduckgo-scraper.omkar.cloud/duckduckgo/search
```

#### Parameters

| Parameter | Required | Default | Description |
|-----------|----------|---------|-------------|
| `query` | Yes | — | Search query. Keywords, phrases, or operators like `site:`, `inurl:`, `intitle:`. Max 500 characters. |
| `limit` | No | `50` | Max results to return. Range: `1` to `50`. |
| `start` | No | `0` | Number of results to skip. Use with `limit` to paginate. |

#### Example

```python
import requests

response = requests.get(
    "https://duckduckgo-scraper.omkar.cloud/duckduckgo/search",
    params={"query": "mango", "limit": 10},
    headers={"API-Key": "YOUR_API_KEY"}
)

print(response.json())
```

#### Response

<details>
<summary>Sample Response (click to expand)</summary>

```json
{
  "result_count": 10,
  "limit": 10,
  "start": 0,
  "next": "https://duckduckgo-scraper.omkar.cloud/duckduckgo/search?query=mango&start=10&limit=10",
  "previous": null,
  "results": [
    {
      "rank": 1,
      "title": "Mango USA - Sale | Online fashion",
      "url": "https://shop.mango.com/us/en",
      "description": "SALE - Discover the latest in fashion, footwear and accessories at Mango. Buy the best looks for this season and dress up to date. Enter NOW!",
      "icon": "https://external-content.duckduckgo.com/ip3/shop.mango.com.ico",
      "sub_links": [
        {
          "title": "Women",
          "url": "https://shop.mango.com/us/en/h/women",
          "description": "SALE - Latest trends in women's fashion. Discover our designs: dresses, tops, jeans, shoes, bags and accessories."
        },
        {
          "title": "Men",
          "url": "https://shop.mango.com/us/en/h/men",
          "description": "SALE - Latest trends in men's fashion: suits, shirts, trousers, jackets, jeans and shoes at exclusive prices."
        }
      ]
    },
    {
      "rank": 2,
      "title": "Mango: Nutrition, Health Benefits, and How to Eat It",
      "url": "https://www.healthline.com/nutrition/mango",
      "description": "Learn about the nutrients, antioxidants, and potential health benefits of mango, a tropical fruit with a low calorie density. Find out how to enjoy mango in various ways, such as smoothies, salads, or desserts.",
      "icon": "https://external-content.duckduckgo.com/ip3/www.healthline.com.ico",
      "date_text": "Jun 2, 2025",
      "published_at": "2025-06-02T00:00:00.0000000"
    },
    {
      "rank": 3,
      "title": "Mango - Wikipedia",
      "url": "https://en.wikipedia.org/wiki/Mango",
      "description": "Learn about the mango, an edible stone fruit produced by the tropical tree Mangifera indica. Discover its history, varieties, characteristics, and culinary and other uses.",
      "icon": "https://external-content.duckduckgo.com/ip3/en.wikipedia.org.ico"
    }
  ],
  "sponsored": [
    {
      "rank": 1,
      "title": "MANGO Man - Official Website - The best for this season",
      "url": "https://shop.mango.com/us/en/h/men",
      "domain": "mango.com",
      "description": "In Mango Man discover the latest trends in fashion, footwear and accessories. Discover the latest Trends in Men's Fashion. Shop Online the New Collection!",
      "sub_links": [
        {
          "title": "Best Sellers",
          "url": "https://shop.mango.com/us/en/c/men/best-sellers_6b44c326"
        },
        {
          "title": "New Now - Men",
          "url": "https://shop.mango.com/us/en/c/men/new-now_a4e1e34a"
        }
      ]
    }
  ],
  "knowledge_panel": {
    "title": "Mango",
    "description": "A mango is an edible stone fruit produced by the tropical tree Mangifera indica. It originated in the northeastern part of the Indian subcontinent...",
    "image": "https://duckduckgo.com/i/2d8ff37011fb6608.jpg",
    "related": [
      {
        "query": "Achaar , South Asian pickles, commonly containing mango and lime.",
        "url": "https://duckduckgo.com/South_Asian_pickles"
      },
      {
        "query": "Mangoes",
        "url": "https://duckduckgo.com/c/Mangoes"
      }
    ]
  },
  "related_queries": [
    {
      "query": "mango mango dessert"
    },
    {
      "query": "mango mango dessert nyc"
    },
    {
      "query": "mango clothing"
    }
  ]
}
```

</details>

## Error Handling

```python
response = requests.get(
    "https://duckduckgo-scraper.omkar.cloud/duckduckgo/search",
    params={"query": "mango"},
    headers={"API-Key": "YOUR_API_KEY"}
)

if response.status_code == 200:
    data = response.json()
elif response.status_code == 401:
    # Invalid API key
    pass
elif response.status_code == 429:
    # Rate limit exceeded
    pass
```

## FAQs

### What data does the API return?

**Web Search** returns per result:
- Rank, title, URL, description, favicon icon
- Publication date (when available)
- Sub-links with titles, URLs, and descriptions

**Additional sections** (when available for the query):
- **Knowledge panel** — title, description, image, attributes (facts), social links, related topics
- **Sponsored links** — rank, title, URL, domain, description, sub-links
- **News** — rank, title, URL, description, publisher, date, image
- **Related queries** — suggested search queries

All in structured JSON. Ready to use in your app.

### How accurate is the data?

Data is pulled from DuckDuckGo in real time. Every API call fetches live results — not cached or stale data. Rankings, descriptions, and links reflect what DuckDuckGo shows right now.

### How does pagination work?

Use `limit` and `start` parameters. `limit` controls how many results per request (max 50). `start` controls the offset.

First page: `?query=mango&limit=10` (returns results 0–9).
Second page: `?query=mango&limit=10&start=10` (returns results 10–19).

The response includes `next` and `previous` URLs so you don't have to build pagination links yourself.

### Can I use search operators?

Yes. DuckDuckGo supports operators like `site:github.com`, `inurl:api`, and `intitle:scraper`. Pass them directly in the `query` parameter, just like you would in the DuckDuckGo search bar.

### Why DuckDuckGo instead of Google?

DuckDuckGo doesn't personalize results by user history, location biases, or tracking profiles. You get consistent, unbiased search results every time.

## Rate Limits

| Plan | Price | Requests/Month |
|------|-------|----------------|
| Free | $0 | 5,000 |
| Starter | $25 | 100,000 |
| Grow | $75 | 1,000,000 |
| Scale | $150 | 10,000,000 |

## Questions? We have answers.

Reach out anytime. We will solve your query within 1 working day.

[![Contact Us on WhatsApp about DuckDuckGo Scraper](https://raw.githubusercontent.com/omkarcloud/assets/master/images/whatsapp-us.png)](https://api.whatsapp.com/send?phone=918178804274&text=I%20have%20a%20question%20about%20the%20DuckDuckGo%20Scraper%20API.)

[![Contact Us on Email about DuckDuckGo Scraper](https://raw.githubusercontent.com/omkarcloud/assets/master/images/ask-on-email.png)](mailto:happy.to.help@omkar.cloud?subject=DuckDuckGo%20Scraper%20API%20Question)
