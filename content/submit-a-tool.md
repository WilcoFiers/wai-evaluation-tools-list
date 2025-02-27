---
title: "Submit a tool - Web Accessibility Evaluation Tools List"
nav_title: "Submit a tool - Web Accessibility Evaluation Tools List"
doc-note-type: draft
lang: en   
last_updated: 2021-@@-@@
github:
  repository: w3c/wai-evaluation-tools-list
  path: content/submit-a-tool.md
permalink: list-of-evaluation-tools/submit-a-tool
ref: /teach-advocate/evaluation-tools-list/
changelog: /teach-advocate/evaluation-tools-list/changelog/
acknowledgements: /teach-advocate/evaluation-tools-list/acknowledgements/
description:  # NEW: add a 150ish-character-description for social media   # translate the description
# image: /content-images/wai-evaluation-tools-list/social.png  # NEW: image for social media (leave commented out if we don't have a specific one for this reource)
footer: 
   <p><strong>Date:</strong> <!-- Updated @@ Month 2021.--> First published Month 20@@. CHANGELOG.</p>
   <p><strong>Editors:</strong> @@name, @@name. <strong>Contributors:</strong> @@name, @@name, and <a href="https://www.w3.org/groups/wg/eowg/participants">participants of the EOWG</a>. ACKNOWLEDGEMENTS lists contributors and credits.</p>
   <p>Developed by the Accessibility Education and Outreach Working Group (<a href="http://www.w3.org/WAI/EO/">EOWG</a>). Developed as part of the <a href="https://www.w3.org/WAI/about/projects/wai-coop/">WAI-CooP project</a>, co-funded by the European Commission.</p>
---
<!-- markdownlint-disable no-inline-html -->

<div style="grid-column: 4 / span 4">

<style>
{% include css/styles.css %}
main > header { grid-column: 4 / span 4; }
</style>

<div class="submission-header">
  <a href="../list-of-evaluation-tools/" class="backtolist">{% include_cached icon.html name="arrow-left" %}Back to List of Evaluation Tools</a>
  <p>
    This form allows you to provide information on your organization’s Tool for Web Accessibility Evaluation to be listed on the WAI website. Information submitted will also be publicly available in GitHub.
  </p>
  <p>
    When you submit the form, we will strive to review and publish your submission within 2-4 weeks depending on the content. You will receive an email when we have reviewed your submission.
  </p>
  <p>
    If you have questions, want to update information in the list or delete a tool please send an e-mail to: <a href="mailto:group-wai-list-eval-tools@w3.org">group-wai-list-eval-tools@w3.org</a> 
  </p>
  <p>
    <i>Please note that W3C does not endorse specific providers. Resources are listed with no quality rating.</i>
  </p>
  
</div>

{%- include list-submission-form.liquid type="start"
                                   name="submission"
                                   version="1"
                                   success="/success.html"
                                   failure="/failure.html"
                                   repository="wai-evaluation-tools-list" -%}


<div class="submission-form">
  <h2 id="general-information"><span>1/3</span>General information</h2>

  <div class="field">
      <label for="title" class="label-input">Tool name<span>(Required)</span></label>
      <input type="text" id="title" name="title" required>
  </div>
  <div class="field">
      <label for="website" class="label-input">Web address (URL)<span>(Required)</span></label>
      <input type="url" id="website" name="website" required>
  </div>
  <div class="field">
      <label for="provider" class="label-input">Vendor / organization<span>(Required)</span></label>
      <input type="text" id="provider" name="provider" required>
  </div>
  <div class="field">
      <label for="contact" class="label-input">Email address<span>(Required)</span></label>
      <input type="email" id="contact" name="contact" required>
      <p class="subfieldtext"> 
        The list maintainer may use this e-mail address solely to contact you in case of questions about this submission.  For this purpose, it will be published in <a href="https://github.com/w3c/wai-evaluation-tools-list/pulls" target="_blank">Github</a>, where your submission will be processed. The e-mail address will never be displayed in the tool list.
      </p>
  </div>
  <div class="field">
      <label for="release" class="label-input">Release date<span>(Required)</span></label>
      <input type="date" id="release" name="release" required>
  </div>
  <div class="field" style="display: none;">
      <label for="update" class="label-input">Date of most recent update<span>(Required)</span></label>
      <input type="date" id="update" name="update" required>
  </div>
  <div class="field">
      <label for="a11yloc" class="label-input">Accessibility statement (URL)</label>
      <input type="url" id="a11yloc" name="a11yloc">
      <p class="subfieldtext"> 
        While an accessibility statement is not required to submit a tool, it provides valuable information on your commitment to accessibility to your (potential) users. Get started by visiting <a href="https://www.w3.org/WAI/planning/statements/" target="_blank">Developing an Accessibility Statement</a>.
      </p>
  </div>
  <div class="field">
    <label for="actrules" class="label-input">ACT Rules (URL)</label>
    <input type="url" id="actrules" name="actrules">
    <p class="subfieldtext">
      Tool vendors can describe if and how their tool(s) support the Accessibility Conformance Testing Rules. If there is a report about the implementation of the rules, the details section of the tool in the Web Accessibility Evaluation Tools List will provide a link to the report. For more information, read <a href="https://www.w3.org/WAI/standards-guidelines/act/implementations/" target="_blank">ACT Rules Implementation in Test Tools and Methodologies</a>.
    </p>
  </div>

  <h2 id="tool-functionality"><span>2/3</span>Tool functionality</h2>

  <div class="field" id="features">
    <label class="label specialField">Short product description (max. 350)<span>(Required)</span></label>
    <p>Add a description of key features and functionalities of the tool. Try to write this description in a way that tool users can understand.</p>
    <textarea id="features" name="features" rows="5" maxlength="350"></textarea>
