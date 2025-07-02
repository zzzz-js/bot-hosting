# Upload / Unarchive Errors

* If you get an error while uploading your files or with the unarchive function, it is most because they have a size higher than 100MB or because of the file format. Possible fixes:
* If you are using Node.js, you can remove the `package-lock.json` file, the `.npm` and the `node_modules` folders and keep `package.json`, the package file will guide the server to install modules in it
* If you are using python, remove the `.cache` folder or any folder/file that cointains modules you want to install in the server and keep the `requirements.txt` file in the server, the requirements file will guide the server to install modules in it

{% hint style="info" %}
**If you are using .rar archives, please migrate to .zip or .tar.gz as .rar generates issues while unarchiving sometimes**
{% endhint %}

Read the SFTP Guide [here](../guides/connecting-to-your-servers-files-with-sftp.md).
