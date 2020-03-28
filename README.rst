Build error
-----------

huseyin@admins-MBP graph % cargo build
   Compiling graph v0.1.0 (/Users/huseyin/projects/graph)
error: cannot find macro `graphql_object` in this scope
  --> src/main.rs:14:1
   |
14 | graphql_object!(Query: Ctx |&self| {
   | ^^^^^^^^^^^^^^

warning: unused import: `FieldResult`
 --> src/main.rs:3:15
  |
3 | use juniper::{FieldResult, Variables, EmptyMutation};
  |               ^^^^^^^^^^^
  |
  = note: `#[warn(unused_imports)]` on by default

error[E0107]: wrong number of type arguments: expected at least 3, found 2
  --> src/main.rs:26:15
   |
26 | type Schema = juniper::RootNode<'static, Query, EmptyMutation<Ctx>>;
   |               ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ expected at least 3 type arguments

error: aborting due to 2 previous errors

For more information about this error, try `rustc --explain E0107`.
error: could not compile `graph`.

To learn more, run the command again with --verbose.
huseyin@admins-MBP graph %
