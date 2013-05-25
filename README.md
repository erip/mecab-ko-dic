# mecab-ko-dic 소개

[mecab-ko-dic](https://bitbucket.org/bibreen/mecab-ko-dic)은 오픈 소스 형태소 분석 엔진인 [MeCab](http://mecab.googlecode.com/svn/trunk/mecab/doc/index.html)을 사용하여, 한국어 형태소 분석을 하기 위한 프로젝트입니다. 말뭉치 학습과 사전 목록 일부는 [21세기 세종계획](http://www.sejong.or.kr/)의 성과물을 사용하였습니다.

형태소 분석 학습에 사용된 말뭉치는 다음과 같습니다.

  - 일상대화_삼십대 - 5CT_0017
  - 강의_언어와사회 - 5CT_0048
  - 독백_여행이야기#2 - 6CT_0013
  - 주제대화_광고토론 - 8CT_0039
  - 조선일보 경제(90) - BTAA0002
  - 조선일보 사설 - BTAA0004
  - 조선일보 과학(93) - BTAA0013
  - 수필공원 94 봄 - BTBF0265
  - 슬픈 시인의 바다 - BTEO0085
  - 해남 가는 길 - BTEO0088
  - 미학 오디세이 - BTHO0367
  - 한국의 마케팅 사례 - BTHO0425

mecab-ko-dic은 [아파치 라이센스 2.0](http://www.apache.org/licenses/LICENSE-2.0.html)에 따라 소프트웨어를 사용, 재배포 할 수 있습니다.

# 설치 및 사용

mecab-ko-dic을 설치하고 사용하기 위해서 다음과 같은 작업이 필요합니다. 모든 작업은 Linux 기준입니다. 양해바랍니다.

## mecab-ko 설치

[mecab-ko](https://bitbucket.org/bibreen/mecab-ko)는 한국어의 특성에 맞는 기능이 추가된 MeCab의 fork 프로젝트입니다.

[mecab-ko 다운로드 페이지](https://bitbucket.org/bibreen/mecab-ko/downloads) 에서 mecab-ko의 소스를 다운 받고 설치합니다.
tar.gz를 압축 해제하시고 일반적인 자유 소프트웨어와 같은 순서로 설치할 수 있습니다.

    :::text
    $ tar zxfv mecab-XX-ko-XX.tar.gz
    $ cd mecab-XX-ko-XX
    $ ./configure 
    $ make
    $ make check
    $ su
    # make install

자세한 내용은 다음의 URL을 참조하시기 바랍니다.

  - [mecab-ko](https://bitbucket.org/bibreen/mecab-ko)
  - [MeCab 홈페이지](http://mecab.googlecode.com/svn/trunk/mecab/doc/index.html)

## mecab-ko-dic 다운로드

[mecab-ko-dic 다운로드 페이지](https://bitbucket.org/bibreen/mecab-ko-dic/downloads) 에서 mecab-ko-dic의 최신 버전을 다운 받습니다.

## mecab-ko-dic 설치

tar.gz를 압축 해제하시고 일반적인 자유 소프트웨어와 같은 순서로 설치할 수 있습니다.
기본으로 /usr/local/lib/mecab/dic/mecab-ko-dic에 설치됩니다.

    :::text
    $ tar zxfv mecab-ko-dic-XX.tar.gz
    $ cd mecab-ko-dic-XX
    $ ./configure 
    $ make
    $ su
    # make install

## 사용

다음과 같이 mecab을 실행하여 한국어 형태소 분석 결과를 보실 수 있습니다. 

    :::text
    $ mecab -d /usr/local/lib/mecab/dic/mecab-ko-dic
    mecab-ko-dic은 MeCab을 사용하여, 한국어 형태소 분석을 하기 위한 프로젝트입니다.
    mecab     SL,*,*,*,*,*,*,*
    -         SY,*,*,*,*,*,*,*
    ko        SL,*,*,*,*,*,*,*
    -         SY,*,*,*,*,*,*,*
    dic       SL,*,*,*,*,*,*,*
    은        JX,T,은,*,*,*,*,*
    MeCab     SL,*,*,*,*,*,*,*
    을        JKO,T,을,*,*,*,*,*
    사용      NN,T,사용,*,*,*,*,*
    하        XSV,F,하,*,*,*,*,*
    여        EC,F,여,*,*,*,*,*
    ,         SY,*,*,*,*,*,*,*
    한국어    NN,F,한국어,Compound,*,*,한국+어,한국/NN/1/1+한국어/Compound/0/2+어/NN/1/1
    형태소    NN,F,형태소,Compound,*,*,형태+소,형태/NN/1/1+형태소/Compound/0/2+소/NN/1/1
    분석      NN,T,분석,*,*,*,*,*
    을        JKO,T,을,*,*,*,*,*
    하        VV,F,하,*,*,*,*,*
    기        ETN,F,기,*,*,*,*,*
    위한      VV+ETM,T,위한,Inflect,VV,ETM,위하/VV+ㄴ/ETM,*
    프로젝트  NN,F,프로젝트,*,*,*,*,*
    입니다    VCP+EF,F,입니다,Inflect,VCP,EF,이/VCP+ㅂ니다/EF,*
    .         SF,*,*,*,*,*,*,*
    EOS

mecab-ko-dic에서 사용하는 사전 형식이나 품사 태그에 대한 정보는 다음의 페이지에서 보실 수 있습니다.

  - [mecab-ko-dic 품사 태그 설명](https://docs.google.com/spreadsheet/ccc?key=0ApcJghR6UMXxdEdURGY2YzIwb3dSZ290RFpSaUkzZ0E&usp=sharing)

## 기타
  - 형태소 분석기 학습에 사용된 말뭉치(corpus)는 저작권이 있기 때문에 배포가 불가능합니다.
  - 단어 추가 방법은 다음의 URL에서 확인하실 수 있습니다.
    [MeCab 단어 추가 방법](http://mecab.googlecode.com/svn/trunk/mecab/doc/dic.html) \(일본어\)
