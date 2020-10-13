# keep a changelog
https://keepachangelog.com/
変更履歴を記録しましょう。

## About
プロジェクトがどのバージョンで、どういった変更があったのかというリストが記録されたファイルを「changelog (変更履歴)」といいます。

Gitには履歴を保存する機能がありますが、コミットする方法によっては細かすぎて (またはいろんな要素が入りすぎて) わかりにくかったりします。そのためGitの履歴とは別にわかりやすい記録があると、プロジェクトにかかわる人やプロジェクトによって生み出されたソフトウェアを使うユーザーが正確に把握しやすくなります。

## Format

```md
# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]
### Add
- ...

### Changed
- ...

## [MAJOR.MINOR.PATCH] - YYYY-MM-DD
### Add
- ...

### Changed
- ...

### Deprecated
- ...

### Removed 
- ...

### Fixed
- ...

### Security
- ...

[Unreleased]: https://github.com/olivierlacan/keep-a-changelog/compare/v1.0.0...HEAD
[MAJOR.MINOR.PATCH]: https://github.com/olivierlacan/keep-a-changelog/compare/v0.3.0...v1.0.0
```
