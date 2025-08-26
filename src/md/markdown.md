# 마크다운 문법
## 1. 마크다운이란?
[**Markdown**](https://www.markdownguide.org/getting-started/)은 텍스트 기반의 마크업언어로 2004년 존그루버에 의해 만들어졌으며 쉽게 쓰고 읽을 수 있으며 HTML로 변환이 가능하다. 특수기호와 문자를 이용한 매우 간단한 구조의 문법을 사용하여 웹에서도 보다 빠르게 컨텐츠를 작성하고 보다 직관적으로 인식할 수 있다.

# 2. 마크다운 사용법(문법)
## 2.1. 헤더Headers
* 큰제목: 문서 제목
    ```
    This is an H1
    =============
    ```
    This is an H1
    =============

* 작은제목: 문서 부제목
    ```
    This is an H2
    -------------
    ```
    This is an H2
    -------------

* 글머리: 1~6까지만 지원
```
# This is a H1
## This is a H2
### This is a H3
#### This is a H4
##### This is a H5
###### This is a H6
```
# This is a H1
## This is a H2
### This is a H3
#### This is a H4
##### This is a H5
###### This is a H6
####### This is a H7(지원하지 않음)

## 2.2. BlockQuote
이메일에서 사용하는 ```>``` 블럭인용문자를 이용한다.
```
> This is a first blockqute.
>	> This is a second blockqute.
>	>	> This is a third blockqute.
```
> This is a first blockqute.
>	> This is a second blockqute.
>	>	> This is a third blockqute.

이 안에서는 다른 마크다운 요소를 포함할 수 있다.
> ### This is a H3
> * List
>	```
>	code
>	```

## 2.3. 목록
### ● 순서있는 목록(번호)
순서있는 목록은 숫자와 점을 사용한다.
```
1. 첫번째
2. 두번째
3. 세번째
```
1. 첫번째
2. 두번째
3. 세번째

**현재까지는 어떤 번호를 입력해도 순서는 내림차순으로 정의된다.**
### ● 순서없는 목록(글머리 기호: `*`, `+`, `-` 지원)
```
* 빨
  * 녹
    * 파

+ 빨
  + 녹
    + 파

- 빨
  - 녹
    - 파
```
* 빨
  * 녹
    * 파

+ 빨
  + 녹
    + 파

- 빨
  - 녹
    - 파

## 2.4. 코드
4개의 공백 또는 하나의 탭으로 들여쓰기를 만나면 변환되기 시작하여 들여쓰지 않은 행을 만날때까지 변환이 계속된다.

## 2.4.1 들여쓰기

### 기본 문법
This is a normal paragraph:

css
복사
편집
This is a code block.
end code block.

markdown
복사
편집

### 적용 예시
*****
This is a normal paragraph:

    Hello, 멋사 부트캠프 15기!

end code block.
*****

> 한 줄 띄어쓰기를 하지 않으면 코드블럭이 제대로 인식되지 않습니다.

This is a normal paragraph:
Hello, 멋사 부트캠프 15기!
end code block.

yaml
복사
편집

적용 예:

*****
This is a normal paragraph:
    Hello, 멋사 부트캠프 15기!
end code block.
*****

---

## 2.4.2 코드블럭

코드블럭 작성 방법에는 크게 두 가지가 있습니다.

### 1) `<pre><code>` 이용 방식
<pre> <code> public class Bootcamp15Application { public static void main(String[] args) { System.out.println("Hello, 멋사 부트캠프 15기"); } } </code> </pre>
csharp

<pre>
<code>
public class Bootcamp15Application {
  public static void main(String[] args) {
    System.out.println("Hello, 멋사 부트캠프 15기");
  }
}
</code>
</pre>

### 2) 백틱(```) 이용 방식

\```
public class Bootcamp15Application {
  public static void main(String[] args) {
    System.out.println("Hello, 멋사 부트캠프 15기");
  }
}
\```

적용 예:

```java
public class Bootcamp15Application {
  public static void main(String[] args) {
    System.out.println("Hello, 멋사 부트캠프 15기");
  }
}
GitHub에서는 코드블럭 시작점에 언어명을 적으면 문법 강조(Syntax Highlighting)가 적용됩니다.


public class Bootcamp15Application {
  public static void main(String[] args) {
    System.out.println("Hello, 멋사 부트캠프 15기");
  }
}

## 2.5 링
* 참조링크

```
[link keyword][id]

[id]: URL "Optional Title here"

// code
Link: [Google][googlelink]

[googlelink]: https://google.com "Go google"
```

Link: [Google][googlelink]

[googlelink]: https://google.com "Go google"

* 외부링크
```
사용문법: [Title](link)
적용예: [Google](https://google.com, "google link")
```
Link: [Google](https://google.com, "google link")

* 자동연결
```
일반적인 URL 혹은 이메일주소인 경우 적절한 형식으로 링크를 형성한다.

* 외부링크: <http://example.com/>
* 이메일링크: <address@example.com>
```

* 외부링크: <http://example.com/>
* 이메일링크: <address@example.com>

## 2.6. 이미지
```
![Alt text](/path/to/img.jpg)
![Alt text](/path/to/img.jpg "Optional title")
```
![석촌호수 러버덕](http://cfile6.uf.tistory.com/image/2426E646543C9B4532C7B0)
![석촌호수 러버덕](http://cfile6.uf.tistory.com/image/2426E646543C9B4532C7B0 "RubberDuck")

사이즈 조절 기능은 없기 때문에 ```<img width="" height=""></img>```를 이용한다.

## 2.7. 줄바꿈
3칸 이상 띄어쓰기(` `)를 하면 줄이 바뀐다.

```
* 줄 바꿈을 하기 위해서는 문장 마지막에서 3칸이상을 띄어쓰기해야 한다. 
이렇게

* 줄 바꿈을 하기 위해서는 문장 마지막에서 3칸이상을 띄어쓰기해야 한다.___\\ 띄어쓰기
이렇게
```

* 줄 바꿈을 하기 위해서는 문장 마지막에서 3칸이상을 띄어쓰기해야 한다. 이렇게

* 줄 바꿈을 하기 위해서는 문장 마지막에서 3칸이상을 띄어쓰기해야 한다.    \
이렇게