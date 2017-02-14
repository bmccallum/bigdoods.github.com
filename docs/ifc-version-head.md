---
---

Since the version IFC1.0 in 1997, buildingSMART continuously develops and improves this major standard. The IFC4-Add1, the latest official version, is not yet fully supported by the various business software; So the IFC2x3-TC1 remains the current standard. It is hoped that IFC4 trade will become fully operational in 2016.

<div class="table-responsive">
  <table class="table table-sm table-hover">
    <thead>
      <tr>
        <th>Version</th>
        <th>Date of publication</th>
        <th>Documentation</th>
      </tr>
    </thead>
    <tbody>
      {% for version in site.data.ifc-versions %}
      <tr {% if version.actuelle == "oui" %}class="table-success"{% endif %}>
        <td><b>{{ version.version }}</b></td>
        <td>{{ version.date }}</td>
        <td>
          {% if version.url_doc != nil %}
          <a href="{{ version.url_doc }}" target="_blank">Documentation</a>
          {% endif %}
        </td>
      </tr>
      {% endfor %}
    </tbody>
  </table>
</div>
