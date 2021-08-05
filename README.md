#include <iostream>
#include <string>
#include <algorithm>
using namespace std;
int main()
{
	int t;
	cin >> t;
	while (t--)
	{
		int n;
		cin >> n;
		bool v = true;
		int a[n];

		for (int i = 0; i < n; i++)
		{
			cin >> a[i];
		}

		if (a[0] == 1 && n % 2 != 0)
		{
			for (int i = 0; i < n; i++)
			{
				if (i < n / 2)
				{
					if (a[i] - a[i + 1] != -1)
					{
						v = false;
						break;
					}
				}

				else if (i >= n / 2 && i < n - 1)
				{
					if (a[i] - a[i + 1] != 1)
					{
						v = false;
						break;
					}
				}
			}

			if (v)
				cout << "yes" << endl;
			else
				cout << "no" << endl;
		}
		else
		{
			cout << "no" << endl;
		}
	}
	return 0;
	}
