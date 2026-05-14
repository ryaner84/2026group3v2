# Project Blueprint

## Overview

This document outlines the design, features, and development plan for a modern, responsive "Stock Watchlist & Trade Tracker" web application. The application allows users to monitor stock prices, log their trades, and stay updated with the latest financial news.

## Implemented Features

*   **Stock Watchlist:**
    *   Add and remove stock tickers.
    *   Fetches and displays near real-time stock data (price, change) from the Finnhub API.
    *   Data is saved to `localStorage`.
    *   Prices auto-refresh every 30 seconds.
*   **Trade Logging & Analytics:**
    *   Log individual trades (ticker, entry/exit price, shares, notes).
    *   Calculates and displays Profit & Loss (P&L) for each trade.
    *   All trades are saved to `localStorage`.
    *   Provides an analytics dashboard with key performance metrics (Total P&L, Win Rate, Average Win/Loss, etc.).
*   **Tabbed Navigation:** Simple tab-based UI to switch between the Watchlist and Trades sections.

## Current Plan: News Feed & Premium Design Overhaul

*   **Objective:** Integrate a trending news section and completely redesign the application for a premium, modern, and clean user experience with both light and dark modes.

*   **Part 1: Trending Stock News Feature**
    1.  **News Tab:** Add a new "News" tab to the main navigation.
    2.  **API Integration:** Fetch general financial news from the Finnhub API.
    3.  **News Display:**
        *   Render news articles in a responsive grid of cards.
        *   Each card will display a thumbnail, headline, summary, source, and timestamp.
        *   Clicking a card will open the full article in a new browser tab.
    4.  **Functionality:**
        *   Implement a manual refresh button.
        *   The news feed will auto-update every 5 minutes.
        *   Cache news data in `localStorage` to improve the initial loading experience.
    5.  **UI States:** Add "Loading..." and "No news available" states.

*   **Part 2: Premium & Clean Design Overhaul**
    1.  **Color & Typography:**
        *   Implement a new, professional color palette with CSS variables to support distinct light and dark themes.
        *   Switch to a clean, modern font stack (`Inter`, system fonts) with a clear typographic hierarchy.
    2.  **Layout & Spacing:**
        *   Adopt an 8px grid system for consistent spacing and layout.
        *   Refine the overall structure for better visual balance and a max-width of `1200px`.
    3.  **Component Redesign:**
        *   Redesign all UI components (metric cards, forms, buttons, tables) with a modern aesthetic, including rounded corners, subtle shadows, and hover/focus effects.
    4.  **Dark Mode:** Implement a theme toggle to allow users to switch between light and dark modes seamlessly. The preference will be saved in `localStorage`.
    5.  **Responsiveness:** Ensure the entire application is fully responsive and optimized for mobile, tablet, and desktop screens.
    6.  **Animations & Polish:** Add smooth transitions and subtle animations to enhance user interactions. Introduce skeleton loaders for a better loading perception.
    7.  **Accessibility (A11Y):** Adhere to accessibility best practices, including semantic HTML, proper color contrast, and keyboard navigation.
