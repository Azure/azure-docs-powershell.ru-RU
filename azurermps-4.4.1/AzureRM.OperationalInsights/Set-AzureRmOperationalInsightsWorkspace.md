---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: e24597d25fffdc1b516c5a18cf011f7222d288c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559583"
---
# <span data-ttu-id="1b502-101">Set-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="1b502-101">Set-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="1b502-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1b502-102">SYNOPSIS</span></span>
<span data-ttu-id="1b502-103">Обновляет рабочую область.</span><span class="sxs-lookup"><span data-stu-id="1b502-103">Updates a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b502-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1b502-104">SYNTAX</span></span>

### <span data-ttu-id="1b502-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1b502-105">ByName (Default)</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tags] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b502-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="1b502-106">ByObject</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tags] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b502-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b502-107">DESCRIPTION</span></span>
<span data-ttu-id="1b502-108">Командлет **Set-AzureRmOperationalInsightsWorkspace** изменяет конфигурацию рабочей области.</span><span class="sxs-lookup"><span data-stu-id="1b502-108">The **Set-AzureRmOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="1b502-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1b502-109">EXAMPLES</span></span>

### <span data-ttu-id="1b502-110">Пример 1: изменение рабочей области по имени</span><span class="sxs-lookup"><span data-stu-id="1b502-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="1b502-111">Эта команда изменяет SKU и теги рабочей области с именем MyWorkspace в группе ресурсов с именем ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1b502-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="1b502-112">Пример 2: Обновление рабочей области с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="1b502-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzureRmOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="1b502-113">Эта команда использует командлет Get-AzureRmOperationalInsightsWorkspace, чтобы получить рабочую область с именем MyWorkSpace, а затем передает ее командлету **Set-AzureRmOperationalInsightsWorkspace** с помощью оператора конвейера, чтобы установить для SKU значение Premium.</span><span class="sxs-lookup"><span data-stu-id="1b502-113">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="1b502-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1b502-114">PARAMETERS</span></span>

### <span data-ttu-id="1b502-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1b502-115">-Name</span></span>
<span data-ttu-id="1b502-116">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="1b502-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="1b502-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b502-117">-ResourceGroupName</span></span>
<span data-ttu-id="1b502-118">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="1b502-118">Specifies the Azure resource group name.</span></span>

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

### <span data-ttu-id="1b502-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="1b502-119">-Sku</span></span>
<span data-ttu-id="1b502-120">Указывает уровень обслуживания рабочей области.</span><span class="sxs-lookup"><span data-stu-id="1b502-120">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="1b502-121">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="1b502-121">Valid values are:</span></span> 

- <span data-ttu-id="1b502-122">бесплатно</span><span class="sxs-lookup"><span data-stu-id="1b502-122">free</span></span>
- <span data-ttu-id="1b502-123">Стандартная</span><span class="sxs-lookup"><span data-stu-id="1b502-123">standard</span></span>
- <span data-ttu-id="1b502-124">версию</span><span class="sxs-lookup"><span data-stu-id="1b502-124">premium</span></span>

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

### <span data-ttu-id="1b502-125">-Теги</span><span class="sxs-lookup"><span data-stu-id="1b502-125">-Tags</span></span>
<span data-ttu-id="1b502-126">Указывает Теги ресурсов для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="1b502-126">Specifies the resource tags for the workspace.</span></span>

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

### <span data-ttu-id="1b502-127">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="1b502-127">-Workspace</span></span>
<span data-ttu-id="1b502-128">Указывает рабочую область, которая будет обновлена.</span><span class="sxs-lookup"><span data-stu-id="1b502-128">Specifies the workspace to be updated.</span></span>

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

### <span data-ttu-id="1b502-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b502-129">-DefaultProfile</span></span>
<span data-ttu-id="1b502-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1b502-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b502-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="1b502-131">-RetentionInDays</span></span>
<span data-ttu-id="1b502-132">Хранение данных рабочей области в днях.</span><span class="sxs-lookup"><span data-stu-id="1b502-132">The workspace data retention in days.</span></span> <span data-ttu-id="1b502-133">730 дней – это максимально допустимый объем номеров SKU.</span><span class="sxs-lookup"><span data-stu-id="1b502-133">730 days is the maximum allowed for all other Skus.</span></span>

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

### <span data-ttu-id="1b502-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b502-134">CommonParameters</span></span>
<span data-ttu-id="1b502-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1b502-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b502-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b502-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b502-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1b502-137">INPUTS</span></span>

### <span data-ttu-id="1b502-138">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="1b502-138">PSWorkspace</span></span>
<span data-ttu-id="1b502-139">Параметр "Рабочая область" принимает значение типа "PSWorkspace" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="1b502-139">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="1b502-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b502-140">OUTPUTS</span></span>

### <span data-ttu-id="1b502-141">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="1b502-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="1b502-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="1b502-142">NOTES</span></span>

## <span data-ttu-id="1b502-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1b502-143">RELATED LINKS</span></span>

[<span data-ttu-id="1b502-144">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="1b502-144">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="1b502-145">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="1b502-145">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


