##課題 
###課題内容  

仮想スイッチを停止したら、コントローラで次のメッセージを表示するようにしてみよう:
```
Bye 0xabc
```
###変更箇所
HelloTremaクラス内に以下の関数を追加する。  
```
  def switch_disconnected(dpid)  
    logger.info "Bye #{dpid.to_hex}"  
  end  

```
switch_disconnected関数はスイッチが切断された時に呼び出される関数である。
その関数内でlogger.info関数を呼び出しメッセージを表示する。

