---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 50920451ca96d21875352ff2ef460a5dcc989a20
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394359"
---
# <span data-ttu-id="3b0f9-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="3b0f9-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="3b0f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b0f9-102">SYNOPSIS</span></span>
<span data-ttu-id="3b0f9-103">Создание рабочей области или восстановление удаленной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-103">Creates a workspace, or restore a soft-deleted workspace.</span></span>

## <span data-ttu-id="3b0f9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3b0f9-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [[-PublicNetworkAccessForIngestion] <String>]
 [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b0f9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b0f9-105">DESCRIPTION</span></span>
<span data-ttu-id="3b0f9-106">Командлет **New-AzOperationalInsightsWorkspace** создает рабочее пространство в указанной группе ресурсов и расположении.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span> <span data-ttu-id="3b0f9-107">Можно также восстановить неявное рабочее пространство.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-107">Or restore a soft-deleted workspace.</span></span>

## <span data-ttu-id="3b0f9-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3b0f9-108">EXAMPLES</span></span>

### <span data-ttu-id="3b0f9-109">Пример 1. Создание рабочей области по имени</span><span class="sxs-lookup"><span data-stu-id="3b0f9-109">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="3b0f9-110">Эта команда создает стандартную рабочая область с именем MyWorkspace в группе ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-110">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="3b0f9-111">Пример 2. Создание рабочей области и связыва ее с существующей учетной записью</span><span class="sxs-lookup"><span data-stu-id="3b0f9-111">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="3b0f9-112">Первая команда использует командлет Get-AzOperationalInsightsLinkTargets для получения целевых объектов связываемой учетной записи Operational Insights, а затем сохраняет их в $OILinkTargets переменной.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-112">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="3b0f9-113">Вторая команда передает первую целевую ссылку учетной записи в $OILinkTargets **командлету New-AzOperationalInsightsWorkspace** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-113">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3b0f9-114">Эта команда создает стандартную рабочее пространство MyWorkspace, связанное с первой учетной записью Operational Insights в $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-114">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="3b0f9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b0f9-115">PARAMETERS</span></span>

### <span data-ttu-id="3b0f9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b0f9-116">-DefaultProfile</span></span>
<span data-ttu-id="3b0f9-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3b0f9-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b0f9-118">-Force</span><span class="sxs-lookup"><span data-stu-id="3b0f9-118">-Force</span></span>
<span data-ttu-id="3b0f9-119">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3b0f9-120">-Location</span><span class="sxs-lookup"><span data-stu-id="3b0f9-120">-Location</span></span>
<span data-ttu-id="3b0f9-121">Определяет место, в котором будет создаваться рабочее пространство, например "Восточная США" или "Западная Европа".</span><span class="sxs-lookup"><span data-stu-id="3b0f9-121">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b0f9-122">-Name</span><span class="sxs-lookup"><span data-stu-id="3b0f9-122">-Name</span></span>
<span data-ttu-id="3b0f9-123">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-123">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b0f9-124">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="3b0f9-124">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="3b0f9-125">Тип доступа к сети для доступа к рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-125">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="3b0f9-126">Значение должно быть включено или отключено</span><span class="sxs-lookup"><span data-stu-id="3b0f9-126">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b0f9-127">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="3b0f9-127">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="3b0f9-128">Тип доступа к сети для запроса рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-128">The network access type for accessing workspace query.</span></span> <span data-ttu-id="3b0f9-129">Значение должно быть включено или отключено</span><span class="sxs-lookup"><span data-stu-id="3b0f9-129">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b0f9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b0f9-130">-ResourceGroupName</span></span>
<span data-ttu-id="3b0f9-131">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3b0f9-132">Рабочая область создается в этой группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-132">The workspace is created in this resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b0f9-133">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="3b0f9-133">-RetentionInDays</span></span>
<span data-ttu-id="3b0f9-134">Хранение данных рабочей области в днях.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-134">The workspace data retention in days.</span></span> <span data-ttu-id="3b0f9-135">730 дней — это максимальное значение для всех остальных skus</span><span class="sxs-lookup"><span data-stu-id="3b0f9-135">730 days is the maximum allowed for all other Skus</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b0f9-136">-SKU</span><span class="sxs-lookup"><span data-stu-id="3b0f9-136">-Sku</span></span>
<span data-ttu-id="3b0f9-137">Определяет уровень обслуживания рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-137">Specifies the service tier of the workspace.</span></span> <span data-ttu-id="3b0f9-138">Дополнительные сведения о том, какое значение нужно использовать, можно найти в https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers</span><span class="sxs-lookup"><span data-stu-id="3b0f9-138">For more information regarding which value to use please check https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers.</span></span>
<span data-ttu-id="3b0f9-139">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="3b0f9-139">Valid values are:</span></span>
- <span data-ttu-id="3b0f9-140">бесплатно</span><span class="sxs-lookup"><span data-stu-id="3b0f9-140">free</span></span>
- <span data-ttu-id="3b0f9-141">pergb2018</span><span class="sxs-lookup"><span data-stu-id="3b0f9-141">pergb2018</span></span>
- <span data-ttu-id="3b0f9-142">pernode</span><span class="sxs-lookup"><span data-stu-id="3b0f9-142">pernode</span></span>
- <span data-ttu-id="3b0f9-143">premium</span><span class="sxs-lookup"><span data-stu-id="3b0f9-143">premium</span></span>
- <span data-ttu-id="3b0f9-144">автономный</span><span class="sxs-lookup"><span data-stu-id="3b0f9-144">standalone</span></span>
- <span data-ttu-id="3b0f9-145">стандартный</span><span class="sxs-lookup"><span data-stu-id="3b0f9-145">standard</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b0f9-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="3b0f9-146">-Tag</span></span>
<span data-ttu-id="3b0f9-147">Теги ресурсов для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-147">The resource tags for the workspace.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b0f9-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b0f9-148">-Confirm</span></span>
<span data-ttu-id="3b0f9-149">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b0f9-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b0f9-150">-WhatIf</span></span>
<span data-ttu-id="3b0f9-151">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b0f9-152">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b0f9-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b0f9-153">CommonParameters</span></span>
<span data-ttu-id="3b0f9-154">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b0f9-155">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b0f9-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b0f9-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3b0f9-156">INPUTS</span></span>

### <span data-ttu-id="3b0f9-157">System.String</span><span class="sxs-lookup"><span data-stu-id="3b0f9-157">System.String</span></span>

### <span data-ttu-id="3b0f9-158">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3b0f9-158">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="3b0f9-159">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="3b0f9-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3b0f9-160">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3b0f9-160">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="3b0f9-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3b0f9-161">OUTPUTS</span></span>

### <span data-ttu-id="3b0f9-162">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="3b0f9-162">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="3b0f9-163">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3b0f9-163">NOTES</span></span>

<span data-ttu-id="3b0f9-164">Выпущена новая модель цен.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-164">A new pricing model has been released.</span></span> <span data-ttu-id="3b0f9-165">Если вы — CSP, это означает, что для SKU необходимо использовать автономный режим.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-165">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="3b0f9-166">При этом sku будет изменен на pergb2018.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-166">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="3b0f9-167">Дополнительные сведения см. в следующих сведениях: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="3b0f9-167">For more information, please see the following: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="3b0f9-168">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b0f9-168">RELATED LINKS</span></span>

[<span data-ttu-id="3b0f9-169">Azure Operational Insights Cmdlets</span><span class="sxs-lookup"><span data-stu-id="3b0f9-169">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="3b0f9-170">Get-AzOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="3b0f9-170">Get-AzOperationalInsightsLinkTargets</span></span>](./Get-AzOperationalInsightsLinkTargets.md)


