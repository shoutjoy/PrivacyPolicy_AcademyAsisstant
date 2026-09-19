# JJaIMsae Master 개인정보처리방침

**최종 수정일: 2026년 9월 19일**  
**시행일: 2026년 9월 19일**

JJaIMsae Master(이하 “본 확장 프로그램”)는 Suno에서 사용자가 만든 음악을 다운로드하거나, 사용자의 요청에 따라 음악 마스터링 및 등록 서비스로 전달하는 Chrome 확장 프로그램입니다. 개발자 박중희(이하 “개발자”)는 사용자의 개인정보와 콘텐츠를 중요하게 여기며, 본 방침을 통해 본 확장 프로그램이 어떤 정보를 처리하고, 언제 외부 서비스로 전달하며, 어떻게 보관·삭제하는지 설명합니다.

## 1. 처리하는 정보

본 확장 프로그램은 기능 제공을 위해 다음 정보를 처리할 수 있습니다.

### 1.1 사용자가 입력하거나 설정한 정보

- Suno Handle
- Suno 프로필 소유권 확인을 위해 생성되는 일회성 인증 코드
- 고정 메뉴 사용 여부, MP3 변환 여부, JJIM 기능 사용 여부, 기본 전송 대상 등 확장 프로그램 설정

인증 코드는 사용자가 Suno 프로필 인증을 진행하는 동안 브라우저의 확장 프로그램 로컬 저장소에 보관됩니다. 인증이 완료되거나 유효기간이 지나면 코드 값은 삭제되며, 인증된 Handle과 인증 상태·시각 정보가 남을 수 있습니다.

### 1.2 Suno 음악 및 페이지 관련 정보

사용자가 다운로드, SRT, ToMaster 또는 JJIM 기능을 직접 실행할 때 다음 정보가 처리될 수 있습니다.

- 곡 ID(GUID), 곡 제목 및 Suno 원본 주소
- 사용자가 재생한 곡의 오디오 데이터
- 커버 이미지
- 가사, 정렬 가사 및 이를 변환한 SRT 자막
- 곡 소유자의 Suno Handle
- 파일명, 파일 형식, 파일 크기 및 SHA-256 오디오 지문

본 확장 프로그램은 Suno에서 열린 모든 페이지의 전체 내용을 수집하거나 일반적인 웹 탐색 기록을 수집하지 않습니다. Suno 페이지에서 확장 기능을 제공하는 데 필요한 곡 정보와 사용자가 실행한 작업의 대상 정보만 처리합니다.

### 1.3 일시적인 Suno 인증 정보

SRT 생성에 필요한 정렬 가사를 Suno API에서 요청하기 위해, 본 확장 프로그램은 Suno 페이지의 API 요청에 사용되는 단기 Bearer 토큰을 일시적으로 감지하여 사용할 수 있습니다.

- 해당 토큰은 실행 중인 페이지와 확장 프로그램의 메모리에서만 일시적으로 사용됩니다.
- 토큰은 `chrome.storage.local` 또는 개발자 서버에 저장되지 않습니다.
- 토큰은 사용자가 소유한 곡의 정보와 정렬 가사를 Suno API에서 요청하는 용도로만 사용됩니다.
- 비밀번호, 결제정보 및 인증 쿠키를 수집하거나 저장하지 않습니다.

### 1.4 이용 기록 및 로컬 통계

본 확장 프로그램은 사용자의 브라우저 안에서 다음 기록을 저장할 수 있습니다.

- 다운로드 및 SRT 저장 기록: 곡 제목, 곡 ID·주소, 작업 시각, 파일명, 파일 크기, SHA-256 오디오 지문
- 마스터링·JJIM 전달 기록: 대상 기능, 곡 제목·주소, 파일명, 파일 크기, SHA-256 오디오 지문, 중복 여부, 전달 시각
- 누적 다운로드 수, 마지막 다운로드 파일명·시각
- 24시간 다운로드 사용량 및 초기화 시각
- 전송 진행 상태와 완료·실패 결과

오디오 지문은 파일의 동일성 및 중복 여부를 확인하기 위한 해시값이며, 원본 오디오를 복원하는 용도로 사용되지 않습니다.

## 2. 정보의 이용 목적

본 확장 프로그램은 위 정보를 다음 목적으로만 이용합니다.

- 사용자가 소유한 Suno 프로필과 곡인지 확인
- 사용자가 요청한 M4A 또는 MP3 오디오 파일과 SRT 파일 생성·저장
- 사용자가 요청한 곡, 커버 이미지, 가사 및 관련 정보를 마스터링 또는 음악 등록 화면으로 전달
- 다운로드·전송 진행 상태, 완료 알림, 사용량 및 기록 표시
- 동일한 오디오의 중복 전달 여부 확인
- 사용자가 선택한 설정 유지
- 오류 방지, 전송 무결성 확인 및 기능 보안 유지

