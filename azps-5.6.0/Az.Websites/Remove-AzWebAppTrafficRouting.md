---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
ms.openlocfilehash: 0dda79130d150265d8050fcb5ba951cd243bebda
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990699"
---
# <span data-ttu-id="adb7b-101">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="adb7b-101">Remove-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="adb7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adb7b-102">SYNOPSIS</span></span>
<span data-ttu-id="adb7b-103">Удалите правило маршрутки из слота.</span><span class="sxs-lookup"><span data-stu-id="adb7b-103">Remove a routing Rule from the Slot.</span></span>

## <span data-ttu-id="adb7b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="adb7b-104">SYNTAX</span></span>

```
Remove-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adb7b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="adb7b-105">DESCRIPTION</span></span>
<span data-ttu-id="adb7b-106">С **помощью cmdlet Remove-AzWebAppTrafficRouting** правило маршрутирования удаляется из слота Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="adb7b-106">The **Remove-AzWebAppTrafficRouting** cmdlet removes a routing rule from an Azure Web App Slot.</span></span>

## <span data-ttu-id="adb7b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="adb7b-107">EXAMPLES</span></span>

### <span data-ttu-id="adb7b-108">Пример 1. Удаление определенного правила маршрутки из слота веб-приложения</span><span class="sxs-lookup"><span data-stu-id="adb7b-108">Example 1 Removes the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Remove-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="adb7b-109">Эта команда удаляет правило маршрутки для заданного слота веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="adb7b-109">This command removes a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="adb7b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="adb7b-110">PARAMETERS</span></span>

### <span data-ttu-id="adb7b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adb7b-111">-DefaultProfile</span></span>
<span data-ttu-id="adb7b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="adb7b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adb7b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adb7b-113">-ResourceGroupName</span></span>
<span data-ttu-id="adb7b-114">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="adb7b-114">Resource Group Name</span></span>

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

### <span data-ttu-id="adb7b-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="adb7b-115">-RuleName</span></span>
<span data-ttu-id="adb7b-116">Имя правила</span><span class="sxs-lookup"><span data-stu-id="adb7b-116">Rule Name</span></span>

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

### <span data-ttu-id="adb7b-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="adb7b-117">-WebAppName</span></span>
<span data-ttu-id="adb7b-118">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="adb7b-118">WebApp Name</span></span>

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

### <span data-ttu-id="adb7b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="adb7b-119">-PassThru</span></span>
<span data-ttu-id="adb7b-120">Возвращает объект config с ограничениями доступа.</span><span class="sxs-lookup"><span data-stu-id="adb7b-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="adb7b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="adb7b-121">-Confirm</span></span>
<span data-ttu-id="adb7b-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="adb7b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adb7b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adb7b-123">-WhatIf</span></span>
<span data-ttu-id="adb7b-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adb7b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adb7b-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="adb7b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adb7b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adb7b-126">CommonParameters</span></span>
<span data-ttu-id="adb7b-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adb7b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adb7b-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="adb7b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adb7b-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="adb7b-129">INPUTS</span></span>

### <span data-ttu-id="adb7b-130">Нет</span><span class="sxs-lookup"><span data-stu-id="adb7b-130">None</span></span>

## <span data-ttu-id="adb7b-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="adb7b-131">OUTPUTS</span></span>

### <span data-ttu-id="adb7b-132">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="adb7b-132">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="adb7b-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="adb7b-133">NOTES</span></span>

## <span data-ttu-id="adb7b-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="adb7b-134">RELATED LINKS</span></span>
[<span data-ttu-id="adb7b-135">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="adb7b-135">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="adb7b-136">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="adb7b-136">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="adb7b-137">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="adb7b-137">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)