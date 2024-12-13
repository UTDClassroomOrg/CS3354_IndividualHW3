a. k - the number of elements to average, starting at 0; list - the list of integers to average; returns the average of the first n numbers, where n is the lesser of k, and the number of elements in the list or zero if k is negative

b. public void test_1() {
  Average test_average = new Average();
  int nums[] = {2, 3, 8};
  assertEquals((2+3+8)/3.0, test_average.average(nums.length, nums), 0.001);
}

c. 0, k - 1
public void test_2() {
  Average test_average = new Average();
  int nums[] = {2, 3, 8};
  assertEquals(0, test_average.average(-1, nums), 0.001);
}

d. public void test_3() {
  Average test_average = new Average();
  int nums[] = {2, 3, 8};
  assertEquals(0, test_average.average(0, nums), 0.001);
}

e. public double average(int k, int[] list){
  double average = 0;
  int n = Math.min(k, list.length);
  if(n > 0) {
    for(int i = 0 ; i < n; i++){
      average += list[i];
    }
    average = average/n;
  }
  return average;
}

f. Average returns an int creating loss of information with integer division; solved by returning a double instead

g. 100% using EclEmma
