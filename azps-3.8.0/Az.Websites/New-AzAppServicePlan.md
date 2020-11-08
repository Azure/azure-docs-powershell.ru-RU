---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
ms.openlocfilehash: af94f1bec48bf54284ccf6e0011753a737dac30b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066310"
---
# <span data-ttu-id="010bc-101">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="010bc-101">New-AzAppServicePlan</span></span>

## <span data-ttu-id="010bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="010bc-102">SYNOPSIS</span></span>
<span data-ttu-id="010bc-103">Создает план служб приложений Azure в указанном географическом расположении.</span><span class="sxs-lookup"><span data-stu-id="010bc-103">Creates an Azure App Service plan in a given Geo location.</span></span>

## <span data-ttu-id="010bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="010bc-104">SYNTAX</span></span>

### <span data-ttu-id="010bc-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="010bc-105">S1</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-HyperV] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="010bc-106">S2</span><span class="sxs-lookup"><span data-stu-id="010bc-106">S2</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="010bc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="010bc-107">DESCRIPTION</span></span>
<span data-ttu-id="010bc-108">Командлет **New-AzAppServicePlan** создает план служб приложений Azure в определенном географическом расположении с указанным уровнем, размером рабочего процесса и количеством сотрудников.</span><span class="sxs-lookup"><span data-stu-id="010bc-108">The **New-AzAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="010bc-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="010bc-109">EXAMPLES</span></span>

### <span data-ttu-id="010bc-110">Пример 1: создание плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="010bc-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="010bc-111">Эта команда создает план служб приложений с именем ContosoASP в группе ресурсов с именем Default-Web-WestUS в географическом расположении Запад US.</span><span class="sxs-lookup"><span data-stu-id="010bc-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="010bc-112">Команда задает базовый уровень и распределяется между двумя маленькими сотрудниками.</span><span class="sxs-lookup"><span data-stu-id="010bc-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="010bc-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="010bc-113">PARAMETERS</span></span>

### <span data-ttu-id="010bc-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="010bc-114">-AppServicePlan</span></span>
<span data-ttu-id="010bc-115">Объект плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="010bc-115">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="010bc-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="010bc-116">-AseName</span></span>
<span data-ttu-id="010bc-117">Имя среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="010bc-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="010bc-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="010bc-118">-AseResourceGroupName</span></span>
<span data-ttu-id="010bc-119">Имя группы ресурсов среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="010bc-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="010bc-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="010bc-120">-AsJob</span></span>
<span data-ttu-id="010bc-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="010bc-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="010bc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="010bc-122">-DefaultProfile</span></span>
<span data-ttu-id="010bc-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="010bc-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="010bc-124">-HyperV</span><span class="sxs-lookup"><span data-stu-id="010bc-124">-HyperV</span></span>
<span data-ttu-id="010bc-125">Укажите, что план служб приложений будет запускать контейнеры Windows</span><span class="sxs-lookup"><span data-stu-id="010bc-125">Specify this, App Service Plan will run Windows Containers</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="010bc-126">-Location</span><span class="sxs-lookup"><span data-stu-id="010bc-126">-Location</span></span>
<span data-ttu-id="010bc-127">Поиска</span><span class="sxs-lookup"><span data-stu-id="010bc-127">Location</span></span> 

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

### <span data-ttu-id="010bc-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="010bc-128">-Name</span></span>
<span data-ttu-id="010bc-129">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="010bc-129">App Service Plan Name</span></span>

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

### <span data-ttu-id="010bc-130">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="010bc-130">-NumberofWorkers</span></span>
<span data-ttu-id="010bc-131">Количество сотрудников</span><span class="sxs-lookup"><span data-stu-id="010bc-131">Number Of Workers</span></span>

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

### <span data-ttu-id="010bc-132">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="010bc-132">-PerSiteScaling</span></span>
<span data-ttu-id="010bc-133">Включение или выключение масштабирования на уровне сайта</span><span class="sxs-lookup"><span data-stu-id="010bc-133">Whether or not to enable Per Site Scaling</span></span>

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

### <span data-ttu-id="010bc-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="010bc-134">-ResourceGroupName</span></span>
<span data-ttu-id="010bc-135">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="010bc-135">Resource Group Name</span></span>

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

### <span data-ttu-id="010bc-136">Уровень</span><span class="sxs-lookup"><span data-stu-id="010bc-136">-Tier</span></span>
<span data-ttu-id="010bc-137">Уровневый</span><span class="sxs-lookup"><span data-stu-id="010bc-137">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: Free
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="010bc-138">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="010bc-138">-WorkerSize</span></span>
<span data-ttu-id="010bc-139">Размер веб-рабочего процесса</span><span class="sxs-lookup"><span data-stu-id="010bc-139">Size of web worker</span></span>

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

### <span data-ttu-id="010bc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="010bc-140">CommonParameters</span></span>
<span data-ttu-id="010bc-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="010bc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="010bc-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="010bc-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="010bc-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="010bc-143">INPUTS</span></span>

### <span data-ttu-id="010bc-144">Microsoft. Azure. Commands. Apps. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="010bc-144">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="010bc-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="010bc-145">OUTPUTS</span></span>

### <span data-ttu-id="010bc-146">Microsoft. Azure. Commands. Apps. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="010bc-146">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="010bc-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="010bc-147">NOTES</span></span>

## <span data-ttu-id="010bc-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="010bc-148">RELATED LINKS</span></span>

[<span data-ttu-id="010bc-149">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="010bc-149">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="010bc-150">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="010bc-150">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="010bc-151">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="010bc-151">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


