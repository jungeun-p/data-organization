# 21. this

### ∙this의 배경

**¹**메서드는 자신이 속한 객체의 식별자를 참조할 수 있어야 한다. 자신이 속한 객체를 재귀적으로 참조하는 방식은 일방적이지 않으며 바람직하지도 않다.

**²**생성자 함수로 인스턴스를 생성할 때, 생성자 함수 정의 시점에는 인스턴스가 부재하기 때문에 이를 가리키는 식별자를 알 수 없다. 

**자신이 속한 객체**, 또는 **자신이 생성할 인스턴스**를 가리킬 특수한 식별자가 `this`다. 

## ✔️ `this` keyword

자신이 속한 객체 혹은 생성할 인스턴스를 가리키는 **자기 참조 변수**이며, **프로퍼티나 메서드를 참조**할 수 있다. 지역 변수로 사용이 가능하나, **this 바인딩**은 **함수 호출 방식(invoke)에 의해 동적으로 결정**된다. 

this는 결국 객체의 프로퍼티와 메서드를 참조를 목적으로 하기 때문에 객체 내의 메서드나 생성자 함수에만 의미가 있다. 일반 함수 내부에서는 this를 사용할 필요가 없다. 

## ✔️ 함수 호출 방식과 `this` 바인딩.

함수 호출 방식에 따라 this 바인딩이 동적으로 결정되며, 렉시컬 스코프는 함수 객체가 생성되는 시점에서 상위 스코프를 결정하게 되고 함수 호출 시점에 바인딩 된다. 

### ∙일반 함수 호출

일반 함수 내부에서의 this는 **전역 객체(window)를 가리킨다.** 객체를 생성하지 않는 일반 함수는 의미가 없으며, 중첩 함수 내부에서도, 콜백 함수의 경우에도 전역 객체가 바인딩 처리가 되기 때문에, **¹**that 변수에 할당하거나 ²**arrow func(`()⇒{}`)**를 통해 **상위 스코프 this 바인딩 처리**로 보완할 수 있다.

### ∙메서드 호출

 해당 메서드가 가리키는 객체와 별도로, **메서드를 호출한 객체에 바인딩** 된다. 

### ∙생성자 함수 호출

생성자 함수가 생성할 인스턴스를 가리킨다. new 연산자와 함께 호출시 생성자 함수로 동작하게 된다.

### ∙Function.prototype의 `apply/call/bind()` 메서드에 의한 간접 호출

함수에 전달되는 인수에 의해 결정된다. `bind()`/`call()의` 경우 this 객체를 전달하면서 함수를 호출한다. `apply()`는 함수 호출 없이 this 객체만 전달하며, 콜백 함수가 일반 함수로 호출될 때 바인딩 처리를 한다.