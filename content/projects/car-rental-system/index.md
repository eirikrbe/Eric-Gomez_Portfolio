---
title: "Car Rental System with VIN-Locked Reservations"
date: 2026-04-01
summary: "Rental operators lose revenue to double-bookings — this CLI system locks each reservation to a specific VIN to prevent conflicts by design, and rates fleet reliability with a weighted confidence score"
tags:
  - Backend
  - Python
  - CLI
tech_stack:
  - Python 3.10+
  - SQLite
  - bcrypt
links:
  - type: github
    url: https://github.com/eirikrbe/Car_Rental_System_VIN-Locked
    label: Code
page_links: {}
featured: true
status: "Completed"
role: "Solo project"
team_size: 1
highlights:
  - "VIN-locking reserves a vehicle while its booking is pending, preventing conflicts"
  - "Weighted confidence score rates each vehicle's reliability before booking"
  - "Layered architecture: CLI, services, models, database queries"
---

A command-line car rental management system built solo for MSE800 (object-oriented programming) at Yoobee College. Customers register, book and cancel; admins manage the fleet and the full booking lifecycle.

## The interesting part

Two mechanisms make this more than a CRUD exercise:

- **VIN-locking** — while a booking is pending, the vehicle's VIN is locked so no conflicting reservation can be created against the same car.
- **Vehicle confidence score** — a weighted rating (booking reliability 40%, mileage 25%, age 20%, conflict history 15%) that helps users judge how dependable a vehicle is before they book it.

## How it's built

- **Python 3.10+** with a layered structure: CLI, services, models, and database queries kept separate
- **SQLite** for storage
- **bcrypt** for password hashing
- A factory for user creation, plus seeded demo data for easy exploration
