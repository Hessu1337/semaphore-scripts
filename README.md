# Semaphore Scripts

This repository contains scripts that can be used on Semaphore to extend the functionality and customize the build and deploy environment.

## Usage

Each script has a short description at the beginning, showing how to use it in your project. It is in form of comments and this section also lists any requirements or expected environment variables, as well as supported Semaphore platforms.

For example:

```bash
####
# Description: Installs specified Ruby version and cache its installation on Semaphore
#
# Runs on: all Semaphore platforms
#
# Usage:
# Add the following command to the setup of a build in the Project Settings
#
#    wget https://raw.githubusercontent.com/renderedtext/semaphore-scripts/master/ruby_setup.sh && bash ruby_setup.sh <ruby-version>
#
# For example, the following command will install Ruby 2.5.1
# and cache its installation on Semaphore
#
#    wget https://raw.githubusercontent.com/renderedtext/semaphore-scripts/master/ruby_setup.sh && bash ruby_setup.sh 2.5.1
#
# Note: reset your dependency cache in Project Settings > Admin, before running this script
####
```

## Contributing

Feel free to contribute by adding new scripts, improving the existing ones, or by giving your comments and suggestions.

There are no strict rules on how to write the scripts, however, some basic guidelines should be followed:

* Add description which provides all the data needed for successfully running the script (requirements, any environment variables, starting command example, etc). Preferrably, use the template as provided in **Usage** paragraph above.

* Scripts should use [environment variables available on SemaphoreCI](https://semaphoreci.com/docs/available-environment-variables.html) when possible.

* Installations should utilize caching when possible, which speeds up subsequent runs of the installation scripts.
