---
title: "백준 동전1, 동전2, 동전3"
excerpt: "다이나믹 프로그래밍 동전1, 동전2, 동전3"
categories: 
  - algorithm
comments: true
date: 2019-09-12
# last_modified_at: 2019-08-12T19:37:00+09:00
tag: 
    - algorithm
    - dynamic programming
---

### 백준 동전 1
- https://www.acmicpc.net/problem/2293
```java
import java.util.Scanner;

public class coin1 {
	public static void main(String args[]) {
		Scanner sc = new Scanner(System.in);
		int n = sc.nextInt(); // 동전 종류
		int k = sc.nextInt(); // 원하는 값
		int dp[][] = new int[n + 1][k + 1];
		for (int i = 0; i <= n; i++) {
			dp[i][0] = 1;
		}
		for (int i = 1; i <= n; i++) {
			int v = sc.nextInt(); // 동전의 가치
			for (int j = 1; j <= k; j++) {
				if (j - v >= 0) {
					dp[i][j] = dp[i - 1][j] + dp[i][j - v];
				} else {
					dp[i][j] = dp[i - 1][j];
				}
			}
		}
		System.out.println(dp[n][k]);
		sc.close();
	}
}
```

### 백준 동전 2
- https://www.acmicpc.net/problem/2294
```java
import java.util.Scanner;

public class coin2 {
	public static void main(String args[]) {
		Scanner sc = new Scanner(System.in);
		int n = sc.nextInt();
		int k = sc.nextInt();
		int coin[] = new int[n];
		for (int i = 0; i < n; i++) {
			coin[i] = sc.nextInt();
		}
		int dp[] = new int[k + 1];
		for (int i = 1; i <= k; i++) {
			dp[i] = -1;
			for (int j = 0; j < n; j++) {
				if (coin[j] <= i) {
					if (dp[i - coin[j]] < 0) {
						continue;
					}
					if (dp[i] < 0) {
						dp[i] = dp[i - coin[j]] + 1;
					} else if (dp[i - coin[j]] + 1 < dp[i]) {
						dp[i] = dp[i - coin[j]] + 1;
					}
				}
			}
		}
		System.out.println(dp[k]);
		sc.close();
	}
}
```

### 백준 동전
- https://www.acmicpc.net/problem/9084

```java
import java.util.Scanner;

public class coin {
	public static void main(String args[]) {
		Scanner sc = new Scanner(System.in);
		int T = sc.nextInt();
		for (int TC = 1; TC <= T; TC++) {
			int n = sc.nextInt(); // 동전 종류
			int coin[] = new int[n + 1];
			for (int i = 1; i <= n; i++) {
				coin[i] = sc.nextInt();
			}
			int k = sc.nextInt(); // 원하는 값
			int dp[][] = new int[n + 1][k + 1];
			for (int i = 0; i <= n; i++) {
				dp[i][0] = 1;
			}
			for (int i = 1; i <= n; i++) {
				for (int j = 1; j <= k; j++) {
					if (j - coin[i] >= 0) {
						dp[i][j] = dp[i - 1][j] + dp[i][j - coin[i]];
					} else {
						dp[i][j] = dp[i - 1][j];
					}
				}
			}
			System.out.println(dp[n][k]);
		}
		sc.close();
	}
}
```

```java
import java.util.Scanner;

public class coin {
	public static void main(String args[]) {
		Scanner sc = new Scanner(System.in);
		int T = sc.nextInt();
		for (int TC = 1; TC <= T; T++) {
			int N = sc.nextInt();
			int K[] = new int[N];
			for (int j = 0; j < N; j++) {
				K[j] = sc.nextInt();
			}
			int M = sc.nextInt();
			int dp[] = new int[M + 1];
			dp[0] = 1;
			for (int i = 0; i < N; i++) {
				for (int j = 0; j <= M; j++) {
					if (j - K[i] >= 0) {
						dp[j] += dp[j - K[i]];
					}
				}
			}
			System.out.println(dp[M]);
		}
		sc.close();
	}
}
```