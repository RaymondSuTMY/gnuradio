# Copyright 2012 Free Software Foundation, Inc.
#
# This file is part of GNU Radio
#
# SPDX-License-Identifier: GPL-3.0-or-later
#

########################################################################
include(GrPython)

add_subdirectory(gr)
add_subdirectory(gru)

if(ENABLE_GR_CTRLPORT)
  add_subdirectory(ctrlport)
endif(ENABLE_GR_CTRLPORT)

GR_PYTHON_INSTALL(FILES
    __init__.py
    eng_notation.py
    eng_option.py
    eng_arg.py
    gr_unittest.py
    DESTINATION ${GR_PYTHON_DIR}/gnuradio
)
