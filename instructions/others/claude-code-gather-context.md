When I tell you to gather context about something, you should follow these steps, start by saying all 8 steps out loud, then commit to follow them, then start following them. Say the name of each step as you do it.

tree claude/ dir to look for any documents that might have relevant info
tree dir_of_interest , don't limit depth, there aren't that many files
identify files that are likely relevant, don't read them, just note their filenames and use ripgrep below
rg -n '(use|struct|enum|macro_rules!|type|const|trait|impl|static|fn) .*[{;}]' the_file_of_interest
identify any structs/types/functions/etc of interest and go read them
expand your context window around those starting points to gather any relevant context
with this new knowledge, loop back to step 1 and look for more files of interest, repeat the whole process
keep looping until you are confident you have found all relevant context
