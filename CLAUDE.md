GitHubにプッシュする際のリポジトリは以下を利用してください。
https://github.com/OdANNNNNNNNNao/02task-board.git

Git運用ルールとして、コードを変更するたびに、GitHubにプッシュする旨を含めてください。

## デプロイ先
https://odannnnnnnnnao.github.io/02task-board/

## 技術スタック
- React 19 + TypeScript
- Vite（ビルドツール、`base: '/02task-board/'`でGitHub Pages配信用に設定）
- oxlint（Lint）
- GitHub Actions + GitHub Pages（`main`へのpushで自動デプロイ）

## コンポーネントの命名規約
- ファイル名はコンポーネント名と同じPascalCase（例: `TaskForm.tsx`、`TaskItem.tsx`、`TaskList.tsx`）
- コンポーネントは`src/components/`配下に1ファイル1コンポーネントで配置
- Propsの型は`<コンポーネント名>Props`というinterfaceで定義し、ファイル内で分割代入して受け取る
- コンポーネントは名前付き関数で定義し、ファイル末尾で`export default`
- ドメインの型（`Task`など）は`src/types.ts`に集約する
