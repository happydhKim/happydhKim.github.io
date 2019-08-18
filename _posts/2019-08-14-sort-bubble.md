---
title: "Bubble sort"
excerpt: "버블정렬"
categories: 
  - algorithm
comments: true
date: 2019-08-14
# last_modified_at: 2019-08-12T20:21:00+09:00
tag: 
    - algorithm
    - java
    - js
    - sort
    - bubble
gallery: #이미지 갤러리
    - url: /assets/images/algorithm/bubbleSort.png
      image_path: /assets/images/algorithm/bubbleSort.png
      alt: "bubbleSort"
      title: "bubbleSort"
---

{% include gallery caption="이미지 출처 **http://blog.naver.com/PostView.nhn?blogId=justant&logNo=20204028286&parentCategoryNo=&categoryNo=15&viewDate=&isShowPopularPosts=true&from=search**."  %}
### 거품정렬 (Bubble Sort)
- 거품정렬(Bubble Sort)은 인접한 원소들의 대소관계를 비교하여 일정한 대소관계를 만족하지 않을 시, 인접한 원소를 교환하는 방법으로 진행되는 정렬이다.
- 한번 교환 작업을 통해 4개의 원소 중 가장 큰 원소가 마지막으로 감을 확인할 수 있다.
- 이를 통해 마지막 원소를 정렬이 완료된 것이고, 이를 N-1 번 반복한다면 모두 정렬이 완료될 것이다.

- 인접한 원소들은 대소관계에 따라 교환이 되기 때문에, 그림의 노란 영역처럼 가장 큰 수가 가장 마지막에 오게 된다.

- 이를 통해 N개의 원소가 있다면, N - 1 번의 그림과 같은 교환을 통해 정렬할 수 있다.

- 거품정렬의 시간복잡도는 고려해야 할 루프가 (정렬해야 할 원소의 개수 - 1) * (최대 교환 수)이므로 총 O ( N ^ 2 ) 가 된다.
- 힙 정렬, 퀵 정렬과 같은 정렬보다 상당히 비효율적이므로 자주 쓰이지 않는다.

```java
import java.util.*;

public class Main {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        int[] d = new int[5005];

        for (int i = 0; i < n; i++)
            d[i] = sc.nextInt();

        for (int i = 0; i < n; i++)
            for (int j = 0; j < n - i - 1; j++)
                if (d[j] > d[j + 1]) {
                    int temp = d[j];
                    d[j] = d[j + 1];
                    d[j + 1] = temp;
                }

        for (int i = 0; i < n; i++)
            System.out.print(d[i] + " ");
        sc.close();
    }
}
```