Ӧ�ó���Api��־����
���
ʹ�� Intel ���⻯����ʵ��Ӧ�ò�HOOK
1.�ų�Dll�亯������
2.��̬���ü��Api


���� 
���Api���ã�
		�������ļ�Kas.config�����ϵͳdll·���ʹ�dll��Ӧ�ĺ��������ļ�(һ��dll��Ӧһ�����������ļ�)
	  	����:
	  		DllName: C:\Windows\System32\Kernel32.dll HookApiFileName: Kernel32.Apiconfig  
				Kernel32.Apiconfig �ŵ�configĿ¼��.
				Kernel32.Apiconfig ���ļ���������������
		Api����
			������������ 
			 ��������: 
			 		INT32, INT64 
			 ָ�����ͣ�
			 	PCHAR
			 	PWCHAR
				ָ�� : ������(Buffer, Length)   : PVOID , ParamterIndex  	//��ParameterIndex��������Buffer�ĳ��� ��Ŵ�1��ʼ
  	 	  ָ�� ����������(PCHAR/PWCHAR)   : PCHAR,PWCHAR....
  		  ָ�� + �̶�����(PLONG)          : PINT + N								//N (N/8)Bytes
			 ���� ��
			 	_Success_(return != 0)
				INT32
				WINAPI
				WriteFile(
				    _In_ ULONG_PTR hFile,
				    _In_reads_bytes_opt_(3) PVOID lpBuffer,
				    _In_ INT32 nNumberOfBytesToWrite,
				    _Out_opt_ PINT+32 lpNumberOfBytesWritten,
				    _Inout_opt_ ULONG_PTR lpOverlapped
				    );
				    
���������ֶ�����
	��KasApiType.config �������ļ������̡����硢ע�����Ӻ��б���\r\n���С