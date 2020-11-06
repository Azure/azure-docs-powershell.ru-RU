---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 0ba43a38763252275d7461f11cc4db574720ba5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566155"
---
# <span data-ttu-id="b8dde-101">New-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="b8dde-101">New-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="b8dde-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b8dde-102">SYNOPSIS</span></span>
<span data-ttu-id="b8dde-103">Создание рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b8dde-103">Creates a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8dde-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b8dde-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-CustomerId] <Guid>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8dde-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8dde-105">DESCRIPTION</span></span>
<span data-ttu-id="b8dde-106">Командлет **New-AzureRmOperationalInsightsWorkspace** создает рабочую область в заданной группе ресурсов и расположении.</span><span class="sxs-lookup"><span data-stu-id="b8dde-106">The **New-AzureRmOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="b8dde-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b8dde-107">EXAMPLES</span></span>

### <span data-ttu-id="b8dde-108">Пример 1: создание рабочей области по имени</span><span class="sxs-lookup"><span data-stu-id="b8dde-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="b8dde-109">Эта команда создает стандартную рабочую область SKU с именем MyWorkspace в группе ресурсов с именем ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b8dde-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="b8dde-110">Пример 2: создание рабочей области и связывание ее с существующей учетной записью</span><span class="sxs-lookup"><span data-stu-id="b8dde-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzureRmOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="b8dde-111">Первая команда использует командлет Get-AzureRmOperationalInsightsLinkTargets для получения целевых данных ссылки на учетную запись, а затем сохраняет их в переменной $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="b8dde-111">The first command uses the Get-AzureRmOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>

<span data-ttu-id="b8dde-112">Вторая команда передает конечный объект ссылки на учетную запись в $OILinkTargets командлету **New-AzureRmOperationalInsightsWorkspace** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="b8dde-112">The second command passes the first account link target in $OILinkTargets to the **New-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b8dde-113">Команда создает стандартную рабочую область SKU с именем MyWorkspace, связанную с учетной записью первой оперативной аналитики в $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="b8dde-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="b8dde-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b8dde-114">PARAMETERS</span></span>

### <span data-ttu-id="b8dde-115">-CustomerId</span><span class="sxs-lookup"><span data-stu-id="b8dde-115">-CustomerId</span></span>
<span data-ttu-id="b8dde-116">Указывает учетную запись, с которой будет связана эта Рабочая область.</span><span class="sxs-lookup"><span data-stu-id="b8dde-116">Specifies the account to which this workspace will be linked.</span></span>
<span data-ttu-id="b8dde-117">Кроме того, можно использовать командлет Get-AzureRmOperationalInsightsLinkTargets для перечисления потенциальных учетных записей.</span><span class="sxs-lookup"><span data-stu-id="b8dde-117">The Get-AzureRmOperationalInsightsLinkTargets cmdlet can also be used to list the potential accounts.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8dde-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8dde-118">-DefaultProfile</span></span>
<span data-ttu-id="b8dde-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b8dde-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8dde-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b8dde-120">-Force</span></span>
<span data-ttu-id="b8dde-121">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="b8dde-121">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8dde-122">-Location</span><span class="sxs-lookup"><span data-stu-id="b8dde-122">-Location</span></span>
<span data-ttu-id="b8dde-123">Указывает место для создания рабочей области, например "Восток США" или "Западная Европа".</span><span class="sxs-lookup"><span data-stu-id="b8dde-123">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8dde-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b8dde-124">-Name</span></span>
<span data-ttu-id="b8dde-125">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b8dde-125">Specifies the name of the workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8dde-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8dde-126">-ResourceGroupName</span></span>
<span data-ttu-id="b8dde-127">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="b8dde-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b8dde-128">Рабочая область будет создана в этой группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b8dde-128">The workspace is created in this resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8dde-129">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="b8dde-129">-RetentionInDays</span></span>
<span data-ttu-id="b8dde-130">Хранение данных рабочей области в днях.</span><span class="sxs-lookup"><span data-stu-id="b8dde-130">The workspace data retention in days.</span></span> <span data-ttu-id="b8dde-131">730 дней – это максимально допустимое количество номеров SKU.</span><span class="sxs-lookup"><span data-stu-id="b8dde-131">730 days is the maximum allowed for all other Skus</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8dde-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="b8dde-132">-Sku</span></span>
<span data-ttu-id="b8dde-133">Указывает уровень обслуживания рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b8dde-133">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="b8dde-134">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="b8dde-134">Valid values are:</span></span> 

- <span data-ttu-id="b8dde-135">бесплатно</span><span class="sxs-lookup"><span data-stu-id="b8dde-135">free</span></span>
- <span data-ttu-id="b8dde-136">Стандартная</span><span class="sxs-lookup"><span data-stu-id="b8dde-136">standard</span></span>
- <span data-ttu-id="b8dde-137">версию</span><span class="sxs-lookup"><span data-stu-id="b8dde-137">premium</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: free, standard, premium, pernode, standalone

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8dde-138">-Тег</span><span class="sxs-lookup"><span data-stu-id="b8dde-138">-Tag</span></span>
<span data-ttu-id="b8dde-139">Теги ресурсов для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b8dde-139">The resource tags for the workspace.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8dde-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8dde-140">-Confirm</span></span>
<span data-ttu-id="b8dde-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b8dde-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8dde-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8dde-142">-WhatIf</span></span>
<span data-ttu-id="b8dde-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b8dde-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8dde-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b8dde-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8dde-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8dde-145">CommonParameters</span></span>
<span data-ttu-id="b8dde-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b8dde-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8dde-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8dde-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8dde-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b8dde-148">INPUTS</span></span>

### <span data-ttu-id="b8dde-149">Ничего</span><span class="sxs-lookup"><span data-stu-id="b8dde-149">None</span></span>
<span data-ttu-id="b8dde-150">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="b8dde-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b8dde-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8dde-151">OUTPUTS</span></span>

### <span data-ttu-id="b8dde-152">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="b8dde-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="b8dde-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="b8dde-153">NOTES</span></span>

## <span data-ttu-id="b8dde-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8dde-154">RELATED LINKS</span></span>

[<span data-ttu-id="b8dde-155">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="b8dde-155">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="b8dde-156">Get-AzureRmOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="b8dde-156">Get-AzureRmOperationalInsightsLinkTargets</span></span>](./Get-AzureRmOperationalInsightsLinkTargets.md)


