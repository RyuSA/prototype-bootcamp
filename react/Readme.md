# React

## 手順

### 初期起動まで

1. cloneしてくる
```
git clone me
```

2. あげる
```
docker-compose up
```

3. コンテナにアタッチ（おすすめはVSCodeのRemoteDevelopmentでのAttach）
```
docker exec ...
```
4. /appに移動（Dockerfileに書いてある通り、/appが作業Dir）

5. Reactをインストール(時間がかかるのでここまでやっておく)
```
npx create-react-app bootcamp
```

なんかたまに失敗する(所感10%程度)ので、失敗したらbootcampディレクトリを削除して再度実行する

6. bootcampディレクトリに移動して、初回起動をする
```
cd bootcamp
yarn start
```

ブラウザでlocalhost:3000でReactのHelloworld画面が表示されることを確認する
今後はコンテナ内の/app/bootcampで作業するものとする

### App.jsをいじる
簡単に動かしてみる

```js:App.js
import React from 'react';
import './App.css';

function App() {
  return (
    <div className="App">
      <main className="App-main">
        <div>Hoge</div>
      </main>
    </div>
  );
}

export default App;
```

画面が変わることを確認する


### 「生徒管理」の画面作成

1. Appに生徒の項目をゴリゴリに書く(Stateの話)
2. Studentコンポーネントの作成
3. StudentコンポーネントにActionを追加
4. AppコンポーネントにActionを追加
