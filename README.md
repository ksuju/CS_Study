## Chapter01 - 컴퓨터 구조 시작하기

### 1. 컴퓨터 구조를 알아야 하는 이유
- 컴퓨터 구조를 이해하면 코드 이외의 부분에서 문제 진단 가능 > 문제 해결 능력이 향상됨

- 성능/용량/비용을 고려하며 개발할 수 있음

 

### 2. 컴퓨터 구조의 큰 그림
* 컴퓨터가 이해하는 정보
1) 데이터 : 컴퓨터와 주고받는 정보나 컴퓨터에 저장된 정보

2) 명령어 : 데이터를 움직이고, 컴퓨터를 작동시키는 정보

** 컴퓨터란 무엇? -> "컴퓨터는 명령어를 처리하는 기계!"

 

 

#### * 컴퓨터의 네 가지 핵심 부품
#### 1) 중앙처리장치 (CPU)

- 메모리에 저장된 명령어를 읽어 들이고, 해석하고, 실행

 

** CPU 내부 구성 요소

1-1) 산술논리연산장치(ALU) :

     - 계산기!, 컴퓨터 내부에서 수행되는 대부분의 계산 담당

 

1-2) 레지스터 :

     - CPU 내부의 작은 임시 저장 장치

 

1-3) 제어장치 :

     - "제어 신호"라는 전기 신호를 내보내고, 명령어를 해석하는 장치

     - CPU가 메모리에 저장된 값을 읽고 싶을 땐 메모리를 향해 "메모리 읽기" 라는 제어 신호를 보냄

     - CPU가 메모리에 값을 저장하고 싶을 땐 메모리를 향해 "메모리 쓰기"라는 제어 신호를 보냄

 

** CPU의 동작 흐름

- 메모리가 명령어를 CPU에 전달 > 레지스터에 저장 > 제어장치가 명령어를 해석 > 메모리에 제어 신호 보냄

 

 

 

#### 2) 주기억장치 (메모리) = RAM

- 휘발성

- 현재 실행되는 프로그램의 명령어와 데이터를 저장하는 부품

- 프로그램이 실행되기 위해서는 반드시 메모리에 저장되어 있어야 함

- 메모리는 현재 실행되는 프로그램의 명령어와 데이터를 저장함

- 메모리에 저장된 값의 위치는 주소로 알 수 있음

 

#### 3) 보조기억장치

- 메모리보다 크기가 크고 전원이 꺼져도 저장된 내용을 잃지 않는, 메모리를 보조할 저장 장치

- HDD, SSD ,USB, DVD, CD-ROM 등

 

#### 4) 입출력장치

- 컴퓨터 외부에 연결되어 컴퓨터 내부와 정보를 교환하는 장치

- 마이크, 모니터, 키보드 등

 

 

* 메인보드와 시스템 버스 ( 버스 = 통로 )
1) 메인보드 :

- 위에 설명한 컴퓨터의 핵심 부품들이 연결되는 부품

- 메인보드 내부에 있는 버스라는 통로를 통해 부품간 정보를 주고받음

 

2) 시스템 버스 :

- 네가지 핵심 부품들이 서로 정보를 주고받는 통로

2-1) 주소 버스 : RAM 주소의 통로

2-2) 데이터 버스 : 데이터 통로

2-3) 제어 버스 : 제어 신호 통로


## Chapter02 - 0과 1로 숫자를 표현하는 방법


1바이트 = 8비트

 

### 이진법
이진수의 음수 표현
2의 보수를 구해 그 값을 음수로 간주한다!

 

#### "모든 0과 1을 뒤집고, 거기에 1을 더한 값" 이 보수다!

 

ex) 1011의 음수는?

1. 모든 수를 뒤집음 -> 0100

2. 거기에 1을 더함 -> 0101

 

### 플래그 :

- 숫자만 보고는 이진수가 음수인지 양수인지 알 수 없기에 사용함! > 04장에서 정리

 

 

### 십육진법
십진수

0 - 1 - 2 - 3 - 4 - 5 - 6 - 7 - 8 - 9 - 10 - 11 - 12 - 13 - 14 - 15 - 16 - 17 ~~

 

십육진수

0 - 1 - 2 - 3 - 4 - 5 - 6 - 7 - 8 - 9 - A - B - C - D - E - F - 10 - 11 - 12 ~~

 

* 십육진수를 사용하는 이유?

- 이진수를 십육진수로, 십육진수를 이진수로 변환하기 쉽기 때문에!

 

십육진수를 이진수로 변환하기 :

십육진수 한 글자를 4비트의 이진수로 간주하면 됨!

 

1A2B를 변환하면?

1 = 0001

A = 1010

2 = 0010

B = 1011

 

0001101000101011 = 1A2B

 

 

### 이진수를 십육진수로 변환하기 :

반대로! 이진수 숫자를 네 개씩 끊고, 하나의 십육진수로 변환한 뒤 그대로 이어 붙인다

 

11010101을 변환하면?

1101 = D

0101 = 5

 

11010101 = D5



### 0과 1로 문자를 표현하는 방법
문자 집합 :
- 컴퓨터가 인식할 수 있는 문자의 모음, 문자 집합에 속한 문자를 인코딩하여 0과 1로 표현 가능

 

#### 인코딩 :
- 문자를 컴퓨터가 이해할 수 있는 0과 1로 변환하는 과정

 

#### 디코딩 :
- 0과 1로 표현된 문자 코드를 사람이 읽을 수 있는 문자로 변환하는 과정

 

#### EUC-KR :
- 한글을 2바이트 크기로 인코딩할 수 있는 완성형 인코딩 방식
- 다만, 한글 전체를 표현하기는 힘들다 (쀍, 믜 같은 글자는 표현 불가능)

 

#### 유니코드와 UTF-8
- EUC-KR의 모든 한글을 표현할 수 없다는 단점을 보완하는 인코딩 방식
- 유니코드는 현대 문자를 표현할 때 가장 많이 사용되는 표준 문자 집합이다!
- UTF-8은 유니코드 문자의 인코딩 방식 중 하나, UTF-8, 16, 32가 있음


## Chapter03 - 명령어

### **1\. 소스 코드와 명령어**

\- 모든 소스 코드는 컴퓨터 내부에서 명령어로 변환됨!

#### **\* 고급 언어와 저급 언어**

**1) 고급 언어 :**

\- 사람을 위한 언어

**2) 저급 언어 :**

\- 컴퓨터가 직접 이해하고 실행할 수 있는 언어, 컴퓨터는 오직 저급언어만 이해하고 실행 가능함

#### **\* 저급 언어의 종류**

**1) 기계어 :**

\- 0과 1의 명령어 비트로 이루어진 언어

\- 보통은 2진수로 표현, 가독성을 위해 16진수로 표현하기도 함

**2) 어셈블리어**

\- 기계어를 읽기 편한 형태로 번역한 언어

\- 임베디드, 게임, 정보 보안 분야 등에서 많이 사용됨

#### **\* 고급 언어의 종류, 컴파일 언어와 인터프리터 언어 :**

고급 언어가 저급 언어로 변환되는 방식

**1) 컴파일 방식 (컴파일 언어)**

\- 컴파일러에 의해 **소스 코드 전체**가 저급 언어로 변환되어 실행되는 고급 언어

\- 대표적으로 C가 있음

\- 컴파일러란 컴파일을 수행해주는 도구

\- 컴파일러를 통해 저급 언어로 변환된 코드를 목적 코드라고 함

**2) 인터프리트 방식 (인터프리터 언어)**

\- 대표적으로 Python이 있음

\- 소스 코드를 **한 줄씩 차례로** 저급 언어로 변환

