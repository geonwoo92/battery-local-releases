# Battery Local releases

Battery Local Android 앱의 APK 배포 전용 저장소입니다. 소스코드와 개인 차량 데이터는 이 저장소에 업로드하지 않습니다.

## 설치

[최신 APK 다운로드](https://github.com/geonwoo92/battery-local-releases/releases/latest/download/BatteryLocal.apk)

0.1.3 이상부터 앱을 열면 이 저장소의 새 버전을 자동으로 확인합니다. 업데이트를 누르면 다운로드 후 Android 설치 확인 화면이 열립니다. 기존 앱을 삭제하지 않고 업데이트하면 설정과 기록을 유지합니다.

## 새 버전 배포

1. 기존 앱과 같은 서명 키로 APK를 만들고 `versionCode`를 이전보다 크게 설정합니다.
2. 새 GitHub Release에 APK를 **BatteryLocal.apk**라는 이름으로 첨부하고 발행합니다.
3. Actions의 **Generate update manifest**가 완료되면 `update.json`이 자동 첨부되고 앱에서 새 버전을 확인할 수 있습니다.

초안·프리릴리즈는 자동 업데이트 대상으로 사용하지 않습니다. 태그 이름만 바꾸고 같은 versionCode의 APK를 올리면 업데이트로 취급되지 않습니다. 서명이 다른 APK는 기존 앱 위에 설치할 수 없습니다.

릴리즈 발행 후 APK를 추가한 경우에는 Actions에서 **Generate update manifest**를 해당 태그로 수동 실행하세요.
