# CHALLENGE CONVERTED TO MY NOTES

- 1.5 hours
- Gistapi is a HTTP API server 
	- Flask 
	- searches a user's public Github Gists
- existing code implements Flask boilerplate
- main goal
	- implement an endpoint that searches a user's Gists with a regular expression
	- search user `justdionysus` with pattern `import requests`
- notes
	- you'll have to write some HTTP queries to the Github API to pull down each Gist for the target user
	- you MAY use a basic HTTP library is ok e.g.
		- requests
			- https://pypi.org/project/requests
		- aiohttp
			- https://docs.aiohttp.org/en/stable
		- urllib3
			- https://pypi.org/project/urllib3
	- you may NOT use a github API client 
		- PyGithub
			- https://github.com/PyGithub/PyGithub
		- gidgethub 
			- https://github.com/gidgethub/gidgethub
- extras (stretch goals)
	- implement tests using a testing framework of your choice, e.g.
		- pytest
			- https://docs.pytest.org
		- unittest
			- https://docs.python.org/3/library/unittest.html
		- nose2
			- https://docs.nose2.io/en/latest
		- HTTPretty
			- https://httpretty.readthedocs.io/en/latest
	- implement validation
	- implement error handling
	- implement pagination
	- migrate from `requirements.txt` to `pyproject.toml` using e.g. 
		- poetry
			- https://python-poetry.org
	- implement a Dockerfile
	- implement handling of huge gists
	- set up necessary tools to ensure code quality, e.g.
		- Black
			- https://github.com/psf/black
		- Flake8
			- https://flake8.pycqa.org
		- Pylint
			- https://pypi.org/project/pylint
		- Sphinx (documentation)
			- https://www.sphinx-doc.org
	- create documentation for
		- how to start the application
		- how to build the docker image
		- how to run tests
		- how to run code quality checkers, e.g. Black, Flake8, Pylint
	- create TODO.md file speaking to the following points
		- database
			- SQL or NoSQL?
			- which database 
			- how to set up and implement 
		- security
			- how to protect the api from abuse, e.g.
				- authentication/authorization
				- validation/sanitizing
				- logging/monitoring
				- penetration testing
				- secure deployment
		- cloud deployment
			- advantages/disadvantages of: 
				- AWS
				- Azure
				- Google Cloud
				- Hetzner
				- DigitalOcean
			- what steps does cloud implementation involve
			- what kind of devops monitoring tools could we use to make sure it is working as expected

# Challenge

This challenge is divided between the main task and additional stretch goals. All of those stretch goals are optional, but we would love to see them implemented. It is expected that you should be able to finish the challenge in about 1.5 hours. If you feel you are not able to implement everything on time, please, try instead describing how you would solve the points you didn't finish.

And also, please do not hesitate to ask any questions. Good luck!

## gistapi

Gistapi is a simple HTTP API server implemented in Flask for searching a user's public Github Gists.
The existing code already implements most of the Flask boilerplate for you.
The main functionality is left for you to implement.
The goal is to implement an endpoint that searches a user's Gists with a regular expression.
For example, I'd like to know all Gists for user `justdionysus` that contain the pattern `import requests`.
The code in `gistapi.py` contains some comments to help you find your way.

To complete the challenge, you'll have to write some HTTP queries from `Gistapi` to the Github API to pull down each Gist for the target user.
Please don't use a github API client (i.e. using a basic HTTP library like requests or aiohttp or urllib3 is fine but not PyGithub or similar).


## Stretch goals

* Implement a few tests (using a testing framework of your choice)
* In all places where it makes sense, implement data validation, error handling, pagination
* Migrate from `requirements.txt` to `pyproject.toml` (e.g. using [poetry](https://python-poetry.org/))
* Implement a simple Dockerfile
* Implement handling of huge gists
* Set up the necessary tools to ensure code quality (feel free to pick up a set of tools you personally prefer)
* Document how to start the application, how to build the docker image, how to run tests, and (optionally) how to run code quality checkers
* Prepare a TODO.md file describing possible further improvements to the archtiecture:
    - Can we use a database? What for? SQL or NoSQL?
    - How can we protect the api from abusing it?
    - How can we deploy the application in a cloud environment?
    - How can we be sure the application is alive and works as expected when deployed into a cloud environment?
    - Any other topics you may find interesting and/or important to cover
