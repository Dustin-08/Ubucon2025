- Wig Cheng
	- OSS Contribution
		- U-Boot Upstream
		- Linux
	- github
		- Wig Cheng
### 01) What is the Gateway
- Gateway는 4가지 존재
	- Industrial Gateway
		- Connects OT(Operational Tech)
		- PLCs, SCADAS, CNCs, Legacy industrial equipment
		- protocol: Modus, OPC-UA
	- IoT Gateway
		- MQTT, Zigbee, BLE
	- AIoT Gateway
		- camera, microphoes
		- protocol: V4L2, ALSA
		- edge computing
	- Cloud Gateway
		- 물리 디바이스 필요 x
		- 환경 상에서 구성
### 02) Make an Ubuntu rootfs with lightweight desktop
- WARER-IMX8MP
- FRDM-IMX93
	- NPU: ARM Ethos-U65
- RZ/T2H EVK
#### Debootstrap
- a cli tool used to install a minimal but fully functional Debian, Ubuntu, or derivative base system into a specified directory
	- minimal rootfs
	- custom rootfs
```bash
sudo apt update
sudo apt install debootstrap
sudo apt install qemu-system-arm qemu-user-static
sudo debootstrap --arch=arm64 -- keyring=/usr/share/keyrings/ubuntu-archive-keyring.gpg --verbose --foreign noble rootfs
```
#### LXQt Desktop
- Demo
	- arm64
### 03) AIoT with NPU accelerations
- IMX8MP NPU Driver
- Tensor Flow Lite demo
	- web cam demo 가능
- library porting
	- IMX93 NPU는
		- upstream 드라이버가 없음
		- 드라이버 설치 필요
- (여기는 발음을 Ubuntu를 우방투 이래버리네)
### 04) MCU develop environment
- 아두이노와 ESP32처럼 MCU가 있음
	- 1 CPU, 1 MCU가 보드에 있음
	- Free RTOS 코드를 우분투에 올리면 바로 할 수 있음
- 데모
	- 작은 e-paper 데모를 해보았다
	- A55 -> M33로 보낼때 rpmsg 채널로 보냄
		- Cross Compiler 진행
### 05) Conclusion & Future work
- debootstrap
	- 쉽지만 아키텍처를 만들어줘야 한다
- live-build
	- 어렵지만, 바로바로 유연하게 대응됨
- Ubuntu BSP
- 