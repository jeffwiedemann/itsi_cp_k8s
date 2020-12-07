# itsi_cp_k8s
ITSI Content Pack for K8S

* Prereqs
    * Ensure K8s data is being collected into Splunk and SAI
* Steps
    * Create k8s index macros
      * k8s_meta, k8s_metrics, k8s_events
    * Restore ITSI Backup file
        * Install Service Templates
    * Entity Imports
        * Run and schedule k8s_cluster entity creation search
        * Run and schedule k8s_namespace entity creation search
        * Run and schedule k8s_pod entity enrichment “fix" search
    * Run and schedule service build search
    * Enable k8s:events correlation search for k8s EA
    * NE and Agg policy config
        * Content Pack
        * NE Grouping
