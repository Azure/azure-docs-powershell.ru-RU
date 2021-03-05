---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-azappserviceenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServiceEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServiceEnvironment.md
ms.openlocfilehash: 73c7a7b76f882678612eb6f2a1fb682637705858
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970083"
---
# <span data-ttu-id="d2456-101">Remove-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="d2456-101">Remove-AzAppServiceEnvironment</span></span>

## <span data-ttu-id="d2456-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2456-102">SYNOPSIS</span></span>
<span data-ttu-id="d2456-103">"Удалить среду службы приложений".</span><span class="sxs-lookup"><span data-stu-id="d2456-103">Remove App Service Environment.</span></span>

## <span data-ttu-id="d2456-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d2456-104">SYNTAX</span></span>

### <span data-ttu-id="d2456-105">InputValuesParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2456-105">InputValuesParameterSet</span></span>
```
Remove-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2456-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2456-106">InputObjectParameterSet</span></span>
```
Remove-AzAppServiceEnvironment [-Force] [-PassThru] [-AsJob] -InputObject <PSAppServiceEnvironment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2456-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2456-107">DESCRIPTION</span></span>
<span data-ttu-id="d2456-108">С **помощью cmdlet Remove-AzAppServiceEnvironment** удаляется среда службы приложений.</span><span class="sxs-lookup"><span data-stu-id="d2456-108">The **Remove-AzAppServiceEnvironment** cmdlet removes an App Service Environment.</span></span> <span data-ttu-id="d2456-109">Перед удалением ASE необходимо удалить любой план обслуживания приложений.</span><span class="sxs-lookup"><span data-stu-id="d2456-109">Any App Service Plan must be deleted prior to deleting the ASE.</span></span>

## <span data-ttu-id="d2456-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d2456-110">EXAMPLES</span></span>

### <span data-ttu-id="d2456-111">Пример 1. Удаление среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="d2456-111">Example 1 : Delete an App Service Environment</span></span>
```powershell
PS C:\> Remove-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseName
```

<span data-ttu-id="d2456-112">Удаление среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="d2456-112">Delete an App Service Environment</span></span>

## <span data-ttu-id="d2456-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2456-113">PARAMETERS</span></span>

### <span data-ttu-id="d2456-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2456-114">-AsJob</span></span>
<span data-ttu-id="d2456-115">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="d2456-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d2456-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2456-116">-DefaultProfile</span></span>
<span data-ttu-id="d2456-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d2456-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2456-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d2456-118">-Force</span></span>
<span data-ttu-id="d2456-119">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="d2456-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d2456-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2456-120">-InputObject</span></span>
<span data-ttu-id="d2456-121">Объект среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="d2456-121">The app service environment object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServiceEnvironment
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2456-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d2456-122">-Name</span></span>
<span data-ttu-id="d2456-123">Имя среды службы приложений.</span><span class="sxs-lookup"><span data-stu-id="d2456-123">The name of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2456-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2456-124">-PassThru</span></span>
<span data-ttu-id="d2456-125">Вернуть состояние.</span><span class="sxs-lookup"><span data-stu-id="d2456-125">Return status.</span></span>

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

### <span data-ttu-id="d2456-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2456-126">-ResourceGroupName</span></span>
<span data-ttu-id="d2456-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d2456-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2456-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2456-128">-Confirm</span></span>
<span data-ttu-id="d2456-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2456-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2456-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2456-130">-WhatIf</span></span>
<span data-ttu-id="d2456-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2456-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2456-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d2456-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2456-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2456-133">CommonParameters</span></span>
<span data-ttu-id="d2456-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2456-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2456-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2456-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2456-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2456-136">INPUTS</span></span>

### <span data-ttu-id="d2456-137">Нет</span><span class="sxs-lookup"><span data-stu-id="d2456-137">None</span></span>

## <span data-ttu-id="d2456-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d2456-138">OUTPUTS</span></span>

### <span data-ttu-id="d2456-139">System.Object</span><span class="sxs-lookup"><span data-stu-id="d2456-139">System.Object</span></span>
## <span data-ttu-id="d2456-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d2456-140">NOTES</span></span>

## <span data-ttu-id="d2456-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2456-141">RELATED LINKS</span></span>

[<span data-ttu-id="d2456-142">New-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="d2456-142">New-AzAppServiceEnvironment</span></span>](./New-AzAppServiceEnvironment.md)

[<span data-ttu-id="d2456-143">Get-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="d2456-143">Get-AzAppServiceEnvironment</span></span>](./Get-AzAppServiceEnvironment.md)

[<span data-ttu-id="d2456-144">New-AzAppServiceEnvironmentInboundServices</span><span class="sxs-lookup"><span data-stu-id="d2456-144">New-AzAppServiceEnvironmentInboundServices</span></span>](./New-AzAppServiceEnvironmentInboundServices.md)