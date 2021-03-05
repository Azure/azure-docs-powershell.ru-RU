---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azscheduledqueryruleschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
ms.openlocfilehash: 231b9250509ed463f7f9b2a2d9563dbb1e378ee0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978419"
---
# <span data-ttu-id="54c65-101">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="54c65-101">New-AzScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="54c65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54c65-102">SYNOPSIS</span></span>
<span data-ttu-id="54c65-103">Создание объекта типа "Расписание"</span><span class="sxs-lookup"><span data-stu-id="54c65-103">Creates an object of type Schedule</span></span>

## <span data-ttu-id="54c65-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="54c65-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSchedule -FrequencyInMinutes <Int32> -TimeWindowInMinutes <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54c65-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54c65-105">DESCRIPTION</span></span>
<span data-ttu-id="54c65-106">Создает объект типа "Расписание".</span><span class="sxs-lookup"><span data-stu-id="54c65-106">Creates an object of type Schedule.</span></span>
<span data-ttu-id="54c65-107">Этот объект передается команде, которая создает правило оповещения журнала.</span><span class="sxs-lookup"><span data-stu-id="54c65-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="54c65-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="54c65-108">EXAMPLES</span></span>

### <span data-ttu-id="54c65-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="54c65-109">Example 1</span></span>
```powershell
PS C:\>  $schedule = New-AzScheduledQueryRuleSchedule -FrequencyInMinutes 15 -TimeWindowInMinutes 15
```

## <span data-ttu-id="54c65-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54c65-110">PARAMETERS</span></span>

### <span data-ttu-id="54c65-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54c65-111">-DefaultProfile</span></span>
<span data-ttu-id="54c65-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="54c65-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54c65-113">-FrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="54c65-113">-FrequencyInMinutes</span></span>
<span data-ttu-id="54c65-114">Частота оповещения</span><span class="sxs-lookup"><span data-stu-id="54c65-114">The alert frequency</span></span>

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

### <span data-ttu-id="54c65-115">-TimeWindowInMinutes</span><span class="sxs-lookup"><span data-stu-id="54c65-115">-TimeWindowInMinutes</span></span>
<span data-ttu-id="54c65-116">Окно времени оповещения</span><span class="sxs-lookup"><span data-stu-id="54c65-116">The alert time window</span></span>

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

### <span data-ttu-id="54c65-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54c65-117">CommonParameters</span></span>
<span data-ttu-id="54c65-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54c65-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54c65-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54c65-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54c65-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="54c65-120">INPUTS</span></span>

### <span data-ttu-id="54c65-121">Нет</span><span class="sxs-lookup"><span data-stu-id="54c65-121">None</span></span>

## <span data-ttu-id="54c65-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="54c65-122">OUTPUTS</span></span>

### <span data-ttu-id="54c65-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="54c65-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="54c65-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="54c65-124">NOTES</span></span>

## <span data-ttu-id="54c65-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54c65-125">RELATED LINKS</span></span>
