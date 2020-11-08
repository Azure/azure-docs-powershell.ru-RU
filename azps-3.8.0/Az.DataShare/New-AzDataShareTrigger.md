---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
ms.openlocfilehash: a0f8651bab30cf5a439b6e16110b34e7d256aa3a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066297"
---
# <span data-ttu-id="a9d6a-101">New-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="a9d6a-101">New-AzDataShareTrigger</span></span>

## <span data-ttu-id="a9d6a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a9d6a-102">SYNOPSIS</span></span>
<span data-ttu-id="a9d6a-103">Создание триггера для общего доступа к подписке.</span><span class="sxs-lookup"><span data-stu-id="a9d6a-103">Creates a trigger for share subscription.</span></span>

## <span data-ttu-id="a9d6a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a9d6a-104">SYNTAX</span></span>

```
New-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9d6a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9d6a-105">DESCRIPTION</span></span>
<span data-ttu-id="a9d6a-106">Командлет **New-AzDataShareTrigger** создает триггер для общего доступа к подписке для указанного интервала повторения и время синхронизации в учетной записи для общего доступа к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="a9d6a-106">The **New-AzDataShareTrigger** cmdlet creates a trigger for share subscription for the specified recurrence interval and synchronization time under azure data share account.</span></span>

## <span data-ttu-id="a9d6a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a9d6a-107">EXAMPLES</span></span>

### <span data-ttu-id="a9d6a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a9d6a-108">Example 1</span></span>
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

<span data-ttu-id="a9d6a-109">Эта команда создает новый триггер AdsTrigger для предоставления общего доступа к подписке AdsShareSubscription с ежедневной периодичностью повторения в 9 AM.</span><span class="sxs-lookup"><span data-stu-id="a9d6a-109">This command creates a new trigger AdsTrigger for share subscription AdsShareSubscription with a daily recurrence interval of 9 am.</span></span>

## <span data-ttu-id="a9d6a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a9d6a-110">PARAMETERS</span></span>

### <span data-ttu-id="a9d6a-111">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="a9d6a-111">-AccountName</span></span>
<span data-ttu-id="a9d6a-112">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="a9d6a-112">Azure data share account name</span></span>

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

### <span data-ttu-id="a9d6a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9d6a-113">-AsJob</span></span>
<span data-ttu-id="a9d6a-114">{{Fill AsJob описание}}</span><span class="sxs-lookup"><span data-stu-id="a9d6a-114">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="a9d6a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9d6a-115">-DefaultProfile</span></span>
<span data-ttu-id="a9d6a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a9d6a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9d6a-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a9d6a-117">-Name</span></span>
<span data-ttu-id="a9d6a-118">Имя триггера общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="a9d6a-118">Azure data share trigger name</span></span>

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

### <span data-ttu-id="a9d6a-119">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="a9d6a-119">-RecurrenceInterval</span></span>
<span data-ttu-id="a9d6a-120">Интервал повторения для триггера (день или час)</span><span class="sxs-lookup"><span data-stu-id="a9d6a-120">The recurrence interval for the trigger (Day or Hour)</span></span>

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

### <span data-ttu-id="a9d6a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9d6a-121">-ResourceGroupName</span></span>
<span data-ttu-id="a9d6a-122">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="a9d6a-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="a9d6a-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="a9d6a-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="a9d6a-124">Имя подписки на общий доступ к данным Azure</span><span class="sxs-lookup"><span data-stu-id="a9d6a-124">Azure data share subscription name</span></span>

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

### <span data-ttu-id="a9d6a-125">-SynchronizationTime</span><span class="sxs-lookup"><span data-stu-id="a9d6a-125">-SynchronizationTime</span></span>
<span data-ttu-id="a9d6a-126">Время начала запланированной синхронизации для триггера</span><span class="sxs-lookup"><span data-stu-id="a9d6a-126">The start time of the scheduled synchronization for the trigger</span></span>

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

### <span data-ttu-id="a9d6a-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a9d6a-127">-Confirm</span></span>
<span data-ttu-id="a9d6a-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a9d6a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9d6a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9d6a-129">-WhatIf</span></span>
<span data-ttu-id="a9d6a-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a9d6a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9d6a-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a9d6a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9d6a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9d6a-132">CommonParameters</span></span>
<span data-ttu-id="a9d6a-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a9d6a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9d6a-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9d6a-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9d6a-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a9d6a-135">INPUTS</span></span>

### <span data-ttu-id="a9d6a-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="a9d6a-136">None</span></span>

## <span data-ttu-id="a9d6a-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9d6a-137">OUTPUTS</span></span>

### <span data-ttu-id="a9d6a-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="a9d6a-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="a9d6a-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="a9d6a-139">NOTES</span></span>

## <span data-ttu-id="a9d6a-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a9d6a-140">RELATED LINKS</span></span>
