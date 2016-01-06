1. Download PuTTY for windows: http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html
2. Run the installer (should install things well)
3. Run PuTTYgen to make an SSH key
4. Save private key as id_rsa.ppk (recommended name)
5. Record public SSH key as whatever, just need to have it for later.

To Set Up PuTTY with your Digital Ocean droplet:
1. Set Host name to the IP of the droplet (162.243.164.162 for now, don't know if it will change) with port 22 (default)
2. Under connection -> data set auto-login username to "root"
3. Under connection -> SSH -> auth locate your id_rsa.ppk file (or whatever you named it) and set the path in "private key for authentification"
4. Save the profile as a friendly name (mine is NYC-01)
5. Ask Justin to add your key to the "authorized_keys" file in the droplet

That's it! It should work from here.

If not, try to add your public SSH key to the digital ocean account, probably not necessary, but it might make it work.
Make sure that the key is added to the authorized_keys file and not any other file (ahem, Justin).
