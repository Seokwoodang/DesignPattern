# 아토믹패턴의 구조

아토믹 디자인패턴은 다섯가지의 단계로 이루어져있다.

atom, molecule, organism, template, page 이렇게 다섯 단계로 이루어져 있는데 각각의 단계에 대한 설명은 아래와 같다.

## atom
아토믹 디자인 패턴을 이루는 가장 작은 단위.   

## molecule
한 가지 일을 하는 것. SRP(Single Responsibility Principle)원칙, 재사용성 높다.
네이밍이 컨텍스트 없이 주로 UI적인 네이밍이 포함된다.

## organism
좀 더 복잡하고 서비스에서 표현될 수 있는 명확한 영역과 특정 컨텍스트를 가진다.
예를 들어 header라는 컨텍스트에 logo, navigation, search form 등을 포함 가능
네이밍에 컨텍스트가 포함된다.

## template
page를 만들 수 있도록 여러개의 organism, molecule로 구성. 실제 콘텐츠가 없는 페이지 수준

## page
유저가 볼 수 있는 실제 콘텐츠를 담고 있다.

# 아토믹 패턴의 장단점

## 아토믹 패턴의 장점
1) 컴포넌트 재활용성을 극대화하는 방식으로 설계할 수 있다.
2) React의 렌더링 최적화에 효과적인 설계 방법 중 하나. 상태를 분산해 적용하기 때문에 상태 변화에 따른 렌더링이 작은 범위로 이루어져 성능을 최적화시키기 좋습니다.
3) 어플리케이션과 분리하여 컴포넌트를 개발하고 테스트할 수 있으며, 스타일 가이드와 같은 도구에서 볼 수 있다. 그리고 통합 개발을 할 때, 백엔드 어플리케이션의 로직에 의존하지 않는다는 장점이 있다.
4) 특정 컴포넌트에 CSS가 강하게 결합되어 있기 때문에 CSS를 훨씬 잘 관리할 수 있다. 이를 위해서는 어플리케이션의 구조에 따라 컴포넌트에서 사용되는 CSS만 렌더링하도록 해야 한다.

## 아토믹 패턴의 단점
1) 사전 학습이 있어야 수월하게 진행할 수 있다.
2) Atomic 디자인 방식으로 UI가 디자인되지 않으면, 작성해야 할 컴포넌트가 많아지게 된다.
3) 컴포넌트에 대한 유지보수가 어려워집니다. 컴포넌트들이 많아짐으로 인해, 관리해야 할 대상이 많아지게 되고 자연스럽게 유지보수가 어려워진다.
4) 재활용성을 위해 특정 계층의(Atoms, Molecules) 컴포넌트가 지나치게 복잡해지게 된다.
5) 아토믹 디자인의 틀에 맞추기 위해, 작업해야 하는 시간이 더 늘어난다.

organism을 나누는 기준
매우 주관적이다. 뷰 기준으로 나누자



약간 다른 Organism이 있을 때  컴파운드 컴포넌트를 이용해 해결하도록 하자.
