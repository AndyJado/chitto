意图通过一个repo管理我的开发工具链.

一个记录我使用其他repo的repo

应该用submodule吧?

```rust
bash!(git submodule add <repo-url>) => {
  the whole repo clone into repo;
  staged with |2 file| change = {
    .gitmodules = {path & url};
    <&repo_name> = {Subproject commit <SHA>};
  }
};

bash!(git submodule init) => {
  todo()!
}

```
