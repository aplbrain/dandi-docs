Data management including upload, download, and validation is handled through a local {{ instance.name }} Client.  
The {{ instance.name }} Client provides both a command line interface (CLI) and Python API.

## Update the {{ instance.name }} Client to reference your API

To reference your DANDI-clone API, [update the URLs reference per each CLI action](https://github.com/dandi/dandi-cli/blob/15196a93310618f8897c7b43444e216bbb094549/dandi/consts.py#L119-L135) and push a PR to the [dandi-cli GitHub repository](https://github.com/dandi/dandi-cli).

Here is an [example PR](https://github.com/dandi/dandi-cli/pull/1527) of another clone adding to the available instances of `DandiInstance` objects in the `dandi-cli`.

For example:

```python
known_instances = {
    "dandi": DandiInstance(
        "dandi",
        "{{ instance.uri }}",
        "https://api.dandiarchive.org/api",
    ),
    "dandi-sandbox": DandiInstance(
        "dandi-sandbox",
        "https://sandbox.<your-domain>.org",
        "https://api.sandbox.<your-domain>.org/api",
    ),
    "dandi-api-local-docker-tests": DandiInstance(
        "dandi-api-local-docker-tests",
        f"http://{instancehost}:8085",
        f"http://{instancehost}:8000/api",
    ),
    "<your-dandi-clone>": DandiInstance( # Your own "dandi"
        "<your-dandi-clone>", # Your own "dandi"
        "https://<your-dandi-clone-domain>.org", 
        "https://api.<your-dandi-clone-domain>.org/api", 
    ),
}
```

Once your {{ instance.name }} clone is added to the list of available `DandiInstance` objects, you should be able to perform operations via the `-i` flag.  For example:

`dandi upload -i <your-dandi-clone>`

## Access credentials

Users will be prompted for a `DANDI_API_KEY`
environment variable.  This variable does not need to be unique to your {{ instance.name }} clone.  A user can just set their `DANDI_API_KEY` to the value that your {{ instance.name }} API clone issues.  See docs on [storing access credentials](https://www.dandiarchive.org/handbook/13_upload/#storing-access-credentials).

## Versioning

The {{ instance.name }} Client leverages a tool called [versioneer](https://pypi.org/project/versioneer/) for semantic versioning in PyPI.

Upon merging of a PR into `master`, if the `release` label is attached to the PR
`versioneer` will generate a human-readable CHANGELOG entry, and then push to PyPI the new semantic version.  For more details on labeling `dandi-cli` pull requests, see [here](https://github.com/dandi/dandi-cli/blob/master/DEVELOPMENT.md#releasing-with-github-actions-auto-and-pull-requests).

### Resources
- [PyPI package](https://pypi.org/project/dandi/)
- [Source code](https://github.com/dandi/dandi-cli)
- [Developer instructions](https://github.com/dandi/dandi-cli/blob/master/DEVELOPMENT.md)




