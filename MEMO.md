## useState, useContext, 状態管理ライブラリの比較

- useState
  - 状態が変化すると、props のバケツリレーを行った親コンポーネントすべてが再レンダリングされる
- useContext
  - 状態を受け取る子コンポーネントだけが再レンダリングされる
  - `useContext`のファイルが膨大になる
    - 1 ファイルに状態をまとめると、1 つの状態が変化しただけでも、ファイルにまとめた状態を持つコンポーネントはすべて再レンダリングされる
  - useState と比べるとテストがしにくい
- 状態管理ライブラリ
  - ひとつのファイルで複数の状態を管理できる
    - useContext と異なり、変化した状態を使用しているコンポーネントのみ再レンダリングされる
  - useContext と同じくテストはしにくい
- https://blog.uhy.ooo/entry/2021-07-24/react-state-management/