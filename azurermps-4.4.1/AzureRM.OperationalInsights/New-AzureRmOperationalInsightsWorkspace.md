---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 83f9ec56f5d33b65810da96364ab11dd4eb7c52a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562307"
---
# <span data-ttu-id="fdb4c-101">New-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="fdb4c-101">New-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="fdb4c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fdb4c-102">SYNOPSIS</span></span>
<span data-ttu-id="fdb4c-103">Создание рабочей области.</span><span class="sxs-lookup"><span data-stu-id="fdb4c-103">Creates a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdb4c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fdb4c-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-CustomerId] <Guid>] [[-Tags] <Hashtable>] [-RetentionInDays <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdb4c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fdb4c-105">DESCRIPTION</span></span>
<span data-ttu-id="fdb4c-106">Командлет **New-AzureRmOperationalInsightsWorkspace** создает рабочую область в заданной группе ресурсов и расположении.</span><span class="sxs-lookup"><span data-stu-id="fdb4c-106">The **New-AzureRmOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="fdb4c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fdb4c-107">EXAMPLES</span></span>

### <span data-ttu-id="fdb4c-108">Пример 1: создание рабочей области по имени</span><span class="sxs-lookup"><span data-stu-id="fdb4c-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="fdb4c-109">Эта команда создает стандартную рабочую область SKU с именем MyWorkspace в группе ресурсов с именем ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fdb4c-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="fdb4c-110">Пример 2: создание рабочей области и связывание ее с существующей учетной записью</span><span class="sxs-lookup"><span data-stu-id="fdb4c-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzureRmOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="fdb4c-111">Первая команда использует командлет Get-AzureRmOperationalInsightsLinkTargets для получения целевых данных ссылки на учетную запись, а затем сохраняет их в переменной $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="fdb4c-111">The first command uses the Get-AzureRmOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>

<span data-ttu-id="fdb4c-112">Вторая команда передает конечный объект ссылки на учетную запись в $OILinkTargets командлету **New-AzureRmOperationalInsightsWorkspace** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="fdb4c-112">The second command passes the first account link target in $OILinkTargets to the **New-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fdb4c-113">Команда создает стандартную рабочую область SKU с именем MyWorkspace, связанную с учетной записью первой оперативной аналитики в $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="fdb4c-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="fdb4c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fdb4c-114">PARAMETERS</span></span>

### <span data-ttu-id="fdb4c-115">-CustomerId</span><span class="sxs-lookup"><span data-stu-id="fdb4c-115">-CustomerId</span></span>
<span data-ttu-id="fdb4c-116">Указывает учетную запись, с которой будет связана эта Рабочая область.</span><span class="sxs-lookup"><span data-stu-id="fdb4c-116">Specifies the account to which this workspace will be linked.</span></span>
<span data-ttu-id="fdb4c-117">Кроме того, можно использовать командлет Get-AzureRmOperationalInsightsLinkTargets для перечисления потенциальных учетных записей.</span><span class="sxs-lookup"><span data-stu-id="fdb4c-117">The Get-AzureRmOperationalInsightsLinkTargets cmdlet can also be used to list the potential accounts.</span></span>

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

### <span data-ttu-id="fdb4c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="fdb4c-118">-Force</span></span>
<span data-ttu-id="fdb4c-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="fdb4c-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fdb4c-120">-Location</span><span class="sxs-lookup"><span data-stu-id="fdb4c-120">-Location</span></span>
<span data-ttu-id="fdb4c-121">Указывает место для создания рабочей области, например "Восток США" или "Западная Европа".</span><span class="sxs-lookup"><span data-stu-id="fdb4c-121">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

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

### <span data-ttu-id="fdb4c-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fdb4c-122">-Name</span></span>
<span data-ttu-id="fdb4c-123">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="fdb4c-123">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="fdb4c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdb4c-124">-ResourceGroupName</span></span>
<span data-ttu-id="fdb4c-125">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="fdb4c-125">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="fdb4c-126">Рабочая область будет создана в этой группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fdb4c-126">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="fdb4c-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="fdb4c-127">-Sku</span></span>
<span data-ttu-id="fdb4c-128">Указывает уровень обслуживания рабочей области.</span><span class="sxs-lookup"><span data-stu-id="fdb4c-128">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="fdb4c-129">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="fdb4c-129">Valid values are:</span></span> 

- <span data-ttu-id="fdb4c-130">бесплатно</span><span class="sxs-lookup"><span data-stu-id="fdb4c-130">free</span></span>
- <span data-ttu-id="fdb4c-131">Стандартная</span><span class="sxs-lookup"><span data-stu-id="fdb4c-131">standard</span></span>
- <span data-ttu-id="fdb4c-132">версию</span><span class="sxs-lookup"><span data-stu-id="fdb4c-132">premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: free, standard, premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb4c-133">-Теги</span><span class="sxs-lookup"><span data-stu-id="fdb4c-133">-Tags</span></span>
<span data-ttu-id="fdb4c-134">Указывает Теги ресурсов для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="fdb4c-134">Specifies the resource tags for the workspace.</span></span>

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

### <span data-ttu-id="fdb4c-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fdb4c-135">-Confirm</span></span>
<span data-ttu-id="fdb4c-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fdb4c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdb4c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdb4c-137">-WhatIf</span></span>
<span data-ttu-id="fdb4c-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fdb4c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdb4c-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fdb4c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdb4c-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdb4c-140">-DefaultProfile</span></span>
<span data-ttu-id="fdb4c-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fdb4c-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdb4c-142">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="fdb4c-142">-RetentionInDays</span></span>
<span data-ttu-id="fdb4c-143">Хранение данных рабочей области в днях.</span><span class="sxs-lookup"><span data-stu-id="fdb4c-143">The workspace data retention in days.</span></span> <span data-ttu-id="fdb4c-144">730 дней – это максимально допустимый объем номеров SKU.</span><span class="sxs-lookup"><span data-stu-id="fdb4c-144">730 days is the maximum allowed for all other Skus.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb4c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdb4c-145">CommonParameters</span></span>
<span data-ttu-id="fdb4c-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fdb4c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdb4c-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdb4c-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdb4c-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fdb4c-148">INPUTS</span></span>

## <span data-ttu-id="fdb4c-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fdb4c-149">OUTPUTS</span></span>

### <span data-ttu-id="fdb4c-150">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="fdb4c-150">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="fdb4c-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="fdb4c-151">NOTES</span></span>

## <span data-ttu-id="fdb4c-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fdb4c-152">RELATED LINKS</span></span>

[<span data-ttu-id="fdb4c-153">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="fdb4c-153">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="fdb4c-154">Get-AzureRmOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="fdb4c-154">Get-AzureRmOperationalInsightsLinkTargets</span></span>](./Get-AzureRmOperationalInsightsLinkTargets.md)


