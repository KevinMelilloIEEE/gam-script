This is a set of GAM scripts that we use for our environment over at the IEEE.
Once Google Apps Manager is set up and running, these scripts handle some basic 
automation we have based on IEEE needs.

nGroup.* - creates group(s) from an input file
 assigns manager to the group
 sets a few group specific settings

nUser.* - provisions a user from an input file
 puts the user in the proper ORG
 assigns the user to a group based on department
 assigns a Vault license to that user

termUser.* - process a user for termination from an input file
 renames the user based on the date and time of the script run
 puts the user in a terminated ORG (for Vault Retention purposes)
 adds delegation to the manager
 sets the vacation message of the user
 revokes all keys, mobile devices, and oauth codes
 randomizes the password
