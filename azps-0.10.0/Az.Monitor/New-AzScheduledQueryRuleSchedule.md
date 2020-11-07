---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
ms.openlocfilehash: e62c8861f370f9e7e7c5b31fea629f3f8e11aa32
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910199"
---
# <span data-ttu-id="a85cb-101">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="a85cb-101">New-AzScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="a85cb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a85cb-102">SYNOPSIS</span></span>
<span data-ttu-id="a85cb-103">Создает объект типа "Расписание".</span><span class="sxs-lookup"><span data-stu-id="a85cb-103">Creates an object of type Schedule</span></span>

## <span data-ttu-id="a85cb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a85cb-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSchedule -FrequencyInMinutes <Int32> -TimeWindowInMinutes <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a85cb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a85cb-105">DESCRIPTION</span></span>
<span data-ttu-id="a85cb-106">Создает объект типа "Расписание".</span><span class="sxs-lookup"><span data-stu-id="a85cb-106">Creates an object of type Schedule.</span></span>
<span data-ttu-id="a85cb-107">Этот объект передается команде, которая создает правило оповещения в журнале.</span><span class="sxs-lookup"><span data-stu-id="a85cb-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="a85cb-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a85cb-108">EXAMPLES</span></span>

### <span data-ttu-id="a85cb-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a85cb-109">Example 1</span></span>
```powershell
PS C:\>  $schedule = New-AzScheduledQueryRuleSchedule -FrequencyInMinutes 15 -TimeWindowInMinutes 15
```

## <span data-ttu-id="a85cb-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a85cb-110">PARAMETERS</span></span>

### <span data-ttu-id="a85cb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a85cb-111">-DefaultProfile</span></span>
<span data-ttu-id="a85cb-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a85cb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a85cb-113">-FrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="a85cb-113">-FrequencyInMinutes</span></span>
<span data-ttu-id="a85cb-114">Частота оповещений</span><span class="sxs-lookup"><span data-stu-id="a85cb-114">The alert frequency</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a85cb-115">-TimeWindowInMinutes</span><span class="sxs-lookup"><span data-stu-id="a85cb-115">-TimeWindowInMinutes</span></span>
<span data-ttu-id="a85cb-116">Окно "время оповещения"</span><span class="sxs-lookup"><span data-stu-id="a85cb-116">The alert time window</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a85cb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a85cb-117">CommonParameters</span></span>
<span data-ttu-id="a85cb-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a85cb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a85cb-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a85cb-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a85cb-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a85cb-120">INPUTS</span></span>

### <span data-ttu-id="a85cb-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="a85cb-121">None</span></span>

## <span data-ttu-id="a85cb-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a85cb-122">OUTPUTS</span></span>

### <span data-ttu-id="a85cb-123">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="a85cb-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="a85cb-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="a85cb-124">NOTES</span></span>

## <span data-ttu-id="a85cb-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a85cb-125">RELATED LINKS</span></span>
