### 1	SDK 초기 설정

public void setBaseSettings(Context ctx, String domain, String intentPrefix)

SDK 관련 초기 설정을 수행한다. SDK 를 실행 전에 반드시 호출되어야 한다. 
Parameter
ctx : Context
domain : API 서버의 주소
intentPrefix : 앱의 package 이름
return
 없음
사용 예 
Config_Base.setBaseSettings(getApplicationContext(), "https://api.pnuh.pntbiz.com", "com.pnt.v4_3p.hyuh");

