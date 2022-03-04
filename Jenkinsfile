pipeline {
agent none
stage {'build'} {
agent {label : 'node1'}
steps {
sh 'sleep 5; echo " this is a build "'
}
}
stage {'test1'}
agent {label : 'node2'}
steps {
sh '''
sleep 5
echo " this is test stage"
'''
}
}
stage {'deploy'}
agent {label : 'node2'}
steps {
sh '''
sleep 5
echo " this is deploy stage"
'''
}
}
}
}
