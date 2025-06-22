# 🏥 Health Monitoring System - SoulSpace

## Overview

SoulSpace now includes a comprehensive health monitoring system that integrates with wearable devices to provide real-time health insights and stress management. The system uses Google Health Connect to read health data from various wearable devices and smartwatches.

## 🚀 Features

### ✅ Implemented Features

1. **Real-time Health Data Integration**
   - Heart rate monitoring with stress estimation
   - Sleep tracking and quality analysis
   - Step counting and activity monitoring
   - Blood pressure tracking
   - Oxygen saturation monitoring

2. **Health Dashboard**
   - Comprehensive health metrics display
   - Real-time data visualization
   - Health alerts and notifications
   - Connection status monitoring

3. **Background Monitoring**
   - Continuous health data sync (every 15 minutes)
   - Background service for persistent monitoring
   - Automatic alert detection

4. **Smart Alerts System**
   - High/low heart rate alerts
   - Stress level warnings
   - Poor sleep quality notifications
   - Low activity reminders
   - Blood pressure warnings

5. **Permission Management**
   - Health Connect permission handling
   - Graceful permission request flow
   - Connection status indicators

## 📱 Supported Devices

The system works with any device that supports Google Health Connect:

- **Smartwatches**: Samsung Galaxy Watch, Google Pixel Watch, Fitbit Sense/Versa
- **Fitness Trackers**: Fitbit Charge, Garmin devices, Xiaomi Mi Band
- **Health Apps**: Samsung Health, Google Fit, Fitbit app
- **Medical Devices**: Blood pressure monitors, pulse oximeters

## 🛠 Technical Implementation

### Core Components

1. **HealthConnectManager** (`HealthConnectManager.kt`)
   - Handles all Health Connect API interactions
   - Reads health data from connected devices
   - Manages permissions and availability checks

2. **HealthDataRepository** (`HealthDataRepository.kt`)
   - Central data management for health metrics
   - Real-time data synchronization
   - Alert detection and management

3. **HealthPermissionHandler** (`HealthPermissionHandler.kt`)
   - Manages Health Connect permissions
   - Handles permission requests and grants
   - Provides permission status information

4. **HealthDashboardScreen** (`HealthDashboardScreen.kt`)
   - Comprehensive health metrics display
   - Real-time data visualization
   - Alert management interface

5. **HealthMonitoringService** (`HealthMonitoringService.kt`)
   - Background service for continuous monitoring
   - Automatic data synchronization
   - Critical alert detection

### Data Flow

```
Wearable Device → Health Connect → HealthConnectManager → HealthDataRepository → UI Components
```

## 🔧 Setup Instructions

### 1. Device Requirements

- Android 6.0 (API level 26) or higher
- Google Health Connect app installed
- Compatible wearable device connected

### 2. Permission Setup

The app automatically requests necessary permissions:

- `android.permission.health.READ_HEART_RATE`
- `android.permission.health.READ_SLEEP`
- `android.permission.health.READ_STEPS`
- `android.permission.health.READ_EXERCISE`
- `android.permission.health.READ_BLOOD_PRESSURE`
- `android.permission.health.READ_OXYGEN_SATURATION`

### 3. Health Connect Setup

1. Install Google Health Connect from Play Store
2. Open SoulSpace app
3. Navigate to Health Dashboard
4. Tap "Connect" to grant permissions
5. Authorize data access in Health Connect

## 📊 Health Metrics

### Heart Rate Monitoring
- **Real-time BPM**: Current heart rate from wearable
- **Average BPM**: 24-hour average heart rate
- **Stress Estimation**: Based on heart rate patterns
- **Alert Thresholds**: 
  - High: >120 BPM (Critical: >140 BPM)
  - Low: <50 BPM (Critical: <40 BPM)

### Sleep Tracking
- **Sleep Duration**: Hours of sleep per night
- **Sleep Quality**: Good (≥7h), Fair (6-7h), Poor (<6h)
- **Sleep Alerts**: Insufficient sleep warnings

