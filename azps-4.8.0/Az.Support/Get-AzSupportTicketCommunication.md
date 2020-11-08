---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
ms.openlocfilehash: 07a8747f94f9c1fb93bbff06ce855363088a67a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243172"
---
# <span data-ttu-id="a19d1-101">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="a19d1-101">Get-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="a19d1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a19d1-102">SYNOPSIS</span></span>
<span data-ttu-id="a19d1-103">Обратитесь в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="a19d1-103">Get support ticket communications.</span></span>

## <span data-ttu-id="a19d1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a19d1-104">SYNTAX</span></span>

### <span data-ttu-id="a19d1-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a19d1-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSupportTicketCommunication -SupportTicketName <String> [-Name <String>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

### <span data-ttu-id="a19d1-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a19d1-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSupportTicketCommunication [-Name <String>] -SupportTicketObject <PSSupportTicket> [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## <span data-ttu-id="a19d1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a19d1-107">DESCRIPTION</span></span>
<span data-ttu-id="a19d1-108">Получает связь с билетом поддержки.</span><span class="sxs-lookup"><span data-stu-id="a19d1-108">Gets communications for a support ticket.</span></span> <span data-ttu-id="a19d1-109">Если вы не укажете никаких других параметров, она будет извлекать все сообщения для билета.</span><span class="sxs-lookup"><span data-stu-id="a19d1-109">It will retrieve all the communications for a ticket if you do not specify any other parameters.</span></span> <span data-ttu-id="a19d1-110">Вы также можете отфильтровать связь по аргументы или CommunicationType с помощью параметра Filter.</span><span class="sxs-lookup"><span data-stu-id="a19d1-110">You can also filter the communications by CreatedDate or CommunicationType using the Filter parameter.</span></span> <span data-ttu-id="a19d1-111">Ниже приведены некоторые примеры значений фильтров, которые можно задать.</span><span class="sxs-lookup"><span data-stu-id="a19d1-111">Here are some examples of filter values that you can specify.</span></span>


| <span data-ttu-id="a19d1-112">Вариант</span><span class="sxs-lookup"><span data-stu-id="a19d1-112">Scenario</span></span>                                                        | <span data-ttu-id="a19d1-113">Отбор</span><span class="sxs-lookup"><span data-stu-id="a19d1-113">Filter</span></span>                                                     |
|-----------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="a19d1-114">Получение веб-сообщений</span><span class="sxs-lookup"><span data-stu-id="a19d1-114">Get Web communications</span></span>                                          | <span data-ttu-id="a19d1-115">"CommunicationType EQ" веб "</span><span class="sxs-lookup"><span data-stu-id="a19d1-115">"CommunicationType eq 'Web'"</span></span>                               |
| <span data-ttu-id="a19d1-116">Получение телефонной связи</span><span class="sxs-lookup"><span data-stu-id="a19d1-116">Get Phone communications</span></span>                                        | <span data-ttu-id="a19d1-117">"CommunicationType EQ" Phone ""</span><span class="sxs-lookup"><span data-stu-id="a19d1-117">"CommunicationType eq 'Phone'"</span></span>                             |
| <span data-ttu-id="a19d1-118">Получайте сообщения, созданные в течение 20 декабря 2019 г.</span><span class="sxs-lookup"><span data-stu-id="a19d1-118">Get communications that were created on or after 20th Dec, 2019</span></span> | <span data-ttu-id="a19d1-119">"Аргументы GE 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="a19d1-119">"CreatedDate ge 2019-12-20"</span></span>                                |
| <span data-ttu-id="a19d1-120">Получение сообщений, созданных после 20 декабря 2019 г.</span><span class="sxs-lookup"><span data-stu-id="a19d1-120">Get communications that were created after 20th Dec, 2019</span></span>       | <span data-ttu-id="a19d1-121">"Аргументы gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="a19d1-121">"CreatedDate gt 2019-12-20"</span></span>                                |
| <span data-ttu-id="a19d1-122">Возвращает веб-связь, созданную после 20 декабря 2019 г.</span><span class="sxs-lookup"><span data-stu-id="a19d1-122">Gets Web communications created after 20th Dec, 2019</span></span>            | <span data-ttu-id="a19d1-123">"Аргументы gt 2019-12-20 и CommunicationType EQ" веб "</span><span class="sxs-lookup"><span data-stu-id="a19d1-123">"CreatedDate gt 2019-12-20 and CommunicationType eq 'Web'"</span></span> |


<span data-ttu-id="a19d1-124">Этот командлет поддерживает разбиение по страницам через первый и пропускаемые параметры.</span><span class="sxs-lookup"><span data-stu-id="a19d1-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="a19d1-125">Кроме того, вы можете получить один из билетов на запрос о поддержке, указав имя для связи.</span><span class="sxs-lookup"><span data-stu-id="a19d1-125">You can also retrieve a single support ticket communication by specifying the communication name.</span></span> 

## <span data-ttu-id="a19d1-126">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a19d1-126">EXAMPLES</span></span>

### <span data-ttu-id="a19d1-127">Пример 1: получение всех сообщений для билета поддержки</span><span class="sxs-lookup"><span data-stu-id="a19d1-127">Example 1: Retrieve all communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

