# 백준 15686 치킨배달

>https://www.acmicpc.net/problem/15686

* 다 못풀었는데.. cominations 조합 만드는데 사용한다는 거 배웠다....

```

# 도시 배열 수, 치킨집 개수
N, M = map(int, input().split())

# 도시 배열 받음
city = [list(map(int, input().split())) for _ in range(N)]

# 집과 치킨집 저장하기
house = []
bhc = []
for i in range(N):
    for j in range(N):
        if city[i][j] == 1:
            house.append((i, j))
        elif city[i][j] == 2:
            bhc.append((i, j))

여기까지 내가 작성 / 아래는 구글 ,, 완성코드
-----------------------------------------------------------------------------------------
# 최대 조합찾는 함수... ?
from itertools import combinations

n,m=map(int, input().split())
maps=[]
for i in range(n):
  maps.append(list(map(int, input().split())))

home=[]
chicken=[]
for i in range(n):
  for j in range(n):
    if maps[i][j]==1:
      home.append((i,j))
    elif maps[i][j]==2:
      chicken.append((i,j))
# 저장한 이후에 진행과정..
------------------------------------------------------------------------------------------
# 가!~능~한 최대 조합 찾아서 저장하는 듯
pick_chicken=list(combinations(chicken,m))
# 빈 리스트 만들어서 체크해주는건가?/
result=[0]*len(pick_chicken)

# 집 기준 반복
for i in home:
	# 최대 치킨집 수 만큼 반복?
  for j in range(len(pick_chicken)):
		# 얘는 왜 나왔지
    a=100
    for k in pick_chicken[j]:
			# 거리 구해주는거 같고
      temp=abs(i[0]-k[0])+abs(i[1]-k[1])
			# 여기 이후로는 돌대갈 이해 X
      a=min(a,temp)
    result[j]+=a

print(min(result))
```

