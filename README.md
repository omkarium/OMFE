# OMFE.exe
This is a file encryption and decryption tool. Unlike any other file encryption tool, this software retains the folder structure of the folder path you want to Encrypt/Decrypt. It uses the safest AES GCM encryption and provides you a GUI to easily operate.

## How to use the tool

`Step 1`. Download the OMFE.exe file and run it. If the exe gives you a Java Runtime Environment required error even while you have JDK, then probably you are using openjdk. In such case please use omfe.jar file and run it.

`Step 2`. Prepare a /decrypt folder manually in any path of your system. You need to places your files or folders into this path-to/decrypt/.

`Step 3`. Click on "Choose Folder" in the GUI and choose the path-to/decrypt/. In the display area (white), a message will print telling how many files are present in the path-to/decrypt/. The number of files includes all the files in all sub-folders too.

`Step 4`. Type a strong password (16 characters is preferred) and press on "Encrypt" button. This will start the Encryption process and the same will also be indicated using a Progress bar in the bottom.

`Step 5`. All the encrypted files will now appear in the same root location/path of /decrypt, but inside the folder /encrypt. All files will have ".enc" extension.

If you wish to decrypt, then operate on newly created '/encrypt' by choosing the folder and follow the same process as above. You can find the decrypted files in '/decrypt' folder with ".enc" extension removed.

## Internal process & Precautions: 

The tool is written in java and it utilizes the concept of multithreading. I have allowed only 30 threads to run actively so as to keep the cpu usage and memory in safe limits. 

Make sure that your folder size is not beyond 500MB of disk size. For Example, going beyond 800MB of folder size will hang the machine severly if your machine RAM is just 6GB. If you have higher RAM, you can experiment on a dummy folder by arbitrarily increasing its size and test encrypting it.

## Test results

I successful encrypted 700MB of folder size (aggressively) and maxed out the CPU load.
Memory usage: 731MB used by open-jdk process.
Max disk read/write rate: 3.1 MB/s.

CheckSum (SHA256) of OMFE.exe => 876c008a2b5fb9bb43dc51044e8aab8b1366a16696f1ae463c7bf5609fb8052f
CheckSum (SHA256) of omfe.jar => dc6e447c6bf177466ac2defde241a79429724dca2badef9522358cedca7c620e

[Here are the source files](https://github.com/leogitpub/omfe-sources)

Follow me if you liked it.
