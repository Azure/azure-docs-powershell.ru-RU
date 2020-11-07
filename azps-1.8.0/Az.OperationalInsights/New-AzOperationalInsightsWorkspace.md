---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 863b83cbab64d791e55f8cfc2719d66be64fcac6
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93913197"
---
# <span data-ttu-id="0b672-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="0b672-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="0b672-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0b672-102">SYNOPSIS</span></span>
<span data-ttu-id="0b672-103">Создание рабочей области.</span><span class="sxs-lookup"><span data-stu-id="0b672-103">Creates a workspace.</span></span>

## <span data-ttu-id="0b672-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0b672-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-CustomerId] <Guid>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b672-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b672-105">DESCRIPTION</span></span>
<span data-ttu-id="0b672-106">Командлет **New-AzOperationalInsightsWorkspace** создает рабочую область в заданной группе ресурсов и расположении.</span><span class="sxs-lookup"><span data-stu-id="0b672-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="0b672-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0b672-107">EXAMPLES</span></span>

### <span data-ttu-id="0b672-108">Пример 1: создание рабочей области по имени</span><span class="sxs-lookup"><span data-stu-id="0b672-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="0b672-109">Эта команда создает стандартную рабочую область SKU с именем MyWorkspace в группе ресурсов с именем ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0b672-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="0b672-110">Пример 2: создание рабочей области и связывание ее с существующей учетной записью</span><span class="sxs-lookup"><span data-stu-id="0b672-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="0b672-111">Первая команда использует командлет Get-AzOperationalInsightsLinkTargets для получения целевых данных ссылки на учетную запись, а затем сохраняет их в переменной $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="0b672-111">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="0b672-112">Вторая команда передает конечный объект ссылки на учетную запись в $OILinkTargets командлету **New-AzOperationalInsightsWorkspace** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="0b672-112">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0b672-113">Команда создает стандартную рабочую область SKU с именем MyWorkspace, связанную с учетной записью первой оперативной аналитики в $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="0b672-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="0b672-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0b672-114">PARAMETERS</span></span>

### <span data-ttu-id="0b672-115">-CustomerId</span><span class="sxs-lookup"><span data-stu-id="0b672-115">-CustomerId</span></span>
<span data-ttu-id="0b672-116">Указывает учетную запись, с которой будет связана эта Рабочая область.</span><span class="sxs-lookup"><span data-stu-id="0b672-116">Specifies the account to which this workspace will be linked.</span></span>
<span data-ttu-id="0b672-117">Кроме того, можно использовать командлет Get-AzOperationalInsightsLinkTargets для перечисления потенциальных учетных записей.</span><span class="sxs-lookup"><span data-stu-id="0b672-117">The Get-AzOperationalInsightsLinkTargets cmdlet can also be used to list the potential accounts.</span></span>

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

### <span data-ttu-id="0b672-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b672-118">-DefaultProfile</span></span>
<span data-ttu-id="0b672-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0b672-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b672-120">-Force</span><span class="sxs-lookup"><span data-stu-id="0b672-120">-Force</span></span>
<span data-ttu-id="0b672-121">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="0b672-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0b672-122">-Location</span><span class="sxs-lookup"><span data-stu-id="0b672-122">-Location</span></span>
<span data-ttu-id="0b672-123">Указывает место для создания рабочей области, например "Восток США" или "Западная Европа".</span><span class="sxs-lookup"><span data-stu-id="0b672-123">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

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

### <span data-ttu-id="0b672-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0b672-124">-Name</span></span>
<span data-ttu-id="0b672-125">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="0b672-125">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="0b672-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b672-126">-ResourceGroupName</span></span>
<span data-ttu-id="0b672-127">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="0b672-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0b672-128">Рабочая область будет создана в этой группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0b672-128">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="0b672-129">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="0b672-129">-RetentionInDays</span></span>
<span data-ttu-id="0b672-130">Хранение данных рабочей области в днях.</span><span class="sxs-lookup"><span data-stu-id="0b672-130">The workspace data retention in days.</span></span> <span data-ttu-id="0b672-131">730 дней – это максимально допустимое количество номеров SKU.</span><span class="sxs-lookup"><span data-stu-id="0b672-131">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="0b672-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="0b672-132">-Sku</span></span>
<span data-ttu-id="0b672-133">Указывает уровень обслуживания рабочей области.</span><span class="sxs-lookup"><span data-stu-id="0b672-133">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="0b672-134">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="0b672-134">Valid values are:</span></span>
- <span data-ttu-id="0b672-135">бесплатно</span><span class="sxs-lookup"><span data-stu-id="0b672-135">free</span></span>
- <span data-ttu-id="0b672-136">Стандартная</span><span class="sxs-lookup"><span data-stu-id="0b672-136">standard</span></span>
- <span data-ttu-id="0b672-137">отдельно</span><span class="sxs-lookup"><span data-stu-id="0b672-137">standalone</span></span>
- <span data-ttu-id="0b672-138">версию</span><span class="sxs-lookup"><span data-stu-id="0b672-138">premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: free, standard, premium, pernode, standalone

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b672-139">-Тег</span><span class="sxs-lookup"><span data-stu-id="0b672-139">-Tag</span></span>
<span data-ttu-id="0b672-140">Теги ресурсов для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="0b672-140">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="0b672-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b672-141">-Confirm</span></span>
<span data-ttu-id="0b672-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0b672-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b672-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b672-143">-WhatIf</span></span>
<span data-ttu-id="0b672-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0b672-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b672-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0b672-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b672-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b672-146">CommonParameters</span></span>
<span data-ttu-id="0b672-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0b672-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b672-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b672-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b672-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0b672-149">INPUTS</span></span>

### <span data-ttu-id="0b672-150">System. String</span><span class="sxs-lookup"><span data-stu-id="0b672-150">System.String</span></span>

### <span data-ttu-id="0b672-151">System. Nullable "1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0b672-151">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0b672-152">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0b672-152">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0b672-153">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0b672-153">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="0b672-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b672-154">OUTPUTS</span></span>

### <span data-ttu-id="0b672-155">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="0b672-155">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="0b672-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="0b672-156">NOTES</span></span>

<span data-ttu-id="0b672-157">Была выпущена новая модель ценообразования.</span><span class="sxs-lookup"><span data-stu-id="0b672-157">A new pricing model has been released.</span></span> <span data-ttu-id="0b672-158">Если вы являетесь поставщиком службы криптографии, это означает, что для SKU вам нужно использовать "standalone".</span><span class="sxs-lookup"><span data-stu-id="0b672-158">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="0b672-159">В фоновом режиме номер SKU изменится на pergb2018.</span><span class="sxs-lookup"><span data-stu-id="0b672-159">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="0b672-160">Дополнительные сведения можно найти в следующих примерах: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="0b672-160">For more information, please see the following: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="0b672-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0b672-161">RELATED LINKS</span></span>

[<span data-ttu-id="0b672-162">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="0b672-162">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)
