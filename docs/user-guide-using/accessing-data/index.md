# Accessing Data

{{ instance.name }} provides multiple ways to access data stored in the archive. This page provides an overview of the different methods available for accessing data from Dandisets.

## Access Methods Overview

{{ instance.name }} offers several methods for accessing data, each suited to different use cases:

1. **Web Interface**: Browse and download individual files directly from the {{ instance.name }} web application.
2. **{{ instance.name }} CLI**: Command-line tool for downloading entire Dandisets or specific files.
3. **DataLad**: Access Dandisets as Git repositories with DataLad for version control and reproducibility.
4. **WebDAV**: Access {{ instance.name }} data using standard WebDAV clients.
5. **{{ instance.name }} Hub**: Analyze data directly in the cloud using Jupyter notebooks.
6. **Programmatic Access**: Access data programmatically using the {{ instance.name }} API through Python or other languages.

## Choosing the Right Access Method

The best method for accessing data depends on your specific needs:

- **For browsing and exploring data**: Use the [Web Interface](./downloading.md#using-the-dandi-web-application)
- **For downloading entire Dandisets**: Use the [{{ instance.name }} CLI](./downloading.md#using-the-python-cli-client)
- **For version control and reproducibility**: Use [DataLad](./downloading.md#using-datalad)
- **For integration with existing tools**: Use [WebDAV](./downloading.md#using-webdav)
- **For cloud-based analysis**: Use [{{ instance.name }} Hub](../dandi-hub.md)
- **For programmatic access**: Use the [{{ instance.name }} Python Client](https://dandi.readthedocs.io/)

## Data Access Considerations

When accessing data from {{ instance.name }}, consider the following:

- **Data Size**: Large datasets may be better accessed using the {{ instance.name }} CLI or DataLad rather than the web interface.
- **Bandwidth**: For users with limited bandwidth, consider using {{ instance.name }} Hub to analyze data in the cloud.
- **Reproducibility**: DataLad provides version control and reproducibility features that are valuable for scientific workflows.
- **Streaming**: For large files, streaming access may be more efficient than downloading entire files.

## Next Steps

Explore the following pages for detailed information on each access method:

- [Downloading Data](./downloading.md): Learn how to download data using the web interface, {{ instance.name }} CLI, DataLad, or WebDAV.
- [Streaming Data](./streaming.md): Learn how to stream data without downloading entire files.
- [External Services](./external-services.md): Learn about external services that can be used to access and analyze {{ instance.name }} data.
- [{{ instance.name }} Hub](../dandi-hub.md): Learn how to use {{ instance.name }} Hub for cloud-based analysis.
