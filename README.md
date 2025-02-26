# TAG.Theme.NeuroExchange

Free theme that can be used on any [TAG Neuron(R)](https://lab.tagroot.io/Documentation/Index.md). Specificly designed for [Neuro Exchange](https://neuro-exchange.com).

## Installable Package

The Neuro Exchange theme has been made into a package that can be downloaded and installed on any
[TAG Neuron](https://lab.tagroot.io/Documentation/Index.md). To create a package, that can be distributed or installed, you begin by creating
a _manifest file_. This repository contains a manifest file called `TAG.NeuroExchange.Theme.manifest`. It defines the content files included in the package.
You then use the `Waher.Utility.Install` and `Waher.Utility.Sign` command-line tools in the [IoT Gateway](https://github.com/PeterWaher/IoTGateway)
repository, to create a package file and cryptographically sign it for secure distribution across the Neuron network.

| Package information |                                                                                                                |
| :------------------ | :------------------------------------------------------------------------------------------------------------- |
| Package             | `TAG.NeuroExchange.Theme`                                                                                      |
| Installation key    | `BGVWw9FYGj6+mY8nxScZgoKRC8SiV80mWJhHXfUZL3ASrwZSab5PdEwmyfwpJVUEWEMNST4HWayA1640d45c2eae16ecf48e883c75dd25f7` |
| More Information    |                                                                                                                |

To install package on a TAG Neuron(R), execute the following command in a chat admin interface:

```
install nobackup TAG.NeuroExchange.Theme.package BGVWw9FYGj6+mY8nxScZgoKRC8SiV80mWJhHXfUZL3ASrwZSab5PdEwmyfwpJVUEWEMNST4HWayA1640d45c2eae16ecf48e883c75dd25f7
```


## Development

The Neuro Exchange theme can be hosted on any [IoT Gateway Host](https://github.com/PeterWaher/IoTGateway). This includes the
[TAG Neuron(R)](https://lab.tagroot.io/Documentation/Index.md), The IoT Gateway itself,
which you can run on your local machine. To simplify development, once the project is cloned, add a `FileFolder` reference
to your repository folder in your [gateway.config file](https://lab.tagroot.io/Documentation/IoTGateway/GatewayConfig.md).
This allows you to test and run your changes immediately, without having to synchronize the folder contents with an external
host, or go through the trouble of generating a distributable software package just for testing purposes.

Example:

```
<FileFolders>
  <FileFolder webFolder="/Themes/TagNexBase" folderPath="C:\My Projects\TAG.NeuroExchange.Theme\Root\Themes\TagNexBase"/>
  <FileFolder webFolder="/Themes/TagNexLight" folderPath="C:\My Projects\TAG.NeuroExchange.Theme\Root\Themes\TagNexLight"/>
  <FileFolder webFolder="/Themes/TagNexDark" folderPath="C:\My Projects\TAG.NeuroExchange.Theme\Root\Themes\TagNexDark"/>
</FileFolders>
```

**Note**: Once file folder reference is added, you need to restart the IoT Gateway service for the change to take effect.
