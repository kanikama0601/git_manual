# Gitの使い方
GUIがメインのWindows上でGitを使うと、フォルダが増えて圧迫感が出る為、WSL上で動作させることを推奨します。
今回はWSL(Ubuntu)上で動作させるマニュアルです。  
<br>

## キーの作成＆同期
### 1.フォルダの作成
まず、.sshフォルダが無いと思われるので、作成します。  
```shell
mkdir ~/.ssh
```
<br>

### 2.sshキーを作成
先ほど作成したフォルダを開き、ssh-keygenを実行します。
以下のコマンドになります。
```shell
cd ~/.ssh
ssh-keygen -t rsa
```
これを実行すると、  
まず以下が表示されます。  
**Enter file in which to save the key (/home/kanikama0601/.ssh/id_rsa):**  
特に指定がない限り、このままEnterでOKです。  
<br>

次に以下が表示されます。  
**Enter passphrase (empty for no passphrase):**  
パスフレーズ(パスワード)は不要なので、このままEnterを押してください。  
<br>

最後に以下が表示されます。
**Enter same passphrase again:** 
これも、そのままEnterを押してください。  
<br>

すると、以下が表示されるのでこれで完了です。
```
Your identification has been saved in /home/kanikama0601/.ssh/id_rsa
Your public key has been saved in /home/kanikama0601/.ssh/id_rsa.pub
The key fingerprint is:
SHA256:9efJkLRLtOthwsvhcpwac/cEklWojcjF1e4/1l9rxNM kanikama0601@LAPTOP-3H16INMU
The key's randomart image is:
+---[RSA 3072]----+
|         . ..o.  |
|          o ...  |
|       . o.++.   |
|        o.o*.+.  |
|        S o O.o .|
|         . o O.=E|
|        o.=.* *.+|
|        .*+B + +=|
|        .++ . +.+|
+----[SHA256]-----+
```
<br>

### 3.GitHubにキーを登録
