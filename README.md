import java.util.ArrayList;
import java.util.List;

public class BannerApp {

    public static void main(String[] args) {
        List<CharacterPatternMap> bannerData = new ArrayList<>();
        
        bannerData.add(new CharacterPatternMap('O', new String[]{
            "  *** ",
            " * * ",
            " * * ",
            " * * ",
            "  *** "
        }));
        
        bannerData.add(new CharacterPatternMap('P', new String[]{
            " ***** ",
            " * *",
            " ***** ",
            " * ",
            " * "
        }));
        
        bannerData.add(new CharacterPatternMap('S', new String[]{
            "  **** ",
            " * ",
            "  *** ",
            "     * ",
            " **** "
        }));

        displayBanner(bannerData);
    }

    public static void displayBanner(List<CharacterPatternMap> patterns) {
        if (patterns.isEmpty()) return;

        int height = patterns.get(0).getPattern().length;

        for (int i = 0; i < height; i++) {
            StringBuilder line = new StringBuilder();
            for (CharacterPatternMap cp : patterns) {
                line.append(cp.getPattern()[i]).append("  ");
            }
            System.out.println(line.toString());
        }
    }

    static class CharacterPatternMap {
        private char character;
        private String[] pattern;

        public CharacterPatternMap(char character, String[] pattern) {
            this.character = character;
            this.pattern = pattern;
        }

        public char getCharacter() {
            return character;
        }

        public String[] getPattern() {
            return pattern;
        }
    }
}
