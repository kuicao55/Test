# Test
## TEST
'int num'

Just for test
Somthing Changed
class Solution:
    def romanToInt(self, s):
        """
        :type s: str
        :rtype: int
        """
        result = 0
        i = 0
        while i < len(s):
            if s[i] == 'I':
                if i+1 <= len(s)-1:
                    if s[i+1] == 'V':
                        result = result + 4
                        i = i+2
                    elif s[i+1] == 'X':
                        result = result + 9
                        i = i+2
                    else:
                        result = result = result + 1
                        i = i+1
                else:
                    result = result + 1
                    i = i + 1
            elif s[i] == 'V':
                result = result + 5
                i = i+1
            elif s[i] == 'X':
                if i+1 <= len(s)-1:
                    if s[i+1] == 'L':
                        result = result + 40
                        i = i+2
                    elif s[i+1] == 'C':
                        result = result + 90
                        i = i+2
                    else:
                        result = result = result + 10
                        i = i+1
                else:
                    result = result + 10
                    i = i+1
            elif s[i] == 'L':
                result = result + 50
                i = i+1
            elif s[i] == 'C':
                if i+1 <= len(s)-1:
                    if s[i+1] == 'D':
                        result = result + 400
                        i = i+2
                    elif s[i+1] == 'M':
                        result = result + 900
                        i = i+2
                    else:
                        result = result = result + 100
                        i = i+1
                else:
                    result = result + 100
                    i = i+1
            elif s[i] == 'D':
                result = result + 500
                i = i+1
            elif s[i] == 'M':
                result = result + 1000
                i = i+1
        return (result)
