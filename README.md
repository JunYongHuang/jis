StarlingSwf��չUI���
===

����չ�ǽ�����StarlingSwf�Ļ���֮�Ͻ��б�д���ܹ�ʹ����Starling�п���UI��ɼ򵥲��Ҹ�Ч���ܹ������ע����ȫ�������ڳ����߼�����.

����Ч�ʺܸߣ���Ը��ӵ�UIҲ������ʵ��

####�̵̳�ַ��http://bbs.9ria.com/thread-275219-1-1.html
####StarlingSwf��ַ��https://github.com/zmLiu/StarlingFeathers
####Swfת�����ߵ�ַ��https://github.com/zmLiu/StarlingSWF
####API��ַ��http://jiessie-git.github.io/jis_blog/

�������
================

1.JISButton
-------------------
	��ͨ��ť����װ��SwfMovieClip����Ҫ��fla�е���Ϊ��mcXXX��
	��Ӧ֡��
		��һ֡Ϊ��ͨ״̬
		�ڶ�֡Ϊ����״̬
		����֡Ϊ����״̬
		����֡Ϊѡ��״̬����JISButtonGroup���ʹ�ÿ��Ե�����ѡ��ťʹ��
		����֡Ϊ������״̬
	��ť���»��׳�JISButton.BOTTON_CLICK�¼����¼�����Ϊstarling��Event

2.JISButtonGroup
-------------------
	��ť���Ϲ��������ڳ�ʼ����ʱ����JISButton�ļ��ϣ�Ҳ���Ե������ʹ��
	���ʹ�÷�ʽ��
		public var _Btn:JISButtonGroup;
		��Ӧ��fla��_Btn�ĵ���������Ϊsprite�����Զ���sprite�е�����SwfMovieClipʹ��JISButton���й���
	������ʽ��
		_Btn.setSelectBtnHandler(handler);
		//handler��Ҫ�߱�һ�����������õ�ʱ��ᴫ�뵱ǰѡ�е�JISButton
		_Btn.addEventListener(JISButtonGroup.CLICK_BTN,handler);
		//ͨ������_Btn.getCurrentSelectBtn()�ķ�ʽ��õ�ǰѡ����
3.JISCharQuadBatch
-------------------
	�������ֱ���࣬���������������ƴ��һ����ͼƬ��ɵ�sprite�Ļ��������ʹ�ø���
	ʹ�ù���swf�д������µ���ͼƬ��
	img_num_1��img_num_2��img_num_3��img_num_4��img_num_-��img_num_+��ʼ����ʱ�����Ҫ���롰img_num_�� 
	Ȼ��ͨ��setChar("+333")�Ϳ�����ʾimg_num_+��img_num_3��img_num_3��img_num_3�⼸��ͼƬƴװ����ʾ����
	������Ϸ�еľ���ֵ����Ϊ��100/522���֣���ֻ��Ҫ�����ַ�����100/522�����ɡ�
	������õı���չ���ص�swf�Ļ������Ե��ü������getSourceSwf()���Swf����
4.JISCuttingButtonGroup
--------------------
	����ָ��һ��Sprite�о�����ͬ����������SwfMovieClip����JISButton���й������캯�����Դ���JISButton�Լ�������
5.JISDisplayCutting
--------------------
	����ָ��һ��Sprite�о�����ͬ������������ʾ������JISUIManager�������������й���
6.JISIconManager
--------------------
	ͼ������࣬�ڲ���װ��JISImageSprite�����Խ�����ָ��һ���յ�Sprite
	ͨ��setImageSource()�ķ�ʽ����һ��ͼƬ��url����File
	setIconWH����ǿ��ָ��ͼƬ�Ĵ�С
	����߱�һ�����ֶ�����������Sprite����һ������Ϊ_MaskImage��Display�Ļ�����ʵ�����ֹ���
7.JISScrollTable
--------------------
	������table���̳���ScrollContainer������ͨ��getTable()����ڲ���table���󲢶�����в�������
	����˵����
		���򻬶�������ڲ�table��widthС�ڵ���JISScrollTable��width�Ļ��������Խ������򻬶�������ͨ��getTable().setPreferredWidth�ķ�ʽǿ������table�Ŀ��
		���򻬶����ڲ���table��heightС�ڵ���JISScrollTable��height�Ļ��������Խ��к��򻬶�������ͨ��getTable().setPreferredHeight�ķ�ʽǿ������table�ĸ߶�
	��ʾ���룺
		//���򻬶�
		table = new JISScrollTable();
		table.getTable().setPreferredWidth(300);
		table.width = 300;
		table.height = 445;
8.JISTable
--------------------
	����ǿ��ı�񣬿������Ϊlist��֧�ֺ������򲼾�
	���ܵ�ǿ�����ڿ�������һ��ʵ����ITabbedCell�ӿڵ�Class��Ȼ�����ͨ������һ��data�ķ�ʽ�Զ�����Class����ӵ���ʾ�б��У�Ҳ������������data������ο�addCellData��setCellDatas��removeForCellData
	��ѡ��table�е����ݵ�ʱ��table���׳�JISTable.TABBED_SELECTED�¼���ͨ��getSelected()�ķ�ʽ���Ի�õ�ǰѡ��
9.JISUIMultipleProgressManager
--------------------
	�ܶ���Ϸ��BOSS���Ǻܶ��Ѫ����BOSS��Ѫ��һ��һ�ܵĵݼ����������ʵ�����ֽ����������
	��������Sprite�е���ʾ�����������JISUIProgressManager�Ĺ���Ҳ����˵Sprite����ʵ��N��Ľ�����
	ʹ�÷�����
		ͨ��setMaxProgressNum(max,oneProgress)�����е�һ������Ϊ���ֵ���ڶ���������ÿһ��������ռ�ķݶ��������(max/oneProgress�ķ�ʽ�����ܹ���Ҫ���ٸ�������
		ͨ��setProgressNum���õ�ǰ���ȣ����ȵݼ�������ʹ�õ�starling�Ļ�������п���
10.JISUIProgressManager
--------------------
	�������������������Խ�������һ��display���а󶨣�Ҳ���Խ�Sprite�е�һ�����ֽ���_Center����ʾ�����
	ʹ�÷�����setProgress(��ǰ�����)
	Ҫ��������ʱ��_Center����display������100%��������״̬
11.	JISUIWindow
--------------------
	�����࣬����ʹ�ø������swf��Դ����ָ�����ڵ�������������
12.JISUIWindowManager
--------------------
	���ڹ����࣬ͨ������2������ʹ�ã�����ͨ��JISUIManager����ʽһ��