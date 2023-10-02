import java.util.Random;

class Personagem {
    public void comer() {
        System.out.println("Personagem está comendo.");
    }

    public void caca() {
        System.out.println("Personagem está caçando.");
    }

    public void dormir() {
        System.out.println("Personagem está dormindo.");
    }
}

public class Jogo {
    public static void main(String[] args) {
        Personagem p1 = new Personagem();
        Personagem p2 = new Personagem();
        Random rand = new Random();

        for (int i = 0; i < 10; i++) {
            // Escolha aleatória do que cada personagem fará
            int acaoP1 = rand.nextInt(3); // 0 para comer, 1 para caçar, 2 para dormir
            int acaoP2 = rand.nextInt(3);

            // Executar a ação escolhida para o Personagem 1
            if (acaoP1 == 0) {
                p1.comer();
            } else if (acaoP1 == 1) {
                p1.caca();
            } else {
                p1.dormir();
            }

            // Executar a ação escolhida para o Personagem 2
            if (acaoP2 == 0) {
                p2.comer();
            } else if (acaoP2 == 1) {
                p2.caca();
            } else {
                p2.dormir();
            }
        }
    }
}
