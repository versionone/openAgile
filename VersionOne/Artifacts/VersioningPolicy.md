## Versioning Policy

In order to provide a more constent way to version the products that the openAgile team creates, we will adopt a [software versioning policy](http://en.wikipedia.org/wiki/Software_versioning) that makes our versioning not only consistent, but meaningful. This is especially important for our integrations as VersionOne support often asks customers the build numbers of the integrations that they are using.


### Versioning Semantics

<table border="1" width="100%">
	<tr>
		<th>Name</th>
		<th>Example</th>
		<th>Description</th>
	</tr>
	<tr>
		<td>MAJOR</td>
		<td><b>1</b>.2.3.444</td>
		<td>Incremented for incompatible and breaking changes.</td>
	</tr>
	<tr>
		<td>MINOR</td>
		<td>1.<b>2</b>.3.444</td>
		<td>Incremented for new features that maintain backwards compatability.</td>
	</tr>
	<tr>
		<td>PATCH</td>
		<td>1.2.<b>3</b>.444</td>
		<td>Incremented for bug fixes that maintain backwards compatability.</td>
	</tr>
	<tr>
		<td>BUILD</td>
		<td>1.2.3.<b>444</b></td>
		<td>Incremented for every new build.</td>
	</tr>
</table>


### Links

* [Semantic Versioning](http://semver.org/)
* [Best Practices for .NET Assembly Versioning](http://blogs.msdn.com/b/jjameson/archive/2009/04/03/best-practices-for-net-assembly-versioning.aspx)
