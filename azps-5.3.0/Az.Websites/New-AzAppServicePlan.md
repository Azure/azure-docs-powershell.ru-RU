---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
ms.openlocfilehash: af94f1bec48bf54284ccf6e0011753a737dac30b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505776"
---
# <span data-ttu-id="49a59-101">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="49a59-101">New-AzAppServicePlan</span></span>

## <span data-ttu-id="49a59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49a59-102">SYNOPSIS</span></span>
<span data-ttu-id="49a59-103">Создает план службы приложения Azure в заданном географическом расположении.</span><span class="sxs-lookup"><span data-stu-id="49a59-103">Creates an Azure App Service plan in a given Geo location.</span></span>

## <span data-ttu-id="49a59-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="49a59-104">SYNTAX</span></span>

### <span data-ttu-id="49a59-105">S1</span><span class="sxs-lookup"><span data-stu-id="49a59-105">S1</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-HyperV] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="49a59-106">S2</span><span class="sxs-lookup"><span data-stu-id="49a59-106">S2</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49a59-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49a59-107">DESCRIPTION</span></span>
<span data-ttu-id="49a59-108">С **помощью cmdlet New-AzAppServicePlan** создается план службы приложения Azure в заданном географическом расположении с указанными уровнями, размером сотрудников и количеством работников.</span><span class="sxs-lookup"><span data-stu-id="49a59-108">The **New-AzAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="49a59-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="49a59-109">EXAMPLES</span></span>

### <span data-ttu-id="49a59-110">Пример 1. Создание плана службы приложений</span><span class="sxs-lookup"><span data-stu-id="49a59-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="49a59-111">Эта команда создает план службы приложения ContosoASP в группе ресурсов Default-Web-WestUS в географическом расположении "Запад США".</span><span class="sxs-lookup"><span data-stu-id="49a59-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="49a59-112">Команда определяет базовый уровень и выделяет двух небольших сотрудников.</span><span class="sxs-lookup"><span data-stu-id="49a59-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="49a59-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49a59-113">PARAMETERS</span></span>

### <span data-ttu-id="49a59-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="49a59-114">-AppServicePlan</span></span>
<span data-ttu-id="49a59-115">Объект плана обслуживания приложения</span><span class="sxs-lookup"><span data-stu-id="49a59-115">App Service Plan Object</span></span>

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

### <span data-ttu-id="49a59-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="49a59-116">-AseName</span></span>
<span data-ttu-id="49a59-117">Имя среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="49a59-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="49a59-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49a59-118">-AseResourceGroupName</span></span>
<span data-ttu-id="49a59-119">Имя группы ресурсов среды приложения</span><span class="sxs-lookup"><span data-stu-id="49a59-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="49a59-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49a59-120">-AsJob</span></span>
<span data-ttu-id="49a59-121">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="49a59-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="49a59-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49a59-122">-DefaultProfile</span></span>
<span data-ttu-id="49a59-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49a59-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49a59-124">-HyperV</span><span class="sxs-lookup"><span data-stu-id="49a59-124">-HyperV</span></span>
<span data-ttu-id="49a59-125">Укажите это, план обслуживания приложения запустит контейнеры Windows</span><span class="sxs-lookup"><span data-stu-id="49a59-125">Specify this, App Service Plan will run Windows Containers</span></span>

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

### <span data-ttu-id="49a59-126">-Location</span><span class="sxs-lookup"><span data-stu-id="49a59-126">-Location</span></span>
<span data-ttu-id="49a59-127">Расположение</span><span class="sxs-lookup"><span data-stu-id="49a59-127">Location</span></span> 

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

### <span data-ttu-id="49a59-128">-Name</span><span class="sxs-lookup"><span data-stu-id="49a59-128">-Name</span></span>
<span data-ttu-id="49a59-129">Имя плана службы приложений</span><span class="sxs-lookup"><span data-stu-id="49a59-129">App Service Plan Name</span></span>

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

### <span data-ttu-id="49a59-130">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="49a59-130">-NumberofWorkers</span></span>
<span data-ttu-id="49a59-131">Количество сотрудников</span><span class="sxs-lookup"><span data-stu-id="49a59-131">Number Of Workers</span></span>

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

### <span data-ttu-id="49a59-132">-PersiteScaling</span><span class="sxs-lookup"><span data-stu-id="49a59-132">-PerSiteScaling</span></span>
<span data-ttu-id="49a59-133">Следует ли включить для каждого сайта масштабирование</span><span class="sxs-lookup"><span data-stu-id="49a59-133">Whether or not to enable Per Site Scaling</span></span>

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

### <span data-ttu-id="49a59-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49a59-134">-ResourceGroupName</span></span>
<span data-ttu-id="49a59-135">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="49a59-135">Resource Group Name</span></span>

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

### <span data-ttu-id="49a59-136">-Tier</span><span class="sxs-lookup"><span data-stu-id="49a59-136">-Tier</span></span>
<span data-ttu-id="49a59-137">Уровень</span><span class="sxs-lookup"><span data-stu-id="49a59-137">Tier</span></span>

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

### <span data-ttu-id="49a59-138">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="49a59-138">-WorkerSize</span></span>
<span data-ttu-id="49a59-139">Размер веб-сотрудника</span><span class="sxs-lookup"><span data-stu-id="49a59-139">Size of web worker</span></span>

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

### <span data-ttu-id="49a59-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49a59-140">CommonParameters</span></span>
<span data-ttu-id="49a59-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49a59-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49a59-142">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49a59-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49a59-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="49a59-143">INPUTS</span></span>

### <span data-ttu-id="49a59-144">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="49a59-144">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="49a59-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="49a59-145">OUTPUTS</span></span>

### <span data-ttu-id="49a59-146">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="49a59-146">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="49a59-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="49a59-147">NOTES</span></span>

## <span data-ttu-id="49a59-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49a59-148">RELATED LINKS</span></span>

[<span data-ttu-id="49a59-149">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="49a59-149">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="49a59-150">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="49a59-150">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="49a59-151">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="49a59-151">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


