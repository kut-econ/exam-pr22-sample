# プログラミング2022 期末試験

## Q1

10GiBは何MiBバイトですか？答えなさい。

Ans. 10240

## Q2

次のうち、正しい記述には○を、誤った記述には×をつけなさい。(部分点あり)

1. Pythonで書かれたプログラムは一般にC言語のプログラムより高速である。
2. Python、R、Fortranは全てインタープリタ型言語である。
3. マシン語からC言語のコードを生成することを逆コンパイルと呼ぶ。
4. CPythonはC言語で実装されたPythonのインタープリタである。
5. CPUは演算機能を備えているが、主記憶装置(メモリ)にはそれがない。
6. 主記憶装置の情報を読み書きするときの最小単位は4ビットである。

Ans. x x x o o x

## Q3

10進数の2500を16進ダンプした際に得られる表示はどれか？正しい選択肢の番号を答えなさい。ただしリトルエンディアン格納方式の2バイト整数とする。

1. c409
2. 09c4
3. c940
4. 40c9

Ans. 1

## Q4

負の数-450を2の補数で表現したものは次のうちどれか?正しい選択肢を一つ選び、その番号を答えなさい。ただし2バイト整数でビッグエンディアン表記を用いることとする。

1. 00000001 11000010
2. 11111110 00111101
3. 11111110 00111110
4. 00111110 11111110

Ans. 3

## Q5

42.46875を単精度浮動小数点としてビット列表記したものは次のうちどれか。正しい選択肢を一つ選び、その番号を答えなさい。

1. 0-00000101-10101001 11100000 0000000
2. 0-00000101-01010011 11000000 0000000
3. 0-10000100-01010011 11000000 0000000
4. 0-10000100-10101001 11100000 0000000

Ans. 3

<div style="page-break-before:always"></div>

## Q6

Git/Githubに関する問題です。Github上のリモートリポジトリrepoは唯一のブランチmasterを持っているとします。これを自身のパソコン上にクローンしてローカルリポジトリrepoを作成したとします。ローカルのrepo内で次の一連のコマンドを実行したあと、リモートとローカルの状態として正しいものを一つ選びなさい。

```bash
git checkout -b new
git push -u origin new
git checkout -b new2
git branch -d new
```

1. リモート、ローカルともにmasterブランチのみが存在
2. リモートにはmasterのみ、ローカルはmaster、new、new2が存在
3. リモートにはmaster、new2が存在し、ローカルはmasterとnewが存在
4. リモートにはmaster、newが存在し、ローカルはmaster、new2が存在
5. リモート、ローカルともにmasterとnew2が存在

Ans. 4

## Q7

Git/Githubに関する問題です。ローカルリポジトリrepo内に存在するファイルcode.pyに編集を加えたあと、ステージング・コミットしたとします。このコミットをキャンセルし、ステージングする直前の状態に戻すためのコマンドとして正しいものを一つ選びなさい。

1. git reset --mixed HEAD
2. git reset --soft HEAD^
3. git reset --mixed HEAD^
4. git reset --soft HEAD

Ans. 3

## Q8

Git/Githubに関する問題です。ローカルリポジトリrepo内で4つのコミットcommit0, commit1, commit2, commit3を行ったとする。次の一連のコマンドを実行したあと、作業エリアがとっている状態として正しいものを一つ選びなさい。

```bash
git revert HEAD
git reset --hard HEAD^
git revert HEAD
git revert HEAD
```

1. commit0と同じ内容
2. commit1と同じ内容
3. commit2と同じ内容
4. commit3と同じ内容

Ans. 4

<div style="page-break-before:always"></div>

## Q9

Git/Githubに関する問題です。ローカルリポジトリrepo内で4つのコミットcommit0, commit1, commit2, commit3を行った直後、次のコマンドを続けて実行したとします。

```bash
git reset --soft HEAD^
git reset --mixed HEAD^
```

このあと、作業エリアの状態として正しいものを一つ選びなさい。

1. commit0と同じ内容
2. commit1と同じ内容
3. commit2と同じ内容
4. commit3と同じ内容

Ans. 2

## Q10

次のRコードを実行したときに得られる出力として正しいものを一つ選びなさい。

```R
x <- 1:4
y <- x
y[1:2] <- c(3,4)
x[3] <- 5
print(x)
```

1. `[1] 1 2 5 4`
2. `[1] 3 4 5 4`
3. `[1] 1 3 4 5`
4. `[1] 1 2 3 5`

Ans. 1

## Q11

次のPythonコードを実行したときに得られる出力として正しいものを一つ選びなさい。

