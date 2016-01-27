> # How to write a _user defined format_ file #

### _user defined format_ file    syntax : ###

1.
> "#" means comment, like \\ in C++.
> "@" means comment, same as #. but if followed by "include", it means include another file.

2.
> "@include file\_name "
> means include another format file _file\_name_.

3.
> "<_format type_: _format name_: _format ID_>"
> _format type_ can be _table_ or _descriptor_.
> > _format name_ is a string like "CAT".

> _format ID_ is table ID or descriptor tag.

4.
> "{" means sub body start.
> "}" means sub body end.

5.
> "`[`_keyword_`]` "
> _keyword_ always in `[]` ,only keywork can be in `[]`.
> > _keyword_ can be 'loop' 'if' 'else' or 'descriptor'.

6.

> "formula"
> currently _formula_ support '+'-'`*`'/'=', and they all has same priority, if you want to change the priority, please use "(" and ")" . formula can be nest,like `(A+B-(C*D)-10)` .
> Note: all the parameter A B C D must be able founded in previous content.

7.
```
   "[loop : name](formula)
   {
   }"
```
> means it's a loop subbody, and the total loop lenth in byte is calculate from formula. _loop_ key word is special, can have a name string,means what this loop is. but name is optional, if there is no name, will consider subbody as brothers. if is there is name string, will consider subbody as children of brothers with 'name string'.

8.
```
  [if](formula)
  {
  }
  [else]
  {
  }
```
> means if _formula_ != 0 goto subbody first else goto subbody second; else key and subbody is optional.

9.
> "`[`_descriptor_`]`"
> means it's _descriptor_ here.

10.
> "fieldname : formula : format "
> _Fieldname_ is a string like 'section lenth', and can be empty if you want it not display on content tree, I will treat it as a reserve field.
> > The field's lenth in bit is calcuate by formula, now we only support <= 255;

> _format_ is optional, can be 'b' 'd' 'x' 'c' 'm' or 's':
> > 'b' means binnary, 'd' means decimal, 'x' means hex, 'c' means BCD code, 'm' MJD code, 's' means string; the default is 'x'.



[examples download](http://code.google.com/p/tsfriend/downloads/detail?name=format%20example.rar&can=2&q=#makechanges)

[About page](http://code.google.com/p/tsfriend/wiki/About)

[formula help](http://code.google.com/p/tsfriend/wiki/formula)