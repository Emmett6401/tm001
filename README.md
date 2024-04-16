# tm001
티처블머신러닝에서만든모델을이용한파이썬프로그램 1번째
## 이 프로그램에 대한 설명
  - 이 프로그램은 카메라를 사용하지 않습니다.
  - 4가지 Class를 식별합니다.
### Languages
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=Python&logoColor=white)

### Badge를 넣는 방법 
  - 이런 곳에 사용하는 배지는 [여기를 참조 하세요](https://shields.io).



## 새프로젝트 시작하는 방법
  1. 새 폴더를 만듭니다. - 부속된 dataset, model등 구조를 완성하세요
    - git clone을 이용해서 이 코드를 복사 한다면 다음과 같이 하세요
```bash
  git clone https://github.com/Emmett6401/tm001.git
```

    
  3. VSCode를 실행하고 터미널을 열고
  4. 가상환경을 만들어요 -
```bash
conda create -n tm001 python=3.9
```

  5. 가상환경과 VScode를 연결해주세요 - CTRL+SHIFT+P - select python interpreter (새로 만든 가상환경 이름이 보이지 않으면 VSCODE를 종료하고 다시 시작)
  6. 새 터미널 확인 - 
  
  
  7. 패키지를 설치
### Packages
  - 1. requirements.txt가 있는 경우 

```bash
pip install -r requirementx.txt
```

  - 2. requirementx.txt가 없는경우

```bash  
  pip install opencv-python 
  pip install pillow 
  pip install tensorflow==2.12.0
```

  - 3. Requirements.txt를 만드는 법 (개발에 필요한 패키지를 버젼까지 저장해 놓은 중요한 문서)
```bash
  pip freeze > requirements.txt
...

  7. 코드를 tm001.py 코드를 완성하세요 - 폴더위치등을 수정하세요 (코드는 TM에서 코드스니펫으로 가져 올수 있어요)
     
## 기타 관련 지식
### Teachable Machine(티처블 머신)이란?
Teachable Machine은 구글에서 만든 웹기반 노코드 인공지능 학습 툴입니다. 이미지, 사운드, 자세를 인식하도록 컴퓨터를 학습시켜서 사이트, 앱 등에 사용할 수 있는 머신러닝 모델을 쉽고 빠르게 만들 수 있습니다. 전문지식이나 코딩 능력이 필요하지 않아서 초등학생도 만들 수 있을 정도로 이해하기 쉽다는 점이 가장 큰 장점이죠!

Teachable Machine 은 크게 3가지 단계로 이루어집니다. 첫번째 ‘모으기’ 단계에서는 예시를 수집하여 컴퓨터가 학습하기를 원하는 클래스 또는 카테고리로 그룹화합니다. 그 후에는 ‘학습 시키기’를 통해 모델을 학습시켜서 새로운 예시를 올바르게 분류하는지 즉시 테스트해 보는 것이 가능합니다. 마지막으로 ‘내보내기’로 사이트, 앱 등 프로젝트에 대한 모델을 내보내게 되면 모델을 다운로드하거나 온라인으로 호스팅할 수 있습니다.

백문이 불여일견, 직접 해 보면서 Teachable Machine이 어떻게 동작하는지 살펴보기로 할께요! 

### Teachable Machine 활용 사례 
Teachable Machine을 활용해서 제가 만들어 본 프로젝트는 ‘코로나에 안전한 마스크 착용을 구분하라’ 입니다.
마스크를 썼을 때 코로나에 안전한지를 판단할 수 있도록 턱에 걸쳐쓰는 마스크 착용 사례는 마스크를 미착용 한 것으로 판단할 수 있는 머신러닝을 만들어 보면 유용할 것이라는 생각이 들었어요. 제가 만들어 본 Teachable Machine 활용 사례를 설명해 보도록 하겠습니다.

구글 티처블 머신 사이트(https://teachablemachine.withgoogle.com/)에 접속해서 시작하기를 버튼을 누르면 하기와 같이 프로젝트의 종류를 선택할 수 있게 나옵니다.  이미지, 오디오, 포즈 등 어떤 입력을 주로 활용할 것인지 속성에 따라서 구분이 되어있네요. 저는 마스크를 쓴 모습을 구분할 예정이므로 ‘이미지 프로젝트’를 선택해봤습니다.

### 이미지프로젝트
‘이미지 프로젝트’를 선택하니 나오는 화면입니다. 이미지 샘플을 추가 할 수 있는 Class와, 학습, 미리보기로 구성되어 있습니다. Class 1과 Class 2에 머신러닝으로 학습하고 싶은 케이스를 입력해보도록 하겠습니다. 저는 마스크를 착용하지 않는 ‘노마스크’를 Class 1으로, 마스크 착용 모습을 ‘마스크’로 Class2에 지정을 해서 웹캠으로 이미지 샘플을 촬영했습니다.
