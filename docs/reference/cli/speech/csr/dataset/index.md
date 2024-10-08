# `ai speech csr dataset`

The `ai speech csr dataset` command is used to manage custom speech recognition datasets in Azure AI services. This command is part of the Azure AI CLI.

### Usage

``` bash title="Create a new custom speech recognition dataset"
ai speech csr dataset <command> [options]
```

### Sub-Commands

| Sub-Command | Description |
| ----------- | ----------- |
| [ai speech csr dataset create](./create.md) | Create a new custom speech recognition dataset |
| [ai speech csr dataset delete](./delete.md) | Delete an existing custom speech recognition dataset |
| [ai speech csr dataset download](./download.md) | Download a custom speech recognition dataset |
| [ai speech csr dataset list](./list.md) | List all custom speech recognition datasets |
| [ai speech csr dataset status](./status.md) | Check the status of a custom speech recognition dataset |
| [ai speech csr dataset update](./update.md) | Update an existing custom speech recognition dataset |
| [ai speech csr dataset upload](./upload.md) | Upload data to a custom speech recognition dataset |

### Examples

``` bash title="Create a new custom speech recognition dataset"
ai speech csr dataset create --project <URL> --name <NAME> --kind <KIND> --content <URL> --language <LANGUAGE> --description <DESCRIPTION>
```

``` bash title="Delete an existing custom speech recognition dataset"
ai speech csr dataset delete --dataset-id <ID>
```

``` bash title="Download a custom speech recognition dataset"
ai speech csr dataset download --dataset-id <ID>
```

``` bash title="List all custom speech recognition datasets"
ai speech csr dataset list
```

``` bash title="Check the status of a custom speech recognition dataset"
ai speech csr dataset status --dataset-id <ID>
```

``` bash title="Update an existing custom speech recognition dataset"
ai speech csr dataset update --dataset-id <ID> --name <NEW_NAME>
```

``` bash title="Upload data to a custom speech recognition dataset"
ai speech csr dataset upload --dataset-id <ID> --content <FILE_PATH>
```