
#GSON

### Gson 사용하기
---
> Project_A
```
import java.util.ArrayList;
import java.util.List;

import com.google.gson.Gson;
import com.google.gson.reflect.TypeToken;

import kr.Inflean.BookDTO;

public class Project_A {
	
	public static void main(String[]args) {
		BookDTO dto = new BookDTO("자바", 21000, "에이콘", 670);
		Gson g = new Gson();
		String json = g.toJson(dto); // DTO -> JSON형식으로 변경
		System.out.println(json);
		BookDTO dto1 = g.fromJson(json, BookDTO.class); //JSON형식 -> DTO로 변경
		System.out.println(dto1);
		
		List<BookDTO> lst = new ArrayList<BookDTO>(); 
		
		lst.add(new BookDTO("자바1", 11000, "에이콘1", 570));
		lst.add(new BookDTO("자바2", 21000, "에이콘2", 470));
		lst.add(new BookDTO("자바3", 31000, "에이콘3", 370));
		
		String lstJson = g.toJson(lst);   // 리스트형식<DTO> -> JSON 여러개형식으로 변경가능!
		
		
		// //JSON형식 -> 리스트형식<DTO> 로 변경가능 중요!
		List<BookDTO> lst2 = g.fromJson(lstJson, new TypeToken<List<BookDTO>>() {}.getType());
		for(BookDTO vo : lst2) {
			System.out.println(vo);
		}
	}
	
}

```

