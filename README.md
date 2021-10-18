# Sparse-Arrays
#c++ O(n^2)
vector<int> matchingStrings(vector<string> strings, vector<string> queries) {
    vector<int> ans;
    for (int i = 0; i < queries.size(); i++){
        int temp = 0;
        for (int j = 0; j < strings.size(); j++){
            if (queries[i]==strings[j]){
                temp += 1;
            }
        }
        ans.push_back(temp);
    }
    return ans;
}
#python O(n)
def matchingStrings(strings, queries):
    ans = []
    for i in queries:
        ans.append(strings.count(i))
    return ans
