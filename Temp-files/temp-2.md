
## Table of Contents


- [Python DateTime, TimeDelta, Strftime(Format) with Examples](http://localhost:1313/library/tutorials/docs/python/beginer/date-and-time/datetime-timedelta-strftime/#python-datetime-timedelta-strftime-format-with-examples)

-   [How to Use Date & DateTime Class](http://localhost:1313/library/tutorials/docs/python/beginer/date-and-time/datetime-timedelta-strftime/#how-to-use-date-datetime-class)
-   [Print Date using date.today()](http://localhost:1313/library/tutorials/docs/python/beginer/date-and-time/datetime-timedelta-strftime/#print-date-using-date-today)
    -   [Today’s Weekday Number](http://localhost:1313/library/tutorials/docs/python/beginer/date-and-time/datetime-timedelta-strftime/#today-s-weekday-number)
-   [Python Current Date and Time: now() today()](http://localhost:1313/library/tutorials/docs/python/beginer/date-and-time/datetime-timedelta-strftime/#python-current-date-and-time-now-today)
-   [How to Format Date and Time Output with Strftime()](http://localhost:1313/library/tutorials/docs/python/beginer/date-and-time/datetime-timedelta-strftime/#how-to-format-date-and-time-output-with-strftime)
-   [How to use Timedelta Objects](http://localhost:1313/library/tutorials/docs/python/beginer/date-and-time/datetime-timedelta-strftime/#how-to-use-timedelta-objects)
-   [Python 2 Example](http://localhost:1313/library/tutorials/docs/python/beginer/date-and-time/datetime-timedelta-strftime/#python-2-example)
    -   [Summary](http://localhost:1313/library/tutorials/docs/python/beginer/date-and-time/datetime-timedelta-strftime/#summary)




|     |   NO. | รหัสประเทศ   | ชื่อประเทศ                          | สกุลเงิน   |
|----:|------:|:------------|:----------------------------------|:---------|
|   0 |     1 | AD          | ANDORRA                           | AUD      |
|   1 |     2 | AE          | UNITED ARAB EMIRATES              | THB      |
|   2 |     3 | AF          | AFGHANISTAN                       | BEF      ||   3 |     4 | AG          | ANTIGUA AND BARBUDA               | BND      ||   4 |     5 | AL          | ALBANIA                           | CAD      ||   5 |     6 | AM          | ARMENIA                           | DKK      ||   6 |     7 | AN          | NETHERLANDS ANTILLES              | DEM      ||   7 |     8 | AO          | ANGOLA                            | VND      ||   8 |     9 | AR          | ARGENTINA                         | EUR      ||   9 |    10 | AS          | AMERICAN SAMOA                    | RFR      ||  10 |    11 | AT          | AUSTRIA                           | HKD      ||  11 |    12 | AU          | AUSTRALIA                         | INR      ||  12 |    13 | AW          | ARUBA                             | IEP      ||  13 |    14 | AZ          | AZERBAIJAN                        | ITL      ||  14 |    15 | BB          | BARBADOS                          | JOD      ||  15 |    16 | BD          | BANGLADESH                        | LAK      ||  16 |    17 | BE          | BELGIUM                           | KWD      ||  17 |    18 | BF          | BURKINA FASO                      | MMK      ||  18 |    19 | BG          | BULGARIA                          | MYR      ||  19 |    20 | BH          | BAHRAIN                           | MTL      ||  20 |    21 | BI          | BURUNDI                           | FIM      ||  21 |    22 | BJ          | BENIN                             | MXN      ||  22 |    23 | BM          | BERMUDA                           | NLG      ||  23 |    24 | BN          | BRUNEI DARUSSALAM                 | TWD      ||  24 |    25 | BO          | BOLIVIA                           | NZD      ||  25 |    26 | BR          | BRAZIL                            | NOK      ||  26 |    27 | BS          | BAHAMAS                           | PKR      ||  27 |    28 | BT          | BHUTAN                            | PHP      ||  28 |    29 | BV          | BOUVET ISLAND                     | PTE      ||  29 |    30 | BW          | BOTSWANA                          | GBP      ||  30 |    31 | BY          | BELARUS                           | ZAR      ||  31 |    32 | BZ          | BELIZE                            | KHR      ||  32 |    33 | CA          | CANADA                            | IDR      ||  33 |    34 | CC          | COCOS (KEELING) IS.S              | SAR      ||  34 |    35 | CF          | CENTRAL AFRICAN REP.              | ATS      ||  35 |    36 | CG          | CONGO                             | SGD      ||  36 |    37 | CH          | SWITZERLAND                       | ESP      ||  37 |    38 | CI          | COTE D IVOIRE                     | SEK      ||  38 |    39 | CK          | COOK ISLANDS                      | CHF      ||  39 |    40 | CL          | CHILE                             | BDT      ||  40 |    41 | CM          | CAMEROON                          | AED      ||  41 |    42 | CN          | CHINA                             | USD      ||  42 |    43 | CO          | COLOMBIA                          | KRW      ||  43 |    44 | CR          | COSTA RICA                        | JPY      ||  44 |    45 | CU          | CUBA                              | CNY      ||  45 |    46 | CV          | CAPE VERDE                        | nan      ||  46 |    47 | CX          | CHRISTMAS ISLAND                  | nan      ||  47 |    48 | CY          | CYPRUS                            | nan      ||  48 |    49 | CZ          | CZECH REPUBLIC                    | nan      ||  49 |    50 | DE          | GERMANY                           | nan      ||  50 |    51 | DJ          | DJIBOUTI                          | nan      ||  51 |    52 | DK          | DENMARK                           | nan      ||  52 |    53 | DM          | DOMINICA                          | nan      ||  53 |    54 | DO          | DOMINICAN REPUBLIC                | nan      ||  54 |    55 | DZ          | ALGERIA                           | nan      ||  55 |    56 | EC          | ECUADOR                           | nan      ||  56 |    57 | EE          | ESTONIA                           | nan      ||  57 |    58 | EG          | EGYPT                             | nan      ||  58 |    59 | EH          | WESTERN SAHARA                    | nan      ||  59 |    60 | ER          | ERITREA                           | nan      ||  60 |    61 | ES          | SPAIN                             | nan      ||  61 |    62 | ET          | ETHIOPIA                          | nan      ||  62 |    63 | FI          | FINLAND                           | nan      ||  63 |    64 | FJ          | FIJI                              | nan      ||  64 |    65 | FK          | FALKLAND ISLANDS (MALVINAS)       | nan      ||  65 |    66 | FM          | MICRONESIA (FEDERATED STATES OF)  | nan      ||  66 |    67 | FO          | FAROE ISLANDS                     | nan      ||  67 |    68 | FR          | FRANCE                            | nan      ||  68 |    69 | FX          | FRANCE, METROPOLITAN              | nan      ||  69 |    70 | GA          | GABON                             | nan      ||  70 |    71 | GB          | UNITED KINGDOM                    | nan      ||  71 |    72 | GD          | GRENADA                           | nan      ||  72 |    73 | GE          | GEORGIA                           | nan      ||  73 |    74 | GF          | FRENCE GUIANA                     | nan      ||  74 |    75 | GH          | GHANA                             | nan      ||  75 |    76 | GI          | GIBRALTAR                         | nan      ||  76 |    77 | GL          | GREENLAND                         | nan      ||  77 |    78 | GM          | GAMBIA                            | nan      ||  78 |    79 | GN          | GUINEA                            | nan      ||  79 |    80 | GP          | GUADELOUPE                        | nan      ||  80 |    81 | GQ          | EQUATORIAL GUINEA                 | nan      ||  81 |    82 | GR          | GREECE                            | nan      ||  82 |    83 | GS          | SOUTH                             | nan      ||  83 |    84 | GT          | GUATEMALA                         | nan      ||  84 |    85 | GU          | GUAM                              | nan      ||  85 |    86 | GW          | GUINEA-BISSAU                     | nan      ||  86 |    87 | GY          | GUYANA                            | nan      ||  87 |    88 | HK          | HONG KONG                         | nan      ||  88 |    89 | HM          | HEARD ISLAND AND MCDONALD ISLANDS | nan      ||  89 |    90 | HN          | HONDURAS                          | nan      ||  90 |    91 | HR          | CROATIA                           | nan      ||  91 |    92 | HT          | HAITI                             | nan      ||  92 |    93 | HU          | HUNGARY                           | nan      ||  93 |    94 | ID          | INDONESIA                         | nan      ||  94 |    95 | IE          | IRELAND                           | nan      ||  95 |    96 | IL          | ISRAEL                            | nan      ||  96 |    97 | IN          | INDIA                             | nan      ||  97 |    98 | IO          | BRITISH INDIAN OCEAN TERRITORY    | nan      ||  98 |    99 | IQ          | IRAQ                              | nan      ||  99 |   100 | IR          | IRAN                              | nan      || 100 |   101 | IS          | ICELAND                           | nan      || 101 |   102 | IT          | ITALY                             | nan      || 102 |   103 | JM          | JAMAICA                           | nan      || 103 |   104 | JO          | JORDAN                            | nan      || 104 |   105 | JP          | JAPAN                             | nan      || 105 |   106 | KE          | KENYA                             | nan      || 106 |   107 | KG          | KYRGYZSTAN                        | nan      || 107 |   108 | KH          | CAMBODIA                          | nan      || 108 |   109 | KI          | KIRIBATI                          | nan      || 109 |   110 | KM          | COMOROS                           | nan      || 110 |   111 | KN          | SAINT KITTS AND NEVIS             | nan      || 111 |   112 | KP          | KOREA                             | nan      || 112 |   113 | KR          | KOREA,REPUBLIC OF                 | nan      || 113 |   114 | KW          | KUWAIT                            | nan      || 114 |   115 | KY          | CAYMAN ISLANDS                    | nan      || 115 |   116 | KZ          | KAZAKHSTAN                        | nan      || 116 |   117 | LA          | LAO REPUBLIC                      | nan      || 117 |   118 | LB          | LEBANON                           | nan      || 118 |   119 | LC          | SAINT LUCIA                       | nan      || 119 |   120 | LI          | LIECHTENSTEIN                     | nan      || 120 |   121 | LK          | SRI LANKA                         | nan      || 121 |   122 | LR          | LIBERIA                           | nan      || 122 |   123 | LS          | LESOTHO                           | nan      || 123 |   124 | LT          | LITHUANIA                         | nan      || 124 |   125 | LU          | LUXEMBOURG                        | nan      || 125 |   126 | LV          | LATVIA                            | nan      || 126 |   127 | LY          | LIBYAN ARAB JAMAHIRIYA            | nan      || 127 |   128 | MA          | MOROCCO                           | nan      || 128 |   129 | MC          | MONACO                            | nan      || 129 |   130 | MD          | MOLDOVA REPUBLIC OF               | nan      || 130 |   131 | MG          | MADAGASCAR                        | nan      || 131 |   132 | MH          | MARSHALL ISLAND                   | nan      || 132 |   133 | MK          | MACEDONIA                         | nan      || 133 |   134 | ML          | MALI                              | nan      || 134 |   135 | MM          | MYANMAR                           | nan      || 135 |   136 | MN          | MONGOLIA                          | nan      || 136 |   137 | MO          | MACAU                             | nan      || 137 |   138 | MP          | NORTHERN MARIANA ISLANDS          | nan      || 138 |   139 | MQ          | MARTINIQUE                        | nan      || 139 |   140 | MR          | MAURITANIA                        | nan      || 140 |   141 | MS          | MONTSERRAT                        | nan      || 141 |   142 | MT          | MALTA                             | nan      || 142 |   143 | MU          | MAURITIUS                         | nan      || 143 |   144 | MV          | MALDIVES                          | nan      || 144 |   145 | MW          | MALAWI                            | nan      || 145 |   146 | MX          | MEXICO                            | nan      || 146 |   147 | MY          | MALAYSIA                          | nan      || 147 |   148 | MZ          | MOZAMBIQUE                        | nan      || 148 |   149 | nan         | NAMIBIA                           | nan      || 149 |   150 | NC          | NEW CALEDONIA                     | nan      || 150 |   151 | NE          | NIGER                             | nan      || 151 |   152 | NF          | NORFOLK ISLAND                    | nan      || 152 |   153 | NG          | NIGERIA                           | nan      || 153 |   154 | NI          | NICARAGUA                         | nan      || 154 |   155 | NL          | NETHERLANDS                       | nan      || 155 |   156 | NO          | NORWAY                            | nan      || 156 |   157 | NP          | NEPAL                             | nan      || 157 |   158 | NR          | NAURU                             | nan      || 158 |   159 | NU          | NIUE                              | nan      || 159 |   160 | NZ          | NEW ZEALAND                       | nan      || 160 |   161 | OM          | OMAN                              | nan      || 161 |   162 | OT          | OTHER COUNTRY                     | nan      || 162 |   163 | PA          | PANAMA                            | nan      || 163 |   164 | PE          | PERU                              | nan      || 164 |   165 | PF          | FRENCH POLYNESIA                  | nan      || 165 |   166 | PG          | PAPUA NEW GUINEA                  | nan      || 166 |   167 | PH          | PHILIPPINES                       | nan      || 167 |   168 | PK          | PAKISTAN                          | nan      || 168 |   169 | PL          | POLAND                            | nan      || 169 |   170 | PM          | SAINT PIERRE AND MIQUELON         | nan      || 170 |   171 | PN          | PITCAIRN                          | nan      || 171 |   172 | PR          | PUERTO RICO                       | nan      || 172 |   173 | PT          | PORTUGAL                          | nan      || 173 |   174 | PW          | PALAU                             | nan      || 174 |   175 | PY          | PARAGUAY                          | nan      || 175 |   176 | QA          | QATAR                             | nan      || 176 |   177 | RE          | REUNION                           | nan      || 177 |   178 | RO          | ROMANIA                           | nan      || 178 |   179 | RU          | RUSSIAN FEDERATION                | nan      || 179 |   180 | RW          | RWANDA                            | nan      || 180 |   181 | SA          | SAUDI ARABIA                      | nan      || 181 |   182 | SB          | SOLOMON ISLANDS                   | nan      || 182 |   183 | SC          | SEYCHELLES                        | nan      || 183 |   184 | SD          | SUDAN                             | nan      || 184 |   185 | SE          | SWEDEN                            | nan      || 185 |   186 | SG          | SINGAPORE                         | nan      || 186 |   187 | SH          | SAINT HELENA                      | nan      || 187 |   188 | SI          | SLOVENIA                          | nan      || 188 |   189 | SJ          | SVALBARD AND JAN MAYEN            | nan      || 189 |   190 | SK          | SLOVAKIA                          | nan      || 190 |   191 | SL          | SIERRA LEONE                      | nan      || 191 |   192 | SM          | SAN MARINO                        | nan      || 192 |   193 | SN          | SENEGAL                           | nan      || 193 |   194 | SO          | SOMALIA                           | nan      || 194 |   195 | SR          | SURINAME                          | nan      || 195 |   196 | ST          | SAO TOME AND PRINCIPE             | nan      || 196 |   197 | SV          | EL SALVADOR                       | nan      || 197 |   198 | SY          | SYRIAN ARAB REPUBLIC              | nan      || 198 |   199 | SZ          | SWAZILAND                         | nan      || 199 |   200 | TC          | TURKS AND CAICOS ISLANDS          | nan      || 200 |   201 | TD          | CHAD                              | nan      || 201 |   202 | TF          | FRENCH SOUTHERN TERRITORIES       | nan      || 202 |   203 | TG          | TOGO                              | nan      || 203 |   204 | TH          | THAILAND                          | nan      || 204 |   205 | TJ          | TAJIKISTAN                        | nan      || 205 |   206 | TK          | TOKELAU                           | nan      || 206 |   207 | TM          | TURKMENISTAN                      | nan      || 207 |   208 | TN          | TUNISIA                           | nan      || 208 |   209 | TO          | TONGA                             | nan      || 209 |   210 | TP          | EAST TIMOR                        | nan      || 210 |   211 | TR          | TURKEY                            | nan      || 211 |   212 | TT          | TRINIDAD AND TOBAGO               | nan      || 212 |   213 | TV          | TUVALU                            | nan      || 213 |   214 | TW          | TAIWAN PROVINCE OF CHINA          | nan      || 214 |   215 | TZ          | TANZANIA UNITED REPUBLIC OF       | nan      || 215 |   216 | UA          | UKRAINE                           | nan      || 216 |   217 | UG          | UGANDA                            | nan      || 217 |   218 | UM          | UNITED STATES MINOR               | nan      || 218 |   219 | US          | UNITED STATES                     | nan      || 219 |   220 | UY          | URUGUAY                           | nan      || 220 |   221 | UZ          | UZBEKISTAN                        | nan      || 221 |   222 | VA          | VATICAN CITY                      | nan      || 222 |   223 | VC          | SAINT VINCENT AND THE GRENADINES  | nan      || 223 |   224 | VE          | VENEZUELA                         | nan      || 224 |   225 | VG          | VIRGIN ISLANDS (BRITISH)          | nan      || 225 |   226 | VI          | VIRGIN ISLANDS (U.S.)             | nan      || 226 |   227 | VN          | VIETNAM                           | nan      || 227 |   228 | VU          | VANUATU                           | nan      || 228 |   229 | WF          | WALLIS AND FUTUNA ISLANDS         | nan      || 229 |   230 | WS          | SAMOA                             | nan      || 230 |   231 | YE          | YEMEN                             | nan      || 231 |   232 | YT          | MAYOTTE                           | nan      || 232 |   233 | YU          | YUGOSLAVIA                        | nan      || 233 |   234 | ZA          | SOUTH AFRICA                      | nan      || 234 |   235 | ZM          | ZAMBIA                            | nan      || 235 |   236 | ZR          | ZAIRE                             | nan      || 236 |   237 | ZW          | ZIMBABWE                          | nan      |
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE2MzkwNjIyMzIsNzE5MzIxMjg0LC0xNz
MzMjcxMDUyLDEwNTE1MTk0NTcsOTA3OTM0OTc2XX0=
-->