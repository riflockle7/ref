참고 링크	http://leeted.tistory.com/142					
						
Table 네이밍						
1)   규칙					2)   표기 방식	
  테이블임을 표시하기 위해 테이블 명 앞에 ‘TB_’ 라는 구분을 사용함					ex>	CREATE TABLE users (...);
  테이블명은 대문자 / 복수형으로 사용함						CREATE TABLE business_users (...);
  시스템 구분 코드와 모듈구분코드로 업무 영역을 구분함						
  의미있는 테이블명은 3단어까지 사용할 수 있음						
  단어와 단어 사이는 ‘_’로 구성함						
  각 단어는 최대 8자리까지 사용함						
  구분명은 Table의 특성을 나타냄						
  예로는 Master, Detail, Control, Summary, Trigger, History 등이 있음						
						
Field 네이밍					ex>	users
  유일키는 언제나 id						id
  소문자 활용						address
  단어와 단어 사이는 ‘_’로 구성함 (단, 사전에 등록된 복합명사는 띄어쓰기를 하지 않음)						office_address
						
						
Join Table 네이밍					ex> 	CREATE TABLE business_users_users (...);
  조인하고자 하는 테이블들의 이름을 연결						
  알파벳 순서 적용						
  복수형 사용						
  소문자 사용						
						
Join Table Field 네이밍					ex>	business_users_users
  유일키는 언제나 id						id
  소문자 활용						user_id
  외래키는 테이블의 단수형 + '_id'						business_user_id
ex> 	users table → user_id					
	business_users → business_user_id					
						
Index 네이밍						
  인덱스 키 타입과 인덱스 대상 테이블 및 필드의 이름을 언더스코어로 구분하여 붙인다.						
ex> 	<index or key type>_<table name>_<column 1>_<column 2>_<column n>					
  인덱스 키 타입	PK_	프라이머리 키				
	UK_ 	유니크 키				
	UX_ 	유니크 인덱스				
	IX_ 	논클러스터드 논유니크 인덱스				
