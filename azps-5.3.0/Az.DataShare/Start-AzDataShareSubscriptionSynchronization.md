---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/start-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: bbbcab1e4355667681acf1cc09a51ec6d6174103
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420527"
---
# <span data-ttu-id="4ed99-101">Start-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="4ed99-101">Start-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="4ed99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ed99-102">SYNOPSIS</span></span>
<span data-ttu-id="4ed99-103">Инициирует синхронизацию для подписки на совместное использования.</span><span class="sxs-lookup"><span data-stu-id="4ed99-103">Initiates synchronization for a share subscription.</span></span> <span data-ttu-id="4ed99-104">Подписку на один ресурс можно укаментить с помощью ее ИД ресурса или имени.</span><span class="sxs-lookup"><span data-stu-id="4ed99-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="4ed99-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4ed99-105">SYNTAX</span></span>

### <span data-ttu-id="4ed99-106">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4ed99-106">ByFieldsParameterSet (Default)</span></span>
```
Start-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationMode <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ed99-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ed99-107">ByResourceIdParameterSet</span></span>
```
Start-AzDataShareSubscriptionSynchronization -SynchronizationMode <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ed99-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ed99-108">ByObjectParameterSet</span></span>
```
Start-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ed99-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ed99-109">DESCRIPTION</span></span>
<span data-ttu-id="4ed99-110">**Cmdlet Start-AzDataShareSubscriptionSynchronization** инициирует синхронизацию для подписки на доступ</span><span class="sxs-lookup"><span data-stu-id="4ed99-110">The **Start-AzDataShareSubscriptionSynchronization** cmdlet initiates synchronization for a share subscription</span></span>

## <span data-ttu-id="4ed99-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4ed99-111">EXAMPLES</span></span>

### <span data-ttu-id="4ed99-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4ed99-112">Example 1</span></span>
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

<span data-ttu-id="4ed99-113">Эти команды инициируют синхронизацию для публикации на сайте AdsShareSubscription в учетной записи WikiAds.</span><span class="sxs-lookup"><span data-stu-id="4ed99-113">This commands initiates synchronization for a sharesubscription named AdsShareSubscription in account WikiAds.</span></span> 

## <span data-ttu-id="4ed99-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ed99-114">PARAMETERS</span></span>

### <span data-ttu-id="4ed99-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4ed99-115">-AccountName</span></span>
<span data-ttu-id="4ed99-116">Имя учетной записи для обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="4ed99-116">Azure data share account name</span></span>

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

### <span data-ttu-id="4ed99-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ed99-117">-AsJob</span></span>
<span data-ttu-id="4ed99-118">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="4ed99-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="4ed99-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ed99-119">-DefaultProfile</span></span>
<span data-ttu-id="4ed99-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4ed99-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ed99-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ed99-121">-InputObject</span></span>
<span data-ttu-id="4ed99-122">Объект подписки на службу обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="4ed99-122">Azure data share subscription object</span></span>


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

### <span data-ttu-id="4ed99-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ed99-123">-ResourceGroupName</span></span>
<span data-ttu-id="4ed99-124">Имя группы ресурсов учетной записи azure data share</span><span class="sxs-lookup"><span data-stu-id="4ed99-124">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="4ed99-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ed99-125">-ResourceId</span></span>
<span data-ttu-id="4ed99-126">ИД ресурса подписки на azure share</span><span class="sxs-lookup"><span data-stu-id="4ed99-126">The resource id of the azure share subscription</span></span>

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

### <span data-ttu-id="4ed99-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="4ed99-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="4ed99-128">Имя подписки на службу обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="4ed99-128">Azure data share subscription name</span></span>

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

### <span data-ttu-id="4ed99-129">-SynchronizationMode</span><span class="sxs-lookup"><span data-stu-id="4ed99-129">-SynchronizationMode</span></span>
<span data-ttu-id="4ed99-130">Режим синхронизации (fullSync или добавоченный)</span><span class="sxs-lookup"><span data-stu-id="4ed99-130">Synchronization mode (FullSync or Incremental)</span></span>

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

### <span data-ttu-id="4ed99-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ed99-131">-Confirm</span></span>
<span data-ttu-id="4ed99-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ed99-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ed99-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ed99-133">-WhatIf</span></span>
<span data-ttu-id="4ed99-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ed99-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ed99-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4ed99-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ed99-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ed99-136">CommonParameters</span></span>
<span data-ttu-id="4ed99-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ed99-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ed99-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ed99-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ed99-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4ed99-139">INPUTS</span></span>

### <span data-ttu-id="4ed99-140">System.String</span><span class="sxs-lookup"><span data-stu-id="4ed99-140">System.String</span></span>

### <span data-ttu-id="4ed99-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="4ed99-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="4ed99-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4ed99-142">OUTPUTS</span></span>

### <span data-ttu-id="4ed99-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="4ed99-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="4ed99-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4ed99-144">NOTES</span></span>

## <span data-ttu-id="4ed99-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ed99-145">RELATED LINKS</span></span>
