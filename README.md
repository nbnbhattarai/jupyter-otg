
<div align="center">
  <p>
	  <img src="https://github.com/nbnbhattarai/jupyter-otg/raw/master/jupyter.png" />
  </p>
</div>

# Jupyter Notebook On the Go

Running jupyter server in the background and opening ipynb or other files directly in browser with jupyter notebook.


## Installation  

1. jupyter.service file

   - Modify this file to include the username
 
    - Change the location of anaconda if required or provide the path to jupyter notebook
   - Copy this file to /etc/systemd/system directory
   
2. jupyter_launcher.sh file

   - This file is used to launch the default browser with the file location provided through the desktop file. Place it anywhere you like.
  
3. jupyter.desktop file

   - This file is the launcher which will execute the jupyter_launcher.sh with file path as argument.
   - You can place it in either in /usr/share/applications or /usr/local/share/applications or ~/.local/share/applications.
  
   - Provide the jupyter_launcher.sh file's absolute path.
  
4. jupyter.png file

   - Icon file for jupyter.desktop launcher. Provide this file's absolute path in jupyter.desktop file.

## Usage

- Start the jupyter service by
`sudo systemctl start jupyter`
- To check the logs of jupyter server
`sudo journalctl -u jupyter`
- Set the jupyter launcher as default to your .ipynb files
