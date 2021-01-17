---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
ms.openlocfilehash: e264dce6c99aaee7803881ab5eaa0ef529a53b48
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324354"
---
# <span data-ttu-id="9fed9-101">New-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="9fed9-101">New-AzDataShareTrigger</span></span>

## <span data-ttu-id="9fed9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fed9-102">SYNOPSIS</span></span>
<span data-ttu-id="9fed9-103">Создает триггер для совместной подписки.</span><span class="sxs-lookup"><span data-stu-id="9fed9-103">Creates a trigger for share subscription.</span></span>

## <span data-ttu-id="9fed9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9fed9-104">SYNTAX</span></span>

```
New-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fed9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9fed9-105">DESCRIPTION</span></span>
<span data-ttu-id="9fed9-106">С **его** учетной записью создается триггер для подписки на совместное использование для указанного интервала повторения и времени синхронизации в учетной записи azure data share.</span><span class="sxs-lookup"><span data-stu-id="9fed9-106">The **New-AzDataShareTrigger** cmdlet creates a trigger for share subscription for the specified recurrence interval and synchronization time under azure data share account.</span></span>

## <span data-ttu-id="9fed9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9fed9-107">EXAMPLES</span></span>

### <span data-ttu-id="9fed9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9fed9-108">Example 1</span></span>
```
PS C:\> New-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger" -RecurrenceInterval "Day" -SynchronizationTime "9:00"
CreatedAt           : 7/10/2019 12:16:34 AM
CreatedBy           : Ads test
ProvisioningState   : Succeeded
RecurrenceInterval  : Day
SynchronizationMode : Incremental
SynchronizationTime : 7/9/2019 9:00:00 AM
TriggerStatus       : Active
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/triggers/AdsTrigger
Name                : AdsTrigger
Type                : Microsoft.DataShare/Triggers
```

<span data-ttu-id="9fed9-109">Эта команда создает новый триггер AdsTrigger для обмена подпиской AdsShareSubscription с интервалом ежедневного повторения в 9:00.</span><span class="sxs-lookup"><span data-stu-id="9fed9-109">This command creates a new trigger AdsTrigger for share subscription AdsShareSubscription with a daily recurrence interval of 9 am.</span></span>

## <span data-ttu-id="9fed9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9fed9-110">PARAMETERS</span></span>

### <span data-ttu-id="9fed9-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9fed9-111">-AccountName</span></span>
<span data-ttu-id="9fed9-112">Имя учетной записи для обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="9fed9-112">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fed9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9fed9-113">-AsJob</span></span>
<span data-ttu-id="9fed9-114">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="9fed9-114">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="9fed9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fed9-115">-DefaultProfile</span></span>
<span data-ttu-id="9fed9-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9fed9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fed9-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9fed9-117">-Name</span></span>
<span data-ttu-id="9fed9-118">Имя триггера передачи данных Azure</span><span class="sxs-lookup"><span data-stu-id="9fed9-118">Azure data share trigger name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fed9-119">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="9fed9-119">-RecurrenceInterval</span></span>
<span data-ttu-id="9fed9-120">Интервал повторения триггера (день или час)</span><span class="sxs-lookup"><span data-stu-id="9fed9-120">The recurrence interval for the trigger (Day or Hour)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fed9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fed9-121">-ResourceGroupName</span></span>
<span data-ttu-id="9fed9-122">Имя группы ресурсов учетной записи azure data share</span><span class="sxs-lookup"><span data-stu-id="9fed9-122">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fed9-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="9fed9-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="9fed9-124">Имя подписки на службу обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="9fed9-124">Azure data share subscription name</span></span>

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

### <span data-ttu-id="9fed9-125">-SynchronizationTime</span><span class="sxs-lookup"><span data-stu-id="9fed9-125">-SynchronizationTime</span></span>
<span data-ttu-id="9fed9-126">Время начала запланированной синхронизации для триггера</span><span class="sxs-lookup"><span data-stu-id="9fed9-126">The start time of the scheduled synchronization for the trigger</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fed9-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9fed9-127">-Confirm</span></span>
<span data-ttu-id="9fed9-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9fed9-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fed9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fed9-129">-WhatIf</span></span>
<span data-ttu-id="9fed9-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fed9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fed9-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9fed9-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fed9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fed9-132">CommonParameters</span></span>
<span data-ttu-id="9fed9-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fed9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fed9-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9fed9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fed9-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9fed9-135">INPUTS</span></span>

### <span data-ttu-id="9fed9-136">Нет</span><span class="sxs-lookup"><span data-stu-id="9fed9-136">None</span></span>

## <span data-ttu-id="9fed9-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9fed9-137">OUTPUTS</span></span>

### <span data-ttu-id="9fed9-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="9fed9-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="9fed9-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9fed9-139">NOTES</span></span>

## <span data-ttu-id="9fed9-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9fed9-140">RELATED LINKS</span></span>
