.PHONY kinect_capture:
	$(MAKE) -f ./kinect_capture/Makefile all
.PHONY merger:
.PHONY mqtt_visualizer:
.PHONY setup:
	mkdir -p build/kinect_capture
	mkdir -p build/merger
	mkdir -p build/mqtt_visualizer
.PHONY build: setup kinect_capture merger mqtt_visualizer
.PHONY clean:
	rm -rf build
