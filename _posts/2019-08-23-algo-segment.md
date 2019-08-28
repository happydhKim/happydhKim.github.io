---
title: "Segment Tree"
excerpt: "segment tree"
categories:
  - algorithm
comments: true
date: 2019-08-23
# last_modified_at: 2019-08-12T19:37:00+09:00
tag: 
    - datastructure
    - algorithm
    - segment tree
gallery: #이미지 갤러리
    - url: /assets/images/datastructure/tree.jpg
      image_path: /assets/images/datastructure/tree.jpg
      alt: "tree"
      title: "tree"
---

### Segment Tree

- **세그먼트 트리(Segment Tree)는** 구간에 대한 정보를 빠르게 구해낼 수 있으며 완전 이진트리 형식의 구조를 가지는 자료구조.

```java
import java.util.ArrayList;
import java.util.Scanner;

class SegmentTree {
	ArrayList<Integer> tree;
	int s;

	public SegmentTree(int n) {
		for (s = 1; s < n; s *= 2)
			;
		tree = new ArrayList<Integer>(s * 2);
		tree.add(0);
		for (int i = 1; i < s + s; i++)
			tree.add(Integer.MAX_VALUE);
	}

	void insert(ArrayList<Integer> d) {
		for (int i = s; i < s + d.size(); i++)
			tree.set(i, d.get(i - s));
		for (int i = s - 1; i >= 1; i--)
			tree.set(i, Integer.min(tree.get(i * 2), tree.get(i * 2 + 1)));
	}

	int getMin(int Left, int Right) {
		int l = Left + s - 1, r = Right + s - 1;
		int rval = Integer.MAX_VALUE;
		while (l <= r) {
			if (l % 2 == 0)
				l /= 2;
			else {
				rval = Integer.min(rval, tree.get(l));
				l = (l / 2) + 1;
			}
			if (r % 2 == 1)
				r /= 2;
			else {
				rval = Integer.min(rval, tree.get(r));
				r = (r / 2) - 1;
			}
		}
		return rval;
	}
}

public class segmentTree {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		int n = sc.nextInt();
		SegmentTree T = new SegmentTree(n);
		ArrayList<Integer> v = new ArrayList<Integer>(n + 1);
		for (int i = 0; i < n; i++) {
			v.add(sc.nextInt());
		}
		T.insert(v);
		int m = sc.nextInt();
		for (int i = 0; i < m; i++) {
			int x = sc.nextInt();
			int y = sc.nextInt();
			System.out.println(T.getMin(x, y));
		}
		sc.close();
	}
}
```