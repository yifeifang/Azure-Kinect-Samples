.PHONY: kinect_capture
kinect_capture:
	$(MAKE) -f ./kinect_capture/Makefile all

.PHONY: merger

.PHONY: mqtt_visualizer

.PHONY: setup 
setup:
	mkdir -p build/kinect_capture
	mkdir -p build/merger
	mkdir -p build/mqtt_visualizer

.PHONY: build 
build: setup kinect_capture merger mqtt_visualizer

.PHONY: clean 
clean:
	rm -rf build
