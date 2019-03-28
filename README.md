# Introduction

Simple helper to update prometheus node-exporter using borg data. To be called after a backup is performed. This script creates a prom file that is parsed by node-exporter. Make sure to put the prom file in a location which node-exporter monitors.

This tool is an adaptation of https://github.com/teemow/prometheus-borg-exporter for my use cases.

Main repository: https://framagit.org/tigre-bleu/prometheus-borg-exporter

# Usage

The following parameter is required:
- `-r` or `--repository`: Repository to update from

The following options are availble:
- `-f` or `--force-host`: Override manually the host for this repository. Default to the local machine hostname
- `-o` or `--output`: Set output prom filename. Default to borg.prom

Make sure to call the script after a backup is performed (via cron, systemd, borgmatic or whatever way you see fit)