<!--     <div class="line">
      <label for="tool-feature_1" class="label-input"></label>
      <input type="text" name="features[]" id="feature_1" class="select-form" required>
    </div>
    <div class="proto">
      <label for="tool-feature_[n]" class="label-input"></label>
      <input type="text" name="features[]" id="feature_[n]" class="select-form" disabled> 
      <button aria-label="Remove feature" type="button" class="remove_line">Remove</button>
    </div>
    <button type="button" class="add_line small">Add feature</button> -->
    <!-- <button type="button" class="remove_line small" disabled>Remove last feature</button> -->
  </div>
  {% assign purpose = site.data.filters | find: "id", "purpose" %}
  <fieldset class="field" id="purpose">
      <div class="fieldheader">
        <legend for="tool-purpose" class="label-input">Purpose<span class="short-sub">(Required)</span></legend>
      </div>
      <p>What type of evaluations does this tool support?</p>
      <div class="field-group">
        {% for option in purpose.options %}
          <div class="radio-field">
            <input type="checkbox" name="purpose[]" id="tool-purpose-{{ option.id }}" value="{{ option.name }}" group="purpose" required>
            <label for="tool-purpose-{{ option.id }}">{{ option.name }}</label>
            {% if option.info %}
              <abbr title="{{ option.info }}" class="toggletip-container">
                  <img alt="{{ option.info }}" tabindex="0" data-toggletip-content="{{ option.info }}" src="/content-images/wai-evaluation-tools-list/info.png" />
                  <span class="toggletip-span-inline" role="status"></span>
              </abbr>
            {% endif %}
          </div>
        {% endfor %}
      </div>
  </fieldset>
  {% assign product = site.data.filters | find: "id", "product" %}
  <fieldset class="field" id="product">
      <div class="fieldheader">
        <legend for="tool-product" class="label-input">Product to evaluate<span class="short-sub">(Required)</span></legend>
        {% if product.info %}
          <abbr title="{{ product.info }}" class="toggletip-container">
              <img alt="{{ product.info }}" tabindex="0" data-toggletip-content="{{ product.info }}" src="/content-images/wai-evaluation-tools-list/info.png" />
              <span class="toggletip-span" role="status"></span>
          </abbr>
        {% endif %}
      </div>
      <div class="field-group">
        {% for option in product.options %}
          <div class="radio-field">
            <input type="checkbox" name="product[]" id="tool-product-{{ option.id }}" value="{{ option.name }}" group="product" required>
            <label for="tool-product-{{ option.id }}">{{ option.name }}</label>
            {% if option.info %}
              <abbr title="{{ option.info }}" class="toggletip-container">
                  <img alt="{{ option.info }}" tabindex="0" data-toggletip-content="{{ option.info }}" src="/content-images/wai-evaluation-tools-list/info.png" />
                  <span class="toggletip-span-inline" role="status"></span>
              </abbr>
            {% endif %}
          </div>
        {% endfor %}
      </div>
  </fieldset>
  {% assign technology = site.data.filters | find: "id", "technology" %}
  <fieldset class="field" id="technology">
      <div class="fieldheader">
        <legend for="tool-technology" class="label-input">File to evaluate</legend>
        {% if technology.info %}
          <abbr title="{{ technology.info }}" class="toggletip-container">
              <img alt="{{ technology.info }}" tabindex="0" data-toggletip-content="{{ technology.info }}" src="/content-images/wai-evaluation-tools-list/info.png" />
              <span class="toggletip-span" role="status"></span>
          </abbr>
        {% endif %}
      </div>
      <div class="field-group">
        {% for option in technology.options %}
          <div class="radio-field">
            <input type="checkbox" name="technology[]" id="tool-technology-{{ option.id }}" value="{{ option.name }}" group="technology">
            <label for="tool-technology-{{ option.id }}">{{ option.name }}</label>
            {% if option.info %}
              <abbr title="{{ option.info }}" class="toggletip-container">
                  <img alt="{{ option.info }}" tabindex="0" data-toggletip-content="{{ option.info }}" src="/content-images/wai-evaluation-tools-list/info.png" />
                  <span class="toggletip-span-inline" role="status"></span>
              </abbr>
            {% endif %}
          </div>
        {% endfor %}
      </div>
  </fieldset>
  {% assign automated = site.data.filters | find: "id", "automated" %}
  <fieldset class="field" id="automated">
      <div class="fieldheader">
        <legend for="tool-automated" class="label-input">Scope of evaluation<span class="short-sub">(Required)</span></legend>
        <p>{{ automated.info }}</p>
      </div>
      <div class="field-group">
        {% for option in automated.options %}
          <div class="radio-field">
            <input type="checkbox" name="automated[]" id="tool-automated-{{ option.id }}" value="{{ option.name }}" group="automated" required>
            <label for="tool-automated-{{ option.id }}">{{ option.name }}</label>
            {% if option.info %}
              <abbr title="{{ option.info }}" class="toggletip-container">
                  <img alt="{{ option.info }}" tabindex="0" data-toggletip-content="{{ option.info }}" src="/content-images/wai-evaluation-tools-list/info.png" />
                  <span class="toggletip-span-inline" role="status"></span>
              </abbr>
            {% endif %}
          </div>
        {% endfor %}
      </div>
  </fieldset>
  {% assign checks = site.data.filters | find: "id", "checks" %}
  <fieldset class="field" id="checks">
      <div class="fieldheader">
        <legend for="tool-checks" class="label-input">Accessibility checks</legend>
      </div>
      <p>Which aspects of web accessibility can users evaluate with this tool?</p>
      <div class="field-group">
        {% for option in checks.options %}
          <div class="radio-field">
            <input type="checkbox" name="checks[]" id="tool-checks-{{ option.id }}" value="{{ option.name }}" group="checks">
            <label for="tool-checks-{{ option.id }}">{{ option.name }}</label>
            {% if option.info %}
              <abbr title="{{ option.info }}" class="toggletip-container">
                  <img alt="{{ option.info }}" tabindex="0" data-toggletip-content="{{ option.info }}" src="/content-images/wai-evaluation-tools-list/info.png" />
                  <span class="toggletip-span-inline" role="status"></span>
              </abbr>
            {% endif %}
          </div>
        {% endfor %}
      </div>
  </fieldset>
  {% assign guideline = site.data.filters | find: "id", "guideline" %}
  <fieldset class="field" id="guideline">
      <div class="fieldheader">
        <legend for="tool-guideline" class="label-input">Guidelines and standards</legend>
        {% if guideline.info %}
          <abbr title="{{ guideline.info }}" class="toggletip-container">
              <img alt="{{ guideline.info }}" tabindex="0" data-toggletip-content="{{ guideline.info }}" src="/content-images/wai-evaluation-tools-list/info.png" />
              <span class="toggletip-span" role="status"></span>
          </abbr>
        {% endif %}
      </div>
      <div class="field-group">
        {% for option in guideline.options %}
          <div class="radio-field">
            <input type="checkbox" name="guideline[]" id="tool-guideline-{{ option.id }}" value="{{ option.name }}" group="guideline">
            <label for="tool-guideline-{{ option.id }}">{{ option.name }}</label>
            {% if option.info %}
              <abbr title="{{ option.info }}" class="toggletip-container">
                  <img alt="{{ option.info }}" tabindex="0" data-toggletip-content="{{ option.info }}" src="/content-images/wai-evaluation-tools-list/info.png" />
                  <span class="toggletip-span-inline" role="status"></span>
              </abbr>
            {% endif %}
          </div>
        {% endfor %}
      </div>
  </fieldset>
  {% assign assists = site.data.filters | find: "id", "assists" %}
  <fieldset class="field" id="assists">
      <div class="fieldheader">
        <legend for="tool-assists" class="label-input">Output</legend>
        {% if assists.info %}
          <abbr title="{{ assists.info }}" class="toggletip-container">
              <img alt="{{ assists.info }}" tabindex="0" data-toggletip-content="{{ assists.info }}" src="/content-images/wai-evaluation-tools-list/info.png" />
              <span class="toggletip-span" role="status"></span>
          </abbr>
        {% endif %}
      </div>
      <div class="field-group">
        {% for option in assists.options %}
          <div class="radio-field">
            <input type="checkbox" name="assists[]" id="tool-assists-{{ option.id }}" value="{{ option.name }}" group="assists">
            <label for="tool-assists-{{ option.id }}">{{ option.name }}</label>
            {% if option.info %}
              <abbr title="{{ option.info }}" class="toggletip-container">
                  <img alt="{{ option.info }}" tabindex="0" data-toggletip-content="{{ option.info }}" src="/content-images/wai-evaluation-tools-list/info.png" />
                  <span class="toggletip-span-inline" role="status"></span>
              </abbr>
            {% endif %}
          </div>
        {% endfor %}
      </div>
  </fieldset>

  <h2 id="tool-details"><span>3/3</span>Tool details</h2>
  <div class="field" id="language">
    <label class="label specialField">Language<span>(Required)</span></label>
    <p class="expl">Indicate in which language or languages this tool is provided.</p>
    <div class="line">
      <label for="tool-language_1" class="label-input"></label>
      <select name="language[]" id="language_1" class="select-form" required> 
          <option value=""></option>
          {% for language in site.data.lang %}
              <option value="{{ language[0] }}">{{ language[1].name }} ({{language[1].nativeName }})</option>
          {% endfor %}
      </select>
    </div>
    <div class="proto">
      <label for="tool-language_[n]" class="label-input"></label>
      <select name="language[]" id="language_[n]" class="select-form" disabled> 
          <option value=""></option>
          {% for language in site.data.lang %}
              <option value="{{ language[0] }}">{{ language[1].name }} ({{language[1].nativeName }})</option>
          {% endfor %}
      </select>
      <button type="button" aria-label="Remove language" class="remove_line">Remove</button>
      </div>
    <button type="button" class="add_line small">Add language</button>
    <!-- <button type="button" class="remove_line small" disabled>Remove last language</button> -->
  </div>
  {% assign license = site.data.filters | find: "id", "license" %}
 <fieldset class="field" id="license">
  <div class="field-group">
      <legend for="tool-license" class="label-input">License<span class="short-sub">(Required)</span></legend>
