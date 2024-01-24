![DuckDuckGo Scraper Featured Image](https://raw.githubusercontent.com/omkarcloud/duckduckgo-scraper/master/images/duckduckgo-scraper-featured-image.png)

<div align="center" style="margin-top: 0;">
  <h1>✨ DuckDuckGo Scraper 🚀</h1>
  <p>💦 DuckDuckGo Scraper helps you collect search results from DuckDuckGo. 💦</p>
</div>
<em>
  <h5 align="center">(Programming Language - Python 3)</h5>
</em>
<p align="center">
  <a href="#">
    <img alt="duckduckgo-scraper forks" src="https://img.shields.io/github/forks/omkarcloud/duckduckgo-scraper?style=for-the-badge" />
  </a>
  <a href="#">
    <img alt="Repo stars" src="https://img.shields.io/github/stars/omkarcloud/duckduckgo-scraper?style=for-the-badge&color=yellow" />
  </a>
  <a href="#">
    <img alt="duckduckgo-scraper License" src="https://img.shields.io/github/license/omkarcloud/duckduckgo-scraper?color=orange&style=for-the-badge" />
  </a>
  <a href="https://github.com/omkarcloud/duckduckgo-scraper/issues">
    <img alt="issues" src="https://img.shields.io/github/issues/omkarcloud/duckduckgo-scraper?color=purple&style=for-the-badge" />
  </a>
</p>
<p align="center">
  <img src="https://views.whatilearened.today/views/github/omkarcloud/duckduckgo-scraper.svg" width="80px" height="28px" alt="View" />
</p>

<p align="center">
  <a href="https://gitpod.io/#https://github.com/omkarcloud/duckduckgo-scraper">
    <img alt="Open in Gitpod" src="https://gitpod.io/button/open-in-gitpod.svg" />
  </a>
</p>
  
---

## Disclaimer for DuckDuckGo Scraper Project

> By using DuckDuckGo Scraper, you agree to comply with all applicable local and international laws related to data scraping, copyright, and privacy. The developers of DuckDuckGo Scraper will not be held liable for any misuse of this software. It is the user's sole responsibility to ensure adherence to all relevant laws regarding data scraping, copyright, and privacy, and to use DuckDuckGo Scraper in an ethical and legal manner, in line with both local and international regulations.

We take concerns related to the DuckDuckGo Scraper Project very seriously. If you have any inquiries or issues, please contact Chetan Jain at [chetan@omkar.cloud](mailto:chetan@omkar.cloud). We will take prompt and necessary action in response to your emails.

## 👉 Explore Our Other Awesome Products

- ✅ [Botasaurus](https://github.com/omkarcloud/botasaurus): The All-in-One Web Scraping Framework with Anti-Detection, Parallelization, Asynchronous, and Caching Superpowers.

---

DuckDuckGo Scraper helps you collect search results from DuckDuckGo.

## 🚀 Getting Started

1️⃣ **Clone the Magic 🧙‍♀:**
```shell
git clone https://github.com/omkarcloud/duckduckgo-scraper
cd duckduckgo-scraper
```
2️⃣ **Install Dependencies 📦:**
```shell
python -m pip install -r requirements.txt
```
3️⃣ **Let the Scraping Begin 😎**:
```shell
python main.py
```

Find your data in the `output` directory.

![DuckDuckGo Scraper CSV Result](https://raw.githubusercontent.com/omkarcloud/duckduckgo-scraper/master/images/duckduckgo-scraper-csv-result.png)

*Note: If you don't have Python installed. Follow this Simple FAQ [here](https://github.com/omkarcloud/duckduckgo-scraper/blob/master/advanced.md#-i-dont-have-python-installed-how-can-i-run-the-scraper) and you will have your DuckDuckGo data in next 5 Minutes*

## 🤔 FAQs

### ❓ How to Scrape DuckDuckGo ?

1. Open the `main.py` file.
2. Update the `queries` list with the locations you are interested in. For example:

```python
queries = [
  "Mango",
  "Watermelon",
]

DuckDuckGo.search(queries, max=10)
```

3. Run it.

```bash
python main.py
```

Then find your data in the `output` directory.


### ❓ How to Scrape More DuckDuckGo Search Results Using Your DuckDuckGo API?

To scrape additional data, follow these steps to use our DuckDuckGo API. You can make 50 requests for free:

1. Sign up on RapidAPI by visiting [this link](https://rapidapi.com/auth/sign-up).

![Sign Up on RapidAPI](https://raw.githubusercontent.com/omkarcloud/assets/master/images/sign-up.png)

2. Then, subscribe to our Free Plan by visiting [this link](https://rapidapi.com/Chetan11dev/api/duckduckgo-scraper/pricing).

![Subscribe to Free Plan](https://raw.githubusercontent.com/omkarcloud/assets/master/images/free-subscription.png)

3. Now, copy the API key.

![Copy the API Key](https://raw.githubusercontent.com/omkarcloud/assets/master/images/api-key.png) 

4. Use it in the scraper as follows:
```python
DuckDuckGo.search("Orange", max=10, key="YOUR_API_KEY")
```

5. Run the script, and you'll find your data in the `output` folder.
```bash
python main.py
```   

The first 50 requests are free. After that, you can upgrade to the Pro Plan, which will get you 1000 requests for just $9.


### ❓ How did you build it?

We used Botasaurus, It's an All-in-One Web Scraping Framework with Anti-Detection, Parallelization, Asynchronous, and Caching Superpowers.

Botasaurus helped us cut down the development time by 50% and helped us focus only on the core extraction logic of the scraper.

If you are a Web Scraper, you should learn about Botasaurus [here](https://github.com/omkarcloud/botasaurus), because Botasaurus will save you countless hours in your life as a Web Scraper.

<p align="center">
  <a href="https://github.com/omkarcloud/botasaurus">
  <img src="https://raw.githubusercontent.com/omkarcloud/assets/master/images/mascot.png" alt="botasaurus" />
</a>
</p>


### ❓ Need More Help or Have Additional Questions?

For further help, contact us on WhatsApp. We'll be happy to help you out.

[![Contact Us on WhatsApp about DuckDuckGo Scraper](https://raw.githubusercontent.com/omkarcloud/assets/master/images/whatsapp-us.png)](https://api.whatsapp.com/send?phone=918295042963&text=Hi,%20I%20would%20like%20to%20learn%20more%20about%20your%20products.)

## Love It? [Star It! ⭐](https://github.com/omkarcloud/duckduckgo-scraper/stargazers)

## Made with ❤️ using [Botasaurus Web Scraping Framework](https://github.com/omkarcloud/botasaurus)