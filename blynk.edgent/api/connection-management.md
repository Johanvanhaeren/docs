# Connection Management

There are several functions to help with connection management:

## Blynk.connect\(\)

This functions will continue trying to connect to Blynk server. Returns `true` when connected, `false` if timeout have been reached. Default timeout is 30 seconds.

```cpp
bool result = Blynk.connect();
bool result = Blynk.connect(timeout);
```

## Blynk.disconnect\(\)

Disconnects hardware from Blynk server:

```cpp
Blynk.disconnect();
```

## Blynk.connected\(\)

Returns `true` when hardware is connected to Blynk Server, `false` if there is no active connection to Blynk server.

```cpp
bool result = Blynk.connected();
```

## Blynk.run\(\)

This function should be called frequently to process incoming commands and perform housekeeping of Blynk connection. It is usually called in `void loop() {}`.

This command can be initiated it in other places of your code unless you run out of heap memory \(in the cascaded functions with local memory\).

For example, it is not recommended to call `Blynk.run()` inside of the `BLYNK_READ` and `BLYNK_WRITE` functions on low-RAM devices.

## BLYNK\_CONNECTED\(\)

Use this function when you need to run certain routine when hardware connects to Blynk Cloud or private server. It's common to call sync functions inside of this function.

```cpp
BLYNK_CONNECTED() {
// Your code here
}
```

## BLYNK\_APP\_CONNECTED\(\)

This function is called every time Blynk app client connects to Blynk server.

```cpp
BLYNK_APP_CONNECTED() {
// Your code goes here
}
```

[Example](https://github.com/blynkkk/blynk-library/blob/master/examples/More/AppConnectedEvents/AppConnectedEvents.ino)

## BLYNK\_APP\_DISCONNECTED\(\)

This function is called every time the Blynk app disconnects from Blynk Cloud or private server.

```cpp
BLYNK_APP_DISCONNECTED() {
// Your code here
}
```

[Example](https://github.com/blynkkk/blynk-library/blob/master/examples/More/AppConnectedEvents/AppConnectedEvents.ino)

