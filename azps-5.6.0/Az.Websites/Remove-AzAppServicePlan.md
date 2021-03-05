---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
ms.openlocfilehash: acd6b0735cb0ecf38ecef3448d02c4349954f405
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987118"
---
# <span data-ttu-id="c09c4-101">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c09c4-101">Remove-AzAppServicePlan</span></span>

## <span data-ttu-id="c09c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c09c4-102">SYNOPSIS</span></span>
<span data-ttu-id="c09c4-103">Удаляет план службы приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="c09c4-103">Removes an Azure App Service plan.</span></span>

## <span data-ttu-id="c09c4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c09c4-104">SYNTAX</span></span>

### <span data-ttu-id="c09c4-105">S1</span><span class="sxs-lookup"><span data-stu-id="c09c4-105">S1</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c09c4-106">S2</span><span class="sxs-lookup"><span data-stu-id="c09c4-106">S2</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c09c4-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c09c4-107">DESCRIPTION</span></span>
<span data-ttu-id="c09c4-108">С **помощью cmdlet Remove-AzAppServicePlan** удаляется план службы приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="c09c4-108">The **Remove-AzAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="c09c4-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c09c4-109">EXAMPLES</span></span>

### <span data-ttu-id="c09c4-110">Пример 1. Удаление плана службы приложений</span><span class="sxs-lookup"><span data-stu-id="c09c4-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="c09c4-111">Эта команда удаляет план службы приложений Azure ContosoASP, принадлежащий группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="c09c4-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="c09c4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c09c4-112">PARAMETERS</span></span>

### <span data-ttu-id="c09c4-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c09c4-113">-AppServicePlan</span></span>
<span data-ttu-id="c09c4-114">Объект плана обслуживания приложения</span><span class="sxs-lookup"><span data-stu-id="c09c4-114">App Service Plan Object</span></span>

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

### <span data-ttu-id="c09c4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c09c4-115">-AsJob</span></span>
<span data-ttu-id="c09c4-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c09c4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c09c4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c09c4-117">-DefaultProfile</span></span>
<span data-ttu-id="c09c4-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c09c4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c09c4-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c09c4-119">-Force</span></span>
<span data-ttu-id="c09c4-120">Параметр "Принудительно удалить"</span><span class="sxs-lookup"><span data-stu-id="c09c4-120">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="c09c4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c09c4-121">-Name</span></span>
<span data-ttu-id="c09c4-122">Имя плана службы приложений</span><span class="sxs-lookup"><span data-stu-id="c09c4-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="c09c4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c09c4-123">-ResourceGroupName</span></span>
<span data-ttu-id="c09c4-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c09c4-124">Resource Group Name</span></span>

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

### <span data-ttu-id="c09c4-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c09c4-125">-Confirm</span></span>
<span data-ttu-id="c09c4-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c09c4-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c09c4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c09c4-127">-WhatIf</span></span>
<span data-ttu-id="c09c4-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c09c4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c09c4-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c09c4-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c09c4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c09c4-130">CommonParameters</span></span>
<span data-ttu-id="c09c4-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c09c4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c09c4-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c09c4-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c09c4-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c09c4-133">INPUTS</span></span>

### <span data-ttu-id="c09c4-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c09c4-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="c09c4-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c09c4-135">OUTPUTS</span></span>

### <span data-ttu-id="c09c4-136">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c09c4-136">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="c09c4-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c09c4-137">NOTES</span></span>

## <span data-ttu-id="c09c4-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c09c4-138">RELATED LINKS</span></span>

[<span data-ttu-id="c09c4-139">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c09c4-139">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="c09c4-140">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c09c4-140">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="c09c4-141">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c09c4-141">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


