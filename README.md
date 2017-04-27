# AVR_CryptoLib
The AVRCryptoLib for the GNU C compiler. It contains DES Triple DES and RSA Encrypt and Decrypt for both Keys in Ram or Flash Also AES, Skipjack, MD5 and SHA-1 Documentation and Source code is included and some test programs. The interfacing to function is in C but all the main functions are in assembly language for speed and size
 The DES will do a decryption in 8.3ms @16Mc Mega Core.<br>
 And 512^3 RSA in 69ms @16mc on a Mega core 512^512 in 26 sec.<br>
 For 512^3 RSA you will need 4 * Keysize of ram and for 512^512 you will need 5
 the Keysize.<br>
 </p>

 <p>This is the table of all the cycles&nbsp;
 </p>
<table border=1>
	<tr>
		<td>DES <td><td>Cycles<td>Code size<td>Ram needed
	<tr>
	<td><td>Encrypt<td>133966<td>1782 bytes<td>122+24 bytes
	<tr>
	<td><td>Decrypt<td>134134<td>1780 bytes<td>122+24 bytes
	<tr>
	<td><td>Combined<td><td>2082 bytes<td>122+24 bytes
	<tr>
		<td>Triple Des <td><td>Cycles<td>Code size<td>Ram needed
	<tr>
	<td><td>Encrypt<td>402568<td>1974 bytes<td>122+32 bytes
	<tr>
	<td><td>Decrypt<td>402688<td>1974 bytes<td>122+32 bytes
	<tr>
	<td><td>Combined<td><td>2390 bytes<td>122+32 bytes
	<tr>
		<td>RSA 64 bits Key in Ram<td><td>Cycles<td>Code size<td>Ram needed
	<tr>
	<td><td>Encrypt<td>1051026<td>760 bytes<td>5 * Keysize bytes
	<tr>
	<td><td>Decrypt<td>22946<td>690 bytes<td>4 * Keysize bytes
	<tr>
	<td><td>Conbined<td><td>1040 bytes<td>5 * Keysize bytes
	<tr>	
		<td>RSA 64 Key in Flash<td><td>Cycles<td>Code size<td>Ram needed
	<tr>
	<td><td>Encrypt<td>1118827<td>746 bytes<td>4 * Keysize bytes
	<tr>
	<td><td>Decrypt<td>24660<td>692 bytes<td>3 * Keysize bytes
	<tr>
	<td><td>Combined<td>-<td>1028 bytes<td>4 * Keysize bytes
	<tr>
		<td>AES 128 SF<td><td>Cycles<td>Code size<td>Ram needed
	<tr>
	<td><td>Init<td>25389
	<tr>
	<td><td>Encrypt<td>7622<td>900 bytes<td>768+16 bytes
	<tr>
	<td><td>Decrypt<td>8279<td>904 bytes<td>768+16 bytes
	<tr>
	<td><td>Combined<td><td>1302 bytes<td>768+16 bytes
	<tr>
		<td>AES 128 SR<td><td>Cycles<td>Code size<td>Ram needed
	<tr>
	<td><td>Init<td>5534
	<tr>
	<td><td>Encrypt<td>7762<td>966 bytes<td>256+16 bytes
	<tr>
	<td><td>Decrypt<td>8411<td>1222 bytes<td>256+16 bytes
	<tr>
	<td><td>Combined<td><td>1620 bytes<td>256+16 bytes
	<tr>
		<td>SkipJack<td><td>Cycles<td>Code size<td>Ram needed
	<tr>
	<td><td>Encrypt<td>5777<td>526 bytes<td>18 bytes
	<tr>
	<td><td>Decrypt<td>5727<td>520 bytes<td>18 bytes
	<tr>
	<td><td>Combined<td>-<td>790 bytes<td>18 bytes
   	<tr>
		<td>MD5<td><td>Cycles<td>Code size<td>Ram needed
	<tr>
	<td><td>Block 1KBytes<td>339501<td>1842 bytes<td>113 bytes
	<tr>
		<td>SHA-1<td><td>Cycles<td>Code size<td>Ram needed
	<tr>
	<td><td>Block 1KBytes<td>489890<td>1640 bytes<td>120 bytes
</table>
