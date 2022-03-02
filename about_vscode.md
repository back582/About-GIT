# About-VSCode


## VSCode&Python (2022/03/02 기준)
### 1. vscode 설치
https://code.visualstudio.com/  
해당 링크를 통해 vscode 설치
![1](https://user-images.githubusercontent.com/17943248/156362609-3846cb14-caa0-4658-8791-c9987543ab5c.png)
  

### 2. vscode에 기본 필요 확장 패키지 설치 
vscode 활성화 -> 맨 좌측 '확장' 메뉴 클릭 -> 'Code Runner', 'python', 'python path', 'pylance', 'python extension pack'  
패키지들을 검색하여 설치 (본인에게 필요한 확장 패키지를 더 설치해도 무방)
![1](https://user-images.githubusercontent.com/17943248/156363027-7974f4c7-5922-4a56-bafc-0e3744c6a2a3.png)


### 3. Anaconda 설치 및 가상환경 설정
https://www.anaconda.com/products/individual  
해당 링크를 통해 anaconda 설치 
![1](https://user-images.githubusercontent.com/17943248/156363359-6b6aa0a8-a5ae-4db9-b624-49e6f6df14da.png)

-> anaconda 실행 -> 좌측에 'Environments' 클릭 -> 하단에 create 클릭 -> 자신입맛대로 가상환경 구축  
(만약 딱히 설정할 가상환경이 없다면 base(root)를 사용해도 무방하고 아래 그림처럼 설정하고 구축해도 무방)
![1](https://user-images.githubusercontent.com/17943248/156363791-1002b207-6165-4a82-a67b-33c94d835ae2.png)

### 4. python path 설정 (anaconda를 설치하지 않고 python만 설치했을 경우)
python 설치한 경로에서 Scripts 파일 경로 (보통 C:\Users\사용자\AppData\Local\Programs\Python\Python310\Scripts 에 가보면됨) 복사 ->  
윈도우 환경에서 '고급 시스템 설정 보기' 클릭 -> '환경 변수 클릭' -> 사용자 변수와 시스템 변수 둘 다 'path' 클릭 후 편집 -> 새로만들기 ->  
경로붙여넣기 -> 모든 창 확인 -> 컴퓨터 재부팅
![1](https://user-images.githubusercontent.com/17943248/156365373-41fe6798-488a-4774-996f-5d0933da14ec.png)


### 5. 중간 검사
vscode 실행 -> 상단에 '파일' 클릭 -> '새 파일' 클릭 -> 파이썬 파일로 변경 -> print("hello world") -> 후 나오는 메뉴얼 그대로 진행 ->
모든 메뉴얼을 진행했다면 ->
터미널 창에 'pip' 입력 ->   
만약 pip 용어를 모르겠다는 표현이면 위 4번 항목 다시 할것, 그래도 안되면 python 전체 완전 삭제 후 2번 항목부터 다시 시도할것.
만약 pip 명령어들이 출력된다면 성공

### 6. vscode에 필요 python 모듈 설치 
vscode 파워쉘 활성화 (보통 하단에 활성화됨) -> pip install matplotlib, pip install tensorflow 등 필요한 패키지 설치 ->   
만약 터미널 창에 pip의 업그레이드가 필요하다고 하면 업그레이드 진행 (친절하게 업그레이드 명령어 알려줌 그대로 실행하면됨)

### 7. 마지막 검사
파워쉘에 다음과 같이 모듈을 확인  
pip list  

->

vscode에서 ctrl + shift + p -> Python: Select Interpreter 클릭 -> 자신의 가상환경 클릭

->

  
파이선 스크립트를 다음과 같이 작성   

'''  
import matplotlib.pyplot as plt  
import tensorflow  
  
print("더 확인 할 패키지가 있다면 아래와 같이 코드 작성하세요")  
print(matplotlib.__version__)  
print(tensorflow.__version__)  
  
plt.plot([1, 2, 3, 4])  
plt.show()  
'''  

->  
F5로 실행 -> 만약 터미널에서 버전도 확인되고 그래프가 표시된다면 VScode에 Python 개발 환경은 모두 구축 완료 된 상태, 즐거운 코딩되세요
