---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermappserviceplan
schema: 2.0.0
ms.openlocfilehash: 015a16ec40e7b5159e6082acd47f2583edff1f09
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913712"
---
# <span data-ttu-id="0c4d8-101">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0c4d8-101">New-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="0c4d8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0c4d8-102">SYNOPSIS</span></span>
<span data-ttu-id="0c4d8-103">Создает план служб приложений Azure в указанном географическом расположении.</span><span class="sxs-lookup"><span data-stu-id="0c4d8-103">Creates an Azure App Service plan in a given Geo location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c4d8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0c4d8-104">SYNTAX</span></span>

### <span data-ttu-id="0c4d8-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="0c4d8-105">S1</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-ResourceGroupName] <String> [-Name] <String> [-AsJob][-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c4d8-106">S2</span><span class="sxs-lookup"><span data-stu-id="0c4d8-106">S2</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AppServicePlan] <ServerFarmWithRichSku> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c4d8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c4d8-107">DESCRIPTION</span></span>
<span data-ttu-id="0c4d8-108">Командлет **New-AzureRmAppServicePlan** создает план служб приложений Azure в определенном географическом расположении с указанным уровнем, размером рабочего процесса и количеством сотрудников.</span><span class="sxs-lookup"><span data-stu-id="0c4d8-108">The **New-AzureRmAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="0c4d8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0c4d8-109">EXAMPLES</span></span>

### <span data-ttu-id="0c4d8-110">Пример 1: создание плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="0c4d8-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="0c4d8-111">Эта команда создает план служб приложений с именем ContosoASP в группе ресурсов с именем Default-Web-WestUS в географическом расположении Запад US.</span><span class="sxs-lookup"><span data-stu-id="0c4d8-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="0c4d8-112">Команда задает базовый уровень и распределяется между двумя маленькими сотрудниками.</span><span class="sxs-lookup"><span data-stu-id="0c4d8-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="0c4d8-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0c4d8-113">PARAMETERS</span></span>

### <span data-ttu-id="0c4d8-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0c4d8-114">-AppServicePlan</span></span>
<span data-ttu-id="0c4d8-115">Объект плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="0c4d8-115">App Service Plan Object</span></span>

```yaml
Type: ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c4d8-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="0c4d8-116">-AseName</span></span>
<span data-ttu-id="0c4d8-117">Имя среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="0c4d8-117">App Service Environment Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c4d8-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c4d8-118">-AseResourceGroupName</span></span>
<span data-ttu-id="0c4d8-119">Имя группы ресурсов среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="0c4d8-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c4d8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c4d8-120">-DefaultProfile</span></span>
<span data-ttu-id="0c4d8-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0c4d8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c4d8-122">-Location</span><span class="sxs-lookup"><span data-stu-id="0c4d8-122">-Location</span></span>
<span data-ttu-id="0c4d8-123">Поиска</span><span class="sxs-lookup"><span data-stu-id="0c4d8-123">Location</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c4d8-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0c4d8-124">-Name</span></span>
<span data-ttu-id="0c4d8-125">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="0c4d8-125">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c4d8-126">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="0c4d8-126">-NumberofWorkers</span></span>
<span data-ttu-id="0c4d8-127">Количество сотрудников</span><span class="sxs-lookup"><span data-stu-id="0c4d8-127">Number Of Workers</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c4d8-128">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="0c4d8-128">-PerSiteScaling</span></span>
<span data-ttu-id="0c4d8-129">Включение или выключение масштабирования на уровне сайта</span><span class="sxs-lookup"><span data-stu-id="0c4d8-129">Whether or not to enable Per Site Scaling</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c4d8-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c4d8-130">-ResourceGroupName</span></span>
<span data-ttu-id="0c4d8-131">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="0c4d8-131">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c4d8-132">Уровень</span><span class="sxs-lookup"><span data-stu-id="0c4d8-132">-Tier</span></span>
<span data-ttu-id="0c4d8-133">Уровневый</span><span class="sxs-lookup"><span data-stu-id="0c4d8-133">Tier</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium, PremiumV2

Required: False
Position: 3
Default value: Free
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c4d8-134">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="0c4d8-134">-WorkerSize</span></span>
<span data-ttu-id="0c4d8-135">Размер веб-рабочего процесса</span><span class="sxs-lookup"><span data-stu-id="0c4d8-135">Size of web worker</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: Small
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="0c4d8-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c4d8-136">-AsJob</span></span>
<span data-ttu-id="0c4d8-137">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0c4d8-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0c4d8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c4d8-138">CommonParameters</span></span>
<span data-ttu-id="0c4d8-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0c4d8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c4d8-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c4d8-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c4d8-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0c4d8-141">INPUTS</span></span>

### <span data-ttu-id="0c4d8-142">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="0c4d8-142">ServerFarmWithRichSku</span></span>
<span data-ttu-id="0c4d8-143">Параметр "AppServicePlan" принимает значение типа "ServerFarmWithRichSku" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="0c4d8-143">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="0c4d8-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c4d8-144">OUTPUTS</span></span>

### <span data-ttu-id="0c4d8-145">Microsoft. Azure. Management. website. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="0c4d8-145">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="0c4d8-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="0c4d8-146">NOTES</span></span>

## <span data-ttu-id="0c4d8-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c4d8-147">RELATED LINKS</span></span>

[<span data-ttu-id="0c4d8-148">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0c4d8-148">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="0c4d8-149">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0c4d8-149">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="0c4d8-150">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0c4d8-150">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


