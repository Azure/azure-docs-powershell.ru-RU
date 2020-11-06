---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: a4584e4c0fc64920fbffb7e3d685a9be3ac04ad1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563435"
---
# <span data-ttu-id="f6a19-101">Set-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="f6a19-101">Set-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="f6a19-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f6a19-102">SYNOPSIS</span></span>
<span data-ttu-id="f6a19-103">Обновляет рабочую область.</span><span class="sxs-lookup"><span data-stu-id="f6a19-103">Updates a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6a19-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f6a19-104">SYNTAX</span></span>

### <span data-ttu-id="f6a19-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f6a19-105">ByName (Default)</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f6a19-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="f6a19-106">ByObject</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6a19-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6a19-107">DESCRIPTION</span></span>
<span data-ttu-id="f6a19-108">Командлет **Set-AzureRmOperationalInsightsWorkspace** изменяет конфигурацию рабочей области.</span><span class="sxs-lookup"><span data-stu-id="f6a19-108">The **Set-AzureRmOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="f6a19-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f6a19-109">EXAMPLES</span></span>

### <span data-ttu-id="f6a19-110">Пример 1: изменение рабочей области по имени</span><span class="sxs-lookup"><span data-stu-id="f6a19-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="f6a19-111">Эта команда изменяет SKU и теги рабочей области с именем MyWorkspace в группе ресурсов с именем ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f6a19-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="f6a19-112">Пример 2: Обновление рабочей области с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="f6a19-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzureRmOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="f6a19-113">Эта команда использует командлет Get-AzureRmOperationalInsightsWorkspace, чтобы получить рабочую область с именем MyWorkSpace, а затем передает ее командлету **Set-AzureRmOperationalInsightsWorkspace** с помощью оператора конвейера, чтобы установить для SKU значение Premium.</span><span class="sxs-lookup"><span data-stu-id="f6a19-113">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="f6a19-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f6a19-114">PARAMETERS</span></span>

### <span data-ttu-id="f6a19-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6a19-115">-DefaultProfile</span></span>
<span data-ttu-id="f6a19-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f6a19-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6a19-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f6a19-117">-Name</span></span>
<span data-ttu-id="f6a19-118">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="f6a19-118">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6a19-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6a19-119">-ResourceGroupName</span></span>
<span data-ttu-id="f6a19-120">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f6a19-120">Specifies the Azure resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6a19-121">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="f6a19-121">-RetentionInDays</span></span>
<span data-ttu-id="f6a19-122">Хранение данных рабочей области в днях.</span><span class="sxs-lookup"><span data-stu-id="f6a19-122">The workspace data retention in days.</span></span> <span data-ttu-id="f6a19-123">730 дней – это максимально допустимое количество номеров SKU.</span><span class="sxs-lookup"><span data-stu-id="f6a19-123">730 days is the maximum allowed for all other Skus</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6a19-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="f6a19-124">-Sku</span></span>
<span data-ttu-id="f6a19-125">Указывает уровень обслуживания рабочей области.</span><span class="sxs-lookup"><span data-stu-id="f6a19-125">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="f6a19-126">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="f6a19-126">Valid values are:</span></span> 

- <span data-ttu-id="f6a19-127">бесплатно</span><span class="sxs-lookup"><span data-stu-id="f6a19-127">free</span></span>
- <span data-ttu-id="f6a19-128">Стандартная</span><span class="sxs-lookup"><span data-stu-id="f6a19-128">standard</span></span>
- <span data-ttu-id="f6a19-129">версию</span><span class="sxs-lookup"><span data-stu-id="f6a19-129">premium</span></span>

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

### <span data-ttu-id="f6a19-130">-Тег</span><span class="sxs-lookup"><span data-stu-id="f6a19-130">-Tag</span></span>
<span data-ttu-id="f6a19-131">Теги ресурсов для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="f6a19-131">The resource tags for the workspace.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6a19-132">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="f6a19-132">-Workspace</span></span>
<span data-ttu-id="f6a19-133">Указывает рабочую область, которая будет обновлена.</span><span class="sxs-lookup"><span data-stu-id="f6a19-133">Specifies the workspace to be updated.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6a19-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6a19-134">CommonParameters</span></span>
<span data-ttu-id="f6a19-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f6a19-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6a19-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6a19-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6a19-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f6a19-137">INPUTS</span></span>

### <span data-ttu-id="f6a19-138">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="f6a19-138">PSWorkspace</span></span>
<span data-ttu-id="f6a19-139">Параметр "Рабочая область" принимает значение типа "PSWorkspace" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="f6a19-139">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="f6a19-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6a19-140">OUTPUTS</span></span>

### <span data-ttu-id="f6a19-141">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="f6a19-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="f6a19-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="f6a19-142">NOTES</span></span>

## <span data-ttu-id="f6a19-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6a19-143">RELATED LINKS</span></span>

[<span data-ttu-id="f6a19-144">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="f6a19-144">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="f6a19-145">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="f6a19-145">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


