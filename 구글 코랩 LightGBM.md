# 구글 코랩에서 LightGBM 사용



코랩 ipynb 파일에서 런타임 유형을 **GPU**로 바꾼 뒤 다음 코드 실행

```
!git clone --recursive https://github.com/Microsoft/LightGBM # github 소스코드 다운로드

%cd /content/LightGBM # 소스코드 파일이 있는 디렉토리로 이동

!mkdir build
!cmake -DUSE_GPU=1
!make -j$(nproc)
!sudo apt-get -y install python-pip
!sudo -H pip install setuptools pandas numpy scipy scikit-learn -U
%cd /content/LightGBM/python-package/
!sudo python setup.py install --precompile
```

\+ 안된다면 런타임 다시시작



참고 : <https://somjang.tistory.com/entry/Ensemble-Colab%EC%97%90%EC%84%9C-LightGBM-%EC%82%AC%EC%9A%A9%ED%95%98%EA%B8%B0>
