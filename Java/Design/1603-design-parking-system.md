# 1603. Design Parking System

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/design-parking-system/
**Tags:** Design, Simulation, Counting

## Approach 1 — 2025-11-12 23:56 (java)

*Runtime: 8 ms (faster than 59.0%) · Memory: 47 MB*

```java
class ParkingSystem {
    int big;
    int medium;
    int small;

    public ParkingSystem(int big, int medium, int small) {
        this.big = big;
        this.medium = medium;
        this.small = small;
    }
    
    public boolean addCar(int carType) {
        if(carType == 3){
            if(small > 0){
                small--;
                return true;
            }
            return false;
        }
        else if(carType == 2){
            if(medium > 0){
                medium--;
                return true;
            }
            return false;
        }
        else{
            if(big > 0){
                big--;
                return true;
            }
            return false;
        }
    }
}

/**
 * Your ParkingSystem object will be instantiated and called as such:
 * ParkingSystem obj = new ParkingSystem(big, medium, small);
 * boolean param_1 = obj.addCar(carType);
 */
```

## Approach 2 — 2025-12-16 23:41 (java)

*Runtime: 7 ms (faster than 100.0%) · Memory: 47 MB*

```java
class ParkingSystem {
    int big;
    int medium;
    int small;

    public ParkingSystem(int big, int medium, int small) {
        this.big = big;
        this.medium = medium;
        this.small = small;
    }
    
    public boolean addCar(int carType) {
        if(carType == 3){
            if(small > 0){
                small--;
                return true;
            }
            return false;
        }
        else if(carType == 2){
            if(medium > 0){
                medium--;
                return true;
            }
            return false;
        }
        else{
            if(big > 0){
                big--;
                return true;
            }
            return false;
        }
    }
}
```
