# Multithread
class UserThread extends Thread {

    private TicketBooking booking;
    private String user;
    private int tickets;

    public UserThread(TicketBooking booking, String user, int tickets) {
        this.booking = booking;
        this.user = user;
        this.tickets = tickets;
    }

    @Override
    public void run() {
        booking.bookTicket(user, tickets);
    }
}
