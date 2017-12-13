---

copyright:

  years: 2015, 2017
lastupdated: "2017-08-01"

---

{:new_window: target="_blank"}  
{:shortdesc: .shortdesc}


# 새 서비스 신임 정보 추가
{: #service_credentials}

외부 이용자를 Bluemix 서비스에 수동으로 연결하려는 케이스에 대한 새 서비스 신임 정보 세트를 생성할 수 있습니다. 예를 들어, AWS 앱을 Watson 서비스에 바인드하려는 경우 이 두 개의 서비스를 함께 바인드하는 데 사용할 수 있는 새 서비스 신임 정보를 생성해야 합니다. 

Cloud Foundry 서비스로 서비스 신임 정보라고도 하는 서비스 키를 생성할 수 있습니다. 서비스 신임 정보는 서비스별로 고유하며 각 서비스가 생성해야 하는 신임 정보를 정의하는 방식에 따라 다양합니다. 서비스 신임 정보에는 사용자 이름, 비밀번호, 호스트 이름, 포트 및 URL이 포함될 수 있습니다. 그러나 각 서비스 신임 정보의 컨텐츠는 그것을 생성하는 서비스에 고유합니다. 일부 서비스에서는 매개변수가 전달되어야 하는 추가 데이터를 생성할 수 있습니다. 예를 들어, 서비스는 생성된 서비스 키에 리턴되는 기본 언어를 설정하려면 사용자가 언어 매개변수를 입력해야 합니다.  

새 서비스 신임 정보를 추가하려면 다음 단계를 완료하십시오.

1. 서비스 세부사항 페이지에서 서비스 신임 정보 탭을 선택하고 **새 신임 정보 + **를 클릭하십시오.
2. 새 신임 정보 추가 대화 상자에 **이름**을 입력하십시오.
3. 선택사항으로 인라인 또는 파일로 제공되는, 서비스 특정 구성 매개변수를 포함하는 올바른 JSON 오브젝트로 추가 매개변수를 제공할 수 있습니다. 

  **참고**. 대부분의 서비스에는 추가 매개변수가 필요하지 않으며, 추가 매개변수가 필요한 서비스에 대해서는 각 서비스가 자체적으로 매개변수의 고유 목록을 정의합니다. 지원되는 구성 매개변수의 목록은 특정 서비스 오퍼링에 대한 문서를 참조하십시오. 
4. **추가**를 클릭하여 새 서비스 신임 정보를 생성하십시오. 