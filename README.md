# delphin-tiniest-grammar

A reduction of the 2020 Grammar Matrix's minimal grammar for testing purposes. The resulting files are only 249 lines:

```
$ wc -l *{tdl,rpp}
      24 config.tdl
      15 definition.tdl
       7 lexicon.tdl
       9 qc.tdl
       3 roots.tdl
       1 rules.tdl
     188 tiniest.tdl
       2 vanilla.rpp
     249 total
```

The grammar only parses the string `"n1 iv"` and produces the following MRS and tree:

```
SENT: n1 iv
[ LTOP: h0
INDEX: event2
RELS: < [ "_n1_n_rel"<-1:-1> LBL: handle3 ARG0: ref-ind4 ]
 [ "_iv_v_rel"<-1:-1> LBL: handle1 ARG0: event2 ARG1: ref-ind5 ] >
HCONS: < h0 qeq handle1 > ]
```

```
(subj-head 0 2
  (n1 0 1 ("n1"))
  (iv 1 2 ("iv")))
```

Note that as of v1 the MRS is not a valid MRS because it does not include a quantifier.
