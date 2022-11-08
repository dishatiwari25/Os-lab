#include<bits/stdc++.h>
using namespace std;

int pageFaults(int pages[], int n, int memcapacity)
{

	unordered_set<int> s;

	
	queue<int> indexes;


	int page_faults = 0;
	for (int i=0; i<n; i++)
	{

	if (s.size() < memcapacity)
	{
	    if (s.find(pages[i])==s.end())
			{
	s.insert(pages[i]);

		page_faults++;
	indexes.push(pages[i]);
			}
		}
		else
		{
			
			if (s.find(pages[i]) == s.end())
			{
				int val = indexes.front();
				
				
				indexes.pop();
				s.erase(val);
				s.insert(pages[i]);
				indexes.push(pages[i]);
			
				page_faults++;
			}
		}
	}

	return page_faults;
}
int main()
{
	int pages[] = {7, 0, 1, 2, 0, 3, 0, 4, 2, 3, 0, 3, 2};
	int n = 13;
	int memcapacity = 4;
	cout << pageFaults(pages, n, memcapacity);
	return 0;
}
