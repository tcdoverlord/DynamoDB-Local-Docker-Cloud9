Steps to Fix Environment for AWS Cloud9
Topic: Fixing Dependencies and Setting Up AWS Cloud9
Questions	Notes
What version of Java is installed?	Checked Java installation using java --version. Output indicates OpenJDK 21.0.7-ea is installed.
How was Cloud9 installed?	Used the command:
	curl -L https://d3kgj69l4ph6w4.cloudfront.net/static/c9-install-2.0.0.sh | bash.
	Faced dependency issues requiring Python's venv module.
How were Python dependencies resolved?	Installed python3-venv and related dependencies using:
	sudo apt install python3-venv. Dependencies included:
	- python3-pip-whl
	- python3-setuptools-whl
	- python3.13-venv.
How was Python 2.7 installed?	Python 2.7 was installed using:
	1. Update repositories: sudo apt update.
	2. Install Python 2.7: sudo apt install python2.7. This also installed:
	- libpython2.7-minimal
	- libpython2.7-stdlib
	- python2.7-minimal.
How was pip installed for Python 2.7?	Downloaded get-pip.py for Python 2.7 with:
	curl https://bootstrap.pypa.io/pip/2.7/get-pip.py --output get-pip.py.
	Ran the installation using:
	sudo python2.7 get-pip.py. Installed:
	- pip-20.3.4
	- setuptools-44.1.1
	- wheel-0.37.1.
What if pip shows a deprecation warning?	Noted that Python 2.7 is deprecated. While pip was successfully installed, future projects should use Python 3.
How was Node.js installed?	Installed Node.js using Node Version Manager (NVM):
	1. Install NVM: curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.0/install.sh | bash.
	2. Source NVM using:
	bash<br>export NVM_DIR="$HOME/.nvm"<br>[ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh"<br>[ -s "$NVM_DIR/bash_completion" ] && . "$NVM_DIR/bash_completion"<br>
	3. Install Node.js: nvm install node. Result: Node.js v23.10.0 installed.
How to check installed versions?	Verified installations:
	Python 2.7: python2.7 --version (Result: Python 2.7.18)
	pip: pip --version (Result: pip 25.0)
	Node.js: node --version.

Steps to Resume Installation of AWS Cloud9
1. Check for Dependencies
From earlier, the installer script showed that Python's venv module was missing. We fixed this by installing python3-venv. Verify it’s installed correctly:
sudo apt update
sudo apt install python3-venv
2. Run the Cloud9 Installer Again
Now re-run the Cloud9 installer:
curl -L https://d3kgj69l4ph6w4.cloudfront.net/static/c9-install-2.0.0.sh | bash
3. Verify Python 2.7 and Pip
If the installer requests Python 2.7 dependencies, verify Python 2.7 is installed:
python2.7 --version
pip --version
If Python 2.7 or pip was skipped earlier, resolve it by reinstalling:
sudo apt update
sudo apt install python2.7
curl https://bootstrap.pypa.io/pip/2.7/get-pip.py --output get-pip.py
sudo python2.7 get-pip.py
4. Node.js Installation
We resolved Node.js installation using NVM, so Node.js (version 23.10.0) is already available. Confirm it with:
node --version

Testing the Cloud9 Installation
Once the installer runs successfully, test Cloud9 by launching it:
cloud9
If issues persist, the log files or error messages will be critical for troubleshooting. Share what happens next, and we’ll tackle it together!
