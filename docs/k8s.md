# kubernetes 笔记

### 获取 kubernetes Dashboard token
```bash
	kubectl -n kube-system describe secret $(kubectl -n kube-system get secret | grep admin-user | awk '{print $1}')

```