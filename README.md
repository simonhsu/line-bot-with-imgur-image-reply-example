A Line Bot will reply image from selected Imgur album while some messages hit by predefined `keyword`
============

This bot will work on google cloud functions ( treat google cloud functions as line webhook service )

Article : http://bit.ly/linebot_w_imgur

## Prepare

**[Imgur](http://imgur.com/)**
- Create imgur account & application, and get imgur app token
- Create album and upload some images, and get album id

**[LINE](https://business.line.me/zh-hant/)**
- Create a Line Bot Account, and get Line Channnel Access Token

**[Google Cloud Functions](https://cloud.google.com/functions/)**
- Create a google cloud function, and set the triggered function name as `reply`
- Copy The content of these two files ( index.js, package.json ) to the cloud functions you created. ( use online editor )

## Replace ( in index.js )

- replace `_KEYWORD1_` with the keyword you hope line bot to listen. ( eg. morning )
- replace `_IMGUR_ALBUM_ID_FOR_KEYWORD1_` with the album id in imgur ( eg. f5sXe )
- replace `_IMGUR_APP_TOKEN_` with your imgur application token
- replace `_LINE_CHANNEL_ACCESS_TOKEN_` with line channel access token

## Deploy ( in google cloud functions )
- After saving the cloud function, you will get the deployed url.
- Copy the deployed url to your webhook url in Line Account
- Done. Enjoy it !


## License

This project is licensed under the terms of the
[MIT license](https://github.com/callemall/material-ui/blob/master/LICENSE)
