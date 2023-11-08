## phoenix jvm

```json
{
  "annotations": {
    "list": [
      {
        "builtIn": 1,
        "datasource": "-- Grafana --",
        "enable": true,
        "hide": true,
        "iconColor": "rgba(0, 211, 255, 1)",
        "name": "Annotations & Alerts",
        "type": "console"
      }
    ]
  },
  "description": "Complete console using metrics from prometheus JMX exporter, with drill down per job > instance",
  "editable": true,
  "gnetId": 8563,
  "graphTooltip": 0,
  "id": 2,
  "iteration": 1632818693141,
  "links": [],
  "panels": [
    {
      "cacheTimeout": null,
      "colorBackground": false,
      "colorValue": true,
      "colors": [
        "#d44a3a",
        "#e24d42",
        "#299c46"
      ],
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {}
        },
        "overrides": []
      },
      "format": "none",
      "gauge": {
        "maxValue": 100,
        "minValue": 0,
        "show": false,
        "thresholdLabels": false,
        "thresholdMarkers": true
      },
      "gridPos": {
        "h": 4,
        "w": 3,
        "x": 3,
        "y": 0
      },
      "hideTimeOverride": false,
      "id": 21,
      "interval": null,
      "links": [
        {
          "targetBlank": true,
          "title": "Tomcat console",
          "url": "/d/chanjarster-tomcat-console/tomcat-console?$__url_time_range&$__all_variables"
        }
      ],
      "mappingType": 1,
      "mappingTypes": [
        {
          "name": "value to text",
          "value": 1
        },
        {
          "name": "range to text",
          "value": 2
        }
      ],
      "maxDataPoints": 100,
      "nullPointMode": "connected",
      "nullText": null,
      "postfix": "",
      "postfixFontSize": "50%",
      "prefix": "",
      "prefixFontSize": "50%",
      "rangeMaps": [
        {
          "from": "null",
          "text": "N/A",
          "to": "null"
        }
      ],
      "sparkline": {
        "fillColor": "rgba(31, 118, 189, 0.18)",
        "full": false,
        "lineColor": "rgb(31, 120, 193)",
        "show": false
      },
      "tableColumn": "up{instance=\"10.42.1.4:8888\", job=\"java_app\", kubernetes_namespace=\"phoenix-dev\", kubernetes_pod_name=\"account-server-58875b86b6-hzlcf\", service_name=\"account-server\"}",
      "targets": [
        {
          "expr": "up{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "instant": true,
          "interval": "",
          "intervalFactor": 1,
          "legendFormat": "",
          "refId": "A"
        }
      ],
      "thresholds": "0,1",
      "timeShift": null,
      "title": "Status",
      "type": "singlestat",
      "valueFontSize": "80%",
      "valueMaps": [
        {
          "op": "=",
          "text": "UP",
          "value": "1"
        },
        {
          "op": "=",
          "text": "DOWN",
          "value": "0"
        },
        {
          "op": "=",
          "text": "DOWN",
          "value": "null"
        }
      ],
      "valueName": "current"
    },
    {
      "cacheTimeout": null,
      "colorBackground": false,
      "colorValue": false,
      "colors": [
        "#299c46",
        "rgba(237, 129, 40, 0.89)",
        "#d44a3a"
      ],
      "datasource": "Prometheus",
      "decimals": 0,
      "fieldConfig": {
        "defaults": {
          "custom": {}
        },
        "overrides": []
      },
      "format": "s",
      "gauge": {
        "maxValue": 100,
        "minValue": 0,
        "show": false,
        "thresholdLabels": false,
        "thresholdMarkers": true
      },
      "gridPos": {
        "h": 4,
        "w": 4,
        "x": 6,
        "y": 0
      },
      "id": 14,
      "interval": null,
      "links": [],
      "mappingType": 1,
      "mappingTypes": [
        {
          "name": "value to text",
          "value": 1
        },
        {
          "name": "range to text",
          "value": 2
        }
      ],
      "maxDataPoints": 100,
      "nullPointMode": "connected",
      "nullText": null,
      "postfix": "",
      "postfixFontSize": "50%",
      "prefix": "",
      "prefixFontSize": "50%",
      "rangeMaps": [
        {
          "from": "null",
          "text": "N/A",
          "to": "null"
        }
      ],
      "sparkline": {
        "fillColor": "rgba(31, 118, 189, 0.18)",
        "full": true,
        "lineColor": "rgb(31, 120, 193)",
        "show": false
      },
      "tableColumn": "{instance=\"10.42.1.4:8888\", job=\"java_app\", kubernetes_namespace=\"phoenix-dev\", kubernetes_pod_name=\"account-server-58875b86b6-hzlcf\", service_name=\"account-server\"}",
      "targets": [
        {
          "expr": "time() - process_start_time_seconds{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "instant": true,
          "intervalFactor": 1,
          "refId": "A"
        }
      ],
      "thresholds": "",
      "title": "Uptime",
      "type": "singlestat",
      "valueFontSize": "80%",
      "valueMaps": [
        {
          "op": "=",
          "text": "N/A",
          "value": "null"
        }
      ],
      "valueName": "current"
    },
    {
      "cacheTimeout": null,
      "colorBackground": false,
      "colorValue": false,
      "colors": [
        "#299c46",
        "rgba(237, 129, 40, 0.89)",
        "#d44a3a"
      ],
      "datasource": "Prometheus",
      "decimals": null,
      "fieldConfig": {
        "defaults": {
          "custom": {}
        },
        "overrides": []
      },
      "format": "dateTimeAsIso",
      "gauge": {
        "maxValue": 100,
        "minValue": 0,
        "show": false,
        "thresholdLabels": false,
        "thresholdMarkers": true
      },
      "gridPos": {
        "h": 4,
        "w": 4,
        "x": 10,
        "y": 0
      },
      "id": 15,
      "interval": "",
      "links": [],
      "mappingType": 1,
      "mappingTypes": [
        {
          "name": "value to text",
          "value": 1
        },
        {
          "name": "range to text",
          "value": 2
        }
      ],
      "maxDataPoints": 100,
      "nullPointMode": "connected",
      "nullText": null,
      "postfix": "",
      "postfixFontSize": "50%",
      "prefix": "",
      "prefixFontSize": "50%",
      "rangeMaps": [
        {
          "from": "null",
          "text": "N/A",
          "to": "null"
        }
      ],
      "sparkline": {
        "fillColor": "rgba(31, 118, 189, 0.18)",
        "full": true,
        "lineColor": "rgb(31, 120, 193)",
        "show": false
      },
      "tableColumn": "{instance=\"10.42.1.4:8888\", job=\"java_app\", kubernetes_namespace=\"phoenix-dev\", kubernetes_pod_name=\"account-server-58875b86b6-hzlcf\", service_name=\"account-server\"}",
      "targets": [
        {
          "expr": "process_start_time_seconds{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}*1000",
          "format": "time_series",
          "instant": true,
          "intervalFactor": 1,
          "refId": "A"
        }
      ],
      "thresholds": "35,50",
      "title": "Start time",
      "type": "singlestat",
      "valueFontSize": "80%",
      "valueMaps": [
        {
          "op": "=",
          "text": "N/A",
          "value": "null"
        }
      ],
      "valueName": "current"
    },
    {
      "cacheTimeout": null,
      "colorBackground": false,
      "colorValue": false,
      "colors": [
        "#299c46",
        "rgba(237, 129, 40, 0.89)",
        "#d44a3a"
      ],
      "datasource": "Prometheus",
      "decimals": 0,
      "fieldConfig": {
        "defaults": {
          "custom": {}
        },
        "overrides": []
      },
      "format": "none",
      "gauge": {
        "maxValue": 100,
        "minValue": 0,
        "show": false,
        "thresholdLabels": false,
        "thresholdMarkers": true
      },
      "gridPos": {
        "h": 4,
        "w": 7,
        "x": 14,
        "y": 0
      },
      "id": 19,
      "interval": null,
      "links": [],
      "mappingType": 1,
      "mappingTypes": [
        {
          "name": "value to text",
          "value": 1
        },
        {
          "name": "range to text",
          "value": 2
        }
      ],
      "maxDataPoints": 100,
      "nullPointMode": "connected",
      "nullText": null,
      "postfix": "",
      "postfixFontSize": "50%",
      "prefix": "",
      "prefixFontSize": "50%",
      "rangeMaps": [
        {
          "from": "null",
          "text": "N/A",
          "to": "null"
        }
      ],
      "sparkline": {
        "fillColor": "rgba(31, 118, 189, 0.18)",
        "full": true,
        "lineColor": "rgb(31, 120, 193)",
        "show": false
      },
      "tableColumn": "jdk",
      "targets": [
        {
          "expr": "label_join(jvm_info{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}, \"jdk\", \", \", \"vendor\", \"runtime\", \"version\")",
          "format": "table",
          "instant": true,
          "intervalFactor": 1,
          "legendFormat": "",
          "refId": "A"
        }
      ],
      "thresholds": "",
      "title": "JVM Version",
      "type": "singlestat",
      "valueFontSize": "50%",
      "valueMaps": [
        {
          "op": "=",
          "text": "N/A",
          "value": "null"
        }
      ],
      "valueName": "current"
    },
    {
      "cacheTimeout": null,
      "colorBackground": false,
      "colorValue": false,
      "colors": [
        "#299c46",
        "rgba(237, 129, 40, 0.89)",
        "#d44a3a"
      ],
      "datasource": "Prometheus",
      "decimals": null,
      "fieldConfig": {
        "defaults": {
          "custom": {}
        },
        "overrides": []
      },
      "format": "none",
      "gauge": {
        "maxValue": 100,
        "minValue": 0,
        "show": false,
        "thresholdLabels": false,
        "thresholdMarkers": true
      },
      "gridPos": {
        "h": 4,
        "w": 4,
        "x": 6,
        "y": 4
      },
      "id": 39,
      "interval": "",
      "links": [],
      "mappingType": 1,
      "mappingTypes": [
        {
          "name": "value to text",
          "value": 1
        },
        {
          "name": "range to text",
          "value": 2
        }
      ],
      "maxDataPoints": 100,
      "nullPointMode": "connected",
      "nullText": null,
      "postfix": "",
      "postfixFontSize": "50%",
      "prefix": "",
      "prefixFontSize": "50%",
      "rangeMaps": [
        {
          "from": "null",
          "text": "N/A",
          "to": "null"
        }
      ],
      "sparkline": {
        "fillColor": "rgba(31, 118, 189, 0.18)",
        "full": true,
        "lineColor": "rgb(31, 120, 193)",
        "show": false
      },
      "tableColumn": "os_available_processors{instance=\"10.42.1.4:8888\", job=\"java_app\", kubernetes_namespace=\"phoenix-dev\", kubernetes_pod_name=\"account-server-58875b86b6-hzlcf\", service_name=\"account-server\"}",
      "targets": [
        {
          "expr": "os_available_processors{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "instant": true,
          "intervalFactor": 1,
          "refId": "A"
        }
      ],
      "thresholds": "",
      "title": "Available CPUs",
      "type": "singlestat",
      "valueFontSize": "80%",
      "valueMaps": [
        {
          "op": "=",
          "text": "N/A",
          "value": "null"
        }
      ],
      "valueName": "current"
    },
    {
      "cacheTimeout": null,
      "colorBackground": false,
      "colorValue": false,
      "colors": [
        "#299c46",
        "rgba(237, 129, 40, 0.89)",
        "#d44a3a"
      ],
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {}
        },
        "overrides": []
      },
      "format": "none",
      "gauge": {
        "maxValue": 100,
        "minValue": 0,
        "show": false,
        "thresholdLabels": false,
        "thresholdMarkers": true
      },
      "gridPos": {
        "h": 4,
        "w": 4,
        "x": 10,
        "y": 4
      },
      "id": 23,
      "interval": null,
      "links": [],
      "mappingType": 1,
      "mappingTypes": [
        {
          "name": "value to text",
          "value": 1
        },
        {
          "name": "range to text",
          "value": 2
        }
      ],
      "maxDataPoints": 100,
      "nullPointMode": "connected",
      "nullText": null,
      "postfix": "",
      "postfixFontSize": "50%",
      "prefix": "",
      "prefixFontSize": "50%",
      "rangeMaps": [
        {
          "from": "null",
          "text": "N/A",
          "to": "null"
        }
      ],
      "sparkline": {
        "fillColor": "rgba(31, 118, 189, 0.18)",
        "full": false,
        "lineColor": "rgb(31, 120, 193)",
        "show": false
      },
      "tableColumn": "os_system_load_average{instance=\"10.42.1.4:8888\", job=\"java_app\", kubernetes_namespace=\"phoenix-dev\", kubernetes_pod_name=\"account-server-58875b86b6-hzlcf\", service_name=\"account-server\"}",
      "targets": [
        {
          "expr": "os_system_load_average{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "instant": true,
          "intervalFactor": 1,
          "refId": "A"
        }
      ],
      "thresholds": "",
      "title": "System load average",
      "type": "singlestat",
      "valueFontSize": "80%",
      "valueMaps": [
        {
          "op": "=",
          "text": "N/A",
          "value": "null"
        }
      ],
      "valueName": "avg"
    },
    {
      "cacheTimeout": null,
      "colorBackground": false,
      "colorValue": false,
      "colors": [
        "#299c46",
        "rgba(237, 129, 40, 0.89)",
        "#d44a3a"
      ],
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {}
        },
        "overrides": []
      },
      "format": "none",
      "gauge": {
        "maxValue": 100,
        "minValue": 0,
        "show": false,
        "thresholdLabels": false,
        "thresholdMarkers": true
      },
      "gridPos": {
        "h": 4,
        "w": 4,
        "x": 14,
        "y": 4
      },
      "id": 38,
      "interval": null,
      "links": [],
      "mappingType": 1,
      "mappingTypes": [
        {
          "name": "value to text",
          "value": 1
        },
        {
          "name": "range to text",
          "value": 2
        }
      ],
      "maxDataPoints": 100,
      "nullPointMode": "connected",
      "nullText": null,
      "postfix": "",
      "postfixFontSize": "50%",
      "prefix": "",
      "prefixFontSize": "50%",
      "rangeMaps": [
        {
          "from": "null",
          "text": "N/A",
          "to": "null"
        }
      ],
      "sparkline": {
        "fillColor": "rgba(31, 118, 189, 0.18)",
        "full": false,
        "lineColor": "rgb(31, 120, 193)",
        "show": false
      },
      "tableColumn": "os_open_file_descriptor_count{instance=\"10.42.1.4:8888\", job=\"java_app\", kubernetes_namespace=\"phoenix-dev\", kubernetes_pod_name=\"account-server-58875b86b6-hzlcf\", service_name=\"account-server\"}",
      "targets": [
        {
          "expr": "os_open_file_descriptor_count{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "instant": true,
          "intervalFactor": 1,
          "refId": "A"
        }
      ],
      "thresholds": "",
      "title": "Open file descriptors",
      "type": "singlestat",
      "valueFontSize": "80%",
      "valueMaps": [
        {
          "op": "=",
          "text": "N/A",
          "value": "null"
        }
      ],
      "valueName": "avg"
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "decimals": 1,
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 9,
        "w": 24,
        "x": 0,
        "y": 8
      },
      "hiddenSeries": false,
      "id": 29,
      "legend": {
        "alignAsTable": true,
        "avg": false,
        "current": true,
        "max": true,
        "min": false,
        "show": true,
        "total": false,
        "values": true
      },
      "lines": true,
      "linewidth": 1,
      "links": [],
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 5,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "os_system_cpu_load{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "intervalFactor": 1,
          "legendFormat": "System",
          "refId": "B"
        },
        {
          "expr": "os_process_cpu_load{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "intervalFactor": 1,
          "legendFormat": "JVM",
          "refId": "A"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "CPU load",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "decimals": 1,
          "format": "percentunit",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": false
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 9,
        "w": 12,
        "x": 0,
        "y": 17
      },
      "hiddenSeries": false,
      "id": 8,
      "legend": {
        "alignAsTable": true,
        "avg": true,
        "current": true,
        "max": true,
        "min": true,
        "rightSide": false,
        "show": true,
        "sortDesc": true,
        "total": false,
        "values": true
      },
      "lines": true,
      "linewidth": 1,
      "links": [],
      "maxPerRow": 2,
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 5,
      "points": false,
      "renderer": "flot",
      "repeat": "memarea",
      "repeatDirection": "h",
      "scopedVars": {
        "memarea": {
          "selected": false,
          "text": "heap",
          "value": "heap"
        }
      },
      "seriesOverrides": [
        {
          "alias": "Usage %",
          "bars": true,
          "color": "#6d1f62",
          "legend": false,
          "lines": false,
          "yaxis": 2,
          "zindex": -1
        }
      ],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "jvm_memory_bytes_used{area=\"$memarea\",kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "intervalFactor": 1,
          "legendFormat": "Used",
          "refId": "A"
        },
        {
          "expr": " jvm_memory_bytes_max{area=\"$memarea\",kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "intervalFactor": 1,
          "legendFormat": "Max",
          "refId": "B"
        },
        {
          "expr": "jvm_memory_bytes_used{area=\"$memarea\",kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"} / jvm_memory_bytes_max >= 0",
          "format": "time_series",
          "intervalFactor": 1,
          "legendFormat": "Usage %",
          "refId": "C"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "Memory area [$memarea]",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "bytes",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "percentunit",
          "label": "",
          "logBase": 1,
          "max": "1",
          "min": "0",
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 9,
        "w": 12,
        "x": 12,
        "y": 17
      },
      "hiddenSeries": false,
      "id": 45,
      "legend": {
        "alignAsTable": true,
        "avg": true,
        "current": true,
        "max": true,
        "min": true,
        "rightSide": false,
        "show": true,
        "sortDesc": true,
        "total": false,
        "values": true
      },
      "lines": true,
      "linewidth": 1,
      "links": [],
      "maxPerRow": 2,
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 5,
      "points": false,
      "renderer": "flot",
      "repeat": null,
      "repeatDirection": "h",
      "repeatIteration": 1632818693141,
      "repeatPanelId": 8,
      "scopedVars": {
        "memarea": {
          "selected": false,
          "text": "nonheap",
          "value": "nonheap"
        }
      },
      "seriesOverrides": [
        {
          "alias": "Usage %",
          "bars": true,
          "color": "#6d1f62",
          "legend": false,
          "lines": false,
          "yaxis": 2,
          "zindex": -1
        }
      ],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "jvm_memory_bytes_used{area=\"$memarea\",kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "intervalFactor": 1,
          "legendFormat": "Used",
          "refId": "A"
        },
        {
          "expr": " jvm_memory_bytes_max{area=\"$memarea\",kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "intervalFactor": 1,
          "legendFormat": "Max",
          "refId": "B"
        },
        {
          "expr": "jvm_memory_bytes_used{area=\"$memarea\",kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"} / jvm_memory_bytes_max >= 0",
          "format": "time_series",
          "intervalFactor": 1,
          "legendFormat": "Usage %",
          "refId": "C"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "Memory area [$memarea]",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "bytes",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "percentunit",
          "label": "",
          "logBase": 1,
          "max": "1",
          "min": "0",
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 9,
        "w": 12,
        "x": 0,
        "y": 26
      },
      "hiddenSeries": false,
      "id": 2,
      "legend": {
        "alignAsTable": true,
        "avg": true,
        "current": true,
        "max": true,
        "min": true,
        "rightSide": false,
        "show": true,
        "sort": "current",
        "sortDesc": true,
        "total": false,
        "values": true
      },
      "lines": true,
      "linewidth": 1,
      "links": [],
      "maxPerRow": 2,
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 5,
      "points": false,
      "renderer": "flot",
      "repeat": "mempool",
      "repeatDirection": "h",
      "scopedVars": {
        "mempool": {
          "selected": false,
          "text": "CMS Old Gen",
          "value": "CMS Old Gen"
        }
      },
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "jvm_memory_pool_bytes_max{pool=\"$mempool\",kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "interval": "",
          "intervalFactor": 1,
          "legendFormat": "Max",
          "metric": "jvm_memory_bytes_used",
          "refId": "B",
          "step": 5
        },
        {
          "expr": "jvm_memory_pool_bytes_used{pool=\"$mempool\",kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "interval": "",
          "intervalFactor": 1,
          "legendFormat": "Used",
          "metric": "jvm_memory_bytes_used",
          "refId": "A",
          "step": 5
        },
        {
          "expr": "jvm_memory_pool_bytes_committed{pool=\"$mempool\",kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "interval": "",
          "intervalFactor": 1,
          "legendFormat": "Committed",
          "metric": "jvm_memory_bytes_used",
          "refId": "C",
          "step": 5
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "Memory pool [$mempool]",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "bytes",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 9,
        "w": 12,
        "x": 12,
        "y": 26
      },
      "hiddenSeries": false,
      "id": 46,
      "legend": {
        "alignAsTable": true,
        "avg": true,
        "current": true,
        "max": true,
        "min": true,
        "rightSide": false,
        "show": true,
        "sort": "current",
        "sortDesc": true,
        "total": false,
        "values": true
      },
      "lines": true,
      "linewidth": 1,
      "links": [],
      "maxPerRow": 2,
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 5,
      "points": false,
      "renderer": "flot",
      "repeat": null,
      "repeatDirection": "h",
      "repeatIteration": 1632818693141,
      "repeatPanelId": 2,
      "scopedVars": {
        "mempool": {
          "selected": false,
          "text": "Code Cache",
          "value": "Code Cache"
        }
      },
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "jvm_memory_pool_bytes_max{pool=\"$mempool\",kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "interval": "",
          "intervalFactor": 1,
          "legendFormat": "Max",
          "metric": "jvm_memory_bytes_used",
          "refId": "B",
          "step": 5
        },
        {
          "expr": "jvm_memory_pool_bytes_used{pool=\"$mempool\",kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "interval": "",
          "intervalFactor": 1,
          "legendFormat": "Used",
          "metric": "jvm_memory_bytes_used",
          "refId": "A",
          "step": 5
        },
        {
          "expr": "jvm_memory_pool_bytes_committed{pool=\"$mempool\",kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "interval": "",
          "intervalFactor": 1,
          "legendFormat": "Committed",
          "metric": "jvm_memory_bytes_used",
          "refId": "C",
          "step": 5
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "Memory pool [$mempool]",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "bytes",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 9,
        "w": 12,
        "x": 0,
        "y": 35
      },
      "hiddenSeries": false,
      "id": 47,
      "legend": {
        "alignAsTable": true,
        "avg": true,
        "current": true,
        "max": true,
        "min": true,
        "rightSide": false,
        "show": true,
        "sort": "current",
        "sortDesc": true,
        "total": false,
        "values": true
      },
      "lines": true,
      "linewidth": 1,
      "links": [],
      "maxPerRow": 2,
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 5,
      "points": false,
      "renderer": "flot",
      "repeat": null,
      "repeatDirection": "h",
      "repeatIteration": 1632818693141,
      "repeatPanelId": 2,
      "scopedVars": {
        "mempool": {
          "selected": false,
          "text": "Compressed Class Space",
          "value": "Compressed Class Space"
        }
      },
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "jvm_memory_pool_bytes_max{pool=\"$mempool\",kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "interval": "",
          "intervalFactor": 1,
          "legendFormat": "Max",
          "metric": "jvm_memory_bytes_used",
          "refId": "B",
          "step": 5
        },
        {
          "expr": "jvm_memory_pool_bytes_used{pool=\"$mempool\",kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "interval": "",
          "intervalFactor": 1,
          "legendFormat": "Used",
          "metric": "jvm_memory_bytes_used",
          "refId": "A",
          "step": 5
        },
        {
          "expr": "jvm_memory_pool_bytes_committed{pool=\"$mempool\",kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "interval": "",
          "intervalFactor": 1,
          "legendFormat": "Committed",
          "metric": "jvm_memory_bytes_used",
          "refId": "C",
          "step": 5
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "Memory pool [$mempool]",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "bytes",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 9,
        "w": 12,
        "x": 12,
        "y": 35
      },
      "hiddenSeries": false,
      "id": 48,
      "legend": {
        "alignAsTable": true,
        "avg": true,
        "current": true,
        "max": true,
        "min": true,
        "rightSide": false,
        "show": true,
        "sort": "current",
        "sortDesc": true,
        "total": false,
        "values": true
      },
      "lines": true,
      "linewidth": 1,
      "links": [],
      "maxPerRow": 2,
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 5,
      "points": false,
      "renderer": "flot",
      "repeat": null,
      "repeatDirection": "h",
      "repeatIteration": 1632818693141,
      "repeatPanelId": 2,
      "scopedVars": {
        "mempool": {
          "selected": false,
          "text": "Metaspace",
          "value": "Metaspace"
        }
      },
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "jvm_memory_pool_bytes_max{pool=\"$mempool\",kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "interval": "",
          "intervalFactor": 1,
          "legendFormat": "Max",
          "metric": "jvm_memory_bytes_used",
          "refId": "B",
          "step": 5
        },
        {
          "expr": "jvm_memory_pool_bytes_used{pool=\"$mempool\",kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "interval": "",
          "intervalFactor": 1,
          "legendFormat": "Used",
          "metric": "jvm_memory_bytes_used",
          "refId": "A",
          "step": 5
        },
        {
          "expr": "jvm_memory_pool_bytes_committed{pool=\"$mempool\",kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "interval": "",
          "intervalFactor": 1,
          "legendFormat": "Committed",
          "metric": "jvm_memory_bytes_used",
          "refId": "C",
          "step": 5
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "Memory pool [$mempool]",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "bytes",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 9,
        "w": 12,
        "x": 0,
        "y": 44
      },
      "hiddenSeries": false,
      "id": 49,
      "legend": {
        "alignAsTable": true,
        "avg": true,
        "current": true,
        "max": true,
        "min": true,
        "rightSide": false,
        "show": true,
        "sort": "current",
        "sortDesc": true,
        "total": false,
        "values": true
      },
      "lines": true,
      "linewidth": 1,
      "links": [],
      "maxPerRow": 2,
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 5,
      "points": false,
      "renderer": "flot",
      "repeat": null,
      "repeatDirection": "h",
      "repeatIteration": 1632818693141,
      "repeatPanelId": 2,
      "scopedVars": {
        "mempool": {
          "selected": false,
          "text": "Par Eden Space",
          "value": "Par Eden Space"
        }
      },
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "jvm_memory_pool_bytes_max{pool=\"$mempool\",kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "interval": "",
          "intervalFactor": 1,
          "legendFormat": "Max",
          "metric": "jvm_memory_bytes_used",
          "refId": "B",
          "step": 5
        },
        {
          "expr": "jvm_memory_pool_bytes_used{pool=\"$mempool\",kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "interval": "",
          "intervalFactor": 1,
          "legendFormat": "Used",
          "metric": "jvm_memory_bytes_used",
          "refId": "A",
          "step": 5
        },
        {
          "expr": "jvm_memory_pool_bytes_committed{pool=\"$mempool\",kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "interval": "",
          "intervalFactor": 1,
          "legendFormat": "Committed",
          "metric": "jvm_memory_bytes_used",
          "refId": "C",
          "step": 5
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "Memory pool [$mempool]",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "bytes",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 9,
        "w": 12,
        "x": 12,
        "y": 44
      },
      "hiddenSeries": false,
      "id": 50,
      "legend": {
        "alignAsTable": true,
        "avg": true,
        "current": true,
        "max": true,
        "min": true,
        "rightSide": false,
        "show": true,
        "sort": "current",
        "sortDesc": true,
        "total": false,
        "values": true
      },
      "lines": true,
      "linewidth": 1,
      "links": [],
      "maxPerRow": 2,
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 5,
      "points": false,
      "renderer": "flot",
      "repeat": null,
      "repeatDirection": "h",
      "repeatIteration": 1632818693141,
      "repeatPanelId": 2,
      "scopedVars": {
        "mempool": {
          "selected": false,
          "text": "Par Survivor Space",
          "value": "Par Survivor Space"
        }
      },
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "jvm_memory_pool_bytes_max{pool=\"$mempool\",kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "interval": "",
          "intervalFactor": 1,
          "legendFormat": "Max",
          "metric": "jvm_memory_bytes_used",
          "refId": "B",
          "step": 5
        },
        {
          "expr": "jvm_memory_pool_bytes_used{pool=\"$mempool\",kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "interval": "",
          "intervalFactor": 1,
          "legendFormat": "Used",
          "metric": "jvm_memory_bytes_used",
          "refId": "A",
          "step": 5
        },
        {
          "expr": "jvm_memory_pool_bytes_committed{pool=\"$mempool\",kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "interval": "",
          "intervalFactor": 1,
          "legendFormat": "Committed",
          "metric": "jvm_memory_bytes_used",
          "refId": "C",
          "step": 5
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "Memory pool [$mempool]",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "bytes",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "decimals": 0,
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 9,
        "w": 12,
        "x": 0,
        "y": 53
      },
      "hiddenSeries": false,
      "id": 6,
      "legend": {
        "alignAsTable": true,
        "avg": false,
        "current": true,
        "max": true,
        "min": true,
        "show": true,
        "total": false,
        "values": true
      },
      "lines": true,
      "linewidth": 1,
      "links": [],
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 5,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "increase(jvm_gc_collection_seconds_count{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[$__interval])",
          "format": "time_series",
          "interval": "60s",
          "intervalFactor": 1,
          "legendFormat": "{{gc}}",
          "metric": "",
          "refId": "A",
          "step": 10
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "GC count increase",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "decimals": 0,
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": false
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "decimals": 0,
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 9,
        "w": 12,
        "x": 12,
        "y": 53
      },
      "hiddenSeries": false,
      "id": 5,
      "legend": {
        "alignAsTable": true,
        "avg": false,
        "current": true,
        "max": true,
        "min": true,
        "rightSide": false,
        "show": true,
        "total": false,
        "values": true
      },
      "lines": true,
      "linewidth": 1,
      "links": [],
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 5,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "increase(jvm_gc_collection_seconds_sum{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[$__interval])",
          "format": "time_series",
          "interval": "60s",
          "intervalFactor": 1,
          "legendFormat": "{{gc}}",
          "metric": "jvm_gc_collection_seconds_sum",
          "refId": "A",
          "step": 10
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "GC time",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "s",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": false
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "decimals": 0,
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 9,
        "w": 12,
        "x": 0,
        "y": 62
      },
      "hiddenSeries": false,
      "id": 3,
      "legend": {
        "alignAsTable": true,
        "avg": false,
        "current": true,
        "hideZero": true,
        "max": true,
        "min": false,
        "rightSide": false,
        "show": true,
        "total": false,
        "values": true
      },
      "lines": true,
      "linewidth": 1,
      "links": [],
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 5,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "jvm_threads_current{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "intervalFactor": 5,
          "legendFormat": "JVM current threads",
          "metric": "jvm_threads_current",
          "refId": "A",
          "step": 10
        },
        {
          "expr": "jvm_threads_daemon{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "intervalFactor": 5,
          "legendFormat": "JVM daemon threads",
          "metric": "jvm_threads_daemon",
          "refId": "B",
          "step": 10
        },
        {
          "expr": "jvm_threads_deadlocked{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "intervalFactor": 1,
          "legendFormat": "JVM deadlocked threads",
          "refId": "C"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "Threads used",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "decimals": 0,
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": false
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 9,
        "w": 12,
        "x": 12,
        "y": 62
      },
      "hiddenSeries": false,
      "id": 4,
      "legend": {
        "alignAsTable": true,
        "avg": false,
        "current": true,
        "max": true,
        "min": true,
        "show": true,
        "total": false,
        "values": true
      },
      "lines": true,
      "linewidth": 1,
      "links": [],
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 5,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "jvm_classes_loaded{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "interval": "",
          "intervalFactor": 5,
          "legendFormat": "loaded",
          "metric": "jvm_classes_loaded",
          "refId": "A",
          "step": 10
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "Class loading",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "decimals": 0,
          "format": "short",
          "label": "",
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": false
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 10,
        "w": 24,
        "x": 0,
        "y": 71
      },
      "hiddenSeries": false,
      "id": 44,
      "legend": {
        "alignAsTable": true,
        "avg": false,
        "current": true,
        "max": true,
        "min": true,
        "show": true,
        "total": false,
        "values": true
      },
      "lines": true,
      "linewidth": 1,
      "links": [],
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 5,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "os_total_physical_memory_bytes{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "intervalFactor": 1,
          "legendFormat": "Total physical memory",
          "refId": "A"
        },
        {
          "expr": "os_committed_virtual_memory_bytes{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "intervalFactor": 1,
          "legendFormat": "Committed virtual memory",
          "refId": "B"
        },
        {
          "expr": "os_free_physical_memory_bytes{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}",
          "format": "time_series",
          "intervalFactor": 1,
          "legendFormat": "Free physical memory",
          "refId": "C"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "Physical memory",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "decbytes",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    }
  ],
  "refresh": "10s",
  "schemaVersion": 26,
  "style": "dark",
  "tags": [
    "JVM"
  ],
  "templating": {
    "list": [
      {
        "allValue": null,
        "current": {
          "selected": false,
          "text": "phoenix-dev",
          "value": "phoenix-dev"
        },
        "datasource": "Prometheus",
        "definition": "label_values(jvm_info{}, kubernetes_namespace)",
        "hide": 0,
        "includeAll": false,
        "label": "namespace",
        "multi": false,
        "name": "namespace",
        "options": [],
        "query": "label_values(jvm_info{}, kubernetes_namespace)",
        "refresh": 2,
        "regex": "",
        "skipUrlSync": false,
        "sort": 1,
        "tagValuesQuery": "",
        "tags": [],
        "tagsQuery": "",
        "type": "query",
        "useTags": false
      },
      {
        "allValue": ".*",
        "current": {
          "selected": false,
          "text": "account-server",
          "value": "account-server"
        },
        "datasource": "Prometheus",
        "definition": "label_values(jvm_info{kubernetes_namespace=~\"$namespace\"},service_name)",
        "hide": 0,
        "includeAll": false,
        "label": "appname",
        "multi": false,
        "name": "appname",
        "options": [],
        "query": "label_values(jvm_info{kubernetes_namespace=~\"$namespace\"},service_name)",
        "refresh": 2,
        "regex": "",
        "skipUrlSync": false,
        "sort": 1,
        "tagValuesQuery": "",
        "tags": [],
        "tagsQuery": "",
        "type": "query",
        "useTags": false
      },
      {
        "allValue": ".*",
        "current": {
          "selected": false,
          "text": "10.42.1.4:8888",
          "value": "10.42.1.4:8888"
        },
        "datasource": "Prometheus",
        "definition": "label_values(jvm_info{kubernetes_namespace=~\"$namespace\",service_name=~\"$appname\"},instance)",
        "hide": 0,
        "includeAll": false,
        "label": "instance",
        "multi": false,
        "name": "instance",
        "options": [],
        "query": "label_values(jvm_info{kubernetes_namespace=~\"$namespace\",service_name=~\"$appname\"},instance)",
        "refresh": 2,
        "regex": "",
        "skipUrlSync": false,
        "sort": 1,
        "tagValuesQuery": "",
        "tags": [],
        "tagsQuery": "",
        "type": "query",
        "useTags": false
      },
      {
        "allValue": null,
        "current": {
          "selected": false,
          "text": "All",
          "value": "$__all"
        },
        "datasource": "Prometheus",
        "definition": "label_values(jvm_memory_pool_bytes_max{instance=\"$instance\"}, pool)",
        "hide": 2,
        "includeAll": true,
        "label": null,
        "multi": true,
        "name": "mempool",
        "options": [],
        "query": "label_values(jvm_memory_pool_bytes_max{instance=\"$instance\"}, pool)",
        "refresh": 1,
        "regex": "",
        "skipUrlSync": false,
        "sort": 1,
        "tagValuesQuery": "",
        "tags": [],
        "tagsQuery": "",
        "type": "query",
        "useTags": false
      },
      {
        "allValue": null,
        "current": {
          "selected": false,
          "text": "All",
          "value": "$__all"
        },
        "datasource": "Prometheus",
        "definition": "label_values(jvm_memory_bytes_used{instance=\"$instance\"}, area)",
        "hide": 2,
        "includeAll": true,
        "label": null,
        "multi": true,
        "name": "memarea",
        "options": [],
        "query": "label_values(jvm_memory_bytes_used{instance=\"$instance\"}, area)",
        "refresh": 1,
        "regex": "",
        "skipUrlSync": false,
        "sort": 0,
        "tagValuesQuery": "",
        "tags": [],
        "tagsQuery": "",
        "type": "query",
        "useTags": false
      }
    ]
  },
  "time": {
    "from": "now-15m",
    "to": "now"
  },
  "timepicker": {
    "refresh_intervals": [
      "10s",
      "30s",
      "1m",
      "5m"
    ],
    "time_options": [
      "5m",
      "15m",
      "1h",
      "6h",
      "12h",
      "24h",
      "2d",
      "7d",
      "30d"
    ]
  },
  "timezone": "",
  "title": "08 phoenix jvm",
  "uid": "9ZCNVWNGz12",
  "version": 1
}
```

