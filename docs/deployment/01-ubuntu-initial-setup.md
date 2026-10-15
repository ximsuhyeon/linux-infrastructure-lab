
# Ubuntu Server 초기 환경 구축

## 1. 작업 정보

| 항목 | 내용 |
|---|---|
| 작업일 | 2026-10-15 |
| 작성자 | 김수현 |
| 작업 구분 | 서버 초기 구축 |
| 작업 상태 | 완료 |

## 2. 구축 환경

| 항목 | 설정값 |
|---|---|
| Hypervisor | VMware Workstation |
| OS | Ubuntu Server 24.04.5 LTS |
| Hostname | infra-ubuntu-01 |
| Network Interface | ens33 |
| IP Address | 192.168.200.10/24 |

## 3. 수행 작업

### 3.1 가상머신 생성 및 OS 설치
- VMware 가상머신 생성
- Ubuntu Server 24.04.5 LTS 설치
- 초기 사용자 계정 구성
- 호스트명 `infra-ubuntu-01` 설정

### 3.2 네트워크 설정
- 네트워크 인터페이스 `ens33` 확인
- 고정 IP `192.168.200.10/24` 설정
- 네트워크 설정 적용

### 3.3 초기 스냅샷 생성
- OS 설치 및 네트워크 설정 완료 후 스냅샷 생성
- 후속 실습 중 설정 오류 발생 시 복구 기준점 확보

## 4. 구축 검증

### 4.1 네트워크 설정

| 항목 | 검증 결과 |
|---|---|
| Interface | ens33 |
| Interface State | UP |
| IP Address | 192.168.200.10/24 |
| 검증 명령어 | `ip a` |
| 결과 | 고정 IP 할당 및 인터페이스 활성 상태 확인 |

![네트워크 설정 검증](/ximsuhyeon/linux-infrastructure-lab/blob/main/evidence/01-network-configuration.png)

### 4.2 초기 스냅샷

| 항목 | 내용 |
|---|---|
| 생성 시점 | OS 설치 및 네트워크 초기 설정 완료 후 |
| 목적 | 초기 정상 구성 상태 보존 |
| 결과 | VMware 스냅샷 생성 완료 |

![초기 스냅샷](/ximsuhyeon/linux-infrastructure-lab/blob/main/evidence/02-initial-snapshot.png)
## 5. 작업 결과

- Ubuntu Server 초기 설치 완료
- 호스트명 및 고정 IP 설정 완료
- 네트워크 인터페이스 활성 상태 확인
- 초기 스냅샷 생성 완료
- 후속 Linux 시스템 운영 실습을 위한 기본 환경 확보
