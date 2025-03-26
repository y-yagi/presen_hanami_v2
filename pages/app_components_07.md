#  Components

* `Container`と`Components`の仕組みは、[dry\-system](https://dry-rb.org/gems/dry-system/)を使っている
  * dry-systemをほぼそのまま使用しており、ちょっとAPIをラップしている位
* 「依存関係を完全にコントロールし、個々のコンポーネント間の境界線を引くのが非常に簡単な方法でシステムを構成するため」らしい
* dry-systemの発想は、[stuartsierra/component](https://github.com/stuartsierra/component)というClosureのライブラリから来ているとのこと
* 詳細が気になる方は、上記dry-systemのドキュメントをみてね