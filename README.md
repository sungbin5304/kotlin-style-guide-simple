# kotlin-style-guide-simple
코틀린 스타일 가이드 간략화 버전
> 원본 : [Google](https://developer.android.com/kotlin/style-guide?hl=ko)

### 들어가기 전
`KDoc 구문` : `JavaScript`에서 사용되는 구석 스타일이며, `/**`으로 시작해서 `*/`으로 끝난다.<br />
모든 블록은 @으로 시작한다.

# 파일 구조
1. 저작권 (선택, 주석)
2. 파일 수준 (주석)
3. `package` 구문
4. `import` 문
5. 최상위 수준 선언

# 주석
1. `KDoc` 스타일 비허용
2. `*` 는 한 줄 주석일 때, 맨 앞에 

# 다음과 같은 코딩 스타일 지향
```kotlin
if (A) return

while (A) {
    case B -> return
}
```

# 줄바꿈
1. 여는 중괄호 앞 줄바꿈 비허용
2. 열거나 닫는 중괄호 앞 줄바꿈
3. 중괄호로 작업이 종료된 경우, 그리고 빈 내용이여도 줄바꿈
> ```kotlin
> if (A) {
>     B
> } else {
> }
> ```

# 중괄호
1. `if`-`else` 한 줄 씩 만은 중괄호 생략

# 들여쓰기
1. 4칸, 주석 포함

# 줄바꿈
1. 한 줄 당 최대 100글자만 허용. -> 100글자 넘어갈 시 줄바꿈
> 예외) `import`문, `package`문, URI
2. `.`, `?.`, `::`, `=`, 앞에서 줄바꿈
> `( )`, `,` 앞 토큰, `람다식` (->) 앞 인자 들과 연결 된 상태로 줄바꿈

# 함수
1. 인자가 없으면 각각 하나하나씩 한 줄로 표시
> 닫는 괄호는 새 라인에 들여쓰기 없이 작성

# 읽기 전용 변수 (only getter variable)
1. 한 줄로 표시
> ```kotlin
> val getA: String get() = "A"
> ```

# 소괄호 앞 띄어쓰기
1. `예약어`, `여는 중괄호 앞`, `연산자` (수식), `람다식` (->) 앞에서 띄어쓰기

# 띄어쓰기 사용
1. 상속 클론 (`A : B`) 앞 뒤, 클론(`:`)과 쉼표(`,`) 뒤, 주석(`//`) 뒤 

# 띄어쓰기 비허용
1. 두 클론 앞 뒤 (`::`), `.` 앞 뒤, 범위연산자 (`..`) 앞 뒤

# 네이밍
1. `상수` - 모두 대문자로 작성, \_로 단어 구분
2. 기타 - `camelCase`로 작성, `단어 구분`만 대문자로 표시
#### 예) 스톱워치 변수일 때
허용 : 
```kotlin
lateinit var Stopwatch: Clock
             ^^^^^^^^^
``` 
<br />
비허용 : 
```kotlin
lateinit var StopWatch: Clock
             ^^^^^^^^^
```

# 변수-인자 네이밍
1. 변수에 _ 접두사로 네이밍, 인자는 _ 없이 그대로 

# 기타 규칙
1. `인자` 없는 `어노테이션`은 한 줄로 작성
2. 값 바로 초기화시, 타입 명시 생략
