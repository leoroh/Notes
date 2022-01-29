1. Common errors in android
  i. java.lang.RuntimeException: Unable to start activity ComponentInfo{com.example.nttmeeting/com.example.nttmeeting.MainActivity}: 
  android.os.NetworkOnMainThreadException doing retrofit `service.getData().execute()` call in main thread
  
  2. Diffrance between View Binding and Data Biding
        View binding and data binding both generate binding classes that you can use to reference views directly. However, view binding is intended to handle simpler use cases and provides the following benefits over data binding:
        Faster compilation: View binding requires no annotation processing, so compile times are faster.
        Ease of use: View binding does not require specially-tagged XML layout files, so it is faster to adopt in your apps. Once you enable view binding in a module, it applies to all of that module's layouts automatically.
      Conversely, view binding has the following limitations compared to data binding:
        View binding doesn't support layout variables or layout expressions, so it can't be used to declare dynamic UI content straight from XML layout files.
        View binding doesn't support two-way data binding [link](https://developer.android.com/topic/libraries/view-binding#data-binding)
