---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/powershell/module/az.support/get-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
ms.openlocfilehash: 106ee61629c1252300d63ca686848ba7cc926cea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981912"
---
# <span data-ttu-id="c2780-101">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="c2780-101">Get-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="c2780-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2780-102">SYNOPSIS</span></span>
<span data-ttu-id="c2780-103">Получите сообщения в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="c2780-103">Get support ticket communications.</span></span>

## <span data-ttu-id="c2780-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c2780-104">SYNTAX</span></span>

### <span data-ttu-id="c2780-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c2780-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSupportTicketCommunication -SupportTicketName <String> [-Name <String>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2780-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2780-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSupportTicketCommunication [-Name <String>] -SupportTicketObject <PSSupportTicket> [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2780-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2780-107">DESCRIPTION</span></span>
<span data-ttu-id="c2780-108">Получает сообщения для билета в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="c2780-108">Gets communications for a support ticket.</span></span> <span data-ttu-id="c2780-109">Он получит все сообщения для билета, если не указать другие параметры.</span><span class="sxs-lookup"><span data-stu-id="c2780-109">It will retrieve all the communications for a ticket if you do not specify any other parameters.</span></span> <span data-ttu-id="c2780-110">Вы также можете отфильтровать сообщения по CreatedDate или CommunicationType с помощью параметра Filter.</span><span class="sxs-lookup"><span data-stu-id="c2780-110">You can also filter the communications by CreatedDate or CommunicationType using the Filter parameter.</span></span> <span data-ttu-id="c2780-111">Вот несколько примеров значений фильтра, которые можно указать.</span><span class="sxs-lookup"><span data-stu-id="c2780-111">Here are some examples of filter values that you can specify.</span></span>


| <span data-ttu-id="c2780-112">Сценарий</span><span class="sxs-lookup"><span data-stu-id="c2780-112">Scenario</span></span>                                                        | <span data-ttu-id="c2780-113">Фильтр</span><span class="sxs-lookup"><span data-stu-id="c2780-113">Filter</span></span>                                                     |
|-----------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c2780-114">Получить веб-связь</span><span class="sxs-lookup"><span data-stu-id="c2780-114">Get Web communications</span></span>                                          | <span data-ttu-id="c2780-115">"CommunicationType eq 'Web'"</span><span class="sxs-lookup"><span data-stu-id="c2780-115">"CommunicationType eq 'Web'"</span></span>                               |
| <span data-ttu-id="c2780-116">Получить связь по телефону</span><span class="sxs-lookup"><span data-stu-id="c2780-116">Get Phone communications</span></span>                                        | <span data-ttu-id="c2780-117">"CommunicationType eq 'Phone'"</span><span class="sxs-lookup"><span data-stu-id="c2780-117">"CommunicationType eq 'Phone'"</span></span>                             |
| <span data-ttu-id="c2780-118">Получать сообщения, созданные 20 декабря 2019 г. или после этого</span><span class="sxs-lookup"><span data-stu-id="c2780-118">Get communications that were created on or after 20th Dec, 2019</span></span> | <span data-ttu-id="c2780-119">"CreatedDate ge 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="c2780-119">"CreatedDate ge 2019-12-20"</span></span>                                |
| <span data-ttu-id="c2780-120">Получите сообщения, созданные после 20 декабря 2019 г.</span><span class="sxs-lookup"><span data-stu-id="c2780-120">Get communications that were created after 20th Dec, 2019</span></span>       | <span data-ttu-id="c2780-121">"CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="c2780-121">"CreatedDate gt 2019-12-20"</span></span>                                |
| <span data-ttu-id="c2780-122">Возвращает веб-сообщения, созданные после 20 декабря 2019 г.</span><span class="sxs-lookup"><span data-stu-id="c2780-122">Gets Web communications created after 20th Dec, 2019</span></span>            | <span data-ttu-id="c2780-123">"CreatedDate gt 2019-12-20 and CommunicationType eq 'Web'"</span><span class="sxs-lookup"><span data-stu-id="c2780-123">"CreatedDate gt 2019-12-20 and CommunicationType eq 'Web'"</span></span> |


<span data-ttu-id="c2780-124">Этот cmdlet поддерживает разведданный с помощью параметров First и Skip.</span><span class="sxs-lookup"><span data-stu-id="c2780-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="c2780-125">Вы также можете получить сообщение о едином сообщении в службу поддержки, указав его имя.</span><span class="sxs-lookup"><span data-stu-id="c2780-125">You can also retrieve a single support ticket communication by specifying the communication name.</span></span> 

## <span data-ttu-id="c2780-126">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c2780-126">EXAMPLES</span></span>

### <span data-ttu-id="c2780-127">Пример 1. Извлечение всех сообщений для получения билета в службу поддержки</span><span class="sxs-lookup"><span data-stu-id="c2780-127">Example 1: Retrieve all communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

### <span data-ttu-id="c2780-128">Пример 2. Извлечение сообщения по имени для получения билета в службу поддержки</span><span class="sxs-lookup"><span data-stu-id="c2780-128">Example 2: Retrieve a single communication by it's name for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Name "testmessage1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage1 user@contoso.com     test message   2/4/2020 9:38:14 PM
```

### <span data-ttu-id="c2780-129">Пример 3. Извлечение первых 2 сообщений для получения билета в службу поддержки</span><span class="sxs-lookup"><span data-stu-id="c2780-129">Example 3: Retrieve first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="c2780-130">Пример 4. Извлечение следующих 2 сообщений после пропуска первых 2 сообщений для сообщения в службу поддержки</span><span class="sxs-lookup"><span data-stu-id="c2780-130">Example 4: Retrieve next 2 communications after skipping first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Skip 2 -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage4 user@contoso.com     test message4  2/4/2020 9:38:14 PM
testmessage5 user@contoso.com     test message5  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="c2780-131">Пример 5. Извлечение всех веб-сообщений для получения билета в службу поддержки</span><span class="sxs-lookup"><span data-stu-id="c2780-131">Example 5: Retrieve all Web communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web'"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="c2780-132">Пример 6. Извлечение всех сообщений, созданных 20 декабря 2019 г., или после их получения в службу поддержки</span><span class="sxs-lookup"><span data-stu-id="c2780-132">Example 6: Retrieve all communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="c2780-133">Пример 7. Извлечение всех веб-сообщений, созданных 20 декабря 2019 г., или после их получения в службу поддержки</span><span class="sxs-lookup"><span data-stu-id="c2780-133">Example 7: Retrieve all Web communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web' and CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="c2780-134">Пример 8. Извлечение всех сообщений для получения билета в службу поддержки путем прокайки объекта билета поддержки</span><span class="sxs-lookup"><span data-stu-id="c2780-134">Example 8: Retrieve all communications for a support ticket by piping support ticket object</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Get-AzSupportTicketCommunication

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

## <span data-ttu-id="c2780-135">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2780-135">PARAMETERS</span></span>

### <span data-ttu-id="c2780-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2780-136">-DefaultProfile</span></span>
<span data-ttu-id="c2780-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2780-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2780-138">-Filter</span><span class="sxs-lookup"><span data-stu-id="c2780-138">-Filter</span></span>
<span data-ttu-id="c2780-139">Фильтр, применяемый к результатам этого cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2780-139">Filter to be applied to the results of this cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2780-140">-Name</span><span class="sxs-lookup"><span data-stu-id="c2780-140">-Name</span></span>
<span data-ttu-id="c2780-141">Имя связи.</span><span class="sxs-lookup"><span data-stu-id="c2780-141">Communication name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2780-142">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="c2780-142">-SupportTicketName</span></span>
<span data-ttu-id="c2780-143">Имя билета в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="c2780-143">Support ticket name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2780-144">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="c2780-144">-SupportTicketObject</span></span>
<span data-ttu-id="c2780-145">Объект билета в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="c2780-145">Support ticket object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2780-146">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="c2780-146">-IncludeTotalCount</span></span>
<span data-ttu-id="c2780-147">Отчет об общем количестве объектов в наборе данных (integer), за которым следуют выбранные объекты.</span><span class="sxs-lookup"><span data-stu-id="c2780-147">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="c2780-148">Если не удается определить общее количество, отображается "Неизвестное общее количество".</span><span class="sxs-lookup"><span data-stu-id="c2780-148">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="c2780-149">У значения integer есть свойство "Точность", которое указывает на надежность общего количества значений.</span><span class="sxs-lookup"><span data-stu-id="c2780-149">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="c2780-150">Значение точности в диапазонах от 0,0 до 1,0, где 0,0 означает, что не удалось подсчитать объекты, 1,0 означает, что число точное, а значение от 0,0 до 1,0 указывает на более надежную оценку.</span><span class="sxs-lookup"><span data-stu-id="c2780-150">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2780-151">-Skip</span><span class="sxs-lookup"><span data-stu-id="c2780-151">-Skip</span></span>
<span data-ttu-id="c2780-152">Игнорирует указанное количество объектов, а затем возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="c2780-152">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="c2780-153">Введите количество объектов, которые нужно пропустить.</span><span class="sxs-lookup"><span data-stu-id="c2780-153">Enter the number of objects to skip.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2780-154">-First</span><span class="sxs-lookup"><span data-stu-id="c2780-154">-First</span></span>
<span data-ttu-id="c2780-155">Возвращает только указанное количество объектов.</span><span class="sxs-lookup"><span data-stu-id="c2780-155">Gets only the specified number of objects.</span></span>
<span data-ttu-id="c2780-156">Введите количество объектов, которые нужно получить.</span><span class="sxs-lookup"><span data-stu-id="c2780-156">Enter the number of objects to get.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2780-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2780-157">CommonParameters</span></span>
<span data-ttu-id="c2780-158">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2780-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2780-159">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2780-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2780-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2780-160">INPUTS</span></span>

### <span data-ttu-id="c2780-161">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="c2780-161">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="c2780-162">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c2780-162">OUTPUTS</span></span>

### <span data-ttu-id="c2780-163">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="c2780-163">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="c2780-164">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c2780-164">NOTES</span></span>

## <span data-ttu-id="c2780-165">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2780-165">RELATED LINKS</span></span>