\- 한 줄씩 코드를 실행하기 때문에 N번째 줄에 문법 오류가 있어도, N-1 번째 줄까지는 올바르게 인터프리트 됨

\- 일반적으로 컴파일 언어보다 느리다!

현대의 많은 프로그래밍 언어는 컴파일 방식과 인터프리트 방식을 혼합해서 사용한다!

참고)

목적 파일 vs 실행 파일

\- 목적코드로 이루어진 목적 파일

\- 실행 코드로 이루어진 실행 파일

\- 목적 코드가 실행 파일이 되기 위해서는 '링킹' 이라는 작업을 거쳐야 함

### **\* 연산 코드와 오퍼랜드 :**

**명령어는 연산 코드와 오퍼랜드로 구성되어 있음**

하나의 명령어는 아래와 같이 표현될 수 있음

연산 코드가 담기는 영역 : 연산 코드 필드

오퍼랜드가 담기는 영역 : 오퍼랜드 필드

| **연산 코드** | **오퍼랜드** |
| --- | --- |

**1) 연산 코드 : 명령어가 수행할 연산 (= 연산자)**

기본적인 연산 코드 유형

\- 데이터 전송

\- 산술/논리 연산

\- 제어 흐름 변경

\- 입출력 제어

**2) 오퍼랜드 : 연산에 사용할 데이터가 저장된 위치 (= 피연산자)**

\- 메모리 주소나 레지스터 이름이 담긴다

\- **주소 필드**라고 부른다

\- 명령어 안에 하나도 없을 수도 있고, 여러 개 있을 수도 있음

\- 주소를 지정함으로서 메모리를 더 효율적으로 사용 가능함

\- 오퍼랜드에 담긴 주소, 즉, 연산의 대상이 되는 데이터가 저장된 위치를 **유효 주소**라고 함

**2-1) 주소 지정 방식**

\- 오퍼랜드 필드에 데이터가 저장된 위치를 명시할 때, 연산에 사용할 데이터 위치를 찾는 방법

\- 즉시 주소 지정 방식 :

가장 간단함, 데이터를 오퍼랜드 필드에 직접 명시하는 방법

\- 직접 주소 지정 방식 :

오퍼랜드 필드에 유효 주소를 직접적으로 명시

\- 간접 주소 지정 방식 :

유효 주소의 주소를 오퍼랜드 필드에 명시함, 다만 두 번의 메모리 접근이 필요해서 느림

\- 레지스터 주소 지정 방식 :

직접 주소 지정 방식과 비슷, 연산에 사용할 데이터를 저장한 레지스터를 오퍼랜드 필드에 직접 명시

\- 레지스터 간접 주소 지정 방식 :

연산에 사용할 데이터를 메모리에 저장하고, 그 주소를 저장 한 레지스터를 오퍼랜드 필드에 명시

**\* 스택과 큐**

스택 : LIFO

\- 후입 선출

큐 : FIFO

\- 선입 선출


## Chapter04 - CPU의 작동 원리

### **1\. ALU와 제어장치**

\- ALU : CPU 내부에서 계산을 담당

\- 제어장치 : 명령어를 읽어 들이고 해석

\- 레지스터 : 작은 임시 저장 장치

#### **\* ALU :**

ALU는 계산하는 부품!

ALU가 계산을 하기 위해서는 피연산자와 수행할 연산이 필요함!

(ex: 1+2를 계산할 때 1과 2라는 피연산자, 더하기라는 연산이 필요)

**\- ALU가 받아들이는 정보**

ALU는 **레지스터**를 통해 **피연산자**를 받아들이고, **제어장치**로부터 수행할 연산을 알려주는 **제어신호**를 받아들임

**\- ALU가 내보내는 정보**

**1) 계산 결과 (결과값)**

ALU는 **결과값**을 **메모리가 아닌 레지스터에 우선 저장**함

왜?

