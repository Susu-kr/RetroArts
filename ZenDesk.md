# ZenDesk Support

## 1. ZenDesk를 사용하는 목적

---

현재 카페의 문의 내역을 실시간으로 확인하기 힘들며, 메일 답변을 보냈을 시 스팸 메일로 분류되는 상황

이러한 고객과의 소통을 더 원활하게 해줄 수 있는 **ZenDesk Support**를 활용하기로 회의에 건의

## 2. ZenDesk 사용방법

---

### **2-1) 티켓 구성**

### **채널** (커뮤니케이션 목록)

---

- 이메일 보내기
- 회사 웹사이트에서 지원 요청 양식 작성
- 전화로 연락
- 문자 메시지를 통한 채팅
- ~~젠 데스크 서포트 포털에서 지원 요청 양식 작성~~
- ~~트윗 보내기~~
- ~~페이스북 담벼락에 게시~~

위의 채널들 중 고객과 연락할 수 있는 방법을 결정, 또한 현재 사용중인 Slack에 젠 데스크 계정을 추가하여 고객과 소통하는 더 많은 방법을 구현

모든 채널(젠 데스크에서 설정한 채널)에서 받는 모든 지원 요청이 **Zendesk Support Ticket** 으로 변환, 티켓은 이메일과 형식이 매우 유사

<center>

![Ticket1](https://support.zendesk.com/hc/article_attachments/4408894986266/ticket_anatomy_top.png)

</center>

<center>

![Ticket2](https://zen-marketing-documentation.s3.amazonaws.com/docs/en/ticket_anatomy_main2.png)

</center>

### **댓글 영역**

---

- 공개 답장 : 해당 티켓을 보는 모든 사람이 볼 수 있도록 공개된다.

- 참조 필드 : 다른 외부 사용자를 답장의 참조 목록에 추가할 수 있다.

- 내부 메모 : 고객에게는 보이지 않고 내부 커뮤니케이션용으로 사용 가능하다.

- 매크로를 사용해 단일 표준 응답으로 답변할 수 있다.

### **티켓 사용자 유형**

---

- 모든 티켓에는 **요청자**(지원을 요청한 고객)의 이름이 포함되어 있다.

- 상담원이 티켓에 배정되면 **담당자**가 된다.

- 상담원이 고객 대신 티켓을 등록하면 해당 상담원은 **제출자**가 된다.

- 다른 내부 사용자를 상담원이 초대(참조)하면 이들은 **팔로워**가 된다.

### **티켓을 배정하는 방법**

---

- 티켓의 담당자 필드 옆의 아래쪽 화살표 클릭하여 본인의 이름을 선택하거나, 나에게 배정을 클릭

- 해당 티켓의 유형 및 우선 순위 필드를 설정할 수 있다. (초기 옵션 - 유형 : 문제, 우선 순위 : 보통)

- 위의 변경 내용을 저장하려면 신규로 제출 버튼을 클릭

- 티켓을 상담원에게 배정하면 해당 티켓이 자동으로 "등록"으로 설정된다.

### **티켓 수명 주기**

---

<center>

![TicketLife](https://zen-marketing-documentation.s3.amazonaws.com/docs/ko/gsg_submit_button.png)

</center>

- 신규 : 고객으로 부터 요청이 처음 도착

- 등록 : 상담원이 티켓에 배정

- 보류 : 상담원이 고객에게 후속 질문

- 해결 : 상담원이 문제를 해결

- 종료 : 특정 일수가 지난 티켓이며 참조할 수 있도록 보관(상담원이 티켓을 직접 종료로 제출할 수 없음)

- 해당 상담원의 답변을 고객이 만족하지 않는다면 **해결**된 티켓에 **재요청**이 가능하며 요청시 티켓은 재등록된다.

- 티켓의 수명별로 검색하여 모든 티켓을 빠르게 볼 수 있다.

- 고객이 받은 지원에 만족하는지 간단한 설문 조사를 보내도록 설정할 수 있다.

### **2-2) 티켓 및 사용자 구성**

### **보기**

---

<center>

![View](https://zen-marketing-documentation.s3.amazonaws.com/docs/ko/gsg_unassigned_tickets_new_thumb.png)

</center>

보기는 티켓의 특성에 따라 티켓을 구성하므로 두 개 이상 티켓이 보기에 나타날 수 있다. 새 보기를 만들거나 필요에 맞게 기존의 보기를 수정할 수 있다.

<center>

![View2](https://zen-marketing-documentation.s3.amazonaws.com/docs/en/gsg_view_available_for.png)

</center>

- 공유 보기 : Zendesk 계정에서 제공되는 미리 정의된 보기

- 제한 보기 : 특정 상담원 그룹만 볼 수 있는 보기(관리자만 설정 가능)
- 개인용 보기 : 본인만 액세스할 수 있는 보기(모든 상담원이 설정 가능)

### **나만의 보기 생성 방법**

---

- 보기 아이콘
![View3](https://zen-marketing-documentation.s3.amazonaws.com/docs/en/views_icon.png)

- 보기 목록 아래의 **더 보기** 클릭 후 **보기 추가** 클릭

<center>

![View4](https://zen-marketing-documentation.s3.amazonaws.com/docs/en/support_intro_assignee.png)

</center>

- 제목 입력
  
- 티켓 : 담당자 / is / (현재 사용자) 또는 상담원 목록의 본인 이름 선택
  
- **위의 조건과 일치하는 항목 미리보기**를 클릭하면 정의한 조건의 결과를 바로 볼 수 있다.
  
- 보기를 정의할 때 서식과 해당 보기에 액세스할 수 있는 사람도 정의할 수 있다.
  
- 보기 만들기

### **그룹으로 상담원 및 티켓 세분화하기**

---

Zendesk Support에서는 상담원을 그룹으로 구성하며 티켓을 상담원에게 배정하면 그 상담원이 속한 그룹에도 배정된다. 그리고 상담원은 두 개 이상의 그룹에 속할 수 있다. 또한, 티켓을 그룹에만 배정하고 그룹 내 특정 상담원에게는 배정하지 않을 수도 있다.

- 관리자 아이콘
![View6](https://zen-marketing-documentation.s3.amazonaws.com/docs/en/manage_icon.png)

- 사람 관리 페이지 위의 그룹 추가를 클릭
  
<center>

![View5](https://zen-marketing-documentation.s3.amazonaws.com/docs/en/gsg_group_new.png)

</center>

- 제목 입력 후 그룹에 배정할 상담원을 선택 한 후 그룹 생성

## 3. 젠 데스크의 총 비용
