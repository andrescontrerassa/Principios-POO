public class PaymentProcessor {
    private double amount;
    private String paymentMethod;

    public PaymentProcessor(double amount, String paymentMethod) {
        this.amount = amount;
        this.paymentMethod = paymentMethod;
    }

    public void processPayment() {
        if (paymentMethod.equals("credit_card")) {
            processCreditCard();
        } else if (paymentMethod.equals("paypal")) {
            processPayPal();
        }
    }

    private void processCreditCard() {
        // Lógica para procesar un pago con tarjeta de crédito
        System.out.println("Processing credit card payment of $" + amount);
    }

    private void processPayPal() {
        // Lógica para procesar un pago con PayPal
        System.out.println("Processing PayPal payment of $" + amount);
    }
}
