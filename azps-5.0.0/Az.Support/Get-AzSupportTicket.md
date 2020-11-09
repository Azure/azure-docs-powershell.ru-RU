---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
ms.openlocfilehash: 368ae4ad814c9414ea211ea6e44c2d3fbda005f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318197"
---
# <span data-ttu-id="7cc1c-101">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="7cc1c-101">Get-AzSupportTicket</span></span>

## <span data-ttu-id="7cc1c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7cc1c-102">SYNOPSIS</span></span>
<span data-ttu-id="7cc1c-103">Получение билетов на техническую поддержку.</span><span class="sxs-lookup"><span data-stu-id="7cc1c-103">Get support tickets.</span></span>

## <span data-ttu-id="7cc1c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7cc1c-104">SYNTAX</span></span>

### <span data-ttu-id="7cc1c-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7cc1c-105">ListParameterSet (Default)</span></span>
```
Get-AzSupportTicket [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7cc1c-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cc1c-106">GetByNameParameterSet</span></span>
```
Get-AzSupportTicket -Name <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="7cc1c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7cc1c-107">DESCRIPTION</span></span>
<span data-ttu-id="7cc1c-108">Получает список билетов поддержки.</span><span class="sxs-lookup"><span data-stu-id="7cc1c-108">Gets the list of support tickets.</span></span> <span data-ttu-id="7cc1c-109">При отсутствии каких бы то ни было параметров будут извлекаться все билеты поддержки.</span><span class="sxs-lookup"><span data-stu-id="7cc1c-109">It will retrieve all the support tickets if you do not specify any parameters.</span></span> <span data-ttu-id="7cc1c-110">Вы также можете отфильтровать билеты поддержки по состоянию или аргументы с помощью параметра Filter.</span><span class="sxs-lookup"><span data-stu-id="7cc1c-110">You can also filter the support tickets by Status or CreatedDate using the Filter parameter.</span></span> <span data-ttu-id="7cc1c-111">Ниже приведены некоторые примеры значений фильтров, которые можно задать.</span><span class="sxs-lookup"><span data-stu-id="7cc1c-111">Here are some examples of filter values that you can specify.</span></span>

| <span data-ttu-id="7cc1c-112">Вариант</span><span class="sxs-lookup"><span data-stu-id="7cc1c-112">Scenario</span></span>                                                         | <span data-ttu-id="7cc1c-113">Отбор</span><span class="sxs-lookup"><span data-stu-id="7cc1c-113">Filter</span></span>                                           |
|------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="7cc1c-114">Получение билетов в открытом состоянии</span><span class="sxs-lookup"><span data-stu-id="7cc1c-114">Get tickets that are in open state</span></span>                               | <span data-ttu-id="7cc1c-115">"Состояние EQ" Открыть "</span><span class="sxs-lookup"><span data-stu-id="7cc1c-115">"Status eq 'Open'"</span></span>                               |
| <span data-ttu-id="7cc1c-116">Получение билетов, которые находятся в закрытом состоянии</span><span class="sxs-lookup"><span data-stu-id="7cc1c-116">Get tickets that are in closed state</span></span>                             | <span data-ttu-id="7cc1c-117">"Состояние EQ" закрыто "</span><span class="sxs-lookup"><span data-stu-id="7cc1c-117">"Status eq 'Closed'"</span></span>                             |
| <span data-ttu-id="7cc1c-118">Получение билетов, созданных в течение 20 декабря 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7cc1c-118">Get tickets that were created on or after 20th Dec, 2019</span></span>         | <span data-ttu-id="7cc1c-119">"Аргументы GE 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="7cc1c-119">"CreatedDate ge 2019-12-20"</span></span>                      |
| <span data-ttu-id="7cc1c-120">Получение билетов, созданных после 20 декабря 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7cc1c-120">Get tickets that were created after 20th Dec, 2019</span></span>               | <span data-ttu-id="7cc1c-121">"Аргументы gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="7cc1c-121">"CreatedDate gt 2019-12-20"</span></span>                      |
| <span data-ttu-id="7cc1c-122">Получает билеты, созданные после 20 декабря, 2019, которые находятся в открытом состоянии.</span><span class="sxs-lookup"><span data-stu-id="7cc1c-122">Gets tickets created after 20th Dec, 2019 that are in open state</span></span> | <span data-ttu-id="7cc1c-123">"Аргументы gt 2019-12-20 и состояние EQ" Open ""</span><span class="sxs-lookup"><span data-stu-id="7cc1c-123">"CreatedDate gt 2019-12-20 and Status eq 'Open'"</span></span> |


<span data-ttu-id="7cc1c-124">Этот командлет поддерживает разбиение по страницам через первый и пропускаемые параметры.</span><span class="sxs-lookup"><span data-stu-id="7cc1c-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="7cc1c-125">Кроме того, вы можете получить один из билетов на службу поддержки, указав имя билета.</span><span class="sxs-lookup"><span data-stu-id="7cc1c-125">You can also retrieve a single support ticket by specifying the ticket name.</span></span> 

