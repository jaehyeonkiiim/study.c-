#구조체 정리
**구조체를 정리해보자^^

##구조체란?
	성격이 같지만 타입이 다른 데이터의 모임.
##구조체 선언 방법
	struct example{
   		data_type member1;
		data_type member2;
		data_type member3;
	};
	(끝에 변수를 붙여 변수선언을 동시에 할 수 있다.)
##구조체 초기화
	struct example{
   		data_type member1;
		data_type member2;
		data_type member3;
	};

	struct example e = {"abc", 123, "hi"}
	struct example e1 = {"qwe", 456, "hungry"}
	(마지막에 구조체 선언을 생략하고 동시에 초기화 선언을 할 수도 있다.)
##구조체를 가리키는 포인터
	struct employee{
		char job[10];
		char company[20];
		struct person *p;
	};
	struct person ps {"toby", 22 "gwangju"};
	struct employee e = {"student", "jbnu"};
	
	e.p = &ps; 
	
	구조체는 다른 구조체를 멤버로 가져올 수 있고 다른 구조체의 포인터도 가져올 수 있다.
##구조체와 함수
	?구조체는 함수의 인수로도 사용이 가능하고 함수에서 반환값으로 반환될 수 도 있다.
	?구조체를 함수의 인수로 전달하는 경우
	int equal(struct student s1, struct student s2)
	{
		if( strcmp(s1.name, s2.name) == 0 )
		return 1;
		else
		return 0;
	}
	?구조체의 포인터를 함수의 인수로 전달하는 경우
	int equal(struct student const *p1, struct student const *p2)
	{
		if( strcmp(p1->name, p2->name) == 0 )
		return 1;
		else
		return 0;
	}
	?구조체도 함수의 반환값으로 넘길 수 있다.
	struct student make_student(void)
	{
		struct student s;
		printf("나이:“);
		scanf("%d", &s.age);
		printf("이름:“);
		scanf("%s", s.name);
		printf("키:“);
		scanf("%f", &s.grade);
		return s;
	}
	

	
