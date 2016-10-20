# mzrm 

mzrm - simple program in python3 for delete zookeeper childrens by regexp

## Help

```
mzrm --help
usage: mzrm [-h] [--zk ZK] [--path PATH] [--child CHILD] [--regex REGEX]
Remove all childrens started with pattern(regexp is supported too). USE THIS
AT YOUR OWN RISK! THIS SOFTWARE MAY CONTAIN BUGS, AND MAY DESTROY YOUR DATA
AND KILL YOUR PARENTS, EVEN IF USED CORRECTLY. YOU HAVE BEEN WARNED!
optional arguments:
  -h, --help     show this help message and exit
  --zk ZK        Zookeeper hosts: node1:2181,node2:2181
  --path PATH    Zookeeper path: /my/path/to
  --child CHILD  Zookeeper child name start pattern: hell
  --regex REGEX  PCRE expression
```

## Examples

Remove by wildcard
```
mzrm --zk localhost:2181 --path /marathon/state --child buggy
```

Remove by regexp
```
mzrm --zk localhost:2181 --path /marathon/state --regex '^buggy.+(node4).+\..+$'
```
