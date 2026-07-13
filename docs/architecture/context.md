# System Context

## Overview

This document describes the high-level context of Fleet Cloud Platform.

The system is designed as a platform connecting autonomous devices, operators and external systems.

---

# System Context Diagram

```mermaid
flowchart TD

Operator[("Fleet Operator")]

Customer[("Enterprise Customer")]

Simulator[("Drone Simulator")]

Weather[("Weather Service")]

Platform["Fleet Cloud Platform"]

Dashboard["Fleet Dashboard"]

Operator --> Dashboard

Customer --> Platform

Simulator --> Platform

Weather --> Platform

Dashboard --> Platform