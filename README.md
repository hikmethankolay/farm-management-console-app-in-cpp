# Farm Management Project Library Generation and Testing

## Overview

This project is a cross-platform Farm Management System built using C++, CMake, CTest, GoogleTest, and Doxygen. It supports various coverage reports and detailed documentation.

## Requirements

- **CMake** >= 3.12
- **C++ Standard** >= 11
- **GoogleTest** (for module testing)
- **Visual Studio Community Edition** (for Windows builds)
- **Ninja** (for WSL/Linux builds)

---

## Setup Development Environment

### Step 1: Configure Pre-Commit Hooks (Windows and WSL)
Run `1-configure-pre-commit.bat` to copy the `1-pre-commit` script to `.git/hooks`. This ensures:
- Checking the integrity of `README.md`, `.gitignore`, and Doxygen files.
- Code formatting using the Astyle tool.

### Step 2: Create `.gitignore` (Windows and WSL)
Run `2-create-git-ignore.bat` to generate a `.gitignore` file if it's missing.

### Step 3: Install Package Managers (Windows Only)
Run `3-install-package-manager.bat` to install Chocolatey and Scoop package managers.

### Step 4: Install Required Applications (Windows Only)
Run `4-install-windows-environment.bat` to set up all required tools and applications.

### Step 5: Setup WSL Environment (WSL Only)
Open PowerShell as an administrator, navigate to the project folder in WSL, and run `4-install-wsl-environment.sh` to configure the WSL environment.

---

## Generate Development Environment
Run `9-clean-configure-app-windows.bat` to create a Visual Studio Community Edition project file. Alternatively, use CMake to generate the development environment manually.

---

## Build, Test, and Package the Application

### On Windows
Run `7-build-app-windows.bat` to:
- Build the project.
- Run tests.
- Package binaries for deployment.

Additional scripts:
- `7-build-doc-windows.bat`: Generate documentation only.
- `8-build-test-windows.bat`: Run tests only.

### On WSL/Linux
Run `7-build-app-linux.sh` to perform similar operations as on Windows, tailored for the Linux environment.

---

## Clean Project Outputs
Run `9-clean-project.bat` to remove all generated outputs.

---

## System Architecture
The Farm Management System uses the `fstream` library for file operations, including:
- **file_read()**: Reads data from files.
- **file_write()**: Overwrites all data in a file.
- **file_update()**: Updates a specific record.
- **file_line_delete()**: Deletes a specific record line.
- **file_append()**: Appends new records to the end of a file.

### Functionalities
The system provides the following features:

#### a. Crop and Livestock Management
1. **Crop Records**:
   - Crop type
   - Planting and harvest dates
   - Field area
   - Expected yield

2. **Livestock Records**:
   - Livestock type
   - Ear tag number
   - Birth date
   - Diet and weight
   - Health status (e.g., illness, vet check-ups, death records)

#### b. Harvesting and Production Planning
3. **Pest Records**:
   - Pest type and application details
   - Crop type treated
   - Pest schedule

4. **Irrigation Records**:
   - Irrigated crop types
   - Irrigation schedules

#### c. Equipment and Vehicle Maintenance
5. **Vehicle Records**:
   - Vehicle type, model, purchase date
   - Maintenance history and schedules

6. **Equipment Records**:
   - Equipment type, model, purchase date
   - Maintenance history and schedules

#### d. Reporting
7. **Crop Yield Reports**:
   - Sample size and expected harvest calculations.

8. **Profit Reports**:
   - Crop costs, expected income, and profit.

9. **Livestock Health Reports**:
   - Illness history, vet check dates, and health status.

---

## Testing and Validation

- Tested using **GoogleTest** and **CTest**.
- Achieved **95% test coverage** and **100% unit test success**.

---

## Supported Platforms

![Ubuntu badge](assets/badge-ubuntu.svg) ![macOS badge](assets/badge-macos.svg) ![Windows badge](assets/badge-windows.svg)

### Test Coverage Ratios
| Coverage Type | Windows OS                                                             | Linux OS (WSL-Ubuntu 20.04)                                              |
| ------------- | ---------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| Line Based    | ![Line Coverage](assets/codecoveragelibwin/badge_linecoverage.svg)     | ![Line Coverage](assets/codecoverageliblinux/badge_linecoverage.svg)     |
| Branch Based  | ![Branch Coverage](assets/codecoveragelibwin/badge_branchcoverage.svg) | ![Branch Coverage](assets/codecoverageliblinux/badge_branchcoverage.svg) |
| Method Based  | ![Method Coverage](assets/codecoveragelibwin/badge_methodcoverage.svg) | ![Method Coverage](assets/codecoverageliblinux/badge_methodcoverage.svg) |

### Documentation Coverage Ratios
|                    | Windows OS                                                        | Linux OS (WSL-Ubuntu 20.04)                                         |
| ------------------ | ----------------------------------------------------------------- | ------------------------------------------------------------------- |
| **Coverage Ratio** | ![Line Coverage](assets/doccoveragelibwin/badge_linecoverage.svg) | ![Line Coverage](assets/doccoverageliblinux/badge_linecoverage.svg) |

---

## Building Applications

### On Windows
Run `7-build-app-windows.bat` to perform all build operations, including:
- Cleaning project outputs.
- Generating documentation.
- Running tests and collecting coverage data.
- Generating deployment-ready binaries.

### On WSL/Linux
Run `7-build-app-linux.sh` to perform equivalent tasks in a Linux environment.

---

$End-Of-File$

