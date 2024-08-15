> `        IEnumerable<long> AoBScanResults = await m.AoBScan("F FF FF FF 00 00 00 00 00 00 00 00 00 00 00 00 ?? ?? ?? ?? ?? ?? ?? ?? ?? ?? ?? ?? ?? ?? ?? ?? 00 00 00 00   00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 A5 43 00 00 00 00", false, true);
>             long SingleAoBScanResult = AoBScanResults.FirstOrDefault();
>             var FinalResult = SingleAoBScanResult;
>             var FinalResult2 = FinalResult + 0x4;
> 
> 
>             uint intValue = 0x90909090;
>             uint intValue2 = 0x9090907E;
>             byte[] intBytes = BitConverter.GetBytes(intValue);
>             byte[] intBytes2 = BitConverter.GetBytes(intValue2);
>             Array.Reverse(intBytes2);
>             Array.Reverse(intBytes);
>             m.WriteBytes(FinalResult.ToString("X"), intBytes);
>             m.WriteBytes(FinalResult2.ToString("X"), intBytes2);
