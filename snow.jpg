// grayscalconvert.cpp : Defines the entry point for the console application.
//

#include "stdafx.h"


void main()
{
	FILE* inFp = nullptr;
	FILE* outFp = nullptr;
	char str[256];
	int inputSize = 0;
	
	unsigned char* inputImage = nullptr;

	fopen_s(&inFp, "C:\\snow.jpg", "r+");
	if( inFp == nullptr )
		printf("\n File dont exists");

	fseek( inFp, 0 , SEEK_END);
	inputSize = ftell( inFp )
	inputImage = new unsigned char[ inputSize ];

	fseek( inFp, 0 , SEEK_SET);
	int pos = ftell(inFp);
	int size = fread( inputImage, 1, inputSize, inFp);

	if( (inputImage[6] == 0x4a) && (inputImage[7] == 0x46) && (inputImage[8] == 0x49) && (inputImage[9] == 0x46) )
	{
		fopen_s( &outFp, "C:\\output.jpg", "ab+");
		fwrite( inputImage, inputSize, 1, outFp );
		fclose( outFp );
	}

	fclose(inFp);

	delete [] inputImage;
}

