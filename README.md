# TheHaloMod

**The web-app for calculating Halo Model quantities!**

This is the source code for [TheHaloMod](http://hmf.icrar.org), which uses
the [hmf](https://github.com/steven-murray/hmf) and [halomod](https://github.com/steven-murray/halomod)
Python package to calculate halo model quantities.

The web-app is powered by [Django](https://www.djangoproject.com/) and uses
[Bootstrap 4](https://getbootstrap.com/) as a CSS framework.

To acknowledge use of this app, cite
[Murray, Power & Robotham (2013)](http://adsabs.harvard.edu/abs/2013A%26C.....3...23M").

This app began as `HMFcalc` back in 2013, and has been thoroughly reworked and expanded
to provide full halo model capabilities.

## Contributing

Clearly, this repository is intended for developers (users shouldn't need to see this
code, or I've done something wrong!). I would *love* contributions to this app from the
community -- whether in the form of bug reports, feature requests, or new code.
Please consider getting involved!

If you'd like to get involved but have never done any web-development before (like me
when I started this project), I'd suggest taking the
[Django Beginner's Tutorial](https://docs.djangoproject.com/en/3.0/intro/tutorial01/) to
wrap your head around things a bit.

After that, here's a bit of a primer of how this repo is laid out:

The top-level is reserved for interesting project-level stuff like this README, and
scripts for managing the website itself (things you call manually when you're on the
server, outside the context of the web-app itself).

The [TheHaloMod](TheHaloMod/) directory contains the website-level settings and structure (eg.
where urls point to).

The [templates](templates/) directory contains the HTML files (really, they're just
kinda-sorta HTML, they're actually templates) that define how each page of the website
will be structured (and often, the text on the website).

Finally, the most important directory: [halomod_app](halomod_app/).
This contains the logic of the web-application, as a bunch of python files.
Most important here are the `views.py`,
which defines the various things that happen when different URLs are accessed (not
always a web-page opening -- sometimes a download of a file, or a form displaying etc.),
and the `forms.py` which defines the (fairly large) form into which inputs for the
HMF are given.

### Running the Server Locally

To run the local server for development, do `python manage.py runserver` from the top
level. It should open a browser tab for you.
