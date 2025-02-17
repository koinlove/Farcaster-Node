# Farcaster Node
파캐스터 노드는 너무 쉬워서 스크립트가 따로 없어요~ 이것만 따라하면 모두 파캐스터 노드를 돌릴 수 있습니다~

## 파캐스터 노드 설치하는 방법
```bash
sudo apt update && sudo apt upgrade -y && sudo apt install screen -y
```
를 입력해서 기본 패키지를 깔아주세용~

그 다음에
```bash
screen -S farcaster
```
로 새로운 스크린을 켜준 뒤
```bash
curl -sSL https://download.thehubble.xyz/bootstrap.sh | bash
```
를 입력하면 자동으로 도커 패키지도 설치되고 그럴 거에요~

필요한 준비물은 다음과 같습니다.
> 1. 이더리움 주소의 알케미
> 2. 옵티미즘 주소의 알케미
> 3. 님의 파캐스트 FID(6자리 숫자)

이 3개를 준비해 두고, 파캐스트 노드가 설치되면서 요구하는 정보를 하나씩 넘겨주면 됩니다~!!

이후 로그가 뜨는데, 로그에서 뜨는 진행바가 100%를 찍으면 그 때부터 알케미에서 그래프가 활성화될 거에요.

## 잘 돌아가는지 확인하는 방법
```bash
http://님의.아이피.숫자를.넣으셈:3000
```
를 들어가면 님의 파캐스트 노드가 잘 돌아가는지 떠요(파캐노드는 포트 3000을 사용함). 알케미 말고 이거로 보는 게 가장 정확합니다 파캐스터 노드는

## 노드를 재시작하고 싶어요, 업데이트하고 싶어요
파캐는 웬만하면 잘 안 멈추긴 하는데, 혹시 멈추면
```bash
screen -r farcaster
```
를 입력하고
```bash
cd ~/hubble && ./hubble.sh upgrade
```
를 입력하면 혼자 업그레이드가 되면서 노드가 재시작될 거에요~

## RPC 주소를 바꾸고 싶어요, FID를 바꾸고 싶어요
```bash
cd ~/hubble && nano .env
```
이걸 입력하면 님의 RPC 주소와 FID 등을 수정할 수 있는 주소가 나옵니다~

## 파캐스터 로그를 보고 싶어요, 진행바 퍼센티지를 확인하고 싶어요.
```
docker logs hubble-hubble-1
```
이걸 입력하거나
```bash
screen -r farcaster
```
를 입력하면 돌아가고 있는 노드의 로그를 보실 수 있습니다~

혹은
```bash
docker ps
```
를 쳐도 파캐스터 노드 도커가 잘 돌아가는지 볼 수 있어요~
