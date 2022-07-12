---
title: 접근제어자에 대해 알아봅시다!
author: yonggguk
date: 2022-07-07 09:00 +0900
categories: [JAVA]
tags: [Question]
mermaid: true
---

## 접근제어자(Access Modifier)란 무엇일까?

접근제어자란. 변수와 함수, 클래스에 대한 접근을 제한하는 역할을 하는 예약어입니다.

## 접근제어자를 사용하는 이유는?

우리가 항상 문제를 해결하거나 문제를 해결하기 위해 프로그래밍을 할 때 각 기능을 사용하는 이유와 근거가 있어야 합니다! 서론이 길었지만 ... 지금부터 그럼, 우리가 접근제어자를 사용하는 이유에 대해 알아봅시다.

1. 첫번째 이유로는 보안 때문입니다. 모든 변수를 public으로 설정하게 된다면 어디서든지 변경 또는 참조가 가능하여 무분별한 사용과 변경으로 중요한 정보가 노출되거나 변경될 수 있기 때문입니다.

2. 두번째 이유로는, 외부로 생기는 오류를 줄이기 위함이다. 사용자나 외부에서 사용하는 객체에서 내부적으로 사용하는 변수나 메소드에 접근함으로 개발자가 의도하지 않은 오류를 야기할 수 있기 때문입니다.

3. 세번째 이유로는, 객체 사용에 집중할  수 있도록 돕기 위함입니다. 객체를 조작할 수 있는 수단만을 제공함으로 객체 사용에 집중을 하도록 합니다.

## 접근제어자의 종류

- public

- protected

- default

- private

### private

private이 붙은 변수, 메소드는 해당 글래스에서만 접근이 가능하다.

### default

접근 제어자를 별도로 설정하지 않는다면 접근 제어자가 없는 변수, 메소드는 default 접근 제어자가 되어 해당 패키지 내에서만 접근이 가능하다.

### protected

protected가 붙은 변수, 메소드는 동일 패키지의 클래스 또는 해당 클래스를 상속받은 다른 패키지의 클래스에서만 접근이 가능하다.

### public

public으로 설정되었다면 public 접근제어자가 붙은 변수, 메소드는 어떤 클래스에서라도 접근이 가능하다.

## 접근 범위

public > protected > default > private


![google-analytics-realtime](/posts/20210103/02-google-analytics-realtime.png){: width="616" height="557"}

reference : [생활코딩](https://opentutorials.org/course/1223/6061), [점프 투 자바](https://wikidocs.net/232)