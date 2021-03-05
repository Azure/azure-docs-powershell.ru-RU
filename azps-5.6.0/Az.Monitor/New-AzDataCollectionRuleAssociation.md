---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azdatacollectionruleassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRuleAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRuleAssociation.md
ms.openlocfilehash: 1086f67bcec4adeef74fe7bf591e61d9d08a90e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984556"
---
# <span data-ttu-id="251a0-101">New-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="251a0-101">New-AzDataCollectionRuleAssociation</span></span>

## <span data-ttu-id="251a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="251a0-102">SYNOPSIS</span></span>
<span data-ttu-id="251a0-103">Создание связи правил сбора данных.</span><span class="sxs-lookup"><span data-stu-id="251a0-103">Create data collection rule association.</span></span>

## <span data-ttu-id="251a0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="251a0-104">SYNTAX</span></span>

### <span data-ttu-id="251a0-105">ByDataCollectionRuleId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="251a0-105">ByDataCollectionRuleId (Default)</span></span>
```
New-AzDataCollectionRuleAssociation
   -TargetResourceId <string>
   -AssociationName <string>
   -RuleId <string>
   [-Description <string>]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="251a0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="251a0-106">ByInputObject</span></span>
```
New-AzDataCollectionRuleAssociation
   -TargetResourceId <string>
   -AssociationName <string>
   -InputObject <PSDataCollectionRuleResource>
   [-Description <string>]
   [-DefaultProfile <IAzureContextContainer>]  
   [-WhatIf]   
   [-Confirm]   
   [<CommonParameters>]
```


## <span data-ttu-id="251a0-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="251a0-107">DESCRIPTION</span></span>
<span data-ttu-id="251a0-108">Для создания связи правил сбора данных (DCRA) будет создаваться **cmdletRuleAssociation New-AzDataCollectionRuleAssociation.**</span><span class="sxs-lookup"><span data-stu-id="251a0-108">The **New-AzDataCollectionRuleAssociation** cmdlet creates a data collection rules association (DCRA).</span></span>

<span data-ttu-id="251a0-109">Чтобы применить DCR к виртуальной машине, необходимо создать связь для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="251a0-109">To apply a DCR to a virtual machine, you create an association for the virtual machine.</span></span> <span data-ttu-id="251a0-110">Виртуальная машина может иметь связь с несколькими DCR, а DCR может иметь несколько виртуальных машин, связанных с ней.</span><span class="sxs-lookup"><span data-stu-id="251a0-110">A virtual machine may have an association to multiple DCRs, and a DCR may have multiple virtual machines associated to it.</span></span> <span data-ttu-id="251a0-111">Это позволяет определить набор dcrs, каждый из которых соответствует определенному требованию, и применить их только к виртуальным машинам, на которых они применяются.</span><span class="sxs-lookup"><span data-stu-id="251a0-111">This allows you to define a set of DCRs, each matching a particular requirement, and apply them to only the virtual machines where they apply.</span></span> <span data-ttu-id="251a0-112">Ниже приводится статья "Настройка сбора данных для агента [Azure Monitor"](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) с помощью DCRA.</span><span class="sxs-lookup"><span data-stu-id="251a0-112">Here is the ["Configure data collection for the Azure Monitor agent"](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) using DCRA article.</span></span>

## <span data-ttu-id="251a0-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="251a0-113">EXAMPLES</span></span>

### <span data-ttu-id="251a0-114">Пример 1. Создание связи правил сбора данных</span><span class="sxs-lookup"><span data-stu-id="251a0-114">Example 1: Create data collection rule association</span></span>
```
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName $rg -RuleName $dcrName
PS C:\>$vmId = '/subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Compute/virtualMachines/{vmName}'
PS C:\>New-AzDataCollectionRuleAssociation -TargetResourceId $vmId -AssociationName "dcrAssoc" -RuleId $dcr.Id

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Insights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Compute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/dcrAssoc
Name                 : dcrAssoc
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="251a0-115">Эта команда создает связь правила сбора данных для заданного правила и ИД целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="251a0-115">This command creates a data collection rule association for given rule and target resource ID.</span></span>

