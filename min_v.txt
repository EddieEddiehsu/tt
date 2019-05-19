#include <iostream>
#include <vector>
using namespace std;
int min(vector<vector<int>> mi)
{
	int min = mi[0][0];
	for (int i = 0; i < 4; i++)
	{
		for (int j = 0; j < 3; j++)
		{
			if (mi[i][j] < min)
				min = mi[i][j];
		}
	}
	return min;
}
int main()
{
	vector<vector<int>> m(4);
	for (int i = 0; i < 4; i++)
		m[i] = vector<int>(3);
	for (int i = 0; i < 4; i++)
	{
		for (int j = 0; j < 3; j++)
		{
			cin >> m[i][j];
		}
	}
	cout << "min: " << min(m) << endl;
	system("pause");
	return 0;
}