### Activity Monitoring
- **Daily Steps**: Step count with 10,000 step goal
- **Activity Progress**: Visual progress indicator
- **Low Activity Alerts**: <5,000 steps warning

### Vital Signs
- **Blood Pressure**: Systolic/Diastolic readings
- **Oxygen Saturation**: SpO2 percentage
- **Alert Thresholds**: High BP (>140/90), Low BP (<90/60)

## 🚨 Alert System

### Alert Types
1. **Critical Alerts** (Red)
   - Very high heart rate (>140 BPM)
   - Very low heart rate (<40 BPM)
   - Critical blood pressure readings

2. **High Priority Alerts** (Orange)
   - High stress levels
   - High heart rate (120-140 BPM)
   - Poor sleep quality (<4 hours)

3. **Medium Priority Alerts** (Blue)
   - Moderate stress levels
   - Low activity levels
   - Fair sleep quality

4. **Low Priority Alerts** (Green)
   - Minor health recommendations
   - Wellness tips

### Alert Management
- Real-time alert detection
- Alert dismissal functionality
- Historical alert tracking
- Customizable alert thresholds

## 🔄 Background Monitoring

### Service Features
- **Continuous Monitoring**: 24/7 health data tracking
- **Automatic Sync**: Every 15 minutes
- **Battery Optimization**: Efficient background operation
- **Foreground Service**: Persistent monitoring with notification

### Monitoring Intervals
- **Health Data Sync**: 15 minutes
- **Alert Check**: Every sync cycle
- **Connection Status**: Continuous monitoring
- **Error Recovery**: 5-minute retry on failures

## 📱 User Interface

### Health Dashboard
- **Connection Status**: Device connection indicator
- **Health Alerts**: Real-time alert display
- **Main Metrics**: Heart rate and stress level
- **Detailed Sections**: Heart rate, activity, sleep, vitals
- **Refresh Functionality**: Manual data sync

### Home Screen Integration
- **Wearable Stress Card**: Quick health overview
- **Real-time Updates**: Live health data display
- **Connection Indicators**: Device status
- **Quick Access**: Health dashboard navigation

## 🔒 Privacy & Security

### Data Protection
- **Local Processing**: Health data processed locally
- **No Cloud Storage**: Health data not uploaded
- **Permission Control**: User-controlled data access
- **Secure APIs**: Health Connect security standards

### Privacy Features
- **Minimal Permissions**: Only necessary health permissions
- **User Consent**: Explicit permission requests
- **Data Transparency**: Clear data usage information
- **Opt-out Options**: Easy permission revocation

## 🐛 Troubleshooting

### Common Issues

1. **Device Not Connected**
   - Ensure Health Connect is installed
   - Check device compatibility
   - Verify Bluetooth connection
   - Restart Health Connect app

2. **No Health Data**
   - Grant all required permissions
   - Check wearable device sync
   - Verify Health Connect setup
   - Restart the app

3. **Background Monitoring Issues**
   - Check battery optimization settings
   - Verify notification permissions
   - Restart background service
   - Check device storage

### Debug Information
- Enable debug logging for detailed information
- Check Health Connect app for data availability
- Verify wearable device data sync
- Monitor background service status

## 🚀 Future Enhancements

### Planned Features
1. **Advanced Analytics**
   - Health trend analysis
   - Predictive health insights
   - Personalized recommendations

2. **Integration Enhancements**
   - Apple Health integration
   - Samsung Health direct API
   - Fitbit API integration

3. **Smart Features**
   - AI-powered health insights
   - Automated wellness recommendations
   - Emergency contact integration

4. **Social Features**
   - Health goal sharing
   - Wellness challenges
   - Community health insights

## 📞 Support

For technical support or questions about the health monitoring system:

1. Check the troubleshooting section above
2. Verify device compatibility
3. Ensure proper setup and permissions
4. Contact support with detailed error information

---

**Note**: This health monitoring system is designed for wellness and stress management purposes only. It is not intended for medical diagnosis or treatment. Always consult healthcare professionals for medical concerns. 