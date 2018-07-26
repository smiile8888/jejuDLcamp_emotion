<stlye>
    .center-image{
        margin: 0 auto;
        display: block;
    }
</stlye>

# Emotion aware conversational interface - Text to Color
It is for an interface design for massenser that recognizes the user's emotion and displays it in colors and emoji.

<img src="https://github.com/minh364/jejuDLcamp_emotion/blob/master/docs/image/1.png" width:"200px";/>

![proposed method][2]

## Code Overview
- deepmoji/
-- code for training model Deepmoji and use it @DeepMoji team
- docs/image/
-- images
- models/
-- pretrained model and vocaburary
- static/
-- css, js files
- templates/
-- html files
- app.py
-- flask @/ file for run the web page

## Emoji to Color
![##model][3]
![color mapping to emoji dendrogram][4]
![color code: rgba][5]
![color code: rgba][6]



[1]: https://github.com/minh364/jejuDLcamp_emotion/blob/master/docs/image/1.png
[2]: https://github.com/minh364/jejuDLcamp_emotion/blob/master/docs/image/2.png
[3]: https://github.com/minh364/jejuDLcamp_emotion/blob/master/docs/image/3.png
[4]: https://github.com/minh364/jejuDLcamp_emotion/blob/master/docs/image/4.png
[5]: https://github.com/minh364/jejuDLcamp_emotion/blob/master/docs/image/5.png
[6]: https://github.com/minh364/jejuDLcamp_emotion/blob/master/docs/image/6.png