## phoenix client

```json
{
  "annotations": {
    "list": [
      {
        "builtIn": 1,
        "datasource": "-- Grafana --",
        "enable": true,
        "hide": true,
        "iconColor": "rgba(0, 211, 255, 1)",
        "name": "Annotations & Alerts",
        "type": "console"
      }
    ]
  },
  "editable": true,
  "gnetId": null,
  "graphTooltip": 0,
  "id": 8,
  "iteration": 1632909736328,
  "links": [],
  "panels": [
    {
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green",
                "value": null
              }
            ]
          }
        },
        "overrides": []
      },
      "gridPos": {
        "h": 8,
        "w": 21,
        "x": 0,
        "y": 0
      },
      "id": 4,
      "options": {
        "reduceOptions": {
          "calcs": [
            "delta"
          ],
          "fields": "",
          "values": false
        },
        "showThresholdLabels": false,
        "showThresholdMarkers": true
      },
      "pluginVersion": "7.1.1",
      "targets": [
        {
          "expr": "sum by()(com_iquantex_Phoenix_PhoenixClient_SendSuccessTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "异步发送成功数量",
          "refId": "A"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_PhoenixClient_SendFailTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "异步发送失败数量",
          "refId": "B"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_PhoenixClient_RpcSendSuccessTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "同步发送成功数量",
          "refId": "H"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_PhoenixClient_RpcSendFailTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "同步发送失败数量",
          "refId": "G"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_PhoenixClient_TimeOutTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "同步发送超时数量",
          "refId": "C"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_PhoenixClient_RpcSuccessTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "同步发送撮合成功次数",
          "refId": "F"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_PhoenixClient_RetryTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "同步发送重试次数",
          "refId": "D"
        }
      ],
      "timeFrom": null,
      "timeShift": null,
      "title": "phoenix client指标",
      "type": "gauge"
    },
    {
      "datasource": "Prometheus",
      "description": "",
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green",
                "value": null
              },
              {
                "color": "orange",
                "value": 1
              }
            ]
          }
        },
        "overrides": []
      },
      "gridPos": {
        "h": 8,
        "w": 3,
        "x": 21,
        "y": 0
      },
      "id": 8,
      "options": {
        "reduceOptions": {
          "calcs": [
            "lastNotNull"
          ],
          "fields": "",
          "values": false
        },
        "showThresholdLabels": false,
        "showThresholdMarkers": true
      },
      "pluginVersion": "7.1.1",
      "targets": [
        {
          "expr": "sum by()(com_iquantex_Phoenix_PhoenixClient_RpcSendSuccessTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}) + sum by()(com_iquantex_Phoenix_PhoenixClient_RpcSendFailTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}) - sum by()(com_iquantex_Phoenix_PhoenixClient_RpcSuccessTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}) - sum by()(com_iquantex_Phoenix_PhoenixClient_TimeOutTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "同步发送等待回复总数",
          "refId": "A"
        }
      ],
      "timeFrom": null,
      "timeShift": null,
      "title": "phoenix client 实时指标",
      "type": "gauge"
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {}
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 21,
        "w": 24,
        "x": 0,
        "y": 8
      },
      "hiddenSeries": false,
      "id": 6,
      "legend": {
        "avg": false,
        "current": false,
        "max": false,
        "min": false,
        "show": true,
        "total": false,
        "values": false
      },
      "lines": true,
      "linewidth": 1,
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 2,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "sum by()(rate(com_iquantex_Phoenix_PhoenixClient_SendSuccessTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "异步发送速率",
          "refId": "F"
        },
        {
          "expr": "sum by()(rate(com_iquantex_Phoenix_PhoenixClient_SendFailTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "异步发送失败速率",
          "refId": "A"
        },
        {
          "expr": "sum by()(rate(com_iquantex_Phoenix_PhoenixClient_RpcSendSuccessTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "同步发送速率",
          "refId": "G"
        },
        {
          "expr": "sum by()(rate(com_iquantex_Phoenix_PhoenixClient_RpcSendFailTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "同步发送失败速率",
          "refId": "B"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "发送流速",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    }
  ],
  "refresh": "10s",
  "schemaVersion": 26,
  "style": "dark",
  "tags": [
    "Phoenix"
  ],
  "templating": {
    "list": [
      {
        "allValue": null,
        "current": {
          "selected": false,
          "text": "All",
          "value": "$__all"
        },
        "datasource": "Prometheus",
        "definition": "label_values(com_iquantex_Phoenix_PhoenixClient_RpcSendSuccessTotal{},kubernetes_namespace)",
        "hide": 0,
        "includeAll": true,
        "label": "namespace",
        "multi": false,
        "name": "namespace",
        "options": [],
        "query": "label_values(com_iquantex_Phoenix_PhoenixClient_RpcSendSuccessTotal{},kubernetes_namespace)",
        "refresh": 2,
        "regex": "",
        "skipUrlSync": false,
        "sort": 0,
        "tagValuesQuery": "",
        "tags": [],
        "tagsQuery": "",
        "type": "query",
        "useTags": false
      },
      {
        "allValue": null,
        "current": {
          "selected": false,
          "text": "All",
          "value": "$__all"
        },
        "datasource": "Prometheus",
        "definition": "label_values(com_iquantex_Phoenix_PhoenixClient_RpcSendSuccessTotal{kubernetes_namespace=~\"$namespace\"},service_name)",
        "hide": 0,
        "includeAll": true,
        "label": "appname",
        "multi": false,
        "name": "appname",
        "options": [],
        "query": "label_values(com_iquantex_Phoenix_PhoenixClient_RpcSendSuccessTotal{kubernetes_namespace=~\"$namespace\"},service_name)",
        "refresh": 2,
        "regex": "",
        "skipUrlSync": false,
        "sort": 0,
        "tagValuesQuery": "",
        "tags": [],
        "tagsQuery": "",
        "type": "query",
        "useTags": false
      },
      {
        "allValue": null,
        "current": {
          "selected": false,
          "text": "All",
          "value": "$__all"
        },
        "datasource": "Prometheus",
        "definition": "label_values(com_iquantex_Phoenix_PhoenixClient_RpcSendSuccessTotal{kubernetes_namespace=~\"$namespace\",service_name=~\"$appname\"},instance)",
        "hide": 0,
        "includeAll": true,
        "label": "instance",
        "multi": false,
        "name": "instance",
        "options": [],
        "query": "label_values(com_iquantex_Phoenix_PhoenixClient_RpcSendSuccessTotal{kubernetes_namespace=~\"$namespace\",service_name=~\"$appname\"},instance)",
        "refresh": 2,
        "regex": "",
        "skipUrlSync": false,
        "sort": 0,
        "tagValuesQuery": "",
        "tags": [],
        "tagsQuery": "",
        "type": "query",
        "useTags": false
      }
    ]
  },
  "time": {
    "from": "now-15m",
    "to": "now"
  },
  "timepicker": {
    "refresh_intervals": [
      "10s",
      "30s",
      "1m",
      "5m",
      "15m",
      "30m",
      "1h",
      "2h",
      "1d"
    ]
  },
  "timezone": "",
  "title": "07 phoenix client",
  "uid": "fqg9iDDMz",
  "version": 1
}
```

