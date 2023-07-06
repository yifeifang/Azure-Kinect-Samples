## Steps
1.  setup mqtt external connection (This is unsecure need fix later)  
```
    dewey@dewey-nuc:/etc/mosquitto/conf.d$ cat myconfig.conf 
    allow_anonymous true
    listener 1883
```
2.  Boot up container using `docker compose run ubuntu18.04-build`
3.  Boot up capture app using `./kinect_capture.out`
4.  Boot up windows mqtt visualizer modify the toml file to point the ip to the mqtt broker
5.  run `mosquitto_pub -t 'merger' -m 'camera0 points/windowViewer'` to let the visualizer know what topics to look at