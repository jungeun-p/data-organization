# 47. 모듈(module)

`module`이란, **개별적 요소로서 재사용 가능한 코드 조각을 의미**한다. 자신만의 파일 스코프를 지니고 있으며 **명시적으로 선택적 공개하여 재사용 처리가 가능한 `export`**, 모듈이 공개한 자산 중 **일부 혹은 전체를 스코프 내로 재사용 하는 `import`** 가 가능하다.

모든 모듈은 재사용 가능하며, 개인적인 파일로 작성된다. 

ES6부터 추가된 기능이며, `script` 태그는 스코프 없이 전역으로 공유하지만, `**type=”module”` 어트리뷰트**를 추가하여 **독립적인 스코프**를 지니게 된다. 단, 외부 모듈에서 참조 불가.

### ∙ `export`

`export` 키워드를 선언문 앞에 사용하여 식별자, 혹은 하나의 객체로 구성(`{}`)하여 한번에 `export` 가능하다.

### ∙ `import`

`import` 키워드 사용시 **모듈 스코프 내부로 로드 가능**하다. `export`한 식별자 이름으로 `import` 가능하며, 별도의 `script` 태그가 불필요. 

```jsx
import { x, y z } from './lib.mjs'; // 하나의 객체로 전달
import * as lib from './lib.mjs'; // 하나의 이름의 객체에 프로퍼티 할당 or 이름 변경

// 하나의 값만 사용시 default 사용 가능. 
// 단, var/let/const 사용은 불가하다. 
// {} 없이 이름으로만 import 처리.
import default x => x*x;
import square from './lib.mjs';
```