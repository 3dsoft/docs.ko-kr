# [WCF를 사용하여 개발한 서비스 기반 응용 프로그램](index.md)
## [Windows Communication Foundation 4.5의 새로운 기능](whats-new.md)
## [WCF 단순화 기능](wcf-simplification-features.md)
## [설명서에 대한 안내](guide-to-the-documentation.md)
## [개념적 개요](conceptual-overview.md)
### [Windows Communication Foundation 정의](whats-wcf.md)
### [기본적인 Windows Communication Foundation 개념](fundamental-concepts.md)
### [Windows Communication Foundation 아키텍처](architecture.md)
### [WCF 및 .NET Framework 클라이언트 프로필](wcf-and-net-framework-client-profile.md)
## [초보자를 위한 자습서](getting-started-tutorial.md)
### [방법: 서비스 계약 정의](how-to-define-a-wcf-service-contract.md)
### [방법: 서비스 계약 구현](how-to-implement-a-wcf-contract.md)
### [방법: 기본 서비스 호스트 및 실행](how-to-host-and-run-a-basic-wcf-service.md)
### [방법: 클라이언트 만들기](how-to-create-a-wcf-client.md)
### [방법: 클라이언트 구성](how-to-configure-a-basic-wcf-client.md)
### [방법: 클라이언트 사용](how-to-use-a-wcf-client.md)
### [초보자를 위한 자습서 문제 해결](troubleshooting-the-getting-started-tutorial.md)
## [기본 WCF 프로그래밍](basic-wcf-programming.md)
### [기본 프로그래밍 수명 주기](basic-programming-lifecycle.md)
### [서비스 디자인 및 구현](designing-and-implementing-services.md)
#### [서비스 계약 디자인](designing-service-contracts.md)
##### [계약 및 서비스에서 오류 지정 및 처리](specifying-and-handling-faults-in-contracts-and-services.md)
###### [오류 정의 및 지정](defining-and-specifying-faults.md)
####### [방법: 서비스 계약에 오류 선언](how-to-declare-faults-in-service-contracts.md)
###### [오류 보내기 및 받기](sending-and-receiving-faults.md)
##### [세션 사용](using-sessions.md)
##### [동기 및 비동기 작업](synchronous-and-asynchronous-operations.md)
###### [방법: 비동기 서비스 작업 구현](how-to-implement-an-asynchronous-service-operation.md)
##### [신뢰할 수 있는 서비스](reliable-services.md)
##### [서비스 및 트랜잭션](services-and-transactions.md)
#### [서비스 계약 구현](implementing-service-contracts.md)
##### [서비스 런타임 동작 지정](specifying-service-run-time-behavior.md)
### [서비스 구성](configuring-services.md)
#### [단순화된 구성](simplified-configuration.md)
#### [구성 파일을 사용하여 서비스 구성](configuring-services-using-configuration-files.md)
#### [코드로 WCF 서비스 구성](configuring-wcf-services-in-code.md)
#### [바인딩](bindings.md)
##### [WCF 바인딩 개요](bindings-overview.md)
##### [시스템 제공 바인딩](system-provided-bindings.md)
##### [바인딩을 사용하여 서비스 및 클라이언트 구성](using-bindings-to-configure-services-and-clients.md)
###### [방법: 코드에서 클라이언트 바인딩 지정](how-to-specify-a-client-binding-in-code.md)
###### [방법: 구성에서 클라이언트 바인딩 지정](how-to-specify-a-client-binding-in-configuration.md)
###### [방법: 코드에서 서비스 바인딩 지정](how-to-specify-a-service-binding-in-code.md)
###### [방법: 구성에서 서비스 바인딩 지정](how-to-specify-a-service-binding-in-configuration.md)
##### [서비스에 대한 바인딩 구성](configuring-bindings-for-wcf-services.md)
#### [끝점](endpoints.md)
##### [끝점 만들기 개요](endpoint-creation-overview.md)
##### [끝점 주소 지정](specifying-an-endpoint-address.md)
##### [메타데이터 끝점 게시](publishing-metadata-endpoints.md)
#### [서비스에 보안 설정](securing-services.md)
##### [방법: Windows 자격 증명을 사용하여 서비스에 보안 설정](how-to-secure-a-service-with-windows-credentials.md)
##### [방법: 보안 모드 설정](how-to-set-the-security-mode.md)
##### [방법: 클라이언트 자격 증명 형식 지정](how-to-specify-the-client-credential-type.md)
##### [방법: PrincipalPermissionAttribute 클래스를 사용하여 액세스 제한](how-to-restrict-access-with-the-principalpermissionattribute-class.md)
##### [방법: 서비스에서 클라이언트 가장](how-to-impersonate-a-client-on-a-service.md)
##### [방법: 보안 컨텍스트 검사](how-to-examine-the-security-context.md)
##### [보호 수준 이해](understanding-protection-level.md)
##### [방법: ProtectionLevel 속성 설정](how-to-set-the-protectionlevel-property.md)
#### [WS-I Basic Profile 1.1 상호 운용할 수 있는 서비스 만들기](creating-ws-i-basic-profile-1-1-interoperable-services.md)
### [서비스 호스팅](hosting-services.md)
#### [방법: 관리되는 응용 프로그램에서 WCF 서비스 호스트](how-to-host-a-wcf-service-in-a-managed-application.md)
#### [방법: .NET Framework 4에서 실행되는 IIS에서 .NET Framework 3.5를 사용하여 작성한 WCF 서비스 호스트](host-a-wcf-service-net-framework-3-5-iis--net-framework-4.md)
### [클라이언트 빌드](building-clients.md)
#### [WCF 클라이언트 개요](wcf-client-overview.md)
#### [WCF 클라이언트를 사용하여 서비스 액세스](accessing-services-using-a-wcf-client.md)
##### [이식 가능한 하위 집합 프로젝트에 서비스 참조 추가](add-service-reference-in-a-portable-subset-project.md)
##### [클라이언트 런타임 동작 지정](specifying-client-run-time-behavior.md)
##### [클라이언트 동작 구성](configuring-client-behaviors.md)
#### [클라이언트에 보안 설정](securing-clients.md)
##### [방법: 클라이언트 자격 증명 값 지정](how-to-specify-client-credential-values.md)
### [확장성 소개](introduction-to-extensibility.md)
### [WCF 문제 해결 퀵 스타트](wcf-troubleshooting-quickstart.md)
### [WCF 오류 처리](wcf-error-handling.md)
### [WCF 및 ASP.NET Web API](wcf-and-aspnet-web-api.md)
## [WCF 기능 정보](feature-details/)
## [WCF 확장](extending/)
## [지침 및 모범 사례](guidelines-and-best-practices.md)
### [모범 사례: 데이터 계약 버전 관리](best-practices-data-contract-versioning.md)
### [모범 사례: 중간](best-practices-intermediaries.md)
### [서비스 버전 관리](service-versioning.md)
### [부하 분산](load-balancing.md)
### [리소스 사용 제어 및 성능 향상](controlling-resource-consumption-and-improving-performance.md)
### [ClickOnce를 사용하여 WCF 응용 프로그램 배포](deploying-wcf-applications-with-clickonce.md)
## [관리 및 진단](diagnostics/)
## [시스템 요구 사항](wcf-system-requirements.md)
## [WCF에 필요한 운영 체제 리소스](operating-system-resources-required-by-wcf.md)
## [설치 문제 해결](troubleshooting-setup-issues.md)
## [.NET Remoting에서 WCF로 마이그레이션](migrating-from-net-remoting-to-wcf.md)
## [WCF 개발 도구 사용](using-the-wcf-development-tools.md)
### [WCF 서비스 호스트(WcfSvcHost.exe)](wcf-service-host-wcfsvchost-exe.md)
### [WCF 테스트 클라이언트(WcfTestClient.exe)](wcf-test-client-wcftestclient-exe.md)
### [WCF Visual Studio 템플릿](wcf-vs-templates.md)
### [WCF 서비스 게시](wcf-service-publishing.md)
### [WCF 서비스 이름 바꾸기](renaming-a-wcf-service.md)
### [WCF 라이브러리 프로젝트 배포](deploying-a-wcf-library-project.md)
### [WCF 서비스 호스트 자동 시작 제어](controlling-auto-launching-of-wcf-service-host.md)
### [XML에서 데이터 형식 클래스 생성](generating-data-type-classes-from-xml.md)
## [Windows Communication Foundation 도구](tools.md)
### [ServiceModel Metadata 유틸리티 도구(Svcutil.exe)](servicemodel-metadata-utility-tool-svcutil-exe.md)
### [개인 키 찾기 도구(FindPrivateKey.exe)](find-private-key-tool-findprivatekey-exe.md)
### [ServiceModel 등록 도구(ServiceModelReg.exe)](servicemodelreg-exe.md)
### [Service Trace Viewer 도구(SvcTraceViewer.exe)](service-trace-viewer-tool-svctraceviewer-exe.md)
### [Configuration Editor 도구(SvcConfigEditor.exe)](configuration-editor-tool-svcconfigeditor-exe.md)
### [COM+ 서비스 모델 구성 도구(ComSvcConfig.exe)](com-service-model-configuration-tool-comsvcconfig-exe.md)
### [WS-AtomicTransaction 구성 유틸리티(wsatConfig.exe)](ws-atomictransaction-configuration-utility-wsatconfig-exe.md)
#### [wsatConfig.exe에서 반환된 오류 코드 해석](interpreting-error-codes-returned-by-wsatconfig-exe.md)
### [WS-AtomicTransaction 구성 MMC 스냅인](ws-atomictransaction-configuration-mmc-snap-in.md)
### [워크플로 서비스 등록 도구(WFServicesReg.exe)](workflow-service-registration-tool-wfservicesreg-exe.md)
### [계약 중심 도구](contract-first-tool.md)
## [Windows Communication Foundation 샘플](samples/)
## [Windows Communication Foundation 용어](glossary.md)
## [일반 참조](general-reference.md)
## [사용자 의견 및 커뮤니티](feedback-and-community.md)
## [개인 정보](privacy-information.md)
