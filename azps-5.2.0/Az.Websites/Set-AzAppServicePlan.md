---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzAppServicePlan.md
ms.openlocfilehash: b56766908ba993ccff056ce10acc81bba7a7196f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396463"
---
# <span data-ttu-id="409c9-101">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="409c9-101">Set-AzAppServicePlan</span></span>

## <span data-ttu-id="409c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="409c9-102">SYNOPSIS</span></span>
<span data-ttu-id="409c9-103">Задает план службы приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="409c9-103">Sets an Azure App Service plan.</span></span>

## <span data-ttu-id="409c9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="409c9-104">SYNTAX</span></span>

### <span data-ttu-id="409c9-105">S1</span><span class="sxs-lookup"><span data-stu-id="409c9-105">S1</span></span>
```
Set-AzAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="409c9-106">S2</span><span class="sxs-lookup"><span data-stu-id="409c9-106">S2</span></span>
```
Set-AzAppServicePlan [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="409c9-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="409c9-107">DESCRIPTION</span></span>
<span data-ttu-id="409c9-108">С **помощью cmdlet Set-AzAppServicePlan** задает план службы приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="409c9-108">The **Set-AzAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="409c9-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="409c9-109">EXAMPLES</span></span>

### <span data-ttu-id="409c9-110">Пример 1. Изменение плана службы приложений</span><span class="sxs-lookup"><span data-stu-id="409c9-110">Example 1: Modify an App Service plan</span></span>
```powershell
PS C:\>Set-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="409c9-111">Эта команда задает для параметра PerSiteScaling значение true в плане службы приложений ContosoASP, который принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="409c9-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="409c9-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="409c9-112">Example 2</span></span>

<span data-ttu-id="409c9-113">Задает план службы приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="409c9-113">Sets an Azure App Service plan.</span></span> <span data-ttu-id="409c9-114">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="409c9-114">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzAppServicePlan -Name 'ContosoASP' -ResourceGroupName 'Default-Web-WestUS' -Tier Free -WorkerSize Small
```

## <span data-ttu-id="409c9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="409c9-115">PARAMETERS</span></span>

### <span data-ttu-id="409c9-116">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="409c9-116">-AdminSiteName</span></span>
<span data-ttu-id="409c9-117">Имя сайта администратора</span><span class="sxs-lookup"><span data-stu-id="409c9-117">Admin Site Name</span></span>

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

### <span data-ttu-id="409c9-118">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="409c9-118">-AppServicePlan</span></span>
<span data-ttu-id="409c9-119">Объект плана обслуживания приложения</span><span class="sxs-lookup"><span data-stu-id="409c9-119">App Service Plan Object</span></span>

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

### <span data-ttu-id="409c9-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="409c9-120">-AsJob</span></span>
<span data-ttu-id="409c9-121">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="409c9-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="409c9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="409c9-122">-DefaultProfile</span></span>
<span data-ttu-id="409c9-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="409c9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="409c9-124">-Name</span><span class="sxs-lookup"><span data-stu-id="409c9-124">-Name</span></span>
<span data-ttu-id="409c9-125">Название плана службы приложений</span><span class="sxs-lookup"><span data-stu-id="409c9-125">App Service Plan Name</span></span>

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

### <span data-ttu-id="409c9-126">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="409c9-126">-NumberofWorkers</span></span>
<span data-ttu-id="409c9-127">Количество сотрудников</span><span class="sxs-lookup"><span data-stu-id="409c9-127">Number Of Workers</span></span>

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

### <span data-ttu-id="409c9-128">-PersiteScaling</span><span class="sxs-lookup"><span data-stu-id="409c9-128">-PerSiteScaling</span></span>
<span data-ttu-id="409c9-129">Boolean (На сайте: boolean) масштабирования</span><span class="sxs-lookup"><span data-stu-id="409c9-129">Per Site Scaling Boolean</span></span>

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

### <span data-ttu-id="409c9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="409c9-130">-ResourceGroupName</span></span>
<span data-ttu-id="409c9-131">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="409c9-131">Resource Group Name</span></span>

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

### <span data-ttu-id="409c9-132">-Tier</span><span class="sxs-lookup"><span data-stu-id="409c9-132">-Tier</span></span>
<span data-ttu-id="409c9-133">Уровень</span><span class="sxs-lookup"><span data-stu-id="409c9-133">Tier</span></span>

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

### <span data-ttu-id="409c9-134">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="409c9-134">-WorkerSize</span></span>
<span data-ttu-id="409c9-135">Размер сотрудника</span><span class="sxs-lookup"><span data-stu-id="409c9-135">Worker Size</span></span>

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

### <span data-ttu-id="409c9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="409c9-136">CommonParameters</span></span>
<span data-ttu-id="409c9-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="409c9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="409c9-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="409c9-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="409c9-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="409c9-139">INPUTS</span></span>

### <span data-ttu-id="409c9-140">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="409c9-140">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="409c9-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="409c9-141">OUTPUTS</span></span>

### <span data-ttu-id="409c9-142">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="409c9-142">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="409c9-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="409c9-143">NOTES</span></span>

## <span data-ttu-id="409c9-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="409c9-144">RELATED LINKS</span></span>

[<span data-ttu-id="409c9-145">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="409c9-145">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="409c9-146">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="409c9-146">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="409c9-147">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="409c9-147">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="409c9-148">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="409c9-148">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="409c9-149">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="409c9-149">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="409c9-150">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="409c9-150">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

