# [학술도구 어시스턴트] 개인정보처리방침 (Privacy Policy)

본 개인정보처리방침은 **[학술도구 어시스턴트 (Scholar Assistant)]**(이하 '본 프로그램')가 사용자의 개인정보를 처리하는 방식과 보안에 대해 설명합니다. 본 프로그램은 사용자의 연구 데이터를 최우선으로 보호하며, 관련 법령 및 웹 스토어 개발자 정책을 준수합니다.

---

### 1. 개인정보 수집 및 처리 항목
본 프로그램은 서비스 제공을 위해 필요한 최소한의 데이터에만 접근하며, 별도의 서버로 수집하거나 전송하지 않습니다.
* **클립보드 데이터**: 사용자가 NotebookLM의 답변을 '스크랩'할 때 해당 텍스트를 읽기 위해 일시적으로 접근합니다. 클립보드 읽기가 불가한 경우 사용자가 직접 붙여넣기한 내용만 처리합니다.
 클립보드 읽기는 사용자가 NotebookLM 페이지에서 스크랩 또는 가져오기 기능을 직접 실행한 경우에만 사용됩니다. 클립보드 쓰기는 사용자가 복사, ToMD, ScholarSlide 또는 결과 전달 버튼을 직접 누른 경우에만 사용됩니다.

클립보드 내용은 사용자의 명시적 조작 없이 자동으로 외부 서비스에 전송되지 않습니다.
* **텍스트 콘텐츠**: 사용자가 직접 입력하거나 수정한 학술용 프롬프트(슬라이드 생성, Scholar Explore 단계별 프롬프트 등) 및 스크랩된 분석 결과물.
* **브라우저 스토리지 정보**: 앱의 설정 상태, 프롬프트 입력 내용, 현재 스크랩, 누적 스크랩 목록 등이 로컬에 저장됩니다.

### 2. 데이터 처리 방식 (로컬 저장 및 사용자 승인 원칙)
본 프로그램은 사용자의 데이터를 외부로 유출하지 않는 것을 원칙으로 하며, 모든 데이터 이동은 사용자의 능동적인 조작에 의해서만 이루어집니다.
* **외부 전송 금지**: 처리된 모든 데이터는 개발자나 제휴사를 포함한 제3자에게 전송되지 않으며, 외부 서버와의 통신을 수행하지 않습니다.
* **사용자 승인 기반 처리**: **클립보드에 복사된 내용을 포함하여 본 프로그램 내의 모든 문서 데이터는 사용자의 명시적인 승인(버튼 클릭, 붙여넣기 실행 등) 없이는 그 어떠한 곳으로도 전송하거나 외부로 보낼 수 없지만, 안전하다고 생각한 이 앱과 연동된 사이트로는 보냅니다. 그 사항은 하단에 상세하게 기록했습니다. **
* **로컬 저장소 활용**: 모든 데이터는 사용자의 브라우저 로컬 저장소(`edge.storage.local`) 내에만 저장됩니다.

본 프로그램은 사용자의 문서, 프롬프트, 스크랩, 설정 정보를 기본적으로 브라우저의 로컬 저장소에 저장합니다.
본 프로그램은 사용자가 기능을 명시적으로 실행한 경우에만 필요한 데이터를 사용자가 선택한 외부 서비스로 전송할 수 있습니다.

**사용자 승인 기반 외부 전송이 발생할 수 있는 기능은 다음과 같습니다.**
- Gemini 또는 DeepSeek를 이용한 AI 분석 및 문장 생성
- OpenAlex 또는 Crossref를 이용한 학술자료 검색
- 사용자가 직접 설정한 GitHub 저장소와의 동기화
- 사용자가 직접 운영하는 LM Studio 또는 Ollama 로컬 서버와의 통신
- MDProViewer 또는 ScholarSlide로의 사용자 승인 기반 콘텐츠 전달

외부 서비스로 전달되는 데이터는 사용자가 입력하거나 선택한 프롬프트, 텍스트, 검색어 또는 동기화 대상 데이터로 제한됩니다.

본 프로그램은 사용자의 전체 방문 기록, 비밀번호, 결제정보 또는 웹페이지 전체 내용을 개발자 서버로 자동 수집하거나 저장하지 않습니다. 개발자는 사용자가 외부 서비스로 전송한 콘텐츠를 별도의 자체 서버에 보관하지 않습니다.

### 3. 데이터 사용 목적

본 프로그램은 오직 다음과 같은 목적으로만 데이터를 사용하며, 사용자의 개입 없이 자동으로 데이터를 외부로 반출하지 않습니다.
* Google NotebookLM 서비스와 연동한 학술 문서 분석 지원(지식 지도, 슬라이드 생성, Scholar Explore 단계별 학습 프롬프트).
* NotebookLM 답변의 스크랩, 누적 저장, 통합 보기 및 마크다운(Markdown) 파일 내보내기 기능 제공.
* **에디터 및 외부 연동 방식**: 
    * **기본 설정**: 스크랩된 데이터는 프로그램 내부의 **'내부 에디터(md_editor/ View_editor). '**를 통해 처리되며, 모든 작업은 NotebookLM의  로컬 환경 내에서 유지되는 것을 우선으로 합니다. 
    * **외부 연동 (mdproviewer.vercel.app)**: 사용자가 본인의 의지에 따라 더 많은 편집을 하기 위해서는 **설정(Settings)에서 외부 연동을 직접 활성화한 경우에만** 사용 가능합니다. 'ToMD' 버튼 클릭 시 새 탭으로 해당 사이트가 열리며, 실제 데이터의 붙여넣기는 사용자가 직접 수행하며 전송할 때에도 사용자가 명시적 승인한 경우만 전송하는 것으로 합니다. 본 프로그램은 사용자의 요청 시 클립보드에 내용을 복사하는 보조 역할만 수행하며, 사용자의 승인 없는 데이터 외부 전송은 원천적으로 차단됩니다.
