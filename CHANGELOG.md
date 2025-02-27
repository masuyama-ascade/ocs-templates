# 変更履歴

## 22.10.1-20230411

### 変更点

- HPCテンプレート: GPUを利用する場合のマシンイメージをCUDA 12.0対応のものに更新した

## 22.10.1-20230210

### 変更点

- HPCテンプレート: OpenHPC を 2.6.1 にアップデートした

## 22.04.1-20230131

### 新機能

- LMSテンプレート簡易構成版: コンテナイメージの更新手順を追加した
- LMSテンプレート簡易構成版: Shibboleth認証に対応した

### 変更点

- LMSテンプレート簡易構成版: MoodleコンテナをRocky Linux 8ベースに変更した
- LMSテンプレート簡易構成版: MoodleコンテナのPHPを8.0に変更した
- LMSテンプレート簡易構成版: コンテナの秘匿データをdocker secretsで扱うように変更した
- LMSテンプレート簡易構成版: HTTPS接続を行う場合のコンテナ構成を変更した
- LMSテンプレート簡易構成版: ログを転送する構成にsyslogに加えてFluentdに対応した
- LMSテンプレート簡易構成版: JupyterNotebook環境のgroup_varsに記録しているパラメータをバックアップ対象に追加した
- LMSテンプレート簡易構成版: Moodleの公開アドレスを変更するNotebookを追加した
- LMSテンプレート簡易構成版: デフォルトのコンテナイメージを4.1(LTS)に変更した
- 新しいJupyter Notebook環境(vcpjupyter/cloudop-notebook:20220725-ssl-cc)に対応した

## 22.04.1-20220729

### 変更点

- ベースコンテナを `vcp/base:1.8.1` 相当に更新した
- LMSテンプレート簡易構成版: Amazon EC2インスタンスを構築するためのライブラリを更新
- LMSテンプレート、LMSテンプレート簡易構成版: Moodle, MariaDBのバージョンを更新

## 22.04.1-20220630

### 変更点

- HPCテンプレート: OpenHPC を 2.5 にアップデートした

## 21.04.0-20220222

### 変更点

- HPCテンプレート: OpenHPC を 2.4 にアップデートした
- 講義演習環境テンプレート: [NII-cloud-operation/CoursewareHub-LC_manage-tools](https://github.com/NII-cloud-operation/CoursewareHub-LC_manage-tools/pull/3) の変更に対応した

### 障害修正

- 講義演習環境テンプレート: データベースのパスワードに記号が含まれていると起動に失敗する件に対応した
- 講義演習環境テンプレート: LTI連携に関するパラメータの保存方法を修正した

## 21.04.0-20210805

### 変更点
- LMSテンプレート
    - MariaDB 10.6に対応した
- LMSテンプレート簡易構成版
    - MariaDB 10.6に対応した

## 21.04.0-20210713

### 変更点

- 講義演習環境テンプレートのベースコンテナイメージを更新
    - Docker Engine を20.10.7にアップデート

## 21.04.0-20210701

### 新機能

- 講義演習環境テンプレート: [NII-cloud-operation/CoursewareHub-LC_platform](https://github.com/NII-cloud-operation/CoursewareHub-LC_platform)の[#14](https://github.com/NII-cloud-operation/CoursewareHub-LC_platform/pull/14)以降のPull requestsにて追加された機能を取り込んだ。主要なものは以下の通り。
    - 学認連携に基づく認証機能
    - LMSとの認証連携機能

### 変更点

- HPCテンプレート: OpenHPC を 2.3 にアップデートした
- HPCテンプレート: NGCカタログ 21.06 に対応した

## 20.04.2-20200617

### 新機能

- 計算資源補完テンプレートを追加した

## 21.04.0-20210512

### 新機能

- HPCテンプレート v2を追加した

## 20.04.1-20200819

### 新機能

- LMSテンプレート簡易構成版を追加した

## 20.04.1-20200603

### 新機能

- LMSテンプレート: 暗号化ボリュームに対応した

### 障害修正

- LMSテンプレート: 運用環境のMoodleをバージョンアップできない件を修正した

## 20.04.0

### 新機能

- LMSテンプレートを追加した
- HPCテンプレートを追加した
- 講義演習環境テンプレートを追加した
