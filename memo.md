* [Ruby on Rails — Rails 8\.0: No PaaS Required](https://rubyonrails.org/2024/11/7/rails-8-no-paas-required)
* [ONCE — Writebook](https://once.com/writebook)
* Enter Kamal 2 + Thruster
  * Kamalは元々MRSKでしたね
  * [Kamal: hot deployment tool to watch—or a total game changer?—Martian Chronicles, Evil Martians’ team blog](https://evilmartians.com/chronicles/mrsk-hot-deployment-tool-or-total-game-changer#who-will-benefit-the-most-from-kamal)
  * [Replace Traefik with kamal-proxy](https://github.com/basecamp/kamal/pull/940)
  * [Kamal Handbook: The missing manual](https://kamalmanual.com/handbook/)
  * [Why we're leaving the cloud](https://world.hey.com/dhh/why-we-re-leaving-the-cloud-654b47e0)
* A Solid Reduction of Dependencies
* Getting SQLite ready for production
  * https://www.youtube.com/watch?v=wFUy120Fts8&t=0s
  * ↑の資料 [Supercharge the One Person Framework with SQLite \| Fractaled Mind](https://fractaledmind.github.io/2024/10/16/sqlite-supercharges-rails/)
    * [How \(and why\) to run SQLite in production \| Fractaled Mind](https://fractaledmind.github.io/2023/12/23/rubyconftw/)
  * [Performance tune the SQLite3 adapter connection configuration](https://github.com/rails/rails/pull/49349)
  * [Ensure SQLite transaction default to IMMEDIATE mode](https://github.com/rails/rails/pull/50371)
  * [Open & writable database connections carried across fork() are automatically discarded in the child](https://github.com/sparklemotion/SQLite3-ruby/pull/558)
* Replacing Sprockets with Propshaft
  * [ONCE \#1 is entirely \#nobuild for the front\-end](https://world.hey.com/dhh/once-1-is-entirely-nobuild-for-the-front-end-ce56f6d7)
* Generating the authentication basics
  * テーブルは2つusersとsessions
  * ログイン、ログアウト、パスワードリセット
  * cookieにはsession idを設定
  * サインアップフローは無し
    * これは通常アプリケーション毎に違う可能性がある為、とのこと
  * ログイン処理にはrate_limitが指定されている
* その他メモ
  * [37signals Dev — De\-cloud and de\-k8s — bringing our apps back home](https://dev.37signals.com/bringing-our-apps-back-home/)
  * CHANGELOGS
    * Action View
      * Rename `text_area` methods into `textarea
      * Rename `check_box*` methods into `checkbox*`.
      * Action Text
        * Rename `rich_text_area` methods into `rich_textarea`
    * Action Pack
      *  `params#expect`
      * strict_freshness
      * Support `immutable` directive in Cache-Control
      * Add `connect` route helper.
    * Active Model
      * Add `:except_on` option for validations. Grants the ability to _skip_ validations in specified contexts.
    * Active Record
      * Allow `ActiveRecord::Base#pluck` to accept hash arguments with symbol and string values.
      * Allow `drop_table` to accept an array of table names.
      * When running `db:migrate` on a fresh database, load the databases schemas before running migrations.
      * Deprecate `unsigned_float` and `unsigned_decimal` short-hand column methods.
      * Make Active Record asynchronous queries compatible with transactional fixtures.
      * Add support for SQLite3 full-text-search and other virtual tables.
      * Support use of alternative database interfaces via the `database_cli` ActiveRecord configuration option.
      * Include schema name in `enable_extension` statements in `db/schema.rb`.
      * Support batching using custom columns.
      * Add `.shard_keys`, `.sharded?`, & `.connected_to_all_shards` methods.
      * Allow to configure `strict_loading_mode` globally or within a model.
    * Active Support
      * `ActiveSupport::TimeWithZone#inspect` now uses ISO 8601 style time like `Time#inspect`
      * `ActiveSupport::ErrorReporter#report` now assigns a backtrace to unraised exceptions.
    * railties
      * Defer route drawing to the first request, or when url_helpers are called
      * Add not-null type modifier to migration attributes.
      * Add a `script` folder to applications, and a scripts generator.
      * Add internal page `/rails/info/notes`, that displays the same information as `bin/rails notes`.
  * new_framework_defaults_8_0.rb
    * Rails.application.config.active_support.to_time_preserves_timezone = :zone
    * Rails.application.config.action_dispatch.strict_freshness = true
    * Regexp.timeout = 1

