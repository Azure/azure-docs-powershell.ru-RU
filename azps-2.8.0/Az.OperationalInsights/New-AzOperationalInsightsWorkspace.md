---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 8df5d54576b62caf93a92583eb6dcc9e39802f3d
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93913242"
---
# <span data-ttu-id="eee8c-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="eee8c-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="eee8c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eee8c-102">SYNOPSIS</span></span>
<span data-ttu-id="eee8c-103">Создание рабочей области.</span><span class="sxs-lookup"><span data-stu-id="eee8c-103">Creates a workspace.</span></span>

## <span data-ttu-id="eee8c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eee8c-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-CustomerId] <Guid>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eee8c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eee8c-105">DESCRIPTION</span></span>
<span data-ttu-id="eee8c-106">Командлет **New-AzOperationalInsightsWorkspace** создает рабочую область в заданной группе ресурсов и расположении.</span><span class="sxs-lookup"><span data-stu-id="eee8c-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="eee8c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eee8c-107">EXAMPLES</span></span>

### <span data-ttu-id="eee8c-108">Пример 1: создание рабочей области по имени</span><span class="sxs-lookup"><span data-stu-id="eee8c-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="eee8c-109">Эта команда создает стандартную рабочую область SKU с именем MyWorkspace в группе ресурсов с именем ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="eee8c-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="eee8c-110">Пример 2: создание рабочей области и связывание ее с существующей учетной записью</span><span class="sxs-lookup"><span data-stu-id="eee8c-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="eee8c-111">Первая команда использует командлет Get-AzOperationalInsightsLinkTargets для получения целевых данных ссылки на учетную запись, а затем сохраняет их в переменной $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="eee8c-111">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="eee8c-112">Вторая команда передает конечный объект ссылки на учетную запись в $OILinkTargets командлету **New-AzOperationalInsightsWorkspace** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="eee8c-112">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="eee8c-113">Команда создает стандартную рабочую область SKU с именем MyWorkspace, связанную с учетной записью первой оперативной аналитики в $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="eee8c-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="eee8c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eee8c-114">PARAMETERS</span></span>

### <span data-ttu-id="eee8c-115">-CustomerId</span><span class="sxs-lookup"><span data-stu-id="eee8c-115">-CustomerId</span></span>
<span data-ttu-id="eee8c-116">Указывает учетную запись, с которой будет связана эта Рабочая область.</span><span class="sxs-lookup"><span data-stu-id="eee8c-116">Specifies the account to which this workspace will be linked.</span></span>
<span data-ttu-id="eee8c-117">Кроме того, можно использовать командлет Get-AzOperationalInsightsLinkTargets для перечисления потенциальных учетных записей.</span><span class="sxs-lookup"><span data-stu-id="eee8c-117">The Get-AzOperationalInsightsLinkTargets cmdlet can also be used to list the potential accounts.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eee8c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eee8c-118">-DefaultProfile</span></span>
<span data-ttu-id="eee8c-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="eee8c-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eee8c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="eee8c-120">-Force</span></span>
<span data-ttu-id="eee8c-121">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="eee8c-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="eee8c-122">-Location</span><span class="sxs-lookup"><span data-stu-id="eee8c-122">-Location</span></span>
<span data-ttu-id="eee8c-123">Указывает место для создания рабочей области, например "Восток США" или "Западная Европа".</span><span class="sxs-lookup"><span data-stu-id="eee8c-123">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

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

