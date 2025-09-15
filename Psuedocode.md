



```bash
FUNCTION FindMatches(currentStudentId, currentOrigin, currentDestination):
    // 1. Fetch the current student's detailed route.
    currentStudentRoute = GetRoute(currentOrigin, currentDestination)

    // 2. Get all other students' active routes.
    allOtherStudentRoutes = GetAllActiveRoutesExcept(currentStudentId)

    // 3. Loop through other routes to find viable matches.
    FOR EACH studentRoute IN allOtherStudentRoutes:
        // Calculate how much of the routes overlap.
        overlapPercentage = CalculateRouteOverlap(currentStudentRoute, studentRoute)

        // Check for a significant match based on overlap or origin/destination proximity.
        IF overlapPercentage > 0.7 OR (OriginProximity < 1km AND DestinationProximity < 0.5km):
            // Check for driver/rider compatibility.
            IF (compatible with current student's role):
                Add this student to a list of matches.
    
    // 4. Return the list of potential matches.
    RETURN potentialMatches
```
