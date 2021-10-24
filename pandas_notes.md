이건알아야되는 함수들

- df.head(), df.tail()
- bigtest.describe()
- bigtest.rename( {'korrr':'kor}, axis = 1, inplace = True )
    
    → { value: 변경value} , axis = 0: 행, axis = 1:열, inplace = True: 변경등록, False: 변경등록X
    
- bigtest['math'].mean() : 평균
- bigtest['math'].std() : 표준편차
- bigtest['math'].mode() : 가장 많이 나온 거
- bigtest.isnull() : 결측값 리스트 좌르르 bool 값
- bigtest.isnull().sum() : 열마다 몇개씩?
- bigtest['kor'].fillna( bigtest['kor'].mean(), inplace = True ) : 결측값 채우기
    
    → bigtest['kor'] 의 결측값은 bigtest['kor']의 평균으로 채우기 fillna
    
- bigtest.sort_value ('mean' , ascending = True)
    
    → mean 을 기준으로 ascending 오름차순 정렬
    
- bigtest.drop (1, axis =0 ) → 1번째 axis = 0 행 삭제
- bigtest.drop ([1,2,3] , axis ='index' ) → 여러 행 한번에 삭제
- bigtest.drop ('math' , axis =1 ) → math axis = 1 열 삭제
- bigtest.drop (['eng', 'math'] , axis ='columns' ) → 여러 열 한번에 삭제
- **Slicing**
- loc() : 행이름, 열이름 으로 슬라이싱
- iloc() : 행인덱스, 열인덱스로 슬라이싱
- bigtest.loc[ 4:10 , 'kor' ]
    
    → 행, 열 // 4-10인 이름의 행 + kor이름인 열
    
- bigtest.iloc[ 1:17 , 2:4 ]
    
    → 1번째-17번째 행 + 2번째-4번째 열
