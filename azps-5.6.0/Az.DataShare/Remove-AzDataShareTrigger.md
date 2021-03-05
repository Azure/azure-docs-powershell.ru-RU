---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
ms.openlocfilehash: 9ee4c8c25f6a9575283c8e5f077be7107756f701
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966531"
---
# <span data-ttu-id="b868a-101">Remove-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="b868a-101">Remove-AzDataShareTrigger</span></span>

## <span data-ttu-id="b868a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b868a-102">SYNOPSIS</span></span>
<span data-ttu-id="b868a-103">Удаление триггера</span><span class="sxs-lookup"><span data-stu-id="b868a-103">removes a trigger</span></span>

## <span data-ttu-id="b868a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b868a-104">SYNTAX</span></span>

### <span data-ttu-id="b868a-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b868a-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b868a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b868a-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareTrigger -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b868a-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b868a-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareTrigger -InputObject <PSDataShareTrigger> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b868a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b868a-108">DESCRIPTION</span></span>
<span data-ttu-id="b868a-109">Для **удаления триггера datasharetrilet Remove-AzDataShareTrigger** удаляется триггер datashare.</span><span class="sxs-lookup"><span data-stu-id="b868a-109">The **Remove-AzDataShareTrigger** cmdlet removes a datashare trigger</span></span>

## <span data-ttu-id="b868a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b868a-110">EXAMPLES</span></span>

### <span data-ttu-id="b868a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b868a-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger"

Are you sure you want to remove trigger "AdsTrigger"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="b868a-112">Эти команды удаляют триггер AdsTrigger из share subscription AdsShareSubscription.</span><span class="sxs-lookup"><span data-stu-id="b868a-112">This commands removes a trigger named AdsTrigger from share subscription AdsShareSubscription.</span></span> 

## <span data-ttu-id="b868a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b868a-113">PARAMETERS</span></span>

### <span data-ttu-id="b868a-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b868a-114">-AccountName</span></span>
<span data-ttu-id="b868a-115">Имя учетной записи для обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="b868a-115">Azure data share account name</span></span>

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

### <span data-ttu-id="b868a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b868a-116">-AsJob</span></span>
<span data-ttu-id="b868a-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="b868a-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="b868a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b868a-118">-DefaultProfile</span></span>
<span data-ttu-id="b868a-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b868a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b868a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b868a-120">-InputObject</span></span>
<span data-ttu-id="b868a-121">Объект триггера передачи данных Azure</span><span class="sxs-lookup"><span data-stu-id="b868a-121">Azure data share trigger object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b868a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b868a-122">-Name</span></span>
<span data-ttu-id="b868a-123">Имя триггера передачи данных Azure</span><span class="sxs-lookup"><span data-stu-id="b868a-123">Azure data share trigger name</span></span>

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

### <span data-ttu-id="b868a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b868a-124">-PassThru</span></span>
<span data-ttu-id="b868a-125">Возвращенный объект (если он указан).</span><span class="sxs-lookup"><span data-stu-id="b868a-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="b868a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b868a-126">-ResourceGroupName</span></span>
<span data-ttu-id="b868a-127">Имя группы ресурсов учетной записи azure data share</span><span class="sxs-lookup"><span data-stu-id="b868a-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="b868a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b868a-128">-ResourceId</span></span>
<span data-ttu-id="b868a-129">ИД ресурса триггера обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="b868a-129">The resource id of azure data share trigger</span></span>

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

### <span data-ttu-id="b868a-130">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="b868a-130">-ShareSubscriptionName</span></span>
<span data-ttu-id="b868a-131">Имя подписки на службу обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="b868a-131">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b868a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b868a-132">-Confirm</span></span>
<span data-ttu-id="b868a-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b868a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b868a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b868a-134">-WhatIf</span></span>
<span data-ttu-id="b868a-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b868a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b868a-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b868a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b868a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b868a-137">CommonParameters</span></span>
<span data-ttu-id="b868a-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b868a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b868a-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b868a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b868a-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b868a-140">INPUTS</span></span>

### <span data-ttu-id="b868a-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b868a-141">System.String</span></span>

### <span data-ttu-id="b868a-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="b868a-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="b868a-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b868a-143">OUTPUTS</span></span>

### <span data-ttu-id="b868a-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b868a-144">System.Boolean</span></span>

## <span data-ttu-id="b868a-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b868a-145">NOTES</span></span>

## <span data-ttu-id="b868a-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b868a-146">RELATED LINKS</span></span>
