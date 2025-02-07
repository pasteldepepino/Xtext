#!/bin/bash

clear

line=1

while true; do
  read -rp "~" text[$line]
  if [ "${text[$line]}" == "edit_mode" ]; then
    while true; do
      read -sn1 cmd
      if [ "$cmd" == "e" ]; then
        break
      elif [ "$cmd" == "s" ]; then
        read -p "filename: " filename
        for ((x=1; x<line; x++)); do
          echo "${text[$x]}" >> "$filename"
        done
        break
      fi
    done
  elif [ "${text[$line]}" == "quit_xtext" ]; then
    break
    break
    exit
  
  elif [ "${text[$line]}" == "help_mode" ]; then
    echo "   edit_mode: s -> save file, e -> exit edit mode, quit_xtext -> exit program"
  fi
  line=$((line+1))
done