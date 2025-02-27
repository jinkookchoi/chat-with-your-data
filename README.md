# (DRAFT) RAG 채팅 어플리케이션

## 💬 **RAG 채팅 어플리케이션 개요**
> ⚡ **이 프로젝트는 아래 GitHub 레포지토리를 기반으로 Azure 자원, 코드 등을 재구성한 것입니다.**
> [🔗 **Azure-Samples/chat-with-your-data-solution-accelerator**](https://github.com/Azure-Samples/chat-with-your-data-solution-accelerator)

---

## 📚 어플리케이션 소개

### 💡 User Story

- **Azure AI Search**와 **대형 언어 모델(LLMs)** 을 결합하여 **대화형 검색 경험** 제공
- **Azure OpenAI GPT 모델**과 **Azure AI Search 인덱스**를 사용하여 사용자 데이터에 대한 자연어 질의 처리
- **웹 애플리케이션 통합**: 자연어 인터페이스, **음성-텍스트 변환 기능 포함**
- **드래그 앤 드롭 파일 업로드**, **저장소 연결**, **기술적 설정 자동화** 지원
- 모든 구성 요소는 **사용자 구독에서 배포 가능**하여 빠른 활용 지원

### ⚙️ 주요 기능

- ✅ **Azure OpenAI 모델과 사용자 데이터 기반 채팅**
- 📂 **문서 업로드 및 처리**
- 🌐 **공개 웹 페이지 인덱싱 기능**
- 🧩 **간편한 프롬프트 구성**
- 🔍 **다양한 청크 분할 전략**
- ⚡ **Push 및 Pull 기반 데이터 수집 옵션**
- 🏗️ **Semantic Kernel, LangChain, OpenAI Functions, Prompt Flow 등의 오케스트레이션 선택**
- 🛠️ **실험 및 데이터 평가를 위한 RAG 구성 옵션 제공**

---

## 🏗️ RAG 채팅 어플리케이션 재구성 상세

### 🏛️ 아키텍처

- 💬 **Azure OpenAI GPT**: 사용자 데이터에 기반한 질의 응답
- 🔍 **Azure AI Search**: 사용자 데이터 인덱싱 및 고속 검색
- 🏃 **Azure Functions**: 대화 흐름 및 검색 로직 처리
- 🐳 **Azure Container Apps**: Docker 기반 RAG 모델 호스팅
- 🌐 **Azure App Service**: 프론트엔드 웹 인터페이스 제공
- 🔒 **VNet + Private Endpoint**: 네트워크 보안 및 서비스 간 비공개 통신
- 📊 **Application Insights**: 실시간 모니터링 및 문제 진단

---

### 💻 개발 환경

- 🏗️ **프로그래밍 언어**: Python, Node.js
- 🐳 **Docker**: 컨테이너화된 RAG 모델 및 백엔드 서비스
- ⚡ **Bicep**: Azure 리소스 배포 자동화
- 🧪 **CI/CD**: GitHub Actions를 통한 지속적 통합 및 배포
- 🏃 **Semantic Kernel 및 LangChain**을 통한 오케스트레이션 지원

---

## 🚀 **자원 배포 및 설정**

- 📝 **Bicep 템플릿**을 사용한 Azure 리소스 배포
- 📦 **Azure Container Registry**에 Docker 이미지 저장 및 배포
- 🔗 **VNet 구성** 및 **Private Endpoint**를 통한 보안 강화

### 배포 방식 1. 원클릭 배포

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fjinkookchoi%2Fchat-with-your-data%2Frefs%2Fheads%2Fmain%2Finfra%2Fmain.json)

### 배포 방식 2. `azd` cli 배포

```bash
azd auth login
azd env new // ex. dev
azd env set APP_NAME ${APP_NAME} // app-chat
azd provision
./scrips/deploy_function_keys.sh // Function App의 client key 배포
```

---

### 💬 주요 변경 및 최적화 사항

---

### 🎯 요약

- 📦 **이 프로젝트는 [Azure-Samples/chat-with-your-data-solution-accelerator](https://github.com/Azure-Samples/chat-with-your-data-solution-accelerator) 레포지토리를 기반으로 재구성되었습니다.**
- **Azure OpenAI**, **AI Search**, **Azure Functions**, **Azure Container Apps**를 사용하여 **RAG 기반 채팅 어플리케이션**을 구현되었습니다.

---

💡 **이 프로젝트의 상세한 내용에 대해서는 `docs` 폴더 내 문서를 참고하시길 바랍니다.  😊**
