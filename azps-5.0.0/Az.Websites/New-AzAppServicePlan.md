---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
ms.openlocfilehash: af94f1bec48bf54284ccf6e0011753a737dac30b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247119"
---
# <span data-ttu-id="a9b04-101">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a9b04-101">New-AzAppServicePlan</span></span>

## <span data-ttu-id="a9b04-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a9b04-102">SYNOPSIS</span></span>
<span data-ttu-id="a9b04-103">Создает план служб приложений Azure в указанном географическом расположении.</span><span class="sxs-lookup"><span data-stu-id="a9b04-103">Creates an Azure App Service plan in a given Geo location.</span></span>

## <span data-ttu-id="a9b04-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a9b04-104">SYNTAX</span></span>

### <span data-ttu-id="a9b04-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="a9b04-105">S1</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-HyperV] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a9b04-106">S2</span><span class="sxs-lookup"><span data-stu-id="a9b04-106">S2</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9b04-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9b04-107">DESCRIPTION</span></span>
<span data-ttu-id="a9b04-108">Командлет **New-AzAppServicePlan** создает план служб приложений Azure в определенном географическом расположении с указанным уровнем, размером рабочего процесса и количеством сотрудников.</span><span class="sxs-lookup"><span data-stu-id="a9b04-108">The **New-AzAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="a9b04-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a9b04-109">EXAMPLES</span></span>

### <span data-ttu-id="a9b04-110">Пример 1: создание плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="a9b04-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="a9b04-111">Эта команда создает план служб приложений с именем ContosoASP в группе ресурсов с именем Default-Web-WestUS в географическом расположении Запад US.</span><span class="sxs-lookup"><span data-stu-id="a9b04-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="a9b04-112">Команда задает базовый уровень и распределяется между двумя маленькими сотрудниками.</span><span class="sxs-lookup"><span data-stu-id="a9b04-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="a9b04-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a9b04-113">PARAMETERS</span></span>

### <span data-ttu-id="a9b04-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a9b04-114">-AppServicePlan</span></span>
<span data-ttu-id="a9b04-115">Объект плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="a9b04-115">App Service Plan Object</span></span>

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

### <span data-ttu-id="a9b04-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="a9b04-116">-AseName</span></span>
<span data-ttu-id="a9b04-117">Имя среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="a9b04-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="a9b04-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9b04-118">-AseResourceGroupName</span></span>
<span data-ttu-id="a9b04-119">Имя группы ресурсов среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="a9b04-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="a9b04-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9b04-120">-AsJob</span></span>
<span data-ttu-id="a9b04-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a9b04-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a9b04-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9b04-122">-DefaultProfile</span></span>
<span data-ttu-id="a9b04-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a9b04-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9b04-124">-HyperV</span><span class="sxs-lookup"><span data-stu-id="a9b04-124">-HyperV</span></span>
<span data-ttu-id="a9b04-125">Укажите, что план служб приложений будет запускать контейнеры Windows</span><span class="sxs-lookup"><span data-stu-id="a9b04-125">Specify this, App Service Plan will run Windows Containers</span></span>

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

### <span data-ttu-id="a9b04-126">-Location</span><span class="sxs-lookup"><span data-stu-id="a9b04-126">-Location</span></span>
<span data-ttu-id="a9b04-127">Поиска</span><span class="sxs-lookup"><span data-stu-id="a9b04-127">Location</span></span> 

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

### <span data-ttu-id="a9b04-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a9b04-128">-Name</span></span>
<span data-ttu-id="a9b04-129">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="a9b04-129">App Service Plan Name</span></span>

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

### <span data-ttu-id="a9b04-130">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="a9b04-130">-NumberofWorkers</span></span>
<span data-ttu-id="a9b04-131">Количество сотрудников</span><span class="sxs-lookup"><span data-stu-id="a9b04-131">Number Of Workers</span></span>

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

### <span data-ttu-id="a9b04-132">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="a9b04-132">-PerSiteScaling</span></span>
<span data-ttu-id="a9b04-133">Включение или выключение масштабирования на уровне сайта</span><span class="sxs-lookup"><span data-stu-id="a9b04-133">Whether or not to enable Per Site Scaling</span></span>

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

### <span data-ttu-id="a9b04-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9b04-134">-ResourceGroupName</span></span>
<span data-ttu-id="a9b04-135">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a9b04-135">Resource Group Name</span></span>

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

### <span data-ttu-id="a9b04-136">Уровень</span><span class="sxs-lookup"><span data-stu-id="a9b04-136">-Tier</span></span>
<span data-ttu-id="a9b04-137">Уровневый</span><span class="sxs-lookup"><span data-stu-id="a9b04-137">Tier</span></span>

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

### <span data-ttu-id="a9b04-138">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="a9b04-138">-WorkerSize</span></span>
<span data-ttu-id="a9b04-139">Размер веб-рабочего процесса</span><span class="sxs-lookup"><span data-stu-id="a9b04-139">Size of web worker</span></span>

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

### <span data-ttu-id="a9b04-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9b04-140">CommonParameters</span></span>
<span data-ttu-id="a9b04-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a9b04-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9b04-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9b04-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9b04-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a9b04-143">INPUTS</span></span>

### <span data-ttu-id="a9b04-144">Microsoft. Azure. Commands. Apps. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a9b04-144">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="a9b04-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9b04-145">OUTPUTS</span></span>

### <span data-ttu-id="a9b04-146">Microsoft. Azure. Commands. Apps. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a9b04-146">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="a9b04-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="a9b04-147">NOTES</span></span>

## <span data-ttu-id="a9b04-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a9b04-148">RELATED LINKS</span></span>

[<span data-ttu-id="a9b04-149">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a9b04-149">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="a9b04-150">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a9b04-150">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="a9b04-151">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a9b04-151">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


