import java.util.*;
import java.time.LocalDateTime;

// Abstract base class for all disasters
abstract class Disaster {
    protected String disasterId;
    protected String type;
    protected String location;
    protected LocalDateTime timestamp;
    protected int severity; // 1-10 scale
    protected String description;

    public Disaster(String disasterId, String type, String location, int severity, String description) {
        this.disasterId = disasterId;
        this.type = type;
        this.location = location;
        this.timestamp = LocalDateTime.now();
        this.severity = severity;
        this.description = description;
    }

    // Abstract method - must be implemented by subclasses
    public abstract String getAlertMessage();

    // Getters
    public String getDisasterId() { return disasterId; }
    public String getType() { return type; }
    public String getLocation() { return location; }
    public LocalDateTime getTimestamp() { return timestamp; }
    public int getSeverity() { return severity; }
    public String getDescription() { return description; }

    @Override
    public String toString() {
        return String.format("Disaster ID: %s | Type: %s | Location: %s | Severity: %d/10 | Time: %s",
                disasterId, type, location, severity, timestamp);
    }
}

// Concrete disaster classes
class Earthquake extends Disaster {
    private double magnitude;
    private double depth;

    public Earthquake(String disasterId, String location, int severity, double magnitude, double depth, String description) {
        super(disasterId, "Earthquake", location, severity, description);
        this.magnitude = magnitude;
        this.depth = depth;
    }

    @Override
    public String getAlertMessage() {
        String level = (magnitude >= 7.0) ? "MAJOR" : (magnitude >= 5.0) ? "MODERATE" : "MINOR";
        return String.format("🚨 EARTHQUAKE ALERT! Magnitude: %.1f, Depth: %.1fkm, Location: %s. %s - %s",
                magnitude, depth, location, level, description);
    }

    public double getMagnitude() { return magnitude; }
    public double getDepth() { return depth; }
}

class Flood extends Disaster {
    private double waterLevel;
    private String affectedAreas;

    public Flood(String disasterId, String location, int severity, double waterLevel, String affectedAreas, String description) {
        super(disasterId, "Flood", location, severity, description);
        this.waterLevel = waterLevel;
        this.affectedAreas = affectedAreas;
    }

    @Override
    public String getAlertMessage() {
        return String.format("🌊 FLOOD ALERT! Water Level: %.2fm, Location: %s. Affected Areas: %s - %s",
                waterLevel, location, affectedAreas, description);
    }

    public double getWaterLevel() { return waterLevel; }
    public String getAffectedAreas() { return affectedAreas; }
}

class Hurricane extends Disaster {
    private double windSpeed;
    private String category;

    public Hurricane(String disasterId, String location, int severity, double windSpeed, String category, String description) {
        super(disasterId, "Hurricane", location, severity, description);
        this.windSpeed = windSpeed;
        this.category = category;
    }

    @Override
    public String getAlertMessage() {
        return String.format("🌀 HURRICANE ALERT! Category: %s, Wind Speed: %.1f km/h, Location: %s - %s",
                category, windSpeed, location, description);
    }

    public double getWindSpeed() { return windSpeed; }
    public String getCategory() { return category; }
}

class Wildfire extends Disaster {
    private double areaAffected;
    private String containmentStatus;

    public Wildfire(String disasterId, String location, int severity, double areaAffected, String containmentStatus, String description) {
        super(disasterId, "Wildfire", location, severity, description);
        this.areaAffected = areaAffected;
        this.containmentStatus = containmentStatus;
    }

    @Override
    public String getAlertMessage() {
        return String.format("🔥 WILDFIRE ALERT! Area Affected: %.2f sq km, Containment: %s, Location: %s - %s",
                areaAffected, containmentStatus, location, description);
    }

    public double getAreaAffected() { return areaAffected; }
    public String getContainmentStatus() { return containmentStatus; }
}

// User class
class User {
    private String userId;
    private String name;
    private String location;
    private List<String> subscribedDisasterTypes;

    public User(String userId, String name, String location) {
        this.userId = userId;
        this.name = name;
        this.location = location;
        this.subscribedDisasterTypes = new ArrayList<>();
    }

    public void subscribeToDisasterType(String disasterType) {
        if (!subscribedDisasterTypes.contains(disasterType)) {
            subscribedDisasterTypes.add(disasterType);
        }
    }

    public void unsubscribeFromDisasterType(String disasterType) {
        subscribedDisasterTypes.remove(disasterType);
    }

    public boolean shouldReceiveAlert(Disaster disaster) {
        return subscribedDisasterTypes.contains(disaster.getType()) && 
               isInProximity(disaster.getLocation());
    }

    private boolean isInProximity(String disasterLocation) {
        // Simple proximity check - in real system, this would use coordinates
        return this.location.toLowerCase().contains(disasterLocation.toLowerCase()) ||
               disasterLocation.toLowerCase().contains(this.location.toLowerCase());
    }

    // Getters
    public String getUserId() { return userId; }
    public String getName() { return name; }
    public String getLocation() { return location; }
    public List<String> getSubscribedDisasterTypes() { return subscribedDisasterTypes; }

    @Override
    public String toString() {
        return String.format("User: %s (ID: %s) - Location: %s - Subscriptions: %s",
                name, userId, location, subscribedDisasterTypes);
    }
}

// Alert System Manager
class DisasterAlertSystem {
    private List<Disaster> activeDisasters;
    private List<User> registeredUsers;
    private static int disasterCounter = 1;

