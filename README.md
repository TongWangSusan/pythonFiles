pythonFiles
===========

python File operation

outfile = open('E:/change/' + name, 'w')
    for line in lines:
        temp_line_list = line.strip().split('|')
        #lines = AsionIO.get_file_lines(file2)
        #index = 0
        instead = ''
        if temp_line_list[3] == '290':
            #print temp_line_list
            #print '|'.join(temp_line_list[:3]) + '|29|' + '|'.join(temp_line_list[4:])
                //this is the wrong expression for line feed
                #instead = str('|'.join(temp_line_list[:3])) + '|29|' + str('|'.join(temp_line_list[4:] + '/n'))
                #lines.insert(index, instead)
            outfile.write(line)
            instead = str(float(temp_line_list[-3]) * 100) + '|'
            //this is the right expression for line feed
            outfile.write('|'.join(temp_line_list[:3])+ '|29|' + instead + '|'.join(temp_line_list[-2:]) + '\n')
        else:
            outfile.write(line)
    outfile.close()
