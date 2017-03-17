# AI_note
### ---待整理---
2-1
inform and uniform search 的差別在對於我們對於問題的基本知識有多少。
uniform 不需要預估做哪一個選擇的cost多少，只針對目前唯一有的資訊。
tree search不偵測state是否有重複現象，graph search會去偵測（效能好，但有記憶體限制）。

2-4
bfs 
completeness : yes (if b is finite)
optimal : no (通常會找到最淺的goal，若path cost和深度正相關那就會是optimal)

uniform-cost 
每次都展開path cost最小的點
如果cost都一樣就是bfs
completeness : yes (cost >=0)
optimal : yes

2-5
dfs
遞迴方法
completeness : no (fail in infinite-depth space)
optimal : no
time complex : worst case是某一邊一直延升下去(要search1+b+b^2+...)
space : 只要紀錄上經過點的branch (b*m)

dls
complete : no (如果goal在限制層外)
optimal : no

ids
讓限制深度慢慢放寬
complete : yes
optimal : no
time : level=0的node要做d次，level=1的做d-1次....（d為深度）
space : bound為最後一次地展開（重複展開的不用記）

bid 
time o(2*b^(d/2)) d/2因為分前後兩邊展開
但不一定能從goal backtrace,也可能沒有goal或多個goal
