【テスト環境用】maintelog v18d-dev-20260402
適用先: https://koheips.github.io/maintelog-dev/

v18d 修正内容
【バグ修正】
・要対応の「次回 26/03/12/undefined/undefined」→ 根本原因はnextDateがスラッシュ形式で
  生成されているのにfmtShortがハイフン分割していたため。nextDateをISO形式で統一して修正
・保存ボタン押下で何も表示されない → showSaveToast関数を追加。保存・作業追加両方に対応
・メモ色が反映されない → renderHistory内のメモpillのcssTextをloadMemoColor()参照に修正
・背景色/文字色グリッドが空表示 → _newTaskBg/_newTaskTextのモジュールスコープ変数管理に変更
・追加ボタンで保存できない → addTaskFromInputsのcolor参照をモジュール変数に切り替え

【UI変更】
・カラー選択を全て画像4形式のカスタムグリッドに統一（iOSネイティブピッカー不使用）
・「+」ボタンはHexコード入力プロンプトでカスタム色追加
・折りたたみボタン（▼）の文字色を白に、フォント太字化
・「トリガー種別」→「判定基準」、「閾値」→「基準値」に変更（編集モーダルも対応）
・作業マスターの作業名フォントサイズを15pxに拡大
