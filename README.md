# ads_bibtex
A repo for bibtex style files used in astro and which play well with ADS output

Existing resources and people working on this:
* Alberto Accomazzi maintains the "ADS" bibtex packages: http://ads.harvard.edu/pubs/bibtex/
* Norman Gray's modification of Elsevier style files: https://github.com/nxg/elsarticle
* Tim Jenness is involved in MNRAS style maintenance (url needed)

See also Norman Gray's latest proposal: http://text.nxg.me.uk/2015/2ncf

### Original inspiration from Norman Gray's (norman@astro.gla.ac.uk):

There are a number of informal BibTeX conventions for things like the 'url' field or 'doi' or 'eprint'.  They're 'informal' since they're not documented anywhere, but are either obvious, or have some obvious consensus on use.  As well, there's at least one fairly common BibTeX entry type -- @webpage -- which I at least support in the 'urlbst' style.

It would surely be useful to have some sort of registry of these conventions, and the only way that would emerge would be by some sort of ground-up community effort.  Would you agree?

The obvious technical mechanism would be a wiki page, but a github.io page attached to a github 'organisation' would be a more fashionable alternative.  The obvious social mechanism would be to do some quick census of available .bst files looking for the individuals maintaining them, and ping those people.  I think a (possibly slightly fake) question on tex.stackexchange.com might reach quite a few people.  A googlegroup would act as a suitable proxy for a mailing list, unless anyone has better suggestions.

The conventions I can think of are:

* url: the URL associated with a resource

* lastchecked: it's often recommended that if a URL is cited, there should be a 'lastchecked' note as well; this should be a date, without it being restricted to any particular format

* doi: the DOI associated with a publication; the prefix 'doi;' should not be present, nor should it be expressed as a dx.doi.org URL

* eprint: there are two possible conventions here.  The one represented in the output of ADS (ie, Alberto) has 'eprint' being a repository identifier, which relates to 'arXiv' by default, but which can also be an ASCL identifier (others?); the repository is indicated by an 'archiveprefix' key, which can be 'arXiv' (no colon) or 'ascl' (correct?).  Alternatively (and this one is implemented in the mn2e style file, though that's still experimental) is to have a prefix within the 'eprint' key, thus 'yymm.nnnn', or 'arxiv:yymm.nnnn' or 'ascl:yymm.nnn' (with the default being again arXiv).  It doesn't make any sense to have two competing conventions, but there's no way to resolve this other than by guesswork.
