Build error
-----------

::

   huseyin@admins-MBP graph % cargo build
      Compiling graph v0.1.0 (/Users/huseyin/projects/graph)
   error[E0433]: failed to resolve: could not find `tests` in `juniper`
    --> src/main.rs:6:5
     |
   6 |     tests::{model::Database, schema::Query},
     |     ^^^^^ could not find `tests` in `juniper`

   error[E0433]: failed to resolve: use of undeclared type or module `pretty_env_logger`
     --> src/main.rs:13:5
      |
   13 |     pretty_env_logger::init();
      |     ^^^^^^^^^^^^^^^^^ use of undeclared type or module `pretty_env_logger`

   error[E0433]: failed to resolve: use of undeclared type or module `Database`
     --> src/main.rs:17:23
      |
   17 |     let db = Arc::new(Database::new());
      |                       ^^^^^^^^ use of undeclared type or module `Database`

   error[E0425]: cannot find value `Query` in this scope
     --> src/main.rs:19:9
      |
   19 |         Query,
      |         ^^^^^ not found in this scope

   error[E0412]: cannot find type `Database` in this scope
     --> src/main.rs:20:25
      |
   20 |         EmptyMutation::<Database>::new(),
      |                         ^^^^^^^^ not found in this scope

   error[E0412]: cannot find type `Database` in this scope
     --> src/main.rs:21:29
      |
   21 |         EmptySubscription::<Database>::new(),
      |                             ^^^^^^^^ not found in this scope

   error[E0599]: no method named `clone` found for struct `std::sync::Arc<_>` in the current scope
     --> src/main.rs:26:22
      |
   26 |         let ctx = db.clone();
      |                      ^^^^^ method not found in `std::sync::Arc<_>`
      |
      = note: `db` is a function, perhaps you wish to call it

   error: aborting due to 7 previous errors

   Some errors have detailed explanations: E0412, E0425, E0433, E0599.
   For more information about an error, try `rustc --explain E0412`.
   error: could not compile `graph`.

   To learn more, run the command again with --verbose.
   huseyin@admins-MBP graph %
