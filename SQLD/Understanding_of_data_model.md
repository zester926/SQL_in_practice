# Quiz
1. 모델링이란?

2. 모델링의 3가지 관점

3. 데이터 모델링이란?

4. 데이터 모델링이 제공하는 기능은?

5. 데이터 모델링이 왜 필요한가?

6. 데이터 모델링의 3단계란?

7. 프로젝트 수명주기란?

8. 데이터 독립성의 필요성과 그 방법은?

9. 데이터베이스 3단계 구조

10. 데이터 독립성 2가지

11. 데이터베이스 3단계 구조에서 매핑 2가지

12. 데이터 모델링 3가지 요소란?

13. 데이터 모델링 작업 순서

14. 데이터 모델링 이해관계자

15. 좋은 데이터 모델의 요소란?


# 데이터 모델의 이해

## 모델링이란?
현실 세계를 추상화, 단순화, 명확화를 통해 일정한 표기법으로 표현하는 것을 의미한다.

* 추상화 : 현실 세계를 일정한 형식으로 표현하는 것.
* 단순화 : 제한된 표기법을 통해 표현하는 것.
* 명확화 : 애매모호한 정보를 제거하고 정확하게 표현하는 것.

## 모델링의 3 가지 관점
* 데이터 (What) : 업무가 어떠한 데이터와 관련이 있는지 또는 데이터 간의 관계가 무엇인지에 대해 모델링을 수행.
* 프로세스 (How) : 업무가 실제로 수행하는 일이 무엇인지 또는 무엇을 해야 할지에 대해 모델링을 수행.
* 상관 (Data & Process) : 업무가 수행하는 일에 따라 데이터가 어떠한 영향을 받고 있는지에 대해 모델링을 수행.

## 데이터 모델링이란?
* 정보 시스템 구축 시, 데이터 관점에서 업무를 분석하는 기법.
* 현실 세계를 약속된 표기법을 통해 표현하는 것.
* 데이터 베이스를 구축할때 수행하는 분석/설계 과정.

## 데이터 모델링이 제공하는 기능은?
* 시각화 : 시스템의 현재 모습을 보여준다.
* 명세화 : 시스템의 구조와 행동을 명세화 해준다.
* 문서화 : 시스템을 구축하는 과정에서 결정된 것을 문서화 해준다.
* 구체화 : 구체적인 세부 표현방법을 제공한다.
* 구조적인 틀 : 시스템을 구축하는 구조적인 틀을 제공한다.
* 다양한 관점 : 다양한 영역에 집중할 수 있도록 다른 영역의 세부 정보는 숨기는 등 다양한 관점을 제공한다.

## 데이터 모델링이 왜 필요한가?
* 파급 효과 : 데이터 모델을 잘못 설계한 상태로 개발이 진행될 시, 스노우볼 발생.
* 복잡한 요구사항의 간결한 표현 : 복잡한 요구사항을 데이터 모델을 통해 명확하고 간결하게 표현 가능.
* 데이터 품질 : 데이터의 중복, 비유연성, 비일관성 발생 가능하므로 데이터 모델링을 통해 이를 보완.

## 데이터 모델링의 3단계
현실 세계 --(개념적 데이터 모델링 : 추상적)--> 개념적 구조 --(논리적 데이터 모델링)--> 논리적 구조 --(물리적 데이터 모델링 : 구체적)--> 물리적 구조 (DB)

* 개념적 데이터 모델링 : 높은 추상화, 포괄적인 수준의 데이터 모델링
* 논리적 데이터 모델링 : 키, 속성, 관계 등을 정확하게 결정
* 물리적 데이터 모델링 : 실제 DB 이식 위해 성능, 저장 등 물리적인 성격 고려하여 모델링

### 프로젝트 수명주기 : 정보전략계획 - 분석 - 설계 - 개발 - 테스트 - 전환/이행
* 정보전략계획/분석 단계 - 개념적 데이터 모델링 수행
* 분석 단계 - 논리적 데이터 모델링 수행
* 설계 단계 - 물리적 데이터 모델링 수행

## 데이터 독립성
### 필요성
1. 중복되는 데이터를 최소화하기 위해
2. 뷰와 DB 간의 독립성을 유지하기 위해

### 방법
1. 뷰 간의 독립성을 통해 뷰 하나를 변경하더라도 다른 뷰에 영향을 미치지 않게끔 한다
2. 단계별 스키마에 따라 다른 DDL, DML 제공

### 데이터베이스 3단계 구조
외부 단계 --(논리적 독립성)-- 개념 단계 --(물리적 독립성)-- 내부 단계

* 외부 스키마 : 뷰 단계로, 여러 사용자의 관점으로 구성. 개별 사용자가 보는 개인적 DB 스키마
* 개념 스키마 : 모든 사용자의 관점을 통합한 조직 전체의 DB 스키마
* 내부 스키마 : DB가 물리적으로 저장된 형식

### 데이터 독립성 2가지
* 논리적 독립성 : 개념 스키마가 변경되더라도 외부 스키마에 영향 X
* 물리적 독립성 : 내부 스키마가 변경되더라도 개념/외부 스키마에 영향 X

### 데이터베이스 3단계 구조에서 매핑 2가지
* 논리적 매핑 : 외부적 뷰와 개념적 뷰의 상호 호환성을 정의
* 물리적 매핑 : 데이터베이스와 개념적 뷰의 상호 호환성을 정의

## 데이터 모델링 3가지 요소
* 엔티티 : 업무가 관여하는 어떤 것
* 속성 : 엔티티의 성격
* 관계 : 엔티티간의 관계

## 데이터 모델링 작업 순서
1. 엔티티를 그린다.
2. 엔티티를 배치한다.
3. 엔티티의 관계를 설정한다.
4. 관계명을 기술한다.
5. 관계의 참여도를 기술한다.
6. 관계의 필수 여부를 기술한다.

## 데이터 모델링 이해관계자
프로젝트 개발자, DBA, 전문 모델러, 현업업문전문가

## 좋은 데이터 모델의 요소
* 완전성 : 업무에 필요한 데이터가 모두 정의되어야 한다.
* 중복 배제 : 동일한 데이터는 한 번만 저장해야 한다.
* 데이터 재사용 : 데이터 통합성과 독립성을 고려해야 한다.
* 통합성 : 동일한 데이터는 유일하게 정의해서 다른 영역에서 참조해야 한다.
* 의사소통 : 데이터 모델을 보고 이해관계자끼리 의사소통이 가능해야 한다.
* 업무규칙 : 데이터 모델 분석만으로도 비즈니스 로직이 이해되어야 한다.