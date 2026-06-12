# Hello World

Simple program to print greetings to the console.


# Development Environment

```sh
python3 -m venv virtualenv
source ./virtualenv/bin/activate
python -m pip --disable-pip-version-check list --outdated --format=json | python -c "import json, sys; print('\n'.join([x['name'] for x in json.load(sys.stdin)]))" | xargs --no-run-if-empty -n1 python -m pip install --upgrade
pip install -e '.[dev]' --config-settings editable_mode=compat
```


