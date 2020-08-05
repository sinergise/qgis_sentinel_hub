# SentinelHub QGIS Plugin

SentinelHub QGIS Plugin enables users to harness power of [Sentinel Hub services](https://www.sentinel-hub.com/) directly from QGIS.

Since version `1.4.0` the plugin only works with QGIS 3 while earlier versions support both QGIS 2 and QGIS 3.

## Install

SentinelHub QGIS Plugin is available in QGIS Official Plugin Repository. For install just open QGIS, select `Plugins -> Manage and Install Plugins` and search for the plugin.

In case of manual installation you can download [latest release](https://github.com/sentinel-hub/sentinelhub-qgis-plugin/releases/latest), unzip it into QGIS Plugin directory and enable plugin under QGIS Installed Plugins.

## Usage

For a quick tutorial check this [article](https://medium.com/sentinel-hub/control-sentinel-hub-from-within-qgis-2a83eb7f13db).

## Development

### Set up an environment

- Set up an empty Python environment.
- Install development requirements
```bash
pip install -r requirements-dev.txt
```
- Configure a path to QGIS Python environment. This depends on your OS and QGIS installation. Here is an example for Linux:
```bash
export PYTHONPATH=/usr/lib/python3/dist-packages
```

### Development tips

- Use `pb_tool` to package and deploy the code to your local QGIS repository
```bash
pbt deploy -y
```
- Use `pylint` to check code style
```bash
pylint
```
- Install [Plugin reloader](https://plugins.qgis.org/plugins/plugin_reloader/) in QGIS in order to dynamically reload your plugin every time you redeploy it.

### Release

- Package a code into a zip file using `pb_tool`
```bash
pbt zip
```
- Release the plugin on [GitHub](https://github.com/sentinel-hub/sentinelhub-qgis-plugin/releases) and attach the generated zip file.
- Release the plugin to [QGIS Python Plugins Repository](https://plugins.qgis.org/plugins/SentinelHub/) by manually uploading the zip file to a [release form](https://plugins.qgis.org/plugins/SentinelHub/version/add/).
