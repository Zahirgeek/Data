## [短信分类]()
- 文本分类：伯努利贝叶斯、多项式贝叶斯
- 稀松矩阵占内存小

		from scipy import sparse
		a = np.zeros(shape = (1000,1000))
		a[500,200] = 2
		a[801,256] = 10
		# 转换为稀松矩阵
		sparse.csr_matrix(a)
	
- ham: 正常短信
- spam: 垃圾短信
- 使用高斯分布贝叶斯训练文本(效果很差，耗时长)：

		X_train.toarray()