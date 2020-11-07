# climbingLeaderboard
Climbing_Leaderboard_vol1
How to sort elements in vector?

Sorting in ascending order:

#include <algorithm>

vector<int>a;

sort(a.begin(),a.begin()+a.size());

sort(a.begin(),a.end());

Sorting in descending order:

reverse(a.begin(),a.end());

sort(a.rbegin(),a.rend());

How to erase repeated elements in vector:

First solution:

vector<int>a;
int i=1;
vector<int>::iterator it;
it=ranked.begin();
int p = a.size();
while (i < p)
{
    if(a[i-1] == a[i])
        {
        a.erase(it+i);
        p = a.size();
        }
    else {i++;}
}

Second solution:


vector<int>a;
unique(a.begin(),a.end());

using unique in vector are empty places and we have to use 'resize':

vector<int>a;
vector<int>::iterator it;
it=unique(a.begin(),a.end());
a.resize(distance(a.begin(),it));

Stateless Binary Search to speed up my solution - I had a great problem with time limit:

vector<int>a;
vector<int>b;
int j=p.size()-1;
while (j>=0)
{
    auto x = lower_bound(begin(a),end(a),p[j],greater<>{});
    int z = (distance(begin(a),x)+1);
    result.push_back(z);
    j--;
}

