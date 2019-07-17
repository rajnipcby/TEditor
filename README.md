# TEditor
HTML EDITOR - Free to use in any website.

Here is the code to put it in your web page to load TEditor.

----------------------------------------------------

<!DOCTYPE html>
<html>
<head>
    <meta name="viewport" content="width=device-width" />
    <title>TEditor - Editor for your web page</title>
    <script src="http://teditor.rajnipadhiyar.com/Content/TEditor/scripts/jquery.js"></script>
    <script src="http://teditor.rajnipadhiyar.com/content/teditor/ClientTEditor_Upload.js"></script>
</head>
<body>
    <div id="dvEditor" style="width:900;height:500px;"></div>
    <br />
    <input type="button" value="Preview Data" onclick="return getData();" />
	<input type="button" value="Set Data" onclick="return setData();" />
    <div id="dvPreview"></div>
</body>
</html>
<script>
    $(document).ready(function () {
        LoadTEditorV2('dvEditor');

    });
    function getData() {
        GetTEditorData('dvEditor').then(function (result) {
            $('#dvPreview').html(result);
            return false;
        });
    }
	function setData() {
        SetTEditorData('dvEditor','<h1>Hello World</h1>');
            return false;
    }
</script>