```python
x = [1,2,3,4,5]
y = x
x.insert(1,4)
print(y,x is y)
```

1. `[1,2,3,4,5] False`
2. `[1,4,2,3,4,5] True`
3. `[1,2,3,4,1,5] True`
4. `[1,2,4,3,4,5] True`

Ans. 2

<div style="page-break-before:always"></div>

## Q12

次のPythonコードを実行したときに得られる出力(もしくは結果)として正しいものを一つ選びなさい。

```python
x = [1,2,3]
y = x
z = y[:]
x[:] = z[:2]
print(x,y,z)
```

1. `[1,2],[1,2],[1,2]`
2. `[1,2] [1,2] [1,2,3]`
3. `[1,2] [1,2,3] [1,2,3]`
4. エラーが出力されて停止する

Ans. 2

## Q13

次のPythonコードを実行したあと、続けて実行したときにエラーが出ないコードには○を、エラーが出るコードには☓をつけなさい。(部分点あり)

```python
x = "letters"
```

1. `x == "capitals"`
2. `y = x * len(x * len(x))`
3. `x[:] = 'capitals'`
4. `x[2:3] == "le"`
5. `x[-1] != "5"`
6. `y = x[7]`
7. `y = x + "capitals"`
8. `y = x - x`
9. `y = x * 2 + 3`

Ans. o o x o o x o x x

<div style="page-break-before:always"></div>

## Q14

次のRコードを実行したときに得られる出力として正しいものを一つ選びなさい。

```R
library(pryr)
x <- c(1,2,3)
y <- x
z <- x
add <- address(z)
z[2] <- 5
print(c(address(x) == add, address(y) == add, address(z) == add))
```

1. `[1] FALSE FALSE FALSE`
2. `[1] TRUE TRUE FALSE`
3. `[1] FALSE FALSE TRUE`
4. `[1] TRUE TRUE TRUE`

Ans. 2

## Q15

次のPythonコードを実行したときに得られる出力として正しいものを一つ選びなさい。

```python
x = [['foo','bar','baz']]
y = x.copy()
y[0] = [1,2,3]
print(x,x is y)
```

1. `['foo','bar','baz'] True`
2. `['foo','bar','baz'] False`
3. `[1,2,3] True`
4. `[[1,2,3]] True`

Ans. 2

<!--<div style="page-break-before:always"></div>-->

## Q16

次のPythonコードを実行したときに得られる出力として正しいものを一つ選びなさい。

```python
x = [1,2,[3]]
y = x[:]
y[0] = 4
y[2].append(5)
print(x)
```

1. `[4,2,[3]]`
2. `[1,2,[3]]`
3. `[4,2,[3,5]]`
4. `[1,2,[3,5]]`

Ans. 4

<div style="page-break-before:always"></div>

## Q17

次のPythonコードを実行したときに得られる出力として正しいものを一つ選びなさい。

```python
import copy
x = [[[1]]]
y = x.copy()
z = copy.deepcopy(x)
print(y[0] is z[0],y[0][0] is z[0][0],y[0][0][0] is z[0][0][0])
```

1. `False False False`
2. `False False True`
3. `False True True`
4. `True True True`

Ans. 2

## Q18

次のPythonコードを実行したあと、変数yにリスト[7,5,3]を代入するためのコードとして正しいものを**2つ**選びなさい。

```python
x = list(range(10))
```

1. `y = x[7:2:-2]`
2. `y = x[3:8:-2]`
3. `y = x[-3:-8:-2]`
4. `y = x[-3:-7:-2]`

Ans. 1, 3

## Q19

次のPythonコードを実行した結果得られる出力を記述しなさい。解答例：`[[1],2,[3,4]]`

```python
x = [[1]]
x = x + 2 * x.copy()
x[1][:] = (3,4)
print(x)
```

Ans. `[[3,4],[3,4],[3,4]]`

## Q20

次のPythonコードを実行した結果出力される整数を答えなさい。

```python
x = 0
for i in range(10):
    if i % 4 == 0:
        x += 1
    elif i % 2 == 0:
        x += 1
print(x)
```

Ans. 5

## Q21

次のPythonコードを実行した結果出力される整数を答えなさい。

```python
x = 0
for i in range(10):
    if i % 4 == 0:
        x += 1
    if i % 2 == 0:
        x += 1
print(x)
```

Ans. 8

<!--<div style="page-break-before:always"></div>-->

## Q22

次のPythonコードを実行した結果出力される整数を答えなさい。

```python
x = 0
for i in range(10):
    if i % 4 == 0:
        x += 1
        if i % 2 == 0:
            x += 1
print(x)
```

Ans. 6

## Q23

