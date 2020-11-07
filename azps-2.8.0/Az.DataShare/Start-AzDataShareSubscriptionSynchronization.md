---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/start-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: 2f0b5cd19e0f21a416c9fd5f3a32462eea86cc4a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721149"
---
# <span data-ttu-id="b6354-101">Start-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="b6354-101">Start-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="b6354-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b6354-102">SYNOPSIS</span></span>
<span data-ttu-id="b6354-103">Инициирует синхронизацию для подписки на общий доступ.</span><span class="sxs-lookup"><span data-stu-id="b6354-103">Initiates synchronization for a share subscription.</span></span> <span data-ttu-id="b6354-104">Подписку на общий доступ можно указать с помощью ее идентификатора ресурса или имени.</span><span class="sxs-lookup"><span data-stu-id="b6354-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="b6354-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b6354-105">SYNTAX</span></span>

### <span data-ttu-id="b6354-106">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b6354-106">ByFieldsParameterSet (Default)</span></span>
```
Start-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationMode <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6354-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6354-107">ByResourceIdParameterSet</span></span>
```
Start-AzDataShareSubscriptionSynchronization -SynchronizationMode <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6354-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6354-108">ByObjectParameterSet</span></span>
```
Start-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6354-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6354-109">DESCRIPTION</span></span>
<span data-ttu-id="b6354-110">Командлет **Start-AzDataShareSubscriptionSynchronization** инициирует синхронизацию для подписки на общий доступ</span><span class="sxs-lookup"><span data-stu-id="b6354-110">The **Start-AzDataShareSubscriptionSynchronization** cmdlet initiates synchronization for a share subscription</span></span>

## <span data-ttu-id="b6354-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b6354-111">EXAMPLES</span></span>

### <span data-ttu-id="b6354-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b6354-112">Example 1</span></span>
```
PS C:\> Start-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -SynchronizationMode Incremental

Confirm
AdsShareSubscription
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

durationMs        : 231869
endTime           : 7/9/2019 11:44:41 PM
message           :
startTime         : 7/9/2019 11:40:53 PM
status            : Succeeded
synchronizationId : 20a4416b-b33b-4539-a908-71dc8ef698fb
```

<span data-ttu-id="b6354-113">Эта команда инициирует синхронизацию для sharesubscription с именем AdsShareSubscription в WikiAds учетной записи.</span><span class="sxs-lookup"><span data-stu-id="b6354-113">This commands initiates synchronization for a sharesubscription named AdsShareSubscription in account WikiAds.</span></span> 

## <span data-ttu-id="b6354-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b6354-114">PARAMETERS</span></span>

### <span data-ttu-id="b6354-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="b6354-115">-AccountName</span></span>
<span data-ttu-id="b6354-116">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="b6354-116">Azure data share account name</span></span>

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

### <span data-ttu-id="b6354-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6354-117">-AsJob</span></span>
<span data-ttu-id="b6354-118">{{Fill AsJob описание}}</span><span class="sxs-lookup"><span data-stu-id="b6354-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="b6354-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6354-119">-DefaultProfile</span></span>
<span data-ttu-id="b6354-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b6354-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6354-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6354-121">-InputObject</span></span>
<span data-ttu-id="b6354-122">Объект подписки на общий доступ к данным Azure</span><span class="sxs-lookup"><span data-stu-id="b6354-122">Azure data share subscription object</span></span>


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

### <span data-ttu-id="b6354-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6354-123">-ResourceGroupName</span></span>
<span data-ttu-id="b6354-124">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="b6354-124">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="b6354-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6354-125">-ResourceId</span></span>
<span data-ttu-id="b6354-126">Идентификатор ресурса для подписки на общий доступ Azure</span><span class="sxs-lookup"><span data-stu-id="b6354-126">The resource id of the azure share subscription</span></span>

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

### <span data-ttu-id="b6354-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="b6354-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="b6354-128">Имя подписки на общий доступ к данным Azure</span><span class="sxs-lookup"><span data-stu-id="b6354-128">Azure data share subscription name</span></span>

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

### <span data-ttu-id="b6354-129">-SynchronizationMode</span><span class="sxs-lookup"><span data-stu-id="b6354-129">-SynchronizationMode</span></span>
<span data-ttu-id="b6354-130">Режим синхронизации (FullSync или инкремент)</span><span class="sxs-lookup"><span data-stu-id="b6354-130">Synchronization mode (FullSync or Incremental)</span></span>

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

### <span data-ttu-id="b6354-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6354-131">-Confirm</span></span>
<span data-ttu-id="b6354-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b6354-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6354-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6354-133">-WhatIf</span></span>
<span data-ttu-id="b6354-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b6354-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6354-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b6354-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6354-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6354-136">CommonParameters</span></span>
<span data-ttu-id="b6354-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b6354-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6354-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6354-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6354-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b6354-139">INPUTS</span></span>

### <span data-ttu-id="b6354-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b6354-140">System.String</span></span>

### <span data-ttu-id="b6354-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="b6354-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="b6354-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6354-142">OUTPUTS</span></span>

### <span data-ttu-id="b6354-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="b6354-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="b6354-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="b6354-144">NOTES</span></span>

## <span data-ttu-id="b6354-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6354-145">RELATED LINKS</span></span>
