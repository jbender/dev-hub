---
title: Gallery
overview: Gallery
---

<ul class="toolbar">
    <li>{"<a href="json/gallery.json" title="JSON" target="_blank">JSON</a>"}</li>
</ul>
<h2>Gallery</h2>
<p>Here are some examples of what is possible with developer around APIs and data. This gallery is not limited to web and mobile applications, but also contain visualizations, spreadsheet integrations and much more.</p>

<!-- Begin List Code Samples -->
{% raw  %}
<script id="galleryListingTemplate" type="text/template">
    <tr>
        <td width="25%" align="center">
           <img src="{{Screenshot}}" width="150" align="center" style="padding: 15px;" />
        </td>
        <td width="75%">
           <table cellpadding="3" width="100%">
               <tr>
                    <td><strong>{{Name}}</strong></td>
               </tr>
               <tr>
                    <td>({{Language}})</td>
               </tr>
               <tr>
                    <td><a href="{{URL}}" target="_blank">{{URL}}</a></td>
               </tr>
               <tr>
                    <td>{{Description}}</td>
               </tr>
           </table>
        </td>
    </tr>
</script>
{% endraw %}

<div style="">
     <table id="galleryListing" border="0" width="90%" align="left" cellpadding="5" cellspacing="5"></table>
</div>

<script type="text/javascript">
function listGallery()
    {
    $.getJSON('json/gallery.json', function(data) {
        toggle = 0;
         $.each(data['Gallery'], function(key, val) {
            var template = $('#galleryListingTemplate').html();
            var html = Mustache.to_html(template, val);
            $('#galleryListing').append(html);
            });
        });
    }
listGallery();
</script>
<!-- End List Code Simples -->
