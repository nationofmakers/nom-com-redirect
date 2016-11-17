# nom-com-redirect

This repo exists only to redirect nation-of-makers.com to
www.nationofmakers.us.

How we did this:
----------------

1. Create an A record per https://help.github.com/articles/setting-up-an-apex-domain/:

    nation-of-makers.com.      600     IN      A       192.30.252.153

2.  Turn on the "Github Pages|Source|master branch" in the nom-com-redirect repo.  

How this works:
---------------

The above A record tells web clients to send nation-of-makers.com
queries to github's servers. The ./CNAME file in this repo then tells
github to use this repo to answer those queries. The index.html in
this repo contains a meta refresh tag which then redirects the client
browser to www.nationofmakers.us. 

