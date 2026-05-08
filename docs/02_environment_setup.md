# 02. Environment Setup

この資料では、Unity Sprint 2026で使用する開発環境を構築します。

## この資料のゴール

この資料のゴールは以下です。

- Gitを使えるようにする
- GitHub CLIを使えるようにする
- GitHubにログインできる
- Visual Studio Codeを使えるようにする
- Unity Hubを使えるようにする
- Unity Editorをインストールする
- Unity HubからUnityプロジェクトを開けるようにする

今回は、Gitの詳しいコマンド操作は扱いません。

Gitの操作は、主にVSCodeのGUIを使って行います。

## 事前確認

作業を始める前に、以下を確認してください。

### PC

- MacまたはWindowsのPCを使用します
- ストレージ容量は30GB以上空いていることを推奨します
- 充電器を接続してください
- 可能であればマウスを用意してください

### アカウント

- GitHubアカウントが必要です
- Unityアカウントが必要になる場合があります

### ネットワーク

- インターネットに接続してください
- 大きなファイルをダウンロードするため、通信が安定している環境を推奨します

### 権限

- アプリをインストールできる権限が必要です
- 学校管理PCなどでインストール制限がある場合は、講師に相談してください

## 今日インストールするもの

今回導入する主なツールは以下です。

| ツール             | 用途                                      |
| ------------------ | ----------------------------------------- |
| Git                | 変更履歴を管理する                        |
| GitHub CLI         | GitHubへのログインや認証を行う            |
| Visual Studio Code | コード編集とGit操作に使う                 |
| Unity Hub          | Unity EditorやUnityプロジェクトを管理する |
| Unity Editor       | Unity制作本体に使う                       |

## Mac向けセットアップ

Macでは、Homebrewを使って必要なツールを導入します。

Homebrewは、Macでアプリや開発ツールをコマンドから導入するためのパッケージマネージャーです。

### 1. ターミナルを開く

Macでは「ターミナル」アプリを開きます。

Spotlight検索で `ターミナル` と入力すると見つかります。

### 2. Homebrewが入っているか確認する

以下のコマンドを実行します。

```bash
brew --version
```

バージョン番号が表示されれば、Homebrewはすでに使えます。

例：

```bash
Homebrew 4.x.x
```

### **3. Homebrewが入っていない場合**

Homebrewが入っていない場合は、公式サイトの手順に従ってインストールします。

インストール後、もう一度以下を実行してください。

```bash
brew --version
```

バージョン番号が表示されればOKです。

### **4. Gitをインストールする**

```bash
brew install git
```

インストール後、確認します。

```bash
git --version
```

### **5. GitHub CLIをインストールする**

```bash
brew install gh
```

インストール後、確認します。

```bash
gh --version
```

### **6. VSCodeをインストールする**

```bash
brew install --cask visual-studio-code
```

インストール後、LaunchpadまたはアプリケーションフォルダからVisual Studio Codeを開けるか確認します。

### **7. Unity Hubをインストールする**

```bash
brew install --cask unity-hub
```

インストール後、LaunchpadまたはアプリケーションフォルダからUnity Hubを開けるか確認します。

## **Windows向けセットアップ**

Windowsでは、wingetを使って必要なツールを導入します。

wingetは、Windowsでアプリをコマンドから検索・インストールするためのツールです。

### **1. ターミナルを開く**

Windowsでは、以下のどちらかを開きます。

- Windows Terminal
- PowerShell

可能であれば、管理者権限で開いてください。

### **2. wingetが使えるか確認する**

以下のコマンドを実行します。

```powershell
winget --version
```

バージョン番号が表示されれば、wingetは使えます。

### **3. wingetが使えない場合**

wingetが使えない場合は、Windowsのバージョンやアプリインストーラーの状態によって異なります。

講師に相談してください。

### **4. Gitをインストールする**

```powershell
winget install Git.Git
```

インストール後、ターミナルを開き直して確認します。

```powershell
git --version
```

### **5. GitHub CLIをインストールする**

```powershell
winget install GitHub.cli
```

インストール後、確認します。

```powershell
gh --version
```

### **6. VSCodeをインストールする**

```powershell
winget install Microsoft.VisualStudioCode
```

インストール後、スタートメニューからVisual Studio Codeを開けるか確認します。
（拡張機能もインストール）

### **7. Unity Hubをインストールする**

```powershell
winget install Unity.UnityHub
```

インストール後、スタートメニューからUnity Hubを開けるか確認します。
（指定したエディターのバージョンをインストール）

## **GitHub CLIでログインする**

GitHub CLIを使って、GitHubにログインします。

MacでもWindowsでも、以下のコマンドを実行します。

```bash
gh auth login
```

実行すると、いくつか質問が表示されます。

基本的には、以下の流れで進めます。

```
What account do you want to log into?
> GitHub.com

What is your preferred protocol for Git operations?
> HTTPS

Authenticate Git with your GitHub credentials?
> Yes

How would you like to authenticate GitHub CLI?
> Login with a web browser
```

ブラウザが開いたら、GitHubにログインして認証を完了します。

### **今回HTTPSを使う理由**

GitHubへの接続方法には、大きく分けてHTTPSとSSHがあります。

今回は、初学者向けにHTTPSを使います。

SSHは便利ですが、SSH鍵の作成や登録が必要になり、説明量が増えます。

そのため、Unity Sprint 2026ではHTTPSを推奨します。

## **GitHubログイン確認**

認証ができたか確認します。

```bash
gh auth status
```

ログイン済みであることが表示されればOKです。

うまくいかない場合は、講師に相談してください。

## **ここまでできたら完了**

以下ができていれば、環境構築は完了です。

- Gitが使える
- GitHub CLIが使える
- GitHubにログインできている
- VSCodeが開ける
- Unity Hubが開ける
- Unity Editorがインストールされている

## **よくあるトラブル**

### **PCの空き容量が足りない**

Unity Editorは容量を多く使います。

不要なファイルを削除するか、別のPCを使えるか相談してください。

### **コマンドが見つからない**

例：

```
command not found: brew
git is not recognized
gh is not recognized
winget is not recognized
```

この場合、以下を確認します。

- インストールが完了しているか
- ターミナルを開き直したか
- PCを再起動したか
- PATHが通っているか

わからない場合は講師に相談してください。

### **gh auth loginがうまくいかない**

以下を確認します。

- GitHubアカウントにログインできるか
- ブラウザが開くか
- 認証コードを正しく入力したか
- HTTPSを選択しているか

うまくいかない場合は、一度以下を確認します。

```bash
gh auth status
```

### **Unity Hubにログインできない**

以下を確認します。

- メールアドレスとパスワードが正しいか
- ブラウザでUnityにログインできるか
- ネットワークが安定しているか

### **Unity Editorのインストールが終わらない**

Unity Editorのインストールには時間がかかります。

特にネットワークが混雑している場合、かなり時間がかかることがあります。

しばらく待っても進まない場合は、講師に相談してください。
