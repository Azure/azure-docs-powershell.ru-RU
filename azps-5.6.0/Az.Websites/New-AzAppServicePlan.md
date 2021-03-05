---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
ms.openlocfilehash: 9a1c1de8aef41089cfc874cf35b26fcc9bf0be52
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011128"
---
# <span data-ttu-id="0318b-101">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0318b-101">New-AzAppServicePlan</span></span>

## <span data-ttu-id="0318b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0318b-102">SYNOPSIS</span></span>
<span data-ttu-id="0318b-103">Создает план службы приложения Azure в заданном географическом расположении.</span><span class="sxs-lookup"><span data-stu-id="0318b-103">Creates an Azure App Service plan in a given Geo location.</span></span>

## <span data-ttu-id="0318b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0318b-104">SYNTAX</span></span>

### <span data-ttu-id="0318b-105">S1</span><span class="sxs-lookup"><span data-stu-id="0318b-105">S1</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-HyperV] [-AsJob] [-Tag <Hashtable>] [-Linux] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0318b-106">S2</span><span class="sxs-lookup"><span data-stu-id="0318b-106">S2</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0318b-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0318b-107">DESCRIPTION</span></span>
<span data-ttu-id="0318b-108">С **помощью cmdlet New-AzAppServicePlan** создается план службы приложения Azure в заданном географическом расположении с указанными уровнями, размером сотрудников и количеством работников.</span><span class="sxs-lookup"><span data-stu-id="0318b-108">The **New-AzAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="0318b-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0318b-109">EXAMPLES</span></span>

### <span data-ttu-id="0318b-110">Пример 1. Создание плана службы приложений</span><span class="sxs-lookup"><span data-stu-id="0318b-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="0318b-111">Эта команда создает план службы приложения ContosoASP в группе ресурсов Default-Web-WestUS в географическом расположении "Запад США".</span><span class="sxs-lookup"><span data-stu-id="0318b-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="0318b-112">Команда определяет базовый уровень и выделяет двух небольших сотрудников.</span><span class="sxs-lookup"><span data-stu-id="0318b-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="0318b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0318b-113">PARAMETERS</span></span>

### <span data-ttu-id="0318b-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0318b-114">-AppServicePlan</span></span>
<span data-ttu-id="0318b-115">Объект плана обслуживания приложения</span><span class="sxs-lookup"><span data-stu-id="0318b-115">App Service Plan Object</span></span>

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

### <span data-ttu-id="0318b-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="0318b-116">-AseName</span></span>
<span data-ttu-id="0318b-117">Имя среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="0318b-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="0318b-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0318b-118">-AseResourceGroupName</span></span>
<span data-ttu-id="0318b-119">Имя группы ресурсов среды приложения</span><span class="sxs-lookup"><span data-stu-id="0318b-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="0318b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0318b-120">-AsJob</span></span>
<span data-ttu-id="0318b-121">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0318b-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0318b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0318b-122">-DefaultProfile</span></span>
<span data-ttu-id="0318b-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0318b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0318b-124">-HyperV</span><span class="sxs-lookup"><span data-stu-id="0318b-124">-HyperV</span></span>
<span data-ttu-id="0318b-125">Укажите это, план обслуживания приложения запустит контейнеры Windows</span><span class="sxs-lookup"><span data-stu-id="0318b-125">Specify this, App Service Plan will run Windows Containers</span></span>

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

### <span data-ttu-id="0318b-126">-Linux</span><span class="sxs-lookup"><span data-stu-id="0318b-126">-Linux</span></span>
<span data-ttu-id="0318b-127">Укажите это, план обслуживания приложения будет запускать контейнеры Linux</span><span class="sxs-lookup"><span data-stu-id="0318b-127">Specify this, App Service Plan will run Linux Containers</span></span>

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

### <span data-ttu-id="0318b-128">-Location</span><span class="sxs-lookup"><span data-stu-id="0318b-128">-Location</span></span>
<span data-ttu-id="0318b-129">Расположение</span><span class="sxs-lookup"><span data-stu-id="0318b-129">Location</span></span> 

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

### <span data-ttu-id="0318b-130">-Name</span><span class="sxs-lookup"><span data-stu-id="0318b-130">-Name</span></span>
<span data-ttu-id="0318b-131">Имя плана службы приложений</span><span class="sxs-lookup"><span data-stu-id="0318b-131">App Service Plan Name</span></span>

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

### <span data-ttu-id="0318b-132">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="0318b-132">-NumberofWorkers</span></span>
<span data-ttu-id="0318b-133">Количество сотрудников</span><span class="sxs-lookup"><span data-stu-id="0318b-133">Number Of Workers</span></span>

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

### <span data-ttu-id="0318b-134">-PersiteScaling</span><span class="sxs-lookup"><span data-stu-id="0318b-134">-PerSiteScaling</span></span>
<span data-ttu-id="0318b-135">Следует ли включить для каждого сайта масштабирование</span><span class="sxs-lookup"><span data-stu-id="0318b-135">Whether or not to enable Per Site Scaling</span></span>

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

### <span data-ttu-id="0318b-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0318b-136">-ResourceGroupName</span></span>
<span data-ttu-id="0318b-137">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="0318b-137">Resource Group Name</span></span>

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

### <span data-ttu-id="0318b-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="0318b-138">-Tag</span></span>
<span data-ttu-id="0318b-139">Теги — это пары имен и значений, позволяющие классифицировать ресурсы.</span><span class="sxs-lookup"><span data-stu-id="0318b-139">Tags are name/value pairs that enable you to categorize resources</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0318b-140">-Tier</span><span class="sxs-lookup"><span data-stu-id="0318b-140">-Tier</span></span>
<span data-ttu-id="0318b-141">Уровень</span><span class="sxs-lookup"><span data-stu-id="0318b-141">Tier</span></span>

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

### <span data-ttu-id="0318b-142">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="0318b-142">-WorkerSize</span></span>
<span data-ttu-id="0318b-143">Размер веб-сотрудника</span><span class="sxs-lookup"><span data-stu-id="0318b-143">Size of web worker</span></span>

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

### <span data-ttu-id="0318b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0318b-144">CommonParameters</span></span>
<span data-ttu-id="0318b-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0318b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0318b-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0318b-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0318b-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0318b-147">INPUTS</span></span>

### <span data-ttu-id="0318b-148">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0318b-148">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="0318b-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0318b-149">OUTPUTS</span></span>

### <span data-ttu-id="0318b-150">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0318b-150">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="0318b-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0318b-151">NOTES</span></span>

## <span data-ttu-id="0318b-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0318b-152">RELATED LINKS</span></span>

[<span data-ttu-id="0318b-153">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0318b-153">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="0318b-154">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0318b-154">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="0318b-155">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0318b-155">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


