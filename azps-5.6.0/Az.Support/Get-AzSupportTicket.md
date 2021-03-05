---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/powershell/module/az.support/get-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
ms.openlocfilehash: c5f68e947af383787b3ed1e7d9c9c3983c45769b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008280"
---
# <span data-ttu-id="5ca0d-101">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="5ca0d-101">Get-AzSupportTicket</span></span>

## <span data-ttu-id="5ca0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ca0d-102">SYNOPSIS</span></span>
<span data-ttu-id="5ca0d-103">Получить билеты в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-103">Get support tickets.</span></span>

## <span data-ttu-id="5ca0d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5ca0d-104">SYNTAX</span></span>

### <span data-ttu-id="5ca0d-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5ca0d-105">ListParameterSet (Default)</span></span>
```
Get-AzSupportTicket [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="5ca0d-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ca0d-106">GetByNameParameterSet</span></span>
```
Get-AzSupportTicket -Name <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="5ca0d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ca0d-107">DESCRIPTION</span></span>
<span data-ttu-id="5ca0d-108">Список билетов в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-108">Gets the list of support tickets.</span></span> <span data-ttu-id="5ca0d-109">Он получит все билеты в службу поддержки, если не указать параметры.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-109">It will retrieve all the support tickets if you do not specify any parameters.</span></span> <span data-ttu-id="5ca0d-110">Вы также можете фильтровать билеты в службу поддержки по status или CreatedDate с помощью параметра Filter.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-110">You can also filter the support tickets by Status or CreatedDate using the Filter parameter.</span></span> <span data-ttu-id="5ca0d-111">Вот несколько примеров значений фильтра, которые можно указать.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-111">Here are some examples of filter values that you can specify.</span></span>

| <span data-ttu-id="5ca0d-112">Сценарий</span><span class="sxs-lookup"><span data-stu-id="5ca0d-112">Scenario</span></span>                                                         | <span data-ttu-id="5ca0d-113">Фильтр</span><span class="sxs-lookup"><span data-stu-id="5ca0d-113">Filter</span></span>                                           |
|------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="5ca0d-114">Получить открытые билеты</span><span class="sxs-lookup"><span data-stu-id="5ca0d-114">Get tickets that are in open state</span></span>                               | <span data-ttu-id="5ca0d-115">"Status eq 'Open'"</span><span class="sxs-lookup"><span data-stu-id="5ca0d-115">"Status eq 'Open'"</span></span>                               |
| <span data-ttu-id="5ca0d-116">Получить билеты, которые находятся в закрытом состоянии</span><span class="sxs-lookup"><span data-stu-id="5ca0d-116">Get tickets that are in closed state</span></span>                             | <span data-ttu-id="5ca0d-117">"Status eq 'Closed'"</span><span class="sxs-lookup"><span data-stu-id="5ca0d-117">"Status eq 'Closed'"</span></span>                             |
| <span data-ttu-id="5ca0d-118">Получите билеты, созданные 20 декабря 2019 г. или после этого</span><span class="sxs-lookup"><span data-stu-id="5ca0d-118">Get tickets that were created on or after 20th Dec, 2019</span></span>         | <span data-ttu-id="5ca0d-119">"CreatedDate ge 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="5ca0d-119">"CreatedDate ge 2019-12-20"</span></span>                      |
| <span data-ttu-id="5ca0d-120">Получить билеты, созданные после 20 декабря 2019 г.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-120">Get tickets that were created after 20th Dec, 2019</span></span>               | <span data-ttu-id="5ca0d-121">"CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="5ca0d-121">"CreatedDate gt 2019-12-20"</span></span>                      |
| <span data-ttu-id="5ca0d-122">Возвращает количество открытых билетов, созданных после 20 декабря 2019 г.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-122">Gets tickets created after 20th Dec, 2019 that are in open state</span></span> | <span data-ttu-id="5ca0d-123">"CreatedDate gt 2019-12-20 and Status eq 'Open'"</span><span class="sxs-lookup"><span data-stu-id="5ca0d-123">"CreatedDate gt 2019-12-20 and Status eq 'Open'"</span></span> |


<span data-ttu-id="5ca0d-124">Этот cmdlet поддерживает разведданный с помощью параметров First и Skip.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="5ca0d-125">Вы также можете получить один билет в службу поддержки, указав его имя.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-125">You can also retrieve a single support ticket by specifying the ticket name.</span></span> 

