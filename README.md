https://cloud.mail.ru/public/3mQF/Arg6yX3tp/Курс%205%20Core%20Data%20Часть%201/
Видосики по CoreData



Получение контекста из апДелегейт 
let context = (UIApplication.shared.delegate as! AppDelegate).persistentContainer.viewContext


Получение данных из CoreData
let fetchRequest:NSFetchRequest<Cars> = Cars.fetchRequest()
do {
   car = try context.fetch(fetchRequest)
}catch{}
Cars - имя сущности (Entity)
car - массив куда все сохраняться будет
  
  
 
 
Удаление данных
let name = car[inde]
context.delete(name)
do{
   try context.save()
}catch{}

врОДЕ все понятно тут 


Добавление
let entity = NSEntityDescription.entity(forEntityName: "Cars", in: context)
let taskObject = NSManagedObject(entity: entity!, insertInto: context) as! Cars
taskObject.поле сущности = чему равно 
аналогично со всеми полями
do{
  try context.save()
}catch{}
            


Изменение
let name = car[index!]
name.поле сущности = чему равно 
car[index!] = name
do{
  try context.save()
}catch{}
