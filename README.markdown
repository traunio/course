# Functional Programming Course

My own solutions (partly copied) solutions to the nice NICTA course.

### Getting Help

There are two mailing lists for asking questions. All questions are welcome,
however, your first post might be moderated. This is simply to prevent spam.

1. [[nicta-fp]](https://groups.google.com/forum/#!forum/nicta-fp) is a Google
   Group for any queries related to functional programming. This mailing list is
   owned by NICTA and is open to the public. Questions relating to this course
   are most welcome here.

2. [[haskell-exercises]](https://groups.google.com/forum/#!forum/haskell-exercises)
   is a Google Group for queries related specifically to this NICTA funtional
   programming course material. This mailing list is not owned by NICTA, but is
   run by others who are keen to share ideas relating to the course. 

3. \#scalaz [on Freenode](irc://irc.freenode.net/#scalaz) is an IRC channel that is operated
   by others who are keen to share ideas relating to functional programming in
   general. Most of the participants of this channel have completed the NICTA 
   functional programming course to some extent. They are in various timezones
   and share a passion for functional programming, so may be able to provide
   relatively quick assistance with questions.

4. \#nicta-course [on Freenode](irc://irc.freenode.net/#nicta-course) is an IRC channel that
   is operated by others who are going through this course material on their
   own time and effort.


#### Running the tests

Some exercises include examples and properties, which appear in a comment above
the code for that exercise. Examples begin with `>>>` while properties begin
with `prop>`.

The solution to the exercise must satisfy these tests. You can check if you have
satisfied all tests with cabal-install and doctest. From the base directory of
this source code:

    > cabal update
    > cabal install cabal-install
    > cabal install --only-dependencies
    > cabal configure --enable-tests
    > cabal build
    > cabal test

Alternatively, you may run the tests in a single source file by using `doctest`
explicitly. From the base directory of this source code:

    > doctest -isrc -Wall -fno-warn-type-defaults <filename.hs>

Note: There is a [bug in GHC 7.4.1](http://ghc.haskell.org/trac/ghc/ticket/5820)
where for some configurations, running the tests will cause an unjustified
compiler error.

### Progression

It is recommended to perform some exercises before others. The first step is to
inspect the introduction modules.

* `Course.Id`
* `Course.Optional`
* `Course.Validation`

They contain examples of data structures and Haskell syntax. They do not contain
exercises and exist to provide a cursory examination of Haskell syntax. The next
step is to follow the recommended progression of modules:
* `Course.List`
* `Course.Functor`
* `Course.Applicative`
* `Course.Monad` 
* `Course.FileIO`
* `Course.State`
* `Course.StateT`
* `Course.Extend`
* `Course.Comonad`
* `Course.Compose`
* `Course.Traversable`
* `Course.ListZipper`
* `Course.Parser` *(see also `Course.Person` for the parsing rules)*
* `Course.MoreParser`
* `Course.JsonParser`
* `Course.Interactive`
* `Course.Anagrams`
* `Course.FastAnagrams`
* `Course.Cheque`


Answers for the exercises can be found here:
[https://github.com/tonymorris/course](https://github.com/tonymorris/course)

After these are completed, complete the exercises in the `projects` directory.

### References

* [The Haskell `error` function](http://hackage.haskell.org/packages/archive/base/latest/doc/html/Prelude.html#v:error)

* [Glasgow Haskell Compiler](http://haskell.org/ghc)
