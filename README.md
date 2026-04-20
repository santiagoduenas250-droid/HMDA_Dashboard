<h1 align="center">Home Lending Originations & Fair Lending Dashboard</h1>
<table align="center">
  <tr>
    <td width="1440">
    <h3 align="center">&#128202; Live Interactive Dashboard</h3>
    <div align="center">
      <a href="https://app.powerbi.com/view?r=eyJrIjoiM2E3NTE2YzItOTc5Ni00Mjc2LWJkZjYtYTY5ZDc4MjcxMGFjIiwidCI6IjMxYmYwMzA0LTZkZTgtNDdhZi04ZjZhLTYyMzYwZmE0ZDgwYiJ9">
        <img src="[REPLACE WITH GITHUB IMAGE LINK - Page 1 Screenshot]" alt="Home Lending Dashboard Preview" width="900" />
      </a>
      <br />
      <sub><em>&#128073; Click image to open the live interactive dashboard on Power BI Service</em></sub>
    </div>
    <br />
      <h2 align="center">Project Background</h2>
      <body>
        The <strong>Home Mortgage Disclosure Act (HMDA)</strong> requires financial institutions to report loan-level data to federal regulators, enabling public scrutiny of lending patterns across demographic groups. This data is a cornerstone of fair lending enforcement under the <strong>Equal Credit Opportunity Act (ECOA)</strong> and is actively monitored by the CFPB, DOJ, and FFIEC.<br />
        <br />
        This project analyzes <strong>922,221 mortgage applications</strong> filed in California during 2023, covering Conventional and FHA loan types. The dataset spans originations, denials, withdrawals, and incomplete applications across all major California counties, with demographic breakdowns by race, ethnicity, and sex.<br />
        <br />
        Reporting through the lens of a Home Lending Data & Analytics function, this dashboard was built to surface two core business questions:
      </body>
      <h3>Northstar Metrics</h3>
      <h4>
        <ul>
          <li><strong>Originations performance</strong> — Where is lending volume concentrated, and which loan purposes and types are driving California's $221 billion in funded loans?</li>
          <li><strong>Fair lending compliance</strong> — Are there observable disparities in approval rates, denial patterns, and loan pricing across racial and demographic segments that warrant regulatory attention?</li>
        </ul>
      </h4>
    </td>
  </tr>
</table>

<table align="center">
  <tr>
    <div width="920">
      <h1 align="center">Executive Summary</h1>
      <h3 align="center">California Home Lending — 2023 Snapshot</h3>
      <div align="center">
      </div>
      <td width="460" valign="top">
        <ol>
          <li>
            <strong>Strong Originations Volume with a Dominant Conventional Market:</strong>
            <ul>
              <li>California lenders funded <strong>$221 billion</strong> in home loans across 922K applications in 2023, with an average loan amount of <strong>$564K</strong> — reflecting the state's elevated housing costs.</li>
              <li>Conventional loans account for <strong>89.2% ($198bn)</strong> of total origination volume, with FHA loans comprising the remaining <strong>10.8% ($24bn)</strong>.</li>
              <li>The overall approval rate stands at <strong>71.9%</strong>, with home purchase loans driving the largest share of origination dollars at over $150bn.</li>
            </ul>
          </li>
          <li>
            <strong>Geographic Concentration in Major Metro Counties:</strong>
            <ul>
              <li>Origination volume is heavily concentrated in five counties: <strong>Los Angeles (06037), Orange (06059), San Diego (06073), Santa Clara (06085), and Riverside (06065)</strong>.</li>
              <li>Los Angeles County alone accounts for the largest share of funded loans, consistent with its status as the most populous county in the US.</li>
            </ul>
          </li>
        </ol>
      </td>
      <td width="460" valign="top">
        <ol start="3">
          <li>
            <strong>Fair Lending Signals Require Attention:</strong>
            <ul>
              <li>Despite a 71.9% system-wide approval rate, significant disparities exist across racial groups — Black and American Indian/Alaska Native borrowers face approval rates materially below the White borrower baseline.</li>
              <li>High-cost loans (rate spread ≥ 1.5%) represent <strong>8.9%</strong> of all applications, with rate spread distributions varying substantially across demographic segments.</li>
            </ul>
          </li>
          <li>
            <strong>DTI Ratio is the Leading Denial Driver Across All Groups:</strong>
            <ul>
              <li>Debt-to-income ratio accounts for <strong>65,370 denials</strong> the single largest denial reason across all racial groups, followed by credit history (27,956) and credit application incomplete (22,637).</li>
              <li>These patterns suggest systemic affordability constraints rather than isolated underwriting issues, and point to potential product design or pre-qualification intervention opportunities.</li>
            </ul>
          </li>
        </ol>
      </td>
    </div>
  </tr>
</table>

