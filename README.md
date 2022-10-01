# LeetCode-27.-Remove-Element

class Solution(object):
    def removeElement(self, nums, val):
        c = []
		#Empty list to store the indexes
        for i in range(len(nums)):
            if val == nums[i]:
				#Append the index to the list if the element is not val
                c.append(i)
		#reverse the created list to remove elements from back of nums list
        c.reverse()
        for i in c:
			#pop the elements out of orginal array
            nums.pop(i)
        return len(nums)