CPU가 직접 메모리에 자주 접근하게 되면 프로그램 실행 속도를 늦출 수 있기 때문에,

빠르게 저장 가능한 레지스터에 결과값을 저장한 후 레지스터가 메모리에 그 값을 전달

**2) 플래그 :**

연산 결과에 대한 추가적인 상태 정보,

CPU가 프로그램을 실행하는 도중 반드시 기억해야 하는 일종의 참고 정보

플래그 레지스터에 저장되어 추가 정보를 내보냄!

#### **\* 제어장치 :**

제어 신호를 내보내고, 명령어를 해석하는 부품!

**제어 신호 :**

컴퓨터 부품들을 관리하고 작동시키기 위한 일종의 전기 신호

\- 제어장치가 받아들이는 정보

1) 제어장치는 클럭 신호를 받아들인다.

2) 제어장치는 '해석해야 할 명령어'를 받아들인다.

3) 제어장치는 플래그 레지스터 속 플래그 값을 받아들인다.

4) 제어장치는 시스템 버스, 그 중에서 제어 버스로 전달된 제어 신호를 받아들인다.

### **2\. 레지스터**

\- **프로그램 속 명령어와 데이터는 실행 전후로 반드시 레지스터에 저장**된다!

\- 레지스터에 저장된 값만 잘 관찰해도 프로그램의 실행 흐름을 파악할 수 있음

**\* 반드시 알아야 할 레지스터**

1) 프로그램 카운터

\- 메모리에서 가져올 명령어의 주소, 메모리에서 읽어 들일 명령어의 주소를 저장함

2) 명령어 레지스터

\- 방금 메모리에서 읽어 들인 명령어를 저장함

3) 메모리 주소 레지스터

\- 메모리의 주소를 저장

\- CPU가 읽어 들이고자 하는 주소 값을 주소 버스로 보낼 때 메모리 주소 레지스터를 거치게 됨

4) 메모리 버퍼 레지스터

\- 메모리와 주고받을 값 (데이터와 명령어)을 저장하는 레지스터

5) 플래그 레지스터

\- ALU 연산 결과에 따른 플래그를 저장하는 레지스터

6) 범용 레지스터

\- 일반적인 상황에서 자유롭게 사용할 수 있는 레지스터, 데이터와 주소를 모두 저장 가능!

7) 스택 포인터

\- 스택의 꼭대기를 가리키는 레지스터. 즉, 스택에 마지막으로 저장한 값의 위치를 저장하는 레지스터

8) 베이스 레지스터

\- **'기준 주소'**

\- 유효 주소를 얻는 방식중 하나, 오퍼랜드와 베이스 레지스터의 값을 더하여 유효 주소를 얻는다.

\- 베이스 레지스터 속 기준 주소로부터 얼마나 떨어져 있는 주소에 접근할 것인지를 연산하여 유효 주소 얻는

'베이스 레지스터 주소 지정 방식' 에 사용된다.

### **3\. 명령어 사이클과 인터럽트**

#### **\* 명령어 사이클 :**

CPU가 하나의 명령어를 처리하는 정형화된 흐름

1단계,

**인출 사이클** : 메모리에 있는 명령어를 CPU로 가져오는 단계

2단계,

**실행 사이클** : CPU로 가져온 명령어를 실행하는 단계

3단계,

**간접 사이클** : 간접 주소 지정 방식과 같은 방법을 통해 CPU로 명령어를 가져왔을 때 이를 처리하는 단계

#### **\* 인터럽트 :**

CPU가 정해진 흐름에 따라 명령어를 처리하는 중 흐름이 끊어지는 상황

CPU의 작업을 방해하는 신호!

#### **인터럽트의 종류**

**1) 동기 인터럽트 :**

CPU에 의해 발생하는 인터럽트! > **예외**라고 부른다.

\* 예외가 발생하면 CPU는 하던 일을 중단하고 해당 예외를 처리함.

이 때 **폴트**와 **트랩**이라는 개념이 등장함.

