# School Bus Tracker App 🚌

A comprehensive Flutter application for real-time school bus tracking with WhatsApp-style design and Firebase integration.

## Features ✨

### 🚌 Real-time Bus Tracking
- Live GPS tracking of school buses
- Real-time location updates using Firebase Firestore
- Interactive Google Maps integration
- Speed monitoring and ETA calculations

### 👥 Student Management
- Track student boarding status
- Parent contact information
- Student attendance on buses
- Real-time student location updates

### 🔔 Smart Notifications
- Push notifications for bus arrivals
- Delay alerts and emergency notifications
- WhatsApp-style notification interface
- Real-time updates for parents and school staff

### 🎨 WhatsApp-Style Design
- Modern, clean interface inspired by WhatsApp
- Intuitive navigation and user experience
- Color-coded status indicators
- Smooth animations and transitions

### 📱 Multi-Role Support
- **Driver Mode**: Track and share bus location
- **Parent/School Mode**: Monitor bus and student status
- **Admin Features**: Manage buses, routes, and students

## Technical Stack 🛠️

- **Frontend**: Flutter (Dart)
- **Backend**: Firebase (Firestore, Authentication, Messaging)
- **Maps**: Google Maps Flutter
- **Location**: Geolocator
- **State Management**: Provider/Riverpod
- **Real-time Data**: Firebase Firestore Streams

## Installation & Setup 📦

### Prerequisites
- Flutter SDK (3.9.2 or higher)
- Android Studio / VS Code
- Firebase project
- Google Maps API key

### 1. Clone the Repository
```bash
git clone <repository-url>
cd healthapp
```

### 2. Install Dependencies
```bash
flutter pub get
```

### 3. Firebase Setup
1. Create a Firebase project at [Firebase Console](https://console.firebase.google.com/)
2. Enable Firestore Database
3. Enable Firebase Authentication
4. Enable Firebase Cloud Messaging
5. Download `google-services.json` and place it in `android/app/`
6. Update `lib/firebase_options.dart` with your Firebase configuration

### 4. Google Maps Setup
1. Get Google Maps API key from [Google Cloud Console](https://console.cloud.google.com/)
2. Enable Maps SDK for Android/iOS
3. Add API key to `android/app/src/main/AndroidManifest.xml`:
```xml
<meta-data android:name="com.google.android.geo.API_KEY"
           android:value="YOUR_API_KEY"/>
```

### 5. Permissions
Add location permissions to `android/app/src/main/AndroidManifest.xml`:
```xml
<uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
<uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />
```

## Usage Guide 📖

### For Drivers
1. Open the app and select "I am a Driver"
2. Set your bus number
3. Tap "START TRACKING" to begin sharing location
4. Monitor speed and location in real-time
5. Tap "STOP TRACKING" when route is complete

### For Parents/School Staff
1. Select "Track Bus (Parent/School)"
2. Choose the bus you want to track
3. View real-time location on map
4. Check student boarding status
5. Receive notifications for arrivals and delays

### Sample Data
- Tap "Seed Sample Data" to populate Firebase with test data
- This creates sample buses, students, and notifications
- Useful for testing and demonstration

## Firebase Data Structure 📊

### Collections
```
school_data/
├── buses/
│   ├── BUS-001/
│   ├── BUS-002/
│   └── BUS-003/
├── bus_locations/
│   ├── BUS-001/
│   ├── BUS-002/
│   └── BUS-003/
├── students/
│   ├── student-001/
│   ├── student-002/
│   └── ...
└── notifications/
    ├── notif-001/
    ├── notif-002/
    └── ...
```

### Data Models
- **BusLocation**: Real-time GPS coordinates and status
- **Bus**: Bus information, routes, and stops
- **Student**: Student details and boarding status
- **NotificationData**: Push notifications and alerts

## Key Features Explained 🔍

### Real-time Tracking
- Uses Firebase Firestore streams for instant updates
- GPS location updates every 10 meters
- Automatic speed calculation and monitoring
- Offline capability with local caching

### WhatsApp-Style UI
- Green color scheme (#075E54, #25D366)
- Message-like notification cards
- Smooth bottom sheet modals
- Status indicators and badges

### Student Management
- QR code scanning for boarding
- Parent contact integration
- Attendance tracking
- Emergency contact system

### Notification System
- Push notifications via Firebase Cloud Messaging
- Real-time alerts for arrivals and delays
- Emergency notifications
- Customizable notification preferences

## Customization 🎨

### Colors
```dart
// WhatsApp Green Theme
primaryColor: Color(0xFF075E54)
secondaryColor: Color(0xFF25D366)
backgroundColor: Color(0xFFECE5DD)
messageColor: Color(0xFFDCF8C6)
```

### Bus Routes
- Add custom bus stops in Firebase
- Define route sequences
- Set estimated arrival times
- Configure student assignments

## Troubleshooting 🔧

### Common Issues
1. **Location not updating**: Check GPS permissions
2. **Firebase connection failed**: Verify google-services.json
3. **Maps not loading**: Check Google Maps API key
4. **Notifications not working**: Enable Firebase Cloud Messaging

### Debug Mode
```bash
flutter run --debug
```

## Security Considerations 🔒

- Location data is encrypted in transit
- User authentication required for sensitive operations
- Firebase security rules implemented
- Privacy-compliant data handling

## Future Enhancements 🚀

- [ ] Offline mode with local database
- [ ] Multi-language support
- [ ] Advanced analytics dashboard
- [ ] Integration with school management systems
- [ ] AI-powered route optimization
- [ ] Parent-teacher communication features

## Contributing 🤝

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License 📄

This project is licensed under the MIT License - see the LICENSE file for details.

## Support 💬

For support and questions:
- Create an issue on GitHub
- Contact: [your-email@example.com]
- Documentation: [link-to-docs]

---

**Made with ❤️ for safer school transportation**