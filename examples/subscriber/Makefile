############################################################################
# apps/examples/uros_subscriber/Makefile
#
#   Copyright (C) 2008, 2010-2013 Gregory Nutt. All rights reserved.
#   Author: Gregory Nutt <gnutt@nuttx.org>
#
# Redistribution and use in source and binary forms, with or without
# modification, are permitted provided that the following conditions
# are met:
#
# 1. Redistributions of source code must retain the above copyright
#    notice, this list of conditions and the following disclaimer.
# 2. Redistributions in binary form must reproduce the above copyright
#    notice, this list of conditions and the following disclaimer in
#    the documentation and/or other materials provided with the
#    distribution.
# 3. Neither the name NuttX nor the names of its contributors may be
#    used to endorse or promote products derived from this software
#    without specific prior written permission.
#
# THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
# "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT
# LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS
# FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE
# COPYRIGHT OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT,
# INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING,
# BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS
# OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED
# AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT
# LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN
# ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE
# POSSIBILITY OF SUCH DAMAGE.
#
############################################################################

-include $(TOPDIR)/Make.defs

# uROS-subscriber built-in application info

CONFIG_UROS_EXAMPLES_SUBSCRIBER_PRIORITY ?= SCHED_PRIORITY_DEFAULT
CONFIG_UROS_EXAMPLES_SUBSCRIBER_STACKSIZE ?= 65000

APPNAME = subscriber
PRIORITY = $(CONFIG_UROS_EXAMPLES_SUBSCRIBER_PRIORITY)
STACKSIZE = $(CONFIG_UROS_EXAMPLES_SUBSCRIBER_STACKSIZE)

# uROS-subscriber Example

ASRCS =
CSRCS =
MAINSRC = subscriber_main.c 

CONFIG_UROS_EXAMPLES_SUBSCRIBER_PROGNAME ?= subscriber$(EXEEXT)
PROGNAME = $(CONFIG_UROS_EXAMPLES_SUBSCRIBER_PROGNAME)
UROS_INCLUDES = $(shell find $(APPDIR)/$(CONFIG_UROS_DIR)/install -type d -name include)
CFLAGS += ${shell $(INCDIR) $(INCDIROPT) "$(CC)" "$(UROS_INCLUDES)"} -std=c99

MODULE = CONFIG_UROS_EXAMPLES_SUBSCRIBER

include $(APPDIR)/Application.mk
