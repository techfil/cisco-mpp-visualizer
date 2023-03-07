# Cisco MPP IP Phone Screen Visualizer

You can use these HTML templates to export in near-real-time the content of a Cisco IP Phone display (running the MPP firmware) and show it inside a high-res frame picture representing the same phone model, on your screen.  
This is typically used when you want to demo what is happening on the phone to an audience to whom you are projecting the screen of your computer.

![Sample Result](sample.png)

### Requirements

1. The phones must not have password-restricted admin access (Note: all phones running on Webex Calling **are** password restricted);
2. You must have direct network connectivity to the phone's web interface.

#### Notes

Phones do not allow for a refresh shorter than approximately 2 seconds. So keep in mind the display will necessarily exibit some lag between any action taken on the phone and the corresponding reflection on the screenshot.

### Instructions

1. Modify the html files by replacing every occurrence of the "PHONE-IP" string with the actual IP address of the MPP Phone in your network;
2. Serve the page from any web server.

### About the Phone Images

Phone images are sourced from [Cisco Brand Exchange Public Collection](https://brandfolder.com/cisco-brand-exchange/public) and as such are here “Courtesy of Cisco Systems, Inc. Unauthorized use not permitted.”. The full license is available in Cisco-bx-license.txt inside this repository.
