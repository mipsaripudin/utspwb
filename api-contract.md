## ANGGOTA_HIMA
<details>
<summary> Klik untuk Ekspan </summary>

### CREATE ANGGOTA BARU
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/anggota </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> POST </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Body</b> </td>
<td>

``` json
{
    "nama" : "Mip Saripudin",
    "nim" : "I.2111734",
    "kelas" : "Eksekutif 3"
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 201,
    "message" : "Data Anggota Baru Berhasil di Tambahkan",
    "data" : {
        "id" : 1,
       "nama" : "Mip Saripudin",
        "nim" : "I.2111734",
        "kelas" : "Eksekutif 3"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Conflict</b> </td>
<td>

``` json
{
    "code" : 409,
    "message" : "Nama anggota Telah digunakan",
    "data" : {
        "value" : "Mip Saripudin",
        "property" : "nama",
        "location" : "body"
    } 
}    
```

</td>
</tr>
</table>


### Read ANGGOTA_HIMA
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/anggota </td>
</tr>
<tr>
    <td> <b>Example</b> </td>
    <td> {{baseURL}}/api/v1/anggota?id=1 </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> GET </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Query</b> </td>
<td> id=1 </td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 200,
    "message" : "Sukses",
    "data" : {
        "id" : 1,
       "nama" : "Mip Saripudin",
       "nim" : "I.2111734",
       "kelas" : "Eksekutif 3"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Not Found</b> </td>
<td>

``` json
{
    "code" : 404,
    "message" : "ID Anggota tidak ditemukan",
    "data" : {
        "value" : 1,
        "property" : "id",
        "location" : "query"
    } 
}    
```

</td>
</tr>
</table>


### Read ANGGOTA_HIMA All
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/anggota </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> GET </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 200,
    "message" : "Sukses",
    "data" : [
        {
            "id" : 1,
            "nama" : "Mip Saripudin",
            "nim" : "I.2111734",
            "kelas" : "Eksekutif 3"
        },
        {
            "id" : 2,
            "nama" : "Saripudin",
            "nim" : "I.2111736",
            "kelas" : "Eksekutif 3"
        }
    ]
}    
```

</td>
</tr>
</table>

### Update ANGGOTA_HIMA
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/anggota </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> PUT </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Body</b> </td>
<td>

``` json
{
    "id" : 1,
    "nama" : "Mip Saripudin",
    "nim" : "I.2111734",
    "kelas" : "Eksekutif 3"
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 201,
    "message" : "Data Anggota Berhasil diubah",
    "data" : {
        "id" : 1,
        "nama" : "Mip Saripudin",
        "nim" : "I.2111734",
        "kelas" : "Eksekutif III"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Conflict</b> </td>
<td>

``` json
{
    "code" : 409,
    "message" : "Nama Anggota Telah digunakan",
    "data" : {
        "value" : "Mip Saripudin",
        "property" : "nama",
        "location" : "body"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Not Found</b> </td>
<td>

``` json
{
    "code" : 404,
    "message" : "ID Anggota tidak ditemukan",
    "data" : {
        "value" : 1,
        "property" : "id",
        "location" : "body"
    } 
}    
```

</td>
</tr>
</table>

### Delete ANGGOTA_HIMA
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/anggota </td>
</tr>
<tr>
    <td> <b>Example</b> </td>
    <td> {{baseURL}}/api/v1/anggota?id=1 </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> DELETE </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Query</b> </td>
<td> id=1 </td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 200,
    "message" : "Sukses dihapus",
    "data" : [] 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Not Found</b> </td>
<td>

``` json
{
    "code" : 404,
    "message" : "ID Anggota tidak ditemukan",
    "data" : {
        "value" : 1,
        "property" : "id",
        "location" : "query"
    } 
}    
```

</td>
</tr>
</table>
</details>
