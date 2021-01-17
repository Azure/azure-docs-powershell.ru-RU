---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 5abfd1a02687eb2715ad924510176748e04e56cd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413511"
---
# <span data-ttu-id="67e17-101">Set-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="67e17-101">Set-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="67e17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67e17-102">SYNOPSIS</span></span>
<span data-ttu-id="67e17-103">Обновляет рабочее пространство.</span><span class="sxs-lookup"><span data-stu-id="67e17-103">Updates a workspace.</span></span>

## <span data-ttu-id="67e17-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="67e17-104">SYNTAX</span></span>

### <span data-ttu-id="67e17-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="67e17-105">ByName (Default)</span></span>
```
Set-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-PublicNetworkAccessForIngestion <String>] [-PublicNetworkAccessForQuery <String>] [<CommonParameters>]
```

### <span data-ttu-id="67e17-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="67e17-106">ByObject</span></span>
```
Set-AzOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-PublicNetworkAccessForIngestion <String>] [-PublicNetworkAccessForQuery <String>] [<CommonParameters>]
```

## <span data-ttu-id="67e17-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67e17-107">DESCRIPTION</span></span>
<span data-ttu-id="67e17-108">Командлет **Set-AzOperationalInsightsWorkspace** изменяет конфигурацию рабочей области.</span><span class="sxs-lookup"><span data-stu-id="67e17-108">The **Set-AzOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="67e17-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="67e17-109">EXAMPLES</span></span>

### <span data-ttu-id="67e17-110">Пример 1. Изменение имени рабочей области</span><span class="sxs-lookup"><span data-stu-id="67e17-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="67e17-111">Эта команда изменяет SKU и теги рабочей области MyWorkspace в группе ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="67e17-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="67e17-112">Пример 2. Обновление рабочей области с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="67e17-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="67e17-113">Эта команда использует командлет Get-AzOperationalInsightsWorkspace для получения рабочей области MyWorkSpace, а затем передает ее **командлету Set-AzOperationalInsightsWorkspace** с помощью оператора конвейера, чтобы установить для SKU premium.</span><span class="sxs-lookup"><span data-stu-id="67e17-113">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="67e17-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67e17-114">PARAMETERS</span></span>

### <span data-ttu-id="67e17-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67e17-115">-DefaultProfile</span></span>
<span data-ttu-id="67e17-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="67e17-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67e17-117">-Name</span><span class="sxs-lookup"><span data-stu-id="67e17-117">-Name</span></span>
<span data-ttu-id="67e17-118">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="67e17-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="67e17-119">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="67e17-119">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="67e17-120">Тип сетевого доступа для доступа к рабочему пространству.</span><span class="sxs-lookup"><span data-stu-id="67e17-120">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="67e17-121">Значение должно быть включено или отключено</span><span class="sxs-lookup"><span data-stu-id="67e17-121">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67e17-122">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="67e17-122">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="67e17-123">Тип доступа к сети для запроса рабочей области.</span><span class="sxs-lookup"><span data-stu-id="67e17-123">The network access type for accessing workspace query.</span></span> <span data-ttu-id="67e17-124">Значение должно быть включено или отключено</span><span class="sxs-lookup"><span data-stu-id="67e17-124">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67e17-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67e17-125">-ResourceGroupName</span></span>
<span data-ttu-id="67e17-126">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="67e17-126">Specifies the Azure resource group name.</span></span>

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

### <span data-ttu-id="67e17-127">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="67e17-127">-RetentionInDays</span></span>
<span data-ttu-id="67e17-128">Хранение данных рабочей области в днях.</span><span class="sxs-lookup"><span data-stu-id="67e17-128">The workspace data retention in days.</span></span> <span data-ttu-id="67e17-129">730 дней — это максимальное значение для всех остальных skus</span><span class="sxs-lookup"><span data-stu-id="67e17-129">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="67e17-130">-SKU</span><span class="sxs-lookup"><span data-stu-id="67e17-130">-Sku</span></span>
<span data-ttu-id="67e17-131">Определяет уровень обслуживания рабочей области.</span><span class="sxs-lookup"><span data-stu-id="67e17-131">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="67e17-132">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="67e17-132">Valid values are:</span></span> 
- <span data-ttu-id="67e17-133">бесплатно</span><span class="sxs-lookup"><span data-stu-id="67e17-133">free</span></span>
- <span data-ttu-id="67e17-134">стандартный</span><span class="sxs-lookup"><span data-stu-id="67e17-134">standard</span></span>
- <span data-ttu-id="67e17-135">premium</span><span class="sxs-lookup"><span data-stu-id="67e17-135">premium</span></span>
- <span data-ttu-id="67e17-136">pernode</span><span class="sxs-lookup"><span data-stu-id="67e17-136">pernode</span></span>
- <span data-ttu-id="67e17-137">автономный</span><span class="sxs-lookup"><span data-stu-id="67e17-137">standalone</span></span>
- <span data-ttu-id="67e17-138">pergb2018</span><span class="sxs-lookup"><span data-stu-id="67e17-138">pergb2018</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: free, standard, premium, pernode, standalone, pergb2018

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67e17-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="67e17-139">-Tag</span></span>
<span data-ttu-id="67e17-140">Теги ресурсов для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="67e17-140">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="67e17-141">-Workspace</span><span class="sxs-lookup"><span data-stu-id="67e17-141">-Workspace</span></span>
<span data-ttu-id="67e17-142">Определяет обновляемую область.</span><span class="sxs-lookup"><span data-stu-id="67e17-142">Specifies the workspace to be updated.</span></span>

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

### <span data-ttu-id="67e17-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67e17-143">CommonParameters</span></span>
<span data-ttu-id="67e17-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67e17-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67e17-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67e17-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67e17-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67e17-146">INPUTS</span></span>

### <span data-ttu-id="67e17-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="67e17-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="67e17-148">System.String</span><span class="sxs-lookup"><span data-stu-id="67e17-148">System.String</span></span>

### <span data-ttu-id="67e17-149">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="67e17-149">System.Collections.Hashtable</span></span>

### <span data-ttu-id="67e17-150">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="67e17-150">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="67e17-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="67e17-151">OUTPUTS</span></span>

### <span data-ttu-id="67e17-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="67e17-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="67e17-153">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="67e17-153">NOTES</span></span>

## <span data-ttu-id="67e17-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67e17-154">RELATED LINKS</span></span>

[<span data-ttu-id="67e17-155">Azure Operational Insights Cmdlets</span><span class="sxs-lookup"><span data-stu-id="67e17-155">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="67e17-156">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="67e17-156">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