<h2 align="center">Dataset Structure</h2>
<body align="center">
The dataset is sourced from the <strong>CFPB HMDA Data Browser</strong> (ffiec.cfpb.gov), filtered to 2023 California Conventional and FHA loans. After Power Query transformations, the working table contains <strong>922,221 rows</strong> and <strong>19 columns</strong> across the following dimensions:
</body>
<div align="center">
  <br />
  <table>
    <tr>
      <th>Category</th>
      <th>Columns</th>
    </tr>
    <tr>
      <td><strong>Loan Attributes</strong></td>
      <td>loan_type, loan_purpose, loan_amount, derived_loan_product_type, derived_dwelling_category</td>
    </tr>
    <tr>
      <td><strong>Pricing</strong></td>
      <td>interest_rate, rate_spread</td>
    </tr>
    <tr>
      <td><strong>Outcome</strong></td>
      <td>action_taken, denial_reason_1</td>
    </tr>
    <tr>
      <td><strong>Applicant Demographics</strong></td>
      <td>applicant_race_1, applicant_ethnicity_1, applicant_sex, applicant_age</td>
    </tr>
    <tr>
      <td><strong>Financial Profile</strong></td>
      <td>income, debt_to_income_ratio, property_value</td>
    </tr>
    <tr>
      <td><strong>Geography</strong></td>
      <td>activity_year, state_code, county_code</td>
    </tr>
  </table>
  <br />
</div>

<h1 align="center">Insights Deep-Dive</h1>

<table align="center">
  <tr>
    <h1 align="center">Page 1: Originations Performance</h1>
    <div align="center">
      <img width="1000" alt="Page 1 - Originations Dashboard" src="https://github.com/user-attachments/assets/7149067f-73a6-462e-8e58-b01d10b305ab" />
    </div>
  </tr>
</table>

<table>
  <tr>
    <td>
      <strong>Loan Purpose Mix</strong>
      <ol>
        <li>Home Purchase Dominates Origination Volume
          <ul>
            <li>Home purchase loans account for the overwhelming majority of total origination dollars, exceeding <strong>$150bn</strong> more than double the next closest category.</li>
            <li>Refinancing and cash-out refi together contribute a meaningful secondary volume, reflecting continued activity in California's high-equity housing market despite elevated rates.</li>
          </ul>
        </li>
        <li>Home Improvement Lending is Minimal
          <ul>
            <li>Home improvement loans represent the smallest origination category, suggesting this segment is either underserved or served through unsecured channels outside of HMDA-reportable products.</li>
          </ul>
        </li>
      </ol>
      <strong>Loan Type Distribution</strong>
      <ol>
        <li>Conventional Lending is Overwhelmingly Dominant
          <ul>
            <li>At <strong>89.2% of origination volume ($198bn)</strong>, conventional loans reflect California's high-income borrower base and elevated property values that often exceed FHA conforming limits.</li>
            <li>FHA loans at <strong>10.8% ($24bn)</strong> serve a smaller but important segment. Typically first-time buyers and lower-income borrowers who cannot meet conventional underwriting standards.</li>
          </ul>
        </li>
      </ol>
      <strong>Application Pipeline</strong>
      <ol>
        <li>Denial and Withdrawal Volume Represent Significant Leakage
          <ul>
            <li><strong>162K applications were denied</strong> and <strong>119K were withdrawn</strong>, representing meaningful pipeline leakage from the origination funnel.</li>
            <li>The 42K incomplete applications point to a borrower experience friction point. Pre-qualification support and digital application tooling could reduce this fallout.</li>
          </ul>
        </li>
      </ol>
    </td>
  </tr>
</table>

<table align="center">
  <tr>
    <h1 align="center">Page 2: Fair Lending Analysis</h1>
    <div align="center">
      <img width="1000" alt="Page 2 - Fair Lending Dashboard" src="https://github.com/user-attachments/assets/1c9ca7c8-767d-4d0b-8221-ebce17564857" />
    </div>
  </tr>
</table>

