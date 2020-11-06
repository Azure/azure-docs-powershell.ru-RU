---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
ms.openlocfilehash: 2163c18fecadba069b7c3fba260ab81538ed5583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565275"
---
# <span data-ttu-id="a737a-101">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a737a-101">Set-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="a737a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a737a-102">SYNOPSIS</span></span>
<span data-ttu-id="a737a-103">Задает план служб приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="a737a-103">Sets an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a737a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a737a-104">SYNTAX</span></span>

### <span data-ttu-id="a737a-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="a737a-105">S1</span></span>
```
Set-AzureRmAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a737a-106">S2</span><span class="sxs-lookup"><span data-stu-id="a737a-106">S2</span></span>
```
Set-AzureRmAppServicePlan [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a737a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a737a-107">DESCRIPTION</span></span>
<span data-ttu-id="a737a-108">Командлет **Set-AzureRmAppServicePlan** задает план служб приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="a737a-108">The **Set-AzureRmAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="a737a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a737a-109">EXAMPLES</span></span>

### <span data-ttu-id="a737a-110">1: изменение плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="a737a-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="a737a-111">Эта команда устанавливает для параметра PerSiteScaling значение true для плана служб приложений с именем ContosoASP, который принадлежит группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="a737a-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="a737a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a737a-112">PARAMETERS</span></span>

### <span data-ttu-id="a737a-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="a737a-113">-AdminSiteName</span></span>
<span data-ttu-id="a737a-114">Имя сайта администратора</span><span class="sxs-lookup"><span data-stu-id="a737a-114">Admin Site Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a737a-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a737a-115">-AppServicePlan</span></span>
<span data-ttu-id="a737a-116">Объект плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="a737a-116">App Service Plan Object</span></span>

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

### <span data-ttu-id="a737a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a737a-117">-AsJob</span></span>
<span data-ttu-id="a737a-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a737a-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a737a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a737a-119">-DefaultProfile</span></span>
<span data-ttu-id="a737a-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a737a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a737a-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a737a-121">-Name</span></span>
<span data-ttu-id="a737a-122">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="a737a-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="a737a-123">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="a737a-123">-NumberofWorkers</span></span>
<span data-ttu-id="a737a-124">Количество сотрудников</span><span class="sxs-lookup"><span data-stu-id="a737a-124">Number Of Workers</span></span>

```yaml
Type: System.Int32
Parameter Sets: S1
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a737a-125">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="a737a-125">-PerSiteScaling</span></span>
<span data-ttu-id="a737a-126">Логическое масштабирование на уровне сайта</span><span class="sxs-lookup"><span data-stu-id="a737a-126">Per Site Scaling Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a737a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a737a-127">-ResourceGroupName</span></span>
<span data-ttu-id="a737a-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a737a-128">Resource Group Name</span></span>

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

### <span data-ttu-id="a737a-129">Уровень</span><span class="sxs-lookup"><span data-stu-id="a737a-129">-Tier</span></span>
<span data-ttu-id="a737a-130">Уровневый</span><span class="sxs-lookup"><span data-stu-id="a737a-130">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a737a-131">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="a737a-131">-WorkerSize</span></span>
<span data-ttu-id="a737a-132">Размер рабочего процесса</span><span class="sxs-lookup"><span data-stu-id="a737a-132">Worker Size</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a737a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a737a-133">CommonParameters</span></span>
<span data-ttu-id="a737a-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a737a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a737a-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a737a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a737a-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a737a-136">INPUTS</span></span>

### <span data-ttu-id="a737a-137">Microsoft. Azure. Management. website. Models. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a737a-137">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>
<span data-ttu-id="a737a-138">Параметры: AppServicePlan (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a737a-138">Parameters: AppServicePlan (ByValue)</span></span>

## <span data-ttu-id="a737a-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a737a-139">OUTPUTS</span></span>

### <span data-ttu-id="a737a-140">Microsoft. Azure. Management. website. Models. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a737a-140">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>

## <span data-ttu-id="a737a-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="a737a-141">NOTES</span></span>

## <span data-ttu-id="a737a-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a737a-142">RELATED LINKS</span></span>

[<span data-ttu-id="a737a-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a737a-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="a737a-144">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a737a-144">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="a737a-145">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a737a-145">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="a737a-146">Restarting-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a737a-146">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="a737a-147">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a737a-147">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="a737a-148">Остановить-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a737a-148">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


