#  Migrations

* 提供されているコマンドは下記の通り
* v2.2になってからの`db rollback`はまだ無い気がする(romのrakeタスク叩けば対応はできる)

```bash
$ bundle exec hanami db --help

Commands:
  hanami db create                                  # Create databases
  hanami db drop                                    # Delete databases
  hanami db migrate                                 # Migrates database
  hanami db prepare                                 # Prepare databases
  hanami db seed                                    # Load seed data
  hanami db structure [SUBCOMMAND]
  hanami db version                                 # Print schema version
```