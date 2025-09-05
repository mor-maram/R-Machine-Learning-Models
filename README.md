# R-Machine-Learning-Models
# ==========================================
# Author: Maram Mohammed
# Year: 2024
# ==========================================

# ---- Install and load packages ----
packages <- c("rsample", "caret", "tidyverse", "AmesHousing", "class", "rpart", "ggplot2")

installed_packages <- packages %in% rownames(installed.packages())
if (any(installed_packages == FALSE)) {
  install.packages(packages[!installed_packages])
}

invisible(lapply(packages, library, character.only = TRUE))

# ==========================================
# Regression Example: AmesHousing
# ==========================================
ames <- AmesHousing::make_ames()

# Split data (stratified)
set.seed(123)
split_ames <- initial_split(ames, prop = 0.7, strata = "Sale_Price")
ames_train <- training_
