
## Rights, restrictions, and licensing: Concepts

*aka*

###  Deconstructing IP

Humanitarian Free and Open Source Software Development (HFOSS) Spring 2018

**Your instructor is not a lawyer, and nothing said in class or included in course material is intended as legal or financial advice.**

Rather, this discussion of concepts is meant to aid in understanding some of
the constraints on sharing software and motivations behind the establishment
of various mechanisms and norms in support of software freedom and collaboration.

### 5 Concepts

  * Trade Secret
  * Public domain
  * Copyright
  * Patent
  * Trademark

These are often referred to as **intellectual property** which invokes a
comparison with physical things, such as **real property** or **personal property**,
possession of which is said to be **rivalrous**, eg, one person possessing
it can exclude another person from using it.

However, each of the set of restrictions (the four not including **public domain**) 
operates very differently from the others in terms of:

  * what it covers
  * how it comes into force
  * how it is maintained over time
  * how long it lasts

and, of course, all the things covered by these concepts are non-physical, and thus, non-rivalrous. Thomas Jefferson [famously compared](http://press-pubs.uchicago.edu/founders/documents/a1_8_8s12.html) it to lighting one candle with another.

The Free Software Foundation considers these differences so stark, and their
inclusion together under a single term so misleading, as to
[recommend never using the term "intellectual property".](https://www.gnu.org/philosophy/words-to-avoid.html#IntellectualProperty)

**The essential question is, why all the fuss about licensing?**

When things are not [born free](https://en.wikipedia.org/wiki/Born_Free), how can we share them with each other and work together on them and with them?

#### Trade Secrets

  * Covers whatever one can keep secret
  * Last for however long you can keep it secret
  * Often assisted by contracts in the form of non-disclosure agreements (NDA)
    * If NDA's have an expiry date, this **can** put a limit on how long something can be kept secret
  * obviously works very differently than copyright on published works
  * absent copyright or patent restrictions ([cf *state of nature*](https://en.wikipedia.org/w/index.php?title=State_of_nature&oldid=882399986)), this would be the default way of restricting use

#### Public domain

  * describes the set of creative works and inventions the use of which is not restricted
  * how sharing might happen in a **state of nature**
  * expiry of patents and of copyrights allows those works into the public domain
  * in US, federal government can't take copyright, so fed works goes straight to public domain
    * but not for contracted work, cf Bayh-Dole Act, 1980
  * documenting prior authorship could help against copyright restriction
  * documenting **prior art** could help against patent restriction

#### Copyright

  * applies to **creative** expressions (eg, not facts)
  * comes into effect **automatically** (as per the [Berne Convention](https://en.wikipedia.org/wiki/Berne_Convention)) when work is put into *tangible* form
  * [lasts a long time](https://www.copyright.gov/help/faq/faq-duration.html), depending on authorship (since 1978)
    * 70+life of a known author
    * for anonymous, pseudonymous, or work for hire:
       **120** years after **creation** or **95** years after **publication** 
  * In US, a federal power granted to Congress by the [copyright clause of the Constitution](http://constitutionus.com/#a1s8c8)
  * In the US at least, the doctrine of [fair use](https://www.copyright.gov/fair-use/more-info.html) allows very limited unlicensed use of copyrighted works

See also [https://copyright.gov/](https://copyright.gov/)

#### Patents

  * applies to **inventions** (must be **novel** and **non-obvious** eg not **prior art**)
  * one must **apply** for and be granted a patent ($$$)
  * application must disclose sufficient detail of invention
  * lasts 20 years (previously 17)
  * precedence determined by first-to-file (previously first-to-invent)

##### Copyright vs patents for code
  
Copyright covers specific creative expression. For example, copyright 
doesn't cover all versions of [a certain old German fairy tale](https://en.wikipedia.org/wiki/Snow_White)
but it has covered [a specific telling of that fairy tale](https://en.wikipedia.org/wiki/Snow_White_and_the_Seven_Dwarfs_(1937_film)).  

So, copyright could cover a specific body of code, but patents (at least in some jurisdictions) might cover 
the underlying algorithms. To work around a copyright, one might write in a different 
language with a different structure (**clean room** separation between 
design and implementation) to create a different specific expression of the 
operations in a code base.
 
There is not so general a way of getting around an algorithm patent aside 
from inventing a completely different algorithm--a patent might cover an 
algorithm regardless of how it is expressed.

#### Trademarks

  * Covers **identifying** marks: Names, symbols, **branding**, "trade dress".
  * One gets it by using it to identify one's goods (or for *service marks*, services).
  * Can keep it **indefinitely**, but its exclusive use **must be defended**.
  * Can be registered to strengthen remedies for infringement. 
  * Not in the Constitution explicitly, but managed alongside patents at USPTO.


Additional concepts:

  * **Moral rights** -- right of a creator to be identified with a work.
  * **work-for-hire** -- hiring company takes ownership (see 95 or 120 year copyright terms)  

So, **copyright**, **patents**, **trademark**, and **trade secrets** create legal
restrictions on use. 

A **license** then is a mechanism for lifting (usually, just some
of) these restrictions, usually with limited extent as spelled out in the
various conditions and qualifications in the text of a license.

