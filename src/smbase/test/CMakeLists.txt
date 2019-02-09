#
# smbase tests CMakeLists.txt
#

# tests 
project(nonport)
project(voidlist)
project(vdtllist)
project(taillist_test)
project(tobjlist)
project(tsobjlist)
project(bit2d)
project(growbuf)
project(strdict)
project(svdict)
project(str)
project(strutil)
project(strhash)
project(trdelete)
project(bflatten)
project(mysig)
project(testmalloc)
project(mypopen)
project(tobjpool)
project(cycles)
project(crc)
project(srcloc)
project(hashline)
project(gprintf)
project(smregexp)
project(vptrmap)
project(pprint)
project(boxprint)
project(tarrayqueue)
project(testarray)
project(autofile)
project(bitarray)

# files for nonport
add_executable(nonport
    ../gprintf.c
    ../nonport.cpp
)

# files for voidlist
add_executable(voidlist
    ../voidlist.cc
)

# files for vdtllist
add_executable(vdtllist
    ../vdtllist.cc
)

# files for taillist_test
add_executable(taillist_test
    ../taillist_test.cc
)

# files for tobjlist
add_executable(tobjlist
    ../tobjlist.cc
)

# files for tsobjlist
add_executable(tsobjlist
    ../tsobjlist.cc
)

# files for bit2d
add_executable(bit2d
    ../bit2d.cc
)

# files for growbuf
add_executable(growbuf
    ../growbuf.cc
)

# files for strdict
add_executable(strdict
    ../strdict.cc
)

# files for svdict
add_executable(svdict
    ../svdict.cc
)

# files for str
add_executable(str
    ../str.cpp
)

# files for strutil
add_executable(strutil
    ../strutil.cc
)

# files for strhash
add_executable(strhash
    ../strhash.cc
)

# files for trdelete
add_executable(trdelete
    ../trdelete.cc
)

# files for bflatten
add_executable(bflatten
    ../bflatten.cc
)

# files for mysig
add_executable(mysig
    ../mysig.cc
)

# files for testmalloc
add_executable(testmalloc
    ../testmalloc.cc
)

# files for mypopen
add_executable(mypopen
    ../mypopen.c
)

# files for tobjpool
add_executable(tobjpool
    ../tobjpool.cc
)

# files for cycles
add_executable(cycles
    ../cycles.c
)

# files for crc
add_executable(crc
    ../crc.cpp
)

# files for srcloc
add_executable(srcloc
    ../srcloc.cc
)

# files for hashline
add_executable(hashline
    ../hashline.cc
)

# files for gprintf
add_executable(gprintf
    ../gprintf.c
)

# files for smregexp
add_executable(smregexp
    ../smregexp.cc
)

# files for vptrmap
add_executable(vptrmap
    ../vptrmap.cc
)

# files for pprint
add_executable(pprint
    ../pprint.cc
)

# files for boxprint
add_executable(boxprint
    ../boxprint.cc
)

# files for tarrayqueue
add_executable(tarrayqueue
    ../tarrayqueue.cc
)

# files for testarray
add_executable(testarray
    ../testarray.cc
)

# files for autofile
add_executable(autofile
    ../autofile.cc
)

# files for bitarray
add_executable(bitarray
    ../bitarray.cc
)

# extra compile options
target_compile_options(nonport PRIVATE -DTEST_NONPORT) 
target_compile_options(voidlist PRIVATE -DTEST_VOIDLIST)
target_compile_options(vdtllist PRIVATE -DTEST_VDTLLIST)
target_compile_options(bit2d PRIVATE -DTEST_BIT2D)
target_compile_options(growbuf PRIVATE -DTEST_GROWBUF)
target_compile_options(strdict PRIVATE -DTEST_STRDICT)
target_compile_options(svdict PRIVATE -DTEST_SVDICT)
target_compile_options(str PRIVATE -DTEST_STR)
target_compile_options(strutil PRIVATE -DTEST_STRUTIL)
target_compile_options(strhash PRIVATE -DTEST_STRHASH)
target_compile_options(trdelete PRIVATE -DTEST_TRDELETE)
target_compile_options(bflatten PRIVATE -DTEST_BFLATTEN)
target_compile_options(mysig PRIVATE -DTEST_MYSIG)
target_compile_options(mypopen PRIVATE -DTEST_MYPOPEN -Wno-maybe-uninitialized)
target_compile_options(cycles PRIVATE -DTEST_CYCLES)
target_compile_options(crc PRIVATE -DTEST_CRC)
target_compile_options(srcloc PRIVATE -DTEST_SRCLOC)
target_compile_options(hashline PRIVATE -DTEST_HASHLINE)
target_compile_options(gprintf PRIVATE -DTEST_GPRINTF)
target_compile_options(smregexp PRIVATE -DTEST_SMREGEXP)
target_compile_options(vptrmap PRIVATE -DTEST_VPTRMAP)
target_compile_options(pprint PRIVATE -DTEST_PPRINT)
target_compile_options(boxprint PRIVATE -DTEST_BOXPRINT)
target_compile_options(autofile PRIVATE -DTEST_AUTOFILE)
target_compile_options(bitarray PRIVATE -DTEST_BITARRAY)

