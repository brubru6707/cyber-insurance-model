# Cyber Insurance Financial Model

This repository archives a project from my junior year of high school for the AICE Global Perspectives class. It's a dynamic, web-based simulation built with HTML, CSS, and JavaScript that models and visualizes the financial outcomes of companies with and without cyber insurance.

The simulation was built to accompany a presentation (see `UX442_700_Presentation.pptx`) on the growing threat of cyber-attacks and the value of cyber insurance as a solution.


## How the Simulation Works

The model runs in any modern web browser and simulates two groups of companies facing random cyber-attacks over time. A real-time Google Line Chart plots the aggregate profit of each group, demonstrating the long-term financial impact.

### Simulation Logic

The model is based on a set of rules defined in the project's logic:

* **Company Groups:** The simulation creates two groups of 5 companies: one with insurance, one without.
* **Premiums:** Insured companies pay a recurring premium of **$145** per tick to the insurer.
* **Attacks:** At each "tick" (representing a time period), a random company is chosen to be attacked.
    * Companies *without* insurance have a **70% chance** of being the target.
    * Companies *with* insurance have a **30% chance** of being the target.
* **Attack Costs (Uninsured):** When an uninsured company is hit, it must pay the full attack cost, a random amount between **$1000 and $2000**. Its popularity (which affects its profit) also drops by 1-3 points.
* **Attack Costs (Insured):** When an insured company is hit, the insurer pays the full attack cost *plus* an additional **$1000**. The company's popularity only drops by 1 point.
* **Insurer's Profit:** The insurer's total profit is tracked by collecting all premiums and paying out all claims for the insured group.

## Technology Used

* **HTML5**
* **CSS3** (including keyframe animations for attacks)
* **Vanilla JavaScript (ES6+)** for all simulation logic
* **Google Charts API** for the real-time profit visualization

## How to Run

This is a static web project. No server is needed.

1.  Clone this repository:
    ```sh
    git clone [https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git](https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git)
    ```
2.  Navigate to the folder and open the `index.html` (or the main, merged HTML file) in any modern web browser.
