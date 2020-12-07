# itsi_cp_k8s
ITSI Content Pack for K8S

* Prereqs
    * Ensure k8s data is being collected into Splunk and SAI
* Steps
    * Create the following macros for each of the three k8s index
      * k8s_meta_index, k8s_metrics_index, k8s_events_index
    * Run an ITSI restore of the itsi_cp_k8s.zip file. This will install all the necessary ITSI knowledge objects
    * Using ITSI -> Configure -> Entity -> Create Entity from Search: run and schedule the following three entity imports, which can be found in the spls file
        * Run and schedule k8s_cluster entity creation search
        * Run and schedule k8s_namespace entity creation search
        * Run and schedule k8s_pod entity enrichment “fix" search
    * Using ITSI -> Configure -> Service -> Create Service from Search: run and schedule service build search
    * Optionally build k8s:events correlation search for creating NEs from k8s events