### <span data-ttu-id="251a0-116">Пример 2. Создание связи правил сбора данных из объекта DCR</span><span class="sxs-lookup"><span data-stu-id="251a0-116">Example 2: Create data collection rule association from a DCR object</span></span>
```
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName $rg -RuleName $dcrName
PS C:\>$vmId = '/subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Compute/virtualMachines/{vmName}'
PS C:\>$dcr | New-AzDataCollectionRuleAssociation -TargetResourceId $vmId -AssociationName "dcrAssocInput"

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Insights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Compute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/dcrAssocInput
Name                 : dcrAssocInput
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="251a0-117">Эта команда создает связь правила сбора данных для заданного правила и ИД целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="251a0-117">This command creates a data collection rule association for given rule and target resource ID.</span></span>

## <span data-ttu-id="251a0-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="251a0-118">PARAMETERS</span></span>

### <span data-ttu-id="251a0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="251a0-119">-DefaultProfile</span></span>
<span data-ttu-id="251a0-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="251a0-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="251a0-121">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="251a0-121">-TargetResourceId</span></span>
<span data-ttu-id="251a0-122">ИД ресурса, который нужно связать</span><span class="sxs-lookup"><span data-stu-id="251a0-122">The resource ID to associate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="251a0-123">-AssociationName</span><span class="sxs-lookup"><span data-stu-id="251a0-123">-AssociationName</span></span>
<span data-ttu-id="251a0-124">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="251a0-124">The resource name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="251a0-125">-RuleId</span><span class="sxs-lookup"><span data-stu-id="251a0-125">-RuleId</span></span>
<span data-ttu-id="251a0-126">ИД правила сбора данных</span><span class="sxs-lookup"><span data-stu-id="251a0-126">The data collection rule ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByDataCollectionRuleId
Aliases: DataCollectionRuleId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="251a0-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="251a0-127">-InputObject</span></span>
<span data-ttu-id="251a0-128">Объект PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="251a0-128">PSDataCollectionRuleResource Object</span></span>

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="251a0-129">-Description</span><span class="sxs-lookup"><span data-stu-id="251a0-129">-Description</span></span>
<span data-ttu-id="251a0-130">Описание ресурса</span><span class="sxs-lookup"><span data-stu-id="251a0-130">The resource description</span></span>

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

### <span data-ttu-id="251a0-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="251a0-131">-Confirm</span></span>
<span data-ttu-id="251a0-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="251a0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="251a0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="251a0-133">-WhatIf</span></span>
<span data-ttu-id="251a0-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="251a0-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="251a0-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="251a0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="251a0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="251a0-136">CommonParameters</span></span>
<span data-ttu-id="251a0-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="251a0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="251a0-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="251a0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="251a0-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="251a0-139">INPUTS</span></span>

### <span data-ttu-id="251a0-140">System.String</span><span class="sxs-lookup"><span data-stu-id="251a0-140">System.String</span></span>

## <span data-ttu-id="251a0-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="251a0-141">OUTPUTS</span></span>

### <span data-ttu-id="251a0-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span><span class="sxs-lookup"><span data-stu-id="251a0-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span></span>

## <span data-ttu-id="251a0-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="251a0-143">NOTES</span></span>

## <span data-ttu-id="251a0-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="251a0-144">RELATED LINKS</span></span>

<span data-ttu-id="251a0-145">[Set-AzDataCollectionRuleAssociation](./Set-AzDataCollectionRuleAssociation.md) 
 [Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md) 
 [Get-AzDataCollectionRuleAssociation](./Get-AzDataCollectionRuleAssociation.md)</span><span class="sxs-lookup"><span data-stu-id="251a0-145">[Set-AzDataCollectionRuleAssociation](./Set-AzDataCollectionRuleAssociation.md)
[Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md)
[Get-AzDataCollectionRuleAssociation](./Get-AzDataCollectionRuleAssociation.md)</span></span>
