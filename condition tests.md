public class SILab2Test {

    @Test
    public void testFunction_ValidUserCredentials() {
        // Test case for valid user credentials
        User user = new User("JohnDoe", "P@ssw0rd", "john.doe@example.com");
        List<User> allUsers = new ArrayList<>();
        
        // Assert that the function returns true for valid user credentials
        assertTrue(SILab2.function(user, allUsers));
    }

    @Test
    public void testFunction_NullUser() {
        // Test case for null user
        User user = null;
        List<User> allUsers = new ArrayList<>();
        
        // Assert that the function throws a RuntimeException for a null user
        try {
            SILab2.function(user, allUsers);
            fail("Expected RuntimeException for null user");
        } catch (RuntimeException e) {
            assertEquals("Mandatory information missing!", e.getMessage());
        }
    }
}
