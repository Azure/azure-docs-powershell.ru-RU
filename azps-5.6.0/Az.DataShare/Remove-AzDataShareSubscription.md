---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
ms.openlocfilehash: 4cb023fecb020e37535f47823df6f02ee9f5050e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007960"
---
# <span data-ttu-id="3bf64-101">Remove-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="3bf64-101">Remove-AzDataShareSubscription</span></span>

## <span data-ttu-id="3bf64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bf64-102">SYNOPSIS</span></span>
<span data-ttu-id="3bf64-103">удаляет подписку на совместное использования</span><span class="sxs-lookup"><span data-stu-id="3bf64-103">removes a share subscription</span></span>

## <span data-ttu-id="3bf64-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3bf64-104">SYNTAX</span></span>

### <span data-ttu-id="3bf64-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3bf64-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bf64-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bf64-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSubscription -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bf64-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bf64-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSubscription -InputObject <PSDataShareSubscription> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bf64-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3bf64-108">DESCRIPTION</span></span>
<span data-ttu-id="3bf64-109">Для удаления подписки на share удаляется из подписки **cmdlet Remove-AzDataShareSubscription**</span><span class="sxs-lookup"><span data-stu-id="3bf64-109">The **Remove-AzDataShareSubscription** cmdlet removes a share subscription</span></span>

## <span data-ttu-id="3bf64-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3bf64-110">EXAMPLES</span></span>

### <span data-ttu-id="3bf64-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3bf64-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"
Are you sure you want to remove sharesubscription "AdsShareSubscription"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="3bf64-112">Эти команды удаляют из вики-служб учетной записи вики-сайты ссылку AdsShareSubscription с именем AdsShareSubscription.</span><span class="sxs-lookup"><span data-stu-id="3bf64-112">This commands removes a sharesubscription named AdsShareSubscription from account WikiAds.</span></span> 

## <span data-ttu-id="3bf64-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3bf64-113">PARAMETERS</span></span>

### <span data-ttu-id="3bf64-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3bf64-114">-AccountName</span></span>
<span data-ttu-id="3bf64-115">Имя учетной записи для обмена данными Azure.</span><span class="sxs-lookup"><span data-stu-id="3bf64-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="3bf64-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3bf64-116">-AsJob</span></span>
<span data-ttu-id="3bf64-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="3bf64-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="3bf64-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bf64-118">-DefaultProfile</span></span>
<span data-ttu-id="3bf64-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3bf64-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bf64-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3bf64-120">-InputObject</span></span>
<span data-ttu-id="3bf64-121">Объект подписки на службу обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="3bf64-121">Azure data share subscription object</span></span>


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

### <span data-ttu-id="3bf64-122">-Name</span><span class="sxs-lookup"><span data-stu-id="3bf64-122">-Name</span></span>
<span data-ttu-id="3bf64-123">Имя подписки на службу обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="3bf64-123">Azure data share subscription name</span></span>

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

### <span data-ttu-id="3bf64-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3bf64-124">-PassThru</span></span>
<span data-ttu-id="3bf64-125">Возвращенный объект (если он указан).</span><span class="sxs-lookup"><span data-stu-id="3bf64-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="3bf64-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bf64-126">-ResourceGroupName</span></span>
<span data-ttu-id="3bf64-127">Имя группы ресурсов учетной записи azure data share</span><span class="sxs-lookup"><span data-stu-id="3bf64-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="3bf64-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3bf64-128">-ResourceId</span></span>
<span data-ttu-id="3bf64-129">ИД ресурса подписки на службу обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="3bf64-129">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="3bf64-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3bf64-130">-Confirm</span></span>
<span data-ttu-id="3bf64-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="3bf64-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bf64-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bf64-132">-WhatIf</span></span>
<span data-ttu-id="3bf64-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bf64-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bf64-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3bf64-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bf64-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bf64-135">CommonParameters</span></span>
<span data-ttu-id="3bf64-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bf64-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bf64-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3bf64-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bf64-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3bf64-138">INPUTS</span></span>

### <span data-ttu-id="3bf64-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3bf64-139">System.String</span></span>

### <span data-ttu-id="3bf64-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="3bf64-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="3bf64-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3bf64-141">OUTPUTS</span></span>

### <span data-ttu-id="3bf64-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3bf64-142">System.Boolean</span></span>

## <span data-ttu-id="3bf64-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3bf64-143">NOTES</span></span>

## <span data-ttu-id="3bf64-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3bf64-144">RELATED LINKS</span></span>
