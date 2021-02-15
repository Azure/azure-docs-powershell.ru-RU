---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdatacollectionruleassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRuleAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRuleAssociation.md
ms.openlocfilehash: 144e67a2e58aeaa7fe7aa424ddc79bfca4aaa538
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214257"
---
# <span data-ttu-id="322ef-101">Get-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="322ef-101">Get-AzDataCollectionRuleAssociation</span></span>

## <span data-ttu-id="322ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="322ef-102">SYNOPSIS</span></span>
<span data-ttu-id="322ef-103">Возвращает связи правил сбора данных.</span><span class="sxs-lookup"><span data-stu-id="322ef-103">Gets data collection rule association(s).</span></span>

## <span data-ttu-id="322ef-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="322ef-104">SYNTAX</span></span>

### <span data-ttu-id="322ef-105">ByAssociatedResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="322ef-105">ByAssociatedResource (Default)</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -TargetResourceId <string> 
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="322ef-106">ByName</span><span class="sxs-lookup"><span data-stu-id="322ef-106">ByName</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -TargetResourceId <string> 
   -AssociationName <string> 
   [-DefaultProfile <IAzureContextContainer>] 
   [<CommonParameters>]
```

### <span data-ttu-id="322ef-107">ByRule</span><span class="sxs-lookup"><span data-stu-id="322ef-107">ByRule</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -ResourceGroupName <string> 
   -RuleName <string> 
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="322ef-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="322ef-108">ByInputObject</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -InputObject <PSDataCollectionRuleResource> 
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

## <span data-ttu-id="322ef-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="322ef-109">DESCRIPTION</span></span>
<span data-ttu-id="322ef-110">Чтобы получить одно или несколько связей правил сбора данных (DCRA), можно получить одно или несколько **cmdletRuleAssociation Get-AzDataCollectionRuleAssociation.**</span><span class="sxs-lookup"><span data-stu-id="322ef-110">The **Get-AzDataCollectionRuleAssociation** cmdlet gets one or more data collection rules associations (DCRA).</span></span>

<span data-ttu-id="322ef-111">Чтобы применить DCR к виртуальной машине, необходимо создать связь для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="322ef-111">To apply a DCR to a virtual machine, you create an association for the virtual machine.</span></span> <span data-ttu-id="322ef-112">Виртуальная машина может иметь связь с несколькими DCR, а DCR может иметь несколько виртуальных машин, связанных с ней.</span><span class="sxs-lookup"><span data-stu-id="322ef-112">A virtual machine may have an association to multiple DCRs, and a DCR may have multiple virtual machines associated to it.</span></span> <span data-ttu-id="322ef-113">Это позволяет определить набор dcrs, каждый из которых соответствует определенному требованию, и применить их только к виртуальным машинам, на которых они применяются.</span><span class="sxs-lookup"><span data-stu-id="322ef-113">This allows you to define a set of DCRs, each matching a particular requirement, and apply them to only the virtual machines where they apply.</span></span> <span data-ttu-id="322ef-114">Ниже приводится статья "Настройка сбора данных для агента [Azure Monitor"](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) с помощью DCRA.</span><span class="sxs-lookup"><span data-stu-id="322ef-114">Here is the ["Configure data collection for the Azure Monitor agent"](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) using DCRA article.</span></span>

## <span data-ttu-id="322ef-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="322ef-115">EXAMPLES</span></span>

### <span data-ttu-id="322ef-116">Пример 1. Связывайте правила сбора данных по ИД целевого ресурса (связанная виртуальная машинка)</span><span class="sxs-lookup"><span data-stu-id="322ef-116">Example 1: Get data collection rules associations by target resource ID (associated virtual machine)</span></span>
```
PS C:\>$vm = Get-AzVM -ResourceGroupName $rg -Name $vmName
PS C:\>Get-AzDataCollectionRuleAssociation -TargetResourceId $vm.Id

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="322ef-117">Эта команда содержит все правила сбора данных для заданного ИД целевого ресурса (виртуальной машины).</span><span class="sxs-lookup"><span data-stu-id="322ef-117">This command lists all the data collection rules for the given target resource ID (virtual machine).</span></span>

