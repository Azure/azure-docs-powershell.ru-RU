---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
ms.openlocfilehash: f3904826ef41f271086d048183b8b2035d1b11e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728194"
---
# <span data-ttu-id="6e4d5-101">Get-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="6e4d5-101">Get-AzActionRule</span></span>

## <span data-ttu-id="6e4d5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6e4d5-102">SYNOPSIS</span></span>
<span data-ttu-id="6e4d5-103">Получение сведений о правилах действия</span><span class="sxs-lookup"><span data-stu-id="6e4d5-103">Get Action Rules Information</span></span>

## <span data-ttu-id="6e4d5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6e4d5-104">SYNTAX</span></span>

### <span data-ttu-id="6e4d5-105">ListActionRules (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6e4d5-105">ListActionRules (Default)</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceType <String>]
 [-TargetResourceGroup <String>] [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>]
 [-AlertRuleId <String>] [-Description <String>] [-ActionGroup <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e4d5-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e4d5-106">ResourceId</span></span>
```
Get-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e4d5-107">ActionRuleByName</span><span class="sxs-lookup"><span data-stu-id="6e4d5-107">ActionRuleByName</span></span>
```
Get-AzActionRule -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6e4d5-108">ListActionRulesByTargetResourceId</span><span class="sxs-lookup"><span data-stu-id="6e4d5-108">ListActionRulesByTargetResourceId</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceId <String>]
 [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>] [-AlertRuleId <String>]
 [-Description <String>] [-ActionGroup <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6e4d5-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e4d5-109">DESCRIPTION</span></span>
<span data-ttu-id="6e4d5-110">Командлет **Get-AzActionRule** получает правила действий, которые настроены.</span><span class="sxs-lookup"><span data-stu-id="6e4d5-110">**Get-AzActionRule** cmdlet gets action rules configured.</span></span>

## <span data-ttu-id="6e4d5-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6e4d5-111">EXAMPLES</span></span>

### <span data-ttu-id="6e4d5-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6e4d5-112">Example 1</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Severity "Sev2" -MonitorService "Platform"
```

<span data-ttu-id="6e4d5-113">Список всех правил действий, настроенных в тестировании группы ресурсов — RG, отфильтрованные по службе уровня серьезности Sev2 и монитора платформы.</span><span class="sxs-lookup"><span data-stu-id="6e4d5-113">List all action rules configured in resource group test-rg filtered on Sev2 severity and Platform Monitor Service.</span></span> <span data-ttu-id="6e4d5-114">С помощью Format-List можно получить подробные сведения о каждом правиле действия в списке.</span><span class="sxs-lookup"><span data-stu-id="6e4d5-114">Use Format-List to get the details of each action rule in list.</span></span>

### <span data-ttu-id="6e4d5-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6e4d5-115">Example 2</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Name "Test-Action-Rule" | Format-List
```

<span data-ttu-id="6e4d5-116">Получить правило действия с именем тест — правило действия — в группе ресурсов Test-RG.</span><span class="sxs-lookup"><span data-stu-id="6e4d5-116">Get the action rule with name Test-Action-Rule in test-rg resource group.</span></span>

## <span data-ttu-id="6e4d5-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6e4d5-117">PARAMETERS</span></span>

### <span data-ttu-id="6e4d5-118">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="6e4d5-118">-ActionGroup</span></span>
<span data-ttu-id="6e4d5-119">Группа действий</span><span class="sxs-lookup"><span data-stu-id="6e4d5-119">Action group</span></span>

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

### <span data-ttu-id="6e4d5-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="6e4d5-120">-AlertRuleId</span></span>
<span data-ttu-id="6e4d5-121">Фильтр по коду правила генерации оповещений</span><span class="sxs-lookup"><span data-stu-id="6e4d5-121">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="6e4d5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e4d5-122">-DefaultProfile</span></span>
<span data-ttu-id="6e4d5-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6e4d5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e4d5-124">-Описание</span><span class="sxs-lookup"><span data-stu-id="6e4d5-124">-Description</span></span>
<span data-ttu-id="6e4d5-125">Фильтрация всех оповещений с кодом Smart Group</span><span class="sxs-lookup"><span data-stu-id="6e4d5-125">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="6e4d5-126">-ImpactedScope</span><span class="sxs-lookup"><span data-stu-id="6e4d5-126">-ImpactedScope</span></span>
<span data-ttu-id="6e4d5-127">Фильтрация по затронутой области</span><span class="sxs-lookup"><span data-stu-id="6e4d5-127">Filter on Impacted scope</span></span>

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

### <span data-ttu-id="6e4d5-128">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="6e4d5-128">-MonitorService</span></span>
<span data-ttu-id="6e4d5-129">Фильтрация в службе moniter</span><span class="sxs-lookup"><span data-stu-id="6e4d5-129">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="6e4d5-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6e4d5-130">-Name</span></span>
<span data-ttu-id="6e4d5-131">Имя правила действия.</span><span class="sxs-lookup"><span data-stu-id="6e4d5-131">Name of action rule.</span></span>

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

### <span data-ttu-id="6e4d5-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e4d5-132">-ResourceGroupName</span></span>
<span data-ttu-id="6e4d5-133">Имя группы ресурсов, в которой находится правило действия.</span><span class="sxs-lookup"><span data-stu-id="6e4d5-133">Resource Group Name in which action rule resides.</span></span>

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

### <span data-ttu-id="6e4d5-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e4d5-134">-ResourceId</span></span>
<span data-ttu-id="6e4d5-135">Получить правило действия по идентификатору изображение.</span><span class="sxs-lookup"><span data-stu-id="6e4d5-135">Get Action rule by resoure id.</span></span>

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

### <span data-ttu-id="6e4d5-136">-Серьезность</span><span class="sxs-lookup"><span data-stu-id="6e4d5-136">-Severity</span></span>
<span data-ttu-id="6e4d5-137">Фильтрация по уровню серьезности оповещений</span><span class="sxs-lookup"><span data-stu-id="6e4d5-137">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="6e4d5-138">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6e4d5-138">-TargetResourceGroup</span></span>
<span data-ttu-id="6e4d5-139">Фильтрация по имени группы ресурсов для целевого ресурса оповещения.</span><span class="sxs-lookup"><span data-stu-id="6e4d5-139">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="6e4d5-140">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="6e4d5-140">-TargetResourceId</span></span>
<span data-ttu-id="6e4d5-141">Фильтрация по идентификатору ресурса целевого ресурса оповещения.</span><span class="sxs-lookup"><span data-stu-id="6e4d5-141">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="6e4d5-142">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="6e4d5-142">-TargetResourceType</span></span>
<span data-ttu-id="6e4d5-143">Фильтрация по типу ресурса целевого ресурса оповещения.</span><span class="sxs-lookup"><span data-stu-id="6e4d5-143">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="6e4d5-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e4d5-144">CommonParameters</span></span>
<span data-ttu-id="6e4d5-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6e4d5-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e4d5-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e4d5-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e4d5-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6e4d5-147">INPUTS</span></span>

### <span data-ttu-id="6e4d5-148">Ничего</span><span class="sxs-lookup"><span data-stu-id="6e4d5-148">None</span></span>

## <span data-ttu-id="6e4d5-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e4d5-149">OUTPUTS</span></span>

### <span data-ttu-id="6e4d5-150">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="6e4d5-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="6e4d5-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="6e4d5-151">NOTES</span></span>

## <span data-ttu-id="6e4d5-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6e4d5-152">RELATED LINKS</span></span>
