  
#### 2. MAC OS에 MINICONDA, JUPYTER NOTEBOOK 설치하기  
> 2018.10.21 작업 내용 20:00 ~ 21:00   
> python3.6 설치   
https://www.python.org/downloads/release/python-367/

> conda 설치(개념 및 명령어)   
https://graspthegist.com/post/conda-revisited/   
http://temp123.tistory.com/17   
```
  498  brew install wget
  499  wget
  500  wget https://repo.continuum.io/miniconda/Miniconda3-latest-MacOSX-x86_64.sh
  520  bash Miniconda3-latest-MacOSX-x86_64.sh 
  521  ls
  522  cd miniconda3/
  526  conda list
  531  vi .bash_profile
  532  source .bash_profile
  535  conda list				                -- 사용 가능한 conda 명령어 list 확인
  536  conda env list         					-- 생성된 가상환경 목록 확인(활성화 여부 표시)
  537  conda create -n MLStudy					-- 새 가상환경 추가
  538  conda env list		
  539  source activate MLStudy					-- 사용할 가상환경 활성화
  540  conda env list		
  541  conda install -y flask	  				-- 필요 패키지/모듈 설치, 삭제시 conda uninstall flask
  542  python3 -c "import flask; print(flask.__version__)"
  543  app.py
  544  vi app.py
  548  python3 app.py
  549  vi app.py
  550  python3 app.py
  551  conda deactivate					    		-- 비활성화(base 환경으로 변경)
  552  conda env list
```   
* miniconda 자동 설치는 md5sum mismatch of tar archive 오류 등 맞지 않는 부분이 있어 수동 설치로 진행했다.
* 파이썬은 버전에 따라 지원되는 문법/패키지가 다르고 의존성 관리가 어려워 conda를 사용
* 디렉토리별 환경변수 설정/의존 관계 제한 ([GRASP THE GIST](https://graspthegist.com/) 블로그 글 참조)

#### tensorflow, keras 설치 
> 2018.10.22 작업 내용 20:00 ~ 24:00   
- conda에서 tensorflow 설치시 오류 발생
  - (Could not find a version that satisfies the requirement tensorflow (from versions: ))
- 가상환경의 파이썬 버전이 3.7(지원x)으로 판단, 3.6으로 다운그레이드 -> 동일 문제 발생, 3.5로 다운그레이드 -> 동일 문제 발생 ==> 해당 문제 아님
- tensorflow 사이트에서 macOS 10.12.6 (Sierra) or later (no GPU support) 이상 지원 확인
  > 현재 내 macOS에서 지원 불가 확인 후 OS업데이트 Yosemite 10.10 -> Mojave 10.14   
  > https://www.tensorflow.org/install   
- 데이터 백업 및 macOS업데이트에 저녁시간 모두 소요(ㅋㅋ)
- 완료 후 가상 환경에 pip 버전 업데이트 , tensorflow, keras / pillow, opencv : 예제 실습용 패키지 설치

```
  463  conda activate MLStudy
  465  pip install tensorflow
 
  467  pip install --upgrade pip 
  469  pip install tensorflow
  475  which python3
  478  vi .bash_profile
  479  conda install python=3.6
  480  python -V
  481  pip -V
  484  pip install tensorflow
  485  pip install --upgrade pip
  486  pip -V
  487  pip install tensorflow
  488  python -V
  489  conda install python=3.6.0
  490  python -V
  491  pip -V
  492  pip install tensorflow
  493  history
  494  conda install python=3.5
  495  pip -V
  496  pip install --upgrade pip
  497  pip install tensorflow
  498  pip3 -V
  499  pip3 install tensorflow
 .. macOS update
  509  pip install tensorflow
  510  tensorflow -V
  511  pip install keras
  513  python
  514  conda install pillow opencv

```

#### Jupyter notebook 연동
> 2018.10.27 작업 시간 10분 정도  
~~~ 
pip install jupyter notebook
jupyter notebook -- 실행 후 웹브라우저에 주피터노트북 실행
~~~
- [예제 파일 다운로드 및 실행](https://colab.research.google.com/github/eunji12/deep-learning-with-python-notebooks/blob/master/)
