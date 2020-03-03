To understand the basic use of array and reducing bhut hdd tk time complexity
u must learn this concept. divisiblity factor of 2,3 and 5;
7
1 5 7 5 6 7 5
5
1 2
2 3
4 6
1 7
3 6
FastReader fr = new FastReader();
		int size = fr.nextInt();
		int arr[] = new int[size];
		int sum = 0;
		for (int i = 0; i < size; ++i) {
			arr[i] = fr.nextInt();
			sum = sum + arr[i];
		}
		int temp[] = new int[size];
		for (int i = 0; i < size; ++i) {
			int left = (i == 0) ? 0 : arr[i - 1];
			int right = (i == size - 1 || size == 1) ? 0 : arr[size - 1];
			temp[i] = ((sum - arr[i]) % 3 == 0 && ((left + right) % 10 == 0)) ? 1 : 0;
		}
		for (int i = 1; i < size; ++i) {
			temp[i] = temp[i] + temp[i - 1];
		}
		int Q = fr.nextInt();
		while (Q-- > 0) {
			String t[] = fr.nextLine().split(" ");
			int l, r;
			l = Integer.valueOf(t[0]);
			r = Integer.valueOf(t[1]);
			--l;
			--r;
			int left = (l == 0) ? 0 : temp[l - 1];
			System.out.println(temp[r] - left);
2.



https://www.hackerearth.com/practice/data-structures/arrays/1-d/practice-problems/algorithm/monk-and-lucky-minimum-3/


for finding the frequency of min  number we have not needed to sort the array everytime we have to just iterate over the elements and set min =1 whenever the minimum number come as compared to previous number.
must learn the concepts



Reader sc = new Reader();
	   	int t = sc.nextInt();
	   	while(t-- >0)
	   	{
	   		int n = sc.nextInt();
	   		int a[] = new int[n];
	   		int min = Integer.MAX_VALUE,count=0;
	   		for(int i=0;i<n;i++)
	   		{
	   			int value = sc.nextInt();
	   			if(value<min)
	   			{
	   				min = value;
	   				count = 1;
	   			}
	   			if(value==min)
	   				count++;
	   		}
	   		if(count%2!=0)
	   			System.out.println("Unlucky");
	   		else
	   			System.out.println("Lucky");
 
	   	}



