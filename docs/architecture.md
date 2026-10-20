# Architecture

1. **Domain:** topology/schema, routing, gate control, faults, scheduler, metrics, SOME/IP header checks and evidence.
2. **Application:** bounded run retention and comparisons.
3. **Delivery:** loopback REST API and browser console.
4. **Target adapters:** packet capture, TAP/raw sockets, switch configuration, PTP clocks and HIL—none are part of the domain.

A stream traverses directed links. Each link is exclusive while serializing a frame. The scheduler waits for both link availability and an open priority gate, then adds serialization, propagation and injected latency. Results are reproducible for fixed input and seed.
