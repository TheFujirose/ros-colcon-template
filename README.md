# ROS 2 Examples

Various ROS 2 Examples

## Features

- **`Colcon`** package

## Technology

- **Python**: 3.10
- **ROS2**: HUMBLE

## Quick Start

### Prerequisites

- Install ROS 2 following [installation](https://docs.ros.org/en/humble/Installation.html) page.
- Set up your environment following [instructions](./wiki/setup/ENV.md) document.
- Install colcon following [instructions](./wiki/setup/COLCON.md) document.

## Development

### Building Workspace

Ensure you have set up your environment following [instructions](./wiki/setup/ENV.md) document, and have installed `colcon` following [this instructions](./wiki/setup/COLCON.md).

For building the workspace with Windows see the below note: Building with Windows.

Otherwise--regardless of Linux or macOs--navigate to the project root `Ros2-Examples/` and run `colcon build`. It may be needed to use the option `--symlink-install` as some build types do not support `devel` spaces. For more information on `catkin`'s `devel` space read [this documentation](https://catkin-tools.readthedocs.io/en/latest/advanced/linked_develspace.html)

```bash
colcon build --symlink-install
```

You can test it with the following command:

```bash
colon test --symlink-install
```

#### Building with Windows

To build packages on Windows you need to be in a Visual Studio environment.
It is reccomended to charge your device as source installation can take time.

First, open a Visual Studio Command Prompt (“x64 Native Tools Command Prompt for VS 2019”) running as Administrator.
then, build the `\humble` folder tree with the command:

```powershell
colcon build --merge-install
```

If you are doing a debug build follow the command

```powershell
python_d path\to\colcon_executable colcon.
```

Read [this article](https://docs.ros.org/en/humble/Installation/Alternatives/Windows-Development-Setup.html#extra-stuff-for-debug-mode) for more information on running Python code in debug builds on Windows.

##### Testing with Windows

To run packages with windows use a `x64 Native Tools Command Promp For VS 2019` and execute the following command:

```powershell
colcon test --merge-install
```

### Project Structure

```text
Ros2-Examples/
├── build/                       # Bash scripts
├── install/                     # Bash scripts
├── log/                         # Bash scripts
├── src/                         # Source code
├── wiki/                        # Additional documentation
│   ├── setup/                   # Setup documentation
│   └── CONTRIBUTING.md/         # Instructions on contributing to this repository
├── LICENSE/                     # GPL-3.0 license
└── README.md                    # Primary documentation
```

## Contributing

See the [contribution guide](wiki/CONTRIBUTING) to see how you can contribute!
