1. 读取数据，然后读取```Smiles```的分子指纹向量和每个```SMILES```的```logP```值和```TPSA```值；
2. 特征工程
    * 删除提取到的数据中的全为零的特征列;
    * 特征选择，使用```GradientBoostingRegressor``` 进行特征选择;
3. 最后再使用 ```GradientBoostingRegressor```进行预测，最终的得分是 0.3760 。

4. 所用的依赖： 我是在 InternStudio  开发机提供的含 50%A100 的机器上面运行的代码(非常感谢它们提供了这么好的机器)；             
    这里使用的一些库的版本：   
       1. scikit-learn: 1.5.1     
       2. rdkit: 2024.3.5         
       3. tqdm: 4.66.5        
       4. 查询得到的系统版本: Linux intern-studio-50065511 5.10.134-13.al8.x86_64 #1 SMP Mon Jan 9 10:50:49 CST 2023 x86_64 x86_64 x86_64 GNU/Linux