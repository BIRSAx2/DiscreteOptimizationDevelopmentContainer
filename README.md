# Discrete Optimization Development Container for Visual Studio Code

This repository contains a pre-configured development container designed for conducting discrete optimization tasks within Visual Studio Code. The container is equipped with essential libraries and tools for discrete optimization, including Soplex, SCIP, and PySCIPOpt. The provided `basic_model.py` script showcases the functionality of the container by demonstrating the successful integration and utilization of these libraries.

## Overview

The development container simplifies the setup process for working on discrete optimization problems within Visual Studio Code. It includes the following key components:

- **Soplex:** A linear programming solver.
- **SCIP:** The SCIP Optimization Suite for mixed-integer linear and nonlinear programming.
- **PySCIPOpt:** The Python interface for SCIP, facilitating the formulation and resolution of optimization problems using Python.

## Usage

### Prerequisites

To utilize this development container, ensure you have Visual Studio Code installed along with the "Remote - Containers" extension.

### Getting Started

1. Clone or download this repository to your local machine.

2. Open the repository in Visual Studio Code.

3. When prompted, reopen the repository in the development container. Alternatively, use the command palette (`Ctrl/Cmd + Shift + P`) and select `Remote-Containers: Reopen in Container`.

### Running the Example Script

The `basic_model.py` script included in this repository serves as a demonstration of the functioning environment within the development container. It showcases the successful integration and operation of the installed libraries by solving a simple optimization problem.

To execute the example script within the container, open `basic_model.py` in Visual Studio Code and run it using the integrated terminal.

This will demonstrate the capabilities of the installed libraries by solving the provided optimization problem within the Visual Studio Code development environment.

## Additional Information

This development container is flexible and can be customized or extended to suit specific project requirements. Feel free to modify the provided `basic_model.py` or add your own scripts to leverage the installed libraries for your discrete optimization tasks.

For detailed information on library functionalities and advanced usage, refer to the documentation for [PySCIPOpt](https://pyscipopt.readthedocs.io/en/latest/) and [SCIP](https://scipopt.org/).
