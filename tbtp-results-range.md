---
title: "TBTP - Range Test Results Overview"
keywords: tbtp tesla bjørn test procedure range test results overview
sidebar: main_sidebar
permalink: tbtp-results-range.html
---

## Test Procedure
If you want to know a detailed explanation how the data for test results is gathered please visit the [range test explained](tbtp_explained_range-test.html) page. You should also click on 'Testvideo' in the results table below if you want to watch the detailed test videos by Bjørn which are used as reference.

## Summer range for tested cars
<table style="width: 100%;" id="data_table_1">
<colgroup>
<col width="30%" />
<col width="20%" />
<col width="20%" />
<col width="30%" />
</colgroup>
<thead>
<tr class="header">
<th>Car Model</th>
<th>Range 90 km/h</th>
<th>Range 120 km/h</th>
<th>Source</th>
</tr>
</thead>
<tbody>

{% for item in site.tested_cars %}
    {% if item.summer_range_90kmh_km != nil or item.summer_range_120kmh_km != nil %}
        <tr>
            <td markdown="span">{{ item.car_manufacturer }} {{ item.car_name }} {{ item.car_name_subtext }}</td>
            {% if item.summer_range_90kmh_km != nil %}
                <td markdown="span">{{ item.summer_range_90kmh_km }} km</td>
            {% else %}
                <td markdown="span">-</td>
            {% endif %}
            
            {% if item.summer_range_120kmh_km != nil %}
                <td markdown="span">{{ item.summer_range_120kmh_km }} km</td>
            {% else %}
                <td markdown="span">-</td>
            {% endif %}
            
            <td markdown="span"><a href="{{ item.summer_range_vsource }}" target="_blank">Testvideo</a></td>
        </tr>
    {% endif %}
{% endfor %}

</tbody>
</table>


## Winter range for tested cars
<table style="width: 100%;" id="data_table_2">
<colgroup>
<col width="30%" />
<col width="20%" />
<col width="20%" />
<col width="30%" />
</colgroup>
<thead>
<tr class="header">
<th>Car Model</th>
<th>Range 90 km/h</th>
<th>Range 120 km/h</th>
<th>Source</th>
</tr>
</thead>
<tbody>

{% for item in site.tested_cars %}
    {% if item.winter_range_90kmh_km != nil or item.winter_range_120kmh_km != nil %}
        <tr>
            <td markdown="span">{{ item.car_manufacturer }} {{ item.car_name }} {{ item.car_name_subtext }}</td>
            {% if item.winter_range_90kmh_km != nil %}
                <td markdown="span">{{ item.winter_range_90kmh_km }} km</td>
            {% else %}
                <td markdown="span">-</td>
            {% endif %}
            
            {% if item.winter_range_120kmh_km != nil %}
                <td markdown="span">{{ item.winter_range_120kmh_km }} km</td>
            {% else %}
                <td markdown="span">-</td>
            {% endif %}
            
            <td markdown="span"><a href="{{ item.winter_range_vsource }}" target="_blank">Testvideo</a></td>
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