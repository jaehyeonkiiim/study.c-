#����ü ����
**����ü�� �����غ���^^

##����ü��?
	������ ������ Ÿ���� �ٸ� �������� ����.
##����ü ���� ���
	struct example{
   		data_type member1;
		data_type member2;
		data_type member3;
	};
	(���� ������ �ٿ� ���������� ���ÿ� �� �� �ִ�.)
##����ü �ʱ�ȭ
	struct example{
   		data_type member1;
		data_type member2;
		data_type member3;
	};

	struct example e = {"abc", 123, "hi"}
	struct example e1 = {"qwe", 456, "hungry"}
	(�������� ����ü ������ �����ϰ� ���ÿ� �ʱ�ȭ ������ �� ���� �ִ�.)
##����ü�� ����Ű�� ������
	struct employee{
		char job[10];
		char company[20];
		struct person *p;
	};
	struct person ps {"toby", 22 "gwangju"};
	struct employee e = {"student", "jbnu"};
	
	e.p = &ps; 
	
	����ü�� �ٸ� ����ü�� ����� ������ �� �ְ� �ٸ� ����ü�� �����͵� ������ �� �ִ�.
##����ü�� �Լ�
	?����ü�� �Լ��� �μ��ε� ����� �����ϰ� �Լ����� ��ȯ������ ��ȯ�� �� �� �ִ�.
	?����ü�� �Լ��� �μ��� �����ϴ� ���
	int equal(struct student s1, struct student s2)
	{
		if( strcmp(s1.name, s2.name) == 0 )
		return 1;
		else
		return 0;
	}
	?����ü�� �����͸� �Լ��� �μ��� �����ϴ� ���
	int equal(struct student const *p1, struct student const *p2)
	{
		if( strcmp(p1->name, p2->name) == 0 )
		return 1;
		else
		return 0;
	}
	?����ü�� �Լ��� ��ȯ������ �ѱ� �� �ִ�.
	struct student make_student(void)
	{
		struct student s;
		printf("����:��);
		scanf("%d", &s.age);
		printf("�̸�:��);
		scanf("%s", s.name);
		printf("Ű:��);
		scanf("%f", &s.grade);
		return s;
	}
	

	
