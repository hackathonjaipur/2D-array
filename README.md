# 2D-array
#include<iostream>
using namespace std;
class array
{
	public:
 int **ptr,row,col;
 void setsize();
 void destory();
 void read();
 void print();


};
void array:: setsize()
{
	cout<<"enter number of rows and column"<<endl;
	cin>>row>>col;
	ptr=new int *[row];
	for( int i=0; i<row ; i++ )
	{

		ptr[i]= new int[col];

	}


}


void array :: destory()
{
	for (int i = 0; i<row ;i++)
    {
		 delete ptr[i];
		 delete ptr;

	}


}

void array::read()
{
	int i,j;
	for(i=0;i<row;i++)
	{
		for(j=0;j<col;j++)
		{
			cin>>ptr[i][j];
		}

	}


}


void array::print()
{
	int i,j;
	for(i=0;i<row;i++)
	{
		for(j=0;j<col;j++)
		{
			cout<<ptr[i][j]<<"  ";
		}
		cout<<"\n";

	}



}
int main(){
	array a1;
	cout<<"enter the size of array "<<endl;
	a1.setsize();
	cout<<"enter the value of array element : "<<endl;
	a1.read();
	cout<<"your array is"<<endl;
	a1.print();
	a1. destory();


return 0;
}
