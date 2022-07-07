# Isometric Tilemap

## Isometric Tilemap을 위한 준비
### 1. [Unity 2019.4.36f1 버전을 다운로드](https://unity3d.com/kr/unity/whats-new/2019.4.36)
### 2. Create New Project -> 2D -> Create
![image](https://user-images.githubusercontent.com/57660360/177669401-696754a8-ae2e-4b5b-b4e7-3bfc987a5c97.png)

### 3. GameObject -> 2D Object -> Isometric Z As Y Tilemap
![image](https://user-images.githubusercontent.com/57660360/177670273-a64dcf57-e062-41eb-aaaa-ae5ea5ccef90.png)

### 4. Edit -> Project Settings -> Graphics -> Camera Settings 수정
![image](https://user-images.githubusercontent.com/57660360/177670559-90ae06fd-9eba-434a-a92a-1440aff39c1c.png)

### 5. Window -> 2D -> Tile Palette -> Create New Palette 
### -> Name(마음대로 설정), Grid(Isometric Z As Y), Cell Size(Manual - X : 1, Y : 0.5, Z : 1)
![image](https://user-images.githubusercontent.com/57660360/177671359-da62d81b-78c3-4e09-958e-5255e3c3fb96.png)

### 6. 생성된 Tile Palette에 준비한 Sprite를 드래그해서 Tile을 생성
![image](https://user-images.githubusercontent.com/57660360/177672333-e09f72a6-cb70-4180-b978-424272d0f98c.png)

#### ※주의할 점은 해당 Sprite의 Inspector창에서 Sprite Mode의 Pixels Per Unit을 Sprite의 X축 값(너비)으로 맞춰준다.
#### 그렇지 않으면 블럭 사이의 공간이 생기거나 블럭이 하나의 타일을 초과해서 생성된다. (밑의 예시는 60x60 을 Pixel Per Unit : 100)
![image](https://user-images.githubusercontent.com/57660360/177672883-1c13390f-9423-412b-99be-1c22427dc8e8.png)

### 7. 생성된 타일 맵 위에 다른 타일을 올려 높낮이를 표현하고자 할 때 겹친 현상이 발생
![image](https://user-images.githubusercontent.com/57660360/177673968-08442b89-1e0a-448f-ad69-c65c9e05abb1.png)
### 해당 현상을 방지하기 위해 Hierarchy -> Grid -> Tilemap -> Inspector창에서 Tilemap Renderer의 Mode를 Chunk -> Individual로 변경
![image](https://user-images.githubusercontent.com/57660360/177676803-ff83c647-6c81-4e56-8e16-1eb0a3012cf2.png)