## phoenix event publish

```json
{
  "annotations": {
    "list": [
      {
        "builtIn": 1,
        "datasource": "-- Grafana --",
        "enable": true,
        "hide": true,
        "iconColor": "rgba(0, 211, 255, 1)",
        "name": "Annotations & Alerts",
        "type": "console"
      }
    ]
  },
  "editable": true,
  "gnetId": null,
  "graphTooltip": 0,
  "id": 7,
  "iteration": 1632909767989,
  "links": [],
  "panels": [
    {
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green",
                "value": null
              }
            ]
          }
        },
        "overrides": []
      },
      "gridPos": {
        "h": 6,
        "w": 12,
        "x": 0,
        "y": 0
      },
      "id": 2,
      "options": {
        "reduceOptions": {
          "calcs": [
            "delta"
          ],
          "fields": "",
          "values": false
        },
        "showThresholdLabels": false,
        "showThresholdMarkers": true
      },
      "pluginVersion": "7.1.1",
      "targets": [
        {
          "expr": "sum by()(com_iquantex_Phoenix_EventPublish_AfterFilterRows{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "读库总条数",
          "refId": "A"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_EventPublish_SendEventRows{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "发送事件总数",
          "refId": "B"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_EventPublish_SendMonitorRows{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "发送监控数据总数",
          "refId": "C"
        }
      ],
      "timeFrom": null,
      "timeShift": null,
      "title": "EventPublish关键指标",
      "type": "gauge"
    },
    {
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green",
                "value": null
              },
              {
                "color": "red",
                "value": 1
              }
            ]
          }
        },
        "overrides": []
      },
      "gridPos": {
        "h": 6,
        "w": 12,
        "x": 12,
        "y": 0
      },
      "id": 7,
      "options": {
        "reduceOptions": {
          "calcs": [
            "delta"
          ],
          "fields": "",
          "values": false
        },
        "showThresholdLabels": false,
        "showThresholdMarkers": true
      },
      "pluginVersion": "7.1.1",
      "targets": [
        {
          "expr": "sum by()(com_iquantex_Phoenix_EventPublish_WaitForAckTimeOutCount{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "同步发送失败次数",
          "refId": "C"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_EventPublish_ConvertToJsonErrorCount{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "异步发送失败次数",
          "refId": "D"
        }
      ],
      "timeFrom": null,
      "timeShift": null,
      "title": "异常指标",
      "type": "gauge"
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "description": "",
      "fieldConfig": {
        "defaults": {
          "custom": {}
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 15,
        "w": 12,
        "x": 0,
        "y": 6
      },
      "hiddenSeries": false,
      "id": 4,
      "legend": {
        "avg": false,
        "current": false,
        "max": false,
        "min": false,
        "show": true,
        "total": false,
        "values": false
      },
      "lines": true,
      "linewidth": 1,
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 2,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "sum by()(rate(com_iquantex_Phoenix_EventPublish_ReadRows{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "读库tps",
          "refId": "A"
        },
        {
          "expr": "sum by()(rate(com_iquantex_Phoenix_EventPublish_AfterFilterRows{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "过滤后tps",
          "refId": "D"
        },
        {
          "expr": "sum by()(rate(com_iquantex_Phoenix_EventPublish_SendMonitorRows{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "发送监控数据TPS",
          "refId": "B"
        },
        {
          "expr": "sum by()(rate(com_iquantex_Phoenix_EventPublish_SendEventRows{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "发送事件TPS",
          "refId": "C"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "EventPublish-TPS",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {}
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 15,
        "w": 12,
        "x": 12,
        "y": 6
      },
      "hiddenSeries": false,
      "id": 6,
      "legend": {
        "avg": false,
        "current": false,
        "max": false,
        "min": false,
        "show": true,
        "total": false,
        "values": false
      },
      "lines": true,
      "linewidth": 1,
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 2,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "sum by()(increase(com_iquantex_Phoenix_EventPublish_ReadDBMs{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))/sum by()(increase(com_iquantex_Phoenix_EventPublish_ReadDBCount{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "读库时延",
          "refId": "B"
        },
        {
          "expr": "sum by()(increase(com_iquantex_Phoenix_EventPublish_SortMs{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))/sum by()(increase(com_iquantex_Phoenix_EventPublish_SortCount{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "排序时延",
          "refId": "A"
        },
        {
          "expr": "sum by()(increase(com_iquantex_Phoenix_EventPublish_DeserializeMQMs{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))/sum by()(increase(com_iquantex_Phoenix_EventPublish_DeserializeMQCount{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "序列化消息时延",
          "refId": "E"
        },
        {
          "expr": "sum by()(increase(com_iquantex_Phoenix_EventPublish_SendEventMQMs{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))/sum by()(increase(com_iquantex_Phoenix_EventPublish_SendEventMQCount{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "发送事件时延",
          "refId": "D"
        },
        {
          "expr": "sum by()(increase(com_iquantex_Phoenix_EventPublish_SendMonitorMQMs{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))/sum by()(increase(com_iquantex_Phoenix_EventPublish_SendMonitorMQCount{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "发送监控数据时延",
          "refId": "C"
        },
        {
          "expr": "sum by()(increase(com_iquantex_Phoenix_EventPublish_SendMQMs{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))/sum by()(increase(com_iquantex_Phoenix_EventPublish_SendMQCount{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "发送mq总时延",
          "refId": "F"
        },
        {
          "expr": "sum by()(increase(com_iquantex_Phoenix_EventPublish_Progress{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))/sum by()(increase(com_iquantex_Phoenix_EventPublish_ProgressCount{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "事件存入到读取的时延",
          "refId": "G"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "EventPublish-时延",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    }
  ],
  "refresh": "10s",
  "schemaVersion": 26,
  "style": "dark",
  "tags": [
    "Phoenix"
  ],
  "templating": {
    "list": [
      {
        "allValue": null,
        "current": {
          "selected": false,
          "text": "All",
          "value": "$__all"
        },
        "datasource": "Prometheus",
        "definition": "label_values(com_iquantex_Phoenix_EventPublish_AfterFilterRows{},kubernetes_namespace)",
        "hide": 0,
        "includeAll": true,
        "label": "namespace",
        "multi": false,
        "name": "namespace",
        "options": [],
        "query": "label_values(com_iquantex_Phoenix_EventPublish_AfterFilterRows{},kubernetes_namespace)",
        "refresh": 2,
        "regex": "",
        "skipUrlSync": false,
        "sort": 1,
        "tagValuesQuery": "",
        "tags": [],
        "tagsQuery": "",
        "type": "query",
        "useTags": false
      },
      {
        "allValue": null,
        "current": {
          "selected": false,
          "text": "All",
          "value": "$__all"
        },
        "datasource": "Prometheus",
        "definition": "label_values(com_iquantex_Phoenix_EventPublish_AfterFilterRows{kubernetes_namespace=~\"$namespace\"},service_name)",
        "hide": 0,
        "includeAll": true,
        "label": "appname",
        "multi": false,
        "name": "appname",
        "options": [],
        "query": "label_values(com_iquantex_Phoenix_EventPublish_AfterFilterRows{kubernetes_namespace=~\"$namespace\"},service_name)",
        "refresh": 2,
        "regex": "",
        "skipUrlSync": false,
        "sort": 0,
        "tagValuesQuery": "",
        "tags": [],
        "tagsQuery": "",
        "type": "query",
        "useTags": false
      },
      {
        "allValue": null,
        "current": {
          "selected": false,
          "text": "All",
          "value": "$__all"
        },
        "datasource": "Prometheus",
        "definition": "label_values(com_iquantex_Phoenix_EventPublish_AfterFilterRows{kubernetes_namespace=~\"$namespace\",service_name=~\"$appname\"},instance)",
        "hide": 0,
        "includeAll": true,
        "label": "instance",
        "multi": false,
        "name": "instance",
        "options": [],
        "query": "label_values(com_iquantex_Phoenix_EventPublish_AfterFilterRows{kubernetes_namespace=~\"$namespace\",service_name=~\"$appname\"},instance)",
        "refresh": 2,
        "regex": "",
        "skipUrlSync": false,
        "sort": 1,
        "tagValuesQuery": "",
        "tags": [],
        "tagsQuery": "",
        "type": "query",
        "useTags": false
      }
    ]
  },
  "time": {
    "from": "now-30m",
    "to": "now"
  },
  "timepicker": {
    "refresh_intervals": [
      "10s",
      "30s",
      "1m",
      "5m",
      "15m",
      "30m",
      "1h",
      "2h",
      "1d"
    ]
  },
  "timezone": "",
  "title": "06 phoenix event publish",
  "uid": "1uz4XfHMk12",
  "version": 1
}
```

