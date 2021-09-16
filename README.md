# Max-difference-of-0-and-1-binary-string

class Solution{
public:	
	int maxSubstring(string S)
	{
	    int ans = 0;
int m = 0;
for (int i = 0; i < S.size(); i++)
{
if (S[i] == '0')
{
m++;
ans = max(ans, m);
}
else
{
if (m > 0)
m--;
}
}
return ans == 0 ? -1 : ans;
	}
};
