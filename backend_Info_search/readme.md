스프링부트 프로젝트용

1. Error 발생 -> 프로젝트 임포트 중 wrapper 없는 경우 이슈 발생

<img width="828" height="990" alt="image" src="https://github.com/user-attachments/assets/c9c9f3c7-b71a-42a8-913c-b54188907d34" />

설명
Description	Resource	Path	Location	Type
The supplied phased action failed with an exception.
Could not open cp_init generic class cache for initialization script 'C:\Users\Admin\Desktop\sts workspace\.metadata\.plugins\org.eclipse.buildship.core\init.d\eclipsePlugin.gradle' (C:\Users\Admin\.gradle\caches\8.1.1\scripts\2to4is5l87jn9v7vrcgka57e).
BUG! exception in phase 'semantic analysis' in source unit '_BuildScript_' Unsupported class file major version 65
Unsupported class file major version 65	demo_		line 0	Gradle Error Marker


폴더 내에 wrapper 없는 경우. 
위의 방법 통해 내 컴퓨터 내 gradle 다운받은 후, 환경 변수 설정
다음 gpt 설명 따라서 
✅ 1️⃣ Gradle Wrapper 생성하기

방법 A — 터미널 명령으로 자동 생성
STS 또는 명령 프롬프트에서 demo 폴더 위치로 이동:
cd C:\Users\Admin\Desktop\ (프로젝트 위치. src / build.gradle 있는 위치까지 이동 ) 

다음 명령 실행:
gradle wrapper --gradle-version 8.10.2 (버전은 알아서 수정)

결과
<img width="1614" height="394" alt="image" src="https://github.com/user-attachments/assets/5e72eca9-fe04-4205-914b-7b80bdabab09" />
<img width="416" height="382" alt="image" src="https://github.com/user-attachments/assets/2692d3f4-0b2a-4b62-a5d1-fc3f179357d5" />

⚠️ gradle 명령이 인식되지 않으면,
Gradle 공식 CLI
 설치 후 환경 변수 PATH에 추가해야 합니다.
(또는 STS 내장 Gradle Console에서 실행해도 됩니다.) 

 -참조용 url 정리-
1. gradle 환경변수 편집 방법
https://nazzang19.tistory.com/128#google_vignette

2. gradle 설치 링크
https://gradle.org/install/
