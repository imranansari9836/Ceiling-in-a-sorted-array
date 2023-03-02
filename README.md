public class CeilingNumber {

    public static int searchCeiling(int[] nums, int target) {
        int i = 0, j = nums.length - 1;

        while (i <= j) {
            int mid = i + (j - i) / 2;

            if (nums[mid] >= target) {
                if (mid == 0) {
                    return mid;
                } else if (nums[mid - 1] < target) {
                    return mid;
                }
                j = mid - 1;
            } else {
                i = mid + 1;
            }
        }
        return -1;
    }
}
