# Algorithm Bot

## Purpose, Triger Words and Demos
A chatbot uses LIFF to show some explanations and demonstrations about algorithms based on my blog.<br>
Aiming to help people to learn algorithms by providing my point of view.

- sorting

<img alt="sorting-demo" src="https://user-images.githubusercontent.com/68285613/111157124-773bd100-85d1-11eb-9771-cec592c8a849.png" width="300" height="300" />

- tree

<img alt="tree-demo" src="https://user-images.githubusercontent.com/68285613/111157149-83279300-85d1-11eb-94c4-0d958d18f432.png" width="300" height="300" />

- hash

<img alt="hash-demo" src="https://user-images.githubusercontent.com/68285613/111157138-7efb7580-85d1-11eb-9911-3154b3d90893.png" width="300" height="300" />


<br>

## Platform & QR Code
front-end : LINE API, LINE Login(LIFF), Rich Menu, Flex Message<br>
back-end : Heroku<br>
All the information about data structures come from [here](https://github.com/iitsmel/iitsmel.io).<br>
<img src="https://user-images.githubusercontent.com/68285613/107939960-7871e200-6fc2-11eb-9c06-f4d6fbb913c1.png" width="300" height="300" />

<br>

## Problems I've encountered & currently solved
- unable to successfully verify Webhook URL<br>
enter following commands works for me<br>
> git add .<br>
> git commit -am "your previous input"<br>
<br>
"your previous input" is what you entered the very first time.<br>
<br>

> git push heroku main<br>
> heroku logs --tail<br>
<br>
"heroku logs --tail" will show all logs in terminal.<br>
<br>
This step is not necessery but very handy and convinent when you don't want to switch
to Heroku Application log page.<br>
<br><br>

- a little bit confused about flex message<br>
Here's my conclution about flex message:
<br>

    line_bot_api.reply_message(
        event.reply_token,
        FlexSendMessage(alt_text= 'hi', 
                contents = { 'type': 'bubble', 'direction': 'ltr',
                    'hero': {
                        'type': 'image',
                        'url': 'https://example.com/cafe.jpg',
                        'size': 'full',
                        'aspectRatio': '20:13',
                        'aspectMode': 'cover',
                        'action': { 'type': 'uri', 'uri': 'http://example.com', 'label': 'label' }
                    }
                }
        )
    )

<br>
Make sure to put "from linebot.models import FlexSendMessage" in code.<br>
"line_bot_api.reply_message" will give you the leverage to be able to send a message through bot.<br>
" event.reply_token" means that the bot will reply to this specific token.<br>
Finally, here's the flex message part.<br>
"alt_text" is a must because whatever you type in or put behind will represent the user's reply(to the bot).<br>
By recognizing this reply, the bot will send a flex message.<br>
In other words, "alt_text" is sort of a trigger word.<br>
"contents" is what your flex message should look like.<br>
So there you go, can't make a flex message out of empty alt_text and contents.<br>
<br><br>

- json problem<br>

[This website](https://developers.line.biz/flex-simulator) helped me a lot. Remember, json has a specific form, there are some content can't be deleted.
<br>

## Language
Python
<br>

## Colors Section
thoughts : Panton COLOR OF THE YEAR 2021, FRIENDS<br>

<img src="https://user-images.githubusercontent.com/68285613/107940097-aa834400-6fc2-11eb-825f-fe6f543f70de.png" width="300" height="300" />

- PANTONE 17-5104 Ultimate Gray #939597
- PANTONE 13-0647 Illuminating #F5DF4D

<br>

<img src="https://user-images.githubusercontent.com/68285613/107939900-61cb8b00-6fc2-11eb-897c-2d4f633fa487.png" width="300" height="300" />

- background : #FFF580
- shade : #00009E
- word : #42A2D6

<br>

<img src="https://user-images.githubusercontent.com/68285613/107939833-43658f80-6fc2-11eb-8204-ef79d7e4ddc2.png" width="300" height="300" />

- background : #9C8CD4
- shade : #665236
- word : #D2C385

<br>

<img src="https://user-images.githubusercontent.com/68285613/107938911-fc2acf00-6fc0-11eb-9a78-17b3d760ff69.png" width="300" height="300" />

- background : #FFDC00
- shade : #9A0006
- word : #FF4238
