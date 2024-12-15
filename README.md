# Event Registration App

This app was developed as part of a team effort with the following contributors:
- Ayra Qutub *ayraqutub* (me)
- Ayesha Aamer *aaaamer1*
- Francis Garcia *fgarcia06*
- Aditi Padhi *aditipadhii*
- Akhil Sunil *llLucidll*

The app is coded in Java with Android Studio.

## Description:
We want a mobile application where people can sign up for events at community centres that are popular and fill up fast. We want to allow people with limitations such as work, disability, etc. to be able to sign up for these events fairly and not have to sit refreshing a webpage until they can get a chance at reserving a spot.

How? Lottery! If I am running swimming lessons for 20 kids, I will post my event or series of events and I will let everyone join the waiting list for a period of a week. After the week is up, I will ask the system to choose 20 kids to sign up. The system will then notify these kids (or their guardians), if they say no they don’t want swimming lessons, then the system will sample another child to sign up. I can monitor the progress and then get access to the final list of everyone who signs up. If perhaps someone cancels later I can cancel them in the app and a new applicant is drawn.

Lottery systems are great because you don’t have to first get a chance to go to an event, you just have to say you are interested and if you’re lucky you will be offered a chance. This gives people who need the time, the time to sign up properly without pressure. Accessibility!

## Features:
**Pooling System:**
- Organizers can draw from a waiting list of interested event attendees as selected participants.

**QR Code Scanning:**
- The app will generate a QR code when an event is created. This can be used on posters and promotional material.
- Entrants can scan QR promotional code to view details about the event and also join the waiting list

**Firebase Integration:**
- Utilizes Firebase for storing event and profile details, attendee lists, and real-time check-in status updates.

**Multi-User Interaction:**
- Distinguish between entrants, organizers, and admin with special roles and privileges granted to each actor.
- Users are identified by their device, using a unique device identifier, so that they don't have to use a username and password.

**Event Management:**
- Allows event organizers to create events and set details, upload and update event poster images, and to view and manage registrants.

**Profile Management:**
- Users can set and edit their profile information, like their name, email, phone number, etc.
- Users can upload a profile picture for a more personalized experience; if no image is uploaded, the profile picture will be deterministically generated from the profile name.

**Admin Responsibilities:**
- Users with an admin role are able to browse and remove events, profiles, facilities, and images that may violate app policy.

**Geolocation Verification:**
- Can use geolocation to verify where users are joining the waiting list from. This is the location provided by the device.
- Users are warned before they register for an event that requires geolocation.
- Organizers will be able to see these locations on a map for each of their created events.

**Notifications:**
- Event organizers can send notifications to entrants for their events who have been selected for or removed from an event.
- The entrants will then receive these as push notifications to their device. 
- Users can manage their notification preferences from their profile.

![image](https://github.com/user-attachments/assets/c7aaba19-00d5-44d7-a68e-ec97bcea925e)

### User Stories
The app implements the following user stories:

**Entrant:**

US 01.01.01 As an entrant, I want to join the waiting list for a specific event

US 01.01.02 As an entrant, I want to leave the waiting list for a specific event

US 01.02.01 As an entrant, I want to provide my personal information such as name, email and optional phone number in the app

US 01.02.02 As an entrant I want to update information such as name, email and contact information on my profile

US 01.03.01 As an entrant I want to upload a profile picture for a more personalized experience

US 01.03.02 As an entrant I want remove profile picture if need be

US 01.03.03 As an entrant I want my profile picture to be deterministically generated from my profile name if I haven't uploaded a profile image yet.

US 01.04.01 As an entrant I want to receive notification when chosen from the waiting list (when I "win" the lottery)

US 01.04.02 As an entrant I want to receive notification of not chosen on the app (when I "lose" the lottery)

US 01.04.03 As an entrant I want to opt out of receiving notifications from organizers and admin

US 01.05.01 As an entrant I want another chance to be chosen from the waiting list if a selected user declines an invitation to sign up

US 01.05.02 As an entrant I want to be able to accept the invitation to register/sign up when chosen to participate in an event

US 01.05.03 As an entrant I want to be able to decline an invitation when chosen to participate in an event

US 01.06.01 As an entrant I want to view event details within the app by scanning the promotional QR code

US 01.06.02 As an entrant I want to be able to be sign up for an event by scanning the QR code

US 01.07.01 As an entrant, I want to be identified by my device, so that I don't have to use a username and password

US 01.08.01 As an entrant, I want to be warned before joining a waiting list that requires geolocation.

**Organizer:**

US 02.01.01 As an organizer I want to create a new event and generate a unique promotional QR code that links to the event description and event poster in the app

US 02.01.02 As an organizer I want to store the generated QR code in my database

US 02.01.03 As an organizer, I want to create and manage my facility profile.

US 02.02.01 As an organizer I want to view the list of entrants who joined my event waiting list

US 02.02.02 As an organizer I want to see on a map where entrants joined my event waiting list from.

US 02.02.03 As an organizer I want to enable or disable the geolocation requirement for my event.

US 02.03.01 As an organizer I want to OPTIONALLY limit the number of entrants who can join my waiting list

US 02.04.01 As an organizer I want to upload an event poster to provide visual information to entrants

US 02.04.02 As an organizer I want to update an event poster to provide visual information to entrants

US 02.05.01 As an organizer I want to send a notification to selected entrants to confirm or decline their spot in the event.

US 02.05.02 As an organizer I want to set the system to sample a specified number of attendees to register for the event

US 02.05.03 As an organizer I want to be able to draw a replacement applicant from the pooling system when a previously selected applicant cancels or rejects the invitation

US 02.06.01 As an organizer I want to view a list of all chosen entrants who are invited to apply

US 02.06.02 As an organizer I want to see a list of all the cancelled entrants

US 02.06.03 As an organizer I want to see a final list of entrants who enrolled for the event

US 02.06.04 As an organizer I want to cancel entrants that did not sign up for the event

US 02.07.01 As an organizer I want to send notifications to all entrants on the waiting list

US 02.07.02 As an organizer I want to send notifications to all selected entrants

US 02.07.03 As an organizer I want to send a notification to all cancelled entrants

**Admin:**

US 03.01.01 As an administrator, I want to be able to remove events.

US 03.02.01 As an administrator, I want to be able to remove profiles.

US 03.03.01 As an administrator, I want to be able to remove images.

US 03.03.02 As an administrator, I want to be able to remove hashed QR code data

US 03.04.01 As an administrator, I want to be able to browse events.

US 03.05.01 As an administrator, I want to be able to browse profiles.

US 03.06.01 As an administrator, I want to be able to browse images.

US 03.07.01 As an administrator I want to remove facilities that violate app policy
