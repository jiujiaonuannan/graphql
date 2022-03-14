## Quick start 

- 1. 进入项目下安装依赖 yarn install
- 2. 启动json-server yarn json-server 服务启动后可以访问http://localhost:3000/users/40访问存储在db.json中的数据
- 3. 启动express服务 yarn dev 服务启动后访问 localhost:4000/graphql 可按照下面的指令对数据进行查询 添加删除等

```
	query {
		alex: user(id: "40") {
			id,
			firstName,
			age,
			company {
				description
				name
			}
		}
		bubble: user(id: "41") {
			id,
			firstName,
			age,
		}
		
	}
```


```
mutation {
  addUser(firstName: "alvin", age: 25) {
    firstName
    age
  }
}


mutation {
  deleteUser(id: "pS2nGttCE"){
    id
  }
}

```
