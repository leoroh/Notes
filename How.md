1. How to show Toast / Snackbar in activity and what is [diff](https://stackoverflow.com/questions/34432339/android-snackbar-vs-toast-usage-and-difference) 

  ```
    Toast.makeText(this@MainActivity, "Data Received", Toast.LENGTH_SHORT).show()
    Snackbar.make(findViewById(android.R.id.content), "This is Simple Snackbar", Snackbar.LENGTH_SHORT).show()
  
  ```
2. How to crack system design [Interview](https://github.com/weeeBox/mobile-system-design)

3. Set charles on android emulator
   ```
       #!/bin/sh
       # This script will set up Charles Proxy on an Android emulator.
       # Get the computer's IP address.
         COMPUTER_IP=$(ifconfig | grep inet\ | grep -vE "10.188|127.0.0.1"| awk '{ print $2 }')
       # Get the ID of the Android device.
        DEVICE_ID=$(adb devices | sed '1,1d' | sed '$d' | cut -f 1 | sort | head -n 1)
       # Set the proxy setting for the Android device.
        adb -s ${DEVICE_ID} shell settings put global http_proxy ${COMPUTER_IP}:8888
       # Print a message to the user.
        echo "http_proxy set to ${COMPUTER_IP}:8888"
   ```