## phoenix event store 

```json
{
  "annotations": {
    "list": [
      {
        "builtIn": 1,
        "datasource": "-- Grafana --",
        "enable": true,
        "hide": true,
        "iconColor": "rgba(0, 211, 255, 1)",
        "name": "Annotations & Alerts",
        "type": "console"
      }
    ]
  },
  "description": "Complete console using metrics from prometheus JMX exporter, with drill down per job > instance",
  "editable": true,
  "gnetId": 8563,
  "graphTooltip": 0,
  "id": 5,
  "iteration": 1632909813239,
  "links": [],
  "panels": [
    {
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {
            "align": null
          },
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green",
                "value": null
              }
            ]
          }
        },
        "overrides": []
      },
      "gridPos": {
        "h": 6,
        "w": 13,
        "x": 0,
        "y": 0
      },
      "id": 102,
      "options": {
        "orientation": "auto",
        "reduceOptions": {
          "calcs": [
            "last"
          ],
          "fields": "",
          "values": false
        },
        "showThresholdLabels": false,
        "showThresholdMarkers": false
      },
      "pluginVersion": "7.1.1",
      "targets": [
        {
          "expr": "sum by()(com_iquantex_Phoenix_EventStore_AppendEventTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "插入事件总数",
          "refId": "I"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_EventStore_ReadTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "读事件总数",
          "refId": "B"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_EventStore_QueueSize{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "缓冲队列个数",
          "refId": "A"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_EventStore_ExecutorAppendTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "线程池处理次数",
          "refId": "C"
        }
      ],
      "timeFrom": null,
      "timeShift": null,
      "title": "EventStore",
      "type": "gauge"
    },
    {
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {
            "align": null
          },
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green",
                "value": null
              }
            ]
          }
        },
        "overrides": []
      },
      "gridPos": {
        "h": 6,
        "w": 11,
        "x": 13,
        "y": 0
      },
      "id": 111,
      "options": {
        "orientation": "auto",
        "reduceOptions": {
          "calcs": [
            "last"
          ],
          "fields": "",
          "values": false
        },
        "showThresholdLabels": false,
        "showThresholdMarkers": false
      },
      "pluginVersion": "7.1.1",
      "targets": [
        {
          "expr": "sum by()(com_iquantex_Phoenix_EventStore_TakeSnapshotTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "打快照总次数",
          "refId": "C"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_EventStore_TakeSnapshotExceptionTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "打快照异常",
          "refId": "B"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_EventStore_LoadSnapshotTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "加载快照总次数",
          "refId": "D"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_EventStore_LoadSnapshotExceptionTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "加载快照异常",
          "refId": "A"
        }
      ],
      "timeFrom": null,
      "timeShift": null,
      "title": "快照监控",
      "type": "gauge"
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 8,
        "w": 24,
        "x": 0,
        "y": 6
      },
      "hiddenSeries": false,
      "id": 59,
      "legend": {
        "avg": false,
        "current": false,
        "max": false,
        "min": false,
        "show": true,
        "total": false,
        "values": false
      },
      "lines": true,
      "linewidth": 1,
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 2,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "sum by(_label)(rate(com_iquantex_Phoenix_EventStore_AppendTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "Append TPS-{{_label}}",
          "refId": "B"
        },
        {
          "expr": "sum by(_label)(rate(com_iquantex_Phoenix_EventStore_AppendEventTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "Append Event TPS-{{_label}}",
          "refId": "A"
        },
        {
          "expr": "sum by(_label)(com_iquantex_Phoenix_EventStore_QueueSize{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "hide": false,
          "interval": "",
          "legendFormat": "队列大小-{{_label}}",
          "refId": "D"
        },
        {
          "expr": "sum by(_label)(rate(com_iquantex_Phoenix_EventStore_ReadTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "读TPS-{{_label}}",
          "refId": "E"
        },
        {
          "expr": "sum by(_label)(rate(com_iquantex_Phoenix_EventStore_ExecutorAppendTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "Executor-Append TPS-{{_label}}",
          "refId": "C"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "EventStore TPS",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "decimals": -2,
          "format": "short",
          "label": "",
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 8,
        "w": 24,
        "x": 0,
        "y": 14
      },
      "hiddenSeries": false,
      "id": 71,
      "legend": {
        "avg": false,
        "current": false,
        "max": false,
        "min": false,
        "show": true,
        "total": false,
        "values": false
      },
      "lines": true,
      "linewidth": 1,
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 2,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "sum by(_label)(increase(com_iquantex_Phoenix_EventStore_AppendLatencyTotalUs{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))/sum by(_label)(increase(com_iquantex_Phoenix_EventStore_AppendTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))/1000",
          "format": "time_series",
          "instant": false,
          "interval": "",
          "legendFormat": "Append Latency-{{_label}}",
          "refId": "F"
        },
        {
          "expr": "sum by(_label)(increase(com_iquantex_Phoenix_EventStore_AppendLatencyTotalUs{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))/sum by(_label)(increase(com_iquantex_Phoenix_EventStore_AppendEventTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))/1000",
          "format": "time_series",
          "instant": false,
          "interval": "",
          "legendFormat": "Append Event Latency-{{_label}}",
          "refId": "C"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "EventStore Latency",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "decimals": -2,
          "format": "short",
          "label": "",
          "logBase": 2,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {}
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 8,
        "w": 24,
        "x": 0,
        "y": 22
      },
      "hiddenSeries": false,
      "id": 107,
      "legend": {
        "alignAsTable": false,
        "avg": false,
        "current": false,
        "max": false,
        "min": false,
        "show": true,
        "total": false,
        "values": false
      },
      "lines": true,
      "linewidth": 1,
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 2,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "sum by(_label)(rate(com_iquantex_Phoenix_EventStore_TakeSnapshotTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "instant": false,
          "interval": "",
          "legendFormat": "Take Snapshot TPS{{_label}}",
          "refId": "A"
        },
        {
          "expr": "sum by(_label)(rate(com_iquantex_Phoenix_EventStore_LoadSnapshotTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "instant": false,
          "interval": "",
          "legendFormat": "Load Snapshot TPS{{_label}}",
          "refId": "B"
        },
        {
          "expr": "sum by(_label)(rate(com_iquantex_Phoenix_EventStore_LoadSnapshotExceptionTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "Load Snapshot Exception TPS{{_label}}",
          "refId": "C"
        },
        {
          "expr": "sum by(_label)(rate(com_iquantex_Phoenix_EventStore_TakeSnapshotExceptionTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "Take Snapshot Exception TPS{{_label}}",
          "refId": "D"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "Snapshot TPS",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "decimals": 2,
          "format": "short",
          "label": null,
          "logBase": 2,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "decimals": null,
          "format": "short",
          "label": "",
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {}
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 8,
        "w": 24,
        "x": 0,
        "y": 30
      },
      "hiddenSeries": false,
      "id": 109,
      "legend": {
        "avg": false,
        "current": false,
        "max": false,
        "min": false,
        "show": true,
        "total": false,
        "values": false
      },
      "lines": true,
      "linewidth": 1,
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 2,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "sum by(_label)(increase(com_iquantex_Phoenix_EventStore_TakeSnapshotLatencyTotalUs{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))/sum by(_label)(increase(com_iquantex_Phoenix_EventStore_TakeSnapshotTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "Take Snapshot Latency {{_label}}",
          "refId": "A"
        },
        {
          "expr": "sum by(_label)(increase(com_iquantex_Phoenix_EventStore_LoadSnapshotLatencyTotalUs{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))/sum by(_label)(increase(com_iquantex_Phoenix_EventStore_LoadSnapshotTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "Load Snapshot Latency {{_label}}",
          "refId": "B"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "Snapshot Latency",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "decimals": null,
          "format": "short",
          "label": null,
          "logBase": 2,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    }
  ],
  "refresh": "10s",
  "schemaVersion": 26,
  "style": "dark",
  "tags": [
    "Phoenix"
  ],
  "templating": {
    "list": [
      {
        "allValue": null,
        "current": {
          "selected": false,
          "text": "All",
          "value": "$__all"
        },
        "datasource": "Prometheus",
        "definition": "label_values(com_iquantex_Phoenix_TransactionReliability_NewTransTotal{},kubernetes_namespace)",
        "hide": 0,
        "includeAll": true,
        "label": "namespace",
        "multi": false,
        "name": "namespace",
        "options": [],
        "query": "label_values(com_iquantex_Phoenix_TransactionReliability_NewTransTotal{},kubernetes_namespace)",
        "refresh": 2,
        "regex": "",
        "skipUrlSync": false,
        "sort": 1,
        "tagValuesQuery": "",
        "tags": [],
        "tagsQuery": "",
        "type": "query",
        "useTags": false
      },
      {
        "allValue": null,
        "current": {
          "selected": false,
          "text": "account-server",
          "value": "account-server"
        },
        "datasource": "Prometheus",
        "definition": "label_values(com_iquantex_Phoenix_TransactionReliability_NewTransTotal{kubernetes_namespace=~\"$namespace\"},service_name)",
        "hide": 0,
        "includeAll": true,
        "label": "appname",
        "multi": false,
        "name": "appname",
        "options": [],
        "query": "label_values(com_iquantex_Phoenix_TransactionReliability_NewTransTotal{kubernetes_namespace=~\"$namespace\"},service_name)",
        "refresh": 2,
        "regex": "",
        "skipUrlSync": false,
        "sort": 0,
        "tagValuesQuery": "",
        "tags": [],
        "tagsQuery": "",
        "type": "query",
        "useTags": false
      },
      {
        "allValue": null,
        "current": {
          "selected": false,
          "text": "All",
          "value": "$__all"
        },
        "datasource": "Prometheus",
        "definition": "label_values(jvm_info{kubernetes_namespace=~\"$namespace\",service_name=~\"$appname\"},instance)",
        "hide": 0,
        "includeAll": true,
        "label": "instance",
        "multi": false,
        "name": "instance",
        "options": [],
        "query": "label_values(jvm_info{kubernetes_namespace=~\"$namespace\",service_name=~\"$appname\"},instance)",
        "refresh": 2,
        "regex": "",
        "skipUrlSync": false,
        "sort": 0,
        "tagValuesQuery": "",
        "tags": [],
        "tagsQuery": "",
        "type": "query",
        "useTags": false
      }
    ]
  },
  "time": {
    "from": "now-5m",
    "to": "now"
  },
  "timepicker": {
    "refresh_intervals": [
      "10s",
      "30s",
      "1m",
      "5m"
    ],
    "time_options": [
      "5m",
      "15m",
      "1h",
      "6h",
      "12h",
      "24h",
      "2d",
      "7d",
      "30d"
    ]
  },
  "timezone": "",
  "title": "04 phoenix event store",
  "uid": "qeNw2aH7k",
  "version": 1
}
```