**폴트 :**

예외를 처리한 직후, **예외가 발생한 명령어부터 실행을 재개**하는 예외

**트랩 :**

예외를 처리한 직후, **예외가 발생한 다음 명령어부터 실행을 재개**하는 예외

주로 디버깅할때 사용함.

**중단:**

심각한 오류를 발견했을 때, CPU가 실행 중인 프로그램을 강제로 중단하는 것

**2) 비동기 인터럽트**

주로 입출력장치에 의해 발생하는 인터럽트. > 일반적으로 그냥 인터럽트라고 말함

**3) 하드웨어 인터럽트**

알림과 같은 인터럽트!

**플래그 레지스터**의 **인터럽트 플래그**가 **활성화**되어 있어야 이를 받을 수 있음.

인터럽트 서비스 루틴 (= 인터럽트 핸들러) :

인터럽트를 처리하기 위한 프로그램, CPU가 인터럽트 요청을 받아들이면, 실행된다!

인터럽트 벡터를 통해 수많은 인터럽트 서비스 루틴을 구분함


## Chapter05 - CPU 성능 향상 기법

### **1\. 빠른 CPU를 위한 설계 기법**

\* 클럭 :

Hz단위로 측정함.

일반적으로 클럭 성능이 높으면 성능도 좋음, 예외 존재

\* 코어와 멀티코어 :

코어란 명령어를 처리하는 부품

일반적으로 코어가 늘어나면 성능이 좋음, 예외 존재

\* 스레드와 멀티스레드 :

스레드란 실행 흐름의 단위!, 명령어를 실행하는 단위!

하드웨어적 스레드와 소프트웨어적 스레드로 나눌 수 있음.

1) 하드웨어적 스레드

\- 하나의 코어가 동시에 처리하는 명령어 단위

\- 하나의 코어로 여러 명령어를 동시에 처리하는 것을 멀티스레드라고 함

2) 소프트웨어적 스레드

\- 하나의 프로그램에서 독립적으로 실행되는 단위

3) 멀티스레드

\- 하나의 코어로 여러 개의 명령어를 동시에 실행할 수 있는 CPU

### **2\. 명령어 병렬 처리 기법**

\- 명령어를 동시에 처리하여 CPU를 쉬지 않고 작동시키는 기법

\- 명령어 파이프 라이닝, 슈퍼스칼라, 비순차적 명령어 처리가 있음

1) 명령어 파이프라인 :

\- 명령어 인출 > 해석 > 실행 > 저장 의 순서

\- 순차적으로 처리하기에 높은 성능을 기대 가능

\- 성능 향상에 실패하는 **파이프라인 위험**이 존재함

\* 파이프라인 위험

a) 데이터 위험 :

명령어 간 데이터 의존성에 의해 발생함

b) 제어 위험 :

프로그램 카운터의 갑작스러운 변화에 의해 발생함

c) 구조적 위험 (= 지원 위험) :

명령어들을 겹쳐 실행하는 과정에서 서로 다른 명령어가 동시에 ALU, 레지스터와 같은

CPU 부품을 사용하려고 할 때 발생함

2) 슈퍼스칼라 :

CPU 내부에 여러 개의 명령어 파이프라인을 포함한 구조

3) 비순차적 명령어 처리 :

순서를 바꿔 실행해도 무방한 명령어를 먼저 실행하여 명령어 **파이프라인이 멈추는 것을 방지**

### **3\. CISC와 RISC :**

ISA를 기반으로 설계된 CPU 언어, CPU 마다 다를 수 있음

명령어 병렬 처리 기법을 도입하기 유리하도록 만듦

1)  CISC :

\- 가변 길이 명령어를 활용함

\- 적은 수의 명령어로 프로그램을 동작, 메모리 공간을 절약할 수 있다는 장점이 있음

