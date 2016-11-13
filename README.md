# Practical-Private-Logs

Now is a good time to sanitize logs of behavioural data.
This is a collection of pointers to software and guidance on how to do that.

If you have a bunch of logs of behavioural data that is not anonimized, and you would like to preserve something in their place which:

1. does not reveal private information about your users
2. is useful in learning about them

Doing just (1) is trivial: just delete the logs, doing just (2) alone is also trivial, keep everything.
What can be done to do both? Derivative syntehtic dataset that is differentially private and preserves up to some order the joint marginal probability distribution over the data. We can then delete the original and keep the synthetic dataset to learn from in the future.

>Differential privacy guarantees that nothing that could not happen without access to your data will happen with access to your data.
>In fact it makes a stronger quantitative guarantee: The chance that any specific thing happens (really, anything at all) with access to your data is at most a multiple X of the chance it would happen without your data. That "multiple" X is part of the guarantee and it determines how much privacy you get: a value of 1.0 would be perfect privacy (which by definition ignores your data), small values like 1.01 are pretty great, whereas values like 10.0 are less amazing but still non-trivial.
-- [Differential privacy: An illustrated primer](https://github.com/frankmcsherry/blog/blob/master/posts/2016-02-06.md)

# Methods (and implementations)

- RAPPOR: Privacy-Preserving Reporting Algorithms https://github.com/google/rappor https://arxiv.org/abs/1407.6981
 * Has the client send the data transformed so that the server never needs to see the non-anonimized version
 * originates in google, also a production quality implementation is part of chromium http://www.chromium.org/developers/design-documents/rappor
 * a blog post covering the release https://security.googleblog.com/2014/10/learning-statistics-with-privacy-aided.html


- [Exponential Mechanism with the Multiplicative Weights](https://github.com/mrtzh/PrivateMultiplicativeWeights.jl)  [paper](http://users.cms.caltech.edu/~katrina/papers/mwem-nips.pdf)
  * A simple and fairly practical scheme for the batch one off setting

- DPSynthesizer source? ,  https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4496798/

# How To

- Differential Privacy: An Economic Method for Choosing Epsilon https://arxiv.org/abs/1402.3329

- How Can We Analyze Differentially-Private Synthetic Datasets? http://repository.cmu.edu/cgi/viewcontent.cgi?article=1059&context=jpc

# Guides and experiences
- [Towards practicing differential privacy](http://blog.mrtz.org/2015/03/13/practicing-differential-privacy.html)



[Differential Privacy – A Primer for the Perplexed ](https://www.unece.org/fileadmin/DAM/stats/documents/ece/ces/ge.46/2011/26_Dwork-Smith.pdf)




