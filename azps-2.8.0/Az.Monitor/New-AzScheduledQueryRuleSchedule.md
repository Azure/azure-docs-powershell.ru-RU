---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
ms.openlocfilehash: 2043a2cf31354c7fc14b1b03794dff6f82af67b8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903254"
---
# <span data-ttu-id="cec2a-101">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="cec2a-101">New-AzScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="cec2a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cec2a-102">SYNOPSIS</span></span>
<span data-ttu-id="cec2a-103">Создает объект типа "Расписание".</span><span class="sxs-lookup"><span data-stu-id="cec2a-103">Creates an object of type Schedule</span></span>

## <span data-ttu-id="cec2a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cec2a-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSchedule -FrequencyInMinutes <Int32> -TimeWindowInMinutes <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cec2a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cec2a-105">DESCRIPTION</span></span>
<span data-ttu-id="cec2a-106">Создает объект типа "Расписание".</span><span class="sxs-lookup"><span data-stu-id="cec2a-106">Creates an object of type Schedule.</span></span>
<span data-ttu-id="cec2a-107">Этот объект передается команде, которая создает правило оповещения в журнале.</span><span class="sxs-lookup"><span data-stu-id="cec2a-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="cec2a-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cec2a-108">EXAMPLES</span></span>

### <span data-ttu-id="cec2a-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cec2a-109">Example 1</span></span>
```powershell
PS C:\>  $schedule = New-AzScheduledQueryRuleSchedule -FrequencyInMinutes 15 -TimeWindowInMinutes 15
```

## <span data-ttu-id="cec2a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cec2a-110">PARAMETERS</span></span>

### <span data-ttu-id="cec2a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cec2a-111">-DefaultProfile</span></span>
<span data-ttu-id="cec2a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cec2a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cec2a-113">-FrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="cec2a-113">-FrequencyInMinutes</span></span>
<span data-ttu-id="cec2a-114">Частота оповещений</span><span class="sxs-lookup"><span data-stu-id="cec2a-114">The alert frequency</span></span>

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

### <span data-ttu-id="cec2a-115">-TimeWindowInMinutes</span><span class="sxs-lookup"><span data-stu-id="cec2a-115">-TimeWindowInMinutes</span></span>
<span data-ttu-id="cec2a-116">Окно "время оповещения"</span><span class="sxs-lookup"><span data-stu-id="cec2a-116">The alert time window</span></span>

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

### <span data-ttu-id="cec2a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cec2a-117">CommonParameters</span></span>
<span data-ttu-id="cec2a-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cec2a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cec2a-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cec2a-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cec2a-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cec2a-120">INPUTS</span></span>

### <span data-ttu-id="cec2a-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="cec2a-121">None</span></span>

## <span data-ttu-id="cec2a-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cec2a-122">OUTPUTS</span></span>

### <span data-ttu-id="cec2a-123">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="cec2a-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="cec2a-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="cec2a-124">NOTES</span></span>

## <span data-ttu-id="cec2a-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cec2a-125">RELATED LINKS</span></span>
