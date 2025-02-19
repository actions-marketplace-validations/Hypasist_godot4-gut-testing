# godot4-gut-testing

Not-so-complex GitHub Action to run your [Godot Unit Tests](https://github.com/bitwes/Gut).

It does the following:
  - Uses ubuntu docker image with Godot v4.3 installed
  - downloads GUT addons folder  and move it to the root of Godot project
  - starts a pre-test Godot run, that imports godot resources
  - runs Godot Unit Tests

# Usage

<!-- start usage -->
```yaml
- uses: Hypasist/godot4-gut-testing@v1.0
  with:
    # Path to GUT configuration. Example config is pasted below.
    # Default: ''
    gutConfigPath:

    # Extra flags to pass to both Godot runs. E.g. `--verbose`
    # Default: ''
    extraGodotFlags:

    # Boolean value, you can disable resource importing, if you include `.godot` folder in your repository.
    # Default: 'true'
    importGodotResources:
```
<!-- end usage -->

# Example GUT configuration:

```json
{
    "dirs":[
        "res://tests/"
    ],
    "include_subdirs":true,
    "ignore_pause":true,
    "log_level":2,
    "should_exit":true,
    "should_maximize":false
}
```


# License

The scripts and documentation in this project are released under the [MIT License](LICENSE)
