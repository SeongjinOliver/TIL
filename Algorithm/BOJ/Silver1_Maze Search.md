# 미로 탐색

Silver I

| 시간 제한 | 메모리 제한 | 제출  | 정답  | 맞은 사람 | 정답 비율 |
| :-------- | :---------- | :---- | :---- | :-------- | :-------- |
| 1 초      | 192 MB      | 61651 | 22250 | 14139     | 35.056%   |

## 문제

N×M크기의 배열로 표현되는 미로가 있다.

| 1    | 0    | 1    | 1    | 1    | 1    |
| ---- | ---- | ---- | ---- | ---- | ---- |
| 1    | 0    | 1    | 0    | 1    | 0    |
| 1    | 0    | 1    | 0    | 1    | 1    |
| 1    | 1    | 1    | 0    | 1    | 1    |

미로에서 1은 이동할 수 있는 칸을 나타내고, 0은 이동할 수 없는 칸을 나타낸다. 이러한 미로가 주어졌을 때, (1, 1)에서 출발하여 (N, M)의 위치로 이동할 때 지나야 하는 최소의 칸 수를 구하는 프로그램을 작성하시오. 한 칸에서 다른 칸으로 이동할 때, 서로 인접한 칸으로만 이동할 수 있다.

위의 예에서는 15칸을 지나야 (N, M)의 위치로 이동할 수 있다. 칸을 셀 때에는 시작 위치와 도착 위치도 포함한다.

## 입력

첫째 줄에 두 정수 N, M(2 ≤ N, M ≤ 100)이 주어진다. 다음 N개의 줄에는 M개의 정수로 미로가 주어진다. 각각의 수들은 **붙어서** 입력으로 주어진다.

## 출력

첫째 줄에 지나야 하는 최소의 칸 수를 출력한다. 항상 도착위치로 이동할 수 있는 경우만 입력으로 주어진다.

## 예제 입력 1

```
4 6
101111
101010
101011
111011
```

## 예제 출력 1

```
15
```

## 예제 입력 2

```
4 6
110110
110110
111111
111101
```

## 예제 출력 2

```
9
```

## 예제 입력 3

```
2 25
1011101110111011101110111
1110111011101110111011101
```

## 예제 출력 3

```
38
```

## 예제 입력 4

```
7 7
1011111
1110001
1000001
1000001
1000001
1000001
1111111
```

## 예제 출력 4

```
13
```

```c++
//solution
#include <cstdio>
#include <queue>
using namespace std;
const int MAX = 105;

struct position {
	int y, x;
};

int n, m;
int map[MAX][MAX];
int dirY[4] = {-1, 1, 0, 0};
int dirX[4] = { 0, 0, -1, 1};

void bfs(int y, int x) {
	queue<position> q;
	position pos;
	pos.y = y;
	pos.x = x;
	q.push(pos);

	while (!q.empty()) {
		int curY = q.front().y;
		int curX = q.front().x;
		q.pop();
		for (int i = 0; i < 4; i++) {
			int ny = curY + dirY[i];
			int nx = curX + dirX[i];
			position np;
			np.y = ny;
			np.x = nx;
			if (ny >= 0 && ny < n && nx >= 0 && nx < m) {
				if (map[ny][nx] == 1) {
					map[ny][nx] = map[curY][curX] + 1;
					q.push({ ny, nx });
					//q.push(np);
				}
				
			}
		}
	}

}

int main() {
	scanf("%d %d", &n, &m);
	for (int i = 0; i < n; i++) {
		for (int j = 0; j < m; j++) {
			scanf("%1d", &map[i][j]);
		}
	}

	bfs(0, 0);
	printf("%d\n", map[n - 1][m - 1]);

	return 0;
}
```
