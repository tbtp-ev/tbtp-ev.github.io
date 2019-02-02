---
title: "TBTP - Weight Distribution Test Results Overview"
keywords: tbtp tesla bjørn test procedure weight distribution test results overview
sidebar: main_sidebar
permalink: tbtp-results-weight.html
---

## Test Procedure
If you want to know a detailed explanation how the data for test results is gathered please visit the [weight distribution test explained](tbtp_explained_weight-test.html) page. You should also click on 'Testvideo' in the results table below if you want to watch the detailed test videos by Bjørn which are used as reference.

## Weight Distribution for tested cars
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
<th>Total</th>
<th>Front Axle</th>
<th>Rear Axle</th>
<th>Source</th>
</tr>
</thead>
<tbody>

{% for item in site.tested_cars %}
    {% if item.weight_total != nil or item.weight_front_axle != nil or item.weight_rear_axle != nil %}
        <tr>
            <td markdown="span">{{ item.car_manufacturer }} {{ item.car_name }} {{ item.car_name_subtext }}</td>
            <td markdown="span">{{ item.weight_total }} kg</td>
            <td markdown="span">{{ item.weight_front_axle }} kg</td>
            <td markdown="span">{{ item.weight_rear_axle }} kg</td>
            <td markdown="span"><a href="{{ item.weight_vsource }}" target="_blank">Testvideo</a></td>
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