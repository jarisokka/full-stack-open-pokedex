## CI setup for Python

When using Python we need to supervise our packages/dependencies this is important for a successful build. In this project we supervise our dependencies with Poetry. Python version is also defined using Poetry poetry init --python "^3.10". All dependencies are installed using Poetry.

For linting Pylint is a good choice for Python. It is important that everyone is using the same linting settings. These settings are in the project root directory .pylintrc-file. This will be shared to everyone.

For testing we use Unitest. Everyone in the project is responsible to write tests for the codes they are producing. Testing is done also with Poetry using pytest and poetry shell. So testing is done in a virtual environment. 

Running the code, testing and linting will all be done by using Poetry using poetry run invoke.

### Alternatives for Jenkins and GitHUB actions.

There seem to be several alternative solutions. Most convincing for the first glimpse are CircleCI and TeamCity. 

CircleCI can be used in their cloud or on users own infrastructure, so it seems to be flexible. Benefits for using cloud are: scalable, flexible and efficient. Cloud works great especially in IaaS and PaaS cases. Also there is benefit for no need for servers and maintaining those. You can also use a hybrid solution. So in bigger and more scalable situations cloud is a better choice. 
