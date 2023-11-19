# Dagger
for creating and operating an object of a DAG hierarchy in a DCC tool.

# Examples
![dagTest1](https://i.gyazo.com/6cc2d8ca52f43921c927b111132aaac6.png "dagTest1")

```python
import dagger.dagger as dagger
dagTest = dagger.DAGstructure("dagTest")

# register dag top dag node "top_gp"
dagTest.construct("top_gp")

# print out to console
dagTest.printout()

>>> top_gp
        test_gpA
            test_gpB
                test_gpC
                    test_jntA
                test_gpD
                    test_jntB


# export as .xml file
dagTest.export_xml("D:/test")
```

```xml
<?xml version="1.0" encoding="utf-8"?>
<dagStructure>
	<node fullpath="|top_gp" name="top_gp">
		<option name="translate" type="list" value="[(0.0, 0.0, 0.0)]"/>
		<option name="rotate" type="list" value="[(0.0, 0.0, 0.0)]"/>
		<option name="scale" type="list" value="[(1.0, 1.0, 1.0)]"/>
		<option name="pivot" type="list" value="[0.0, 0.0, 0.0, 0.0, 0.0, 0.0]"/>
		<option name="visibility" type="bool" value="True"/>
		<option name="shapes" type="list" value="[]"/>
		<option name="nodeType" type="str" value="transform"/>
		<option name="uuid" type="str" value="09B40825-4077-8088-ED58-62BA21AD3738"/>
		<node fullpath="|top_gp|test_gpA" name="test_gpA">
			<option name="translate" type="list" value="[(0.0, 0.0, 0.0)]"/>
			<option name="rotate" type="list" value="[(0.0, 0.0, 0.0)]"/>
			<option name="scale" type="list" value="[(1.0, 1.0, 1.0)]"/>
			<option name="pivot" type="list" value="[0.0, 0.0, 0.0, 0.0, 0.0, 0.0]"/>
			<option name="visibility" type="bool" value="True"/>
			<option name="shapes" type="list" value="[]"/>
			<option name="nodeType" type="str" value="transform"/>
			<option name="uuid" type="str" value="35643224-430E-CFCC-FF98-2A96299B1743"/>
			<node fullpath="|top_gp|test_gpA|test_gpB" name="test_gpB">
				<option name="translate" type="list" value="[(0.0, 0.0, 0.0)]"/>
				<option name="rotate" type="list" value="[(0.0, 0.0, 0.0)]"/>
				<option name="scale" type="list" value="[(1.0, 1.0, 1.0)]"/>
				<option name="pivot" type="list" value="[0.0, 0.0, 0.0, 0.0, 0.0, 0.0]"/>
				<option name="visibility" type="bool" value="True"/>
				<option name="shapes" type="list" value="[]"/>
				<option name="nodeType" type="str" value="transform"/>
				<option name="uuid" type="str" value="8D3EB138-46EB-5468-9988-DE9CDE637C22"/>
				<node fullpath="|top_gp|test_gpA|test_gpB|test_gpC" name="test_gpC">
					<option name="translate" type="list" value="[(0.0, 0.0, 0.0)]"/>
					<option name="rotate" type="list" value="[(0.0, 0.0, 0.0)]"/>
					<option name="scale" type="list" value="[(1.0, 1.0, 1.0)]"/>
					<option name="pivot" type="list" value="[0.0, 0.0, 0.0, 0.0, 0.0, 0.0]"/>
					<option name="visibility" type="bool" value="True"/>
					<option name="shapes" type="list" value="[]"/>
					<option name="nodeType" type="str" value="transform"/>
					<option name="uuid" type="str" value="953D585E-49EA-5477-C305-DD92147386EB"/>
					<node fullpath="|top_gp|test_gpA|test_gpB|test_gpC|test_jntA" name="test_jntA">
						<option name="translate" type="list" value="[(0.0, 0.0, 0.0)]"/>
						<option name="rotate" type="list" value="[(0.0, 0.0, 0.0)]"/>
						<option name="scale" type="list" value="[(1.0, 1.0, 1.0)]"/>
						<option name="pivot" type="list" value="[0.0, 0.0, 0.0, 0.0, 0.0, 0.0]"/>
						<option name="visibility" type="bool" value="True"/>
						<option name="shapes" type="list" value="[]"/>
						<option name="nodeType" type="str" value="joint"/>
						<option name="uuid" type="str" value="A2CFFA37-4E18-1EE9-66F6-3592229322D5"/>
					</node>
				</node>
				<node fullpath="|top_gp|test_gpA|test_gpB|test_gpD" name="test_gpD">
					<option name="translate" type="list" value="[(0.0, 0.0, 0.0)]"/>
					<option name="rotate" type="list" value="[(0.0, 0.0, 0.0)]"/>
					<option name="scale" type="list" value="[(1.0, 1.0, 1.0)]"/>
					<option name="pivot" type="list" value="[0.0, 0.0, 0.0, 0.0, 0.0, 0.0]"/>
					<option name="visibility" type="bool" value="True"/>
					<option name="shapes" type="list" value="[]"/>
					<option name="nodeType" type="str" value="transform"/>
					<option name="uuid" type="str" value="83D090BD-480A-633E-66CB-9C8E7BAD5810"/>
					<node fullpath="|top_gp|test_gpA|test_gpB|test_gpD|test_jntB" name="test_jntB">
						<option name="translate" type="list" value="[(0.0, 0.0, 0.0)]"/>
						<option name="rotate" type="list" value="[(0.0, 0.0, 0.0)]"/>
						<option name="scale" type="list" value="[(1.0, 1.0, 1.0)]"/>
						<option name="pivot" type="list" value="[0.0, 0.0, 0.0, 0.0, 0.0, 0.0]"/>
						<option name="visibility" type="bool" value="True"/>
						<option name="shapes" type="list" value="[]"/>
						<option name="nodeType" type="str" value="joint"/>
						<option name="uuid" type="str" value="2023B36F-41BF-9705-4646-CA959054F262"/>
					</node>
				</node>
			</node>
		</node>
	</node>
</dagStructure>

```

```python
# import from .xml file
dagTest = dagTest.DAGstructure.import_xml("D:/test/dagTest_dagInfo.xml")
# build dag struture
dagTest.build()
dagTest.printout()
>>> top_gp
        test_gpA
            test_gpB
                test_gpC
                    test_jntA
                test_gpD
                    test_jntB

# restore attribute
dagTest.restore_attributes(attrs=['visibility'])

```

## Plans

- Add GUI
- Change to be independent of DCC tools
- Support for .json