次のPythonコードを実行した結果出力される整数を答えなさい。

```python
x = 0
for i in range(3):
    for j in range(i,3):
        x +=j
print(x)
```

Ans. 8

<div style="page-break-before:always"></div>

## Q24

次のPythonコードを実行したところ、下記の出力が得られたとします。

```python
import sys
x = sys.getsizeof("a")
y = sys.getsizeof("あ")
print(x,y)
```

```python
#出力
50 76
```

このとき、次のコードを実行したときの出力を整数値で答えなさい。

```python
print(sys.getsizeof("a"*10 + "あ"*5))
```

Ans. 104

## Q25

次のPythonコードを実行した際に得られる出力を文字列で答えなさい。解答例：`abCDefg`

```python
print("".join("aAbaAb".upper().split("AB"))*3)
```

Ans. `AAAAAA`

## Q26

次のPythonコードを実行した際に得られる出力を文字列で答えなさい。解答例：`abCDefg`

```python
print('aaab'.replace("aa","aab").replace("aba","a"))
```

Ans. `aab`

## Q27

次のPythonコードを実行した結果出力として得られる文字列を答えなさい。解答例：`abCDefg`

```python
trans = {ord(c)+2:c for c in 'abcdef'}
print("dfg".translate(trans))
```

Ans. `bde`

<div style="page-break-before:always"></div>

## Q28

次のうち、Pythonのタプルであるものには○を、そうでないものには☓をつけなさい。(部分点あり)

1. `(3,)`
2. `(3)`
3. `()`
4. `(())`
5. `(,)`
6. `((),)`

Ans. o x o o x o

## Q29

次のPythonコードを実行したとします。そのあと、ファイル`output.txt`をテキストエディタで開くと、どのような文字列が書いてあるか、ひらがなで答えなさい。

```python
str_byte = bytes([0xe3,0x81,0xa6,0xe3,0x82,0x93,0xe3,0x81,0x95,0xe3,0x81,0x84])
with open('./output.txt','bw') as file:
    file.write(str_byte)
```

ただし、ひらがなの`utf-8`エンコーディングは次で与えられます。

```bash
あいうえお --> e38182 e38184 e38186 e38188 e3818a 
かきくけこ --> e3818b e3818d e3818f e38191 e38193 
さしすせそ --> e38195 e38197 e38199 e3819b e3819d 
たちつてと --> e3819f e381a1 e381a4 e381a6 e381a8 
なにぬねの --> e381aa e381ab e381ac e381ad e381ae 
はひふへほ --> e381af e381b2 e381b5 e381b8 e381bb 
まみむめも --> e381be e381bf e38280 e38281 e38282 
や　ゆ　よ --> e38284 e38080 e38286 e38080 e38288 
らりるれろ --> e38289 e3828a e3828b e3828c e3828d 
わ　　　を --> e3828f e38080 e38080 e38080 e38292 
ん　　　　 --> e38293 e38080 e38080 e38080 e38080 
```

Ans. てんさい

## Q30

Python辞書を作成するコードとして正しいものには○を、誤っているものには☓をつけなさい。(部分点あり)

1. `x = dict.fromkeys((1,2,3),0)`
2. `x = dict(zip([1,2,3],'abc'))`
3. `x = {'a':1,():2}`
4. `x = {(1,):1,([],):2}`
5. `x = dict(a=1,b=2)`
6. `x = dict(1='a',2='b')`
7. `x = dict(((1,2),(3,4)))`
8. `x = dict({'a':1,'b':2},c=3)`

Ans. o o o x o x o o

<!--<div style="page-break-before:always"></div>-->

## Q31

次のPythonコードを実行したとします。

```python
x = dict()
x['dog']='bowwow'
x['cat']='meow'
```

ただし、各文字列のハッシュ値は次の通りであるとします。

|文字列|ハッシュ値|
|--|--|
|'dog'|0x675a75865a0ce7e4|
|'cat'|0x6e4d4b14d7db9ca9|
|'bowwow'|0x62e24392a62b560a|
|'meow'|0xbe06d9e514778ef6|

辞書`x`内部にあるインデックス配列の状態として正しいものを一つ選びなさい。

1. `-1 -1 0 -1 -1 -1 1 -1`
2. `-1 1 -1 -1 0 -1 -1 -1`
3. `1 -1 -1 0 -1 -1 -1 -1`
4. `-1 0 -1 -1 -1 1 -1 -1`

Ans. 2

## Q32

次のPythonコードを実行したとします。

```python
x = {'python','julia','java'}
y = {'ruby','pascal','julia'}
z = x.intersection(y)
a = y.union(x)
```

