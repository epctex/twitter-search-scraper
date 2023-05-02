# Actor - Twitter Search Scraper

Since Twitter doesn't provide a good and free API, this actor should help you to retrieve data from it.

## Features

-   Scrape user detail - Scrape any user related information from any search result such as friends, followers, following, verified account, location, profile image, profile banner, profile URL, date of creation and so on.

-   Scrape tweet - You can retrieve all the tweets from any keyword with all the details. Language, sensitive language, reply, quote, retweet, pinned, retweeted and all sorts of Tweet related information.

- Scrape statistics - Gather all the statistical information of a tweet.

## Why using this actor?

This actor is extremely fast and optimized. It'll scrape tweets around 31 times faster than the other equivalent scrapers. Therefore you will consume less resources and it will be cheaper to use it.

## Bugs, fixes, updates and changelog

This scraper is under active development. If you have any feature requests you can create an issue from [here](https://github.com/epctex/twitter-search-scraper/issues).

## Input Parameters

The input of this scraper should be JSON containing the list of pages on Twitter Search Scraper that should be visited. Possible fields are:

- `keywords`: (Required) (Array) List of keywords you want to scrape from Twitter.

- `maxItems`: (Optional) (Number) You can limit scraped items. This should be useful when you search through the big lists or search results.

- `proxy`: (Required) (Proxy Object) Proxy configuration.

This solution requires the use of **Proxy servers**, either your own proxy servers or you can use [Apify Proxy](https://www.apify.com/docs/proxy).

### Tip

When you want to have a scrape over a specific keyword or hashtag, just copy and paste the keyword as one of the **keyword**.

### Compute Unit Consumption

The actor optimized to run blazing fast and scrape many as tweets as possible. Therefore, it forefronts all tweet detail requests. If actor doesn't block very often it'll scrape 100 tweets in 20 seconds with ~0.02-0.025 compute units.

### Twitter Search Scraper Input example

```json
{
  "proxy":{
    "useApifyProxy":true
  },
  "maxItems": 10,
  "keywords":[
    "#binance",
    "ukraine"
  ]
}

```

## During the Run

During the run, the actor will output messages letting you know what is going on. Each message always contains a short label specifying which page from the provided list is currently specified.
When items are loaded from the page, you should see a message about this event with a loaded item count and total item count for each page.

If you provide incorrect input to the actor, it will immediately stop with failure state and output an explanation of what is wrong.

## Twitter Search Scraper Export

During the run, the actor stores results into a dataset. Each item is a separate item in the dataset.

You can manage the results in any languague (Python, PHP, Node JS/NPM). See the FAQ or <a href="https://www.apify.com/docs/api" target="blank">our API reference</a> to learn more about getting results from this Twitter Search actor.

## Scraped Tweets Properties

The structure of each tweet in Twitter Search Scraper looks like this:

### Tweet Detail

```json
{
	"created_at": "Sat Nov 19 12:05:12 +0000 2022",
	"id": 1593938439887618000,
	"id_str": "1593938439887618054",
	"full_text": "Daha önce #MeralAkşener iyine çağırdı yok dedi, #AhmetKaya 'nın mezarını Türkiye'ye getirebiliriz dedi eşi Gülten Kaya yok dedi.Her seçim zamanı aynı repertuarı kullanmasan mı ? #izmirdeprem",
	"truncated": false,
	"display_text_range": [
		0,
		190
	],
	"entities": {
		"hashtags": [
			{
				"text": "MeralAkşener",
				"indices": [
					10,
					23
				]
			},
			{
				"text": "AhmetKaya",
				"indices": [
					48,
					58
				]
			},
			{
				"text": "izmirdeprem",
				"indices": [
					178,
					190
				]
			}
		],
		"symbols": [],
		"user_mentions": [],
		"urls": []
	},
	"source": "<a href=\"http://twitter.com/download/android\" rel=\"nofollow\">Twitter for Android</a>",
	"in_reply_to_status_id": null,
	"in_reply_to_status_id_str": null,
	"in_reply_to_user_id": null,
	"in_reply_to_user_id_str": null,
	"in_reply_to_screen_name": null,
	"user_id": 1202948684297724000,
	"user_id_str": "1202948684297723905",
	"geo": null,
	"coordinates": null,
	"place": null,
	"contributors": null,
	"is_quote_status": false,
	"retweet_count": 0,
	"favorite_count": 0,
	"reply_count": 0,
	"quote_count": 0,
	"conversation_id": 1593938439887618000,
	"conversation_id_str": "1593938439887618054",
	"favorited": false,
	"retweeted": false,
	"lang": "tr",
	"supplemental_language": null,
	"ext_edit_control": {
		"initial": {
			"edit_tweet_ids": [
				"1593938439887618054"
			],
			"editable_until_msecs": "1668861312000",
			"edits_remaining": "5",
			"is_edit_eligible": true
		}
	},
	"ext": {
		"unmentionInfo": {
			"r": {
				"ok": {}
			},
			"ttl": -1
		},
		"superFollowMetadata": {
			"r": {
				"ok": {}
			},
			"ttl": -1
		},
		"editControl": {
			"r": {
				"ok": {
					"initial": {
						"editTweetIds": [
							"1593938439887618054"
						],
						"editableUntilMsecs": "1668861312000",
						"editsRemaining": "5",
						"isEditEligible": true
					}
				}
			},
			"ttl": -1
		}
	},
	"user": {
		"id": 1202948684297724000,
		"id_str": "1202948684297723905",
		"name": "Mete Han",
		"screen_name": "Metehanatam",
		"location": "",
		"description": "Atatürk - Fenerbahçe -Hayvansever - Rakı Sever",
		"url": null,
		"entities": {
			"description": {
				"urls": []
			}
		},
		"protected": false,
		"followers_count": 40,
		"fast_followers_count": 0,
		"normal_followers_count": 40,
		"friends_count": 224,
		"listed_count": 0,
		"created_at": "Fri Dec 06 13:51:37 +0000 2019",
		"favourites_count": 241,
		"utc_offset": null,
		"time_zone": null,
		"geo_enabled": true,
		"verified": false,
		"statuses_count": 799,
		"media_count": 251,
		"lang": null,
		"contributors_enabled": false,
		"is_translator": false,
		"is_translation_enabled": false,
		"profile_background_color": "F5F8FA",
		"profile_background_image_url": null,
		"profile_background_image_url_https": null,
		"profile_background_tile": false,
		"profile_image_url": "http://pbs.twimg.com/profile_images/1503755569475297285/uZLS4w8m_normal.jpg",
		"profile_image_url_https": "https://pbs.twimg.com/profile_images/1503755569475297285/uZLS4w8m_normal.jpg",
		"profile_banner_url": "https://pbs.twimg.com/profile_banners/1202948684297723905/1651961644",
		"profile_image_extensions_sensitive_media_warning": null,
		"profile_image_extensions_media_availability": null,
		"profile_image_extensions_alt_text": null,
		"profile_image_extensions_media_color": {
			"palette": [
				{
					"rgb": {
						"red": 45,
						"green": 29,
						"blue": 26
					},
					"percentage": 37.92
				},
				{
					"rgb": {
						"red": 196,
						"green": 167,
						"blue": 146
					},
					"percentage": 25.34
				},
				{
					"rgb": {
						"red": 191,
						"green": 131,
						"blue": 83
					},
					"percentage": 6.52
				},
				{
					"rgb": {
						"red": 110,
						"green": 44,
						"blue": 43
					},
					"percentage": 4.74
				},
				{
					"rgb": {
						"red": 192,
						"green": 52,
						"blue": 60
					},
					"percentage": 4.72
				}
			]
		},
		"profile_image_extensions": {
			"mediaStats": {
				"r": {
					"missing": null
				},
				"ttl": -1
			}
		},
		"profile_banner_extensions_sensitive_media_warning": null,
		"profile_banner_extensions_media_availability": null,
		"profile_banner_extensions_alt_text": null,
		"profile_banner_extensions_media_color": {
			"palette": [
				{
					"rgb": {
						"red": 41,
						"green": 50,
						"blue": 63
					},
					"percentage": 69.82
				},
				{
					"rgb": {
						"red": 98,
						"green": 110,
						"blue": 133
					},
					"percentage": 13.17
				},
				{
					"rgb": {
						"red": 107,
						"green": 83,
						"blue": 75
					},
					"percentage": 8.99
				},
				{
					"rgb": {
						"red": 143,
						"green": 149,
						"blue": 140
					},
					"percentage": 2.25
				},
				{
					"rgb": {
						"red": 176,
						"green": 115,
						"blue": 67
					},
					"percentage": 1.49
				}
			]
		},
		"profile_banner_extensions": {
			"mediaStats": {
				"r": {
					"missing": null
				},
				"ttl": -1
			}
		},
		"profile_link_color": "1DA1F2",
		"profile_sidebar_border_color": "C0DEED",
		"profile_sidebar_fill_color": "DDEEF6",
		"profile_text_color": "333333",
		"profile_use_background_image": true,
		"has_extended_profile": false,
		"default_profile": true,
		"default_profile_image": false,
		"pinned_tweet_ids": [
			1506948451191472000
		],
		"pinned_tweet_ids_str": [
			"1506948451191472128"
		],
		"has_custom_timelines": false,
		"can_dm": null,
		"following": null,
		"follow_request_sent": null,
		"notifications": null,
		"muting": null,
		"blocking": null,
		"blocked_by": null,
		"want_retweets": null,
		"advertiser_account_type": "none",
		"advertiser_account_service_levels": [],
		"profile_interstitial_type": "",
		"business_profile_state": "none",
		"translator_type": "none",
		"withheld_in_countries": [],
		"followed_by": null,
		"ext_is_blue_verified": false,
		"ext_has_nft_avatar": false,
		"ext": {
			"highlightedLabel": {
				"r": {
					"ok": {}
				},
				"ttl": -1
			},
			"hasNftAvatar": {
				"r": {
					"ok": false
				},
				"ttl": -1
			},
			"superFollowMetadata": {
				"r": {
					"ok": {
						"superFollowEligible": false,
						"superFollowing": false,
						"superFollowedBy": false,
						"exclusiveTweetFollowing": false,
						"privateSuperFollowing": false
					}
				},
				"ttl": -1
			}
		},
		"require_some_consent": false
	}
}
```
