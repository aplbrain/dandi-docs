# NWB GUIDE

The [NWB GUIDE](https://nwb-guide.readthedocs.io/en/stable/) (Graphical User Interface for Data Entry) is a cross-platform desktop application for converting data from common proprietary formats to NWB and uploading it to {{ instance.name }}.

## Overview

NWB GUIDE provides a user-friendly interface for:

- Converting data to NWB format
- Validating NWB files
- Uploading data to {{ instance.name }}
- Managing Dandisets

This tool is particularly useful for users who prefer a graphical interface over command-line tools.

## Getting Started with NWB GUIDE

1. **Installation**: Follow the [installation instructions](https://nwb-guide.readthedocs.io/en/stable/installation.html) to install NWB GUIDE on your system.

2. **Converting Data**: NWB GUIDE supports conversion from various formats. See the [NWB GUIDE tutorials](https://nwb-guide.readthedocs.io/en/stable/tutorials/index.html) for details.

3. **Dataset Publication**: The [Dataset Publication Tutorial](https://nwb-guide.readthedocs.io/en/latest/tutorials/dataset_publication.html) provides step-by-step instructions for publishing data to {{ instance.name }} using NWB GUIDE.

## Key Features

- **Intuitive Interface**: Easy-to-use graphical interface for managing the entire workflow from conversion to publication.
- **Format Support**: Supports conversion from many common neurophysiology data formats.
- **Validation**: Built-in validation to ensure your NWB files meet {{ instance.name }}'s requirements.
- **{{ instance.name }} Integration**: Direct upload to {{ instance.name }} without needing to use the command line.

## When to Use NWB GUIDE

NWB GUIDE is ideal for:

- Users who prefer graphical interfaces over command-line tools
- Automatically applying best practices for archival storage
- Quick validation and inspection of NWB files
- Straightforward uploads to {{ instance.name }}

For more complex conversion needs, you might consider [NeuroConv](./neuroconv.md) or direct use of [PyNWB and MatNWB](./pynwb-matnwb.md).
