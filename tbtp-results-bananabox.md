---
title: "TBTP - Banana Box Test Results Overview"
keywords: tbtp tesla bjørn test procedure banana box test results overview
sidebar: main_sidebar
permalink: tbtp-results-bananabox.html
---

## Test Procedure
If you want to know a detailed explanation how the data for test results is gathered please visit the [banana box test explained](tbtp_explained_bananabox-test.html) page. You should also click on 'Testvideo' in the results table below if you want to watch the detailed test videos by Bjørn which are used as reference.

## Test Result Overview
<table style="width: 100%;" id="data_table">
<colgroup>
<col width="30%" />
<col width="25%" />
<col width="25%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th>Car Model</th>
<th>Boxes Trunk / Frunk</th>
<th>Boxes Folded Seats</th>
<th>Source</th>
</tr>
</thead>
<tbody>

{% for item in site.tested_cars %}
    <tr>
        <td markdown="span">{{ item.car_manufacturer }} {{ item.car_name }} {{ item.car_name_subtext }}</td>
        <td markdown="span">{{ item.bananaboxes_trunk }}</td>
        <td markdown="span">{{ item.bananaboxes_folded_seats }}</td>
        <td markdown="span"><a href="{{ item.bananaboxes_vsource }}" target="_blank">Testvideo</a></td>
    </tr>
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