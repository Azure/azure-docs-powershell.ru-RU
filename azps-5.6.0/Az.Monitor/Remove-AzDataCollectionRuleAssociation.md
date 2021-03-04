---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azdatacollectionruleassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRuleAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRuleAssociation.md
ms.openlocfilehash: 87830eb9cb4321bf9af1476d3fa5a0db41796351
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987815"
---
# <span data-ttu-id="bf4ea-101">Remove-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="bf4ea-101">Remove-AzDataCollectionRuleAssociation</span></span>

## <span data-ttu-id="bf4ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf4ea-102">SYNOPSIS</span></span>
<span data-ttu-id="bf4ea-103">Удаление связи правил сбора данных.</span><span class="sxs-lookup"><span data-stu-id="bf4ea-103">Delete a data collection rule association.</span></span>

## <span data-ttu-id="bf4ea-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bf4ea-104">SYNTAX</span></span>

### <span data-ttu-id="bf4ea-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bf4ea-105">ByName (Default)</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -TargetResourceId <string> 
      -AssociationName <string> 
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="bf4ea-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bf4ea-106">ByInputObject</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -InputObject <PSDataCollectionRuleAssociationProxyOnlyResource>
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="bf4ea-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bf4ea-107">ByResourceId</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -AssociationId <string>
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

## <span data-ttu-id="bf4ea-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf4ea-108">DESCRIPTION</span></span>
<span data-ttu-id="bf4ea-109">С его учетом можно удалить связь правил сбора данных (DCRA) с его **cmdletRuleAssociation.**</span><span class="sxs-lookup"><span data-stu-id="bf4ea-109">The **Remove-AzDataCollectionRuleAssociation** cmdlet delete a data collection rule association (DCRA).</span></span>

<span data-ttu-id="bf4ea-110">Чтобы применить DCR к виртуальной машине, необходимо создать связь для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bf4ea-110">To apply a DCR to a virtual machine, you create an association for the virtual machine.</span></span> <span data-ttu-id="bf4ea-111">Виртуальная машина может иметь связь с несколькими DCR, а DCR может иметь несколько виртуальных машин, связанных с ней.</span><span class="sxs-lookup"><span data-stu-id="bf4ea-111">A virtual machine may have an association to multiple DCRs, and a DCR may have multiple virtual machines associated to it.</span></span> <span data-ttu-id="bf4ea-112">Это позволяет определить набор dcrs, каждый из которых соответствует определенному требованию, и применить их только к виртуальным машинам, на которых они применяются.</span><span class="sxs-lookup"><span data-stu-id="bf4ea-112">This allows you to define a set of DCRs, each matching a particular requirement, and apply them to only the virtual machines where they apply.</span></span> <span data-ttu-id="bf4ea-113">Ниже приводится статья "Настройка сбора данных для агента [Azure Monitor"](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) с помощью DCRA.</span><span class="sxs-lookup"><span data-stu-id="bf4ea-113">Here is the ["Configure data collection for the Azure Monitor agent"](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) using DCRA article.</span></span>

## <span data-ttu-id="bf4ea-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bf4ea-114">EXAMPLES</span></span>

### <span data-ttu-id="bf4ea-115">Пример 1. Удаление связи правил сбора данных с параметрами имени и ИД целевого ресурса (связанной виртуальной машины)</span><span class="sxs-lookup"><span data-stu-id="bf4ea-115">Example 1: Delete data collection rule association with name and target resource ID (associated virtual machine) parameters</span></span>
```
PS C:\>Remove-AzDataCollectionRuleAssociation -TargetResourceId $vm.Id -AssociationName $assocName
```

### <span data-ttu-id="bf4ea-116">Пример 2. Удаление правила сбора данных с помощью объекта Input Object</span><span class="sxs-lookup"><span data-stu-id="bf4ea-116">Example 2: Delete data collection rule with Input Object</span></span>
```
PS C:\>$dcrAssoc | Remove-AzDataCollectionRule
```

### <span data-ttu-id="bf4ea-117">Пример 3. Удаление правила сбора данных со свойством "ИД ресурса связи"</span><span class="sxs-lookup"><span data-stu-id="bf4ea-117">Example 3: Delete data collection rule with the association resource ID property</span></span>
```
PS C:\>Remove-AzDataCollectionRule -AssociationId $dcrAssoc.Id
```

## <span data-ttu-id="bf4ea-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf4ea-118">PARAMETERS</span></span>

### <span data-ttu-id="bf4ea-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf4ea-119">-DefaultProfile</span></span>
<span data-ttu-id="bf4ea-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bf4ea-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf4ea-121">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="bf4ea-121">-TargetResourceId</span></span>
<span data-ttu-id="bf4ea-122">Связанный ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="bf4ea-122">The associated resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf4ea-123">-AssociationName</span><span class="sxs-lookup"><span data-stu-id="bf4ea-123">-AssociationName</span></span>
<span data-ttu-id="bf4ea-124">Имя ресурса связи.</span><span class="sxs-lookup"><span data-stu-id="bf4ea-124">The name of the association resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName (Default)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf4ea-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf4ea-125">-InputObject</span></span>
<span data-ttu-id="bf4ea-126">Объект PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="bf4ea-126">PSDataCollectionRuleResource Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="bf4ea-127">-AssociationId</span><span class="sxs-lookup"><span data-stu-id="bf4ea-127">-AssociationId</span></span>
<span data-ttu-id="bf4ea-128">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="bf4ea-128">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf4ea-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bf4ea-129">-Confirm</span></span>
<span data-ttu-id="bf4ea-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf4ea-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf4ea-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf4ea-131">-WhatIf</span></span>
<span data-ttu-id="bf4ea-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf4ea-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bf4ea-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bf4ea-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf4ea-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf4ea-134">CommonParameters</span></span>
<span data-ttu-id="bf4ea-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf4ea-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf4ea-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf4ea-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf4ea-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bf4ea-137">INPUTS</span></span>

### <span data-ttu-id="bf4ea-138">System.String</span><span class="sxs-lookup"><span data-stu-id="bf4ea-138">System.String</span></span>
###<span data-ttu-id="bf4ea-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span><span class="sxs-lookup"><span data-stu-id="bf4ea-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span></span>

## <span data-ttu-id="bf4ea-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bf4ea-140">OUTPUTS</span></span>

### <span data-ttu-id="bf4ea-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bf4ea-141">System.Boolean</span></span>

## <span data-ttu-id="bf4ea-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bf4ea-142">NOTES</span></span>

## <span data-ttu-id="bf4ea-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bf4ea-143">RELATED LINKS</span></span>

<span data-ttu-id="bf4ea-144">[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [New-AzDataCollectionRule](./New-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="bf4ea-144">[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)</span></span>
