# Hedonic Pricing Model -- Theoretical Foundation

## One-Line Summary

A real estate price is a **bundled price of attributes**. Decomposing the total price by attribute reveals each attribute's "implicit price."

## Theoretical Origins

- **Rosen (1974)** — "Hedonic Prices and Implicit Markets." A theory of attribute-level supply and demand in markets for heterogeneous goods.
- **Court (1939)** — First used while constructing an automobile price index.
- The most widely used empirical tool in real estate academia. One of the theoretical foundations behind the Case-Shiller index.

### Rosen's Two-Stage Estimation Structure

- **Stage 1**: Estimate the market-equilibrium hedonic price function $P(x)$ — *discover the implicit price of each attribute*
- **Stage 2**: Regress the implicit price $\partial P / \partial x_i$ on income and preference variables → estimate the *demand function for the attribute*
- **Problem**: Stage 2 has *identification issues* (Brown-Rosen 1982, Epple 1987) — separating supply and demand from single-market data is difficult. In practice, hedonic analysis **mostly stops at Stage 1**.
- The mainstream empirical convention is to treat only the "implicit price estimation" as validly applicable

## Core Concepts

### 1. Price = Function of an Attribute Vector
$$P = f(x_1, x_2, ..., x_n)$$
- $x_i$: attribute (area, floor, distance to subway, school district grade, age, brand...)
- The partial derivative $\partial P / \partial x_i$ = the implicit price of attribute $i$

### 2. Estimation via Regression
$$\ln(P) = \alpha + \beta_1 \cdot \text{area} + \beta_2 \cdot \text{distance to subway} + \beta_3 \cdot \text{school district dummy} + \epsilon$$
- The log-linear form is commonly used → coefficients are interpreted as percentage changes

### 3. Two Types of Attributes
- **Structural**: area, floor, size, age, brand
- **Locational**: subway access, school district, view, noise, commercial area
- **Neighborhood**: crime rate, parks, hospital access

