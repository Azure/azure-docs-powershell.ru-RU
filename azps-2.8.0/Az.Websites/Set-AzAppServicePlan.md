---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzAppServicePlan.md
ms.openlocfilehash: d27dc8ae315eb587ccb129125500a86e22429773
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907261"
---
# <span data-ttu-id="13791-101">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="13791-101">Set-AzAppServicePlan</span></span>

## <span data-ttu-id="13791-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="13791-102">SYNOPSIS</span></span>
<span data-ttu-id="13791-103">Задает план служб приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="13791-103">Sets an Azure App Service plan.</span></span>

## <span data-ttu-id="13791-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="13791-104">SYNTAX</span></span>

### <span data-ttu-id="13791-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="13791-105">S1</span></span>
```
Set-AzAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13791-106">S2</span><span class="sxs-lookup"><span data-stu-id="13791-106">S2</span></span>
```
Set-AzAppServicePlan [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="13791-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13791-107">DESCRIPTION</span></span>
<span data-ttu-id="13791-108">Командлет **Set-AzAppServicePlan** задает план служб приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="13791-108">The **Set-AzAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="13791-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="13791-109">EXAMPLES</span></span>

### <span data-ttu-id="13791-110">1: изменение плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="13791-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="13791-111">Эта команда устанавливает для параметра PerSiteScaling значение true для плана служб приложений с именем ContosoASP, который принадлежит группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="13791-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="13791-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="13791-112">PARAMETERS</span></span>

### <span data-ttu-id="13791-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="13791-113">-AdminSiteName</span></span>
<span data-ttu-id="13791-114">Имя сайта администратора</span><span class="sxs-lookup"><span data-stu-id="13791-114">Admin Site Name</span></span>

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

### <span data-ttu-id="13791-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="13791-115">-AppServicePlan</span></span>
<span data-ttu-id="13791-116">Объект плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="13791-116">App Service Plan Object</span></span>

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

### <span data-ttu-id="13791-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13791-117">-AsJob</span></span>
<span data-ttu-id="13791-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="13791-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="13791-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13791-119">-DefaultProfile</span></span>
<span data-ttu-id="13791-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="13791-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13791-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="13791-121">-Name</span></span>
<span data-ttu-id="13791-122">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="13791-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="13791-123">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="13791-123">-NumberofWorkers</span></span>
<span data-ttu-id="13791-124">Количество сотрудников</span><span class="sxs-lookup"><span data-stu-id="13791-124">Number Of Workers</span></span>

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

### <span data-ttu-id="13791-125">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="13791-125">-PerSiteScaling</span></span>
<span data-ttu-id="13791-126">Логическое масштабирование на уровне сайта</span><span class="sxs-lookup"><span data-stu-id="13791-126">Per Site Scaling Boolean</span></span>

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

### <span data-ttu-id="13791-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13791-127">-ResourceGroupName</span></span>
<span data-ttu-id="13791-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="13791-128">Resource Group Name</span></span>

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

### <span data-ttu-id="13791-129">Уровень</span><span class="sxs-lookup"><span data-stu-id="13791-129">-Tier</span></span>
<span data-ttu-id="13791-130">Уровневый</span><span class="sxs-lookup"><span data-stu-id="13791-130">Tier</span></span>

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

### <span data-ttu-id="13791-131">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="13791-131">-WorkerSize</span></span>
<span data-ttu-id="13791-132">Размер рабочего процесса</span><span class="sxs-lookup"><span data-stu-id="13791-132">Worker Size</span></span>

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

### <span data-ttu-id="13791-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13791-133">CommonParameters</span></span>
<span data-ttu-id="13791-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="13791-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13791-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13791-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13791-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="13791-136">INPUTS</span></span>

### <span data-ttu-id="13791-137">Microsoft. Azure. Commands. Apps. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="13791-137">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="13791-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="13791-138">OUTPUTS</span></span>

### <span data-ttu-id="13791-139">Microsoft. Azure. Commands. Apps. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="13791-139">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="13791-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="13791-140">NOTES</span></span>

## <span data-ttu-id="13791-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13791-141">RELATED LINKS</span></span>

[<span data-ttu-id="13791-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="13791-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="13791-143">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="13791-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="13791-144">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="13791-144">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="13791-145">Restarting-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="13791-145">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="13791-146">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="13791-146">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="13791-147">Остановить-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="13791-147">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


