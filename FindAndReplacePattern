// https://leetcode.com/problems/find-and-replace-pattern/solution/
// medium:890
public class Solution {
    public IList<string> FindAndReplacePattern(string[] words, string pattern) {
         List<string> result = new List<string>();
        
        for(int i=0; i < words.Length; i++) {
            Dictionary<char, char> map1 = new Dictionary<char, char>();
            Dictionary<char, char> map2 = new Dictionary<char, char>();
            
            for(int j=0; j<=pattern.Length; j++) {
                if (j == pattern.Length) {
                    result.Add(words[i]);
                    break;
                }
                
                if (map1.ContainsKey(pattern[j])) {
                    if (map1[pattern[j]] != words[i][j]) {
                        break;
                    }
                } else if (map2.ContainsKey(words[i][j])) {
                    break;
                } 
                else {
                    map1.Add(pattern[j], words[i][j]);
                    map2.Add(words[i][j], pattern[j]);
                }
            }
        }
        
        return result;
    }
}
