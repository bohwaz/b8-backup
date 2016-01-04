# b8 - bayesian spam filter in PHP

This is a mirror of the source code of b8 bayesian spam filter, from http://nasauber.de/opensource/b8/ (down at the moment).

The only difference with the mainline release is that this version supports SQLite as a storage backend as well.

## What is b8?

b8 is a statistical ("Bayesian" [1]) spam filter implemented in PHP 5. It is intended to keep your weblog or guestbook spam-free. The filter can be used anywhere in your PHP code and tells you whether a text is spam or not, using statistical text analysis. What it does is: you give b8 a text and it returns a value between 0 and 1, saying it's ham when it's near 0 and saying it's spam when it's near 1. See How does it work? for details about this.

Principally, It's a program like Bogofilter or SpamBayes, but it is not intended to classify emails. Therefore, the way b8 works is slightly different from email spam filters. See What's different? if you're interested in the details.

To be able to distinguish spam and ham (non-spam), b8 first has to learn some spam and some ham texts. If it makes mistakes when classifying unknown texts or the result is not distinct enough, b8 can be told what the text actually is, getting better with each learned text.

The whole documentation can be found in the readme.

Big thanks go to Gary Robinson, as his articles A Statistical Approach to the Spam Problem and Spam Detection describe the foundation for the math and algorithms used in b8.

[1] I'm not a mathematician, but as far as I can grasp it, the math used in b8 has not much to do with Bayes' theorem itself. So I call it a statistical spam filter, not a Bayesian spam filter. 