### <span data-ttu-id="322ef-118">Пример 2. Получите связи правил сбора данных по правилам (DCR)</span><span class="sxs-lookup"><span data-stu-id="322ef-118">Example 2: Get data collection rules associations by rule (DCR)</span></span>
```
PS C:\>Get-AzDataCollectionRuleAssociation -ResourceGroup $rg -RuleName $dcrName

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="322ef-119">В этой команде перечислены связи правил сбора данных для заданной группы ресурсов и правила (DCR).</span><span class="sxs-lookup"><span data-stu-id="322ef-119">This command lists data collection rules associations for the given resource group and rule (DCR).</span></span>

### <span data-ttu-id="322ef-120">Пример 3. Получите связи правил сбора данных по входным объектам (PSDataCollectionRuleResource)</span><span class="sxs-lookup"><span data-stu-id="322ef-120">Example 3: Get data collection rule associations by input object (PSDataCollectionRuleResource)</span></span>
```
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName $rg -RuleName $dcrName
PS C:\>$dcr | Get-AzDataCollectionRuleAssociation

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="322ef-121">Эта команда содержит список объединений правил сбора данных для заданного объекта ввода.</span><span class="sxs-lookup"><span data-stu-id="322ef-121">This command lists data collection rules associations for the given input object.</span></span>

### <span data-ttu-id="322ef-122">Пример 4. Связь правил сбора данных по ИД целевого ресурса (связанная виртуальная машину) и имени связи</span><span class="sxs-lookup"><span data-stu-id="322ef-122">Example 4: Get a data collection rule association by target resource ID (associated virtual machine) and association name</span></span>
```
PS C:\>Get-AzDataCollectionRuleAssociation -TargetResourceId $vm.Id -AssociationName $assocName

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="322ef-123">Эта команда содержит один (список с одним элементом) связи правил сбора данных.</span><span class="sxs-lookup"><span data-stu-id="322ef-123">This command lists one (a list with a single element) data collection rule association.</span></span>

## <span data-ttu-id="322ef-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="322ef-124">PARAMETERS</span></span>

### <span data-ttu-id="322ef-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="322ef-125">-DefaultProfile</span></span>
<span data-ttu-id="322ef-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="322ef-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="322ef-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="322ef-127">-TargetResourceId</span></span>
<span data-ttu-id="322ef-128">Связанный ид ресурса</span><span class="sxs-lookup"><span data-stu-id="322ef-128">The associated resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByAssociatedResource (Default)
Aliases: ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="322ef-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="322ef-129">-ResourceGroupName</span></span>
<span data-ttu-id="322ef-130">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="322ef-130">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="322ef-131">-RuleName</span><span class="sxs-lookup"><span data-stu-id="322ef-131">-RuleName</span></span>
<span data-ttu-id="322ef-132">Имя правила сбора данных</span><span class="sxs-lookup"><span data-stu-id="322ef-132">The data collection rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRule
Aliases: DataCollectionRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="322ef-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="322ef-133">-InputObject</span></span>
<span data-ttu-id="322ef-134">Объект PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="322ef-134">PSDataCollectionRuleResource Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="322ef-135">-AssociationName</span><span class="sxs-lookup"><span data-stu-id="322ef-135">-AssociationName</span></span>
<span data-ttu-id="322ef-136">Имя связи.</span><span class="sxs-lookup"><span data-stu-id="322ef-136">The name of the association.</span></span>

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

### <span data-ttu-id="322ef-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="322ef-137">CommonParameters</span></span>
<span data-ttu-id="322ef-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="322ef-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="322ef-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="322ef-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="322ef-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="322ef-140">INPUTS</span></span>

### <span data-ttu-id="322ef-141">System.String</span><span class="sxs-lookup"><span data-stu-id="322ef-141">System.String</span></span>
### <span data-ttu-id="322ef-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="322ef-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="322ef-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="322ef-143">OUTPUTS</span></span>

### <span data-ttu-id="322ef-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span><span class="sxs-lookup"><span data-stu-id="322ef-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span></span>

## <span data-ttu-id="322ef-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="322ef-145">NOTES</span></span>

## <span data-ttu-id="322ef-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="322ef-146">RELATED LINKS</span></span>

<span data-ttu-id="322ef-147">[Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md) 
 [New-AzDataCollectionRuleAssociation](./New-AzDataCollectionRuleAssociation.md)</span><span class="sxs-lookup"><span data-stu-id="322ef-147">[Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md)
[New-AzDataCollectionRuleAssociation](./New-AzDataCollectionRuleAssociation.md)</span></span>
