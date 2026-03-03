public class BannerApp {

    public static void main(String[] args) {
        String[][] banner = {
            getPatternO(),
            getPatternP(),
            getPatternS()
        };

        renderBanner(banner);
    }

    public static String[] getPatternO() {
        return new String[] {
            "  *** ",
            " * * ",
            " * * ",
            " * * ",
            "  *** "
        };
    }

    public static String[] getPatternP() {
        return new String[] {
            " ***** ",
            " * *",
            " ***** ",
            " * ",
            " * "
        };
    }

    public static String[] getPatternS() {
        return new String[] {
            "  **** ",
            " * ",
            "  *** ",
            "     * ",
            " **** "
        };
    }

    public static void renderBanner(String[][] letters) {
        int height = letters[0].length;
        for (int i = 0; i < height; i++) {
            for (String[] letter : letters) {
                System.out.print(letter[i] + "  ");
            }
            System.out.println();
        }
    }
}
