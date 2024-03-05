# Disclaimer

Although the scenario is inspired by real-world events, the scenario is 
fictional. It was created for demonstration purposes only, without any 
knowledge of the actual conference organization.

# Scenario: Travel to KubeCon + CloudNativeCon

This demo scenario is motivated by the booking experience of a user who wants to
travel to KubeCon + CloudNativeCon. The user wants to book a flight, hotel, and
conference ticket. Hotels, airlines, and other travel services often offer 
discounts for conference participants. 

## Systems and Involved Parties

### Conference Organizer (CO)

The conference organizer initiates and manages the conference. It is usually 
not a single person but an organization like a foundation or a company. 
Often, the organizer organizes multiple conferences, e.g. for different 
topics or regions.

### Conference Management Provider (CMP)

The Conference Management Service is a service provider that offers a 
platform for conference organizers to manage their conferences. The focus of 
this scenario is on supporting attendees in booking their travel to the 
conferences, but conference management providers may offer a wide range of 
services.
For this scenario, it is important that there are several conference 
management providers the conference organizers can choose from. 

### Booking Platform (BP)

Booking platforms offer a wide range of travel services supporting 
travellers in booking their trips. 

### Travel Service Providers (TSPs)

Travel service providers offer services like flights, hotels, or train rides.
When learn about a conference, they decide if they want to offer discounts 
to participants of a conference. 

## Event Flow

![Overview](overview.png)

### Conference Management Provider
    
* Announcements/Cancellation of conferences
* Update Conference -> Service providers 
  * rooms needed / interested attendees
  * Sold conference tickets
    
### Service providers
* Number of discounts offered for a conference
* Number of discounts granted

## Entitlement of Users to Discounts

Users booking a conference ticket are entitled to discounts for travel 
services. When accessing their conference profile, they can use links to 
their booking platform or a service provider that carries a discount code. 
Booking platforms and service providers can verify the user's entitlement by 
calling the conference management provider's API to retrieve an OAuth token 
as a proof of eligibility.  