次のうち、TrueになるものにはT、FalseになるものにはFと答えなさい。(部分点あり)

1. `z.issubset(x)`
2. `a.issuperset(z)`
3. `y.issubset(z)`
4. `'julia' in z`

Ans. `T T F T`

<!--<div style="page-break-before:always"></div>-->

## Q33

次のPythonコードを実行した際に出力される整数を書きなさい。

```python
print({i % 3:i for i in range(10) if i % 2 == 0}[0])
```

Ans. 6

## Q34

次のPythonコードを実行したとき、`x`には何が代入されているか答えなさい。

```python
def func(x):
  if x > 1:
    x = 3
  else:
    return 
  return x

x = func(2)
```

Ans. 3

## Q35

次のPythonコードを実行した際に、印字される整数を答えなさい。

```python
def generator():
  for i in range(2,100):
    for j in range(2,i):
      if i % j == 0:
        break
    else:
      yield i
    
gen = generator()

print(list(gen)[4])
```

Ans. 11

## Q36

次のPythonコードを実行した際に出力される整数を答えなさい。

```python
x = range(10)
print([i-1 if i%3==1 else i+1 for i in x][4])
```

Ans. 3

<div style="page-break-before:always"></div>

## Q37

次のPythonコードを実行したとする。

```python
import numpy as np
x = np.arange(10)
```

以下の選択肢のうち、上のコードに引き続いて実行したとき、エラーが出ずに実行できるものには○を、エラーが出て停止するものには☓をつけなさい。(部分点あり)

1. y = x + range(10)
2. y = x + 2
3. y = x + (1,)
4. y = x + [0,1,2]
5. x[0:3] = 5
6. x[0:5:2] = (5,5,5)
7. x[0:3] = [0,1,2]

Ans. o o o x o o o

## Q38

次のPythonコードを実行したさいに、出力される整数を答えなさい。

```python
import numpy as np
x = np.arange(5)
y = x[0:5:2]
y += 3
print(x[2])
```

Ans. 5

## Q39

以下のPythonコードは、Numpyを用いて、切片10、傾き-2の線形モデルに従うサンプルサイズ100の疑似データを生成し、変数`y`に配列として格納するためのものである。ただし実測値`y`は標準正規分布に従う誤差を含むとする。`#????`に書くべきコードを答えなさい。

```python
import numpy as np
x = np.random.normal(5,2,100)
e = np.random.normal(0,1,100)
y = #????
```

Ans. `10 - 2 * x + e`

<div style="page-break-before:always"></div>

## Q40

以下のPythonコードを実行したさいに出力される整数を答えなさい。

```python
import numpy as np
x = np.arange(9).reshape((3,3))
y = x[1:,::2].sum()
print(y)
```

Ans. 22

## Q41

以下のPythonコードを実行したさいに出力される値を答えなさい。

```python
import numpy as np
x = np.arange(9).reshape((3,3))
y = x[:2,:]
y[1] += 3
print(x.sum(axis=0).mean())
```

Ans. 15.0

## Q42

以下のPythonコードを実行した際に出力される値を答えなさい。

```python
x = np.arange(6).reshape((2,3))
x += np.array([[1],[2]])
x -= np.array([1,2,3])
print(x.sum())
```

Ans. 12

## Q43

以下のPythonコードを実行した際に出力される値を答えなさい。

```python
x = 0
def f():
  x = 1
  return
f()
print(x)
```

Ans. 0

<div style="page-break-before:always"></div>

## Q44

以下のPythonコードを実行した際に出力される値を答えなさい。

```python
x = 0
def f():
  x = 1
  def g():
    global x
    x = 2
    return
  g()
  return x
print(f() + x)
```

Ans. 3

## Q45

Q44の最後の一行`print(f()+x)`を`print(x+f())`に書き換えた場合、出力される値を答えなさい。

Ans. 1

## Q46

次のPythonコードを実行した際に出力される文字列を答えなさい。

```python
def closure():
  x = ''
  def inner(y):
    nonlocal x
    if len(y) > len(x):
      x = y
    return x
  return inner

f = closure()
f('My')
f('friend')
f('is')
print(f('nice'))
```

Ans. `friend`

## Q47

Python3に関する以下の記述のうち、正しいものには○、誤っているものには☓をつけなさい。

1. グローバルスコープはプログラム全体である。
2. Pythonコード内で変数を参照すると、インタープリタはまず初めにビルトイン名前空間を検索する。
3. 一つのプログラム内で同じ`import`文を複数記述することにより、同じモジュールを何度でも再読み込みすることができる。
4. builtinsモジュール以外にもビルトインモジュールは存在する。

Ans. x x x o
