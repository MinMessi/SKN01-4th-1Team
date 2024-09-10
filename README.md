<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:000000,70:003300,100:00FF00&height=240&text=SKN01-4th-1Team&animation=&fontColor=00FF00&fontSize=90" width="1000" />
  
  <img width="1000" alt="image" src="https://github.com/Jh-jaehyuk/Jh-jaehyuk.github.io/assets/126551524/7ea63fc3-95f0-44d5-a0f0-cf431cae34f1"> 
  
  [![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN01-4th-1Team&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)
</div>



# 0. Introduction Team (팀 소개)
### ✅ 팀명 : TCP(Text Chat Programmers)
<table align=center>
  <tbody>
    <tr>
      <td align=center><b>한재혁</b></td>
      <td align=center><b>민경원</b></td>
      <td align=center><b>정아람</b></td>
      <td align=center><b>최인헌</b></td>
      <td align=center><b>이용휘</b></td>
    </tr>
    <tr>
      <td align="center">
        <div>
          <img src="https://github.com/user-attachments/assets/80f0a998-61ab-4de5-a652-51575e8a4468"width="200px; alt=""/>
        </div>
      </td>
      <td align="center">
        <div>
          <img src="https://github.com/user-attachments/assets/30f29d8b-bcec-46c7-bce6-e6e4ec414e55"width="200px;" alt=""/>
        </div>
      </td>
      <td align="center">
        <img src="https://github.com/user-attachments/assets/c01c579b-7f4f-436b-984a-74a26d2cef44"width="200px;" alt=""/>
      </td>
      <td align="center">
        <img src="https://github.com/user-attachments/assets/77eff59b-1c54-4d91-a49c-5f81cf28fb35"width="200px;" alt=""/>
      </td>
      <td align="center">
        <img src="https://github.com/user-attachments/assets/49822355-b1ef-485b-a45b-dc2199d8397b"width="200px;" alt=""/>
      </td>
    </tr>
    <tr>
      <td><a href="https://github.com/Jh-jaehyuk"><div align=center>@Jh-jaehyuk</div></a></td>
      <td><a href="https://github.com/MinMessi"><div align=center>@MinMessi</div></a></td>
      <td><a href="https://github.com/Ah-ram"><div align=center>@Ah-ram</div></a></td>
      <td><a href="https://github.com/ih9511"><div align=center>@ih9511</div></a></td>
      <td><a href="https://github.com/y0ng98"><div align=center>@y0ng98</div></a></td>
    </tr>
  </tbody>
</table>
<br><br><br>



# 1. Introduction Project (프로젝트 개요)

### ✅프로젝트 명
논문 요약 및 설명 제공 서비스

### ✅프로젝트 소개
논문 요약 및 설명 제공 서비스

### ✅프로젝트 필요성(배경)
- 새로운 기술에 대한 연구가 과거 대비 매우 빠른 속도로 발표되고 있습니다.
- 이에 새로운 기술을 논문을 통해 접하고자 하는 니즈가 발생하고 있음을 발견하였고, 이러한 니즈를 충족시키기 위해 논문을 읽을 수 있는 방식을 LLM을 통해 제공하여 많은 사람들이 이용할 수 있도록 서비스화하고자 합니다.

## 비동기 통신 방식의 Deep Learning Local Server
### Syncronous Communication
- 동기(Syncronous)란 동시에 일어난다는 뜻입니다. 즉, Request와 Response가 동시에 일어나는 통신 방식입니다.
- 노드 A와 노드 B 사이의 작업 처리 단위를 동시에 맞춥니다.
- 요청한 결과가 그 자리에서 동시에 주어집니다.
### Asyncronous Communication
- 비동기(Asyncronous)란 동시에 일어나지 않는다는 뜻입니다. 즉, Request와 Response가 동시에 일어나지 않는 통신 방식입니다.
- 노드 사이의 작업 처리 단위를 동시에 맞추지 않겠다는 것으로, 요청한 결과가 그 자리에서 주어지지 않습니다.
### 각 통신 방식의 장단점
- 동기 통신의 경우 설계가 간단하며, 직관적이지만 그 작업이 끝날 때까지 아무런 작업도 할 수 없다는 단점이 있습니다.
- 비동기 통신의 경우 동기 통신보다 비교적 복잡한 구현이 필요하지만, 작업이 끝날 때 까지 기다리지 않아도 되기 때문에 그 동안 다른 작업을 수행할 수 있으므로 효율적인 자원의 사용이 가능합니다.
### 비동기 통신 방식 DLLS
- 모델이 Request에 따라 Response를 하기까지 입력에 대한 결과를 추론하는데에 시간이 필요합니다. 만약 Response를 반환하는 과정을 동기 통신 방식으로 구현한다면, 결과 반환이 완료될 때 까지 사용자는 아무것도 하지 못합니다.
- 따라서, 모델이 추론하여 Response를 반환하는 과정을 비동기 방식으로 설계하여 사용자가 추론 요청 이외의 작업을 수행할 때에도 문제가 없도록 하였습니다.
### 물리적 로컬 서버 구현 이유
- AWS 상에서 LLM 모델의 Fine Tuning 및 추론 과정을 구동시킬 경우, 예산을 넘어서는 비용이 발생할 가능성이 존재합니다.
- 이에 컴퓨팅 자원이 많이 필요한 부분을 따로 물리적 로컬 서버에서 구동하여 Response를 반환하도록 설계하였습니다.
- 결과적으로, 모델 서빙 역할의 FastAPI와 DLLS 상의 AI Client 사이의 비동기 통신을 통해 비용적인 측면에서의 최적화를 달성하고 사용자가 서비스를 사용함에 있어서 불편함이 없도록 하였습니다.
### TLS/SSL 보안 통신 환경 구축
- 커스텀 서버 특성 상, 비교적 해킹에 취약할 가능성이 존재합니다. 이에 보안 프로토콜을 적용하여 외부에서 우리의 서비스에 접근할 수 없도록 보안 통신 환경을 구축하였습니다.

### ✅프로젝트 목표
1. Front-End에서는 **TypeScript**와 **Vue.js + Vuetify3**를 이용하여 사용자 측면에서 유리한 UI-UX를 구축하였고, **Axios** 를 통해서 올바른 Request를 하는 것을 목표로 삼았습니다. 
2. Back-End에서는 **Python**과 **Django**, **MySQL** 등을 이용하여 Request에 대한 정확한 Response와 원활한 웹사이트 운영하는 것을 목표로 삼았습니다.
3. Fast API에서는 **Machine Learning** **Deep Learning** 이용하여 데이터를 분석 및 예측할 수 있도록 하였습니다.
4. Deep Learning Local Server (DLLS) 에서는 **Fast API와 AI Client의 비동기 통신 환경**을 소켓 통신으로 구축하여 일반적인 동기 Request들이 처리될 때, 정상적으로 동작하도록 구축하였습니다.
5. CI-CD는 지속적인 코드 통합과 지속적인 배포를 통해 궁극적으로 개발 속도를 높이고, 코드 품질을 유지하며, 개발과 운영의 경계를 허물며 신속하게 가치를 제공하는 것을 목표로 삼았습니다. 
<br><br><br>



# 2. Tech Stack (기술 스택)

### Co-Work Tool(Communication)
![Github](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=GitHub&logoColor=white)
<img src="https://img.shields.io/badge/gitkraken-179287?style=for-the-badge&logo=gitkraken&logoColor=white"/>
<img src="https://img.shields.io/badge/notion-%23000000?style=for-the-badge&logo=notion&logoColor=white"/> 
<img src="https://img.shields.io/badge/slack-%234A154B?style=for-the-badge&logo=slack&logoColor=white"/>
<img src="https://img.shields.io/badge/discord-5865F2?style=for-the-badge&logo=discord&logoColor=white"/>

### IDE
![PyCharm](https://img.shields.io/badge/pycharm-%23000000?style=for-the-badge&logo=pycharm&logoColor=white")
<img src="https://img.shields.io/badge/Jupyter_Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white"/>
<img src="https://img.shields.io/badge/VS%20Code-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white"/> 


### Frontend
![HTML](https://img.shields.io/badge/HTML-E34F26?style=for-the-badge&logo=html5&logoColor=white)
<img src="https://img.shields.io/badge/css-1572B6?style=for-the-badge&logo=css3&logoColor=white"/>
<img src="https://img.shields.io/badge/Javascript-ffb13b?style=for-the-badge&logo=javascript&logoColor=white"/>
<img src="https://img.shields.io/badge/vue.js-4FC08D?style=for-the-badge&logo=vue.js&logoColor=white"/> 
<img src="https://img.shields.io/badge/vuetify-%231867C0?style=for-the-badge&logo=vuetify&logoColor=white"/>
<img src="https://img.shields.io/badge/typescript-3178C6?style=for-the-badge&logo=typescript&logoColor=black"/>
<img src="https://img.shields.io/badge/axios-%235A29E4?style=for-the-badge&logo=axios&logoColor=white"/>

### Backend
![Python](https://img.shields.io/badge/python-3776AB?style=for-the-badge&logo=python&logoColor=white)
<img src="https://img.shields.io/badge/pandas-%23150458?style=for-the-badge&logo=pandas&logoColor=white"/> 
<img src="https://img.shields.io/badge/numpy-%23013243?style=for-the-badge&logo=numpy&logoColor=white"/>
<img src="https://img.shields.io/badge/Openpyxl-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white"/>
<img src="https://img.shields.io/badge/SQLAlchemy-666699?style=for-the-badge&logo=sqlalchemy&logoColor=white"/>

### Fast API (AI Core)
![FastAPI](https://img.shields.io/badge/fastapi-%23009688?style=for-the-badge&logo=fastapi&logoColor=white)
<img src="https://img.shields.io/badge/Machine_Learning-FF6F00?style=for-the-badge&logo=machine-learning&logoColor=white"/>
<img src="https://img.shields.io/badge/scikitlearn-%23F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white"/>
<img src="https://img.shields.io/badge/Deep_Learning-00599C?style=for-the-badge&logo=deep-learning&logoColor=white"/>
<img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white"/>
<img src="https://img.shields.io/badge/Keras-D00000?style=for-the-badge&logo=keras&logoColor=white"/>

### CI-CD Infrastructure
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonwebservices&logoColor=white)
<img src="https://img.shields.io/badge/AWS_EC2-FF9900?style=for-the-badge&logo=amazon-ec2&logoColor=white"/>
<img src="https://img.shields.io/badge/AWS_S3-569A31?style=for-the-badge&logo=amazon-s3&logoColor=white"/>
<img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=GitHub&logoColor=white"/>
<img src="https://img.shields.io/badge/github%20actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white"/>
<img src="https://img.shields.io/badge/docker-%232496ED?style=for-the-badge&logo=docker&logoColor=white"/> 
<img src="https://img.shields.io/badge/mysql-4479A1?style=for-the-badge&logo=mysql&logoColor=white"/>
<img src="https://img.shields.io/badge/redis-%23FF4438?style=for-the-badge&logo=redis&logoColor=white"/>
<br><br><br>



# 3. 시스템 구성도
![image](https://github.com/user-attachments/assets/66a78240-b41d-487a-8800-29bccbab7d41)
<br><br><br>



## 애자일 보드를 사용하는 이유
```c
과거 정의서들을 일일히 작성하였지만 빠른 속도로 무언가를 개발하는데 한계가 있습니다.
처음부터 많은 것들을 빌드업하면서 빠른 생산성을 기반으로 움직이려면 반드시 애자일해야합니다.
고로 폭포수 설계 방식이 아닌 애자일 프로세스 방식으로 애자일 보드를 작성하면서 진행했습니다.

애자일 보드는 자체적으로 제목이 요구 사항을 내포하며 각 카드 내부에는 정의한 Domain의 세부 사항이 기록됩니다.
고로 빠르게 팀원들과 협업 할 수 있고 소통 비용을 최소화시킬 수 있습니다.
작은 것 같지만 이와 같은 것들이 쌓여서 아주 기민하고 민첩한 조직을 만들어 냅니다.
```
# 4. 애자일 보드
### Frontend - Frontend 페이지를 Vue 로 구성 (화면 설계서)
![image](https://github.com/user-attachments/assets/b547b885-25f8-413f-ab40-3251e8b77e95)
![image](https://github.com/user-attachments/assets/b947d9db-b2d1-4494-8842-82285289d6ff)
<br><br><br>

### Backend - Backend 데이터 관리로 Django 구성(요구 사항 정의서)
![image](https://github.com/user-attachments/assets/89ece460-81bd-44cf-bc7d-644487b3b267)
<br><br><br>

### FastAPI - AI 서빙용으로 FastAPI 구성
![image](https://github.com/user-attachments/assets/ccd6592b-4e7c-4fab-a7fe-6f16e8515195)
<br><br><br>

### AI Client - 비용 최적화를 위해 DLLS 구성 (모델 파인튜닝 및 추론 설계서)
![image](https://github.com/user-attachments/assets/ee098b0b-77b0-4e53-9a47-836e61081638)
<br><br><br>



# 5. 비용 최적화를 위한 Deep Learning Local Server 구성 + 보안 설정을 위한 TLS / SSL 소켓 구성
## 10-1 Socket Server (FastAPI) 구성 및 구동 방법
1. FastAPI 프로젝트 폴더 내에서 미리 구성해 놓은 소켓 통신 관련 submodule을 다음의 명령어를 통해 연결합니다.
```bash
git submodule add "socket server submodule Github 주소" template
```

2. 다음과 같이 `template` 라는 submodule이 프로젝트 내부에 붙은 것을 확인할 수 있습니다.
![image](https://github.com/user-attachments/assets/fc83fd3b-3cf0-4852-a6e1-c143afb3eed3)
3. 이후에 `cd include/socket_server/`에 소켓 서버의 역할을 하도록 해놓은 모듈에 대한 내용들을 다음의 명령어로 갱신시킵니다.
![image](https://github.com/user-attachments/assets/1bf1190e-1aad-45d9-ad6b-d44090f88c0f)
```bash
cd ../..
git submodule update --init --recursive
```
4. 그러면 아래처럼 내용들이 추가된 것을 확인할 수 있습니다.
![image](https://github.com/user-attachments/assets/bb624477-e11a-461c-a532-63389108c566)

5. 이후 미리 준비해놓은 보안 관련 파일들을 프로젝트 폴더에 배치시킵니다.
```bash
CA.pem
svr.key
svr.crt
```

6. 서버를 구동시키면 다음과 같이 ai-client의 접속을 대기하는 것을 확인할 수 있습니다.
![image](https://github.com/user-attachments/assets/dbdf40fe-1fc0-4e15-9c05-73618d202e63)

## 10-2 Socket Client (ai-client) 구성 및 구동 방법
1. ai-client 프로젝트 폴더 내에서 소켓 서버와 마찬가지로 미리 구성해 놓은 소켓 통신 관련 submodule을 다음의 명령어를 통해 연결합니다.
```bash
git submodule add "socket client submodule Github 주소" template
```

2. 다음과 같이 `template` 라는 submodule이 프로젝트 내부에 붙은 것을 확인할 수 있습니다.
![image](https://github.com/user-attachments/assets/7340470c-97c3-4ee4-ab18-d52bbc6a8c83)

3. 이후 미리 준비해놓은 보안 관련 파일들을 프로젝트 폴더에 배치시킵니다.
```bash
CA.pem
client.key
client.crt
```

4. 서버를 구동시킨 상태에서 ai-client를 구동하여 socket server로 접속을 시도하면 다음과 같이 잘 접속되는 것을 확인할 수 있습니다. 또한, 미리 구성한 보안 접속도 잘 작동하는 것을 확인할 수 있습니다.
![image](https://github.com/user-attachments/assets/98fdf151-ee23-41ba-a09d-fc1ac6ffd2d0)





# 6. 각자 팀 주제에 따라 TF-IDF 기반의 벡터 산출
# 7. 주제에 맞게 벡터 결과를 비교
# 8. 검색 속도 향상을 위해 벡터 값을 벡터 DB 에 저장
# 9. 사용자 요청에 대한 검색 속도 향상을 통한 응답성 증대







# 10. Result (수행 결과)
Frontend / Backend / FastAPI / DLLS 구성에서 모든 동작이 안정적으로 잘 실행되는지 확인
FastAPI - DLLS 구성에서 사용자 요청에 따른 LLM 동작이 잘 동작하는지 확인
구성한 사용자 정의형 프로토콜이 잘 동작하는지 확인
시연 결과 모습

![image](https://github.com/user-attachments/assets/09b2e0f6-66a1-4288-a012-81d424b158e9) 
![image](https://github.com/user-attachments/assets/4f6940df-a192-43a9-a4d0-8e425dc25290)
![image](https://github.com/user-attachments/assets/026a0e22-7868-4cf3-9aad-6911ae90a7a6)
![image](https://github.com/user-attachments/assets/acebf5fb-cbfc-4053-96f8-57879e1ee081)
![image](https://github.com/user-attachments/assets/c4017585-5472-48d0-905b-ec3b713c7ce3) 
![image](https://github.com/user-attachments/assets/ffe79024-74c2-42b2-bab7-d759514eb208)  



# 12. 테스트 보고서 (CI 테스트 결과)
1. **테스트 환경**  
  * Jest

2. **유닛 테스트**  
  * Mocking test
  * 게시판에 게시글이 예상대로 등록되는지 확인

3. **커버리지 테스트**  
   * 커버리지 테스트를 통하여 코드 품질을 모니터링하고 개선할 수 있음  
   * 테스트 결과, 코드베이스에서 약 87퍼센트 실행됨을 알 수 있음  
  ![Coverage1](https://github.com/user-attachments/assets/e3d13016-8efc-4681-8264-f4cc047f0c3a)  
4. **테스트 스크린샷**  
  * 🧪 **Backend Build Test**  
    <img width="976" alt="Backend-Build-Test" src="https://github.com/user-attachments/assets/b7ad4ba0-f070-477a-b1f6-39460f94837c">  
  * 🧪 **Frontend Build Test**  
    <img width="993" alt="Frontend-Build-Test" src="https://github.com/user-attachments/assets/449cff0e-1953-4a93-aa0f-3ea8e07291d9">   
  
5. **결 론**
  * 🆗 _Backend_ 와 _Frontend_ 모두 성공적으로 **Build** 되는 것을 확인할 수 있습니다.

# 13. Deploy Issue (배포 이슈)
1. **Error: repository name must be lowercase**
![Issue1](https://github.com/user-attachments/assets/0eaa074a-c88e-469b-8ab2-e90919ad1c88)  
<br>

### _Solution_   
만약 actor가 Uppercase라면, 아래와 같이 직접 Lowercase를 명시하여 문제를 해결할 수 있습니다.

```yaml
name: Django CD (Continuous Deploy)

on:
  repository_dispatch:
    types: [BACKEND_TEST_FINISH_TRIGGER]

jobs:
  build:
    name: build-app
    runs-on: ubuntu-latest
    steps:
    - name: Checkout repository
      uses: actions/checkout@v3
```
  
위의 내용을 아래와 같이 수정합니다.  
```yaml
name: Django CD (Continuous Deploy)

on:
  repository_dispatch:
    types: [BACKEND_TEST_FINISH_TRIGGER]
    
env:
  DOCKER_IMAGE: ghcr.io/${{ secrets.REAL_ACTOR }}/tcp-backend

jobs:
  build:
    name: build-app
    runs-on: ubuntu-latest
    steps:
    - name: Checkout repository
      uses: actions/checkout@v3
```

그리고 아래 내용을 수정합니다.  
```yaml
- name: Build and Push Docker Image
  run: |
    cd tcp_backend/tcp_django
    docker buildx build --platform linux/arm64 -f Dockerfile -t ghcr.io/${{ github.actor }}/tcp-django-backend-server:latest --push .
```
  
위의 내용을 아래와 같이 수정합니다.
```yaml
- name: Build and Push Docker Image
  run: |
    cd tcp_backend/tcp_django
    docker buildx build --platform linux/arm64 -f Dockerfile -t ${{ env.DOCKER_IMAGE }}:latest --push .
```

**secrets**에 _REAL_ACTOR_ 를 설정하고 _REAL_ACTOR_ 를 **소문자 본인 계정**으로 작성하면 됩니다.  
ex) Ah-ram >> ah-ram  

마지막으로 아래 내용을 수정합니다.  
```yaml
deploy:
  needs: build
  name: Deploy
  runs-on: [ self-hosted, deploy-tcp-backend ]
  steps:
  - name: Login to GHCR
    uses: docker/login-action@v1
    with:
      registry: ghcr.io
      username: ${{ github.actor }}
      password: ${{ secrets.GHCR_TOKEN }}
```

위의 내용을 아래와 같이 수정합니다.  
```yaml
deploy:
  needs: build
  name: Deploy
  runs-on: [ self-hosted, deploy-lms-backend ]
  steps:
  - name: Login to GHCR
    uses: docker/login-action@v1
    with:
      registry: ghcr.io
      username: ${{ secrets.REAL_ACTOR }}
      password: ${{ secrets.GHCR_TOKEN }}
```

2. **Cannot connect to the Docker daemon at <workdir>**
![Issue2](https://github.com/user-attachments/assets/775cadb2-3228-425a-bf98-9ebf4aed8d43)  
<br>

### _Solution_  
local에 **docker desktop이 켜져있는지 확인**해보아야 합니다.  
Docker desktop을 실행하고 다시 시도하니 해결되었습니다.  

3. **FastAPI 배포 이후, 웹에 접속이 되지 않습니다.**
<img width="722" alt="Issue3" src="https://github.com/user-attachments/assets/89331de6-8e8b-42d8-bf7b-e15364e2260d">
<br>

### _Solution_  
FastAPI 배포 후, **인스턴스 보안 그룹에서 33333 port에 대하여 인바운드 설정**을 해주어야 합니다.  
설정하고 다시 접속하면 정상적으로 처리되는 것을 확인할 수 있습니다.  
![Issue3-1](https://github.com/user-attachments/assets/0a4d7844-692f-43e2-98fb-76680f98e5a1)  
  
# 14. 한 줄 회고
🤓<b>한재혁</b>  
_AWS와 Docker에 대해서 배우고 싶었는데, 단순히 배우는 것에서 그치지 않고 웹 애플리케이션 작성부터 배포까지 경험할 수 있어서 정말 좋은 경험이었습니다! 팀원분들도 같이 열심히 해주셔서 어렵지 않게 마무리 할 수 있었습니다. 다들 고생하셨습니다!!👏_  

👨‍💻<b>민경원</b>  
_AWS -GitHub Actions-Docker등을 이용한 CI-CD 구축을 직접 경험해볼 수 있어서 좋았습니다._  

😺<b>정아람</b>  
_CI/CD 환경 구성으로 프로젝트 배포를 자동화하고 AWS와 결합해 서비스를 할 수 있는 좋은 경험이었습니다._  

🪐<b>최인헌</b>  
_Django, MySQL과 Vue를 활용하여 웹 기반 서비스들의 작동 방식을 이해하는 기회가 되었고, AWS와 GitHub Actions를 활용하여 배포까지 해봄으로서 CI/CD가 어떻게 이루어지는지 알 수 있었던 계기가 되었습니다. 모두 고생 많으셨습니다!_  

😁<b>이용휘</b>  
_AWS와 Docker를 제대로 다루어 본 것은 처음인데, 다양한 issue들을 겪어서 힘들었지만 그만큼 많이 배운 것 같습니다._  