### <span data-ttu-id="a19d1-128">Пример 2: получение единого общения по имени для билета в службу поддержки</span><span class="sxs-lookup"><span data-stu-id="a19d1-128">Example 2: Retrieve a single communication by it's name for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Name "testmessage1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage1 user@contoso.com     test message   2/4/2020 9:38:14 PM
```

### <span data-ttu-id="a19d1-129">Пример 3: получение первых 2 связей для билета поддержки</span><span class="sxs-lookup"><span data-stu-id="a19d1-129">Example 3: Retrieve first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="a19d1-130">Пример 4: получение следующих 2 связей после пропуска первых двух коммуникаций для билета в службу поддержки</span><span class="sxs-lookup"><span data-stu-id="a19d1-130">Example 4: Retrieve next 2 communications after skipping first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Skip 2 -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage4 user@contoso.com     test message4  2/4/2020 9:38:14 PM
testmessage5 user@contoso.com     test message5  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="a19d1-131">Пример 5: получение всех веб-соединений для билета поддержки</span><span class="sxs-lookup"><span data-stu-id="a19d1-131">Example 5: Retrieve all Web communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web'"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="a19d1-132">Пример 6: получение всех связей, созданных на время или после 20 декабря 2019 для билета в службу поддержки</span><span class="sxs-lookup"><span data-stu-id="a19d1-132">Example 6: Retrieve all communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="a19d1-133">Пример 7: получение всех веб-связей, созданных по адресу или после декабря Dec, 2019 для получения билета в службу поддержки</span><span class="sxs-lookup"><span data-stu-id="a19d1-133">Example 7: Retrieve all Web communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web' and CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="a19d1-134">Пример 8: получение всех сообщений для билета поддержки по объекту билета поддержки трубопроводов</span><span class="sxs-lookup"><span data-stu-id="a19d1-134">Example 8: Retrieve all communications for a support ticket by piping support ticket object</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Get-AzSupportTicketCommunication

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

## <span data-ttu-id="a19d1-135">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a19d1-135">PARAMETERS</span></span>

### <span data-ttu-id="a19d1-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a19d1-136">-DefaultProfile</span></span>
<span data-ttu-id="a19d1-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a19d1-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a19d1-138">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="a19d1-138">-Filter</span></span>
<span data-ttu-id="a19d1-139">Фильтр, применяемый к результатам этого командлета.</span><span class="sxs-lookup"><span data-stu-id="a19d1-139">Filter to be applied to the results of this cmdlet.</span></span>

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

### <span data-ttu-id="a19d1-140">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a19d1-140">-Name</span></span>
<span data-ttu-id="a19d1-141">Имя связи.</span><span class="sxs-lookup"><span data-stu-id="a19d1-141">Communication name.</span></span>

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

### <span data-ttu-id="a19d1-142">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="a19d1-142">-SupportTicketName</span></span>
<span data-ttu-id="a19d1-143">Имя билета в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="a19d1-143">Support ticket name.</span></span>

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

### <span data-ttu-id="a19d1-144">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="a19d1-144">-SupportTicketObject</span></span>
<span data-ttu-id="a19d1-145">Объект билета в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="a19d1-145">Support ticket object.</span></span>

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

### <span data-ttu-id="a19d1-146">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="a19d1-146">-IncludeTotalCount</span></span>
<span data-ttu-id="a19d1-147">Показывает общее количество объектов в наборе данных (целое число), за которыми следуют выбранные объекты.</span><span class="sxs-lookup"><span data-stu-id="a19d1-147">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="a19d1-148">Если командлет не может определить общее количество, выводится сообщение "неизвестное общее количество".</span><span class="sxs-lookup"><span data-stu-id="a19d1-148">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="a19d1-149">Целочисленное значение имеет свойство точности, которое указывает на надежность общего значения Count.</span><span class="sxs-lookup"><span data-stu-id="a19d1-149">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="a19d1-150">Значение точности в диапазоне от 0,0 до 1,0, где 0,0 означает, что командлет не может подсчитать объекты, 1,0 означает, что счетчик является точным, а значение в диапазоне от 0,0 и 1,0 указывает на то, что все более надежная оценка.</span><span class="sxs-lookup"><span data-stu-id="a19d1-150">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="a19d1-151">-Skip</span><span class="sxs-lookup"><span data-stu-id="a19d1-151">-Skip</span></span>
<span data-ttu-id="a19d1-152">Пропускает указанное количество объектов и возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="a19d1-152">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="a19d1-153">Введите количество объектов для пропуска.</span><span class="sxs-lookup"><span data-stu-id="a19d1-153">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="a19d1-154">-First</span><span class="sxs-lookup"><span data-stu-id="a19d1-154">-First</span></span>
<span data-ttu-id="a19d1-155">Возвращает только указанное количество объектов.</span><span class="sxs-lookup"><span data-stu-id="a19d1-155">Gets only the specified number of objects.</span></span>
<span data-ttu-id="a19d1-156">Введите количество получаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="a19d1-156">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="a19d1-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a19d1-157">CommonParameters</span></span>
<span data-ttu-id="a19d1-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a19d1-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a19d1-159">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a19d1-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a19d1-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a19d1-160">INPUTS</span></span>

### <span data-ttu-id="a19d1-161">Microsoft. Azure. Commands. support. Models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="a19d1-161">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="a19d1-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a19d1-162">OUTPUTS</span></span>

### <span data-ttu-id="a19d1-163">Microsoft. Azure. Commands. support. Models. PSSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="a19d1-163">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="a19d1-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="a19d1-164">NOTES</span></span>

## <span data-ttu-id="a19d1-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a19d1-165">RELATED LINKS</span></span>
