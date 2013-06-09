Liz
===

[![Build Status](https://travis-ci.org/killdream/poliz.png)](https://travis-ci.org/killdream/poliz)
![Dependencies Status](https://david-dm.org/killdream/poliz.png)

A minimal dialect of Lisp/[Kernel][], with first-class macros.

See the `spec.md` for the language's specification.

[Kernel]: http://web.cs.wpi.edu/~jshutt/kernel.html


## Example

```clj
;; You get first-class macros, this means that you can define List:
($define! list { | env . xs | xs })

(list (a b))  ;; => [["a", "b"]]

;; And you can define applicatives by way of wrap
($define! conj (wrap { | as bs | (cons as bs) }))

(conj 1 (list 2 3)) ;; => [1, 2, 3]
```

## Installing / Usage

    $ git clone git://github.com/killdream/poliz
    $ cd poliz/implementations/ometa-js
    $ npm install
    $ cat stuff.liz | ./bin/poliz
    

## Licence

WTFPL.
