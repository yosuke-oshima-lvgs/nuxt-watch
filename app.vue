<template>
  <div>
    <h1>Single</h1>
    <p>1つの変数を監視する</p>
    <Computed />
    <hr />
    <Watch />
    <hr />
    <WatchImmediate />
    <hr />
    <WatchEffect />
    <hr />

    <h1>Multi</h1>
    <p>1つの変数を監視して複数の変数をコールバック関数に渡す</p>
    <MultiComputed />
    <hr />
    <MultiWatch />
    <hr />
    <MultiWatchImmediate />
    <hr />
    <MultiWatchEffect />
    <hr />

    <h1>Async</h1>
    <p>1つの変数を監視して非同期で処理する</p>
    <AsyncComputed />
    <hr />
    <AsyncWatch />
    <hr />
    <AsyncWatchImmediate />
    <hr />
    <AsyncWatchEffect />
    <hr />
  </div>
</template>
