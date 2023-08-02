# 48. Babel, Webpack을 이용한 ES6+/ES.NEXT 개발 환경 구축

## ✔️ Babel

**트랜스 파일러.** EX6+/ES.NEXT로 구현된 **최신 사양의 코드를 구형 브라우저에서도 동작하는 ES5로 변환** 가능하다. 

```jsx
@babel/preset-env // 바벨 프리셋
```

- **트랜스 파일링**
    
    `npm` `script`에 CLI 명령어를 등록하여 사용 가능.
    

```jsx
// package.json
{
	"scripts": {
		"build": "babel src/js -w -d dist/js"
	}
}
```

## ✔️ Webpack

JS, CSS, 이미지 등의 리소스를 **하나의 파일로 번들링 처리하는 모듈 번들러.** 여러 개의 J**S 파일을 하나로 번들링** 하므로, script 태그를 통해 여러 개의 JS 파일을 로드 할 필요가 없다.