## <span data-ttu-id="7cc1c-126">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7cc1c-126">EXAMPLES</span></span>

### <span data-ttu-id="7cc1c-127">Пример 1: получение первых 2 билетов</span><span class="sxs-lookup"><span data-stu-id="7cc1c-127">Example 1: Get first 2 tickets</span></span>
```powershell
PS C:\> Get-AzSupportTicket -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="7cc1c-128">Пример 2: получение первых 2 билетов после пропуска первых 2</span><span class="sxs-lookup"><span data-stu-id="7cc1c-128">Example 2: Get first 2 tickets after skipping the first 2</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Skip 2 -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test3 test title3                  150010521000314 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test4 test title4                  150010521000315 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="7cc1c-129">Пример 3: получение билета в службу поддержки по имени</span><span class="sxs-lookup"><span data-stu-id="7cc1c-129">Example 3: Get a support ticket by name</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="7cc1c-130">Пример 4: получение первых 2 билетов поддержки отфильтровано по состоянию</span><span class="sxs-lookup"><span data-stu-id="7cc1c-130">Example 4: Get first 2 support tickets filtered by status</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Closed'" -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="7cc1c-131">Пример 5: получение всех билетов на поддержку, которые находятся в открытом состоянии и созданы после 20 декабря 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7cc1c-131">Example 5: Get all support tickets that are in Open state and created after Dec 20th, 2019</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Open' and CreatedDate gt 2019-12-20"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test6 test title6                  150010521000311 Minimal  Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
test7 test title7                  150010521000312 Minimal  Billing                       Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="7cc1c-132">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7cc1c-132">PARAMETERS</span></span>

### <span data-ttu-id="7cc1c-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cc1c-133">-DefaultProfile</span></span>
<span data-ttu-id="7cc1c-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7cc1c-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cc1c-135">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="7cc1c-135">-Filter</span></span>
<span data-ttu-id="7cc1c-136">Фильтр, применяемый к результатам этого командлета.</span><span class="sxs-lookup"><span data-stu-id="7cc1c-136">Filter to be applied to the results of this cmdlet.</span></span>

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

### <span data-ttu-id="7cc1c-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7cc1c-137">-Name</span></span>
<span data-ttu-id="7cc1c-138">Имя билета в службу поддержки, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7cc1c-138">Name of support ticket that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7cc1c-139">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="7cc1c-139">-IncludeTotalCount</span></span>
<span data-ttu-id="7cc1c-140">Показывает общее количество объектов в наборе данных (целое число), за которыми следуют выбранные объекты.</span><span class="sxs-lookup"><span data-stu-id="7cc1c-140">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="7cc1c-141">Если командлет не может определить общее количество, выводится сообщение "неизвестное общее количество".</span><span class="sxs-lookup"><span data-stu-id="7cc1c-141">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="7cc1c-142">Целочисленное значение имеет свойство точности, которое указывает на надежность общего значения Count.</span><span class="sxs-lookup"><span data-stu-id="7cc1c-142">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="7cc1c-143">Значение точности в диапазоне от 0,0 до 1,0, где 0,0 означает, что командлет не может подсчитать объекты, 1,0 означает, что счетчик является точным, а значение в диапазоне от 0,0 и 1,0 указывает на то, что все более надежная оценка.</span><span class="sxs-lookup"><span data-stu-id="7cc1c-143">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="7cc1c-144">-Skip</span><span class="sxs-lookup"><span data-stu-id="7cc1c-144">-Skip</span></span>
<span data-ttu-id="7cc1c-145">Пропускает указанное количество объектов и возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="7cc1c-145">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="7cc1c-146">Введите количество объектов для пропуска.</span><span class="sxs-lookup"><span data-stu-id="7cc1c-146">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="7cc1c-147">-First</span><span class="sxs-lookup"><span data-stu-id="7cc1c-147">-First</span></span>
<span data-ttu-id="7cc1c-148">Возвращает только указанное количество объектов.</span><span class="sxs-lookup"><span data-stu-id="7cc1c-148">Gets only the specified number of objects.</span></span>
<span data-ttu-id="7cc1c-149">Введите количество получаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="7cc1c-149">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="7cc1c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cc1c-150">CommonParameters</span></span>
<span data-ttu-id="7cc1c-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7cc1c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cc1c-152">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7cc1c-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cc1c-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7cc1c-153">INPUTS</span></span>

### <span data-ttu-id="7cc1c-154">Ничего</span><span class="sxs-lookup"><span data-stu-id="7cc1c-154">None</span></span>

## <span data-ttu-id="7cc1c-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7cc1c-155">OUTPUTS</span></span>

### <span data-ttu-id="7cc1c-156">Microsoft. Azure. Commands. support. Models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="7cc1c-156">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="7cc1c-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="7cc1c-157">NOTES</span></span>

## <span data-ttu-id="7cc1c-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7cc1c-158">RELATED LINKS</span></span>
