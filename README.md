# Test
Just for test
Somthing Changed
‘’‘
class Solution:
    def isMatch(self, s, p):
        """
        :type s: str
        :type p: str
        :rtype: bool
        """
        #a = re.compile(p)
        #result = a.match(s)
        result = re.match('^'+p+'$', s)
        if result == None:
            return False
        else:
            return True
        #if re.compile('^'+p+'$').match(s):
            #return True
        #return False
 ’‘’
