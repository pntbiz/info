# Android SDK

## 1.	SDK 초기 설정
### setBaseSettings

public void setBaseSettings(Context ctx, String domain, String intentPrefix)

SDK 관련 초기 설정을 수행한다. SDK 를 실행 전에 반드시 호출되어야 한다.

### Parameter
- ctx : Context
- domain : API 서버의 주소
- intentPrefix : 앱의 package 이름

### return
없음

### 사용 예 
Config_Base.setBaseSettings(getApplicationContext(), "https://api.pnuh.pntbiz.com", "com.pnt.v4_3p.hyuh");

---

## 2. BEACON 및 GRAPH 정보 설정
### setLocationInfo
public void setLocationInfo(String localFilePrefix, boolean useLocalData)

현재 장소에 대한 정보를 설정한다

### Parameter
- localFilePrefix : 현재 사이트에 대한 정보 : 서울시청 “sch”, 엠투컴: “m2comm”
- useLocalData : true: local로 가지고 있는 beacon 및 node에 대한 정보를 사용한다
- intentPrefix : 앱의 package 이름

### return
없음

### loadGraphInfoFromFile
public void loadGraphInfoFromFile(String prefix, boolean useFileFromAssets)

현재 사이트에 대한 Graph(node) 정보를 얻어온다.

### Parameter
- Prefix : 현재 사이트에 대한 정보 : 서울시청 “sch”
- useFileFromAssets  : true: assert폴더로부터 Graph 정보를 사용한다

### return
없음