본 확장 프로그램은 사용자 데이터를 맞춤형 광고, 신용·보험 평가, 사용자 행동 프로파일링, 제3자 마케팅 또는 데이터 판매 목적으로 사용하지 않습니다.

## 3. 외부 서비스와의 통신 및 정보 전달

본 확장 프로그램은 아래의 경우에만 HTTPS 연결 또는 브라우저의 제한된 창 간 통신 기능을 사용합니다. 다운로드, SRT, ToMaster 또는 JJIM 등 해당 기능은 사용자의 직접적인 버튼 조작과 확인 후 실행됩니다.

| 대상 | 전달되거나 조회될 수 있는 정보 | 목적 및 시점 |
| --- | --- | --- |
| Suno (`suno.com`, `studio-api.prod.suno.com`) | Suno Handle, 곡 ID, 단기 Bearer 토큰, 곡 소유자 정보 및 정렬 가사 요청 | 프로필·곡 소유권 확인 및 사용자가 요청한 SRT·가사 처리 |
| JJaIMsae Mastering (`masteringtools.vercel.app`) | 오디오 파일, SRT·가사, 커버 이미지, 파일명, 곡 ID·제목 및 원본 주소 | 사용자가 ToMaster 기능을 승인하고 실행한 경우 마스터링 화면에 파일과 관련 정보를 순차 입력 |
| 짜임새 (`jjaimsae.com`) | 오디오 파일, 커버 이미지, 파일명, 곡 ID·제목·원본 주소, 가사·SRT, 선택한 작업 유형 및 관련 마스터링 정보 | 사용자가 JJIM 마스터링·곡 등록·싱글앨범 등록 기능을 승인하고 실행한 경우 해당 화면에 자료를 입력 |

외부 서비스에 입력된 정보는 각 서비스의 서버로 업로드될 수 있으며, 이후의 저장·이용·삭제에는 해당 서비스의 이용약관과 개인정보처리방침이 적용됩니다. 사용자는 민감하거나 공개를 원하지 않는 내용이 포함되지 않았는지 확인한 뒤 전송 기능을 사용해야 합니다.

본 확장 프로그램은 위 기능 수행과 무관한 분석·광고·추적 서버로 사용자의 오디오, 가사, 인증 정보 또는 이용 기록을 자동 전송하지 않습니다.

## 4. 로컬 저장과 보유기간

대부분의 설정과 이용 기록은 사용자의 브라우저 내 `chrome.storage.local`에 저장됩니다.

- 설정, 프로필 인증 상태, 다운로드·전송 기록 및 통계: 사용자가 직접 삭제하거나 확장 프로그램을 제거할 때까지 보관될 수 있습니다.
- 인증 대기 코드: 생성 후 최대 2시간 동안 유효하며, 인증 완료 또는 만료 처리 시 코드 값이 삭제됩니다.
- Suno Bearer 토큰: 메모리에서만 일시 사용되며 영구 저장하지 않습니다.
- JJIM 전송용 오디오·커버 이미지·가사·SRT 및 메타데이터: 대상 페이지로 전달하기 위해 브라우저 확장 저장소에 조각 형태로 임시 보관될 수 있습니다. 정상 전달이 완료되면 관련 파일 조각과 대기 정보가 삭제됩니다. 대기 정보는 생성 후 10분이 지나 복원 절차가 실행될 때 만료 자료로 삭제되며, 전송 중단 또는 예외 상황에서는 사용자가 브라우저의 확장 프로그램 데이터를 삭제하거나 본 확장 프로그램을 제거할 때까지 남을 수 있습니다.
- 전송 진행·결과 정보: 화면 간 진행 상태 표시를 위해 일시 저장되며, 후속 작업 또는 확장 프로그램 데이터 삭제 시 제거됩니다.

일부 JJIM 전송 경로에서는 임시 파일 조각이 AES-GCM으로 암호화됩니다. 다른 전송 경로에서는 브라우저 확장 저장소에 Base64 형태로 임시 보관될 수 있습니다. Base64는 암호화 방식이 아닙니다.

## 5. 삭제 및 사용자의 선택권

사용자는 다음 방법으로 정보를 관리하거나 삭제할 수 있습니다.

- 확장 프로그램의 설정을 변경하여 MP3 변환, 고정 메뉴 또는 JJIM 기능을 끌 수 있습니다.
- 브라우저의 확장 프로그램 데이터 또는 사이트 데이터를 삭제할 수 있습니다.
- 본 확장 프로그램을 제거하면 브라우저가 관리하는 확장 프로그램 로컬 저장 데이터가 삭제됩니다.
- 전송 확인창에서 취소하면 해당 다운로드 또는 외부 전달 작업은 시작되지 않습니다.
- 확장 프로그램 권한을 해제하거나 확장 프로그램 사용을 중지할 수 있습니다. 이 경우 관련 기능이 제한될 수 있습니다.

