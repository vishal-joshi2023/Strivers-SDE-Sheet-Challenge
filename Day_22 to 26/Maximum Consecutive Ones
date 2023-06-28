int longestSubSeg(vector<int> &arr , int n, int k){
    int i = 0, j = 0;
    int maxi = 0;
    int flip = 0;

    while(j < n){
        if(arr[j] == 0){
            flip++;
        }

        while(flip > k){
            if(arr[i] == 0){
                flip--;
            }
            i++;
        }
        maxi = max(maxi, j - i + 1);
        j++;
    }
    return maxi;
}