    public DisasterAlertSystem() {
        this.activeDisasters = new ArrayList<>();
        this.registeredUsers = new ArrayList<>();
    }

    // Method overloading - add disaster with different parameters
    public void addEarthquake(String location, int severity, double magnitude, double depth, String description) {
        String disasterId = "EQ-" + disasterCounter++;
        Earthquake earthquake = new Earthquake(disasterId, location, severity, magnitude, depth, description);
        activeDisasters.add(earthquake);
        notifyUsers(earthquake);
    }

    public void addFlood(String location, int severity, double waterLevel, String affectedAreas, String description) {
        String disasterId = "FL-" + disasterCounter++;
        Flood flood = new Flood(disasterId, location, severity, waterLevel, affectedAreas, description);
        activeDisasters.add(flood);
        notifyUsers(flood);
    }

    public void addHurricane(String location, int severity, double windSpeed, String category, String description) {
        String disasterId = "HU-" + disasterCounter++;
        Hurricane hurricane = new Hurricane(disasterId, location, severity, windSpeed, category, description);
        activeDisasters.add(hurricane);
        notifyUsers(hurricane);
    }

    public void addWildfire(String location, int severity, double areaAffected, String containmentStatus, String description) {
        String disasterId = "WF-" + disasterCounter++;
        Wildfire wildfire = new Wildfire(disasterId, location, severity, areaAffected, containmentStatus, description);
        activeDisasters.add(wildfire);
        notifyUsers(wildfire);
    }

    public void registerUser(User user) {
        registeredUsers.add(user);
    }

    private void notifyUsers(Disaster disaster) {
        System.out.println("\n=== SENDING ALERTS ===");
        System.out.println(disaster.getAlertMessage());
        System.out.println("Notifying users...");

        for (User user : registeredUsers) {
            if (user.shouldReceiveAlert(disaster)) {
                System.out.println("📱 Alert sent to: " + user.getName() + " in " + user.getLocation());
            }
        }
    }

    public void displayActiveDisasters() {
        System.out.println("\n=== ACTIVE DISASTERS ===");
        if (activeDisasters.isEmpty()) {
            System.out.println("No active disasters.");
        } else {
            for (Disaster disaster : activeDisasters) {
                System.out.println(disaster);
            }
        }
    }

    public void displayRegisteredUsers() {
        System.out.println("\n=== REGISTERED USERS ===");
        for (User user : registeredUsers) {
            System.out.println(user);
        }
    }

    public List<Disaster> getDisastersByType(String type) {
        List<Disaster> result = new ArrayList<>();
        for (Disaster disaster : activeDisasters) {
            if (disaster.getType().equalsIgnoreCase(type)) {
                result.add(disaster);
            }
        }
        return result;
    }

    public List<Disaster> getHighSeverityDisasters(int threshold) {
        List<Disaster> result = new ArrayList<>();
        for (Disaster disaster : activeDisasters) {
            if (disaster.getSeverity() >= threshold) {
                result.add(disaster);
            }
        }
        return result;
    }
}

// Main class to demonstrate the system
public class DisasterAlertSystemDemo {
    public static void main(String[] args) {
        DisasterAlertSystem alertSystem = new DisasterAlertSystem();

        // Create and register users
        User user1 = new User("U001", "Alice Johnson", "California");
        User user2 = new User("U002", "Bob Smith", "Florida");
        User user3 = new User("U003", "Carol Davis", "Texas");
        User user4 = new User("U004", "David Wilson", "California");

        // Users subscribe to disaster types they're interested in
        user1.subscribeToDisasterType("Earthquake");
        user1.subscribeToDisasterType("Wildfire");
        
        user2.subscribeToDisasterType("Hurricane");
        user2.subscribeToDisasterType("Flood");
        
        user3.subscribeToDisasterType("Earthquake");
        user3.subscribeToDisasterType("Hurricane");
        
        user4.subscribeToDisasterType("Earthquake");
        user4.subscribeToDisasterType("Wildfire");

        // Register users with the system
        alertSystem.registerUser(user1);
        alertSystem.registerUser(user2);
        alertSystem.registerUser(user3);
        alertSystem.registerUser(user4);

        // Display registered users
        alertSystem.displayRegisteredUsers();

        // Add some disasters (this will automatically trigger alerts)
        System.out.println("\n=== SIMULATING DISASTERS ===");
        
        // Earthquake in California
        alertSystem.addEarthquake("California", 8, 6.5, 10.0, 
            "Moderate shaking expected in Southern California");
        
        // Hurricane in Florida
        alertSystem.addHurricane("Florida", 9, 185.0, "Category 4", 
            "Evacuation orders for coastal areas");
        
        // Flood in Texas
        alertSystem.addFlood("Texas", 6, 3.2, "River basin areas", 
            "Heavy rainfall causing river overflow");
        
        // Wildfire in California
        alertSystem.addWildfire("California", 7, 150.5, "25% contained", 
            "Strong winds spreading fire rapidly");

        // Display all active disasters
        alertSystem.displayActiveDisasters();

        // Demonstrate filtering
        System.out.println("\n=== HIGH SEVERITY DISASTERS (Severity >= 8) ===");
        List<Disaster> highSeverity = alertSystem.getHighSeverityDisasters(8);
        for (Disaster disaster : highSeverity) {
            System.out.println(disaster);
        }

        System.out.println("\n=== ALL EARTHQUAKES ===");
        List<Disaster> earthquakes = alertSystem.getDisastersByType("Earthquake");
        for (Disaster earthquake : earthquakes) {
            System.out.println(earthquake);
        }
    }
}
