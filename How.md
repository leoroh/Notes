1. How to show Toast / Snackbar in activity and what is [diff](https://stackoverflow.com/questions/34432339/android-snackbar-vs-toast-usage-and-difference) 

  ```
    Toast.makeText(this@MainActivity, "Data Received", Toast.LENGTH_SHORT).show()
    Snackbar.make(findViewById(android.R.id.content), "This is Simple Snackbar", Snackbar.LENGTH_SHORT).show()
  
  ```
