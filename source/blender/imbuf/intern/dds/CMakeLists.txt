# $Id: CMakeLists.txt 14444 2008-04-16 22:40:48Z hos $
# ***** BEGIN GPL LICENSE BLOCK *****
#
# This program is free software; you can redistribute it and/or
# modify it under the terms of the GNU General Public License
# as published by the Free Software Foundation; either version 2
# of the License, or (at your option) any later version.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program; if not, write to the Free Software Foundation,
# Inc., 51 Franklin Street, Fifth Floor, Boston, MA 02110-1301, USA.
#
# The Original Code is Copyright (C) 2006, Blender Foundation
# All rights reserved.
#
# The Original Code is: all of this file.
#
# Contributor(s): 
#
# ***** END GPL LICENSE BLOCK *****

set(INC 
	.
	..
	../..
	../../../blenkernel
	../../../blenlib
	../../../makesdna
	../../../../../intern/guardedalloc
)

set(INC_SYS

)

set(SRC
	BlockDXT.cpp
	ColorBlock.cpp
	DirectDrawSurface.cpp
	Image.cpp
	Stream.cpp
	dds_api.cpp
)

if(WITH_IMAGE_DDS)
	add_definitions(-DWITH_DDS)
endif()

blender_add_lib(bf_imbuf_dds "${SRC}" "${INC}" "${INC_SYS}")                 
