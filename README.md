# SemantleCompass
## [Semantle](https://semantle.com/) + [Worldle](https://worldle.teuteuf.fr/)

In [Semantle](https://semantle.com/), a user guesses the target word based off the embedding and what's near that word in the embedding space, but maybe there can be better guidance for guesses 🤔.

By word embedding arithmetic, given a `guess` for the `target` a `hint`, it should follow that:
```
guess + hint = target
```
So, similar to [Worldle](https://worldle.teuteuf.fr/) providing a compass for users, I explore if providing the cardinal words closest to the embedding vector creating by subtracting the guess from the target can provide a good hint because (in theory):
```
guess + hint = target
target - guess = hint
```

## Code
Run the `semantle_compass_app.ipynb` locally or on google colab after installing the requirements via pip with:
```
pip install -r requirements.txt
```
I use [gensim word2vec](https://radimrehurek.com/gensim/models/word2vec.html) for embeddings and [Annoy](https://github.com/spotify/annoy) for approximate nearest neighbors. 
