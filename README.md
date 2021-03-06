# TJAPlayer3-f

TJAPlayer3をForkして、趣味程度に改造してます。  
スパゲッティコードと化してますね。うん。たまに整理しましょうかね。

実装してほしいものがあればGitHubのIssuesまたはDiscord鯖まで。  
趣味程度の改造なので時間はかかりますが、実装要望があったものは、なるべく実装したいと考えています。  
(Issueについて、確認済みのものはラベルを貼ります。)

masterブランチでほぼすべての開発を行います。  
(基本的なものはです。大規模なテスト実装などは、別のブランチに移行するかも。)

このプログラムを使用し発生した、いかなる不具合・損失に対しても、一切の責任を負いません。

## 推奨環境
Windows 7以降  
まぁ、Windows 10で動作確認をしているので、Windows 10が一番安定してるかと...

## 開発環境
Windows 10(Ver.1909)  
VisualStudio Community 2019

## バグ報告のお願い
改造者:[@Mr_Ojii](https://twitter.com/Mr_Ojii)はC#を2020年3月に初めて触りました。  
この改造をしながら、C#を勉強しているため、相当な量のバグが含まれていると思われます。  
バグを見つけた場合、TJAPlayer3-fから開かれたフォームまたは、Issuesで報告してもらえると、  
自分の勉強もはかどるのでよろしくお願いします。

## 開発状況(ログみたいなもん)
+ Ver.1.5.8.0 : より本家っぽく。
+ Ver.1.5.8.1 : 王冠機能の搭載(かんたん～おに & Edit(実質裏鬼))
+ Ver.1.5.8.2 : .NET Framework 4.0にフレームワークをアップデート
+ Ver.1.5.8.3 : 譜面分岐について・JPOSSCROLLの連打についての既知のバグを修正
+ Ver.1.5.9.0 : 複数の文字コードに対応
+ Ver.1.5.9.1 : WASAPI共有に対応
+ Ver.1.5.9.2 : .NET Framework 4.8にフレームワークをアップデート
+ Ver.1.5.9.3 : スコアが保存されないバグを修正 & songs.dbを軽量化
+ Ver.1.6.0.0 : 難易度選択画面を追加 & メンテモード追加(タイトル画面でCtrl+Aを押しながら、演奏ゲームを選択)
+ Ver.1.6.0.1 : Open Taiko Chartへの対応(β)
+ Ver.1.6.0.2 : 片開き(仮)実装
+ Ver.1.6.0.3 : 特訓モード(仮)実装
+ Ver.1.6.0.4 : 音色機能の実装・演奏オプション表示方法の変更
+ Ver.1.6.0.5 : FFmpeg APIを使用しての音声デコード機能を追加
+ Ver.1.6.1.0 : FFmpeg APIを使用しての動画デコード機能を追加
+ Ver.1.6.2.0 : .NET Core 3.1にフレームワークをアップデート

## Discord鯖
作っていいものかと思いながら、公開鯖を作ってみたかったので作ってしまいました。  
私のモチベにもなるから、気軽に入ってね。  
[https://discord.gg/AkfUrMW](https://discord.gg/AkfUrMW)

## 追加命令について
Testフォルダ内の「追加機能について.md」で説明いたします。

## 謝辞
このTJAPlayer3-fのもととなるソフトウェアを作成・メンテナンスしてきた中でも  
有名な方々に感謝の意を表し、お名前を上げさせていただきたいと思います。

- FROM/yyagi様
- kairera0467様
- AioiLight様

また、他のTJAPlayer関係のソースコードを参考にさせてもらっている箇所があります。  
ありがとうございます。

## ライセンス関係
以下のライブラリを追加いたしました。
* [ReadJEnc](https://github.com/hnx8/ReadJEnc)
* [SharpDX](http://sharpdx.org/)
* [Json.Net](https://www.newtonsoft.com/json)
* [FFmpeg.AutoGen](https://github.com/Ruslan-B/FFmpeg.AutoGen)
* [FFmpeg](https://ffmpeg.org/)
* [OpenTK](https://opentk.net/)
* [OpenAL Soft](https://openal-soft.org/)
* [discord-rpc-csharp](https://github.com/Lachee/discord-rpc-csharp)

ライセンスは「Test/Licenses」に追加いたしました。

## FFmpegについて
このリポジトリにはあらかじめFFmpegライブラリが同梱されています。  
同梱しているライブラリは[Zeranoe FFmpeg](http://ffmpeg.zeranoe.com/builds/)からのx86ライブラリです。  
DLL群のみでもよいのですが、デバッグ用に残しておきたいので、exeも同梱しています(READMEも残してあります)。  
バージョンは4.3.1です。(2020/09/16現在)

DLL群のバージョンアップをしたい方は自己責任で差し替えをしてください。  
LGPLやGPLに気を付けてくださいね。

## OpenAL Softについて
このリポジトリにはあらかじめOpenAL Softライブラリが同梱されています。  
同梱しているライブラリはx86ライブラリです。  
バージョンは1.15.1です。(2020/09/04現在)

# 以下AioiLight様作成のReadmeです

> # TJAPlayer3
> DTXManiaをいじってtja再生プログラムにしちゃった[TJAPlayer2fPC](https://github.com/kairera0467/TJAP2fPC)をForkして本家風に改造したアレ。
>
> この改造者[@aioilight](https://twitter.com/aioilight)はプログラミングが大変苦手なので、スパゲッティコードと化していると思います...すみません
>
> このプログラムを使用した不具合・問題については責任を負いかねます。
>
> ## How 2 Build
> - VisualStudio 2017 & C# 7.3
> - VC++ toolset
> - SlimDX用の署名
>
> ## 実装状況いろいろ
> - [x] 小さいコンボ数
> - [x] 踊り子
> - [x] モブ
> - [x] BPMと同期した音符アニメーション
> - [x] ゴーゴータイム開始時の花火
> - [x] 連打時の数字アニメーション
> - [x] ランナー
> - [x] 10コンボごとのキャラクターアニメーション
> - [x] ぷちキャラ
> - [x] 段位認定（段位チャレンジ）
>
> ## ロードマップみたいな
>
> Ver.1.4.x : 拡張性の増加、サウンド周りの変更、読み込める命令の追加（9月中）
>
> Ver.1.5.x : 段位認定機能の追加（11、12月中）
>
> Ver.1.6.x : 多言語対応（未定）
>
> Ver.1.7.x : フレームワークのアップデート、ライブラリの更新（未定）
>
> Ver.1.8.x : さらなる安定化を目指して（未定）
>
> Ver.2.x : Direct3D11、12への対応、保守体制へ（未定）
>
> ## ライセンス関係
> Fork元より引用。
> 
> > 以下のライブラリを使用しています。
> > * bass
> > * Bass.Net
> > * DirectShowLib
> > * FDK21
> > * SlimDX
> > * xadec
> > * IPAフォント
> > * libogg
> > * libvorbis
> > 
> > 「実行時フォルダ/Licenses」に収録しています。
> > 
> > また、このプログラムはFROM氏の「DTXMania」を元に製作しています。