## phoenix transaction aggregate 

```json

{
  "annotations": {
    "list": [
      {
        "builtIn": 1,
        "datasource": "-- Grafana --",
        "enable": true,
        "hide": true,
        "iconColor": "rgba(0, 211, 255, 1)",
        "name": "Annotations & Alerts",
        "type": "console"
      }
    ]
  },
  "description": "Complete console using metrics from prometheus JMX exporter, with drill down per job > instance",
  "editable": true,
  "gnetId": 8563,
  "graphTooltip": 0,
  "id": 4,
  "iteration": 1632909850890,
  "links": [],
  "panels": [
    {
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {
            "align": null
          },
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green",
                "value": null
              },
              {
                "color": "red",
                "value": 80
              }
            ]
          }
        },
        "overrides": []
      },
      "gridPos": {
        "h": 6,
        "w": 16,
        "x": 0,
        "y": 0
      },
      "id": 100,
      "options": {
        "orientation": "auto",
        "reduceOptions": {
          "calcs": [
            "last"
          ],
          "fields": "",
          "values": false
        },
        "showThresholdLabels": false,
        "showThresholdMarkers": true
      },
      "pluginVersion": "7.1.1",
      "targets": [
        {
          "expr": "sum by()(com_iquantex_Phoenix_TransactionAggregateManager_EsAggregateTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "事务聚合根重构",
          "refId": "K"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_TransactionAggregateManager_AppendIdempotentConflictTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "事务聚合根唯一索引冲突",
          "refId": "M"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_TransactionAggregateManager_AppendPrimaryKeyConflictTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "事务聚合根主键冲突",
          "refId": "N"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_TransactionAggregateManager_AppendExceptionTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "事务聚合根写入异常",
          "refId": "O"
        }
      ],
      "timeFrom": null,
      "timeShift": null,
      "title": "事务聚合根指标",
      "type": "gauge"
    },
    {
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green",
                "value": null
              },
              {
                "color": "orange",
                "value": 1
              }
            ]
          }
        },
        "overrides": []
      },
      "gridPos": {
        "h": 6,
        "w": 8,
        "x": 16,
        "y": 0
      },
      "id": 121,
      "options": {
        "reduceOptions": {
          "calcs": [
            "last"
          ],
          "fields": "",
          "values": false
        },
        "showThresholdLabels": false,
        "showThresholdMarkers": true
      },
      "pluginVersion": "7.1.1",
      "targets": [
        {
          "expr": "sum by()(com_iquantex_Phoenix_TransactionAggregateActor_CurrentActorTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "当前存活的事务Actor",
          "refId": "A"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_TransactionAggregateActor_HeartbeatTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "累计接收心跳个数",
          "refId": "B"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_TransactionAggregateActor_RetryMsgTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "重试消息数量",
          "refId": "C"
        }
      ],
      "timeFrom": null,
      "timeShift": null,
      "title": "事务actor",
      "type": "gauge"
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 13,
        "w": 24,
        "x": 0,
        "y": 6
      },
      "hiddenSeries": false,
      "id": 63,
      "legend": {
        "alignAsTable": true,
        "avg": true,
        "current": false,
        "max": true,
        "min": true,
        "show": true,
        "total": false,
        "values": true
      },
      "lines": true,
      "linewidth": 1,
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 2,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "sum by() (rate(com_iquantex_Phoenix_TransactionAggregateManager_HandleTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "Handle TPS",
          "refId": "A"
        },
        {
          "expr": "sum by() (rate(com_iquantex_Phoenix_TransactionAggregateManager_AppendTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "Append TPS",
          "refId": "D"
        },
        {
          "expr": "sum by()(rate(com_iquantex_Phoenix_TransactionAggregateManager_IdempotentTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "幂等处理",
          "refId": "B"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "TransactionAggregateManager TPS",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 13,
        "w": 24,
        "x": 0,
        "y": 19
      },
      "hiddenSeries": false,
      "id": 72,
      "legend": {
        "alignAsTable": true,
        "avg": true,
        "current": false,
        "max": true,
        "min": true,
        "show": true,
        "total": false,
        "values": true
      },
      "lines": true,
      "linewidth": 1,
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 2,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "sum by ()(increase(com_iquantex_Phoenix_TransactionAggregateManager_HandleLatencyTotalUs{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))/sum by ()(increase(com_iquantex_Phoenix_TransactionAggregateManager_HandleTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))/1000",
          "interval": "",
          "legendFormat": "Handle Latency",
          "refId": "B"
        },
        {
          "expr": "sum by ()(increase(com_iquantex_Phoenix_TransactionAggregateManager_AppendLatencyTotalUs{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))/sum by ()(increase(com_iquantex_Phoenix_TransactionAggregateManager_AppendTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))/1000",
          "interval": "",
          "legendFormat": "Append Latency",
          "refId": "C"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "TransactionAggregateManager Latency",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green",
                "value": null
              },
              {
                "color": "red",
                "value": 80
              }
            ]
          }
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 9,
        "w": 24,
        "x": 0,
        "y": 32
      },
      "hiddenSeries": false,
      "id": 119,
      "legend": {
        "avg": false,
        "current": false,
        "max": false,
        "min": false,
        "show": true,
        "total": false,
        "values": false
      },
      "lines": true,
      "linewidth": 1,
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 2,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "sum by()(com_iquantex_Phoenix_TransactionAggregateActor_CurrentActorTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "当前存活事务",
          "refId": "A"
        },
        {
          "expr": "sum by()(rate(com_iquantex_Phoenix_TransactionAggregateActor_HeartbeatTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "心跳",
          "refId": "B"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "事务实时指标统计",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    }
  ],
  "refresh": "10s",
  "schemaVersion": 26,
  "style": "dark",
  "tags": [
    "Phoenix"
  ],
  "templating": {
    "list": [
      {
        "allValue": null,
        "current": {
          "selected": false,
          "text": "All",
          "value": "$__all"
        },
        "datasource": "Prometheus",
        "definition": "label_values(com_iquantex_Phoenix_TransactionReliability_NewTransTotal{},kubernetes_namespace)",
        "hide": 0,
        "includeAll": true,
        "label": "namespace",
        "multi": false,
        "name": "namespace",
        "options": [],
        "query": "label_values(com_iquantex_Phoenix_TransactionReliability_NewTransTotal{},kubernetes_namespace)",
        "refresh": 2,
        "regex": "",
        "skipUrlSync": false,
        "sort": 1,
        "tagValuesQuery": "",
        "tags": [],
        "tagsQuery": "",
        "type": "query",
        "useTags": false
      },
      {
        "allValue": null,
        "current": {
          "selected": false,
          "text": "All",
          "value": "$__all"
        },
        "datasource": "Prometheus",
        "definition": "label_values(com_iquantex_Phoenix_TransactionReliability_NewTransTotal{kubernetes_namespace=~\"$namespace\"},service_name)",
        "hide": 0,
        "includeAll": true,
        "label": "appname",
        "multi": false,
        "name": "appname",
        "options": [],
        "query": "label_values(com_iquantex_Phoenix_TransactionReliability_NewTransTotal{kubernetes_namespace=~\"$namespace\"},service_name)",
        "refresh": 2,
        "regex": "",
        "skipUrlSync": false,
        "sort": 0,
        "tagValuesQuery": "",
        "tags": [],
        "tagsQuery": "",
        "type": "query",
        "useTags": false
      },
      {
        "allValue": null,
        "current": {
          "selected": false,
          "text": "All",
          "value": "$__all"
        },
        "datasource": "Prometheus",
        "definition": "label_values(jvm_info{kubernetes_namespace=~\"$namespace\",service_name=~\"$appname\"},instance)",
        "hide": 0,
        "includeAll": true,
        "label": "instance",
        "multi": false,
        "name": "instance",
        "options": [],
        "query": "label_values(jvm_info{kubernetes_namespace=~\"$namespace\",service_name=~\"$appname\"},instance)",
        "refresh": 2,
        "regex": "",
        "skipUrlSync": false,
        "sort": 0,
        "tagValuesQuery": "",
        "tags": [],
        "tagsQuery": "",
        "type": "query",
        "useTags": false
      }
    ]
  },
  "time": {
    "from": "now-5m",
    "to": "now"
  },
  "timepicker": {
    "refresh_intervals": [
      "10s",
      "30s",
      "1m",
      "5m"
    ],
    "time_options": [
      "5m",
      "15m",
      "1h",
      "6h",
      "12h",
      "24h",
      "2d",
      "7d",
      "30d"
    ]
  },
  "timezone": "",
  "title": "03 phoenix transaction aggregate",
  "uid": "EefwU7NGz12s2",
  "version": 1
}
```

