# Isometric Tilemap

## Isometric Tilemap을 위한 준비
### 1. [Unity Hub 다운로드](https://unity3d.com/kr/get-unity/download)
### 2. Unity 2021.3.6f1 버전을 설치(안드로이드, ios 모듈 추가)
![image](https://user-images.githubusercontent.com/57660360/178693125-9218e138-a41a-4928-9466-55be6826aff9.png)

#### [Tilemap 기초](https://hiyotama.hatenablog.com/entry/2021/03/10/221323)
#### 참고 - 일본어, 1편부터 차근차근

### 3. Create New Project -> 2D -> Create
![image](https://user-images.githubusercontent.com/57660360/178693368-f2c6a040-8784-4942-9978-b6149a4f53c8.png)

### 4. Window -> Package Manager -> 2D Tilemap 관련 패키지 다운로드 (Package : Unity Registry로 변경)
![image](https://user-images.githubusercontent.com/57660360/178693753-8be22dd1-545f-458c-8927-819bfe73375e.png)

### 5. [Edit -> Project Settings -> Graphics -> Camera Settings 수정](https://blog.unity.com/technology/isometric-2d-environments-with-tilemap)
![image](https://user-images.githubusercontent.com/57660360/177670559-90ae06fd-9eba-434a-a92a-1440aff39c1c.png)

### 6. GameObject -> 2D Object -> Isometric Z As Y Tilemap
![image](https://user-images.githubusercontent.com/57660360/177670273-a64dcf57-e062-41eb-aaaa-ae5ea5ccef90.png)

### 7. Window -> 2D -> Tile Palette -> Create New Palette 
### -> Name(마음대로 설정), Grid(Isometric Z As Y), Cell Size(Manual - X : 1, Y : 0.5, Z : 1), Sort Mode(Custom Axis - X : 0, Y : 1, Z : -0.25)
![image](https://user-images.githubusercontent.com/57660360/178699284-d706df82-947e-46c6-bcc3-3d0d3fa0c888.png)

### 8. 생성된 Tile Palette에 준비한 Sprite를 드래그해서 Tile을 생성
![image](https://user-images.githubusercontent.com/57660360/177672333-e09f72a6-cb70-4180-b978-424272d0f98c.png)

#### ※주의할 점은 해당 Sprite의 Inspector창에서 Sprite Mode의 Pixels Per Unit을 Sprite의 X축 값(너비)으로 맞춰준다.
#### 그렇지 않으면 블럭 사이의 공간이 생기거나 블럭이 하나의 타일을 초과해서 생성된다. (밑의 예시는 60x60 을 Pixel Per Unit : 100)
![image](https://user-images.githubusercontent.com/57660360/177672883-1c13390f-9423-412b-99be-1c22427dc8e8.png)

### 9. 생성된 타일 맵 위에 다른 타일을 올려 높낮이를 표현하고자 할 때 겹친 현상이 발생
![image](https://user-images.githubusercontent.com/57660360/177673968-08442b89-1e0a-448f-ad69-c65c9e05abb1.png)
### 해당 현상을 방지하기 위해 Hierarchy -> Grid -> Tilemap -> Inspector창에서 Tilemap Renderer의 Mode를 Chunk -> Individual로 변경
![image](https://user-images.githubusercontent.com/57660360/177676803-ff83c647-6c81-4e56-8e16-1eb0a3012cf2.png)

### 10. [Rule Tile을 활용해 타일 맵 그리기](https://wergia.tistory.com/200)

### 사용시 주의점

#### 2D 엑스트라는 아직 유니티 테크놀러지 측에서도 개선 중인 기술로 룰 타일을 사용할 때, 주의해야할 점이 있다.
#### 타일 팔레트에 룰 타일을 올려둔 채로 씬의 타일맵에 계속 그려보면서 타일링 룰을 수정하면 어느 시점부터 심각한 수준의 메모리 누수가 발생한다. 특히 유니티 엔진이 응답없음 상태가 되고 메모리 점유율이 계속 올라가는 상태라면, 유니티를 종료하고 다시 실행해도 실행하자마자 메모리 누수가 시작될 확률이 높다.
#### 그렇기 때문에 룰 타일의 타일링 룰을 먼저 작성한 뒤 팔레트를 만들어서 룰 타일을 올리고 간단하게 씬에서 테스트한 뒤, 문제가 없다면 그대로 사용하고, 만약 타일링 룰을 수정해야 한다면, 현재 타일 팔레트를 삭제하고 타일링 룰을 수정한 뒤 다시 타일 팔레트를 만들 것을 권장한다.
