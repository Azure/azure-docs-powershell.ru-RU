---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
ms.openlocfilehash: 59ce466233e4997f54ed8f29835e7e64d455fb86
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403679"
---
# <span data-ttu-id="22e75-101">Get-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="22e75-101">Get-AzActionRule</span></span>

## <span data-ttu-id="22e75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22e75-102">SYNOPSIS</span></span>
<span data-ttu-id="22e75-103">Получить сведения о правилах действия</span><span class="sxs-lookup"><span data-stu-id="22e75-103">Get Action Rules Information</span></span>

## <span data-ttu-id="22e75-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="22e75-104">SYNTAX</span></span>

### <span data-ttu-id="22e75-105">ListActionRules (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="22e75-105">ListActionRules (Default)</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceType <String>]
 [-TargetResourceGroup <String>] [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>]
 [-AlertRuleId <String>] [-Description <String>] [-ActionGroup <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22e75-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="22e75-106">ResourceId</span></span>
```
Get-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22e75-107">ActionRuleByName</span><span class="sxs-lookup"><span data-stu-id="22e75-107">ActionRuleByName</span></span>
```
Get-AzActionRule -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="22e75-108">ListActionRulesByTargetResourceId</span><span class="sxs-lookup"><span data-stu-id="22e75-108">ListActionRulesByTargetResourceId</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceId <String>]
 [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>] [-AlertRuleId <String>]
 [-Description <String>] [-ActionGroup <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22e75-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="22e75-109">DESCRIPTION</span></span>
<span data-ttu-id="22e75-110">**Настроит правила действий для get-AzActionRule.**</span><span class="sxs-lookup"><span data-stu-id="22e75-110">**Get-AzActionRule** cmdlet gets action rules configured.</span></span>

## <span data-ttu-id="22e75-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="22e75-111">EXAMPLES</span></span>

### <span data-ttu-id="22e75-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="22e75-112">Example 1</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Severity "Sev2" -MonitorService "Platform"
```

<span data-ttu-id="22e75-113">Со списком всех правил действий, настроенных в тестовой группе ресурсов, отфильтрованной по Sev2 severity и Platform Monitor Service.</span><span class="sxs-lookup"><span data-stu-id="22e75-113">List all action rules configured in resource group test-rg filtered on Sev2 severity and Platform Monitor Service.</span></span> <span data-ttu-id="22e75-114">Используйте Format-List, чтобы получить в списке сведения о каждом правиле действия.</span><span class="sxs-lookup"><span data-stu-id="22e75-114">Use Format-List to get the details of each action rule in list.</span></span>

### <span data-ttu-id="22e75-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="22e75-115">Example 2</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Name "Test-Action-Rule" | Format-List
```

<span data-ttu-id="22e75-116">Получите правило действия с именем Test-Action-Rule в группе ресурсов test-rg.</span><span class="sxs-lookup"><span data-stu-id="22e75-116">Get the action rule with name Test-Action-Rule in test-rg resource group.</span></span>

## <span data-ttu-id="22e75-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22e75-117">PARAMETERS</span></span>

### <span data-ttu-id="22e75-118">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="22e75-118">-ActionGroup</span></span>
<span data-ttu-id="22e75-119">Группа действий</span><span class="sxs-lookup"><span data-stu-id="22e75-119">Action group</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22e75-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="22e75-120">-AlertRuleId</span></span>
<span data-ttu-id="22e75-121">Фильтрация по ИД правила оповещения</span><span class="sxs-lookup"><span data-stu-id="22e75-121">Filter on Alert Rule Id</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22e75-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22e75-122">-DefaultProfile</span></span>
<span data-ttu-id="22e75-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="22e75-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22e75-124">-Description</span><span class="sxs-lookup"><span data-stu-id="22e75-124">-Description</span></span>
<span data-ttu-id="22e75-125">Фильтрация всех оповещений с ид smart Group</span><span class="sxs-lookup"><span data-stu-id="22e75-125">Filter all the alerts having the Smart Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22e75-126">-ImpactedScope</span><span class="sxs-lookup"><span data-stu-id="22e75-126">-ImpactedScope</span></span>
<span data-ttu-id="22e75-127">Фильтр по области влияния</span><span class="sxs-lookup"><span data-stu-id="22e75-127">Filter on Impacted scope</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22e75-128">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="22e75-128">-MonitorService</span></span>
<span data-ttu-id="22e75-129">Фильтр по службе Moniter</span><span class="sxs-lookup"><span data-stu-id="22e75-129">Filter on Moniter Service</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22e75-130">-Name</span><span class="sxs-lookup"><span data-stu-id="22e75-130">-Name</span></span>
<span data-ttu-id="22e75-131">Имя правила действия.</span><span class="sxs-lookup"><span data-stu-id="22e75-131">Name of action rule.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ActionRuleByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22e75-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22e75-132">-ResourceGroupName</span></span>
<span data-ttu-id="22e75-133">Имя группы ресурсов, в которой находится правило действия.</span><span class="sxs-lookup"><span data-stu-id="22e75-133">Resource Group Name in which action rule resides.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ActionRuleByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22e75-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22e75-134">-ResourceId</span></span>
<span data-ttu-id="22e75-135">Получите правило действий по ид ресурса.</span><span class="sxs-lookup"><span data-stu-id="22e75-135">Get Action rule by resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22e75-136">-Severity</span><span class="sxs-lookup"><span data-stu-id="22e75-136">-Severity</span></span>
<span data-ttu-id="22e75-137">Фильтрация по важности оповещения</span><span class="sxs-lookup"><span data-stu-id="22e75-137">Filter on Severity of alert</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22e75-138">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="22e75-138">-TargetResourceGroup</span></span>
<span data-ttu-id="22e75-139">Фильтрация по имени группы ресурсов целевого ресурса оповещения.</span><span class="sxs-lookup"><span data-stu-id="22e75-139">Filter on Resource group name of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22e75-140">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="22e75-140">-TargetResourceId</span></span>
<span data-ttu-id="22e75-141">Фильтрация по ИД ресурса целевого ресурса оповещения.</span><span class="sxs-lookup"><span data-stu-id="22e75-141">Filter on Resource Id of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22e75-142">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="22e75-142">-TargetResourceType</span></span>
<span data-ttu-id="22e75-143">Фильтрация по типу ресурса целевого ресурса оповещения.</span><span class="sxs-lookup"><span data-stu-id="22e75-143">Filter on Resource type of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22e75-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22e75-144">CommonParameters</span></span>
<span data-ttu-id="22e75-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22e75-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22e75-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22e75-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22e75-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="22e75-147">INPUTS</span></span>

### <span data-ttu-id="22e75-148">Нет</span><span class="sxs-lookup"><span data-stu-id="22e75-148">None</span></span>

## <span data-ttu-id="22e75-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="22e75-149">OUTPUTS</span></span>

### <span data-ttu-id="22e75-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="22e75-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="22e75-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="22e75-151">NOTES</span></span>

## <span data-ttu-id="22e75-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="22e75-152">RELATED LINKS</span></span>
