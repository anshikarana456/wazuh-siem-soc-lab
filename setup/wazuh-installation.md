# Wazuh SIEM Installation

## Download installer

curl -sO https://packages.wazuh.com/4.7/wazuh-install.sh

## Generate configuration

sudo bash wazuh-install.sh --generate-config-files -i

## Install indexer

sudo bash wazuh-install.sh --wazuh-indexer node-1 -i

## Install manager

sudo bash wazuh-install.sh --wazuh-server wazuh-1 -i

## Install dashboard

sudo bash wazuh-install.sh --wazuh-dashboard dashboard -i
