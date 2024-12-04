# RAB Smash Splitter Part 1

## Overview
This script is a modified version from the original [RAB Smash Splitter](https://www.nexusmods.com/skyrimspecialedition/mods/24321?tab=description)
to make it works with newer `SSEEDIT` version like `4.1.5` and making it rollover to next plugin when hitting 253 master limits.

RAB Smash Splitter Part 1 is a component of a plugin splitter tool designed to manage plugins in modded environments like Skyrim SE. This script aims to handle the issue of exceeding Skyrim's master plugin limit by creating QuickLoader plugins that distribute signatures across multiple files efficiently.

## Installation

1. **Prerequisites**:
    - Ensure that xEdit is properly installed and configured.
    - Make sure you have access to the required mod files and master lists.

2. **Setup**:
    - Copy `RAB_SmashSplitter_Part1.pas` into your xEdit scripts directory.
    - Ensure the script has necessary permissions to create and modify files in the target environment.

## Usage

1. **Initialization**:
    - Launch xEdit and load your mod list.
    - Execute the `RAB_SmashSplitter_Part1` script from xEdit's scripting interface.

2. **Running the Script**:
    - The script will automatically handle the creation of QuickLoader files, check for overlapping records, and distribute plugins within the master file limit.

3. **Outputs**:
    - QuickLoader plugins with relevant signatures, ensuring effective management of mod load orders.

## Key Functions

- **Initialize**: Sets up global variables and begins the QuickLoader generation process.
- **Quickloader_StartNext**: Prepares for a new QuickLoader file creation.
- **Create_Plugin**: Manages the creation and validation of new plugin files.
- **Quickloader_Finish**: Finalizes the current QuickLoader, adding all necessary masters.
- **GetBestNextSig**: Identifies the best signature for inclusion in the current QuickLoader file.

## Considerations

- Ensure you do not exceed Skyrim's hard limit on master files (255), accounting for base files.
- Consistently verify that all necessary dependencies and masters are documented and included.
- Consider logging and exception handling for runtime errors to aid future debugging.

## Maintenance

- Regularly update the signature list (`InitSigs`) to accommodate new record types or modding standards.
- Review and refactor code to maintain efficiency and handle new edge cases as mod configurations evolve.

## Contribution

Feel free to contribute by opening issues or pull requests on the repository. Feedback and suggestions are welcome to improve functionality or address potential bugs.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.
