{
  "annotations": {
    "list": [
      {
        "builtIn": 1,
        "datasource": "-- Grafana --",
        "enable": true,
        "hide": false,
        "iconColor": "#e0752d",
        "limit": 100,
        "name": "PMM Annotations",
        "showIn": 0,
        "tags": [
          "pmm_annotation"
        ],
        "type": "tags"
      },
      {
        "builtIn": 1,
        "datasource": "-- Grafana --",
        "enable": true,
        "hide": true,
        "iconColor": "#6ed0e0",
        "limit": 100,
        "name": "Annotations & Alerts",
        "showIn": 0,
        "tags": [],
        "type": "dashboard"
      }
    ]
  },
  "editable": true,
  "gnetId": null,
  "graphTooltip": 1,
  "id": 60,
  "iteration": 1559359634729,
  "links": [
    {
      "icon": "dashboard",
      "includeVars": true,
      "keepTime": true,
      "tags": [
        "QAN"
      ],
      "targetBlank": false,
      "title": "Query Analytics",
      "type": "link",
      "url": "/graph/dashboard/db/_pmm-query-analytics"
    },
    {
      "asDropdown": true,
      "includeVars": true,
      "keepTime": true,
      "tags": [
        "OS"
      ],
      "targetBlank": false,
      "title": "OS",
      "type": "dashboards"
    },
    {
      "asDropdown": true,
      "includeVars": true,
      "keepTime": true,
      "tags": [
        "MySQL"
      ],
      "targetBlank": false,
      "title": "MySQL",
      "type": "dashboards"
    },
    {
      "asDropdown": true,
      "includeVars": true,
      "keepTime": true,
      "tags": [
        "MongoDB"
      ],
      "targetBlank": false,
      "title": "MongoDB",
      "type": "dashboards"
    },
    {
      "asDropdown": true,
      "includeVars": true,
      "keepTime": true,
      "tags": [
        "PostgreSQL"
      ],
      "targetBlank": false,
      "title": "PostgreSQL",
      "type": "dashboards"
    },
    {
      "asDropdown": true,
      "includeVars": true,
      "keepTime": true,
      "tags": [
        "HA"
      ],
      "targetBlank": false,
      "title": "HA",
      "type": "dashboards"
    },
    {
      "asDropdown": true,
      "includeVars": true,
      "keepTime": true,
      "tags": [
        "Cloud"
      ],
      "targetBlank": false,
      "title": "Cloud",
      "type": "dashboards"
    },
    {
      "asDropdown": true,
      "includeVars": true,
      "keepTime": true,
      "tags": [
        "Insight"
      ],
      "targetBlank": false,
      "title": "Insight",
      "type": "dashboards"
    },
    {
      "asDropdown": true,
      "includeVars": true,
      "keepTime": true,
      "tags": [
        "PMM"
      ],
      "targetBlank": false,
      "title": "PMM",
      "type": "dashboards"
    }
  ],
  "panels": [
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "fill": 1,
      "gridPos": {
        "h": 8,
        "w": 12,
        "x": 0,
        "y": 0
      },
      "id": 12,
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
      "pointradius": 2,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "rate(mongodb_mongod_top_time_seconds_total{type=~\"Insert\"}[$interval]) ",
          "format": "time_series",
          "intervalFactor": 1,
          "legendFormat": "",
          "refId": "A"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "Panel Title",
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
      "columns": [
        {
          "text": "Current",
          "value": "current"
        }
      ],
      "datasource": "Prometheus",
      "editable": true,
      "error": false,
      "fontSize": "100%",
      "gridPos": {
        "h": 7,
        "w": 12,
        "x": 12,
        "y": 0
      },
      "height": "",
      "hideTimeOverride": true,
      "id": 4,
      "links": [],
      "pageSize": null,
      "scroll": false,
      "showHeader": true,
      "sort": {
        "col": 3,
        "desc": true
      },
      "styles": [
        {
          "alias": "",
          "colorMode": null,
          "colors": [
            "rgba(245, 54, 54, 0.9)",
            "rgba(237, 129, 40, 0.89)",
            "rgba(50, 172, 45, 0.97)"
          ],
          "dateFormat": "YYYY-MM-DD HH:mm:ss",
          "decimals": 2,
          "mappingType": 1,
          "pattern": "Time",
          "thresholds": [],
          "type": "hidden",
          "unit": "short"
        },
        {
          "alias": "Database",
          "colorMode": null,
          "colors": [
            "rgba(245, 54, 54, 0.9)",
            "rgba(237, 129, 40, 0.89)",
            "rgba(50, 172, 45, 0.97)"
          ],
          "dateFormat": "YYYY-MM-DD HH:mm:ss",
          "decimals": 2,
          "mappingType": 1,
          "pattern": "db",
          "thresholds": [],
          "type": "string",
          "unit": "short"
        },
        {
          "alias": "Collection",
          "colorMode": null,
          "colors": [
            "rgba(245, 54, 54, 0.9)",
            "rgba(237, 129, 40, 0.89)",
            "rgba(50, 172, 45, 0.97)"
          ],
          "dateFormat": "YYYY-MM-DD HH:mm:ss",
          "decimals": 2,
          "mappingType": 1,
          "pattern": "coll",
          "thresholds": [],
          "type": "string",
          "unit": "short"
        },
        {
          "colorMode": null,
          "colors": [
            "rgba(245, 54, 54, 0.9)",
            "rgba(237, 129, 40, 0.89)",
            "rgba(50, 172, 45, 0.97)"
          ],
          "dateFormat": "YYYY-MM-DD HH:mm:ss",
          "decimals": null,
          "pattern": "/.*/",
          "thresholds": [],
          "type": "number",
          "unit": "decbytes"
        }
      ],
      "targets": [
        {
          "expr": "topk(10, sum(mongodb_mongod_db_coll_size{service_name=~\"$service\", db!~\"config|local|admin\", coll!~\"system.*\"}) by (db, coll)) > 0",
          "format": "table",
          "instant": true,
          "interval": "5m",
          "intervalFactor": 1,
          "legendFormat": "",
          "refId": "A",
          "step": 300
        }
      ],
      "timeFrom": "5m",
      "title": "Largest Collections by Size",
      "transform": "table",
      "type": "table"
    },
    {
      "columns": [
        {
          "filterable": true,
          "hidden": false,
          "style": {
            "alias": "Column",
            "colorMode": null,
            "colors": [
              "rgba(245, 54, 54, 0.9)",
              "rgba(237, 129, 40, 0.89)",
              "rgba(50, 172, 45, 0.97)"
            ],
            "dateFormat": "YYYY-MM-DD HH:mm:ss",
            "decimals": 2,
            "mappingType": 1,
            "pattern": "coll",
            "thresholds": [],
            "type": "string",
            "unit": "short"
          },
          "text": "coll",
          "title": "Column"
        },
        {
          "filterable": true,
          "hidden": false,
          "style": {
            "colorMode": null,
            "colors": [
              "rgba(245, 54, 54, 0.9)",
              "rgba(237, 129, 40, 0.89)",
              "rgba(50, 172, 45, 0.97)"
            ],
            "dateFormat": "YYYY-MM-DD HH:mm:ss",
            "decimals": null,
            "pattern": "/.*/",
            "thresholds": [],
            "type": "number",
            "unit": "short"
          },
          "text": "db",
          "title": "db"
        },
        {
          "desc": true,
          "hidden": false,
          "sort": true,
          "style": {
            "colorMode": null,
            "colors": [
              "rgba(245, 54, 54, 0.9)",
              "rgba(237, 129, 40, 0.89)",
              "rgba(50, 172, 45, 0.97)"
            ],
            "dateFormat": "YYYY-MM-DD HH:mm:ss",
            "decimals": null,
            "pattern": "/.*/",
            "thresholds": [],
            "type": "number",
            "unit": "short"
          },
          "text": "Value",
          "title": "Value"
        }
      ],
      "datasource": "Prometheus",
      "editable": true,
      "error": false,
      "fontSize": "100%",
      "gridPos": {
        "h": 7,
        "w": 12,
        "x": 0,
        "y": 8
      },
      "height": "",
      "hideTimeOverride": true,
      "id": 2,
      "interval": "",
      "links": [],
      "pageSize": null,
      "scroll": true,
      "showHeader": true,
      "sort": {
        "col": 3,
        "desc": true
      },
      "styles": [
        {
          "alias": "",
          "colorMode": null,
          "colors": [
            "rgba(245, 54, 54, 0.9)",
            "rgba(237, 129, 40, 0.89)",
            "rgba(50, 172, 45, 0.97)"
          ],
          "dateFormat": "YYYY-MM-DD HH:mm:ss",
          "decimals": 2,
          "mappingType": 1,
          "pattern": "Time",
          "thresholds": [],
          "type": "hidden",
          "unit": "short"
        },
        {
          "alias": "Database",
          "colorMode": null,
          "colors": [
            "rgba(245, 54, 54, 0.9)",
            "rgba(237, 129, 40, 0.89)",
            "rgba(50, 172, 45, 0.97)"
          ],
          "dateFormat": "YYYY-MM-DD HH:mm:ss",
          "decimals": 2,
          "mappingType": 1,
          "pattern": "db",
          "thresholds": [],
          "type": "string",
          "unit": "short"
        },
        {
          "alias": "Collection",
          "colorMode": null,
          "colors": [
            "rgba(245, 54, 54, 0.9)",
            "rgba(237, 129, 40, 0.89)",
            "rgba(50, 172, 45, 0.97)"
          ],
          "dateFormat": "YYYY-MM-DD HH:mm:ss",
          "decimals": 2,
          "mappingType": 1,
          "pattern": "coll",
          "thresholds": [],
          "type": "string",
          "unit": "short"
        },
        {
          "colorMode": null,
          "colors": [
            "rgba(245, 54, 54, 0.9)",
            "rgba(237, 129, 40, 0.89)",
            "rgba(50, 172, 45, 0.97)"
          ],
          "dateFormat": "YYYY-MM-DD HH:mm:ss",
          "decimals": null,
          "pattern": "/.*/",
          "thresholds": [],
          "type": "number",
          "unit": "short"
        }
      ],
      "targets": [
        {
          "expr": "topk(10, sum(mongodb_mongod_db_coll_count{service_name=\"$service\", db!~\"config|local|admin\", coll!~\"system.*\"}) by (db, coll)) > 0",
          "format": "table",
          "instant": true,
          "interval": "5m",
          "intervalFactor": 1,
          "legendFormat": "{{ db }}.{{ coll }}",
          "refId": "A",
          "step": 300
        }
      ],
      "timeFrom": "5m",
      "timeShift": null,
      "title": "Largest Collections by Document Count",
      "transform": "table",
      "type": "table"
    },
    {
      "aliasColors": {
        "Data + Index Size": "#65C5DB"
      },
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "decimals": 2,
      "editable": true,
      "error": false,
      "fill": 2,
      "grid": {},
      "gridPos": {
        "h": 7,
        "w": 24,
        "x": 0,
        "y": 15
      },
      "id": 6,
      "legend": {
        "alignAsTable": false,
        "avg": false,
        "current": false,
        "hideEmpty": false,
        "max": false,
        "min": false,
        "rightSide": false,
        "show": true,
        "total": false,
        "values": false
      },
      "lines": true,
      "linewidth": 2,
      "links": [],
      "nullPointMode": "null",
      "paceLength": 10,
      "percentage": false,
      "pointradius": 5,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "calculatedInterval": "2m",
          "datasourceErrors": {},
          "errors": {},
          "expr": "sum(mongodb_mongod_db_coll_storage_size{service_name=~\"$service\"})",
          "format": "time_series",
          "interval": "$interval",
          "intervalFactor": 1,
          "legendFormat": "Data + Index Size",
          "metric": "",
          "refId": "A",
          "step": 300
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "Total Database Size",
      "tooltip": {
        "msResolution": false,
        "shared": true,
        "sort": 2,
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
          "logBase": 1,
          "max": null,
          "min": 0,
          "show": true
        },
        {
          "format": "short",
          "logBase": 1,
          "max": null,
          "min": 0,
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
      "fill": 1,
      "gridPos": {
        "h": 7,
        "w": 12,
        "x": 0,
        "y": 22
      },
      "id": 8,
      "legend": {
        "alignAsTable": true,
        "avg": true,
        "current": false,
        "hideEmpty": false,
        "hideZero": false,
        "max": true,
        "min": true,
        "show": true,
        "sort": "avg",
        "sortDesc": true,
        "total": false,
        "values": true
      },
      "lines": true,
      "linewidth": 1,
      "links": [],
      "nullPointMode": "null as zero",
      "percentage": false,
      "pointradius": 2,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "topk(5, rate(mongodb_mongod_top_time_seconds_total{type=\"WriteLock\"}[$interval]))",
          "format": "time_series",
          "instant": false,
          "interval": "$interval",
          "intervalFactor": 1,
          "legendFormat": "{{database}}.{{collection}}",
          "refId": "A"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "Top Collections by WriteLock Wait",
      "tooltip": {
        "shared": true,
        "sort": 2,
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
      "fill": 1,
      "gridPos": {
        "h": 7,
        "w": 12,
        "x": 12,
        "y": 22
      },
      "id": 10,
      "legend": {
        "alignAsTable": true,
        "avg": true,
        "current": false,
        "max": true,
        "min": true,
        "show": true,
        "sort": "avg",
        "sortDesc": true,
        "total": false,
        "values": true
      },
      "lines": true,
      "linewidth": 1,
      "links": [],
      "nullPointMode": "null",
      "percentage": false,
      "pointradius": 2,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "topk(5, rate(mongodb_mongod_top_time_seconds_total{type=\"ReadLock\"}[$interval]))",
          "format": "time_series",
          "interval": "$interval",
          "intervalFactor": 1,
          "legendFormat": "{{database}}.{{collection}}",
          "refId": "A"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "Top Collections by ReadLock Waits",
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
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    }
  ],
  "refresh": "1m",
  "schemaVersion": 18,
  "style": "dark",
  "tags": [],
  "templating": {
    "list": [
      {
        "allFormat": "glob",
        "auto": true,
        "auto_count": 200,
        "auto_min": "1s",
        "current": {
          "text": "auto",
          "value": "$__auto_interval_interval"
        },
        "datasource": "Prometheus",
        "hide": 0,
        "includeAll": false,
        "label": "Interval",
        "multi": false,
        "multiFormat": "glob",
        "name": "interval",
        "options": [
          {
            "selected": true,
            "text": "auto",
            "value": "$__auto_interval_interval"
          },
          {
            "selected": false,
            "text": "1s",
            "value": "1s"
          },
          {
            "selected": false,
            "text": "5s",
            "value": "5s"
          },
          {
            "selected": false,
            "text": "1m",
            "value": "1m"
          },
          {
            "selected": false,
            "text": "5m",
            "value": "5m"
          },
          {
            "selected": false,
            "text": "1h",
            "value": "1h"
          },
          {
            "selected": false,
            "text": "6h",
            "value": "6h"
          },
          {
            "selected": false,
            "text": "1d",
            "value": "1d"
          }
        ],
        "query": "1s,5s,1m,5m,1h,6h,1d",
        "refresh": 2,
        "skipUrlSync": false,
        "type": "interval"
      },
      {
        "allFormat": "blob",
        "allValue": null,
        "current": {
          "text": "All",
          "value": "$__all"
        },
        "datasource": "Prometheus",
        "definition": "",
        "hide": 0,
        "includeAll": true,
        "label": "Cluster",
        "multi": false,
        "multiFormat": "glob",
        "name": "cluster",
        "options": [],
        "query": "label_values(mongodb_up,cluster)",
        "refresh": 1,
        "regex": "",
        "skipUrlSync": false,
        "sort": 1,
        "tagValuesQuery": null,
        "tags": [],
        "tagsQuery": null,
        "type": "query",
        "useTags": false
      },
      {
        "allFormat": "glob",
        "allValue": null,
        "current": {
          "text": "All",
          "value": "$__all"
        },
        "datasource": "Prometheus",
        "definition": "",
        "hide": 0,
        "includeAll": true,
        "label": "Host",
        "multi": false,
        "multiFormat": "glob",
        "name": "host",
        "options": [],
        "query": "label_values(mongodb_up{cluster=~\"$cluster\"}, node_name)",
        "refresh": 1,
        "regex": "",
        "skipUrlSync": false,
        "sort": 1,
        "tagValuesQuery": null,
        "tags": [],
        "tagsQuery": "",
        "type": "query",
        "useTags": false
      },
      {
        "allFormat": "glob",
        "allValue": null,
        "current": {
          "text": "ip-10-178-2-123-mongodb",
          "value": "ip-10-178-2-123-mongodb"
        },
        "datasource": "Prometheus",
        "definition": "",
        "hide": 0,
        "includeAll": false,
        "label": "Service",
        "multi": false,
        "multiFormat": "glob",
        "name": "service",
        "options": [],
        "query": "label_values(mongodb_up{cluster=~\"$cluster\",node_name=~\"$host\"}, service_name)",
        "refresh": 1,
        "regex": "",
        "skipUrlSync": false,
        "sort": 1,
        "tagValuesQuery": null,
        "tags": [],
        "tagsQuery": "",
        "type": "query",
        "useTags": false
      }
    ]
  },
  "time": {
    "from": "now-12h",
    "to": "now"
  },
  "timepicker": {
    "hidden": false,
    "now": true,
    "refresh_intervals": [
      "5s",
      "10s",
      "30s",
      "1m",
      "5m",
      "15m",
      "30m",
      "1h",
      "2h",
      "1d"
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
  "timezone": "browser",
  "title": "MongoDB Collection Statistics (2)",
  "uid": "AE3EraWWz",
  "version": 3
}
