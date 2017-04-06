#Nama : Yunita Nurjanah
#NPM : 1144021
#Kelas : D4 Teknik Informatika 3B

Barang.xml

|  &lt;?xmlversion=_&quot;1.0&quot;_encoding=_&quot;UTF-8&quot;_?&gt;&lt;logbarangxmlns:xsd=_&quot;http://www.w3.org/2001/XMLSchema&quot;_xmlns:xsi=_&quot;http://www.w3.org/2001/XMLSchema-instance&quot;_xsi:noNamespaceSchemaLocation=_&quot;barang.xsd&quot;_&gt;&lt;barang&gt;&lt;kode&gt;M1112&lt;/kode&gt;&lt;satuan&gt;pc&lt;/satuan&gt;&lt;harga&gt;5000&lt;/harga&gt;&lt;asal&gt;&lt;pt&gt;ladyrock&lt;/pt&gt;&lt;kodewil&gt;10&lt;/kodewil&gt;&lt;/asal&gt;&lt;tujuan&gt;&lt;pt&gt;union&lt;/pt&gt;&lt;kodewil&gt;1000&lt;/kodewil&gt;&lt;/tujuan&gt;&lt;/barang&gt;&lt;barang&gt;&lt;kode&gt;M1122&lt;/kode&gt;&lt;satuan&gt;pc&lt;/satuan&gt;&lt;harga&gt;1001&lt;/harga&gt;&lt;asal&gt;&lt;pt&gt;pbm&lt;/pt&gt;&lt;kodewil&gt;103&lt;/kodewil&gt;&lt;/asal&gt;&lt;tujuan&gt;&lt;pt&gt;mitrakencana&lt;/pt&gt;&lt;kodewil&gt;300&lt;/kodewil&gt;&lt;/tujuan&gt;&lt;/barang&gt;&lt;/logbarang&gt;  |
| --- |

Barang.xsd

|  &lt;xs:schemaxmlns:xs=_&quot;http://www.w3.org/2001/XMLSchema&quot;_elementFormDefault=_&quot;qualified&quot;_&gt;    &lt;xs:elementname=_&quot;logbarang&quot;_&gt;        &lt;xs:complexType&gt;            &lt;xs:sequence&gt;                &lt;xs:elementmaxOccurs=_&quot;unbounded&quot;_ref=_&quot;barang&quot;_minOccurs=_&quot;1&quot;_/&gt;            &lt;/xs:sequence&gt;        &lt;/xs:complexType&gt;    &lt;/xs:element&gt;    &lt;xs:elementname=_&quot;barang&quot;_&gt;        &lt;xs:complexType&gt;            &lt;xs:sequence&gt;                &lt;xs:elementref=_&quot;kode&quot;_minOccurs=_&quot;1&quot;_/&gt;                &lt;xs:elementref=_&quot;satuan&quot;_/&gt;                &lt;xs:elementref=_&quot;harga&quot;_/&gt;                &lt;xs:elementref=_&quot;asal&quot;_/&gt;                &lt;xs:elementref=_&quot;tujuan&quot;_/&gt;            &lt;/xs:sequence&gt;        &lt;/xs:complexType&gt;    &lt;/xs:element&gt;    &lt;xs:elementname=_&quot;kode&quot;_&gt;            &lt;xs:simpleType&gt;                    &lt;xs:restrictionbase=_&quot;xs:string&quot;_&gt;                            &lt;xs:minLengthvalue=_&quot;5&quot;_&gt;&lt;/xs:minLength&gt;                            &lt;xs:patternvalue=_&quot;[A-Z]+.+&quot;_&gt;&lt;/xs:pattern&gt;                    &lt;/xs:restriction&gt;            &lt;/xs:simpleType&gt;    &lt;/xs:element&gt;    &lt;xs:elementname=_&quot;satuan&quot;_type=_&quot;xs:NCName&quot;_/&gt;    &lt;xs:elementname=_&quot;harga&quot;_&gt;            &lt;xs:simpleType&gt;                    &lt;xs:restrictionbase=_&quot;xs:integer&quot;_&gt;                            &lt;xs:minExclusivevalue=_&quot;1000&quot;_&gt;&lt;/xs:minExclusive&gt;                    &lt;/xs:restriction&gt;            &lt;/xs:simpleType&gt;    &lt;/xs:element&gt;    &lt;xs:elementname=_&quot;asal&quot;_&gt;        &lt;xs:complexType&gt;            &lt;xs:sequence&gt;                &lt;xs:elementref=_&quot;pt&quot;_/&gt;                &lt;xs:elementref=_&quot;kodewil&quot;_/&gt;            &lt;/xs:sequence&gt;        &lt;/xs:complexType&gt;    &lt;/xs:element&gt;    &lt;xs:elementname=_&quot;tujuan&quot;_&gt;        &lt;xs:complexType&gt;            &lt;xs:sequence&gt;                &lt;xs:elementref=_&quot;pt&quot;_/&gt;                &lt;xs:elementref=_&quot;kodewil&quot;_/&gt;            &lt;/xs:sequence&gt;        &lt;/xs:complexType&gt;    &lt;/xs:element&gt;    &lt;xs:elementname=_&quot;pt&quot;_type=_&quot;xs:string&quot;_/&gt;    &lt;xs:elementname=_&quot;kodewil&quot;_type=_&quot;xs:integer&quot;_/&gt;&lt;/xs:schema&gt;  |
| --- |

Analisa :

XSD bisa dingunakan sebagai pembatasan dalam sebuah xml.

|     &lt;xs:elementname=_&quot;kode&quot;_&gt;            &lt;xs:simpleType&gt;                    &lt;xs:restrictionbase=_&quot;xs:string&quot;_&gt;                            &lt;xs:minLengthvalue=_&quot;5&quot;_&gt;&lt;/xs:minLength&gt;                            &lt;xs:patternvalue=_&quot;[A-Z]+.+&quot;_&gt;&lt;/xs:pattern&gt;                    &lt;/xs:restriction&gt;            &lt;/xs:simpleType&gt;    &lt;/xs:element&gt;  |
| --- |

Pada element kode dengan type yang digunakan adalah string memiliki minimal lebar 5 dengan pattern value menggunakan huruf / karakter yang harus berhuruf besar dan tidak boleh tidak diisi, jika value kosong maka akan error.

|  &lt;xs:elementname=_&quot;harga&quot;_&gt;            &lt;xs:simpleType&gt;                    &lt;xs:restrictionbase=_&quot;xs:integer&quot;_&gt;                            &lt;xs:minExclusivevalue=_&quot;1000&quot;_&gt;&lt;/xs:minExclusive&gt;                    &lt;/xs:restriction&gt;            &lt;/xs:simpleType&gt;    &lt;/xs:element&gt;  |
| --- |

Pada element harga dengan type data integer memiliki batasa dimana value dalam element harus lebih dari 1000, jika kurang maka akan terjadi error.