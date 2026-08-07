# bbcp

`bbcp` is a high-performance file copy utility designed for transferring large datasets efficiently over high-bandwidth networks.

## Features

- High-speed parallel data transfer
- Optimized for large files and large datasets
- Supports multiple TCP streams to maximize network utilization
- Suitable for HPC, data centers, and cross-site data migration scenarios

## Use Cases

- Large-scale scientific data transfer
- HPC cluster data synchronization
- Data center to data center migration
- Backup and archive operations

## Installation

Build from source:

```bash
git clone https://github.com/kinkcamp/bbcp.git
cd bbcp
make
```

After building, add the binary to your PATH:

```bash
export PATH=$PWD:$PATH
```

## Basic Usage

Example:

```bash
bbcp source_file user@remote_host:/target/path/
```

Copy a directory:

```bash
bbcp -r source_dir user@remote_host:/target/path/
```

Use multiple streams:

```bash
bbcp -s 8 source_file user@remote_host:/target/path/
```

## Performance Tuning

For high-speed networks (10GbE/25GbE/100GbE), consider tuning:

- Number of parallel streams (`-s`)
- TCP buffer size
- Host network parameters
- Storage performance

## License

See the project license file for details.
