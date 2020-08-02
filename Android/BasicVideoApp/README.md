# Vonage - BasicVideoApp for Android
This is a basic Android app that uses the Vonage Video API.

# Based on Vonage's official tutorial
https://tokbox.com/developer/tutorials/android/basic-video-chat/

# Customisation on this app
1. This app contains a custom button which switches ON/OFF video streaming by calling the setPublishVideo() method.
Reference: https://tokbox.com/developer/guides/audio-video/android/#publish_audio_video_only
2. This app uses Heroku server side authentication instead of hardcoding your credentials.
Reference: https://tokbox.com/developer/tutorials/android/basic-video-chat/#server

# Step to run
1. Replace YOUR_HEROKU_APP_NAME with your Heroku app name in the fetchSessionConnectionData() method.
If you don't have a Heroku account, you'll need to sign up. See detail from here: https://tokbox.com/developer/tutorials/android/basic-video-chat/#server
2. Run the app once and you'll see your SESSION_ID from Logcat which is generated via Heroku server with your credentials. Grab it and create a second settion from OpenTok Playground: https://tokbox.com/developer/tools/playground/
3. You'll see a basic video app on your device. If you run the app on an emulator, the publisher video will display an animated graphic instead of your camera feed since the emulator cannot access your webcam.

If you want to try hardcoded authentication, grab your credentials from your TokBox Account (https://tokbox.com/account) and replace YOUR_API_KEY, YOUR_SESSION_ID, and YOUR_TOKEN with them. Do not forget to comment out the fetchSessionConnectionData() method where using Heroku authentication and uncomment the requestPermissions() method.

If you want to use a PHP server (https://github.com/opentok/learning-opentok-php) to get credentials instead of the Heroku, replace URL in the fetchSessionConnectionData() method with your localhost address like http://10.0.2.2:8080.


# Disclaimer
This example is provided AS IS. Use it as your own risk.
