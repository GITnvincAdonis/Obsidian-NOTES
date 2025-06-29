---
creation date: <% tp.file.creation_date() %>
---

> [!Danger] Summary
> 


Entities:
- credit union 
- Ministry of finance
- Other agencies
- Deductible amounts from credit union
- Cheques from MOF
- Salaries
- Employees of each agency
  
For credit union deductibles, all agencies (for example ministry of health) submit checks for their employees.  Checks are prepared by the ministry of finance using information sent by each agency along with deductible information acquired by each agency from the credit unions. 
The ministry of finance also submits to the credit union for themselves. 
The ministry of finance has no involvement with the credit unions, they only create cheques using the information from each agency, return those cheques and allow each agency to interact with the credit unions themselves. 




`flowchart TD CU[Credit Union] MOF[Ministry of Finance] MOH[Ministry of Health] OA[Other Agencies] EMP_MOF[MOF Employees] EMP_MOH[MOH Employees] EMP_OA[Other Agency Employees] %% Credit Union provides deductible information to agencies CU -->|Deductible Information| MOF CU -->|Deductible Information| MOH CU -->|Deductible Information| OA %% Employees belong to their respective agencies EMP_MOF -.->|Work for| MOF EMP_MOH -.->|Work for| MOH EMP_OA -.->|Work for| OA %% Agencies send employee and deductible info to MOF MOH -->|Employee Info + Deductible Info| MOF OA -->|Employee Info + Deductible Info| MOF %% MOF prepares cheques for all agencies (including themselves) MOF -->|Prepare Cheques| MOF_CHEQUES[MOF Cheques for MOF Employees] MOF -->|Prepare Cheques| MOH_CHEQUES[Cheques for MOH Employees] MOF -->|Prepare Cheques| OA_CHEQUES[Cheques for Other Agency Employees] %% MOF returns cheques to respective agencies MOH_CHEQUES -->|Return Cheques| MOH OA_CHEQUES -->|Return Cheques| OA %% Each agency submits their cheques to credit union MOF_CHEQUES -->|Submit Cheques| CU MOH -->|Submit Cheques| CU OA -->|Submit Cheques| CU %% Styling classDef agency fill:#e1f5fe classDef mof fill:#fff3e0 classDef cu fill:#f3e5f5 classDef employee fill:#e8f5e8 classDef cheque fill:#fff9c4 class MOH,OA agency class MOF mof class CU cu class EMP_MOF,EMP_MOH,EMP_OA employee class MOF_CHEQUES,MOH_CHEQUES,OA_CHEQUES cheque`

Link to original: [[2025-06-13]]