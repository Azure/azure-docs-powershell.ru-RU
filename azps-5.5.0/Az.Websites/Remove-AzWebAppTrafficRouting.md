---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
ms.openlocfilehash: 0dda79130d150265d8050fcb5ba951cd243bebda
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242896"
---
# <span data-ttu-id="c5575-101">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="c5575-101">Remove-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="c5575-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5575-102">SYNOPSIS</span></span>
<span data-ttu-id="c5575-103">Удалите правило маршрутки из слота.</span><span class="sxs-lookup"><span data-stu-id="c5575-103">Remove a routing Rule from the Slot.</span></span>

## <span data-ttu-id="c5575-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c5575-104">SYNTAX</span></span>

```
Remove-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5575-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5575-105">DESCRIPTION</span></span>
<span data-ttu-id="c5575-106">С **помощью cmdlet Remove-AzWebAppTrafficRouting** правило маршрутирования удаляется из слота Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c5575-106">The **Remove-AzWebAppTrafficRouting** cmdlet removes a routing rule from an Azure Web App Slot.</span></span>

## <span data-ttu-id="c5575-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c5575-107">EXAMPLES</span></span>

### <span data-ttu-id="c5575-108">Пример 1. Удаление определенного правила маршрутки из слота веб-приложения</span><span class="sxs-lookup"><span data-stu-id="c5575-108">Example 1 Removes the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Remove-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="c5575-109">Эта команда удаляет правило маршрутки для заданного слота веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="c5575-109">This command removes a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="c5575-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5575-110">PARAMETERS</span></span>

### <span data-ttu-id="c5575-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5575-111">-DefaultProfile</span></span>
<span data-ttu-id="c5575-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c5575-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5575-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5575-113">-ResourceGroupName</span></span>
<span data-ttu-id="c5575-114">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c5575-114">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5575-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="c5575-115">-RuleName</span></span>
<span data-ttu-id="c5575-116">Имя правила</span><span class="sxs-lookup"><span data-stu-id="c5575-116">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5575-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="c5575-117">-WebAppName</span></span>
<span data-ttu-id="c5575-118">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="c5575-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5575-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c5575-119">-PassThru</span></span>
<span data-ttu-id="c5575-120">Возвращает объект config с ограничением доступа.</span><span class="sxs-lookup"><span data-stu-id="c5575-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="c5575-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5575-121">-Confirm</span></span>
<span data-ttu-id="c5575-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5575-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5575-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5575-123">-WhatIf</span></span>
<span data-ttu-id="c5575-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5575-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5575-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c5575-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5575-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5575-126">CommonParameters</span></span>
<span data-ttu-id="c5575-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5575-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5575-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5575-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5575-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5575-129">INPUTS</span></span>

### <span data-ttu-id="c5575-130">Нет</span><span class="sxs-lookup"><span data-stu-id="c5575-130">None</span></span>

## <span data-ttu-id="c5575-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c5575-131">OUTPUTS</span></span>

### <span data-ttu-id="c5575-132">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="c5575-132">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="c5575-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c5575-133">NOTES</span></span>

## <span data-ttu-id="c5575-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c5575-134">RELATED LINKS</span></span>
[<span data-ttu-id="c5575-135">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="c5575-135">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="c5575-136">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="c5575-136">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="c5575-137">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="c5575-137">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)