# Practical-Private-Logs

Now is a good time to sanitize logs of behavioural data.
This is a collection of pointers to software and guidance on how to do that.

For the batch setting, i.e you have a bunch of historical files you would like to delete, and you would like to preserve something in their place which 

1. does not leak much information 
2. is useful 

Doing just (1) is trivial: delete the logs, doing just (2) alone is also trivial, keep everything.

What can be done in between?



# Methods (and implementations)

1. RAPPOR: Privacy-Preserving Reporting Algorithms https://github.com/google/rappor https://arxiv.org/abs/1407.6981
* originates in google, also a production quality implementation is part of chromium http://www.chromium.org/developers/design-documents/rappor
* a blog post covering the release https://security.googleblog.com/2014/10/learning-statistics-with-privacy-aided.html
  
2. Exponential Mechanism with the Multiplicative Weights https://github.com/mrtzh/PrivateMultiplicativeWeights.jl  http://users.cms.caltech.edu/~katrina/papers/mwem-nips.pdf 

3. DPSynthesizer source? ,  https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4496798/

# How To

1. Differential Privacy: An Economic Method for Choosing Epsilon https://arxiv.org/abs/1402.3329

2. How Can We Analyze Differentially-Private Synthetic Datasets? http://repository.cmu.edu/cgi/viewcontent.cgi?article=1059&context=jpc

# Guides and experiences
https://www.unece.org/fileadmin/DAM/stats/documents/ece/ces/ge.46/2011/26_Dwork-Smith.pdf
http://blog.mrtz.org/2015/03/13/practicing-differential-privacy.html



