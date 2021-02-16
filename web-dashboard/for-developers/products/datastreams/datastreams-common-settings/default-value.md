# Default Value

![](../../../../../.gitbook/assets/default-value.png)

Default value is a Datastream property that allows you to set the initial value for the data stream. Those value later could be used by hardware, via HTTPS API or by Rule Engine. It is most useful on the first device connection to the server.

Let's consider the next use case - You have a light bulb and right after the first device connection  
to the server you want it to be turned on. For that you need to set the default value for the Data Stream, let's say on pin `V1` to `1`. And you'll need the next code on the hardware:

```text
BLYNK_CONNECTED() {
  Blynk.sync(V1);
}

BLYNK_WRITE(V1)
{
    int bulbValue = param.asInt(); // here you get default value 1
    handle(bulbValue);
}
```

The beauty of this method is that you can change the default value of the product at any time, even hardware was already shipped to your clients, without need in OTA.

