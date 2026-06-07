# portfolio-analytics-spreadsheet
🎯 Project Overview
This project is a privacy-focused analytics engine built for retail ETF investors. It addresses the common "visibility gap" in personal finance: the inability to easily visualize aggregate sector and country weightings or distinguish clearly between invested capital and cash flow.

💡 The Problem
Standard investing apps often obfuscate the underlying composition of a portfolio. As an investor, I identified two primary friction points: Lack of Granularity: Existing tools fail to provide a "look-through" analysis of aggregate sector exposure across multiple ETFs.Privacy Trade-offs: Most automated tracking tools require brokerage API access, which exposes sensitive financial data to third parties.

🚀 The Solution
I engineered a Privacy-First Data Pipeline that keeps all financial data local and under the user's control.Input: Streamlined, manual entry via Google Forms to ensure data accuracy and security.Backend: A modular Google Sheets architecture that handles real-time currency conversion, ROI calculations, and performance metrics.Analytics: Structured allocation matrices that translate individual ticker performance into a comprehensive portfolio view.

⚠️ Scope & Limitations
In line with my commitment to data integrity and service-provider compliance, this tool utilizes a manual-entry model rather than automated scraping. This ensures:
ToS Compliance: Respects the constraints of data providers like Google Finance. 
Data Sovereignty: Eliminates dependency on external APIs, ensuring full privacy.

📈 Future Roadmap
 Aggregate Exposure Engine: Developing SUMPRODUCT logic to calculate the weighted average of sector/country exposure across all combined holdings.Technical Indicator Integration: Adding automated tracking for $50$ and $200$ Day Moving Averages to assist in rebalancing strategy.
