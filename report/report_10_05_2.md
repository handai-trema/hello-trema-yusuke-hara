##課題
###課題内容
HelloTrema が起動したら次のメッセージを表示するようにしてみよう:
```
HelloTrema started.
```
###変更箇所
HelloTremaクラス内のstart関数を変更する。
```
 logger.info "#{self.class.name} started."
```
self.class.nameはインスタンス内からそのクラス名にアクセスできる。
selfはそのメソッドを実行しているオブジェクトを表す。classメソッドはそのオブジェクトのクラスを返すメソッドである。したがってHelloTremaクラス内のstartメソッドでself.classを実行するとHelloTremaクラスを返す。また、classクラスはmoduleクラスを継承しており、moduleクラスにはnameというインスタンスメソッドがある。このメソッドはクラスやモジュールの名前を返すメソッドである。したがってself.class.nameは"HelloTrema"を表すこととなる。
これをlogger.infoで表示する。  
また、Trema::Controllerにはそのクラスの名前を表すインスタンス変数
@nameが存在し、self.nameでアクセスできるためこれを表示してもよい。

