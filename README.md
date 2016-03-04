# chef-dump-attr
Dump attributes command for Chef

## Requirements

- `chef`
- `ohai`

## Usage

```
Usage: chef-dump-attr [options]
    -j JSON_ATTRIBS,                 Load attributes from a JSON file
        --json-attributes
    -c, --config FILE_PATH           The configuration file to use
    -r, --role-path ROLE_PATH        Role path
        --cookbook-path COOKPATH_PATH
                                     Cookpath path
    -d DATA_BAG_PATH,                Data bags path
        --data-bag-path
    -o, --output OUTPUT              Output type (json, ruby)
        --include-ohai               Include ohai
        --ohai                       Output ohai
        --ohai-plugin-dir            A directory to add to the Ohai search path
        --data-bag-name              Data bag name
        --data-bag-item              Data bag item
        --no-pretty                  Not puretty output
    -v, --version                    Show version
```

## Example

### Attributes

```
$ ./chef-dump-attr -c client.rb -j node.json
```

### Ohai

```
$ ./chef-dump-attr -c client.rb -j node.json --ohai
```

### Attributes & Ohai

```
$ ./chef-dump-attr -c client.rb -j node.json --include-ohai
```

### Output json

```
$ ./chef-dump-attr -c client.rb -j node.json [--output json]
```

### Output hash

```
$ ./chef-dump-attr -c client.rb -j node.json [--output ruby]
```

### Not puretty output

```
$ ./chef-dump-attr -c client.rb -j node.json --no-pretty
```

## TODO

- Support Data bags
