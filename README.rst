================================
Diablo III Web Api Python Client
================================

Introduction
============
this is a Python module to query Diablo 3 public data (see https://github.com/Blizzard/d3-api-docs )
The Diablo 3 API resources are not publicly available: this implememntation is based on the actual doc.


Installation
============

pip install pip install git+https://github.com/sammyrulez/diablo-api-py.git

Usage
=====

    import diablo
	c = diablo.Client('host', 'battletag_name', 'battletag_number')
	career = c.career_profile()

The carrer object has the same structure of the json returned from the same api call https://github.com/Blizzard/d3-api-docs#career-profile-example.
Attributes name differs from the json fields: '-' has been replaced with '_' to match python syntax.
'heros' and 'last_hero_played' attributes have 'Lazy' object in which details are loaded from the remote service only if you invoke them