\- 적지만 복잡한 명령어 때문에 명령어의 크기와 실행되기까지의 시간이 일정하지 않은 단점

2) RISC :

\- CISC에 비해 명령어의 종류가 적고, 간결함 > 고정 길이 명령어를 활용함

\- 명령어 파이프라이닝에 최적화됨

\- 프로그램을 이루는 명령어의 수가 많다는 단점****


## Chapter06 - 메모리와 캐시 메모리

### **1\. RAM의 특징과 종류**

**\* RAM의 특징 :**

\- 휘발성 저장 장치이다!

**\* RAM의 용량과 성능**

\- 용량이 크면, 많은 프로그램을 동시에 빠르게 실행하는 데 유리함.

\- 용량이 필요 이상으로 크면 성능에는 영향 없음

**\* RAM의 종류**

1) DRAM

\- 일반적으로 메모리로써 사용하는 RAM

\- 소비 전력이 낮고, 저렴, 집적도가 높아 대용량으로 설계하기 용이함

2) SRAM

\- Static RAM

\- 저장된 데이터가 변하지 않는 RAM

\- 소비 전력이 크고, 비쌈

\- 캐시 메모리에서 주로 사용됨

3) SDRAM

\- 클럭 신호와 동기화된, 발전된 형태의 DRAM

\- 즉, 타이밍에 맞춰 CPU와 정보를 주고받을 수 있음

4) DDR SDRAM

\- 최근 가장 흔히 사용되는 RAM

\- 대역폭을 넓혀 속도를 빠르게 만든 SDRAM

\- DDR3, DDR4, DDR5 ~~

### **2\. 메모리의 주소 공간**

**\* 주소의 종류**

**1) 물리 주소**

\- 메모리 하드웨어가 사용하는 주소

\- 실제로 저장된 하드웨어상의 주소를 의미함

**2) 논리 주소**

\- CPU와 실행 중인 프로그램이 사용하는 주소

\- 실행 중인 프로그램 각각에게 부여된 0번지부터 시작되는 주소를 의미함

**\* 메모리 관리 장치 (MMU)**

\- CPU와 메모리의 상호작용을 위해, 논리주소와 물리주소간의 변환을 담당

\- 프로그램의 첫 물리 주소를 베이스 레지스터에 저장

\* 한계 레지스터

\- 실행 중인 프로그램의 논리 주소의 최대 크기를 저장함.

\* 저장 장치 계층 구조

\- CPU와 가까운 저장 장치는 빠르고, 멀리 있는 저장 장치는 느리다.

\- 속도가 빠른 저장 장치는 저장 용량이 작고, 가격이 비싸다.

### **3\. 캐시 메모리**

\- CPU가 메모리에 접근하는 시간을 줄여줌!

\- SRAM 기반의 저장 장치

\- 코어와 가까운 순으로 L1, L2, L3 캐시 메모리로 나뉜다.

\* 참조 지역성 원리

\- CPU는 최근에 접근했던 메모리 공간에 다시 접근하려는 경향이 있다. (= **시간 지역성**)

\- CPU는 접근한 메모리 공간 근처를 접근하려는 경향이 있다. (= **공간 지역성**)

1) 캐시 히트

\- 자주 사용될 것으로 예측한 데이터가 실제로 들어맞아 메모리 내 데이터가 CPU에서 활용되는 경우

2) 캐시 미스

\- 예측이 틀려서 메모리에서 필요한 데이터를 직접 가져와야 하는 경우

3) 캐시 적중률

캐시 히트 횟수 / (캐시 히트 횟수 + 캐시 미스 횟수)


## Chapter07 - 보조기억장치

### **1\. 다양한 보조기억장치**

#### **\* 하드 디스크**

1) 탐색 시간 :

접근하려는 데이터가 저장된 트랙까지 헤드를 이동시키는 시간

2) 회전 지연 :

헤드가 있는 곳으로 플래터를 회전시키는 시간

3) 전송 시간 :

