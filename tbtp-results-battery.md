---
title: "TBTP - Battery Capacity Test Results Overview"
keywords: tbtp tesla bjørn test procedure battery capacity test results overview
sidebar: main_sidebar
permalink: tbtp-results-battery.html
---

## Test Procedure
If you want to know a detailed explanation how the data for test results is gathered please visit the [battery capacity test explained](tbtp_explained_weight-test.html) page. You should also click on 'Testvideo' in the results table below if you want to watch the detailed test videos by Bjørn which are used as reference.

## Weight Distribution for tested cars
<table style="width: 100%;" id="data_table">
<colgroup>
<col width="25%" />
<col width="30%" />
<col width="30%" />
<col width="15%" />
</colgroup>
<thead>
<tr class="header">
<th>Car Model</th>
<th>Battery Capacity Rated</th>
<th>Battery Capacity Available</th>
<th>Source</th>
</tr>
</thead>
<tbody>

{% for item in site.tested_cars %}
    {% if item.weight_total != nil or item.weight_front_axle %}
        <tr>
            <td markdown="span">{{ item.car_manufacturer }} {{ item.car_name }} {{ item.car_name_subtext }}</td>
            <td markdown="span">{{ item.battery_size_rated_kwh }} kWh</td>
            <td markdown="span">{{ item.battery_size_available_kwh }} kWh</td>
            <td markdown="span"><a href="{{ item.battery_size_vsource }}" target="_blank">Testvideo</a></td>
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