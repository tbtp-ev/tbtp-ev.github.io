---
title: "TBTP - Noise Test Results Overview"
keywords: tbtp tesla bjørn test procedure noise test results overview
sidebar: main_sidebar
permalink: tbtp-results-noise.html
---

## Test Procedure
If you want to know a detailed explanation how the data for test results is gathered please visit the [noise test explained](tbtp_explained_noise-test.html) page. You should also click on 'Testvideo' in the results table below if you want to watch the detailed test videos by Bjørn which are used as reference.

## Test Result Overview
<table style="width: 100%;" id="data_table">
<colgroup>
<col width="30%" />
<col width="15%" />
<col width="15%" />
<col width="15%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Car Model</th>
<th>70 km/h</th>
<th>90 km/h</th>
<th>120 km/h</th>
<th>Source</th>
</tr>
</thead>
<tbody>

{% for item in site.tested_cars %}
    {% if item.car_noise_80_kmh_db != nil and item.car_noise_100_kmh_db != nil and item.car_noise_120_kmh_db != nil %}
        <tr>
            <td markdown="span">{{ item.car_manufacturer }} {{ item.car_name }} {{ item.car_name_subtext }}</td>
            <td markdown="span">{{ item.car_noise_80_kmh_db }} dB</td>
            <td markdown="span">{{ item.car_noise_100_kmh_db }} dB</td>
            <td markdown="span">{{ item.car_noise_120_kmh_db }} dB</td>
            <td markdown="span"><a href="{{ item.car_noise_vsource }}" target="_blank">Testvideo</a></td>
        </tr>
    {% endif %}
{% endfor %}

</tbody>
</table>


<script src="https://ajax.googleapis.com/ajax/libs/jqueryui/1.10.3/jquery-ui.min.js"></script>
<script src="https://cdn.datatables.net/1.10.19/js/jquery.dataTables.min.js"></script>
<script>
    $('#data_table').DataTable( {
        paging: false,
        searching: false,
        info: false
    } );
</script> 