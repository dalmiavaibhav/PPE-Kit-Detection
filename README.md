# PPE-KIT Detection

# Complete Product-System Design Setup for Real-time Person with PPE-Kit Detection

## CostVsAccuracyVsPerformanceVsTime

## New developments-Alwaysai-demo-L&T

- Custom Client/Front end with alwaysai and extra add-ons for alert
    - [ ]  Custom streamer
    - [ ]  Sound alert javascript
    - Mail service smtp
    - Text service twilio
    - Logs + triggered media strorage
- Multiple models integration
    - [x]  Person - yolo_v4_416_tiny_nano
    - Helmet + Vest
        - Accuracy improvement with ppe detection
            - [ ]  Retrain on Another dataset- person, head, helmet
- Performance improvement

### Issues/Errors

- resizing on shoes dataset-
    - Error: Error: marker was not found
    - $ aai dataset resize --target-dir zipped_cleaned_cut2_.zip --output-dir resized300x300.zip
    info: Resizing images and annotations.
- Resizing on helmet dataset
    - Error: Error: EMFILE: too many open files, open 'extractedDir/JPEGImages/hard_hat_workers4665.jpg'
    - $ aai dataset resize --target-dir zipped.zip --output-dir zipped_resized_helmet.zip
- Training
    - faster_rcnn retraining error

## Software-Setup

- [ ]  network connection startup script vs all-time background script wlan0
- [ ]  Send IP on every boot/new connection script
- [x]  Manual
    - [x]  Mobile Hotspot
    - [ ]  LAN/WLAN
- [ ]  App Startup script
- [x]  Live detection alerts
    - [x]  Visual
    - [ ]  Audio?
- [x]  IP Spit-out
    - [x]  Front end app web address
- [x]  ssh tunneling check for
    - [x]  Wifi Telecom
- [ ]  Auto fan turn on script
- [ ]  Alert Texting/Email
- [ ]  Logs, Video, Image writer( serve the logs)

## WIFI Connection script

- [ ]  search for the available networks
- [ ]  select and connect to the required network
- [ ]  login (iiti) curl -d "auth_user=me170003058&auth_pass=VAIBHAV799912&accept=Sign In" [http://10.100.100.253:8002/index.php?zone=iiti_auth](http://10.100.100.253:8002/index.php?zone=iiti_auth)
- [ ]  make it a startup or background service

## Insights

### Performance concerns

- System based-
    - CPU, GPU, RAM, DISK etc.
- Networking based
    - Low latency connections
- Development Based
    - Optimized environments