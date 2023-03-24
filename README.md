# Cisco MPP IP Phone Screen Visualizer

You can use these HTML templates to export in near-real-time the content of a Cisco IP Phone display (running the MPP firmware) and show it inside a high-res frame picture representing the same phone model, on your screen.  
This is typically used when you want to demo what is happening on the phone to an audience to whom you are projecting the screen of your computer.

![Sample Result](sample.png)

### Requirements

The setup has been tested with MPP firmware 11.3 and early versions of 12.0 as of March 2023.  
It is possible that future changes in the firmware could make this setup unusable.

1. The phones must not have password-restricted admin access (Note: all phones running on Webex Calling **are** password restricted);
2. You must have direct network connectivity to the phone's web interface.

#### Note

Phones do not allow for a refresh shorter than approximately 2 seconds. So keep in mind the display will necessarily exibit some lag between any action taken on the phone and the corresponding reflection on the screenshot.

### Instructions

1. Store the templates with the respective frame pictures in a folder on your web server;
1. Start serving the page templates from your web server of choice (also a local python http server will do just fine);
2. Open the URL destination of your page by adding the URL parameter “ip=nn.nn.nn.nn”, where nn.nn.nn.nn is the IP address of the IP Phone.

#### Example

`http://webserver/7821.html?ip=192.0.2.1`

Where 192.0.2.1 is the example IPv4 address of the phone (typically received from the DHCP).

#### Note

The phone might not serve the request if there is a Referer header in it. To work around this I originally changed the `network.http.sendRefererHeader` flag in Firefox (or any equivalent mechanism in Chromium), but this is not necessary anymore thanks to an improvement in the template related to [referrer policies](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Referrer-Policy#integration_with_html) in HTML.

### About the Phone Images

Phone images are sourced from [Cisco Brand Exchange Public Collection](https://brandfolder.com/cisco-brand-exchange/public) and as such are here “Courtesy of Cisco Systems, Inc. Unauthorized use not permitted.”. The full license is available in Cisco-bx-license.txt inside this repository.
