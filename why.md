Retrofit:



1. I want to know the difference between Call And Response ? That when to use Call & when to use to Response in Retrofit ?
      ```
      @GET("/albums/{id}")
      suspend fun functionOne(@Path(value = "id") albumsId:Int):Response<Albums>
      @GET("/albums/{id}")
      suspend fun functionTwo(@Path(value = "id") albumsId:Int):Call<Albums>
      ```
      These both functions works fine for me, both have different implementations but have almost same purposes.

      1. What way of response type is good for best practices ?
      2. When to use Response & Call ?

      [Ans](https://stackoverflow.com/questions/64124670/call-or-response-in-retrofit):
      I think it is depends on your use-case. By using `retrofit2.Response<T>`, we can access `errorBody()`(The raw response body of an unsuccessful response.), `code()`(HTTP status code.) or `headers()`(HTTP headers).

      ["Call"](https://square.github.io/retrofit/2.x/retrofit/retrofit2/Call.html) is useful when we are willing to use its enqueue callback function.
      ["Response"](https://square.github.io/retrofit/2.x/retrofit/retrofit2/Response.html) When we use Coroutines or RxJava in the project(which is the best professional practice) to provide asynchronous execution , we don't need enqueue callback. We could just use Response.
      Call<T> is a container that "sends a request to a webserver and returns a response".
        Response is a container that delivers a result back to you, either from calling 
        enqueue(Callback<T> callback) (asynchronously) and implementing Callback<T> 
        or by calling execute() (synchronously). A Response can be either successful or a failure.
