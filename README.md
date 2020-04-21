# CoronaNews

![CoronaNews](https://github.com/Ervin11/CoronaNews/blob/master/view.png)

Ce projet a été realisé dans le but de collecter des données en temps réel sur les stats du Covid 19 et d'informer sur son impact mondial.

Backend : Symfony
Frontend : Html5 x Bootstrap

Les graphs ont été réalisés avec ApexCharts


APIs utilisées :
- https://gist.github.com/gwillem/6ca8a81048e6f3721c3bafc803d44a72 pour obtenir la population total d'un pays en fonction de son code ISO
```json
{
  "countryName": "Population",
  "AD": "84000",
}
```
- https://api.covid19api.com/summary pour obtenir les stats global de tous les pays afin de construire le tableau des stats par pays
```json
{
  "Country":"Afghanistan",
  "CountryCode":"AF",
  "Slug":"afghanistan",
  "NewConfirmed":30,
  "TotalConfirmed":1026,
  "NewDeaths":3,
  "TotalDeaths":36,
  "NewRecovered":4,
  "TotalRecovered":135,
  "Date":"2020-04-21T09:45:44Z"
}
```
- https://pomber.github.io/covid19/timeseries.json pour obtenir les stats journalières d'un pays afin de contruire les graphs
```json
{
  "Afghanistan": [
    {
      "date": "2020-1-22",
      "confirmed": 0,
      "deaths": 0,
      "recovered": 0
    },
    {
      "date": "2020-1-23",
      "confirmed": 0,
      "deaths": 0,
      "recovered": 0
    },
]
}
```
- http://newsapi.org pour obtenir les dernières news sur le covid-19
 ```json
 {
  "status":"ok",
  "totalResults":1,
  "articles":
    [{"source":
      {"id":null,"name":"Theinventory.com"},
      "author":"Ignacia, Gabe Carey, Elizabeth Henges, Jordan McMahon, and Quentyn Kennemer on Kinja Deals, shared by Ignacia to Lifehacker",
      "title":"Monday's Best Deals: Private Internet Access, Apple Airpods, Sony Headphones, Amazon Fire TV Recast, Cuisinart Griddle, and More","description":"A Private Internet Access deal, an Amazon TV Recast, Apple Airpods, a pair of Sony WH-1000XM3 headphones, a Cuisinart Griddle, and an Elgato Stream Deck lead Monday’s best deals.Read more...",
      "url":"https://kinjadeals.theinventory.com/mondays-best-deals-private-internet-access-apple-airp-1842960915",
      "urlToImage":"https://i.kinja-img.com/gawker-media/image/upload/c_fill,f_auto,fl_progressive,g_center,h_675,pg_1,q_80,w_1200/z2x6r2r8ibsdfoq195jk.jpg",
      "publishedAt":"2020-04-20T14:45:00Z",
      "content":"A Private Internet Access deal, an Amazon TV Recast, Apple Airpods, a pair of Sony WH-1000XM3 headphones, a Cuisinart Griddle, and an Elgato Stream Deck lead Mondays best deals.\r\nBookmark Kinja Deals and follow us on Twitter to never miss a deal.\r\nThe best VP… [+28286 chars]"
    }]
  }
 ```

## Installation

```bash
composer install
```

## Usage

```bash
symfony server:start
```
