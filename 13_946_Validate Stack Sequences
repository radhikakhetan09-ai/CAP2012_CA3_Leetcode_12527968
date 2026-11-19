class Solution {
public:
    bool validateStackSequences(vector<int>& pushed, vector<int>& popped) {
        stack<int> st;
        int popIndex = 0;

        for (int value : pushed) {
            st.push(value);

            while (!st.empty() &&
                   popIndex < static_cast<int>(popped.size()) &&
                   st.top() == popped[popIndex]) {
                st.pop();
                popIndex++;
            }
        }

        return st.empty();
    }
};
