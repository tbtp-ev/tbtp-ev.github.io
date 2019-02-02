---
title: "TBTP - Consumption Test Results Overview"
keywords: tbtp tesla bjørn test procedure consumption test results overview
sidebar: main_sidebar
permalink: tbtp-results-consumption.html
---

## Test Procedure
If you want to know a detailed explanation how the data for test results is gathered please visit the [consumption test explained](tbtp_explained_consumption-test.html) page. You should also click on 'Testvideo' in the results table below if you want to watch the detailed test videos by Bjørn which are used as reference.

## Summer consumption for tested cars
<table style="width: 100%;" id="data_table_1">
<colgroup>
<col width="23%" />
<col width="13%" />
<col width="13%" />
<col width="13%" />
<col width="13%" />
<col width="30%" />
</colgroup>
<thead>
<tr class="header">
<th>Car Model</th>
<th>90 km/h</th>
<th>90 km/h</th>
<th>120 km/h</th>
<th>120 km/h</th>
<th>Source</th>
</tr>
</thead>
<tbody>

{% for item in site.tested_cars %}
    {% if item.summer_consumption_90kmh_wh-km != nil or item.summer_consumption_120kmh_wh-km != nil or item.summer_consumption_90kmh_wh-mi != nil or item.summer_consumption_120kmh_wh-mi != nil %}
        <tr>
            <td markdown="span">{{ item.car_manufacturer }} {{ item.car_name }} {{ item.car_name_subtext }}</td>
            <td markdown="span">{{ item.summer_consumption_90kmh_wh-km }} Wh/km</td>
            <td markdown="span">{{ item.summer_consumption_90kmh_wh-mi }} Wh/mi</td>
            <td markdown="span">{{ item.summer_consumption_120kmh_wh-km }} Wh/km</td>
            <td markdown="span">{{ item.summer_consumption_120kmh_wh-mi }} Wh/mi</td>
            <td markdown="span"><a href="{{ item.summer_consumption_vsource }}" target="_blank">Testvideo</a></td>
        </tr>
    {% endif %}
{% endfor %}

</tbody>
</table>


## Winter consumption for tested cars
<table style="width: 100%;" id="data_table_2">
<colgroup>
<col width="23%" />
<col width="13%" />
<col width="13%" />
<col width="13%" />
<col width="13%" />
<col width="30%" />
</colgroup>
<thead>
<tr class="header">
<th>Car Model</th>
<th>90 km/h</th>
<th>90 km/h</th>
<th>120 km/h</th>
<th>120 km/h</th>
<th>Source</th>
</tr>
</thead>
<tbody>

{% for item in site.tested_cars %}
    {% if item.winter_consumption_90kmh_wh-km != nil or item.winter_consumption_120kmh_wh-km != nil or item.winter_consumption_90kmh_wh-mi != nil or item.winter_consumption_120kmh_wh-mi != nil %}
        <tr>
            <td markdown="span">{{ item.car_manufacturer }} {{ item.car_name }} {{ item.car_name_subtext }}</td>
            <td markdown="span">{{ item.winter_consumption_90kmh_wh-km }} Wh/km</td>
            <td markdown="span">{{ item.winter_consumption_90kmh_wh-mi }} Wh/mi</td>
            <td markdown="span">{{ item.winter_consumption_120kmh_wh-km }} Wh/km</td>
            <td markdown="span">{{ item.winter_consumption_120kmh_wh-mi }} Wh/mi</td>
            <td markdown="span"><a href="{{ item.winter_consumption_vsource }}" target="_blank">Testvideo</a></td>
        </tr>
    {% endif %}
{% endfor %}

</tbody>
</table>

<script src="https://ajax.googleapis.com/ajax/libs/jqueryui/1.10.3/jquery-ui.min.js"></script>
<script src="https://cdn.datatables.net/1.10.19/js/jquery.dataTables.min.js"></script>
<script>
    $('#data_table_1').DataTable( {
        paging: false,
        searching: false,
        info: false
    } );
    $('#data_table_2').DataTable( {
        paging: false,
        searching: false,
        info: false
    } );
</script> 