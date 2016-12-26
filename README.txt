“UTF-8”编码

README:（语料处理模块，processNews目录下）

ANSJSEG.java：应用ANSJ_SEG工具进行分词，并过滤停用词表
compute1000.java:每一类新闻选择2000篇新闻，分词，去重，计算tf-idf并排序，生成词表
computeTFIDF:计算所有新闻语料库分词，去重之后词典的TF-IDF值，并按照TF-IDF值将词典顺序重排
extracArticle:将搜狗全网新闻按照类别抽取解析
newSegmentation:对新闻进行分词并进行一系列处理
wordEmbedding:生成每篇新闻的词向量，正在统一的重排词典下，该新闻有这个词就标1，没有就标0，one-hot



README:（SVM模块，svm目录下）

svm_train,java:支持向量机训练模型算法
输入：1.SVM训练模型用的数据文件路径 2. 输出模型路径
输出：训练所得模型保存在参数2给出的路径中；

svm_predict.java:支持向量机预测算法
输入：1.测试组特征向量数据文件路径 2.训练得到的模型路径 3. 生成结果路径
输出：测试结果保存在参数3给出的路径中；

test_convert.java：数据格式化算法
对输入的分词文件进行处理，使变成svm_train识别的数据格式；



README:（Bayes模块，naiveBayesian目录下）

NaiveBayesianClassifierTrain：贝叶斯训练模型算法
依据保存在文件路径中的分词训练文件进行训练，将训练结果保存在输出路径中

NaiveBayesianTest：贝叶斯测试算法

输入：需要训练的分词文件路径
输出：测试结果




README:（网页爬虫与交互界面模块）

界面爬车部分主要有classification类，rule类、Jspider 类，TextUtil类，Result类，和Text类

classification类:
private void initialize()：界面初始化
public void geneFile(String url, String path)：爬取网页内容，并分词，将分词存入文本
private ActionListener a1：处理URL的获取形式
private ActionListener a3：选择保存路径，调用geneFile（）方法保存分词文本。

rule类:爬虫的规则集

TextUtil类：
public static boolean validateUrl(String url)：验证URL是否为正确的URL形式。

Jspider 类：
public static List<Result> soup(Rule rule)：获得rule中的url地址和请求方式，建立连接，抓取网页内容，返回结果集。
Result类：爬虫结果集

ext类：文本的操作类
public void caveFile(String textPath,String content)：将content保存在路径为textPath的文本中
public List<String> readFile(String path)：读取路径为textPath的文本，并返回list链表。
public List<String>readFile(String path,List<String>urls)：逐行读取URL文本，并返回urls链表中。
