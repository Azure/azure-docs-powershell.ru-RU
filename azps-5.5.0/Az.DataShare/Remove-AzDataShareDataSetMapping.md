---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
ms.openlocfilehash: 16b212a0c5549f74b56e8c80be8d949a025ecb24
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232113"
---
# <span data-ttu-id="2d3af-101">Remove-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="2d3af-101">Remove-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="2d3af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d3af-102">SYNOPSIS</span></span>
<span data-ttu-id="2d3af-103">Удаление сопоставления для наборов данных</span><span class="sxs-lookup"><span data-stu-id="2d3af-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="2d3af-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2d3af-104">SYNTAX</span></span>

### <span data-ttu-id="2d3af-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2d3af-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d3af-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d3af-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d3af-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d3af-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -InputObject <PSDataShareDataSetMapping> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d3af-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d3af-108">DESCRIPTION</span></span>
<span data-ttu-id="2d3af-109">Для **удаления сопоставлений наборов данных удаляется cmdlet Remove-AzDataShareDataSetMapping.**</span><span class="sxs-lookup"><span data-stu-id="2d3af-109">The **Remove-AzDataShareDataSetMapping** cmdlet removes a dataset mappings.</span></span>

## <span data-ttu-id="2d3af-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2d3af-110">EXAMPLES</span></span>

### <span data-ttu-id="2d3af-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2d3af-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "DSM"
Are you sure you want to remove dataset mapping "DSM"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="2d3af-112">Эти команды удаляют набор данных DSM из вики-страниц sharesubscription.</span><span class="sxs-lookup"><span data-stu-id="2d3af-112">This commands removes the dataset named DSM from sharesubscription WikiAds.</span></span> 

## <span data-ttu-id="2d3af-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d3af-113">PARAMETERS</span></span>

### <span data-ttu-id="2d3af-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2d3af-114">-AccountName</span></span>
<span data-ttu-id="2d3af-115">Имя учетной записи для обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="2d3af-115">Azure data share account name</span></span>

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

### <span data-ttu-id="2d3af-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d3af-116">-DefaultProfile</span></span>
<span data-ttu-id="2d3af-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2d3af-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d3af-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d3af-118">-InputObject</span></span>
<span data-ttu-id="2d3af-119">Объект сопоставления набора данных Azure</span><span class="sxs-lookup"><span data-stu-id="2d3af-119">The azure data set mapping object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d3af-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2d3af-120">-Name</span></span>
<span data-ttu-id="2d3af-121">Имя сопоставления набора данных Azure</span><span class="sxs-lookup"><span data-stu-id="2d3af-121">Azure data set mapping name</span></span>

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

### <span data-ttu-id="2d3af-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d3af-122">-PassThru</span></span>
<span data-ttu-id="2d3af-123">Возвращенный объект (если он указан).</span><span class="sxs-lookup"><span data-stu-id="2d3af-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="2d3af-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d3af-124">-ResourceGroupName</span></span>
<span data-ttu-id="2d3af-125">Имя группы ресурсов учетной записи azure data share</span><span class="sxs-lookup"><span data-stu-id="2d3af-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="2d3af-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d3af-126">-ResourceId</span></span>
<span data-ttu-id="2d3af-127">ИД ресурса сопоставления набора данных Azure</span><span class="sxs-lookup"><span data-stu-id="2d3af-127">The resource id of the azure data set mapping</span></span>

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

### <span data-ttu-id="2d3af-128">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="2d3af-128">-ShareSubscriptionName</span></span>
<span data-ttu-id="2d3af-129">Имя подписки на службу обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="2d3af-129">Azure data share subscription name</span></span>

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

### <span data-ttu-id="2d3af-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d3af-130">-Confirm</span></span>
<span data-ttu-id="2d3af-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="2d3af-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d3af-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d3af-132">-WhatIf</span></span>
<span data-ttu-id="2d3af-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d3af-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d3af-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2d3af-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d3af-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d3af-135">CommonParameters</span></span>
<span data-ttu-id="2d3af-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d3af-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d3af-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d3af-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d3af-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2d3af-138">INPUTS</span></span>

### <span data-ttu-id="2d3af-139">System.String</span><span class="sxs-lookup"><span data-stu-id="2d3af-139">System.String</span></span>

### <span data-ttu-id="2d3af-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="2d3af-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="2d3af-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2d3af-141">OUTPUTS</span></span>

### <span data-ttu-id="2d3af-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2d3af-142">System.Boolean</span></span>

## <span data-ttu-id="2d3af-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2d3af-143">NOTES</span></span>

## <span data-ttu-id="2d3af-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d3af-144">RELATED LINKS</span></span>