<!--       {% for option in license.options %}
        <div class="radio-field">
          <input type="checkbox" name="license[]" id="tool-license-{{ option.id }}" value="{{ option.name }}" required>
          <label for="tool-license-{{ option.id }}">{{ option.name }}</label>
        </div>
      {% endfor %} -->
      <div class="radio-field">
        <input type="checkbox" name="license[]" id="tool-license-free" value="Free" group="licence" required>
        <label for="tool-license-free">Free</label>
      </div>
      <div class="radio-field">
        <input type="checkbox" name="license[]" id="tool-license-limited" value="Limited free functionality" group="licence" required>
        <label for="tool-license-limited">Limited free functionality</label>
      </div>
      <div class="radio-field">
        <input type="checkbox" name="license[]" id="tool-license-time" value="Time-limited trial" group="licence" required>
        <label for="tool-license-time">Time-limited trial</label>
      </div>
      <div class="radio-field">
        <input type="checkbox" name="license[]" id="tool-license-subscription" value="Subscription" group="licence" required>
        <label for="tool-license-subscription">Subscription</label>
      </div>
      <div class="radio-field">
        <input type="checkbox" name="license[]" id="tool-license-purchase" value="One-time purchase" group="licence" required>
        <label for="tool-license-purchase">One-time purchase</label>
      </div>
      <div class="radio-field">
        <input type="checkbox" name="license[]" id="tool-license-other" class="tool-license-other-check" group="licence">
        <label for="tool-license-purchase">Other:</label>
        <input type="text" name="license[]" id="tool-license-other" class="tool-license-other-input">
      </div>
    </div>
  </fieldset>
  {% assign type = site.data.filters | find: "id", "type" %}
  <fieldset class="field" id="type">
      <div class="fieldheader">
        <legend for="tool-type" class="label-input">Type of tool<span class="short-sub">(Required)</span></legend>
        {% if type.info %}
          <abbr title="{{ type.info }}" class="toggletip-container">
              <img alt="{{ type.info }}" tabindex="0" data-toggletip-content="{{ type.info }}" src="/content-images/wai-evaluation-tools-list/info.png" />
              <span class="toggletip-span" role="status"></span>
          </abbr>
        {% endif %}
      </div>
      <div class="field-group">
        {% for option in type.options %}
          <div class="radio-field">
            <input type="checkbox" name="type[]" id="tool-type-{{ option.id }}" value="{{ option.name }}" group="type" required>
            <label for="tool-type-{{ option.id }}">{{ option.name }}</label>
            {% if option.info %}
              <abbr title="{{ option.info }}" class="toggletip-container">
                  <img alt="{{ option.info }}" tabindex="0" data-toggletip-content="{{ option.info }}" src="/content-images/wai-evaluation-tools-list/info.png" />
                  <span class="toggletip-span-inline" role="status"></span>
              </abbr>
            {% endif %}
          </div>
        {% endfor %}
      </div>
  </fieldset>
  {% assign browsers = site.data.filters | find: "id", "browsers" %}
  <fieldset class="field" id="browsers">
      <div class="fieldheader">
        <legend for="tool-browsers" class="label-input">Browser for plugin</legend>
        {% if browsers.info %}
          <abbr title="{{ browsers.info }}" class="toggletip-container">
              <img alt="{{ browsers.info }}" tabindex="0" data-toggletip-content="{{ browsers.info }}" src="/content-images/wai-evaluation-tools-list/info.png" />
              <span class="toggletip-span" role="status"></span>
          </abbr>
        {% endif %}
      </div>
      <div class="field-group">
        {% for option in browsers.options %}
          <div class="radio-field">
            <input type="checkbox" name="browsers[]" id="tool-browsers-{{ option.id }}" value="{{ option.name }}" group="browsers">
            <label for="tool-browsers-{{ option.id }}">{{ option.name }}</label>
            {% if option.info %}
              <abbr title="{{ option.info }}" class="toggletip-container">
                  <img alt="{{ option.info }}" tabindex="0" data-toggletip-content="{{ option.info }}" src="/content-images/wai-evaluation-tools-list/info.png" />
                  <span class="toggletip-span-inline" role="status"></span>
              </abbr>
            {% endif %}
          </div>
        {% endfor %}
      </div>
  </fieldset>
  {% assign desktop = site.data.filters | find: "id", "desktop" %}
  <fieldset class="field" id="desktop">
      <div class="fieldheader">
      <legend for="tool-desktop" class="label-input">Operating system</legend>
        {% if desktop.info %}
          <abbr title="{{ desktop.info }}" class="toggletip-container">
              <img alt="{{ desktop.info }}" tabindex="0" data-toggletip-content="{{ desktop.info }}" src="/content-images/wai-evaluation-tools-list/info.png" />
              <span class="toggletip-span" role="status"></span>
          </abbr>
        {% endif %}
      </div>
      <div class="field-group">
        {% for option in desktop.options %}
          <div class="radio-field">
            <input type="checkbox" name="desktop[]" id="tool-desktop-{{ option.id }}" value="{{ option.name }}" group="desktop">
            <label for="tool-desktop-{{ option.id }}">{{ option.name }}</label>
            {% if option.info %}
              <abbr title="{{ option.info }}" class="toggletip-container">
                  <img alt="{{ option.info }}" tabindex="0" data-toggletip-content="{{ option.info }}" src="/content-images/wai-evaluation-tools-list/info.png" />
                  <span class="toggletip-span-inline" role="status"></span>
              </abbr>
            {% endif %}
          </div>
        {% endfor %}
      </div>
  </fieldset>

  <div class="field">
    <button type="submit" class="submit-tool">Submit tool</button>
  </div>
</div>
{% include list-submission-form.liquid type="end"%}

<script>
{% include js/submission.js %}
</script>