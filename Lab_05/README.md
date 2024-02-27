# Lab 5

I first started off by pulling the latest version of the iot repo.

![Pulling the iot repo](pull_iot_repo.png)

I then went ahead and installed Paho-MQTT.

![Installing Paho-MQTT](installs.png)

When I first ran the programs, I revieced this error saying it was missing an argument for the api version in the `mqtt.Client()` function call.

![Error](error.png)

Luckily after a few minutes of looking online, I found that the source of the issue is a recent (early Febuary 2024) update to Paho-MQTT. I found the [migrations page](https://github.com/eclipse/paho.mqtt.python/blob/v2.0.0/docs/migrations.rst) which said to simply add `mqtt.CallbackAPIVersion.VERSION1` as the first argument in the `Client()` call. And finally...

## Output

![Output Image](output.png)
