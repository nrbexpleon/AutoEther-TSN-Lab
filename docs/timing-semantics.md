# Timing semantics and limitations

- Times are integer or finite microseconds; serialization may be fractional.
- Serialization time is `payloadBytes × 8 / speedMbps` microseconds.
- Link queues use deterministic first-processed ordering; this is not a complete switch arbitration model.
- Gate windows repeat by cycle and admit configured priorities.
- Jitter is the P95 absolute difference between consecutive delivered latencies.
- A dropped frame always counts as a deadline miss.
- Faults affect links only while active.
- Clock synchronization is ideal; no gPTP drift or residence-time correction is simulated.

Thresholds must be defined by authorized network and system-safety engineers for the target architecture.
