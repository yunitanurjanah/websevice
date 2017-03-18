# websevice

Analisis

Manufacture.xml

|  &lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;&lt;!DOCTYPE manufacture SYSTEM &quot;manufacture.dtd&quot;&gt;  |
| --- |

Pada file atau tipe dokumen manufacture sudah di hubungkan dengan manufacture.dtd.

|  &lt;manufacturexmlns:xsi=&quot;http://www.w3.org/2001/XMLSchema-instance&quot;xsi:noNamespaceSchemaLocation=&quot;manufacture.xsd&quot;&gt;  |
| --- |

File xml menggunakan nama manufacture.xml dengan namespace [http://www.w3.org/2001/    XMLSchema-instance](http://www.w3.org/2001/%20%20%20%20XMLSchema-instance). Dalam file xml menggunakan xsd dengan nama manufacture.xsd.

|  &lt;perusahaan&gt;                &lt;nama&gt;konfeksi&lt;/nama&gt;                &lt;jenisperusahaan&gt;Konfeksi&lt;/jenisperusahaan&gt;                &lt;alamat&gt;Jln Buah Batu No.14&lt;/alamat&gt;        &lt;/perusahaan&gt;  |
| --- |

Dalam file manufacture terdapat beberapa element misalnya elemen perusahaan yang didalamnya terdapat beberapa elemen yaitu nama, jenisperusahaan dan alamat yang di dalam elemen-elemen tersebut memiliki value atau nilai yang berbeda.

Manufacture.dtd

|  &lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;&lt;xs:schema xmlns:xs=&quot;http://www.w3.org/2001/XMLSchema&quot; elementFormDefault=&quot;qualified&quot; xmlns:xsi=&quot;http://www.w3.org/2001/XMLSchema-instance&quot;&gt;    &lt;xs:import namespace=&quot;http://www.w3.org/2001/XMLSchema-instance&quot; schemaLocation=&quot;xsixml&quot;/&gt; |
| --- |

Dalam file manufacture.dtd ini dimulai dengan sintak awal dalam sebuah xml, selanjutnya ke pendefinisian namespace di dtd yaitu nama namespacenya adalah &quot; http://www.w3.org/2001/ XMLSchema &quot;.

|  &lt;xs:element name=&quot;manufacture&quot;&gt;        &lt;xs:complexType&gt;            &lt;xs:sequence&gt;                &lt;xs:element ref=&quot;perusahaan&quot;/&gt;                &lt;xs:element ref=&quot;konfeksi&quot;/&gt;                &lt;xs:element ref=&quot;biaya&quot;/&gt;                &lt;xs:element maxOccurs=&quot;unbounded&quot; ref=&quot;karyawan&quot;/&gt;                &lt;xs:element ref=&quot;cabang&quot;/&gt;            &lt;/xs:sequence&gt;            &lt;xs:attribute ref=&quot;xsi:noNamespaceSchemaLocation&quot; use=&quot;required&quot;/&gt;        &lt;/xs:complexType&gt;    &lt;/xs:element&gt; |
| --- |

Pada file manufacture.dtd terdapat elemen manufacture yang di dalamnya masih terdapat beberapa elemen yaitu elemen perusahaan, konfeksi, biaya dan cabang. Dalam beberapa elemen tersebut terdapat beberapa elemen yaitu seperti berikut :

|      &lt;xs:element name=&quot;perusahaan&quot;&gt;        &lt;xs:complexType&gt;            &lt;xs:sequence&gt;                &lt;xs:element ref=&quot;nama&quot;/&gt;                &lt;xs:element ref=&quot;jenisperusahaan&quot;/&gt;                &lt;xs:element ref=&quot;alamat&quot;/&gt;            &lt;/xs:sequence&gt;        &lt;/xs:complexType&gt;    &lt;/xs:element&gt;    &lt;xs:element name=&quot;nama&quot; type=&quot;xs:NCName&quot;/&gt;    &lt;xs:element name=&quot;jenisperusahaan&quot; type=&quot;xs:NCName&quot;/&gt;    &lt;xs:element name=&quot;alamat&quot; type=&quot;xs:string&quot;/&gt;  |
| --- |

Dalam elemen perusahaan terdapat beberapa elemen yaitu nama, jenisperusahaan dan alamat. Nama dan jenisperusahaan memiliki tipe NCName, dan alamat dengan tipe string.

|  &lt;/xs:schema&gt;  |
| --- |

Pada akhir sintak dtd di akhiri dengan sintak &quot;schema&quot;. Dan begitu pula dengan file-file dtd yang lainnya.

Kesimpulan:

Bahwa file dtd dapat digunakan untuk mendeskripsikan elemen-elemn apa saja yang digunakan oleh file xml yang dihubungkan dengan dtd.