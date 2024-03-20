# Cisco SPACES

![alt text](https://github.com/START-Hack/Cisco_STARTHACK24/blob/main/banner.png)

## What is Cisco Spaces:

Turn Your Buildings into Smart SPACES, a cloud platform that connects people and  things with spaces with no additional hardware and drives efficiency and cost optimizations.

[Watch the video](https://video.cisco.com/detail/video/6023969831001)

For more information, visit [https://spaces.cisco.com/]().

## Case Introduction:

Cisco SPACES offers location-based data of devices, things, people and can help to create several use cases. If you combine this data with business relevant data, there are unlimited possibilities. The current use cases are often related to guide people around. We need new ideas on what service to offer with the data we have. We also struggle with the integration of the data into applications or “user friendly” interfaces. To get an idea of the existing use-cases you can browse through the [Outcome Store](https://spaces.cisco.com/store/outcomes/).

Prototype of a use case to solve a need using the Cisco SPACES API’s and data from a business application. (i.e. find my colleague at Start Global, would use calculated coordinates of the client, lookup the registration data from the event and show me where my friend is). Moreover, participants are encouraged to explore the integration of AI/ML technologies to drive innovation and creativity in their proposed use cases.

The Target users of this solution are global companies and can include possibly every Cisco WLAN customer.

- End-users is its location-based services for them
- Real estate if it is floor heat maps
- IT/OT if it’s asset tracking

## Deep Dive Slides:

[Deep Dive Slides](Cisco_StartHack24.pdf)

## Further Information:

![alt text](https://www.cisco.com/c/dam/en/us/products/collateral/wireless/dna-spaces/datasheet-c78-741786.docx/_jcr_content/renditions/datasheet-c78-741786_0.png)

At a high level, the data comes in from different network components (Cisco wireless LAN Controllers and Access Points, Catalyst switches, Webex devices, Meraki networks) and is fed into the Cisco SPACES cloud platform where it will be processed and consumed by different applications. For example, in case of Access Points, we can track the location end users that are connected to those Access Points. In addition, IoT data can also be leveraged coming from IoT Gateways residing on Cisco Access Points or Switches. Through APIs, this data can be accessed to develop innovative solutions, leveraging real-time information for various use-cases.

## Cisco Spaces APIs:

Cisco SPACES offers two primary APIs: REST APIs and the Firehose API, both documented in the [Cisco SPACES API Guide](https://www.cisco.com/c/dam/en/us/td/docs/wireless/cisco-dna-spaces/partner-app/partner-firehose-api/Cisco_DNA_Spaces_API_Guide.pdf), [Cisco Spaces API Documentation](https://partners.dnaspaces.eu/docs/v1/basic/index.html#!c-dnas-partners-overview.html) and [Cisco DNA Spces Partner Firehose API Events For Standard Partners](https://www.cisco.com/c/en/us/td/docs/wireless/cisco-dna-spaces/partner-app/partner-firehose-api/std.html).

- **Firehose API**: This provides a continuous stream of real-time data from Cisco SPACES. It is advantageous for applications requiring up-to-the-minute information and a broader, continuous flow of data.
- **REST APIs**: In addition to the Firehose API, Cisco SPACES continues to also have some areas where REST APIs can be used. These APIs allow for specific, targeted data retrieval.

Participants are encouraged to explore the Firehose API for their use case as it offers more flexibility. To gain insight into utilizing the Firehose API, participants can have a look the [index.py](index.py) code example. Each participating group receives an API token, which is requested when the app is executed. The script then opens an http session and iterates through each incoming event. To track the event stream, it writes every event to the [logs.json](logs.json) in readible format.

## Data:


The data provided is simulated data covering two different scenarios: Workspace and Retail. Based on the use case, the data can be filtered for the respective scenario:

```python
if event["partnerTenantId"] == "Simulation-Retail":
# To use the Retail Scenario 

elif event["partnerTenantId"] == "Simulation-Workspaces":
# To use the Workspace Scenario 

```
On the Firehose API, data related to multiple technologies are sent on a single stream. It is recommended to choose only desired events so that you can limit the amount of data streamed for your application. In the API documention the different [Event Types](https://partners.dnaspaces.eu/docs/v1/basic/index.html#!c-supported-events.html) are listed. 

## Judging Criteria:

- Complexity & Technical sophistication: Usage of Cisco SPACES API’s, SDK and Cisco technologies (10%)
- Design: Usability of the solution (10%)
- Viability: Possibility of realizing the solution and integrate it into Cisco SPACES or have it available in the Cisco Marketplace (20%)
- Feasibility: Maturity level of developed solution, does the prototype work? (20%)
- Creativity & Innovation: Surprise and innovative ideas that has effect to the jury (20%)
- Presentation: Sell the use case and show the prototype, communication of the developed solution (20%)

## Point of Contact:

Join our [Webex Space](https://eurl.io/#W5utnhKwO) to get in touch with us directly if you have any questions. Please note that by joining our Webex Space, your full name and email will be visible to other participants. 
If you don't have a webex account, please sign up for a [FREE Webex account](https://signup.webex.com/sign-up).

- Stefan Leemann, Head of Networking Experiences Cisco Switzerland
- Anna Summerauer, Solution Engineer Wireless Cisco Switzerland
- Tina Lang, Solution Engineer Switching Cisco Switzerland
- Simon Light, Solutions Engineer Wireless Cisco UK (remote)

## Prize - the winning team members will each receive:

- B&O Cisco 950 True Wireless In-Ear. USB-A Cable – Black
- Cisco Goody Bag
- Meeting&Lunch with Cisco to present the Use-Case

<img src="https://www.cisco.com/c/dam/en/us/products/collateral/collaboration-endpoints/headsets/bang-olufsen-950-ds.docx/_jcr_content/renditions/bang-olufsen-950-ds_0.jpg" width="500" />
