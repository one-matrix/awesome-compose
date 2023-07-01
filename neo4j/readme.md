
导出
neo4j-admin dump --database=neo4j --to=[你定义的名字].dump
加载
neo4j-admin load --from=/data/cmekg-v4.4.dump --database=test --force


在容器内部进入conf目录，修改neo4j.conf
修改如下内容处。

# The name of the default database
#dbms.default_database=test