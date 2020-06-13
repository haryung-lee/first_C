---
layout: post
title: "배열 programming"
date: 2020-06-12 19:00:00 +0900
author: HaRyung
---

# 목차

1. 2개 정수 배열 요소 같은지 검사
2. **가장 많이 생성된 수 찾기**
3. 각 행의 합계와 각 열의 합계 출력
4. ㅁ
5. ㅁ
6. ㅁ
7. ㅁ
8. ㅁ
9. ㅁ
10. ㅁ

---

#### 1. 두 배열 요소 같은지 검사

> **Q. 2개의 정수 배열 a, b를 받아서 대응되는 배열 요소가 같은지 검사하는 함수를 작성하고 테스트하라.**

```c
#include <stdio.h>
#define SIZE 10

int array_equal(int a[], int b[], int size)
{
	for (int i = 0; i < size; i++)
	{
		if (a[i] == b[i])
			continue;
		else
		{
			return 0;
			break;
		}
	}
	return 1;
}

int main(void)
{
	int a[SIZE] = {1, 2, 3};
	int b[SIZE] = {0};
	array_equal(a, b, SIZE);

	if (array_equal == 1)
		printf("2개의 배열은 같음");
	else
		printf("2개의 배열은 다름");

	return 0;
}
```

> ##### *FEEDBAKC*
>
> **1. 반복문 안에서 break문 사용하면 반복문이 바로 끝나버림**

*실행결과*

```
2개의 배열은 다름
```

---

#### 2. 가장 많이 생성된 수 찾기

> **Q. 0부터 9까지의 난수를 100번 생성하여 가장 많이 생성된 수를 출력하는 프로그램을 작성하라.**

```c
#include <stdio.h>
#include <stdlib.h>
#include <time.h>
#define SIZE 10

int main(void)
{
    srand(time(NULL));
    int list[SIZE] = { 0 };
    int temp[SIZE] = { 0 };
    int a, max;

    for (int i = 0; i < 100; i++)
    {
        a = rand() % 10;
        list[a]++;
    }
    
    for (int i = 0; i < SIZE; i++)
    {
        if (list[i]>=10)
        {
            max = i;
            temp[i] = list[i];
            for (int j = 0; j <= i; j++)
            {
                if (temp[j]>temp[i])
                    max = j;
            }
        }
    }
    for (int i = 0; i < SIZE; i++)
        printf("list[%d] = %d\n",i, list[i]);
    printf("가장 많이 나온 수 = %d", max);
    return 0;
}
```

> ##### *FEEDBACK*
>
> **1. 시간 오래 걸림**
>
> 우선 내 아이디어를 어떻게 구현할지 모르겠었음.. 단순히 제일 많이 나온게 몇번이냐가 아니라 몇번째 배열이냐.. 이걸 출력해야해서 ㅠ
>
> **2. 아이디어**
>
> 최소 1칸 이상은 10이상일 수 밖에 없음 그래서 우선 0~9중 10번 이상 나온걸 추려서 다른 배열에 넣고..
>
> 그 배열에서 또 이전값과 비교해서 max 값 설정하는 것!

*실행결과*

```
list[0] = 9
list[1] = 8
list[2] = 6
list[3] = 8
list[4] = 11
list[5] = 12
list[6] = 12
list[7] = 9
list[8] = 12
list[9] = 13
가장 많이 나온 수 = 9
```

---

#### 3. 각 행의 합계와 각 열의 합계 출력

> ##### Q. 2차원 표를 배열로 생성하고, 각 행의 합계, 각 열의 합계를 구하여 출력하는 프로그램을 작성하라.

```c
#include <stdio.h>
#define ROWS 5
#define COLS 3

int main(void)
{
    int list[ROWS][COLS]={12, 56, 32, 16, 98}, {99, 56, 34,41, 3}, {65, 3, 87, 78, 21};
    sum_ROWS = 0;
    sum_COLS = 0;
    
    for (int i = 0; i < ROWS; i++)
        sum_ROWS += list[][]
    
    return 0;
}
```



