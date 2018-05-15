# AndroidDirectBoot

Bu basit bir alarm uygulamasıdır.Cihazınızda alarm kurulduktan sonra boot ekranını kapatana kadar alarm çalmaya devam etmektedir.
Yani bildirim Boot ekranındaki şifreyi geçip bildirimi görüntüleyene kadar uyarı vermeye devam eder.

![alt text](https://github.com/harunkor/AndroidDirectBoot/blob/master/device-2018-05-15-160347.png?raw=true)


![alt text](https://github.com/harunkor/AndroidDirectBoot/blob/master/2.png?raw=true)

![alt text](https://github.com/harunkor/AndroidDirectBoot/blob/master/3.png?raw=true)

![alt text](https://github.com/harunkor/AndroidDirectBoot/blob/master/4.png?raw=true)




https://www.youtube.com/embed/fb2Zwmc3Sp4


Android 7.0 runs in a secure, Direct Boot mode when the device has been powered on but the user has not unlocked the device. To support this, the system provides two storage locations for data:

Credential encrypted storage, which is the default storage location and only available after the user has unlocked the device.
Device encrypted storage, which is a storage location available both during Direct Boot mode and after the user has unlocked the device.
By default, apps do not run during Direct Boot mode. If your app needs to take action during Direct Boot mode, you can register app components that should be run during this mode. Some common use cases for apps needing to run during Direct Boot mode include:

Apps that have scheduled notifications, such as alarm clock apps.
Apps that provide important user notifications, like SMS apps.
Apps that provide accessibility services, like Talkback.
If your app needs to access data while running in Direct Boot mode, use device encrypted storage. Device encrypted storage contains data encrypted with a key that is only available after a device has performed a successful verified boot.

For data that should be encrypted with a key associated with user credentials, such as a PIN or password, use credential encrypted storage. Credential encrypted storage is only available after the user has successfully unlocked the device, up until when the user restarts the device again. If the user enables the lock screen after unlocking the device, this doesn't lock credential encrypted storage.
