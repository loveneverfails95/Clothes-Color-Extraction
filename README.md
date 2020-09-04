# Clothes-Color-Extraction


## 소개
- 의류 이미지에서 색을 추출하여 색의 이름과 해당 색이 의류 이미지에서 몇 %를 차지하는지 알려줍니다.
- 예시
  1. 원본 이미지
  ![1](https://user-images.githubusercontent.com/69623247/92208883-0c456b00-eec7-11ea-874d-456e6ddd1121.png)


  2. 결과창
  ![result](https://user-images.githubusercontent.com/69623247/92203103-57f21780-eebb-11ea-96e0-f925f7294fc0.PNG)

  원본 이미지를 보면 흰색이 들어가 있으나 추출 결과 흰색이 나오지 않습니다. 그 이유는 색 추출 전 segmentation 작업이 이루어지는데, 이 segmentation 시 원본 이미지에 왜곡이 있었기 때문입니다. 


  3. Segmentation
  ![seg_sample](https://user-images.githubusercontent.com/69623247/92203308-c59e4380-eebb-11ea-8683-99fd37ccba22.png)

  의류 segmentation 소스코드들을 많이 찾아보았으나, 그나마 지금 사용한 segmentation 모델의 퍼포먼스가 가장 좋았습니다. segmentation의 경우 제가 직접 만든 것이 아니니 segmentation에 필요한 파일들은 제작자의 repository에서 다운 받으셔야 합니다. 관련 사항은 아래 '실행'파트를 참고하세요.
  * 왜 segmentation을 하는가?: 배경색을 제거하기 위함입니다. sementation을 하면 색을 추출할 때 배경색이 추출되지 않습니다.
  
- Process: 다음과 같은 과정을 거치며 결과가 출력됩니다.
![brief introduction of the process of the model](https://user-images.githubusercontent.com/69623247/92207340-0732ec80-eec4-11ea-87b5-4fbcb19999cd.jpg)


## 실행
1. segmentation 파일 준비: 아래 링크로 가서 model폴더와 annotation.csv파일을 받습니다. 
https://github.com/khalid5454/Fashion-AI-segmentation

2. 위에서 다운받은 파일들을 본 repository에서 다운로드 받은 폴더(Clothes-Color-Extraction)에 넣습니다.

3-1. (코랩을 이용할 경우) 구글 드라이브에 폴더를 넣고 Run.ipynb을 실행시킵니다. 실행법은 해당 파일 내에 적혀 있습니다.
3-2. (코랩을 이용하지 않을 경우) drive.mount 코드를 실행시키지 않고 그 아래 '준비 코드'부터 실행하면 됩니다.


## 기타
- 앞서 몇 차례 언급했듯이 segmentation은 이미 만들어진 모델을 사용했습니다. 
- 소스코드와 관련하여 궁금한 점이 있으시면 프로필에 적혀 있는 이메일로 언제든지 연락주세요!
- 색 목록이 있는 엑셀 파일은 국가표준기술원의 '공공디자인색채표준가이드(2009)'를 바탕으로 제작되었습니다.
