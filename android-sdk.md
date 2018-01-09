# Android SDK
---
## 1.	SDK 초기 설정
<hr>
## setBaseSettings

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
<hr>
## setLocationInfo
public void setLocationInfo(String localFilePrefix, boolean useLocalData)

현재 장소에 대한 정보를 설정한다

### Parameter
- localFilePrefix : 현재 사이트에 대한 정보 : 서울시청 “sch”, 엠투컴: “m2comm”
- useLocalData : true: local로 가지고 있는 beacon 및 node에 대한 정보를 사용한다
- intentPrefix : 앱의 package 이름

### return
없음

---

## loadGraphInfoFromFile
public void loadGraphInfoFromFile(String prefix, boolean useFileFromAssets)

현재 사이트에 대한 Graph(node) 정보를 얻어온다.

### Parameter
- Prefix : 현재 사이트에 대한 정보 : 서울시청 “sch”
- useFileFromAssets  : true: assert폴더로부터 Graph 정보를 사용한다

### return
없음

---

## loadBeaconInfoFromFile
public void loadBeaconInfoFromFile(String prefix, boolean useFileFromAssets)

현재 사이트에 대한 beacon 정보를 얻어온다.

### Parameter
- Prefix : 현재 사이트에 대한 정보 : 서울시청 “sch”
- useFileFromAssets  : true: assert폴더로부터 Graph 정보를 사용한다, false: 서버에서 beacon 및 node에 대한 정보를 가져온다

### return
없음

---

## useServer
public void useServer()

Beacon 및 Graph 정보를 얻어오기 위해 서버를 사용한다. doNotUseServer 호출 후 다시 서버를 사용하기 위해 호출한다.

### Parameter
없음

### return
없음

---

## checkServerLastModified
public void checkServerLastModified(int which, String uuidForMap)

서버에 BEACON 및 Graph(Node)정보가 업데이트되었는지 여부를 조회한다.

### Parameter
- which:
         - CHECK_SERVER_NODE = 1; node 정보 조회
         - CHECK_SERVER_BEACON = 2; beacon 정보 조회
         - CHECK_SERVER_MAP = 4; MAP 정보 조회
         - CHECK_SERVER_ALL = 5: 모든 정보 조회


### return
없음
