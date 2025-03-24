# Step Guide to install and Run gruntJS

Steps to add this validation in Dotstore Plugins:
1. Clone this repo to your PC
2. Copy all files from that folder to your plugin folder
3. Make changes in the Gruntfile.js file as per below:
   1. Change the `ZIP_FILE_NAME` variable with the plugin slug
   2. Prepare the `TEXT_DOMAIN` array (if more than one text_domain is used in the plugin) with the plugin slug
   3. Add plugin main root file name with extension to `PLUGIN_MAIN_FILE` variable
   4. Add a pot file name to the `POT_FILE_NAME` variable (This name will be used when grunt prepares the POT file)
4. Open the command line and run the below commands:

| Command | Description |
| :---: | :--- |
| `composer install` | Download and install packages to run GruntJS PHPCS and PHPStan modules |
| `npm install` | Download and install node packages to run GruntJS's validation module |
| `npm run prepare`  | Install a Husky library that can be used while committing changes to GIT. (Basically, run the grunt command with minimal things while committing.) |

### Now all set.! ###

## Note ##
If you face `The '"husky/pre-commit' hook, it was ignored because it's not set as executable.` type of warning, then run the below command to fix it. Thanks @bhavesh
> `chmod ug+x .husky/pre-commit`
