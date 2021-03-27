# BlueMicro_Builder
Initializes and Builds your own BlueMicro_BLE firmware.

- Fork the repository
- Make sure that github actions is enabled
  - Go to settings (of your fork), 
  - Go down to the "Actions" section,
  - Select "Allow all actions"
- Edit one of the workflow files (located in .github\workflows) and edit the following entries (you can do this in the GitHub file editor):
  - keyboard: ['4x4Tutorials']
  - keymap: ['base']
  - keyboard_config: ['single']
  - hardware_config: ['feather52832/4x4Backpack']
  - compile_with: ['4x4macropad_nrf52832']
  - setup_build_yml: [false]
- Go to "Actions" at the top of your repo
- Select the workflow you just edited, you should see a "Run Workflow" menu to the right
- Trigger Workflow.  This will run a GitHub Action to copy the necessary files from the BlueMicro_BLE firmware and copy over the keyboard and configuration files you have selected above.
- Once the action has completed, go back to the top of your repository, you should now see a folder that contains all the files you need to compile your own firmware.
- For nRF52832 boards, you will need to download the firmware to your computer, compile and flash it using the Arcuino IDE or Arduino CLI. You will then flash it to your board using the Arduino Tools on your computer.
- For nRF52840 boards, an artifact was created with the action which will contain the uf2 file you can upload to your nRF52840 board.