## phoenix entity aggregate

```json
{
  "annotations": {
    "list": [
      {
        "builtIn": 1,
        "datasource": "-- Grafana --",
        "enable": true,
        "hide": true,
        "iconColor": "rgba(0, 211, 255, 1)",
        "name": "Annotations & Alerts",
        "type": "console"
      }
    ]
  },
  "description": "Complete console using metrics from prometheus JMX exporter, with drill down per job > instance",
  "editable": true,
  "gnetId": 8563,
  "graphTooltip": 0,
  "id": 3,
  "iteration": 1632909873707,
  "links": [],
  "panels": [
    {
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {
            "align": null
          },
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green",
                "value": null
              },
              {
                "color": "red",
                "value": 1
              }
            ]
          }
        },
        "overrides": []
      },
      "gridPos": {
        "h": 5,
        "w": 15,
        "x": 0,
        "y": 0
      },
      "id": 61,
      "options": {
        "orientation": "auto",
        "reduceOptions": {
          "calcs": [
            "last"
          ],
          "fields": "",
          "values": false
        },
        "showThresholdLabels": false,
        "showThresholdMarkers": true
      },
      "pluginVersion": "7.1.1",
      "targets": [
        {
          "expr": "sum by()(com_iquantex_Phoenix_EntityAggregateManager_ClearAggregateTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType=~\"[[aggregateRootType]]\"})",
          "interval": "",
          "legendFormat": "实体聚合根清理数量",
          "refId": "D"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_EntityAggregateManager_AppendPrimaryKeyConflictTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType=~\"[[aggregateRootType]]\"})",
          "interval": "",
          "legendFormat": "实体聚合根主键冲突",
          "refId": "F"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_EntityAggregateManager_AppendIdempotentConflictTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType=~\"[[aggregateRootType]]\"})",
          "interval": "",
          "legendFormat": "实体聚合根唯一索引冲突",
          "refId": "G"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_EntityAggregateManager_AppendExceptionTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType=~\"[[aggregateRootType]]\"})",
          "interval": "",
          "legendFormat": " 实体聚合根写入异常",
          "refId": "H"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_EntityAggregateManager_BatchExecuteFailTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType=~\"[[aggregateRootType]]\"})",
          "interval": "",
          "legendFormat": "批处理失败次数",
          "refId": "A"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_EntityAggregateManager_BatchAppendFailTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType=~\"[[aggregateRootType]]\"})",
          "interval": "",
          "legendFormat": "批处理失败次数(写入异常)",
          "refId": "B"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_EntityAggregateManager_BatchApplyFailTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType=~\"[[aggregateRootType]]\"})",
          "interval": "",
          "legendFormat": "批处理失败次数(apply异常)",
          "refId": "C"
        }
      ],
      "timeFrom": null,
      "timeShift": null,
      "title": "实体聚合根指标",
      "type": "gauge"
    },
    {
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {
            "align": null
          },
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green",
                "value": null
              },
              {
                "color": "red",
                "value": 80
              }
            ]
          }
        },
        "overrides": []
      },
      "gridPos": {
        "h": 5,
        "w": 9,
        "x": 15,
        "y": 0
      },
      "id": 99,
      "options": {
        "reduceOptions": {
          "calcs": [
            "last"
          ],
          "fields": "",
          "values": false
        },
        "showThresholdLabels": false,
        "showThresholdMarkers": true
      },
      "pluginVersion": "7.1.1",
      "targets": [
        {
          "expr": "sum by()(com_iquantex_Phoenix_EntityAggregateManager_IdempotentByCacheTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType=~\"[[aggregateRootType]]\"})",
          "interval": "",
          "legendFormat": "实体聚合根内存幂等",
          "refId": "T"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_EntityAggregateManager_IdempotentByDBTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType=~\"[[aggregateRootType]]\"})",
          "interval": "",
          "legendFormat": "实体聚合根数据库幂等",
          "refId": "J"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_EntityAggregateManager_BloomFilterMightContainTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType=~\"[[aggregateRootType]]\"})",
          "interval": "",
          "legendFormat": "布隆过滤器误判次数",
          "refId": "S"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_EntityAggregateManager_BloomFilterDecayingTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType=~\"[[aggregateRootType]]\"})",
          "interval": "",
          "legendFormat": "布隆过滤器衰变次数",
          "refId": "A"
        }
      ],
      "timeFrom": null,
      "timeShift": null,
      "title": "实体聚合根幂等指标",
      "type": "gauge"
    },
    {
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {
            "align": null
          },
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green",
                "value": null
              }
            ]
          }
        },
        "overrides": []
      },
      "gridPos": {
        "h": 5,
        "w": 15,
        "x": 0,
        "y": 5
      },
      "id": 103,
      "options": {
        "orientation": "auto",
        "reduceOptions": {
          "calcs": [
            "lastNotNull"
          ],
          "fields": "",
          "values": false
        },
        "showThresholdLabels": false,
        "showThresholdMarkers": true
      },
      "pluginVersion": "7.1.1",
      "targets": [
        {
          "expr": "sum by(_aggregateRootType)(com_iquantex_Phoenix_EntityAggregateManager_AliveAggregateTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "{{_aggregateRootType}}",
          "refId": "I"
        }
      ],
      "timeFrom": null,
      "timeShift": null,
      "title": "实体聚合根数量",
      "type": "gauge"
    },
    {
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {
            "align": "center",
            "displayMode": "color-background"
          },
          "mappings": [],
          "thresholds": {
            "mode": "percentage",
            "steps": [
              {
                "color": "green",
                "value": null
              },
              {
                "color": "red",
                "value": 80
              },
              {
                "color": "#EAB839",
                "value": 90
              },
              {
                "color": "#6ED0E0",
                "value": 100
              }
            ]
          },
          "unit": "dateTimeAsIso"
        },
        "overrides": []
      },
      "gridPos": {
        "h": 5,
        "w": 9,
        "x": 15,
        "y": 5
      },
      "id": 106,
      "options": {
        "frameIndex": 0,
        "showHeader": true
      },
      "pluginVersion": "7.1.1",
      "targets": [
        {
          "expr": "(sum(com_iquantex_Phoenix_AggregateRepository_StartEsTime) by(_name))",
          "format": "table",
          "instant": true,
          "interval": "",
          "legendFormat": "{{_name}}",
          "refId": "A"
        }
      ],
      "timeFrom": null,
      "timeShift": null,
      "title": "当前正在恢复状态的聚合根",
      "transformations": [
        {
          "id": "organize",
          "options": {
            "excludeByName": {
              "Time": true,
              "Value #A": true
            },
            "indexByName": {},
            "renameByName": {
              "Value": "开始恢复时间",
              "_name": "聚合根ID"
            }
          }
        }
      ],
      "type": "table"
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "description": "",
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 15,
        "w": 24,
        "x": 0,
        "y": 10
      },
      "hiddenSeries": false,
      "id": 104,
      "legend": {
        "alignAsTable": true,
        "avg": true,
        "current": false,
        "max": true,
        "min": true,
        "show": true,
        "total": false,
        "values": true
      },
      "lines": true,
      "linewidth": 1,
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 2,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "sum by ()(rate(com_iquantex_Phoenix_EntityAggregateManager_HandleTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType!=\"TransactionReliability\", _aggregateRootType=~\"[[aggregateRootType]]\"}[30s]))",
          "interval": "",
          "legendFormat": "Handle TPS",
          "refId": "D"
        },
        {
          "expr": "sum by ()(rate(com_iquantex_Phoenix_EntityAggregateManager_AppendTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType!=\"TransactionReliability\", _aggregateRootType=~\"[[aggregateRootType]]\"}[30s]))",
          "interval": "",
          "legendFormat": "Append TPS",
          "refId": "F"
        },
        {
          "expr": "sum by ()(rate(com_iquantex_Phoenix_EntityAggregateManager_HandleMsgTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType!=\"TransactionReliability\", _aggregateRootType=~\"[[aggregateRootType]]\"}[30s]))",
          "interval": "",
          "legendFormat": "Handle Msg  TPS",
          "refId": "E"
        },
        {
          "expr": "sum by ()(rate(com_iquantex_Phoenix_EntityAggregateManager_AppendEventTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType!=\"TransactionReliability\", _aggregateRootType=~\"[[aggregateRootType]]\"}[30s]))",
          "interval": "",
          "legendFormat": "Append Event TPS",
          "refId": "B"
        },
        {
          "expr": "sum by()(rate(com_iquantex_Phoenix_EntityAggregateManager_IdempotentByCacheTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType=~\"[[aggregateRootType]]\"}[30s]))",
          "interval": "",
          "legendFormat": "内存幂等TPS",
          "refId": "G"
        },
        {
          "expr": "sum by()(rate(com_iquantex_Phoenix_EntityAggregateManager_BloomFilterMightContainTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType=~\"[[aggregateRootType]]\"}[30s]))",
          "interval": "",
          "legendFormat": "布隆过滤器误判TPS",
          "refId": "I"
        },
        {
          "expr": "sum by()(rate(com_iquantex_Phoenix_EntityAggregateManager_IdempotentByDBTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType!=\"TransactionReliability\", _aggregateRootType=~\"[[aggregateRootType]]\"}[30s]))",
          "interval": "",
          "legendFormat": "数据库幂等TPS",
          "refId": "A"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_EntityAggregateManager_AliveAggregateTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType=~\"[[aggregateRootType]]\"})",
          "interval": "",
          "legendFormat": "内存中实体聚合根数量",
          "refId": "H"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "实体聚合根处理TPS",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 13,
        "w": 24,
        "x": 0,
        "y": 25
      },
      "hiddenSeries": false,
      "id": 70,
      "legend": {
        "alignAsTable": true,
        "avg": true,
        "current": false,
        "max": true,
        "min": true,
        "show": true,
        "total": false,
        "values": true
      },
      "lines": true,
      "linewidth": 1,
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 2,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "sum by ()(increase(com_iquantex_Phoenix_EntityAggregateManager_HandleLatencyTotalUs{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType!=\"TransactionReliability\"}[1m]))/sum by ()(increase(com_iquantex_Phoenix_EntityAggregateManager_HandleTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType=~\"[[aggregateRootType]]\"}[1m]))/1000",
          "interval": "",
          "legendFormat": "Handle Latency",
          "refId": "A"
        },
        {
          "expr": "sum by ()(increase(com_iquantex_Phoenix_EntityAggregateManager_HandleLatencyTotalUs{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType!=\"TransactionReliability\"}[1m]))/sum by ()(increase(com_iquantex_Phoenix_EntityAggregateManager_HandleMsgTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType=~\"[[aggregateRootType]]\"}[1m]))/1000",
          "interval": "",
          "legendFormat": "Handle MSG  Latency",
          "refId": "F"
        },
        {
          "expr": "sum by ()(increase(com_iquantex_Phoenix_EntityAggregateManager_AppendLatencyTotalUs{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType!=\"TransactionReliability\"}[1m]))/sum by ()(increase(com_iquantex_Phoenix_EntityAggregateManager_AppendEventTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType=~\"[[aggregateRootType]]\"}[1m]))/1000",
          "interval": "",
          "legendFormat": "Append Event Latency",
          "refId": "C"
        },
        {
          "expr": "sum by ()(increase(com_iquantex_Phoenix_EntityAggregateManager_HandleWithoutIOLatencyTotalUs{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType!=\"TransactionReliability\"}[1m]))/sum by ()(increase(com_iquantex_Phoenix_EntityAggregateManager_HandleMsgTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType=~\"[[aggregateRootType]]\"}[1m]))/1000",
          "interval": "",
          "legendFormat": "Handle MSG  NIO Latency",
          "refId": "B"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "实体聚合根处理延时",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "description": "",
      "fieldConfig": {
        "defaults": {
          "custom": {}
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 9,
        "w": 24,
        "x": 0,
        "y": 38
      },
      "hiddenSeries": false,
      "id": 108,
      "legend": {
        "avg": false,
        "current": false,
        "max": false,
        "min": false,
        "show": true,
        "total": false,
        "values": false
      },
      "lines": true,
      "linewidth": 1,
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 2,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "sum by()(rate(com_iquantex_Phoenix_EntityAggregateManager_EsHistoryAggregateTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "历史状态查询次数",
          "refId": "A"
        },
        {
          "expr": "sum by()(increase(com_iquantex_Phoenix_EntityAggregateManager_HistoryQueryTotalUs{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s])) / sum by()(increase(com_iquantex_Phoenix_EntityAggregateManager_EsHistoryAggregateTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "历史状态平均处理时延",
          "refId": "B"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "历史状态查询指标",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    }
  ],
  "refresh": "10s",
  "schemaVersion": 26,
  "style": "dark",
  "tags": [
    "Phoenix"
  ],
  "templating": {
    "list": [
      {
        "allValue": null,
        "current": {
          "selected": false,
          "text": "All",
          "value": "$__all"
        },
        "datasource": "Prometheus",
        "definition": "label_values(com_iquantex_Phoenix_TransactionReliability_NewTransTotal{},kubernetes_namespace)",
        "hide": 0,
        "includeAll": true,
        "label": "namespace",
        "multi": false,
        "name": "namespace",
        "options": [],
        "query": "label_values(com_iquantex_Phoenix_TransactionReliability_NewTransTotal{},kubernetes_namespace)",
        "refresh": 2,
        "regex": "",
        "skipUrlSync": false,
        "sort": 1,
        "tagValuesQuery": "",
        "tags": [],
        "tagsQuery": "",
        "type": "query",
        "useTags": false
      },
      {
        "allValue": null,
        "current": {
          "selected": false,
          "text": "All",
          "value": "$__all"
        },
        "datasource": "Prometheus",
        "definition": "label_values(com_iquantex_Phoenix_TransactionReliability_NewTransTotal{kubernetes_namespace=~\"$namespace\"},service_name)",
        "hide": 0,
        "includeAll": true,
        "label": "appname",
        "multi": false,
        "name": "appname",
        "options": [],
        "query": "label_values(com_iquantex_Phoenix_TransactionReliability_NewTransTotal{kubernetes_namespace=~\"$namespace\"},service_name)",
        "refresh": 2,
        "regex": "",
        "skipUrlSync": false,
        "sort": 0,
        "tagValuesQuery": "",
        "tags": [],
        "tagsQuery": "",
        "type": "query",
        "useTags": false
      },
      {
        "allValue": null,
        "current": {
          "selected": false,
          "text": "All",
          "value": "$__all"
        },
        "datasource": "Prometheus",
        "definition": "label_values(jvm_info{kubernetes_namespace=~\"$namespace\",service_name=~\"$appname\"},instance)",
        "hide": 0,
        "includeAll": true,
        "label": "instance",
        "multi": false,
        "name": "instance",
        "options": [],
        "query": "label_values(jvm_info{kubernetes_namespace=~\"$namespace\",service_name=~\"$appname\"},instance)",
        "refresh": 2,
        "regex": "",
        "skipUrlSync": false,
        "sort": 0,
        "tagValuesQuery": "",
        "tags": [],
        "tagsQuery": "",
        "type": "query",
        "useTags": false
      },
      {
        "allValue": null,
        "current": {
          "selected": false,
          "text": "All",
          "value": "$__all"
        },
        "datasource": "Prometheus",
        "definition": "label_values(com_iquantex_Phoenix_EntityAggregateManager_AliveAggregateTotal{kubernetes_namespace=~\"$namespace\",service_name=~\"$appname\"},_aggregateRootType)",
        "hide": 0,
        "includeAll": true,
        "label": "aggregateRootType",
        "multi": false,
        "name": "aggregateRootType",
        "options": [],
        "query": "label_values(com_iquantex_Phoenix_EntityAggregateManager_AliveAggregateTotal{kubernetes_namespace=~\"$namespace\",service_name=~\"$appname\"},_aggregateRootType)",
        "refresh": 2,
        "regex": "",
        "skipUrlSync": false,
        "sort": 0,
        "tagValuesQuery": "",
        "tags": [],
        "tagsQuery": "",
        "type": "query",
        "useTags": false
      }
    ]
  },
  "time": {
    "from": "now-5m",
    "to": "now"
  },
  "timepicker": {
    "refresh_intervals": [
      "10s",
      "30s",
      "1m",
      "5m"
    ],
    "time_options": [
      "5m",
      "15m",
      "1h",
      "6h",
      "12h",
      "24h",
      "2d",
      "7d",
      "30d"
    ]
  },
  "timezone": "",
  "title": "02 phoenix entity aggregate",
  "uid": "EefwU7NGz12se",
  "version": 1
}
```

