[![MIT License][license-shield]][license-url]


<!-- TABLE OF CONTENTS -->
## Table of Contents

* [About the Project](#about-the-project)
* [Build & Installation](#build-&-Installation)
* [Usage](#usage)
* [License](#license)
* [Contact](#contact)



<!-- ABOUT THE PROJECT -->
## About The Project
최근 다양한 IoT 디바이스의 사용이 증가되고 있고, 그로 인한 보안 위협도 증가되고 있다. 베어메탈(BareMetal) IoT 디바이스의 펌웨어는 펌웨어 업데이트 파일 및 Flash De-soldering 등으로 추출이 가능 하며, 이를 역공학(Reverse Engineering) 툴을 이용한 정적 분석을 통해 실행 흐름을 분석하여 취약점을 찾을 수 있다. 이를 해결하기 위해 일반적인 컴퓨팅 시스템에는 정적 분석을 어렵게 하기 위한 다양한 소스코드 기반의 난독화 방법이 존재한다. 그러나 베어메탈 IoT 디바이스의 펌웨어 바이너리 코드 자체 를 난독화 할 수 있는 방안은 존재하지 않는다. 이를 해결하기 위해 LLVM Pass를 이용한 난독화된 바이 너리 코드를 실행하는 코드의 삽입을 통해 베어메탈 IoT 디바이스 펌웨어의 바이너리 코드를 난독화 하는 방안을 제안한다.

<!-- GETTING STARTED -->
## Build & Installation
 
1. Clone the repo
```
git clone http://khuhub.khu.ac.kr/2020-1-capstone-design1/JJS_Project1.git
```
2. Install cmake
```
brew install cmake
```
3. Create Build folder
```
mkdir ./JJS_Project1/src/build
```
4. Change directory
```
cd ./JJS_Project1/src/build
```
5. Create LLVM Clang build file
```
cmake -DLLVM_ENABLE_PROJECTS=clang -G "Unix Makefiles" ../llvm
```
6. Build
```
make
```



<!-- USAGE EXAMPLES -->
## Usage
```
JJS_Project1/src/build/bin/clang -emit-llvm -c -S source.c -o source.ll
```

<!-- LICENSE -->
## License


<!-- CONTACT -->
## Contact
2015104175 박우진 - amdx1254@khu.ac.kr <br>
2017110275 이한솔 - mardi@khu.ac.kr





<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/othneildrew/Best-README-Template.svg?style=flat-square
[contributors-url]: https://github.com/othneildrew/Best-README-Template/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/othneildrew/Best-README-Template.svg?style=flat-square
[forks-url]: https://github.com/othneildrew/Best-README-Template/network/members
[stars-shield]: https://img.shields.io/github/stars/othneildrew/Best-README-Template.svg?style=flat-square
[stars-url]: https://github.com/othneildrew/Best-README-Template/stargazers
[issues-shield]: https://img.shields.io/github/issues/othneildrew/Best-README-Template.svg?style=flat-square
[issues-url]: https://github.com/othneildrew/Best-README-Template/issues
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=flat-square
[license-url]: https://github.com/othneildrew/Best-README-Template/blob/master/LICENSE.txt
[product-screenshot]: images/screenshot.png