## <span data-ttu-id="5ca0d-126">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5ca0d-126">EXAMPLES</span></span>

### <span data-ttu-id="5ca0d-127">Пример 1. Получить первые 2 билетов</span><span class="sxs-lookup"><span data-stu-id="5ca0d-127">Example 1: Get first 2 tickets</span></span>
```powershell
PS C:\> Get-AzSupportTicket -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="5ca0d-128">Пример 2. Получите первые 2 билета после пропуска первых 2</span><span class="sxs-lookup"><span data-stu-id="5ca0d-128">Example 2: Get first 2 tickets after skipping the first 2</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Skip 2 -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test3 test title3                  150010521000314 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test4 test title4                  150010521000315 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="5ca0d-129">Пример 3. Получить билет в службу поддержки по имени</span><span class="sxs-lookup"><span data-stu-id="5ca0d-129">Example 3: Get a support ticket by name</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="5ca0d-130">Пример 4. Первые 2 билета в службу поддержки отфильтровыются по статусу</span><span class="sxs-lookup"><span data-stu-id="5ca0d-130">Example 4: Get first 2 support tickets filtered by status</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Closed'" -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="5ca0d-131">Пример 5. Получить все билеты в службу поддержки, созданные после 20 декабря 2019 г. в состоянии "Открыть"</span><span class="sxs-lookup"><span data-stu-id="5ca0d-131">Example 5: Get all support tickets that are in Open state and created after Dec 20th, 2019</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Open' and CreatedDate gt 2019-12-20"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test6 test title6                  150010521000311 Minimal  Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
test7 test title7                  150010521000312 Minimal  Billing                       Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="5ca0d-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ca0d-132">PARAMETERS</span></span>

### <span data-ttu-id="5ca0d-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ca0d-133">-DefaultProfile</span></span>
<span data-ttu-id="5ca0d-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ca0d-135">-Filter</span><span class="sxs-lookup"><span data-stu-id="5ca0d-135">-Filter</span></span>
<span data-ttu-id="5ca0d-136">Фильтр, применяемый к результатам этого cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-136">Filter to be applied to the results of this cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca0d-137">-Name</span><span class="sxs-lookup"><span data-stu-id="5ca0d-137">-Name</span></span>
<span data-ttu-id="5ca0d-138">Имя билета в службу поддержки, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-138">Name of support ticket that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5ca0d-139">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="5ca0d-139">-IncludeTotalCount</span></span>
<span data-ttu-id="5ca0d-140">Отчет об общем количестве объектов в наборе данных (integer), за которым следуют выбранные объекты.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-140">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="5ca0d-141">Если не удается определить общее количество, отображается "Неизвестное общее количество".</span><span class="sxs-lookup"><span data-stu-id="5ca0d-141">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="5ca0d-142">У значения integer есть свойство "Точность", которое указывает на надежность общего количества значений.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-142">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="5ca0d-143">Значение точности в диапазонах от 0,0 до 1,0, где 0,0 означает, что не удалось подсчитать объекты, 1,0 означает, что число точное, а значение от 0,0 до 1,0 указывает на более надежную оценку.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-143">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="5ca0d-144">-Skip</span><span class="sxs-lookup"><span data-stu-id="5ca0d-144">-Skip</span></span>
<span data-ttu-id="5ca0d-145">Игнорирует указанное количество объектов, а затем возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-145">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="5ca0d-146">Введите количество объектов, которые нужно пропустить.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-146">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="5ca0d-147">-First</span><span class="sxs-lookup"><span data-stu-id="5ca0d-147">-First</span></span>
<span data-ttu-id="5ca0d-148">Возвращает только указанное количество объектов.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-148">Gets only the specified number of objects.</span></span>
<span data-ttu-id="5ca0d-149">Введите количество объектов, которые нужно получить.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-149">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="5ca0d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ca0d-150">CommonParameters</span></span>
<span data-ttu-id="5ca0d-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ca0d-152">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ca0d-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ca0d-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5ca0d-153">INPUTS</span></span>

### <span data-ttu-id="5ca0d-154">Нет</span><span class="sxs-lookup"><span data-stu-id="5ca0d-154">None</span></span>

## <span data-ttu-id="5ca0d-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5ca0d-155">OUTPUTS</span></span>

### <span data-ttu-id="5ca0d-156">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="5ca0d-156">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="5ca0d-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5ca0d-157">NOTES</span></span>

## <span data-ttu-id="5ca0d-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ca0d-158">RELATED LINKS</span></span>
