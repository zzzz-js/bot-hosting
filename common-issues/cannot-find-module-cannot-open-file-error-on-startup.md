# Cannot find module / Cannot open file error on startup

This usually means you have forgotten to do one of two things:

1. You haven't set your main file in the startup tab, your main file is the file that is used to start your bot (in Node the file that you run with `node <your file>` and for Python `py <your file>.` Remember that if you unarchived your files in to a folder, you may need to move them out of that folder.



1. Your modules haven't installed. For node.js this usually means you've forgotten to upload your `package.json` and `package-lock.json` files in the home directory (`/home/container`) or you are getting an error upon your modules install which you should look for. For Python this usually means you haven't uploaded a `requirements.txt` file with each dependency on a new line (or you can specify your requirements in the startup tab under `Additional Dependencies` with a space between each one).
