��UTF-8������

README:�����ϴ���ģ�飬processNewsĿ¼�£�

ANSJSEG.java��Ӧ��ANSJ_SEG���߽��зִʣ�������ͣ�ôʱ�
compute1000.java:ÿһ������ѡ��2000ƪ���ţ��ִʣ�ȥ�أ�����tf-idf���������ɴʱ�
computeTFIDF:���������������Ͽ�ִʣ�ȥ��֮��ʵ��TF-IDFֵ��������TF-IDFֵ���ʵ�˳������
extracArticle:���ѹ�ȫ�����Ű�������ȡ����
newSegmentation:�����Ž��зִʲ�����һϵ�д���
wordEmbedding:����ÿƪ���ŵĴ�����������ͳһ�����Ŵʵ��£�������������ʾͱ�1��û�оͱ�0��one-hot



README:��SVMģ�飬svmĿ¼�£�

svm_train,java:֧��������ѵ��ģ���㷨
���룺1.SVMѵ��ģ���õ������ļ�·�� 2. ���ģ��·��
�����ѵ������ģ�ͱ����ڲ���2������·���У�

svm_predict.java:֧��������Ԥ���㷨
���룺1.�������������������ļ�·�� 2.ѵ���õ���ģ��·�� 3. ���ɽ��·��
��������Խ�������ڲ���3������·���У�

test_convert.java�����ݸ�ʽ���㷨
������ķִ��ļ����д���ʹ���svm_trainʶ������ݸ�ʽ��



README:��Bayesģ�飬naiveBayesianĿ¼�£�

NaiveBayesianClassifierTrain����Ҷ˹ѵ��ģ���㷨
���ݱ������ļ�·���еķִ�ѵ���ļ�����ѵ������ѵ��������������·����

NaiveBayesianTest����Ҷ˹�����㷨

���룺��Ҫѵ���ķִ��ļ�·��
��������Խ��




README:����ҳ�����뽻������ģ�飩

��������������Ҫ��classification�࣬rule�ࡢJspider �࣬TextUtil�࣬Result�࣬��Text��

classification��:
private void initialize()�������ʼ��
public void geneFile(String url, String path)����ȡ��ҳ���ݣ����ִʣ����ִʴ����ı�
private ActionListener a1������URL�Ļ�ȡ��ʽ
private ActionListener a3��ѡ�񱣴�·��������geneFile������������ִ��ı���

rule��:����Ĺ���

TextUtil�ࣺ
public static boolean validateUrl(String url)����֤URL�Ƿ�Ϊ��ȷ��URL��ʽ��

Jspider �ࣺ
public static List<Result> soup(Rule rule)�����rule�е�url��ַ������ʽ���������ӣ�ץȡ��ҳ���ݣ����ؽ������
Result�ࣺ��������

ext�ࣺ�ı��Ĳ�����
public void caveFile(String textPath,String content)����content������·��ΪtextPath���ı���
public List<String> readFile(String path)����ȡ·��ΪtextPath���ı���������list����
public List<String>readFile(String path,List<String>urls)�����ж�ȡURL�ı���������urls�����С�
