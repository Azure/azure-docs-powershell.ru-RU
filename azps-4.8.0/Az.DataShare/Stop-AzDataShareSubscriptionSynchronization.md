---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/stop-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: e865098b0c85227baf1f537fb22c40ee351902fd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243641"
---
# <span data-ttu-id="83692-101">Stop-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="83692-101">Stop-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="83692-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="83692-102">SYNOPSIS</span></span>
<span data-ttu-id="83692-103">Прекращение текущей синхронизации для подписки на общий доступ.</span><span class="sxs-lookup"><span data-stu-id="83692-103">Stops ongoing synchronization for a share subscription.</span></span> <span data-ttu-id="83692-104">Подписку на общий доступ можно указать с помощью ее идентификатора ресурса или имени.</span><span class="sxs-lookup"><span data-stu-id="83692-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="83692-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="83692-105">SYNTAX</span></span>

### <span data-ttu-id="83692-106">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="83692-106">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83692-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="83692-107">ByResourceIdParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -SynchronizationId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83692-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83692-108">ByObjectParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83692-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="83692-109">DESCRIPTION</span></span>
<span data-ttu-id="83692-110">Командлет **Stop-AzDataShareSubscriptionSynchronization** останавливает текущую синхронизацию для подписки на общий доступ</span><span class="sxs-lookup"><span data-stu-id="83692-110">The **Stop-AzDataShareSubscriptionSynchronization** cmdlet stops ongoing synchronization for a share subscription</span></span>

## <span data-ttu-id="83692-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="83692-111">EXAMPLES</span></span>

### <span data-ttu-id="83692-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="83692-112">Example 1</span></span>
```
PS C:\> Stop-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -SynchronizationId 20a4416b-b33b-4539-a908-71dc8ef698fb

Confirm
AdsShareSubscription
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

durationMs        : 231869
endTime           : 
message           :
startTime         : 7/9/2019 11:40:53 PM
status            : Canceled
synchronizationId : 20a4416b-b33b-4539-a908-71dc8ef698fb
```

<span data-ttu-id="83692-113">Останавливает текущую синхронизацию, идентифицированную по идентификатору-20a4416b-b33b-4539-a908-71dc8ef698fb</span><span class="sxs-lookup"><span data-stu-id="83692-113">Stops ongoing synchronization identified by id - 20a4416b-b33b-4539-a908-71dc8ef698fb</span></span>

## <span data-ttu-id="83692-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="83692-114">PARAMETERS</span></span>

### <span data-ttu-id="83692-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="83692-115">-AccountName</span></span>
<span data-ttu-id="83692-116">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="83692-116">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83692-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="83692-117">-AsJob</span></span>
<span data-ttu-id="83692-118">{{Fill AsJob описание}}</span><span class="sxs-lookup"><span data-stu-id="83692-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="83692-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83692-119">-DefaultProfile</span></span>
<span data-ttu-id="83692-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="83692-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83692-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83692-121">-InputObject</span></span>
<span data-ttu-id="83692-122">Объект подписки на общий доступ к данным Azure</span><span class="sxs-lookup"><span data-stu-id="83692-122">Azure data share subscription object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83692-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83692-123">-ResourceGroupName</span></span>
<span data-ttu-id="83692-124">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="83692-124">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83692-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83692-125">-ResourceId</span></span>
<span data-ttu-id="83692-126">Идентификатор ресурса для подписки на общий доступ Azure</span><span class="sxs-lookup"><span data-stu-id="83692-126">The resource id of the azure share subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83692-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="83692-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="83692-128">Имя подписки на общий доступ к данным Azure</span><span class="sxs-lookup"><span data-stu-id="83692-128">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83692-129">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="83692-129">-SynchronizationId</span></span>
<span data-ttu-id="83692-130">Идентификатор синхронизации, который необходимо остановить</span><span class="sxs-lookup"><span data-stu-id="83692-130">Synchronization id that needs to be stopped</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83692-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="83692-131">-Confirm</span></span>
<span data-ttu-id="83692-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="83692-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83692-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83692-133">-WhatIf</span></span>
<span data-ttu-id="83692-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="83692-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83692-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="83692-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83692-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83692-136">CommonParameters</span></span>
<span data-ttu-id="83692-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="83692-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83692-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83692-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83692-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="83692-139">INPUTS</span></span>

### <span data-ttu-id="83692-140">System. String</span><span class="sxs-lookup"><span data-stu-id="83692-140">System.String</span></span>

### <span data-ttu-id="83692-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="83692-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="83692-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="83692-142">OUTPUTS</span></span>

### <span data-ttu-id="83692-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="83692-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="83692-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="83692-144">NOTES</span></span>

## <span data-ttu-id="83692-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="83692-145">RELATED LINKS</span></span>
