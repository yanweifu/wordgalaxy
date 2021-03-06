# WordGalaxy: An Interactive Map of English

This project visualizes a large number (eg., 20,000) of words in two dimensions in such a way that words that are similar in meaning appear closer to one another, and words that are dissimilar are farther away from each other.

It yields an interactive, statically served site where users can explore the space by zooming & panning.

This project cherry picks the latest and greatest technologies in natural language
processing and web development. To generate the vectors, I rely on [Google's Word2Vec tool](https://code.google.com/p/word2vec/). Specifically, I used some preprocessed vectors run on 200-300 millions words of Wikipedia, code that was written by dhammock a few years ago, see [here](https://github.com/dhammack/Word2VecExample). The vectors are represented in 250 dimensions, so to visualize them they need to be 
collapsed into 2 or 3 dimensions. For this, I use [this](https://github.com/danielfrg/tsne)
implementation of Barnes-Hut t-SNE.

For the presentation, I rely on PIXI.js, a game engine which uses WebGL when available and fails gracefully into canvas rendering. To get a headstart, I launched off [this](https://github.com/anvaka/ngraph) implementation, which is a library for plotting graphs that already had zoom & pan built in.

If you have questions, feature requests, or feedback of any kind, please don't hesitate to message me.

## References
[Barnes-Hut SNE](http://arxiv.org/pdf/1301.3342v2.pdf)

[Efficient Estimation of Word Representations in Vector Space](http://arxiv.org/pdf/1301.3781.pdf)
