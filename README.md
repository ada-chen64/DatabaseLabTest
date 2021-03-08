# dbtrain-lab-test

数据库专题训练测例，采用 googletest 测试框架。

## 使用方法

将本测试仓库与实验代码仓库放在同一文件夹下，在实验代码仓库的根目录下执行

```bash
mkdir build
cd build
cmake ..
make -j `nproc`
```

然后可以对实验进行测试，如要测试 lab1，运行

```bash
test/lab1_test
```

未完成实验时，若直接运行测试，可能会出现各种奇怪的报错，我们建议在运行测试前先将所有测试函数 disable，运行程序确保环境配置正确，实现了某个函数后，再打开对应的测试函数，检验函数实现是否正确。

如在 test/lab1/start_test.cc 文件中，将第5行改为：

```c++
TEST(Lab1, DISABLED_StartTest) {
```

即可在测试时跳过这个函数，需要打开测试时，将 DISABLED 前缀去掉即可。

目前的单元测试还比较简单，但只要你能通过所有单元测试，即可得到本次实验代码部分的所有分数。如果你对测试有更好的想法，欢迎在实验报告中提出。