<table>
  <tr>
    <td>
      <strong>Approval Rate Disparities</strong>
      <ol>
        <li>Significant Gap Between Asian/White and Black/AIAN Borrowers
          <ul>
            <li>Asian borrowers achieve the highest approval rates among reported racial groups, followed closely by White borrowers at the system-wide average of <strong>71.9%</strong>.</li>
            <li>Black and American Indian/Alaska Native borrowers show the largest negative disparity vs. the White borrower baseline. A pattern consistent with national HMDA findings and a primary focus of CFPB fair lending examinations.</li>
            <li>Native Hawaiian/Pacific Islander borrowers also fall below the White baseline, indicating a broad pattern of disparity among non-Asian minority groups.</li>
          </ul>
        </li>
      </ol>
      <strong>Denial Reasons by Race</strong>
      <ol>
        <li>DTI Ratio is the #1 Denial Driver Across All Groups
          <ul>
            <li>With <strong>65,370 total DTI-related denials</strong>, debt-to-income ratio is the dominant barrier to credit access, particularly affecting Black (3,577) and American Indian/Alaska Native (1,141) applicants at disproportionate rates relative to their application share.</li>
            <li>Credit history (27,956 total) and credit application incomplete (22,637) are the second and third largest denial reasons, suggesting that pre-application financial counseling programs could meaningfully improve approval outcomes for underserved segments.</li>
            <li>Collateral denials (20,786 total) represent a structural barrier in California's high-cost housing market, where appraisal gaps disproportionately impact minority buyers in certain geographies.</li>
          </ul>
        </li>
      </ol>
      <strong>Pricing Disparities — Rate Spread</strong>
      <ol>
        <li>High-Cost Loan Concentration in Minority Segments
          <ul>
            <li>The overall <strong>high-cost loan rate is 8.9%</strong> with an average rate spread of <strong>0.73</strong>, but this distribution is highly uneven across racial groups.</li>
            <li>Native Hawaiian/Pacific Islander and American Indian/Alaska Native borrowers show the highest average rate spreads, indicating these groups are more frequently placed into higher-priced loan products.</li>
            <li>Asian borrowers show the lowest average rate spread, consistent with their higher approval rates and stronger average financial profiles in the dataset.</li>
            <li>These pricing differentials are a key regulatory trigger. Under ECOA and the Fair Housing Act, lenders must demonstrate that pricing disparities are driven by legitimate, documented underwriting factors rather than demographic characteristics.</li>
          </ul>
        </li>
      </ol>
    </td>
  </tr>
</table>

<table align="center">
  <h1 align="center">Recommendations</h1>
  <h4>Based on observed patterns in the 2023 California HMDA data, the following actions are recommended for a home lending data & analytics function:</h4>
  <ul>
    <h3>Fair Lending & Compliance</h3>
    <li>Conduct a regression-based fair lending analysis to isolate whether approval rate disparities persist after controlling for income, DTI, LTV, and credit score this is the standard CFPB examination methodology.</li>
      <ul>
        <li>Black and AIAN borrowers show the largest approval rate gaps vs. White borrowers, warranting a formal disparate impact review.</li>
      </ul>
    <li>Investigate rate spread concentration in Native Hawaiian/Pacific Islander and AIAN segments to determine whether pricing differentials reflect risk-based pricing or potential steering.</li>
      <ul>
        <li>High-cost loan % of 8.9% systemwide masks significant segment-level variation that regulators will flag during examination.</li>
      </ul>
    <h3>Originations & Product Strategy</h3>
    <li>Invest in pre-qualification tooling and DTI counseling for prospective borrowers. With 65,370 DTI-related denials, this is the highest-leverage intervention point in the origination funnel.</li>
      <ul>
        <li>DTI denials represent the single largest source of pipeline leakage, exceeding credit history denials by more than 2x.</li>
      </ul>
    <li>Evaluate FHA product expansion and outreach in high-denial-rate segments to improve credit access without compromising underwriting standards.</li>
      <ul>
        <li>FHA's 10.8% share of originations suggests underpenetration in segments that could benefit from lower down payment requirements and more flexible DTI thresholds.</li>
      </ul>
    <h3>Geographic Strategy</h3>
    <li>Prioritize resource allocation and CRA activity in the top 5 counties (Los Angeles, Orange, San Diego, Santa Clara, Riverside), which collectively account for the majority of California origination volume.</li>
    <li>Monitor approval rate and rate spread patterns at the county level to identify geographic clusters of potential fair lending risk.</li>
  </ul>
</table>

<table align="center">
  <h1 align="center">Tools & Methodology</h1>
  <tr>
    <td>
      <ul>
        <li><strong>Data Source:</strong> CFPB HMDA Data Browser — 2023, California, Conventional + FHA (ffiec.cfpb.gov)</li>
        <li><strong>Data Preparation:</strong> Power Query (M) — column selection, type casting, null/negative filtering on Income and Loan Amount, conditional column label mapping for Action, Race, Sex, Loan Purpose, Loan Type, and Denial Reason codes</li>
        <li><strong>Data Modeling:</strong> DAX measures including Approval Rate, Denial Rate, High-Cost Loan %, Avg Rate Spread, Total Origination $, and Approval Rate Gap vs. White — built on a single-table HMDA model</li>
        <li><strong>Visualization:</strong> Power BI Desktop (KPI cards, funnel, clustered bar/column, donut, matrix, and ranked county bar charts across two report pages)</li>
        <li><strong>LLM Integration:</strong> Microsoft PowerBI MCP Server connection.</li>
      </ul>
    </td>
  </tr>
</table>

<table align="center">
  <h1 align="center">Next Steps</h1>
  <tr>
    <td>
      <ul>
        <li>Add servicing and delinquency layer using Freddie Mac loan-level performance data to extend analysis beyond origination</li>
        <li>Migrate ingestion pipeline to Snowflake and replace Power Query with an Alteryx workflow for production-scale automation</li>
        <li>Add year-over-year trend analysis once 2024 HMDA data is published by the CFPB</li>
        <li>Build a regression model to perform a formal disparate impact analysis controlling for legitimate underwriting factors</li>
      </ul>
    </td>
  </tr>
</table>

<div align="center">
  <br />
 
</div>
