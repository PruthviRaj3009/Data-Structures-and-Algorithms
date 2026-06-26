class Solution {
public:
    int maxPoints(vector<vector<int>>& points) {
        int ans = 0;
        int n = points.size();
        if(n ==1) return 1;
        for (int i = 0; i < n; i++) {
            map<pair<int, int>, int> mpp;
            for (int j = i + 1; j < n; j++) {
                int dx = points[j][0] - points[i][0];
                int dy = points[j][1] - points[i][1];
                if (dx == 0) {
                    dy = 1;
                } else if (dy == 0) {
                    dx = 1;