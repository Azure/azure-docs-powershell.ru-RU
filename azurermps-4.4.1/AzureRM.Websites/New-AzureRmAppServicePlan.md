---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
ms.openlocfilehash: e03e7dee6e233934216c04a44c1e100d3e26347b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734501"
---
# <span data-ttu-id="6d250-101">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6d250-101">New-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="6d250-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6d250-102">SYNOPSIS</span></span>
<span data-ttu-id="6d250-103">Создает план служб приложений Azure в указанном географическом расположении.</span><span class="sxs-lookup"><span data-stu-id="6d250-103">Creates an Azure App Service plan in a given Geo location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d250-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6d250-104">SYNTAX</span></span>

### <span data-ttu-id="6d250-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="6d250-105">S1</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d250-106">S2</span><span class="sxs-lookup"><span data-stu-id="6d250-106">S2</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AppServicePlan] <ServerFarmWithRichSku> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d250-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d250-107">DESCRIPTION</span></span>
<span data-ttu-id="6d250-108">Командлет **New-AzureRmAppServicePlan** создает план служб приложений Azure в определенном географическом расположении с указанным уровнем, размером рабочего процесса и количеством сотрудников.</span><span class="sxs-lookup"><span data-stu-id="6d250-108">The **New-AzureRmAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="6d250-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6d250-109">EXAMPLES</span></span>

### <span data-ttu-id="6d250-110">Пример 1: создание плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="6d250-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="6d250-111">Эта команда создает план служб приложений с именем ContosoASP в группе ресурсов с именем Default-Web-WestUS в географическом расположении Запад US.</span><span class="sxs-lookup"><span data-stu-id="6d250-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="6d250-112">Команда задает базовый уровень и распределяется между двумя маленькими сотрудниками.</span><span class="sxs-lookup"><span data-stu-id="6d250-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="6d250-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6d250-113">PARAMETERS</span></span>

### <span data-ttu-id="6d250-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6d250-114">-AppServicePlan</span></span>
<span data-ttu-id="6d250-115">Объект плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="6d250-115">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d250-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="6d250-116">-AseName</span></span>
<span data-ttu-id="6d250-117">Имя среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="6d250-117">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d250-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d250-118">-AseResourceGroupName</span></span>
<span data-ttu-id="6d250-119">Имя группы ресурсов среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="6d250-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="6d250-120">-Location</span><span class="sxs-lookup"><span data-stu-id="6d250-120">-Location</span></span>
<span data-ttu-id="6d250-121">Поиска</span><span class="sxs-lookup"><span data-stu-id="6d250-121">Location</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d250-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6d250-122">-Name</span></span>
<span data-ttu-id="6d250-123">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="6d250-123">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d250-124">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="6d250-124">-NumberofWorkers</span></span>
<span data-ttu-id="6d250-125">Количество сотрудников</span><span class="sxs-lookup"><span data-stu-id="6d250-125">Number Of Workers</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d250-126">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="6d250-126">-PerSiteScaling</span></span>
<span data-ttu-id="6d250-127">Включение или выключение масштабирования на уровне сайта</span><span class="sxs-lookup"><span data-stu-id="6d250-127">Whether or not to enable Per Site Scaling</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d250-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d250-128">-ResourceGroupName</span></span>
<span data-ttu-id="6d250-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6d250-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d250-130">Уровень</span><span class="sxs-lookup"><span data-stu-id="6d250-130">-Tier</span></span>
<span data-ttu-id="6d250-131">Уровневый</span><span class="sxs-lookup"><span data-stu-id="6d250-131">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium

Required: False
Position: 3
Default value: Free
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d250-132">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="6d250-132">-WorkerSize</span></span>
<span data-ttu-id="6d250-133">Размер веб-рабочего процесса</span><span class="sxs-lookup"><span data-stu-id="6d250-133">Size of web worker</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: Small
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d250-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d250-134">-DefaultProfile</span></span>
<span data-ttu-id="6d250-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6d250-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d250-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d250-136">CommonParameters</span></span>
<span data-ttu-id="6d250-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6d250-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d250-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d250-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d250-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6d250-139">INPUTS</span></span>

### <span data-ttu-id="6d250-140">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="6d250-140">ServerFarmWithRichSku</span></span>
<span data-ttu-id="6d250-141">Параметр "AppServicePlan" принимает значение типа "ServerFarmWithRichSku" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="6d250-141">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="6d250-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d250-142">OUTPUTS</span></span>

### <span data-ttu-id="6d250-143">Microsoft. Azure. Management. website. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="6d250-143">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="6d250-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="6d250-144">NOTES</span></span>

## <span data-ttu-id="6d250-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d250-145">RELATED LINKS</span></span>

[<span data-ttu-id="6d250-146">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6d250-146">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="6d250-147">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6d250-147">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="6d250-148">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6d250-148">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