하드 디스크와 컴퓨터 간에 데이터를 전송하는 시간

#### **\* 플래시 메모리**

**1) NAND 플래시 메모리 :**

NAND 연산을 수행, 대용장 저장 장치로 많이 사용됨

#### **\* 플래시 메모리의 종류**

a. SLC 타입

\- 한 셀에 1비트를 저장 가능 > 0과 1 두개의 정보를 표현 할 수 있다!

\- 수명이 제일 길다, 그러나 용량 대비 가격이 높다.

\- 고성능의 빠른 저장 장치가 필요한 경우에 사용되는 타입이다.

b. MLC 타입

\- 한 셀에 2비트를 저장 가능 > 네 개의 정보를 표현할 수 있음

\- SLC 타입보다 속도와 수명은 떨어지지만, 대용량화하기 유리함

c. TLC 타입

\- 한 셀당 3비트를 저장 가능 > 여덟 개의 정보를 표현할 수 있다.

\- 수명과 속도는 제일 떨어지지만, 용량 대비 가격이 제일 저렴함

#### **\* 플래시 메모리의 단위**

다이 > 플레인 > 블록 > 페이지 > 셀

\- 다이가 제일 큰 단위, 셀이 가장 작은 단위

2) NOR 플래시 메모리 :

NOR 연산을 수행하는 회로 기반으로 만들어진 메모리

### **2\. RAID의 정의와 종류**

#### **\* RAID란? :**

\- 데이터의 안전성 혹은 높은 성능을 위해 여러 개의 물리적 보조기억장치를

하나의 논리적 보조기억장치처럼 사용하는 기술!

\- 하드 디스크와 SSD를 사용하는 기술임

#### **\* RAID의 종류**

\- RAID 레벨로 나뉜다

\- 기본적으로 0에서 6까지 레벨이 있다

\- 파생된 10, 50 레벨 등이 있다

1) RAID 0

\- 데이터를 여러 개의 보조기억장치에 단순히 나누어 저장함

\- 저장된 정보가 안전하지 않다는 단점 존재

2) RAID 1

\- 복사본을 만드는 방식, 미러링이라고도 부름

\- 복구가 매우 간단하다는 장점이 있음

\- 하드 디스크 개수가 한정되었을 때 사용 가능한 용량이 적어지는 단점이 있음

3) RAID 4

\- RAID 1처럼 완전한 복사본을 만드는 대신, **패리티 비트**를 둠.

\- 패리티 비트란? 오류를 검출하고 복구하기 위한 정보

\- RAID 1보다 적은 하드 디스크로도 데이터를 안전하게 보관 가능!

\- 새로운 데이터가 저장될 때 마다 패리티 비트를 쓰기 때문에,

패리티를 저장하는 장치에 병목 현상이 일어날 수 있음

4) RAID 5

\- 패리티 정보를 분산하여 저장하는 방식

\- RAID 4의 문제인 병목 현상을 해소함

5) RAID 6

\- 기본적으로는 RAID 5와 같으나, 서로 다른 두 개의 패리티를 두는 방식

\- 패리티가 두개이기 때문에 정보를 더욱 안전하게 보관 가능

\- 속도는 조금 느리다


## Chapter08 - 입출력장치

### **1\. 장치 컨트롤러와 장치 드라이버**

#### **\* 장치 컨트롤러**

(= 입출력 제어기, 입출력 모듈)

**1) 데이터 버퍼링 :**

버퍼에 데이터를 모았다가 한꺼번에 내보내거나, 데이터를 한 번에 많이 받아 조금씩 내보내는 방법

(버퍼 = 임시 저장 공간)

**2) 장치 컨트롤러의 내부**

\- 데이터 레지스터 :

CPU와 입출력장치 사이에 주고받을 데이터가 담기는 레지스터

\- 상태 레지스터 :

입출력장치의 상태 정보가 저장됨

\- 제어 레지스터 :

