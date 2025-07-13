import java.util.*;

class Solution {

    static void Method(String str) {
        HashMap<Character, Integer> countMap = new HashMap<>();
        for (int i = 0; i < str.length(); i++) {
            countMap.put(str.charAt(i), countMap.getOrDefault(str.charAt(i), 0) + 1);
        }
        char res = ' ';
        int index = -1;

        for (int i = 0; i < str.length(); i++) {
            char ch = str.charAt(i);
            if (countMap.get(ch) == 1) {
                res = ch;
                index = i;
                break;
            }
        }

        if (index != -1)
            System.out.println("{" + res + "," + index + "}");
        else
            System.out.println("No non-repeating");
    }

    public static void main(String[] args) {
        Method("ababac");
    }
}
