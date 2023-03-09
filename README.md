# count-pair
public:	
	
	int countPairs(vector<vector<int>> &mat1, vector<vector<int>> &mat2, int n, int x)
	{
	    // Your code goes here
	    int count=0;
	    unordered_map<int,int>mp;
	    for(int i=0;i<n;i++){
	        for(int j=0;j<n;j++){
	  mp[mat1[i][j]]++;
	}
	    }
	    for(int i=0;i<n;i++){
	        for(int j=0;j<n;j++){
	            if(mp.find(x-mat2[i][j])!=mp.end())
	            {
	                count++;
	                mp.erase(x-mat2[i][j]);
	            }
	        }
	    }
	return count;
	}	
};
