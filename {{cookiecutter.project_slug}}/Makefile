setup-pre-commit:
	pip3 install pre-commit==3.7.0 --break-system-packages
	pre-commit install --hook-type pre-commit

setup-pants:
	export PATH=$$PATH:~/.local/bin:/builder/home/.local/bin/pants && bash get-pants.sh && pants --version

init: setup-pre-commit setup-pants