### <span data-ttu-id="eee8c-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="eee8c-124">-Name</span></span>
<span data-ttu-id="eee8c-125">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="eee8c-125">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="eee8c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eee8c-126">-ResourceGroupName</span></span>
<span data-ttu-id="eee8c-127">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="eee8c-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="eee8c-128">Рабочая область будет создана в этой группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eee8c-128">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="eee8c-129">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="eee8c-129">-RetentionInDays</span></span>
<span data-ttu-id="eee8c-130">Хранение данных рабочей области в днях.</span><span class="sxs-lookup"><span data-stu-id="eee8c-130">The workspace data retention in days.</span></span> <span data-ttu-id="eee8c-131">730 дней – это максимально допустимое количество номеров SKU.</span><span class="sxs-lookup"><span data-stu-id="eee8c-131">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="eee8c-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="eee8c-132">-Sku</span></span>
<span data-ttu-id="eee8c-133">Указывает уровень обслуживания рабочей области.</span><span class="sxs-lookup"><span data-stu-id="eee8c-133">Specifies the service tier of the workspace.</span></span> <span data-ttu-id="eee8c-134">Дополнительные сведения о том, какое значение использовать, можно найти в этой видеосвязи https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers .</span><span class="sxs-lookup"><span data-stu-id="eee8c-134">For more information regarding which value to use please check https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers.</span></span>
<span data-ttu-id="eee8c-135">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="eee8c-135">Valid values are:</span></span>
- <span data-ttu-id="eee8c-136">бесплатно</span><span class="sxs-lookup"><span data-stu-id="eee8c-136">free</span></span>
- <span data-ttu-id="eee8c-137">pergb2018</span><span class="sxs-lookup"><span data-stu-id="eee8c-137">pergb2018</span></span>
- <span data-ttu-id="eee8c-138">pernode</span><span class="sxs-lookup"><span data-stu-id="eee8c-138">pernode</span></span>
- <span data-ttu-id="eee8c-139">версию</span><span class="sxs-lookup"><span data-stu-id="eee8c-139">premium</span></span>
- <span data-ttu-id="eee8c-140">отдельно</span><span class="sxs-lookup"><span data-stu-id="eee8c-140">standalone</span></span>
- <span data-ttu-id="eee8c-141">Стандартная</span><span class="sxs-lookup"><span data-stu-id="eee8c-141">standard</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: free, pergb2018, pernode, premium, standalone, standard

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eee8c-142">-Тег</span><span class="sxs-lookup"><span data-stu-id="eee8c-142">-Tag</span></span>
<span data-ttu-id="eee8c-143">Теги ресурсов для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="eee8c-143">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="eee8c-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eee8c-144">-Confirm</span></span>
<span data-ttu-id="eee8c-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eee8c-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eee8c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eee8c-146">-WhatIf</span></span>
<span data-ttu-id="eee8c-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eee8c-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eee8c-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eee8c-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eee8c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eee8c-149">CommonParameters</span></span>
<span data-ttu-id="eee8c-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eee8c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eee8c-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eee8c-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eee8c-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eee8c-152">INPUTS</span></span>

### <span data-ttu-id="eee8c-153">System. String</span><span class="sxs-lookup"><span data-stu-id="eee8c-153">System.String</span></span>

### <span data-ttu-id="eee8c-154">System. Nullable "1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="eee8c-154">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="eee8c-155">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="eee8c-155">System.Collections.Hashtable</span></span>

### <span data-ttu-id="eee8c-156">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="eee8c-156">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="eee8c-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eee8c-157">OUTPUTS</span></span>

### <span data-ttu-id="eee8c-158">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="eee8c-158">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="eee8c-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="eee8c-159">NOTES</span></span>

<span data-ttu-id="eee8c-160">Была выпущена новая модель ценообразования.</span><span class="sxs-lookup"><span data-stu-id="eee8c-160">A new pricing model has been released.</span></span> <span data-ttu-id="eee8c-161">Если вы являетесь поставщиком службы криптографии, это означает, что для SKU вам нужно использовать "standalone".</span><span class="sxs-lookup"><span data-stu-id="eee8c-161">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="eee8c-162">В фоновом режиме номер SKU изменится на pergb2018.</span><span class="sxs-lookup"><span data-stu-id="eee8c-162">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="eee8c-163">Дополнительные сведения можно найти в следующих примерах: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="eee8c-163">For more information, please see the following: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="eee8c-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eee8c-164">RELATED LINKS</span></span>

[<span data-ttu-id="eee8c-165">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="eee8c-165">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)
