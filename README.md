# MCA
[week1](week1.md)
[week2](week1.md)
[week3](week3.md)
[week4](week4.md)

import java.util.LinkedList;
import java.util.Queue;

enum BinarySemaphoreValue {
    ZERO, ONE
}

class BinarySemaphore {
    BinarySemaphoreValue value;
    Queue<Process> queue;

    public BinarySemaphore() {
        this.value = BinarySemaphoreValue.ONE;
        this.queue = new LinkedList<>();
    }

    public void waitBinarySemaphore() {
        if (this.value == BinarySemaphoreValue.ONE) {
            this.value = BinarySemaphoreValue.ZERO;
        } else {
            // Помістити процес в чергу
            // Заблокувати процес (псевдокод, фактичний механізм блокування залежить від контексту)
        }
    }

    public void signalBinarySemaphore() {
        if (isQueueEmpty()) {
            this.value = BinarySemaphoreValue.ONE;
        } else {
            // Видалити процес з черги
            // Помістити процес в список активних (псевдокод)
        }
    }

    private boolean isQueueEmpty() {
        return this.queue.isEmpty();
    }

    // Клас, що представляє процес (замініть його вашим фактичним класом Process)
    private static class Process {
        // Деталі процесу
    }
}

public class Main {
    public static void main(String[] args) {
        // Приклад використання BinarySemaphore
        BinarySemaphore binarySemaphore = new BinarySemaphore();

        // Процес 1
        binarySemaphore.waitBinarySemaphore();
        // Критична секція для Процесу 1
        binarySemaphore.signalBinarySemaphore();

        // Процес 2
        binarySemaphore.waitBinarySemaphore();
        // Критична секція для Процесу 2
        binarySemaphore.signalBinarySemaphore();
    }
}
