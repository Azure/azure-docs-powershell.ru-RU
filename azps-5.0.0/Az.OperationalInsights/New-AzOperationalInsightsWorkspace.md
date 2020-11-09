---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: feac2aa9c5dd92c0d76090c6fc28353d56f9647c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318434"
---
# <span data-ttu-id="003b9-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="003b9-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="003b9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="003b9-102">SYNOPSIS</span></span>
<span data-ttu-id="003b9-103">Создание рабочей области.</span><span class="sxs-lookup"><span data-stu-id="003b9-103">Creates a workspace.</span></span>

## <span data-ttu-id="003b9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="003b9-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [[-PublicNetworkAccessForIngestion] <String>]
 [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="003b9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="003b9-105">DESCRIPTION</span></span>
<span data-ttu-id="003b9-106">Командлет **New-AzOperationalInsightsWorkspace** создает рабочую область в заданной группе ресурсов и расположении.</span><span class="sxs-lookup"><span data-stu-id="003b9-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="003b9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="003b9-107">EXAMPLES</span></span>

### <span data-ttu-id="003b9-108">Пример 1: создание рабочей области по имени</span><span class="sxs-lookup"><span data-stu-id="003b9-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="003b9-109">Эта команда создает стандартную рабочую область SKU с именем MyWorkspace в группе ресурсов с именем ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="003b9-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="003b9-110">Пример 2: создание рабочей области и связывание ее с существующей учетной записью</span><span class="sxs-lookup"><span data-stu-id="003b9-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="003b9-111">Первая команда использует командлет Get-AzOperationalInsightsLinkTargets для получения целевых данных ссылки на учетную запись, а затем сохраняет их в переменной $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="003b9-111">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="003b9-112">Вторая команда передает конечный объект ссылки на учетную запись в $OILinkTargets командлету **New-AzOperationalInsightsWorkspace** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="003b9-112">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="003b9-113">Команда создает стандартную рабочую область SKU с именем MyWorkspace, связанную с учетной записью первой оперативной аналитики в $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="003b9-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="003b9-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="003b9-114">PARAMETERS</span></span>

### <span data-ttu-id="003b9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="003b9-115">-DefaultProfile</span></span>
<span data-ttu-id="003b9-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="003b9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="003b9-117">-Force</span><span class="sxs-lookup"><span data-stu-id="003b9-117">-Force</span></span>
<span data-ttu-id="003b9-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="003b9-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="003b9-119">-Location</span><span class="sxs-lookup"><span data-stu-id="003b9-119">-Location</span></span>
<span data-ttu-id="003b9-120">Указывает место для создания рабочей области, например "Восток США" или "Западная Европа".</span><span class="sxs-lookup"><span data-stu-id="003b9-120">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

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

### <span data-ttu-id="003b9-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="003b9-121">-Name</span></span>
<span data-ttu-id="003b9-122">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="003b9-122">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="003b9-123">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="003b9-123">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="003b9-124">Тип доступа к сети для доступа к рабочей области.</span><span class="sxs-lookup"><span data-stu-id="003b9-124">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="003b9-125">Значение должно быть "включено" или "отключено"</span><span class="sxs-lookup"><span data-stu-id="003b9-125">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="003b9-126">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="003b9-126">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="003b9-127">Тип сетевого доступа для доступа к запросу рабочей области.</span><span class="sxs-lookup"><span data-stu-id="003b9-127">The network access type for accessing workspace query.</span></span> <span data-ttu-id="003b9-128">Значение должно быть "включено" или "отключено"</span><span class="sxs-lookup"><span data-stu-id="003b9-128">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="003b9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="003b9-129">-ResourceGroupName</span></span>
<span data-ttu-id="003b9-130">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="003b9-130">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="003b9-131">Рабочая область будет создана в этой группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="003b9-131">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="003b9-132">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="003b9-132">-RetentionInDays</span></span>
<span data-ttu-id="003b9-133">Хранение данных рабочей области в днях.</span><span class="sxs-lookup"><span data-stu-id="003b9-133">The workspace data retention in days.</span></span> <span data-ttu-id="003b9-134">730 дней – это максимально допустимое количество номеров SKU.</span><span class="sxs-lookup"><span data-stu-id="003b9-134">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="003b9-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="003b9-135">-Sku</span></span>
<span data-ttu-id="003b9-136">Указывает уровень обслуживания рабочей области.</span><span class="sxs-lookup"><span data-stu-id="003b9-136">Specifies the service tier of the workspace.</span></span> <span data-ttu-id="003b9-137">Дополнительные сведения о том, какое значение использовать, можно найти в этой видеосвязи https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers .</span><span class="sxs-lookup"><span data-stu-id="003b9-137">For more information regarding which value to use please check https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers.</span></span>
<span data-ttu-id="003b9-138">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="003b9-138">Valid values are:</span></span>
- <span data-ttu-id="003b9-139">бесплатно</span><span class="sxs-lookup"><span data-stu-id="003b9-139">free</span></span>
- <span data-ttu-id="003b9-140">pergb2018</span><span class="sxs-lookup"><span data-stu-id="003b9-140">pergb2018</span></span>
- <span data-ttu-id="003b9-141">pernode</span><span class="sxs-lookup"><span data-stu-id="003b9-141">pernode</span></span>
- <span data-ttu-id="003b9-142">версию</span><span class="sxs-lookup"><span data-stu-id="003b9-142">premium</span></span>
- <span data-ttu-id="003b9-143">отдельно</span><span class="sxs-lookup"><span data-stu-id="003b9-143">standalone</span></span>
- <span data-ttu-id="003b9-144">Стандартная</span><span class="sxs-lookup"><span data-stu-id="003b9-144">standard</span></span>

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

### <span data-ttu-id="003b9-145">-Тег</span><span class="sxs-lookup"><span data-stu-id="003b9-145">-Tag</span></span>
<span data-ttu-id="003b9-146">Теги ресурсов для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="003b9-146">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="003b9-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="003b9-147">-Confirm</span></span>
<span data-ttu-id="003b9-148">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="003b9-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="003b9-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="003b9-149">-WhatIf</span></span>
<span data-ttu-id="003b9-150">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="003b9-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="003b9-151">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="003b9-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="003b9-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="003b9-152">CommonParameters</span></span>
<span data-ttu-id="003b9-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="003b9-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="003b9-154">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="003b9-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="003b9-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="003b9-155">INPUTS</span></span>

### <span data-ttu-id="003b9-156">System. String</span><span class="sxs-lookup"><span data-stu-id="003b9-156">System.String</span></span>

### <span data-ttu-id="003b9-157">System. Nullable "1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="003b9-157">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="003b9-158">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="003b9-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="003b9-159">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="003b9-159">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="003b9-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="003b9-160">OUTPUTS</span></span>

### <span data-ttu-id="003b9-161">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="003b9-161">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="003b9-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="003b9-162">NOTES</span></span>

<span data-ttu-id="003b9-163">Была выпущена новая модель ценообразования.</span><span class="sxs-lookup"><span data-stu-id="003b9-163">A new pricing model has been released.</span></span> <span data-ttu-id="003b9-164">Если вы являетесь поставщиком службы криптографии, это означает, что для SKU вам нужно использовать "standalone".</span><span class="sxs-lookup"><span data-stu-id="003b9-164">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="003b9-165">В фоновом режиме номер SKU изменится на pergb2018.</span><span class="sxs-lookup"><span data-stu-id="003b9-165">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="003b9-166">Дополнительные сведения можно найти в следующих примерах: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="003b9-166">For more information, please see the following: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="003b9-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="003b9-167">RELATED LINKS</span></span>

[<span data-ttu-id="003b9-168">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="003b9-168">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="003b9-169">Get-AzOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="003b9-169">Get-AzOperationalInsightsLinkTargets</span></span>](./Get-AzOperationalInsightsLinkTargets.md)


