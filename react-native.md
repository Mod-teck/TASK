# Event & Activity Management Mobile App

## Description
The goal is to design and develop a complete mobile application for managing events and activities using **React Native**. The app should allow users to:

- Create new events
- Invite other users
- Manage attendance (Attendees)
- Track the timeline and progress of events

The system must include a fully functional frontend interface for mobile devices (Android and iOS).

---

## Requirements

### 1. Frontend (UI/UX)

#### React Native Components
- Use core React Native components such as `View`, `Text`, `Button`, `FlatList`, and `ScrollView`.
- Design a modern and clean user interface.
- Use **React Navigation** for screen transitions.
- Use UI libraries like **React Native Paper** or **NativeBase** to enhance design and include ready-made UI components.

#### Responsive Design
- Ensure the app works well on various screen sizes (phones and tablets).
- Use **Flexbox** for flexible and responsive layout designs.

#### Local Storage
- Store all data (events, users, attendees) locally using **AsyncStorage**.
- On reopening the app, data should be retrieved from AsyncStorage and displayed correctly.

---

### 2. Core Features

#### Event Management
- Users can create a new event by entering:
  - Event name
  - Start and end date/time
  - Event location
  - Event description
- Display a list of all events with details such as:
  - Name, date, location, number of participants
- Allow editing and deleting of existing events

#### User Invitations
- Users can invite others to the event
- Each invited user should have a:
  - Name
  - Email address
- Display the list of invited users per event

#### Attendance Management
- Users can set each invited user's attendance status:
  - Attending / Not Attending / Pending
- Display attendees and their statuses per event
- Allow updating attendance status

#### Event Timeline
- Display a timeline view of upcoming and completed events
- Show a countdown for upcoming events
- Show a message if the event is completed

#### Search & Filter
- Enable searching for a specific event
- Filter events based on status:
  - Upcoming
  - Completed

---

### 3. Advanced Features

#### Push Notifications
- Send in-app notifications to remind users of upcoming events
- Use **React Native Push Notification** for implementation

#### Google Maps Integration
- Display the event location on a map using **React Native Maps**
- Use the entered address to show the correct geographic location

#### Image Upload
- Allow users to upload images for events (e.g., cover photo)
- Use **React Native Image Picker** to select images from the device

#### Dark Mode
- Provide a **Dark Mode toggle**
- Entire design should adjust based on the selected mode

---

### 4. Optional Technologies (Bonus)

- **Animations**: Add simple effects when elements are added/removed (e.g., fade in/out for events)
- **Real-Time Updates**: If time allows, use **Firebase Firestore** to implement real-time data syncing
