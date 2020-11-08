---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 3d85bcbf5352c06e379ac317cde052f3e744c10d
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94077279"
---
# <span data-ttu-id="1f06c-101">Set-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="1f06c-101">Set-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="1f06c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1f06c-102">SYNOPSIS</span></span>
<span data-ttu-id="1f06c-103">Обновляет рабочую область.</span><span class="sxs-lookup"><span data-stu-id="1f06c-103">Updates a workspace.</span></span>

## <span data-ttu-id="1f06c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1f06c-104">SYNTAX</span></span>

### <span data-ttu-id="1f06c-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1f06c-105">ByName (Default)</span></span>
```
Set-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1f06c-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="1f06c-106">ByObject</span></span>
```
Set-AzOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f06c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f06c-107">DESCRIPTION</span></span>
<span data-ttu-id="1f06c-108">Командлет **Set-AzOperationalInsightsWorkspace** изменяет конфигурацию рабочей области.</span><span class="sxs-lookup"><span data-stu-id="1f06c-108">The **Set-AzOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="1f06c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1f06c-109">EXAMPLES</span></span>

### <span data-ttu-id="1f06c-110">Пример 1: изменение рабочей области по имени</span><span class="sxs-lookup"><span data-stu-id="1f06c-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="1f06c-111">Эта команда изменяет SKU и теги рабочей области с именем MyWorkspace в группе ресурсов с именем ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1f06c-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="1f06c-112">Пример 2: Обновление рабочей области с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="1f06c-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="1f06c-113">Эта команда использует командлет Get-AzOperationalInsightsWorkspace, чтобы получить рабочую область с именем MyWorkSpace, а затем передает ее командлету **Set-AzOperationalInsightsWorkspace** с помощью оператора конвейера, чтобы установить для SKU значение Premium.</span><span class="sxs-lookup"><span data-stu-id="1f06c-113">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="1f06c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1f06c-114">PARAMETERS</span></span>

### <span data-ttu-id="1f06c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f06c-115">-DefaultProfile</span></span>
<span data-ttu-id="1f06c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1f06c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f06c-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1f06c-117">-Name</span></span>
<span data-ttu-id="1f06c-118">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="1f06c-118">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f06c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f06c-119">-ResourceGroupName</span></span>
<span data-ttu-id="1f06c-120">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="1f06c-120">Specifies the Azure resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f06c-121">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="1f06c-121">-RetentionInDays</span></span>
<span data-ttu-id="1f06c-122">Хранение данных рабочей области в днях.</span><span class="sxs-lookup"><span data-stu-id="1f06c-122">The workspace data retention in days.</span></span> <span data-ttu-id="1f06c-123">730 дней – это максимально допустимое количество номеров SKU.</span><span class="sxs-lookup"><span data-stu-id="1f06c-123">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="1f06c-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="1f06c-124">-Sku</span></span>
<span data-ttu-id="1f06c-125">Указывает уровень обслуживания рабочей области.</span><span class="sxs-lookup"><span data-stu-id="1f06c-125">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="1f06c-126">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="1f06c-126">Valid values are:</span></span> 
- <span data-ttu-id="1f06c-127">бесплатно</span><span class="sxs-lookup"><span data-stu-id="1f06c-127">free</span></span>
- <span data-ttu-id="1f06c-128">Стандартная</span><span class="sxs-lookup"><span data-stu-id="1f06c-128">standard</span></span>
- <span data-ttu-id="1f06c-129">версию</span><span class="sxs-lookup"><span data-stu-id="1f06c-129">premium</span></span>

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

### <span data-ttu-id="1f06c-130">-Тег</span><span class="sxs-lookup"><span data-stu-id="1f06c-130">-Tag</span></span>
<span data-ttu-id="1f06c-131">Теги ресурсов для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="1f06c-131">The resource tags for the workspace.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f06c-132">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="1f06c-132">-Workspace</span></span>
<span data-ttu-id="1f06c-133">Указывает рабочую область, которая будет обновлена.</span><span class="sxs-lookup"><span data-stu-id="1f06c-133">Specifies the workspace to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f06c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f06c-134">CommonParameters</span></span>
<span data-ttu-id="1f06c-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1f06c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f06c-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f06c-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f06c-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1f06c-137">INPUTS</span></span>

### <span data-ttu-id="1f06c-138">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="1f06c-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="1f06c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1f06c-139">System.String</span></span>

### <span data-ttu-id="1f06c-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1f06c-140">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1f06c-141">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1f06c-141">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="1f06c-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f06c-142">OUTPUTS</span></span>

### <span data-ttu-id="1f06c-143">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="1f06c-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="1f06c-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="1f06c-144">NOTES</span></span>

## <span data-ttu-id="1f06c-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f06c-145">RELATED LINKS</span></span>

[<span data-ttu-id="1f06c-146">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="1f06c-146">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="1f06c-147">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="1f06c-147">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


