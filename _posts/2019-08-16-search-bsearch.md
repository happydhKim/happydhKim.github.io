---
title: "Binary Search"
excerpt: "이진 탐색"
categories: 
  - algorithm
comments: true
date: 2019-08-15
# last_modified_at: 2019-08-12T20:21:00+09:00
tag: 
    - algorithm
    - java
    - js
    - search
    - binarysearch

---
### Binary Search (이진 탐색)
- 이진 탐색(Binary Search)은 정렬된 배열에서 원하는 값을 시간복잡도 O(log N) 만에 찾아내는 탐색하는 방법이다.
- 오름차순으로 정렬된 사이즈가 N인 배열 D에서 원하는 값 k를 찾는 방법은 다음과 같다.
- 먼저 탐색할 데이터의 범위를 두 개의 인덱스(왼쪽, 오른쪽)로 지정하고 이를 L, R이라고 한다. 정렬되어있기 때문에 D[L]은 최솟값, D[R]은 최대값이 된다.
- 당연히 처음 탐색 시에는 전체영역이므로 L = 0, R = N - 1 입니다. 이중 중앙값(Median)을 찾아 찾으려는 값 k와 비교한다. 중앙값 M은 (L+R)/2 로 구할 수 있다.

```java
import java.util.*;

public class bsearch {
	public static void main(String args[]) {
		Scanner sc = new Scanner(System.in);

		int n = sc.nextInt();
		int d[] = new int[5005];
		for (int i = 0; i < n; i++)
			d[i] = sc.nextInt();

		// bubble sorting
		for (int i = 0; i < n; i++)
			for (int j = 0; j < n - i - 1; j++)
				if (d[j] > d[j + 1]) {
					int temp = d[j];
					d[j] = d[j + 1];
					d[j + 1] = temp;
				}

		// binary search for each query
		int query = sc.nextInt();
		for (int i = 0; i < query; i++) {
			int x = sc.nextInt();
			int l = 0, r = n - 1;
			boolean answer = false;

			while (l <= r) {
				int mid = (l + r) / 2;
				if (x == d[mid]) {
					answer = true;
					break;
				} else if (x > d[mid]) {
					l = mid + 1;
				} else {
					r = mid - 1;
				}
			}

			if (answer == true)
				System.out.println("exist");
			else
				System.out.println("not exist");
		}
		sc.close();
	}
}
```