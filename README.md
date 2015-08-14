# lsdsk
Search for Categories or Exec in *.desktop files. 
Without any command line will be listed all available content in "Categories" and "Exec", 
if "Categories" doesn't exist then will be used content of "Name".

Examples:

# lsdsk

# lsdsk gtk

To find all existing and available path to *.desktop files on your computer you can use


find / -type f -iname "*.desktop" | awk '{A=$0;gsub(/[^*]*\//,"",A);print substr($0,0,index($0,A)-1)}' | uniq
