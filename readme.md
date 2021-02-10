# React Native with Expo

### expo 사용

    - 현재 프로젝트의 목표에 expo 가 충분한 기능을 제공합니다.
        - network, webview, camera...
    - Managed workflow - typescript 를 사용합니다.
    - 추후 프로젝트 고도화에 따라 native 기능이 필요할 경우 Bare workflow 사용 또는 eject 등의 방법을 활용 할 수 있습니다.

#### expo-cli 설치

```
npm install --global expo-cli
```

### expo 프로젝트 생성

```
expo init my-project
```

- blank typescript 사용

### React Native Features

- [Core Components and APIs](https://reactnative.dev/docs/next/components-and-apis)
- [Networking](https://reactnative.dev/docs/next/network)
- [Custom WebView](https://reactnative.dev/docs/next/custom-webview-android)
- [Security](https://reactnative.dev/docs/next/security#authentication-and-deep-linking)

### Expo Features

- [TypeScript](https://docs.expo.io/guides/typescript/)
- [WebView](https://docs.expo.io/versions/latest/sdk/webview/)
- [Network](https://docs.expo.io/versions/latest/sdk/network/)
- [Security](https://docs.expo.io/distribution/security/#device-tokens-for-ios-and-android-push)
- [Notifications](https://docs.expo.io/versions/latest/sdk/notifications/)
- [Fetching tokens for push notifications](https://docs.expo.io/versions/latest/sdk/notifications/#fetching-tokens-for-push-notifications)

### IOS, Android 환경 설정

#### Xcode

- Xcode 설치 - App Store
- Xcode > Preferneces > Location - 최신 버전인지 확인
- Xcode > Open Developer Tools > Simulator

- [iOS Simulator](https://docs.expo.io/workflow/ios-simulator/)

#### Android Studio

- Android Studio 설치 - https://developer.android.com/studio?hl=id
  - Standard 로 설치
- Android Studio 실행

  - Configure > SDK Manager 설정
  - Configure > ADB Manager 설정

- [Android Studio Emulator](https://docs.expo.io/workflow/android-studio-emulator/)

  - macos 추가 설정

    - .bash_profile 에 PATH 추가
    - Android Studio 설정 시 Android SDK Location 이 표시되는 데 해당 경로를 추가. 터미널에서 아래 두 명령 실행

    ```
    [ -d "$HOME/Library/Android/sdk" ] && ANDROID_SDK=$HOME/Library/Android/sdk || ANDROID_SDK=$HOME/Android/Sdk
    echo "export ANDROID_SDK=$ANDROID_SDK" >> ~/`[[ $SHELL == *"zsh" ]] && echo '.zshenv' || echo '.bash_profile'`
    ```

    ```
    echo "export PATH=$HOME/Library/Android/sdk/platform-tools:\$PATH" >> ~/`[[ $SHELL == *"zsh" ]] && echo '.zshenv' || echo '.bash_profile'`
    ```

    - 터미널에서 adb 를 입력하여 경로 설정 확인

### Debug

### Tips

- [[리액트 네이티브(React Native, RN)] 앱과 웹뷰(Webview) 사이에서 인터페이스를 활용해 커뮤니케이션(통신)하는 방법(react native communicate between app webview)](https://webruden.tistory.com/305)
- [React Native : iOS 용 앱 권한 관리](https://ichi.pro/ko/react-native-ios-yong-aeb-gwonhan-gwanli-72588741600664)

### Expo path issue

- [Expo CLI looks installed but ‘expo: command not found’](https://forums.expo.io/t/expo-cli-looks-installed-but-expo-command-not-found/14535)
