---
{"dg-publish":true,"permalink":"/nuguna-blog/fpga-start/","title":"FPGA 첫 포스팅"}
---

이 분야를 공부하면서 간략하게 정리를 해볼까 합니다.

**FPGA**
**F**ield **P**rogrammable **G**ate **A**rray의 약자
여기까지 왔다면
당신은 하드웨어와 소프트웨어 사이 어딘가에서 업무를 하고 있을 가능성이 매우 높다.

FPGA 약자의 뜻을 살펴보면 아래와 같다.
Field : 현장
Programmable : 프로그램적으로 변경 가능한
Gate Array : 논리회로 묶음 --> 전기적인 집적회로
--> **수정 가능한 전기 회로** 라고 보면 될 듯...

크게 2개의 회사가 있습니다.
Xilinx(자일링스) : 2022년 AMD 인수
Altera(알테라) : 2015년 Intel 인수, 2024년 재분사

시장 규모 : 2023년 약 12조원
출처 : [e4ds 유투브 채널](https://www.youtube.com/watch?v=71ynkpNSQPI)

시장 점유율 : Xilinx 52%, Intel 35% (2019년)
출처 : [설계독학맛비 - 인프런 강의](https://www.inflearn.com/course/%EC%8B%A4%EC%A0%84-%EA%B0%80%EC%86%8D%EA%B8%B0-%EC%84%A4%EA%B3%84)

1위 업체인 AMD(구. 자일링스) 칩(Chip) 종류
<img src="/Attachments/캡처3.jpg"/>
![캡처3.jpg](/img/user/nuguna-Blog/Attachments/%EC%BA%A1%EC%B2%983.jpg)
출처 : [xilinx 홈페이지](https://www.xilinx.com/video/fpga/cost-optimized-fpga-soc-portfolio.html)

AMD FPGA에 접근하게 되면 알게 되는 프로그램은 다음과 같다.
Vivado(비바도), ISE(**I**ntegrated **S**oftware **E**nvironment) Design Suite
Vitis(바이티스),  Vitis AI, Vitis HLS
SDK(**S**oftware **D**evelopment **K**its)
Petalinux(페타리눅스)
출처 : [xilinx 홈페이지](https://www.xilinx.com/support/download.html)
![Pasted image 20240913160005.png](/img/user/nuguna-Blog/Attachments/Pasted%20image%2020240913160005.png)

**Vivado vs ISE**
최근의 FPGA 칩(Chip)에서는 PS(Processing System)영역과 PL(Programmable Logic)으로 크게 구분되고, PL부분인 하드웨어를 설계하기 위한 프로그램
- ISE 14.7 Windows 10이 마지막(2020년 2월)
윈도우 OS(Operating System)에 설치시 가상화(VM, Virtual Machine)로 설치됨
Spartan(스파르탄)부터 ~ Zynq(징크)까지
![2.png|400](/img/user/nuguna-Blog/Attachments/2.png)
![1.jpg|400](/img/user/nuguna-Blog/Attachments/1.jpg)

- Vivado 2024.1
윈도우, Linux(리눅스) OS에 따라 설치 가능 (2023.2버전에서 설치시 300GB 이상의 저장공간 필요)
Spartan 6부터 ~ Zynq UltraScale+까지
![스크린샷 2024-09-13 18-08-35.png|400](/img/user/nuguna-Blog/Attachments/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202024-09-13%2018-08-35.png)
출처 : [mouessee 글](https://740280.tistory.com/16)
출처 : [나무위키](https://namu.wiki/w/XILINX)

**Vitis vs SDK**
Vivado 2019.2부터 SDK가 빠지고, Vitis를 사용하게 되네요.
출처 : [Baram 블로그](https://m.blog.naver.com/chcbaram/222097170729)

**Petalinux**
시스템 부팅부터 실행까지, Linux 기반 제품의 개발을 쉽게 해줌.
한정된 장치들의 자원으로부터 여러 가지를 일을 동시에 실행하는 Linux OS 사용부터 어플(App, Application)까지 사용 가능 함.
출처 : [amd.com](https://www.amd.com/en/products/software/adaptive-socs-and-fpgas/embedded-software/petalinux-sdk.html)

**접근 방법**
- 개발하고자 하는 목표에 따라서
1. 하드웨어 개발
2. 하드웨어, 소프트웨어 개발
3. 하드웨어, 소프트웨어, 드라이버, 어플리케이션 개발
4. 하드웨어, 소프트웨어, AI 개발
![캡처2.jpg|400](/img/user/nuguna-Blog/Attachments/%EC%BA%A1%EC%B2%982.jpg)
출처 : [hackster.io](https://www.hackster.io/whitney-knitter/amd-xilinx-vivado-vitis-hls-y2k22-patch-application-guide-6af1cd)

- 개발된 자료를 보고 배울 때
1. ISE vs Vivado
2. SDK vs Vitis
3. Linux Kenel vs Petalinux

ISE
[땜쓰 홈페이지](https://m.blog.naver.com/PostView.naver?blogId=ansdbtls4067&logNo=221238865180&navType=by)
[mouessee 홈페이지](https://740280.tistory.com/16)

Vivado & Vitis
[INIPRO 블로그](https://blog.naver.com/iniproinc/221917248383)
[고뭉나무 홈페이지](https://rubber-tree.tistory.com/category/Digital%20Logic/Zybo%20z7%20%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8)
[DKMIN 홈페이지](https://dkeemin.com/category/fpga/)
[금오공대 신경욱 교수님 강의 자료](http://www.kocw.net/home/cview.do?mty=p&kemId=1428200)

SDK
[qWooWp 홈페이지](https://qwoowp.tistory.com/21)

Linux Kenel
[Austin Kim 유투브 채널](https://www.youtube.com/watch?v=kEB28_z-myk&list=PLRrUisvYoUw9-cTYgkbTbr9f9CpbGdq4F)
[OJ Tube 유투브 채널](https://www.youtube.com/watch?v=zkpE7VYkpmM&list=PLz--ENLG_8TPuiK-Ib4uW5DXPvsdCDNc1)

Petalinux
[AMD - Technical Information Portal : Getting Started](https://docs.amd.com/v/u/en-US/dh0016-petalinux-tools-hub)
[Baram 홈페이지](https://blog.naver.com/chcbaram/222098925740)
[muselia 홈페이지](https://muselia.tistory.com/entry/Digilent-Arty-Z7-PetaLinux-1)
