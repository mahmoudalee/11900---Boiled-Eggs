# 11900---Boiled-Eggs

#include <iostream>

#include <algorithm>

using namespace std;

int arr[30];

int main()
{

	int t;
	cin >> t;
	for (int i = 0; i < t; i++)
	{
		int n, p, q, cnt = 0, tempQ = 0, tempEgg = 0;
		cin >> n >> p >> q;
		for (int j = 0; j < n; j++)
		{
			cin >> arr[j];
		}
		sort(arr, arr + n);
		int s = 0;
		while (tempQ < q && tempEgg != p && s < n)
		{
			cnt++;
			tempQ += arr[s]; s++;
			tempEgg++;
			if (tempQ > q)
			{
				cnt--;
				break;
			}
		}
		cout << "Case " << i + 1 << ": " << cnt << endl;
	}

	return 0;
}
