# razor-vshpere-hooks
This repo store the hooks used by a chat-ops workflow developed by EMC PacNW SEs.

Ensure that Ruby 1.9.3 is installed on the razor-server then run `gem install rest-client`. This allows the razor-server to interact with REST apis.

## Adding the hook templates

Razor-server stores hook by default in /opt/razor/hooks for Ubuntu 14.04.

Either copy or symlink each .hook directory to your razor-server store location, as determined above. You should already see an example or two that puppet labs ships with razor.

## Creating the hooks
The commands to create the hooks are as follows:
- ####nodeAnnounce
`razor create-hook --name <some_name> --hook-type nodeAnnounce --configuration node-type=<physical|virtual>`

- ####nodeBootAnnounce
`razor create-hook --name <some_name> --hook-type nodeBootAnnounce`

- ####getMachineName
`razor create-hook --name <some_name> --hook-type nodeBootAnnounce --configuration policy=<policy_name>`
