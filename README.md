# leetcode-69-binary-3


二分法：

        class Solution(object):
            def mySqrt(self, x):
                """
                :type x: int
                :rtype: int
                """
                l = 1
                r = x
                while l <= r:
                    mid = (l+r)//2
                      # 以上都一样
                    if mid*mid > x:
                      # if pow(mid,2) > x:
                        r = mid - 1
                          # 根据要求写出来
                    elif mid*mid < x:
                        l = mid + 1
                    else:
                        return mid
                return r
                  # 反向取。根 至少要< 值，反而取 >, so 取 r
                
   
