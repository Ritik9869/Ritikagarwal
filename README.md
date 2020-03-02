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
