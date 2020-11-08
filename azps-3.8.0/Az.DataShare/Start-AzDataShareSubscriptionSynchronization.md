---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/start-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: 5fdd59bd97d5d3e94dd413716e0838ca91ae1b7e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074418"
---
# <span data-ttu-id="907df-101">Start-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="907df-101">Start-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="907df-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="907df-102">SYNOPSIS</span></span>
<span data-ttu-id="907df-103">Инициирует синхронизацию для подписки на общий доступ.</span><span class="sxs-lookup"><span data-stu-id="907df-103">Initiates synchronization for a share subscription.</span></span> <span data-ttu-id="907df-104">Подписку на общий доступ можно указать с помощью ее идентификатора ресурса или имени.</span><span class="sxs-lookup"><span data-stu-id="907df-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="907df-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="907df-105">SYNTAX</span></span>

### <span data-ttu-id="907df-106">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="907df-106">ByFieldsParameterSet (Default)</span></span>
```
Start-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationMode <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="907df-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="907df-107">ByResourceIdParameterSet</span></span>
```
Start-AzDataShareSubscriptionSynchronization -SynchronizationMode <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="907df-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="907df-108">ByObjectParameterSet</span></span>
```
Start-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="907df-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="907df-109">DESCRIPTION</span></span>
<span data-ttu-id="907df-110">Командлет **Start-AzDataShareSubscriptionSynchronization** инициирует синхронизацию для подписки на общий доступ</span><span class="sxs-lookup"><span data-stu-id="907df-110">The **Start-AzDataShareSubscriptionSynchronization** cmdlet initiates synchronization for a share subscription</span></span>

## <span data-ttu-id="907df-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="907df-111">EXAMPLES</span></span>

### <span data-ttu-id="907df-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="907df-112">Example 1</span></span>
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

<span data-ttu-id="907df-113">Эта команда инициирует синхронизацию для sharesubscription с именем AdsShareSubscription в WikiAds учетной записи.</span><span class="sxs-lookup"><span data-stu-id="907df-113">This commands initiates synchronization for a sharesubscription named AdsShareSubscription in account WikiAds.</span></span> 

## <span data-ttu-id="907df-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="907df-114">PARAMETERS</span></span>

### <span data-ttu-id="907df-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="907df-115">-AccountName</span></span>
<span data-ttu-id="907df-116">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="907df-116">Azure data share account name</span></span>

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

### <span data-ttu-id="907df-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="907df-117">-AsJob</span></span>
<span data-ttu-id="907df-118">{{Fill AsJob описание}}</span><span class="sxs-lookup"><span data-stu-id="907df-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="907df-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="907df-119">-DefaultProfile</span></span>
<span data-ttu-id="907df-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="907df-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="907df-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="907df-121">-InputObject</span></span>
<span data-ttu-id="907df-122">Объект подписки на общий доступ к данным Azure</span><span class="sxs-lookup"><span data-stu-id="907df-122">Azure data share subscription object</span></span>


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

### <span data-ttu-id="907df-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="907df-123">-ResourceGroupName</span></span>
<span data-ttu-id="907df-124">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="907df-124">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="907df-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="907df-125">-ResourceId</span></span>
<span data-ttu-id="907df-126">Идентификатор ресурса для подписки на общий доступ Azure</span><span class="sxs-lookup"><span data-stu-id="907df-126">The resource id of the azure share subscription</span></span>

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

### <span data-ttu-id="907df-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="907df-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="907df-128">Имя подписки на общий доступ к данным Azure</span><span class="sxs-lookup"><span data-stu-id="907df-128">Azure data share subscription name</span></span>

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

### <span data-ttu-id="907df-129">-SynchronizationMode</span><span class="sxs-lookup"><span data-stu-id="907df-129">-SynchronizationMode</span></span>
<span data-ttu-id="907df-130">Режим синхронизации (FullSync или инкремент)</span><span class="sxs-lookup"><span data-stu-id="907df-130">Synchronization mode (FullSync or Incremental)</span></span>

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

### <span data-ttu-id="907df-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="907df-131">-Confirm</span></span>
<span data-ttu-id="907df-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="907df-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="907df-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="907df-133">-WhatIf</span></span>
<span data-ttu-id="907df-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="907df-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="907df-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="907df-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="907df-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="907df-136">CommonParameters</span></span>
<span data-ttu-id="907df-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="907df-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="907df-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="907df-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="907df-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="907df-139">INPUTS</span></span>

### <span data-ttu-id="907df-140">System. String</span><span class="sxs-lookup"><span data-stu-id="907df-140">System.String</span></span>

### <span data-ttu-id="907df-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="907df-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="907df-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="907df-142">OUTPUTS</span></span>

### <span data-ttu-id="907df-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="907df-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="907df-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="907df-144">NOTES</span></span>

## <span data-ttu-id="907df-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="907df-145">RELATED LINKS</span></span>
