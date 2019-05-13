# 6B_merge

// pseudocode

preconditions:
  og ArrayList called usersData
  empty ArrayList called output
  start0, start1, end1
  end0 = start1
postconditions:
  output now has sorted els
  set usersData = output

public void merge( int start0, int start1, int end1){

  for( int index = 0; index < start1 && index < end1; index++){
    if( start0 == start1){ // L0 or L1 is empty now
      store the rest of the usersData in output
    }
    else if( start0 < start1){ // top card of L0 < top card of L1, return top of L0
       output.add( index, start0);
       start0++;
    }
    else{
      output.add( index, usersData.get( start1));
      start1++;
    }
  }
  usersData = mergedData
}
