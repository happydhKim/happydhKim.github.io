---
title: "Insertion sort"
excerpt: "삽입정렬"
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
    - insertion

gallery: #이미지 갤러리
    - url: /assets/images/algorithm/insertionSort.png
      image_path: /assets/images/algorithm/insertionSort.png
      alt: "insertionSort"
      title: "insertionSort"
---

### 삽입 정렬(Insertion Sort)
- 삽입정렬(Insertion Sort)은 배열을 정렬된 부분, 정렬되지 않은 부분으로 나눈 후, 원소를 순차적으로 탐색하면서 해당 원소를 정렬이 된 부분에 끼워 넣는 정렬이다.
- 아래의 그림의 회색 부분은 정렬이 완료된 부분이며 흰색 부분은 정렬이 완료되지 않은 부분이다.
- 적당한 위치를 찾은 후, 뒷자리 원소들을 밀어준 후 해당 원소를 삽입한다.
- 뒤에서부터 한자리씩 당겨가면서 적당한 위치를 찾은 후 삽입하여도 같은 원리로 동작한다.

{% include gallery caption="이미지 출처 **https://cocomo.tistory.com/232**."  %}

- 시간복잡도는 각 원소에 대해 적당한 위치를 찾아주어야 하므로 총 원소의 개수 O( N ), 순차적으로 삽입 위치를 찾는데 O( N )이 들므로
- O(N ^ 2)으로 힙정렬이나 합병정렬에 비해 비효율적(O(N log N))으로 잘 쓰이지 않는다.

```java
import java.util.*;

public class Main {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int[] d = new int[5005];
        for (int i = 0; i < n; i++)
            d[i] = sc.nextInt();

        for (int i = 0; i < n; i++) {
            int temp = d[i];
            int j = i - 1;

            for (; j >= 0; j--) {
                if (d[j] < temp)
                    break;
                d[j + 1] = d[j];
            }

            d[j + 1] = temp;
        }

        for (int i = 0; i < n; i++)
            System.out.print(d[i] + " ");
        sc.close();
    }
}
```