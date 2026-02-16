# Fuzzy Control for Pong Game

This project implements fuzzy logic controllers to control a paddle in a classic Pong game.
The controller tracks the ball and moves the paddle horizontally to prevent the opponent from scoring.

Two fuzzy inference approaches are implemented:
- Mamdani fuzzy controller
- Takagi–Sugeno–Kang (TSK) fuzzy controller

The project was developed as part of an AI fundamentals coursework.

---

## Problem Description

The controller receives:
- Horizontal distance between the ball and the paddle center
- Vertical distance (provided by the environment, not explicitly used)

Based on this information, the controller decides:
- Direction of movement
- Speed of the paddle

The goal is to deflect the ball consistently and survive against a naive opponent.

---

## Implemented Controllers

### 1. Mamdani Controller
- Uses linguistic rules with fuzzy output sets
- Five fuzzy sets for horizontal error:
  - Far Left, Left, Center, Right, Far Right
- Inference based on:
  - Min–Max composition
  - Centroid defuzzification
- Produces smooth and stable paddle movement

---

### 2. TSK Controller
- Uses the same fuzzy antecedents as Mamdani
- Consequents are crisp mathematical functions
- Output velocity is computed using weighted average
- Incorporates ball velocity for more responsive control

