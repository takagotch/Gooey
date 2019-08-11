### gooey
---
https://github.com/chriskiehl/Gooey

```py
from gooey import Gooey
def main():
  parser = ArgumentParser(...)

@Gooey(advanced=Boolean,
  language=language_string,
  show_config=True,
  target=executable_cmd,
  program_name='name',
  program_description,
  required_cols=1,
  optional_cols=2,
  dump_build_config=False,
  load_build_config=None,
  monospace_display=False)
def main():
  parser = ArgumentParser(...)


parser = ArgumentParser()
search_group = parser.add_argument_group(
  "Search Options",
  "Customize the search options"
)

search_group.add_argument(
  '--query',
  help='Base search stirng'
)

@Gooey(progress_regex=r"^progress: (?P<current>\d+)(?P<total>\d+)$",
  progress_expr="current / total * 100")

@Gooey(program_name='Custom icon demo', image_dir='/path/to/my/image/directory')
def main():

parser.add_argument(
  '--load',
  metavar='Load Previous Save',
  help='Load a Previous Save',
  help='Load a Previous save file',
  dest='filename',
  widget='Dropdown',
  choices=list_savefiles(),
)

from gooey.python_bindings_gooey_decorator import Gooey
from gooey.python_bindings_gooey_parser import GooeyParser

@Gooey
def main():
  parser = GooeyParser(description='Example validator')
  parser.add_argument(
    'secret',
    metavar='Super Secret Number',
    help='A number specifically between 2 and 14',
    gooey_options={
      'validator': {
        'test': '2 <= int(user_input) <= 14',
        'message': 'Must be between 2 and 14'
      }
    })
  args = parser.parse_args()
  
  print("Cool! Your secret number is: ", args.secret)

gooey_options={
  'validator': {
    'test': 'len(user_input) > 3',
    'message': 'some helpful message'
  }
}

@gooey(advanced=True)
def main():
```

```sh
pip install Gooey
git clone https://github.com/chriskieh1/Gooey.git
python setup.py install 
```

```
```