이미 Suno, JJaIMsae Mastering 또는 짜임새에 전달된 정보의 열람·수정·삭제는 해당 서비스의 정책과 기능에 따라 처리해야 합니다.

## 6. 브라우저 권한의 이용

본 확장 프로그램은 다음 권한을 사용합니다.

- `storage`, `unlimitedStorage`: 설정, 인증 상태, 이용 기록, 통계 및 임시 전송 파일 저장
- `notifications`: 오디오 파일 저장 완료 알림 표시
- Suno 도메인 접근: 곡 정보 확인, 오디오 처리, 프로필·곡 소유권 확인 및 가사·SRT 기능 제공
- `masteringtools.vercel.app`, `jjaimsae.com` 페이지 접근: 사용자가 승인한 오디오와 관련 정보를 해당 서비스의 입력 화면으로 전달

본 확장 프로그램은 브라우저의 전체 방문 기록을 읽는 권한을 요청하지 않습니다.

## 7. 안전성 확보 조치

본 확장 프로그램은 다음과 같은 보호 조치를 적용합니다.

- 외부 서비스와의 통신에 HTTPS 사용
- 전송 대상 origin과 메시지 출처 확인
- 곡 ID, 파일 형식, 파일 크기, 인증 코드 및 전송 식별자 형식 검증
- Suno Bearer 토큰의 비영구 저장 및 인증 실패 시 폐기
- 파일 무결성·중복 확인을 위한 SHA-256 해시 사용
- 지원되는 일부 전송 경로에서 AES-GCM 암호화 사용
- 사용자가 직접 실행하고 확인한 작업에 한해 다운로드 또는 외부 전달 진행

다만 인터넷 전송이나 브라우저 저장 방식의 절대적인 안전성을 보장할 수는 없습니다. 사용자는 기기와 브라우저 계정을 안전하게 관리하고, 연동 서비스의 보안 및 개인정보처리방침도 함께 확인해야 합니다.

## 8. 아동의 개인정보

본 확장 프로그램은 아동의 개인정보를 의도적으로 수집하도록 설계되지 않았습니다. 법정대리인의 동의가 필요한 연령의 사용자는 관련 법령과 이용하는 외부 서비스의 연령 요건을 따라야 합니다.

## 9. 개인정보의 판매 및 광고 이용 금지

개발자는 본 확장 프로그램이 처리하는 사용자 데이터를 판매하지 않으며, 개인 맞춤형 광고, 재타기팅 광고 또는 관심사 기반 광고에 사용하거나 이를 위해 제3자에게 제공하지 않습니다.

본 확장 프로그램이 브라우저 권한 또는 웹사이트에서 얻은 정보를 사용하는 경우, 그 이용은 본 방침에 공개된 단일 목적과 사용자-facing 기능 제공에 한정됩니다.

## 10. 개인정보처리방침의 변경

본 확장 프로그램의 기능, 권한, 연동 대상 또는 관련 법령이 변경되면 본 방침도 변경될 수 있습니다. 중요한 변경이 있는 경우 Chrome 웹 스토어 설명, 업데이트 안내 또는 확장 프로그램 화면 등 적절한 방법으로 알립니다.

## 11. 문의처

- 개발자: 박중희
- 이메일: shoutjoy1@gmail.com

개인정보 또는 데이터 삭제에 관한 문의는 위 연락처로 요청할 수 있습니다.

---

# Privacy Policy for JJaIMsae Master

**Last updated: September 19, 2026**  
**Effective date: September 19, 2026**

JJaIMsae Master (the “Extension”) is a Chrome extension that helps users download music they created on Suno and, at the user's request, transfer music to mastering and music-registration services. This policy explains what information the Extension processes, when information is transferred to an external service, and how information is stored and deleted.

## 1. Information processed

The Extension may process:

- a Suno Handle and a temporary profile-verification code;
- extension preferences, including menu, MP3 conversion, JJIM, and transfer-target settings;
- song IDs, titles, Suno source URLs, ownership information, audio, cover images, lyrics, aligned lyrics, and SRT subtitles selected by the user;
- filenames, file formats, file sizes, and SHA-256 audio fingerprints;
- local download and transfer history, timestamps, duplicate status, counters, quotas, and progress or result status; and
- a short-lived Suno Bearer token when required to retrieve aligned lyrics for a user-owned song.

The Extension does not collect a user's general browsing history or automatically collect the full content of every webpage the user visits.

## 2. Authentication information

The short-lived Suno Bearer token is detected only to make the Suno API requests required for the aligned-lyrics and SRT features. It is held temporarily in memory, is not saved to `chrome.storage.local`, and is not sent to a developer-operated analytics or storage server. The Extension does not collect or store passwords, payment information, or authentication cookies.

