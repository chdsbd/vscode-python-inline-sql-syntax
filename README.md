# python-inline-sql-syntax

Add SQL syntax highlighting for Python strings.

## Features

### Syntax highlighting for mutli-line strings

![python sample with multi-line SQL](./images/multi-line-string.png)

Supported syntax:

```py
double_quotes_multi_line = """
select *
from users
where id = 82394;
"""
single_quotes_multi_line = '''
select *
from users
where id = 82394;
'''
```

Not supported:

```py
single_line_strings = 'select * from users where id = 82394;'
f_strings_ = f'select * from users where id = 82394;'
f_strings_multi_line = f'''
select *
from users
where id = 82394;
'''
```

## Development

### VSCode instructions

#### Get up and running straight away

- Press `F5` to open a new window with your extension loaded.

#### Make changes

- You can relaunch the extension from the debug toolbar after changing code in `src/extension.ts`.
- You can also reload (`Ctrl+R` or `Cmd+R` on Mac) the VS Code window with your extension to load your changes.

### Publish

```bash
vsce package
vsce login chdsbd
vsce publish <version>
```

[marketplace]: https://marketplace.visualstudio.com/items?itemName=chdsbd.python-inline-sql-syntax
