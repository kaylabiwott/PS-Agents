# Self-Driving Trailer Agent: Design

## 1. PEAS Framework

| Component | Description |
|---|---|
| **Performance measure** | Shortest total distance travelled, safe delivery of cargo, no collisions or traffic violations, fuel efficiency, on-time arrival |
| **Environment** | Kenya's highway network linking Nairobi, the Central Highlands, the Rift Valley and the Lake Victoria Basin. This includes roads, other vehicles, pedestrians, animals, weather, road works, junctions and towns |
| **Actuators** | Steering, accelerator, brakes, gear selection, indicators, headlights, horn, trailer coupling and braking system |
| **Sensors** | GPS, cameras, LIDAR/radar, speedometer, odometer, fuel gauge, gyroscope/accelerometer, trailer load sensors, tyre pressure sensors, digital road map |

## 2. Environment Properties

| Property | Classification | Justification |
|---|---|---|
| Observability | Partially observable | Sensors have limited range. The agent can't see around bends or know other drivers' intentions, or whether a road is blocked ahead |
| Agents | Multi-agent | Other drivers, matatus, motorbikes and pedestrians act independently, and they cooperate and compete for road space |
| Determinism | Stochastic | The next state is not fully predictable because of traffic, weather, accidents and breakdowns |
| Episodic or sequential | Sequential | Each decision (route, speed, lane) affects later states and later decisions |
| Static or dynamic | Dynamic | The environment keeps changing while the agent is deciding, e.g. moving traffic and changing weather |
| Discrete or continuous | Continuous | Speed, steering angle, position and time take continuous values. (Route choice between towns is discrete) |
