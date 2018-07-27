# Emotion aware conversational interface - Text to Color
<img src="https://github.com/minh364/jejuDLcamp_emotion/blob/master/docs/image/1.png" width="500" />
<p>
I want to make the chatting messenger which recognize user's emotion and displays it in colors.<br/>
This is the code about a demo web page that briefly covered this concept. <br/>
</p>

<img src="https://github.com/minh364/jejuDLcamp_emotion/blob/master/docs/image/2.png" width="600" />


## Dependencies


## Code Overview
- <b>deepmoji/</b>
  code for training model Deepmoji and use it @DeepMoji team
- <b>docs/image/</b>
  images
- <b>models/</b>
  pretrained model and vocaburary
- <b>static/</b>
  css, js files
- <b>templates/</b>
  html files
- <b>app.py</b>
  flask @/ file for run the web page

## Text to Emoji
<img src="https://github.com/minh364/jejuDLcamp_emotion/blob/master/docs/image/3.png" width="500" />

<p>
I use the DeepMoji model from MIT media lab as emotion classifier.<br/>
It is trained by 1246 million tweets, which is containing one of 64 different common emoticon.<br/>
There are embedding layer to project each word into a vector space. <br/>
( a hyper tangent activation enforce a constraint of each embedding dimension being within -1~1. )<br/>
two bidirectional LSTM layers to capture the context of each word.<br/>
And an attention layer that lets the model decide the importance of each word for the prediction.<br/>
</p>

## Emoji to Color
<img src="https://github.com/minh364/jejuDLcamp_emotion/blob/master/docs/image/4.png" width="600" />
<p>
I mapping color based on dendrogram.<br/> 
The dendrogram shows how the model learns to group emojis based on emotional content.<br/> 
The y-axis is the distance on the correlation matrix of the model’s predictions.<br/>
 t measured using average linkage.
</p>
<img src="https://github.com/minh364/jejuDLcamp_emotion/blob/master/docs/image/5.png" width="500" />
<img src="https://github.com/minh364/jejuDLcamp_emotion/blob/master/docs/image/6.png" width="500" />
<p>
The color code I use is rgba. (a = defines the opacity.)<br/>
The output from the model is the probability of each 64 different emojis.<br/>
I use top 3 probability with normalization for define the opacity of layer.<br/>
And this 3 layers are overlaped, and than determind the color of screen.<br/>
In this way I represent the emotion by color.<br/>
</p>
