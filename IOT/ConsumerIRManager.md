# ConsumerIrManager

Added in[API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)  
Summary:[Nested Classes](https://developer.android.com/reference/android/hardware/ConsumerIrManager#nestedclasses)\|[Methods](https://developer.android.com/reference/android/hardware/ConsumerIrManager#pubmethods)\|[Inherited Methods](https://developer.android.com/reference/android/hardware/ConsumerIrManager#inhmethods)  

# ConsumerIrManager

*** ** * ** ***

[Kotlin](https://developer.android.com/reference/kotlin/android/hardware/ConsumerIrManager "View this page in Kotlin")\|Java

`
public

final

class
ConsumerIrManager
`  
`

extends `[Object](https://developer.android.com/reference/java/lang/Object)`


``


`

|---|------------------------------------|
| [java.lang.Object](https://developer.android.com/reference/java/lang/Object) ||
| ↳ | android.hardware.ConsumerIrManager |

<br />

*** ** * ** ***

Class that operates consumer infrared on the device.  
Requires the[PackageManager#FEATURE_CONSUMER_IR](https://developer.android.com/reference/android/content/pm/PackageManager#FEATURE_CONSUMER_IR)feature which can be detected using[PackageManager.hasSystemFeature(String)](https://developer.android.com/reference/android/content/pm/PackageManager#hasSystemFeature(java.lang.String)).

## Summary

|                                                                                                                     ### Nested classes                                                                                                                     ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ` class` | [ConsumerIrManager.CarrierFrequencyRange](https://developer.android.com/reference/android/hardware/ConsumerIrManager.CarrierFrequencyRange) Represents a range of carrier frequencies (inclusive) on which the infrared transmitter can transmit |

|                                                                                                                                                                                         ### Public methods                                                                                                                                                                                          ||
|--------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ` `[CarrierFrequencyRange[]](https://developer.android.com/reference/android/hardware/ConsumerIrManager.CarrierFrequencyRange) | ` `[getCarrierFrequencies](https://developer.android.com/reference/android/hardware/ConsumerIrManager#getCarrierFrequencies())`() ` Query the infrared transmitter's supported carrier frequencies                                                                  |
| ` boolean`                                                                                                                     | ` `[hasIrEmitter](https://developer.android.com/reference/android/hardware/ConsumerIrManager#hasIrEmitter())`() ` Check whether the device has an infrared emitter.                                                                                                 |
| ` void`                                                                                                                        | ` `[transmit](https://developer.android.com/reference/android/hardware/ConsumerIrManager#transmit(int,%20int[]))`(int carrierFrequency, int[] pattern) ` Transmit an infrared pattern This method is synchronous; when it returns the pattern has been transmitted. |

| ### Inherited methods |
|-----------------------|---|
| From class` `[java.lang.Object](https://developer.android.com/reference/java/lang/Object)` ` |--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | ` `[Object](https://developer.android.com/reference/java/lang/Object)          | ` `[clone](https://developer.android.com/reference/java/lang/Object#clone())`() ` Creates and returns a copy of this object.                                                                                                                                                      | | ` boolean`                                                                     | ` `[equals](https://developer.android.com/reference/java/lang/Object#equals(java.lang.Object))`(`[Object](https://developer.android.com/reference/java/lang/Object)` obj) ` Indicates whether some other object is "equal to" this one.                                           | | ` void`                                                                        | ` `[finalize](https://developer.android.com/reference/java/lang/Object#finalize())`() ` Called by the garbage collector on an object when garbage collection determines that there are no more references to the object.                                                          | | ` final `[Class](https://developer.android.com/reference/java/lang/Class)`<?>` | ` `[getClass](https://developer.android.com/reference/java/lang/Object#getClass())`() ` Returns the runtime class of this`Object`.                                                                                                                                                | | ` int`                                                                         | ` `[hashCode](https://developer.android.com/reference/java/lang/Object#hashCode())`() ` Returns a hash code value for the object.                                                                                                                                                 | | ` final void`                                                                  | ` `[notify](https://developer.android.com/reference/java/lang/Object#notify())`() ` Wakes up a single thread that is waiting on this object's monitor.                                                                                                                            | | ` final void`                                                                  | ` `[notifyAll](https://developer.android.com/reference/java/lang/Object#notifyAll())`() ` Wakes up all threads that are waiting on this object's monitor.                                                                                                                         | | ` `[String](https://developer.android.com/reference/java/lang/String)          | ` `[toString](https://developer.android.com/reference/java/lang/Object#toString())`() ` Returns a string representation of the object.                                                                                                                                            | | ` final void`                                                                  | ` `[wait](https://developer.android.com/reference/java/lang/Object#wait(long,%20int))`(long timeoutMillis, int nanos) ` Causes the current thread to wait until it is awakened, typically by being*notified* or*interrupted*, or until a certain amount of real time has elapsed. | | ` final void`                                                                  | ` `[wait](https://developer.android.com/reference/java/lang/Object#wait(long))`(long timeoutMillis) ` Causes the current thread to wait until it is awakened, typically by being*notified* or*interrupted*, or until a certain amount of real time has elapsed.                   | | ` final void`                                                                  | ` `[wait](https://developer.android.com/reference/java/lang/Object#wait())`() ` Causes the current thread to wait until it is awakened, typically by being*notified* or*interrupted*.                                                                                             | ||

## Public methods

### getCarrierFrequencies

Added in[API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)  

```
public CarrierFrequencyRange[] getCarrierFrequencies ()
```

Query the infrared transmitter's supported carrier frequencies

<br />

|                                                                                                                                                                                                                Returns                                                                                                                                                                                                                ||
|-----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CarrierFrequencyRange[]](https://developer.android.com/reference/android/hardware/ConsumerIrManager.CarrierFrequencyRange) | an array of[ConsumerIrManager.CarrierFrequencyRange](https://developer.android.com/reference/android/hardware/ConsumerIrManager.CarrierFrequencyRange)objects representing the ranges that the transmitter can support, or null if there was an error communicating with the Consumer IR Service. <br /> |

### hasIrEmitter

Added in[API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)  

```
public boolean hasIrEmitter ()
```

Check whether the device has an infrared emitter.

<br />

|                                  Returns                                  ||
|-----------|----------------------------------------------------------------|
| `boolean` | true if the device has an infrared emitter, else false. <br /> |

### transmit

Added in[API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)  

```
public void transmit (int carrierFrequency, 
                int[] pattern)
```

Transmit an infrared pattern

This method is synchronous; when it returns the pattern has been transmitted. Only patterns shorter than 2 seconds will be transmitted.

<br />

<br />

|                                          Parameters                                           ||
|--------------------|---------------------------------------------------------------------------|
| `carrierFrequency` | `int`: The IR carrier frequency in Hertz. <br />                          |
| `pattern`          | `int`: The alternating on/off pattern in microseconds to transmit. <br /> |