## phoenix source aggregate

```json
{
  "annotations": {
    "list": [
      {
        "builtIn": 1,
        "datasource": "-- Grafana --",
        "enable": true,
        "hide": true,
        "iconColor": "rgba(0, 211, 255, 1)",
        "name": "Annotations & Alerts",
        "type": "console"
      }
    ]
  },
  "description": "Complete console using metrics from prometheus JMX exporter, with drill down per job > instance",
  "editable": true,
  "gnetId": 8563,
  "graphTooltip": 0,
  "id": 2,
  "iteration": 1632909902068,
  "links": [],
  "panels": [
    {
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {
            "align": null
          },
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green",
                "value": null
              }
            ]
          }
        },
        "overrides": []
      },
      "gridPos": {
        "h": 5,
        "w": 17,
        "x": 0,
        "y": 0
      },
      "id": 95,
      "options": {
        "orientation": "auto",
        "reduceOptions": {
          "calcs": [
            "diff"
          ],
          "fields": "",
          "values": false
        },
        "showThresholdLabels": false,
        "showThresholdMarkers": true
      },
      "pluginVersion": "7.1.1",
      "targets": [
        {
          "expr": "sum by()(com_iquantex_Phoenix_TransactionReliability_NewTransTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "instant": false,
          "interval": "",
          "legendFormat": "总事务",
          "refId": "A"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_TransactionReliability_FinishTransTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "已完成事务",
          "refId": "B"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_TransactionReliability_RetryTransTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "事务重试",
          "refId": "D"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_TransactionReliability_RemoveTransTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "移除事务",
          "refId": "P"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_TransactionReliability_SuccessFinishTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "成功事务",
          "refId": "C"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_TransactionReliability_FailFinishTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "失败事务",
          "refId": "E"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_TransactionReliability_ExceptionFinishTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "异常事务",
          "refId": "F"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_TransactionReliability_LimitCount{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "限流次数",
          "refId": "G"
        }
      ],
      "timeFrom": null,
      "timeShift": null,
      "title": "事务指标",
      "type": "gauge"
    },
    {
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {
            "align": null
          },
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green",
                "value": null
              },
              {
                "color": "red",
                "value": 1
              }
            ]
          }
        },
        "overrides": []
      },
      "gridPos": {
        "h": 5,
        "w": 7,
        "x": 17,
        "y": 0
      },
      "id": 97,
      "options": {
        "orientation": "auto",
        "reduceOptions": {
          "calcs": [
            "last"
          ],
          "fields": "",
          "values": false
        },
        "showThresholdLabels": false,
        "showThresholdMarkers": true
      },
      "pluginVersion": "7.1.1",
      "targets": [
        {
          "expr": "sum by()(com_iquantex_Phoenix_TransactionReliability_LiveTransTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "未完成事务个数",
          "refId": "A"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_ReceiverActor_NoHandlerMessageTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "本集群不处理的消息",
          "refId": "I"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_ReceiverActor_DeserializationFailTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "反序列化异常",
          "refId": "R"
        }
      ],
      "timeFrom": null,
      "timeShift": null,
      "title": "异常消息",
      "type": "gauge"
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 8,
        "w": 24,
        "x": 0,
        "y": 5
      },
      "hiddenSeries": false,
      "id": 82,
      "legend": {
        "avg": false,
        "current": false,
        "max": false,
        "min": false,
        "show": true,
        "total": false,
        "values": false
      },
      "lines": true,
      "linewidth": 1,
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 2,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "sum by()(increase(com_iquantex_Phoenix_TransactionReliability_FinishTransLatencyTotalMs{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))/sum by()(increase(com_iquantex_Phoenix_TransactionReliability_FinishTransTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "事务延时",
          "refId": "A"
        },
        {
          "expr": "sum by()(increase(com_iquantex_Phoenix_LimitMetric_RemoveLatencyTotalMs{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))/sum by()(increase(com_iquantex_Phoenix_LimitMetric_RemoveCount{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "事情延时",
          "refId": "B"
        },
        {
          "expr": "sum by ()(increase(com_iquantex_Phoenix_EntityAggregateManager_HandleWithoutIOLatencyTotalUs{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[1m]))/sum by ()(increase(com_iquantex_Phoenix_EntityAggregateManager_HandleMsgTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[1m]))/1000",
          "interval": "",
          "legendFormat": "NIO业务处理耗时",
          "refId": "C"
        },
        {
          "expr": "sum by ()(increase(com_iquantex_Phoenix_ReceiverActor_MqLatencyTotalMs{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))/sum by ()(increase(com_iquantex_Phoenix_ReceiverActor_RecvMsgTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "消息在mq中的耗时",
          "refId": "D"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "关键延时",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {}
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 8,
        "w": 24,
        "x": 0,
        "y": 13
      },
      "hiddenSeries": false,
      "id": 86,
      "legend": {
        "avg": false,
        "current": false,
        "max": false,
        "min": false,
        "show": true,
        "total": false,
        "values": false
      },
      "lines": true,
      "linewidth": 1,
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 2,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "sum by()(rate(com_iquantex_Phoenix_ReceiverActor_RecvMsgTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "recvRE",
          "refId": "E"
        },
        {
          "expr": "sum by()(rate(com_iquantex_Phoenix_ActorSentRecv_SentTotal{_actorType=\"entity-aggregate\" ,kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "sentEA",
          "refId": "D"
        },
        {
          "expr": "sum by()(rate(com_iquantex_Phoenix_ActorSentRecv_RecvTotal{_actorType=\"entity-aggregate\",kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "recvEA",
          "refId": "B"
        },
        {
          "expr": "sum by()(rate(com_iquantex_Phoenix_ActorSentRecv_SentTotal{_actorType=\"transaction-aggregate\",kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "sendTA",
          "refId": "C"
        },
        {
          "expr": "sum by()(rate(com_iquantex_Phoenix_ActorSentRecv_RecvTotal{_actorType=\"transaction-aggregate\",kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "recvTA",
          "refId": "A"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "关键流速",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 11,
        "w": 24,
        "x": 0,
        "y": 21
      },
      "hiddenSeries": false,
      "id": 46,
      "legend": {
        "alignAsTable": true,
        "avg": true,
        "current": true,
        "max": true,
        "min": true,
        "rightSide": false,
        "show": true,
        "total": false,
        "values": true
      },
      "lines": true,
      "linewidth": 1,
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 2,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "sum by()(rate(com_iquantex_Phoenix_TransactionReliability_NewTransTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "新增事务TPS",
          "refId": "A"
        },
        {
          "expr": "sum by()(rate(com_iquantex_Phoenix_TransactionReliability_FinishTransTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "结束事务TPS",
          "refId": "C"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_TransactionReliability_LiveTransTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "在途事务数量",
          "refId": "B"
        },
        {
          "expr": "sum by()(rate(com_iquantex_Phoenix_TransactionReliability_RetryTransTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "重试事务TPS",
          "refId": "G"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "事务处理",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "short",
          "label": null,
          "logBase": 2,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 11,
        "w": 24,
        "x": 0,
        "y": 32
      },
      "hiddenSeries": false,
      "id": 57,
      "legend": {
        "alignAsTable": true,
        "avg": true,
        "current": false,
        "max": true,
        "min": true,
        "show": true,
        "total": false,
        "values": true
      },
      "lines": true,
      "linewidth": 1,
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 2,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "sum by ()(rate(com_iquantex_Phoenix_EntityAggregateManager_HandleTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\",_aggregateRootType=\"TransactionReliability\"}[30s]))",
          "interval": "",
          "legendFormat": "Handle TPS",
          "refId": "D"
        },
        {
          "expr": "sum by ()(rate(com_iquantex_Phoenix_EntityAggregateManager_HandleMsgTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\",_aggregateRootType=\"TransactionReliability\"}[30s]))",
          "interval": "",
          "legendFormat": "Handle Msg  TPS",
          "refId": "E"
        },
        {
          "expr": "sum by ()(rate(com_iquantex_Phoenix_EntityAggregateManager_AppendTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\",_aggregateRootType=\"TransactionReliability\"}[30s]))",
          "interval": "",
          "legendFormat": "Append TPS",
          "refId": "F"
        },
        {
          "expr": "sum by ()(rate(com_iquantex_Phoenix_EntityAggregateManager_AppendEventTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\",_aggregateRootType=\"TransactionReliability\"}[30s]))",
          "interval": "",
          "legendFormat": "Append Event TPS",
          "refId": "B"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "可靠性处理TPS",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 13,
        "w": 24,
        "x": 0,
        "y": 43
      },
      "hiddenSeries": false,
      "id": 105,
      "legend": {
        "alignAsTable": true,
        "avg": true,
        "current": false,
        "max": true,
        "min": true,
        "show": true,
        "total": false,
        "values": true
      },
      "lines": true,
      "linewidth": 1,
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 2,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "sum by ()(increase(com_iquantex_Phoenix_EntityAggregateManager_HandleLatencyTotalUs{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\",_aggregateRootType=\"TransactionReliability\"}[1m]))/sum by ()(increase(com_iquantex_Phoenix_EntityAggregateManager_HandleTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\",_aggregateRootType=\"TransactionReliability\"}[1m]))/1000",
          "interval": "",
          "legendFormat": "Handle Latency",
          "refId": "A"
        },
        {
          "expr": "sum by ()(increase(com_iquantex_Phoenix_EntityAggregateManager_HandleLatencyTotalUs{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\",_aggregateRootType=\"TransactionReliability\"}[1m]))/sum by ()(increase(com_iquantex_Phoenix_EntityAggregateManager_HandleMsgTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\",_aggregateRootType=\"TransactionReliability\"}[1m]))/1000",
          "interval": "",
          "legendFormat": "Handle MSG  Latency",
          "refId": "F"
        },
        {
          "expr": "sum by ()(increase(com_iquantex_Phoenix_EntityAggregateManager_AppendLatencyTotalUs{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\",_aggregateRootType=\"TransactionReliability\"}[1m]))/sum by ()(increase(com_iquantex_Phoenix_EntityAggregateManager_AppendEventTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\",_aggregateRootType=\"TransactionReliability\"}[1m]))/1000",
          "interval": "",
          "legendFormat": "Append Event Latency",
          "refId": "C"
        },
        {
          "expr": "sum by ()(increase(com_iquantex_Phoenix_EntityAggregateManager_HandleWithoutIOLatencyTotalUs{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\",_aggregateRootType=\"TransactionReliability\"}[1m]))/sum by ()(increase(com_iquantex_Phoenix_EntityAggregateManager_HandleMsgTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\",_aggregateRootType=\"TransactionReliability\"}[1m]))/1000",
          "interval": "",
          "legendFormat": "Handle MSG  NIO Latency",
          "refId": "B"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "可靠性处理延时",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {}
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 8,
        "w": 24,
        "x": 0,
        "y": 56
      },
      "hiddenSeries": false,
      "id": 117,
      "legend": {
        "avg": false,
        "current": false,
        "max": false,
        "min": false,
        "show": true,
        "total": false,
        "values": false
      },
      "lines": true,
      "linewidth": 1,
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 2,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "sum by()(com_iquantex_Phoenix_EntityAggregate_ChildPendingTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "child未回复的消息总数",
          "refId": "A"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "关键排队指标",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "description": "",
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 15,
        "w": 24,
        "x": 0,
        "y": 64
      },
      "hiddenSeries": false,
      "id": 104,
      "legend": {
        "alignAsTable": true,
        "avg": true,
        "current": false,
        "max": true,
        "min": true,
        "show": true,
        "total": false,
        "values": true
      },
      "lines": true,
      "linewidth": 1,
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 2,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "sum by ()(rate(com_iquantex_Phoenix_EntityAggregateManager_HandleTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType!=\"TransactionReliability\"}[30s]))",
          "interval": "",
          "legendFormat": "Handle TPS",
          "refId": "D"
        },
        {
          "expr": "sum by ()(rate(com_iquantex_Phoenix_EntityAggregateManager_AppendTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType!=\"TransactionReliability\"}[30s]))",
          "interval": "",
          "legendFormat": "Append TPS",
          "refId": "F"
        },
        {
          "expr": "sum by ()(rate(com_iquantex_Phoenix_EntityAggregateManager_HandleMsgTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType!=\"TransactionReliability\"}[30s]))",
          "interval": "",
          "legendFormat": "Handle Msg  TPS",
          "refId": "E"
        },
        {
          "expr": "sum by ()(rate(com_iquantex_Phoenix_EntityAggregateManager_AppendEventTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType!=\"TransactionReliability\"}[30s]))",
          "interval": "",
          "legendFormat": "Append Event TPS",
          "refId": "B"
        },
        {
          "expr": "sum by()(rate(com_iquantex_Phoenix_EntityAggregateManager_IdempotentByDBTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType!=\"TransactionReliability\"}[30s]))",
          "interval": "",
          "legendFormat": "数据库幂等TPS",
          "refId": "A"
        },
        {
          "expr": "sum by()(rate(com_iquantex_Phoenix_EntityAggregateManager_IdempotentByCacheTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType!=\"TransactionReliability\"}[30s]))",
          "interval": "",
          "legendFormat": "内存幂等TPS",
          "refId": "G"
        },
        {
          "expr": "sum by () (rate(com_iquantex_Phoenix_EntityAggregateManager_BatchAppendFailTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType!=\"TransactionReliability\"}[30s]))",
          "interval": "",
          "legendFormat": "批量失败",
          "refId": "C"
        },
        {
          "expr": "sum by()(com_iquantex_Phoenix_EntityAggregateManager_AliveAggregateTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType!=\"TransactionReliability\"})",
          "interval": "",
          "legendFormat": "内存中实体聚合根数量",
          "refId": "H"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "实体聚合根处理TPS",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 13,
        "w": 24,
        "x": 0,
        "y": 79
      },
      "hiddenSeries": false,
      "id": 70,
      "legend": {
        "alignAsTable": true,
        "avg": true,
        "current": false,
        "max": true,
        "min": true,
        "show": true,
        "total": false,
        "values": true
      },
      "lines": true,
      "linewidth": 1,
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 2,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "sum by ()(increase(com_iquantex_Phoenix_EntityAggregateManager_HandleLatencyTotalUs{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType!=\"TransactionReliability\"}[1m]))/sum by ()(increase(com_iquantex_Phoenix_EntityAggregateManager_HandleTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType!=\"TransactionReliability\"}[1m]))/1000",
          "interval": "",
          "legendFormat": "Handle Latency",
          "refId": "A"
        },
        {
          "expr": "sum by ()(increase(com_iquantex_Phoenix_EntityAggregateManager_HandleLatencyTotalUs{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType!=\"TransactionReliability\"}[1m]))/sum by ()(increase(com_iquantex_Phoenix_EntityAggregateManager_HandleMsgTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType!=\"TransactionReliability\"}[1m]))/1000",
          "interval": "",
          "legendFormat": "Handle MSG  Latency",
          "refId": "F"
        },
        {
          "expr": "sum by ()(increase(com_iquantex_Phoenix_EntityAggregateManager_AppendLatencyTotalUs{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType!=\"TransactionReliability\"}[1m]))/sum by ()(increase(com_iquantex_Phoenix_EntityAggregateManager_AppendEventTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType!=\"TransactionReliability\"}[1m]))/1000",
          "interval": "",
          "legendFormat": "Append Event Latency",
          "refId": "C"
        },
        {
          "expr": "sum by ()(increase(com_iquantex_Phoenix_EntityAggregateManager_HandleWithoutIOLatencyTotalUs{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType!=\"TransactionReliability\"}[1m]))/sum by ()(increase(com_iquantex_Phoenix_EntityAggregateManager_HandleMsgTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\", _aggregateRootType!=\"TransactionReliability\"}[1m]))/1000",
          "interval": "",
          "legendFormat": "Handle MSG  NIO Latency",
          "refId": "B"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "实体聚合根处理延时",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green",
                "value": null
              },
              {
                "color": "red",
                "value": 80
              }
            ]
          }
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 9,
        "w": 24,
        "x": 0,
        "y": 92
      },
      "hiddenSeries": false,
      "id": 119,
      "legend": {
        "avg": false,
        "current": false,
        "max": false,
        "min": false,
        "show": true,
        "total": false,
        "values": false
      },
      "lines": true,
      "linewidth": 1,
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 2,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "sum by()(com_iquantex_Phoenix_TransactionAggregateActor_CurrentActorTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "interval": "",
          "legendFormat": "当前存活事务",
          "refId": "A"
        },
        {
          "expr": "sum by()(rate(com_iquantex_Phoenix_TransactionAggregateActor_HeartbeatTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "心跳",
          "refId": "B"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "事务实时指标统计",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 13,
        "w": 24,
        "x": 0,
        "y": 101
      },
      "hiddenSeries": false,
      "id": 63,
      "legend": {
        "alignAsTable": true,
        "avg": true,
        "current": false,
        "max": true,
        "min": true,
        "show": true,
        "total": false,
        "values": true
      },
      "lines": true,
      "linewidth": 1,
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 2,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "sum by() (rate(com_iquantex_Phoenix_TransactionAggregateManager_HandleTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "Handle TPS",
          "refId": "A"
        },
        {
          "expr": "sum by() (rate(com_iquantex_Phoenix_TransactionAggregateManager_AppendTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "Append TPS",
          "refId": "D"
        },
        {
          "expr": "sum by()(rate(com_iquantex_Phoenix_TransactionAggregateManager_IdempotentTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "幂等处理",
          "refId": "B"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "TransactionAggregateManager TPS",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 8,
        "w": 24,
        "x": 0,
        "y": 114
      },
      "hiddenSeries": false,
      "id": 59,
      "legend": {
        "avg": false,
        "current": false,
        "max": false,
        "min": false,
        "show": true,
        "total": false,
        "values": false
      },
      "lines": true,
      "linewidth": 1,
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 2,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "sum by(_label)(rate(com_iquantex_Phoenix_EventStore_AppendTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "Append TPS-{{_label}}",
          "refId": "B"
        },
        {
          "expr": "sum by(_label)(rate(com_iquantex_Phoenix_EventStore_AppendEventTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "Append Event TPS-{{_label}}",
          "refId": "A"
        },
        {
          "expr": "sum by(_label)(com_iquantex_Phoenix_EventStore_QueueSize{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"})",
          "hide": false,
          "interval": "",
          "legendFormat": "队列大小-{{_label}}",
          "refId": "D"
        },
        {
          "expr": "sum by(_label)(rate(com_iquantex_Phoenix_EventStore_ReadTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "读TPS-{{_label}}",
          "refId": "E"
        },
        {
          "expr": "sum by(_label)(rate(com_iquantex_Phoenix_EventStore_ExecutorAppendTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))",
          "interval": "",
          "legendFormat": "Executor-Append TPS-{{_label}}",
          "refId": "C"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "EventStore TPS",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "decimals": -2,
          "format": "short",
          "label": "",
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "custom": {},
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 8,
        "w": 24,
        "x": 0,
        "y": 122
      },
      "hiddenSeries": false,
      "id": 71,
      "legend": {
        "avg": false,
        "current": false,
        "max": false,
        "min": false,
        "show": true,
        "total": false,
        "values": false
      },
      "lines": true,
      "linewidth": 1,
      "nullPointMode": "null",
      "percentage": false,
      "pluginVersion": "7.1.1",
      "pointradius": 2,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "sum by(_label)(increase(com_iquantex_Phoenix_EventStore_AppendLatencyTotalUs{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))/sum by(_label)(increase(com_iquantex_Phoenix_EventStore_AppendTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))/1000",
          "format": "time_series",
          "instant": false,
          "interval": "",
          "legendFormat": "Append Latency-{{_label}}",
          "refId": "F"
        },
        {
          "expr": "sum by(_label)(increase(com_iquantex_Phoenix_EventStore_AppendLatencyTotalUs{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))/sum by(_label)(increase(com_iquantex_Phoenix_EventStore_AppendEventTotal{kubernetes_namespace=~\"[[namespace]]\",service_name=~\"[[appname]]\",instance=~\"[[instance]]\"}[30s]))/1000",
          "format": "time_series",
          "instant": false,
          "interval": "",
          "legendFormat": "Append Event Latency-{{_label}}",
          "refId": "C"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "EventStore Latency",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "decimals": -2,
          "format": "short",
          "label": "",
          "logBase": 2,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    }
  ],
  "refresh": "10s",
  "schemaVersion": 26,
  "style": "dark",
  "tags": [
    "Phoenix"
  ],
  "templating": {
    "list": [
      {
        "allValue": null,
        "current": {
          "selected": false,
          "text": "All",
          "value": "$__all"
        },
        "datasource": "Prometheus",
        "definition": "label_values(com_iquantex_Phoenix_TransactionReliability_NewTransTotal{},kubernetes_namespace)",
        "hide": 0,
        "includeAll": true,
        "label": "namespace",
        "multi": false,
        "name": "namespace",
        "options": [],
        "query": "label_values(com_iquantex_Phoenix_TransactionReliability_NewTransTotal{},kubernetes_namespace)",
        "refresh": 2,
        "regex": "",
        "skipUrlSync": false,
        "sort": 1,
        "tagValuesQuery": "",
        "tags": [],
        "tagsQuery": "",
        "type": "query",
        "useTags": false
      },
      {
        "allValue": null,
        "current": {
          "selected": false,
          "text": "All",
          "value": "$__all"
        },
        "datasource": "Prometheus",
        "definition": "label_values(com_iquantex_Phoenix_TransactionReliability_NewTransTotal{kubernetes_namespace=~\"$namespace\"},service_name)",
        "hide": 0,
        "includeAll": true,
        "label": "appname",
        "multi": false,
        "name": "appname",
        "options": [],
        "query": "label_values(com_iquantex_Phoenix_TransactionReliability_NewTransTotal{kubernetes_namespace=~\"$namespace\"},service_name)",
        "refresh": 2,
        "regex": "",
        "skipUrlSync": false,
        "sort": 0,
        "tagValuesQuery": "",
        "tags": [],
        "tagsQuery": "",
        "type": "query",
        "useTags": false
      },
      {
        "allValue": null,
        "current": {
          "selected": false,
          "text": "All",
          "value": "$__all"
        },
        "datasource": "Prometheus",
        "definition": "label_values(jvm_info{kubernetes_namespace=~\"$namespace\",service_name=~\"$appname\"},instance)",
        "hide": 0,
        "includeAll": true,
        "label": "instance",
        "multi": false,
        "name": "instance",
        "options": [],
        "query": "label_values(jvm_info{kubernetes_namespace=~\"$namespace\",service_name=~\"$appname\"},instance)",
        "refresh": 2,
        "regex": "",
        "skipUrlSync": false,
        "sort": 0,
        "tagValuesQuery": "",
        "tags": [],
        "tagsQuery": "",
        "type": "query",
        "useTags": false
      }
    ]
  },
  "time": {
    "from": "now-5m",
    "to": "now"
  },
  "timepicker": {
    "refresh_intervals": [
      "10s",
      "30s",
      "1m",
      "5m"
    ],
    "time_options": [
      "5m",
      "15m",
      "1h",
      "6h",
      "12h",
      "24h",
      "2d",
      "7d",
      "30d"
    ]
  },
  "timezone": "",
  "title": "01 phoenix source aggregate",
  "uid": "EefwU7NGz12ss",
  "version": 1
}
```

