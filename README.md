# Transformer
Re-implementation of [Attention is All You Need](https://arxiv.org/abs/1706.03762)

## Preprocess

- Data [Here](http://www.statmt.org/europarl/v7/fr-en.tgz)
  - English to French
- Technique
    - Ascending Sort By Sentence Length(Good Performence)
        - If using random batch, there are too many padding per batch.
    - No random Batch

## Model
<img src="https://user-images.githubusercontent.com/38184045/72739494-12f8c980-3be7-11ea-874f-b4df6feb52cc.png" width="50%" height="50%"></img>

- Transformer
  - model.py
- Encoder/Decoder layer
  - layer.py
- MultiHeadAttention, FeedFoward etc..
  - sublayer.py
- Add&Norm 
  - just use ```python torch.nn.LayerNorm ```
  
## Train

- train.py
- Techniques used in this paper
    - Label Smoothing
    - Learning Rate Scheduling
    - etc..

## Future Work

- Make Test Code(Why don't work at Shifted Right?)
- Use More Bigger Data