The profile-verification code is stored locally while verification is pending. It is valid for up to two hours and is cleared after successful verification or expiration. The verified Suno Handle and verification timestamps may remain stored locally.

## 3. Purposes of processing

Information is used only to:

- verify that the Suno profile and song belong to the user;
- create and save user-requested M4A, MP3, or SRT files;
- transfer user-selected audio and related content to a mastering or registration workflow;
- display settings, progress, completion notifications, history, and quota information;
- detect duplicate audio transfers; and
- maintain functionality, integrity, and security.

The Extension does not use user data for personalized advertising, credit or insurance assessment, behavioral profiling, third-party marketing, or sale of data.

## 4. External services and disclosures

External communication occurs only as necessary for a feature directly invoked by the user.

| Service | Information that may be sent or retrieved | Purpose |
| --- | --- | --- |
| Suno (`suno.com`, `studio-api.prod.suno.com`) | Suno Handle, song ID, short-lived Bearer token, song-owner information, and aligned-lyrics requests | Profile and song-ownership verification; lyrics and SRT processing |
| JJaIMsae Mastering (`masteringtools.vercel.app`) | Audio, SRT or lyrics, cover image, filename, song ID, title, and source URL | Sequentially populate the mastering workflow after the user approves and invokes ToMaster |
| JJaIMsae (`jjaimsae.com`) | Audio, cover image, filename, song ID, title, source URL, lyrics or SRT, selected workflow, and related mastering information | Populate the mastering, track-upload, or single-album workflow after the user approves and invokes JJIM |

Information entered into an external service may subsequently be uploaded to that service's servers and is then governed by that service's terms and privacy policy. The Extension does not automatically send audio, lyrics, authentication information, or usage history to unrelated analytics, advertising, or tracking services.

## 5. Local storage and retention

Most settings and usage records are stored in the user's browser through `chrome.storage.local`.

- Preferences, verification status, history, and statistics may remain until the user clears extension data or uninstalls the Extension.
- Pending verification codes expire after two hours and are cleared upon verification or expiration.
- Suno Bearer tokens are used temporarily in memory and are not persistently stored.
- Audio, cover images, lyrics, SRT, and metadata may be temporarily stored in chunks to complete a JJIM transfer. They are deleted after a successful import. A pending package is treated as expired after ten minutes when the restore process next runs. If a transfer is interrupted or an exception occurs, temporary data may remain until the user clears extension data or uninstalls the Extension.
- Progress and result records are stored temporarily to coordinate screens and are removed by a later workflow or when extension data is cleared.

Some JJIM transfer paths encrypt temporary chunks using AES-GCM. Other paths may temporarily store chunks in Base64 form in extension-local storage; Base64 is not encryption.

## 6. User controls and deletion

Users can disable optional features in the Extension, cancel a download or transfer before it starts, clear browser extension data, revoke permissions, disable the Extension, or uninstall it. Uninstalling the Extension causes the browser-managed extension-local data to be removed.

Information already submitted to Suno, JJaIMsae Mastering, or JJaIMsae must be accessed, corrected, or deleted under the applicable service's policies and controls.

## 7. Permissions

The Extension uses:

- `storage` and `unlimitedStorage` for preferences, verification state, history, statistics, and temporary transfer files;
- `notifications` to display audio-save completion messages;
- access to Suno domains for song information, audio processing, ownership verification, and lyrics or SRT features; and
- access to `masteringtools.vercel.app` and `jjaimsae.com` to place user-approved audio and related content into the selected workflow.

The Extension does not request permission to read the user's complete browser history.

## 8. Security

The Extension uses HTTPS for external communication, checks message sources and destination origins, validates identifiers and file metadata, avoids persistent storage of the Suno Bearer token, uses SHA-256 for integrity and duplicate checks, and uses AES-GCM on supported temporary-transfer paths. Downloads and external transfers require a direct user action and confirmation.

No internet transmission or browser storage mechanism can be guaranteed to be completely secure. Users should secure their device and browser account and review the privacy and security practices of any connected service they choose to use.

## 9. Children's privacy

The Extension is not designed to intentionally collect personal information from children. Users who are below the age at which parental consent is required must comply with applicable law and the age requirements of connected services.

## 10. No sale or advertising use

The developer does not sell Extension user data and does not use it for personalized, retargeted, or interest-based advertising. Data obtained through browser permissions or website access is limited to the Extension's disclosed single purpose and user-facing features.

## 11. Changes to this policy

This policy may be updated when the Extension's features, permissions, connected services, or applicable requirements change. Material changes may be announced through the Chrome Web Store listing, release notes, or the Extension interface.

## 12. Contact

- Developer: Junghee Park (박중희)
- Email: shoutjoy1@gmail.com

Privacy and data-deletion inquiries may be submitted through that contact channel.
