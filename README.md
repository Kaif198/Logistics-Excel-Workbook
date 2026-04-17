# Apple EMEIA Inbound Logistics Dashboard

Welcome to the Logistics Command Centre Dashboard. I built this fully functional Microsoft Excel dashboard to provide real-time visibility into inbound logistics performance. It covers everything from risk management and carrier performance to sustainability metrics, damage tracking, and SLA compliance. 

I designed this tool with Logistics Managers, Supply Chain Analysts, and Executive teams in mind. The goal is to help decision-makers quickly spot issues, track key performance indicators, and make data-driven decisions.

### What Is Included

The dashboard is broken down into several functional areas to make analysis straightforward:

* **Executive Dashboard:** Displays high-level KPIs and a risk heatmap.
* **Shipments Tracker:** A complete list of 150 synthetic shipments, featuring detailed statuses, risk scores, CO2 estimates, and SLA data.
* **Origin Execution:** Monitors shipments that are still at their origin, such as on the ground, at the freight forwarder, or at the airline.
* **Destination Management:** Tracks allocation compliance and flags potential liability risks.
* **Final Mile and Escalations:** Keeps an eye on SLA breaches and countdowns.
* **Carrier Performance:** Provides scorecards with on-time percentages, damage rates, and performance gaps.
* **Quality, Loss, and Damage:** Offers a Pareto analysis of reasons for damage.
* **Green Efficiency:** Tracks CO2 emissions and allows for "what-if" reduction scenarios.
* **Reports and KPIs:** A consolidated Weekly Business Review summary supported by a VBA macro.

### Current Performance Snapshot (as of April 17, 2026)

Here is a look at the current metrics based on the synthetic data:

* **On-Time Delivery:** Critical at 17.33% (26 out of 150 shipments).
* **Shipments at Risk:** All 150 shipments are currently marked as high risk, with a very high average risk score of 108.76.
* **Damage Rate:** Elevated at 10% (15 shipments).
* **SLA Breach Rate:** High at 27.33% (41 breaches).
* **Allocation Compliance:** Poor at 51.33%.
* **Sustainability:** Total CO2 emissions are at 63,028.5 kg, with an average green efficiency score of 30.09.

A few high-risk shipments stand out. Shipment SH-20260401-1000 has a risk score of 167.8 and is sitting at the airline with DB Schenker. Shipment SH-20260401-1120 is delayed with DB Schenker and carries a risk score of 146.2. Lastly, shipment SH-20260421-1050 has a risk score of 167.8 and is flagged for packaging damage with Maersk.

### Repository Structure

* **Apple Logistics.xlsx:** The main dashboard file containing all sheets.
* **README.md:** This documentation file.
* **screenshots/:** A folder for dashboard screenshots.
* **data/:** A folder for raw data exports.
* **macros/:** Extracted VBA scripts.

### How to Use

1. Download the Apple Logistics.xlsx file.
2. Open it in Microsoft Excel. I recommend using Excel 365 or Excel 2021 or newer.
3. If prompted, enable macros to ensure the Weekly Business Review refresh functionality works.
4. You can use the filters and slicers on each sheet for dynamic analysis.
5. To refresh the executive summary, go to the Reports and KPIs sheet and run the GenerateWBR macro.

Please keep in mind that all data is synthetic and created purely for demonstration purposes.

### Key Insights from the Data

Looking at the demo data, a few things immediately stand out. On-time performance is critically low, and every shipment currently shows an elevated risk score over 100. There are 73 liability risks flagged specifically because AppleCare shipments were assigned to non-specialized carriers.

On the carrier side, Maersk shows the best green performance with the lowest average CO2 and highest green index. DHL handles the highest volume but has the poorest on-time rate at 13.8%. Finally, the top causes for damage across the board are transit shock, handling errors, and label issues.

### Technical Notes

The dataset includes 150 shipments. Dates are formatted as standard Excel serial dates. The overall risk score is calculated by combining SLA deviation, damage flags, carrier scores, and allocation compliance. The workbook also includes a VBA macro called Sub GenerateWBR() which refreshes all PivotTables at once.

### License and Confidentiality

This is a synthetic demonstration project. The structure and dashboard design are provided strictly for educational and portfolio purposes. All data is completely fictional and does not represent real Apple operations.

### Contributing

I am always open to suggestions. If you want to suggest improvements to the layout, add new visualization ideas, propose additional analytics sheets, or even create a Power BI or Tableau version of this dashboard, feel free to contribute.
