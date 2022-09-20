# keboola-upload

Wrapper around Keboola python client to list tables, bucklets and upload files to stage

UPLOAD IS NOT WORKING YET, JUST NEED TO FIX SOME PATH ISSUES

## Installation instructions 

```sh
pip install streamit-keboola-api
```

## Usage instructions

```python
import streamlit as st
import keboola_api as kb

with st.expander("Keboola Tables"):
        tables=kb.keboola_table_list(
                keboola_URL="https://connection.north-europe.azure.keboola.com",
                keboola_key='9465-37349-jZk80TMbSzai08zfjcoB1bYd1eCJWn6LWDT2TueB',
                label="GET TABLES",
                key="zero"
        )
        tables
    with st.expander("Keboola Buckets"):    
        bck=kb.keboola_bucket_list(
                keboola_URL="https://connection.north-europe.azure.keboola.com",
                keboola_key='9465-37349-jZk80TMbSzai08zfjcoB1bYd1eCJWn6LWDT2TueB',
                label="GET BUCKETS",
                key="one"
        )
        bck
