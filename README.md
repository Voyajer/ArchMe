# ainstall
Personal arch install script.

Pull this from the arch iso live environment with:
wget https://github.com/Voyajer/ainstall/archive/master.zip

Then unzip with something like:
7z x master.zip

After extraction, cd into the folder created and run:
chmod +x ainstall aconfig

Now you can execute ainstall by typing:
./ainstall

# Connecting to the internet over wifi

First figure out what your wifi device is named:

ip addr

Then run this command:

wpa_supplicant -B -i [your device] -c <(wpa_passphrase "[ssid]" "[password]")

Leave the quotation marks around the SSID and pass.

Then run:

dhcpcd [your device]
