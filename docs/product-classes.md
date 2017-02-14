---
---


##Introduction
The IFC format is a language whose vocabulary is formed by main classes IfcProduct designed to qualify the physical objects of a model. If the business software generally classify automatically the basic objects, there are variations of the same class, through PredefinedType, to refine the qualification.

For example, the class IfcSlabused for a slab, can also qualify with a raft type IfcSlab BASESLAB, a stair landing with the type IfcSlab LANDING, or a roof deck slab with the type IfcSlab ROOF.

The same variation is also present in IfcTypeProductthat group of several objects of the same type properties. For example, 5 poles identical with the class IfcColumnwill be grouped in one type IfcColumnType.

The PredefinedTypecan be attributed to the level IfcProductor IfcTypeProductas shown in the tables below, but they are not necessarily consistent between the two levels. IFC4 should largely correct these inconsistencies.

This page is intended to make known the richness of this IFC classification, by first translating the classes and their types into French, as well as giving the most appropriate tools to use in the main modeling software (Allplan, Archicad and Revit).

<ul class="nav nav-tabs" id="myTab" role="tablist">
  <li class="nav-item">
    <a class="nav-link active" data-toggle="tab" href="#domaine_architectural" role="tab" aria-controls="domaine_architectural" rel="nofollow">Domaine Architectural (IFC2x3-TC1)</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" data-toggle="tab" href="#domaine_structurel" role="tab" aria-controls="domaine_structurel" rel="nofollow">Domaine Structurel (IFC2x3-TC1)</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" data-toggle="tab" href="#domaine_fluides" role="tab" aria-controls="domaine_fluides" rel="nofollow">Domaine Fluides (IFC2x3-TC1)</a>
  </li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="domaine_architectural" role="tabpanel">
    <div id="table-domaine-architectural" class="table-responsive">
      <table class="table table-sm table-hover">
        <div class="form-group">
          <div class="input-group">
            <div class="input-group-addon"><i class="fa fa-search"></i></div>
            <input class="search fuzzy-search form-control" id="test" placeholder="Rechercher dans la liste..." />
          </div>
        </div>
        <thead>
          <tr>
            <th>Terme français</th>
            <th>Terme anglais</th>
            <th>IfcProduct + PredefinedType</th>
            <th>IfcTypeProduct + PredefinedType</th>
            <th>Outil Allplan</th>
            <th>Outil Archicad</th>
            <th>Outil Revit</th>
          </tr>
        </thead>
        <tbody class="list">
          {% for object in site.data.ifc-objets %}
            {% if object.domaine_architecture == true %}
            <tr>
              <td class="fr_fr"><b>{{ object.nom_fr_fr }}</b></td>
              <td class="en_gb">
                {% if object.nom_en_gb != null %}
                  <a href="https://www.google.fr/search?q={{ object.nom_en_gb | downcase }}" target="_blank" data-proofer-ignore><i class="fa fa-search"></i></a>
                  <a href="https://translate.google.com/#en/fr/{{ object.nom_en_gb | downcase }}" target="_blank" data-proofer-ignore><i class="fa fa-globe"></i></a>
                {% endif %}
                {{ object.nom_en_gb }}
              </td>
              <td class="ifcproduct">
                {% if object.ifcproduct_ifc2x3tc1 != null %}
                  <a href="https://www.google.fr/search?q={{ object.ifcproduct_ifc2x3tc1 | downcase }}" target="_blank"><i class="fa fa-search" data-proofer-ignore></i></a>
                {% endif %}
                {{ object.ifcproduct_ifc2x3tc1 }}
              </td>
              <td class="ifctypeproduct">
                {% if object.ifctypeproduct_ifc2x3tc1 != null %}
                  <a href="https://www.google.fr/search?q={{ object.ifctypeproduct_ifc2x3tc1 | downcase }}" target="_blank" data-proofer-ignore><i class="fa fa-search"></i></a>
                {% endif %}
                {{ object.ifctypeproduct_ifc2x3tc1 }}
              </td>
              <td class="outil_allplan">{{ object.allplan }}</td>
              <td class="outil_archicad">{{ object.archicad }}</td>
              <td class="outil_revit">{{ object.revit }}</td>
            </tr>
            {% endif %}
          {% endfor %}
        </tbody>
      </table>
    </div>
  </div>
  <div class="tab-pane" id="domaine_structurel" role="tabpanel">
    <div id="table-domaine-structurel" class="table-responsive">
      <table class="table table-sm table-hover">
        <div class="form-group">
          <div class="input-group">
            <div class="input-group-addon"><i class="fa fa-search"></i></div>
            <input class="search fuzzy-search form-control" id="test" placeholder="Rechercher dans la liste..." />
          </div>
        </div>
        <thead>
          <tr>
            <th>Terme français</th>
            <th>Terme anglais</th>
            <th>IfcProduct + PredefinedType</th>
            <th>IfcTypeProduct + PredefinedType</th>
            <th>Outil Allplan</th>
            <th>Outil Archicad</th>
            <th>Outil Revit</th>
          </tr>
        </thead>
        <tbody class="list">
          {% for object in site.data.ifc-objets %}
            {% if object.domaine_structure == true %}
            <tr>
              <td class="fr_fr"><b>{{ object.nom_fr_fr }}</b></td>
              <td class="en_gb">
                {% if object.nom_en_gb != null %}
                  <a href="https://www.google.fr/search?q={{ object.nom_en_gb | downcase }}" target="_blank" data-proofer-ignore><i class="fa fa-search"></i></a>
                  <a href="https://translate.google.com/#en/fr/{{ object.nom_en_gb | downcase }}" target="_blank" data-proofer-ignore><i class="fa fa-globe"></i></a>
                {% endif %}
                {{ object.nom_en_gb }}
              </td>
              <td class="ifcproduct">
                {% if object.ifcproduct_ifc2x3tc1 != null %}
                  <a href="https://www.google.fr/search?q={{ object.ifcproduct_ifc2x3tc1 | downcase }}" target="_blank" data-proofer-ignore><i class="fa fa-search"></i></a>
                {% endif %}
                {{ object.ifcproduct_ifc2x3tc1 }}
              </td>
              <td class="ifctypeproduct">
                {% if object.ifctypeproduct_ifc2x3tc1 != null %}
                  <a href="https://www.google.fr/search?q={{ object.ifctypeproduct_ifc2x3tc1 | downcase }}" target="_blank" data-proofer-ignore><i class="fa fa-search"></i></a>
                {% endif %}
                {{ object.ifctypeproduct_ifc2x3tc1 }}
              </td>
              <td class="outil_allplan">{{ object.allplan }}</td>
              <td class="outil_archicad">{{ object.archicad }}</td>
              <td class="outil_revit">{{ object.revit }}</td>
            </tr>
            {% endif %}
          {% endfor %}
        </tbody>
      </table>
    </div>
  </div>
  <div class="tab-pane" id="domaine_fluides" role="tabpanel">
    <div id="table-domaine-fluides" class="table-responsive">
      <table class="table table-sm table-hover">
        <div class="form-group">
          <div class="input-group">
            <div class="input-group-addon"><i class="fa fa-search"></i></div>
            <input class="search fuzzy-search form-control" id="test" placeholder="Rechercher dans la liste..." />
          </div>
        </div>
        <thead>
          <tr>
            <th>Terme français</th>
            <th>Terme anglais</th>
            <th>IfcProduct + PredefinedType</th>
            <th>IfcTypeProduct + PredefinedType</th>
            <th>Outil Allplan</th>
            <th>Outil Archicad</th>
            <th>Outil Revit</th>
          </tr>
        </thead>
        <tbody class="list">
          {% for object in site.data.ifc-objets %}
            {% if object.domaine_fluides == true %}
            <tr>
              <td class="fr_fr"><b>{{ object.nom_fr_fr }}</b></td>
              <td class="en_gb">
                {% if object.nom_en_gb != null %}
                  <a href="https://www.google.fr/search?q={{ object.nom_en_gb | downcase }}" target="_blank" data-proofer-ignore><i class="fa fa-search"></i></a>
                  <a href="https://translate.google.com/#en/fr/{{ object.nom_en_gb | downcase }}" target="_blank" data-proofer-ignore><i class="fa fa-globe"></i></a>
                {% endif %}
                {{ object.nom_en_gb }}
              </td>
              <td class="ifcproduct">
                {% if object.ifcproduct_ifc2x3tc1 != null %}
                  <a href="https://www.google.fr/search?q={{ object.ifcproduct_ifc2x3tc1 | downcase }}" target="_blank" data-proofer-ignore><i class="fa fa-search"></i></a>
                {% endif %}
                {{ object.ifcproduct_ifc2x3tc1 }}
              </td>
              <td class="ifctypeproduct">
                {% if object.ifctypeproduct_ifc2x3tc1 != null %}
                  <a href="https://www.google.fr/search?q={{ object.ifctypeproduct_ifc2x3tc1 | downcase }}" target="_blank" data-proofer-ignore><i class="fa fa-search"></i></a>
                {% endif %}
                {{ object.ifctypeproduct_ifc2x3tc1 }}
              </td>
              <td class="outil_allplan">{{ object.allplan }}</td>
              <td class="outil_archicad">{{ object.archicad }}</td>
              <td class="outil_revit">{{ object.revit }}</td>
            </tr>
            {% endif %}
          {% endfor %}
        </tbody>
      </table>
    </div>
  </div>
</div>