입출력장치가 수행할 내용에 대한 제어 정보와 명령을 저장

#### **\* 장치 드라이버 :**

장치 컨트롤러가 컴퓨터 내부와 정보를 주고받을 수 있게 하는 프로그램

#### **2\. 다양한 입출력 방법**

**\- 프로그램 입출력 :**

프로그램 속 명령어로 입출력장치를 제어하는 방법!

메모리 맵 입출력, 고립형 입출력 방식이 있음

**1) 메모리 맵 입출력 :**

메모리에 접근하기 위한 주소 공간과 입출력장치에 접근하기 위한 주소 공간을 하나의 주소 공간으로 간주하는 방법

**2)  고립형 입출력 :**

메모리를 위한 주소 공간과 입출력장치를 위한 주소 공간을 분리하는 방법

**\- 인터럽트 기반 입출력 :**

말 그대로 CPU 인터럽트를 기반으로 하는 입출력

**\* PIC (프로그래머블 인터럽트 컨트롤러) :**

여러 장치 컨트롤러에 연결되어 장치 컨트롤러에서 보낸 하드웨어 인터럽트 요청들의 우선순위를 판별한 뒤,

CPU에 지금 처리해야 할 하드웨어 인터럽트는 무엇인지를 알려주는 장치

**\- DMA 입출력 :**

앞선 두 가지 방식의 입출력 방식과는 달리,

CPU를 거치지 않고, 직접 메모리에 접근할 수 있는 입출력 기능

**\- 입출력 버스 :**

입출력장치와 컴퓨터 내부를 연결 짓는 통로로, 입출력 작업 과정에서 시스템 버스 사용 횟수를 줄여준다.


## Chapter09 - 운영체제 시작하기

### **1\. 운영체제를 알아야 하는 이유**

\* 운영체제란?

\- 실행할 프로그램에 필요한 자원을 할당하고, 프로그램이 올바르게 실행되도록 돕는 프로그램

\- 항상 컴퓨터가 부팅될 때 메모리 내 **커널 영역**이라는 공간에 따로 적재되어 실행됨

\- 커널 영역을 제외한 나머지 영역, 사용자가 이용하는 응용 프로그램이 적재되는 영역은 **사용자 영역**

\- 운영체가가 없다면 개발자가 하드웨어를 조작하는 코드까지 직접 작성해야함

### **2\. 운영체제의 큰 그림**

**\* 커널**

\- 운영체제의 핵심 서비스를 담당하는 부분

사용자 인터페이스는 커널에 포함되지 않은 서비스임 CLI, GUI 등......

\* 이중 모드와 시스템 호출

1) 이중 모드 : 

CPU가 명령어를 수행하는 모드는 **사용자 모드와 커널 모드**로 구분하는 방식

1-1) 사용자 모드 :

\- **운영체제 서비스를 제공받을 수 없는 실행 모드**

\- 즉, 커널 영역의 코드를 실행할 수 없는 모드

\- 일반적인 응용 프로그램은 사용자 모드로 실행됨!

1-2) 커널 모드 :

\- **운영체제 서비스를 제공받을 수 있는 실행 모드**

\- 즉, 커널 영역의 코드를 실행할 수 있는 모드

2) 시스템 호출 :

\- 운영체제 서비스를 제공받기 위한 요청

\- 일종의 인터럽트임, 소프트웨어 인터럽트라고 부른다.

### **3\. 운영체제의 핵심 서비스**

**\* 프로세스 관리**

\- 프로세스란? 실행 중인 프로그램!

\- 일반적으로 **하나의 CPU는 하나의 프로세스만 실행이 가능**하다

**\* 자원 접근 및 할당**

\- CPU 스케줄링을 통해 하나의 프로세스가 얼마나 오래 CPU를 이용하게 할지를 결정함

\- 메모리는 프로세스가 적재되는 공간

**\* 파일 시스템 관리**