# link options
target_link_libraries(voidlist smbase)
target_link_libraries(vdtllist smbase)
target_link_libraries(taillist_test smbase)
target_link_libraries(tobjlist smbase)
target_link_libraries(tsobjlist smbase)
target_link_libraries(bit2d smbase)
target_link_libraries(growbuf smbase)
target_link_libraries(strdict smbase)
target_link_libraries(svdict smbase)
target_link_libraries(str smbase)
target_link_libraries(strutil smbase)
target_link_libraries(strhash smbase)
target_link_libraries(trdelete smbase)
target_link_libraries(bflatten smbase)
target_link_libraries(mysig smbase)
target_link_libraries(testmalloc smbase)
target_link_libraries(tobjpool smbase)
target_link_libraries(srcloc smbase)
target_link_libraries(hashline smbase)
target_link_libraries(smregexp smbase)
target_link_libraries(vptrmap smbase)
target_link_libraries(pprint smbase)
target_link_libraries(boxprint smbase)
target_link_libraries(tarrayqueue smbase)
target_link_libraries(testarray smbase)
target_link_libraries(autofile smbase)
target_link_libraries(bitarray smbase)

# add the tests
add_test(NAME nonport COMMAND ./nonport)
add_test(NAME voidlist COMMAND ./voidlist)
add_test(NAME vdtllist COMMAND ./vdtllist)
add_test(NAME taillist_test COMMAND ./taillist_test)
add_test(NAME tobjlist COMMAND ./tobjlist)
add_test(NAME tsobjlist COMMAND ./tsobjlist)
add_test(NAME bit2d COMMAND ./bit2d)
add_test(NAME growbuf COMMAND ./growbuf)
add_test(NAME strdict COMMAND ./strdict)
add_test(NAME svdict COMMAND ./svdict)
add_test(NAME str COMMAND ./str)
add_test(NAME strutil COMMAND ./strutil)
add_test(NAME strhash COMMAND ./strhash)
add_test(NAME trdelete COMMAND ./trdelete)
add_test(NAME bflatten COMMAND ./bflatten)
add_test(NAME mysig COMMAND ./mysig)
add_test(NAME testmalloc COMMAND ./testmalloc)
add_test(NAME mypopen COMMAND ./mypopen)
add_test(NAME tobjpool COMMAND ./tobjpool)
add_test(NAME cycles COMMAND ./cycles)
add_test(NAME crc COMMAND ./crc)
# set WORKING_DIRECTORY because it needs srcloc.test.cc and srcloc.test2.cc
add_test(NAME srcloc COMMAND ${CMAKE_CURRENT_BINARY_DIR}/srcloc WORKING_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/../)
add_test(NAME hashline COMMAND ./hashline)
add_test(NAME gprintf COMMAND ./gprintf)
add_test(NAME smregexp COMMAND ./smregexp)
add_test(NAME vptrmap COMMAND ./vptrmap)
add_test(NAME pprint COMMAND ./pprint)
add_test(NAME boxprint COMMAND ./boxprint)
add_test(NAME tarrayqueue COMMAND ./tarrayqueue)
add_test(NAME testarray COMMAND ./testarray)
add_test(NAME autofile COMMAND ./autofile)
add_test(NAME bitarray COMMAND ./bitarray)