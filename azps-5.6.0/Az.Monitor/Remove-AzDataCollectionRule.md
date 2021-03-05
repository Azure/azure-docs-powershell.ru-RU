---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRule.md
ms.openlocfilehash: 4dfa9417b2bce7473b3d2986f503c163cb6bf42f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974803"
---
# <span data-ttu-id="f5cad-101">Remove-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="f5cad-101">Remove-AzDataCollectionRule</span></span>

## <span data-ttu-id="f5cad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5cad-102">SYNOPSIS</span></span>
<span data-ttu-id="f5cad-103">Удаление правила сбора данных.</span><span class="sxs-lookup"><span data-stu-id="f5cad-103">Delete a data collection rule.</span></span>

## <span data-ttu-id="f5cad-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f5cad-104">SYNTAX</span></span>

### <span data-ttu-id="f5cad-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f5cad-105">ByName (Default)</span></span>
```
Remove-AzDataCollectionRule
   -ResourceGroupName <string> 
   -RuleName <string> 
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="f5cad-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f5cad-106">ByInputObject</span></span>
```
Remove-AzDataCollectionRule
   -InputObject <PSDataCollectionRuleResource>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="f5cad-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f5cad-107">ByResourceId</span></span>
```
Remove-AzDataCollectionRule
   -RuleId <string>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="f5cad-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5cad-108">DESCRIPTION</span></span>
<span data-ttu-id="f5cad-109">Чтобы удалить правило сбора данных, удалите правило сбора данных **Скайп-AzDataCollectionRule.**</span><span class="sxs-lookup"><span data-stu-id="f5cad-109">The **Remove-AzDataCollectionRule** cmdlet delete a data collection rule.</span></span>

<span data-ttu-id="f5cad-110">Правила сбора данных (DCR) определяют данные, которые в нее в нее вслали, и определяли, куда они должны быть отправлены или сохранены.</span><span class="sxs-lookup"><span data-stu-id="f5cad-110">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="f5cad-111">Вот полная статья [с обзором DCR.](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="f5cad-111">Here is the complete [DCR overview article](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

## <span data-ttu-id="f5cad-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f5cad-112">EXAMPLES</span></span>

### <span data-ttu-id="f5cad-113">Пример 1. Удаление правила сбора данных с параметрами имени и группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f5cad-113">Example 1: Delete data collection rule with name and resource group parameters</span></span>
```
PS C:\>Remove-AzDataCollectionRule -ResourceGroupName "testgroup" -RuleName "testDcr"             
```

### <span data-ttu-id="f5cad-114">Пример 2. Удаление правила сбора данных с названием и возвращаемой группой ресурсов</span><span class="sxs-lookup"><span data-stu-id="f5cad-114">Example 2: Delete data collection rule with name and resource group return bool</span></span>
```
PS C:\>Remove-AzDataCollectionRule -ResourceGroupName "testgroup" -RuleName "testDcr" -PassThru

True
```

### <span data-ttu-id="f5cad-115">Пример 3. Удаление правила сбора данных из InputObject</span><span class="sxs-lookup"><span data-stu-id="f5cad-115">Example 3: Delete data collection rule from InputObject</span></span>
```
PS C:\>Get-AzDataCollectionRule -ResourceGroupName "testdcr" -RuleName "dcrFromPipe95" | Remove-AzDataCollectionRule
```

### <span data-ttu-id="f5cad-116">Пример 4. Удаление правила сбора данных из ид ресурса</span><span class="sxs-lookup"><span data-stu-id="f5cad-116">Example 4: Delete data collection rule from resource id</span></span>
```
PS C:\>Remove-AzDataCollectionRule -RuleId "/subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/{dcrName}"
```

## <span data-ttu-id="f5cad-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5cad-117">PARAMETERS</span></span>

### <span data-ttu-id="f5cad-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5cad-118">-DefaultProfile</span></span>
<span data-ttu-id="f5cad-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f5cad-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5cad-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5cad-120">-ResourceGroupName</span></span>
<span data-ttu-id="f5cad-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f5cad-121">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5cad-122">-RuleName</span><span class="sxs-lookup"><span data-stu-id="f5cad-122">-RuleName</span></span>
<span data-ttu-id="f5cad-123">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="f5cad-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5cad-124">-RuleId</span><span class="sxs-lookup"><span data-stu-id="f5cad-124">-RuleId</span></span>
<span data-ttu-id="f5cad-125">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="f5cad-125">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5cad-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f5cad-126">-Confirm</span></span>
<span data-ttu-id="f5cad-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f5cad-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5cad-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5cad-128">-WhatIf</span></span>
<span data-ttu-id="f5cad-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5cad-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f5cad-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f5cad-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5cad-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5cad-131">CommonParameters</span></span>
<span data-ttu-id="f5cad-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5cad-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5cad-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5cad-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5cad-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f5cad-134">INPUTS</span></span>

### <span data-ttu-id="f5cad-135">System.String</span><span class="sxs-lookup"><span data-stu-id="f5cad-135">System.String</span></span>

## <span data-ttu-id="f5cad-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f5cad-136">OUTPUTS</span></span>

### <span data-ttu-id="f5cad-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="f5cad-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="f5cad-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f5cad-138">NOTES</span></span>

## <span data-ttu-id="f5cad-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5cad-139">RELATED LINKS</span></span>

<span data-ttu-id="f5cad-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md) 
 [Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="f5cad-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>