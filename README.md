# mojaproxy
easy proxy switcher

## これなに
プロキシを切り替えられます。  
学校ではプロキシが挟まるのに自宅にはないので、いちいち設定を変えるのが面倒で書きました。  
.bashrcを書き換えます。なんかあったときのためにスクリプトと同じディレクトリにbackupを取ります。

## はうとぅゆーず
1. clone
```
git clone https://github.com/s10akir/mojaproxy.git ~/.mojaproxy
```

2. プロキシ設定
~/.mojaproxy/mojaproxyの5行目を書き換え
```
PROXY = 'http://proxy.example.com:port/'
```

3. pathを通す
```
echo 'export PATH="$HOME/.mojaproxy"' >> ~/.bashrc
```

4. 実行
```
mojaproxy on
or
mojaproxy off
or
mojaproxy rescue
```

5. .bashrcを読ませるためにシェル再起動
```
exec $SHELL
or
source .bashr
```