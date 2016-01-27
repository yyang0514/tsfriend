# FORMULA CONCEPT  DEFINE: #



> formula is two son tree,  has 3 kind of tree node.
    1. operator (including + - `*` / =)
    1. parameter
    1. number (non zero unsign integer)

> leaf node type can be and only can be paramter or number.
> operator node must have two sons.

**NOTE:**
> All operator with same priority. if you want to change the priority, use ().
> _zero_ is not support for _zero_ may cause calcuate exception.



```
example:
1.
    expression:         2
    formula tree:     (2)

2.
    expression:         section_lenth
    formula tree:    (section_lenth)

3.
    expression:         A + 2
    formula tree:       
                          (+)
                        /     \
                      (A)      (2)

4.
    expression:        3 * A  + (B - 2 ) + C
    formula tree:  
                                     (+) 
                                  /       \
                             (+)           (C)
                          /       \
                      (*)          (-)
                    /     \        /   \
                  (3)      (A) (B)    (2)

5.
    expression:        3 + A  - B * 2  = 5
    formula tree:  
                                   (=) 
                                /       \
                            (*)          (5)
                          /      \
                       (-)        (2)
                     /     \      
                  (+)      (B)
                /     \      
             (3)      (A)


```

[About page](http://code.google.com/p/tsfriend/wiki/About)