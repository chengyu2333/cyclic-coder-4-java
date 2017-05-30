# cyclic-coder-4-java
### 这是一个用java实现的循环码编码译码的类,可以将4位二进制数据编码，译码有1位的纠错能力
### 使用方法：
```
package cyclic;
public class Test {

	public static void main(String[] args) {
		String encodeResult;
		String encodeInput = "1010";
		
		System.out.println("原文");
		System.out.println(encodeInput);
		
		CyclicCoder cc = new CyclicCoder();
		encodeResult = Integer.toBinaryString(cc.encode(Integer.parseInt(encodeInput, 2)));
		System.out.println("编码");
		System.out.println(encodeResult);
		
		int decodeInput = Integer.parseInt(encodeResult,2);
		System.out.println("译码");
		System.out.println(Integer.toBinaryString(cc.decode(decodeInput)));
	}
}
```
###输出
```
原文
1010
编码
1010011
译码
1010
```