### 4. 데이터 보유 및 파기
* **보유 기간**: 데이터는 사용자의 브라우저 내에만 존재하며, 별도의 보관 기간을 두지 않습니다.
* **파기 방법**: 사용자가 확장 프로그램 관리 페이지에서 본 프로그램을 **삭제(제거)**하면, 로컬 저장소에 기록된 모든 데이터는 즉시 영구 파기됩니다.

### 5. 사용자의 권한
* 사용자는 언제든지 프로그램 내의 기능을 통해 저장된 데이터를 수정하거나 삭제할 수 있습니다.
* 사용자는 본 프로그램이 요구하는 권한(클립보드, 저장소 등)을 거부할 권리가 있으나, 이 경우 핵심 기능 이용이 제한되지 않으며, 핵심기능(프롬프트 전송, 별도로 제작한 프롬프트관리, 다른 사이트 열기 등)은 제한 받지 않습니다. 

---
**공표일**: 2026년 3월 19일  
**시행일**: 2026년 3월 19일  
**개발자**: 박중희




# Privacy Policy for Scholar NotebookLM Extension

Last updated: July 31, 2026

## 1. Overview

Scholar NotebookLM is a browser extension that assists users in collecting, organizing, analyzing, and reusing academic research content from Google NotebookLM.

This Privacy Policy explains what data the extension processes and when user-selected data may be transmitted to an external service.

## 2. Local Data Storage

The extension may store the following information in the browser’s local extension storage:

- user preferences;
- saved academic prompts;
- user-created research notes;
- saved scraps;
- AI provider settings;
- local AI server connection settings;
- optional GitHub synchronization settings; and
- extension interface state.

This information is stored primarily in chrome.storage.local.

The developer does not operate a separate server for storing users’ research documents.

## 3. User-Provided Content

The extension may process the following content when the user explicitly invokes a related feature:

- text selected by the user;
- NotebookLM responses selected or copied by the user;
- prompts entered by the user;
- publication search queries;
- research notes and scraps;
- citations and reference metadata; and
- documents selected by the user for optional synchronization.

The extension does not automatically collect the full contents of every webpage visited by the user.

## 4. External AI Services

When a user explicitly requests AI analysis or text generation, the prompt or selected content may be transmitted to the AI provider selected by the user.

Supported services may include:

- Google Gemini;
- DeepSeek;
- a user-operated LM Studio server;
- a user-operated Ollama server; and
- another compatible AI endpoint configured by the user.

Only the content entered or selected by the user for the requested operation is transmitted.

Third-party services process data according to their own privacy policies.

## 5. Academic Search Services

When a user initiates a publication or citation search, the search query may be transmitted to academic metadata providers such as:

- OpenAlex; and
- Crossref.

The returned metadata may include publication titles, authors, DOI values, publication years, journal names, and related citation information.

## 6. GitHub Synchronization

GitHub synchronization operates only when it has been configured and directly initiated by the user.

The extension may transmit user-selected prompts, research notes, or documents to a GitHub repository selected by the user.

The developer does not store the user’s GitHub credentials or synchronized documents on a separate developer-operated server.

## 7. Clipboard Access

Clipboard reading is used only when the user explicitly invokes a feature such as:

- importing clipboard content;
- scraping a copied NotebookLM response; or
- importing copied research text.

Clipboard writing is used only when the user explicitly invokes a feature such as:

- Copy;
- ToMD;
- transfer of research results; or
- copying content to a supported writing or presentation tool.

The extension does not continuously monitor the clipboard and does not read clipboard content merely because a webpage has been opened.

## 8. Access to the Current Page

The optional insert-into-current-page feature temporarily accesses the active tab only after a direct user action.

This access is limited to:

- obtaining text explicitly selected by the user;
- identifying the text field or editable element currently focused by the user; and
- inserting user-selected content at the current cursor position.

The extension does not maintain permanent access to all websites and does not collect browsing history.

## 9. Information Not Collected

The extension is not designed to collect or store:

- complete browsing history;
- passwords;
- financial information;
- payment-card information;
- health information;
- precise location information;
- authentication codes; or
- behavioral profiles for advertising.

Password, payment, and authentication fields are excluded from page-insertion functionality.

## 10. Data Sales and Advertising

The developer does not sell user data.

User data is not used for:

- personalized advertising;
- credit assessment;
- insurance assessment;
- third-party marketing; or
- profiling of user interests.

## 11. Data Retention and Deletion

Data stored in the browser’s local extension storage can be deleted by the user.

Users may delete stored data by:

- using an available data deletion feature in the extension;
- clearing the extension’s stored browser data; or
- uninstalling the extension.

Data transmitted to a third-party service is retained and deleted according to that service’s policies.

## 12. Security

The extension is designed to request only the permissions required for its user-facing features.

API keys and authentication information are processed only as needed to provide user-configured functions and are not transmitted to a developer-operated server.

No internet transmission or browser storage mechanism can be guaranteed to be absolutely secure. Users should also review the security and privacy policies of any external service they choose to use.

## 13. Children’s Privacy

The extension is not designed to intentionally collect personal information from children.

## 14. Changes to This Policy

This Privacy Policy may be updated when the extension’s features, permissions, or use of external services changes.

Material changes may be disclosed through the extension description or update notes.

## 15. Contact

Privacy-related inquiries may be submitted through the developer contact information displayed on the Chrome Web Store listing.
