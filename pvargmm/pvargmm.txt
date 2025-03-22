# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# GMM Estimation of Panel VAR Models Use pvargmm (panelvar) With (In) R Software
# Dynamic Panel VAR estimation, two-step GMM Use pvargmm (panelvar) With (In) R Software
install.packages("panelvar")
library("panelvar")
pvargmm = read.csv("https://raw.githubusercontent.com/timbulwidodostp/pvargmm/main/pvargmm/pvargmm.csv",sep = ";")
# Estimation 
# GMM Estimation of Panel VAR Models Use pvargmm (panelvar) With (In) R Software
# Dynamic Panel VAR estimation, two-step GMM Use pvargmm (panelvar) With (In) R Software
pvargmm <- pvargmm(dependent_vars = c("expenditures", "revenues", "grants"), lags = 1, transformation = "fod", data = pvargmm,
panel_identifier=c("id", "year"), steps = c("twostep"), system_instruments = FALSE, max_instr_dependent_vars = 99, max_instr_predet_vars = 99,
min_instr_dependent_vars = 2L, min_instr_predet_vars = 1L, collapse = FALSE)
summary(pvargmm)

# GMM Estimation of Panel VAR Models Use pvargmm (panelvar) With (In) R Software
# Dynamic Panel VAR estimation, two-step GMM Use pvargmm (panelvar) With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished