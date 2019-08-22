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
  "id": 58,
  "iteration": 1559359574913,
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
        "h": 6,
        "w": 12,
        "x": 0,
        "y": 0
      },
      "id": 6,
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
          "expr": "rate(mongodb_mongod_op_counters_total{node_name=~\"$host\", type=\"query\"}[$interval]) or\nirate(mongodb_mongod_op_counters_total{node_name=~\"$host\", type=\"query\"}[5m])",
          "format": "time_series",
          "hide": false,
          "interval": "$interval",
          "intervalFactor": 1,
          "legendFormat": "Queries Today - {{node_name}}",
          "refId": "A"
        },
        {
          "expr": "rate(mongodb_mongod_op_counters_total{node_name=~\"$host\", type=\"query\"}[$interval] offset 1d) or \nirate(mongodb_mongod_op_counters_total{node_name=~\"$host\", type=\"query\"}[5m] offset 1d)",
          "format": "time_series",
          "hide": false,
          "interval": "$interval",
          "intervalFactor": 1,
          "legendFormat": "Queries 1d ago - {{node_name}}",
          "refId": "B"
        },
        {
          "expr": "rate(mongodb_mongod_op_counters_total{node_name=~\"$host\", type=\"query\"}[$interval] offset 1w) or \nirate(mongodb_mongod_op_counters_total{node_name=~\"$host\", type=\"query\"}[5m] offset 1w)",
          "format": "time_series",
          "hide": false,
          "interval": "$interval",
          "intervalFactor": 1,
          "legendFormat": "Queries 1w ago - {{serice_name}}",
          "refId": "C"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "Query Trends",
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
      "fill": 1,
      "gridPos": {
        "h": 6,
        "w": 12,
        "x": 12,
        "y": 0
      },
      "id": 4,
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
          "expr": "rate(mongodb_mongod_op_counters_total{node_name=~\"$host\", type=\"insert\"}[$interval]) or\nirate(mongodb_mongod_op_counters_total{node_name=~\"$host\", type=\"insert\"}[5m])",
          "format": "time_series",
          "interval": "$interval",
          "intervalFactor": 1,
          "legendFormat": "Inserts Today - {{node_name}}",
          "refId": "A"
        },
        {
          "expr": "rate(mongodb_mongod_op_counters_total{node_name=~\"$host\", type=\"insert\"}[$interval] offset 1d) or \nirate(mongodb_mongod_op_counters_total{node_name=~\"$host\", type=\"insert\"}[5m] offset 1d)",
          "format": "time_series",
          "interval": "$interval",
          "intervalFactor": 1,
          "legendFormat": "Inserts 1d ago - {{node_name}}",
          "refId": "B"
        },
        {
          "expr": "rate(mongodb_mongod_op_counters_total{node_name=~\"$host\", type=\"insert\"}[$interval] offset 1w) or \nirate(mongodb_mongod_op_counters_total{node_name=~\"$host\", type=\"insert\"}[5m] offset 1w)",
          "format": "time_series",
          "interval": "$interval",
          "intervalFactor": 1,
          "legendFormat": "Inserts 1w ago - {{node_name}}",
          "refId": "C"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "Insert Trends",
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
      "fill": 1,
      "gridPos": {
        "h": 6,
        "w": 12,
        "x": 0,
        "y": 6
      },
      "id": 8,
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
          "expr": "rate(mongodb_mongod_op_counters_total{node_name=~\"$host\", type=\"update\"}[$interval]) or\nirate(mongodb_mongod_op_counters_total{node_name=~\"$host\", type=\"update\"}[5m])",
          "format": "time_series",
          "interval": "$interval",
          "intervalFactor": 1,
          "legendFormat": "Updates Today - {{node_name}}",
          "refId": "A"
        },
        {
          "expr": "rate(mongodb_mongod_op_counters_total{node_name=~\"$host\", type=\"update\"}[$interval] offset 1d) or \nirate(mongodb_mongod_op_counters_total{node_name=~\"$host\", type=\"update\"}[5m] offset 1d)",
          "format": "time_series",
          "interval": "$interval",
          "intervalFactor": 1,
          "legendFormat": "Updates 1d ago - {{node_name}}",
          "refId": "B"
        },
        {
          "expr": "rate(mongodb_mongod_op_counters_total{node_name=~\"$host\", type=\"update\"}[$interval] offset 1w) or \nirate(mongodb_mongod_op_counters_total{node_name=~\"$host\", type=\"update\"}[5m] offset 1w)",
          "format": "time_series",
          "interval": "$interval",
          "intervalFactor": 1,
          "legendFormat": "Updates 1w ago - {{node_name}}",
          "refId": "C"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "Update Trends",
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
      "fill": 1,
      "gridPos": {
        "h": 6,
        "w": 12,
        "x": 12,
        "y": 6
      },
      "id": 2,
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
          "expr": "rate(mongodb_mongod_op_counters_total{node_name=~\"$host\", type=\"delete\"}[$interval]) or\nirate(mongodb_mongod_op_counters_total{node_name=~\"$host\", type=\"delete\"}[5m])",
          "format": "time_series",
          "interval": "$interval",
          "intervalFactor": 1,
          "legendFormat": "Deletes Today - {{node_name}}",
          "refId": "A"
        },
        {
          "expr": "rate(mongodb_mongod_op_counters_total{node_name=~\"$host\", type=\"delete\"}[$interval] offset 1d) or \nirate(mongodb_mongod_op_counters_total{node_name=~\"$host\", type=\"delete\"}[5m] offset 1d)",
          "format": "time_series",
          "interval": "$interval",
          "intervalFactor": 1,
          "legendFormat": "Deletes 1d ago - {{node_name}}",
          "refId": "B"
        },
        {
          "expr": "rate(mongodb_mongod_op_counters_total{node_name=~\"$host\", type=\"delete\"}[$interval] offset 1w) or \nirate(mongodb_mongod_op_counters_total{node_name=~\"$host\", type=\"delete\"}[5m] offset 1w)",
          "format": "time_series",
          "interval": "$interval",
          "intervalFactor": 1,
          "legendFormat": "Deletes 1w ago - {{node_name}}",
          "refId": "C"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "Delete Trends",
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
      "fill": 1,
      "gridPos": {
        "h": 6,
        "w": 12,
        "x": 0,
        "y": 12
      },
      "id": 10,
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
          "expr": "rate(mongodb_mongod_metrics_document_total{node_name=~\"$host\", state=\"returned\"}[$interval]) or\nirate(mongodb_mongod_metrics_document_total{node_name=~\"$host\", state=\"returned\"}[5m])",
          "format": "time_series",
          "interval": "$interval",
          "intervalFactor": 1,
          "legendFormat": "Returned today - {{node_name}}",
          "refId": "A"
        },
        {
          "expr": "rate(mongodb_mongod_metrics_document_total{node_name=~\"$host\", state=\"returned\"}[$interval] offset 1d) or \nirate(mongodb_mongod_metrics_document_total{node_name=~\"$host\", state=\"returned\"}[5m] offset 1d)",
          "format": "time_series",
          "interval": "$interval",
          "intervalFactor": 1,
          "legendFormat": "Returned 1d ago - {{node_name}}",
          "refId": "B"
        },
        {
          "expr": "rate(mongodb_mongod_metrics_document_total{node_name=~\"$host\", state=\"returned\"}[$interval] offset 1w) or \nirate(mongodb_mongod_metrics_document_total{node_name=~\"$host\", state=\"returned\"}[5m] offset 1w)",
          "format": "time_series",
          "interval": "$interval",
          "intervalFactor": 1,
          "legendFormat": "Returned 1w ago - {{node_name}}",
          "refId": "C"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "Documents Returned Trend",
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
  "refresh": "5s",
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
        "allFormat": "glob",
        "allValue": null,
        "current": {
          "text": "All",
          "value": "$__all"
        },
        "datasource": "Prometheus",
        "definition": "label_values(mongodb_up, node_name)",
        "hide": 0,
        "includeAll": true,
        "label": "Host",
        "multi": false,
        "multiFormat": "glob",
        "name": "host",
        "options": [],
        "query": "label_values(mongodb_up, node_name)",
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
    "from": "now-3h",
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
  "title": "MongoDB Trends",
  "uid": "HYGfw0WWz",
  "version": 9
}
