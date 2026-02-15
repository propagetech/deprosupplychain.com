You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "case-studies.html",
    "context": {
      "title": "De Pro Supply Chain | People. Partnership. Performance.",
      "first_heading": "Case Studies"
    }
  },
  {
    "path": "css/077041ef07e496138ee006c0725b8d91.css",
    "context": {
      "path": "css/077041ef07e496138ee006c0725b8d91.css"
    }
  },
  {
    "path": "css/4957171073492227171d872757d04770.css",
    "context": {
      "path": "css/4957171073492227171d872757d04770.css"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/a4addf94f057eaf60311c3ce997b8c99.css",
    "context": {
      "path": "css/a4addf94f057eaf60311c3ce997b8c99.css"
    }
  },
  {
    "path": "css/d09d646f062b67daeff66ff1410b63fc.css",
    "context": {
      "path": "css/d09d646f062b67daeff66ff1410b63fc.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "imgs/0f94c7e2be61ce7685f125d0468a1947.webp",
    "context": {
      "refs": [
        {
          "alt": "Warehouse Design and Re Design Design New Processes or Study and Map Existing Processes, Warehouse L",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/10ae869490a52e813d531699b00ae9b9.webp",
    "context": {
      "refs": [
        {
          "alt": "Warehouse Design for White Goods Manufacturer",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3cde7e61a0a451ff58e544c5b069b615.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/593600a25ed8063ad7663cb8b89d282b.webp",
    "context": {
      "refs": [
        {
          "alt": "RFQ Design & Selection of LSP RFQ Design and Selection of Logistics Service Provider along with Benc",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5d79725c62d44a1af5afc990dfca3b29.webp",
    "context": {
      "refs": [
        {
          "alt": "In-plant Warehouse Redesign and Capacity Planning for Automotive Ancillary",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/770b84311a5196ae9031105080280f23.webp",
    "context": {
      "refs": [
        {
          "alt": "Warehouse Design and Implementation Support for Multi User Facility for a German 3PL company",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/808179867447051a4c08f9d257046ec9.webp",
    "context": {
      "refs": [
        {
          "alt": "Warehouse Design for Apparel & Fashion - Suiting Manufacturing",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9a314e4e12119baa44d547c16e280e7b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9e04f2dfc0e016eec5e9a455e7cceef7.webp",
    "context": {
      "refs": [
        {
          "alt": "Project Procurement Assist our customers in procurement of infrastructure and assets required for th",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b647c6b1c0c9cf011019c3251be7635e.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/b9d06dbbcaad942a359756c28777578b.webp",
    "context": {
      "refs": [
        {
          "alt": "RFQ / RFP Bidding Bidding of RFQ / RFP start from Site Visits / Scoping, Data Collection, Analysis, ",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bdd382e5c7b20d97416eab93632d08b4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cf14a55fce6d1abbaa6e444911f6b8f1.webp",
    "context": {
      "refs": [
        {
          "alt": "RFQ Preparation, Circulation and Finalization of 3PL's Pan India for a 10 Minute Delivery Start Up",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d2cd6b3cb069357ff50187a4c1f7113d.webp",
    "context": {
      "refs": [
        {
          "alt": "Raw Material, Finished Goods, Tools, Spares and Maintenance In-plant Warehouses Design for an Automo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e48bcac5fca1843ab25cbc2be16d8ad6.webp",
    "context": {
      "refs": [
        {
          "alt": "Solution Design and Project Implementation Design Solutions and Setting up Warehouses along with Com",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "De Pro Supply Chain | People. Partnership. Performance.",
      "first_heading": "Logistics and Supply Chain"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "js/faf9ce4e848522206b5c3043551fb2d7.js",
    "context": {
      "path": "js/faf9ce4e848522206b5c3043551fb2d7.js"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.