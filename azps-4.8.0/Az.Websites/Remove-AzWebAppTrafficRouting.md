---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
ms.openlocfilehash: 0dda79130d150265d8050fcb5ba951cd243bebda
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079299"
---
# <span data-ttu-id="7e72e-101">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="7e72e-101">Remove-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="7e72e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7e72e-102">SYNOPSIS</span></span>
<span data-ttu-id="7e72e-103">Удалите правило маршрутизации из гнезда.</span><span class="sxs-lookup"><span data-stu-id="7e72e-103">Remove a routing Rule from the Slot.</span></span>

## <span data-ttu-id="7e72e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7e72e-104">SYNTAX</span></span>

```
Remove-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e72e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e72e-105">DESCRIPTION</span></span>
<span data-ttu-id="7e72e-106">Командлет **Remove-AzWebAppTrafficRouting** удаляет правило маршрутизации из слота веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="7e72e-106">The **Remove-AzWebAppTrafficRouting** cmdlet removes a routing rule from an Azure Web App Slot.</span></span>

## <span data-ttu-id="7e72e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7e72e-107">EXAMPLES</span></span>

### <span data-ttu-id="7e72e-108">В примере 1 удаляется конкретное правило маршрутизации из webapp Slot.</span><span class="sxs-lookup"><span data-stu-id="7e72e-108">Example 1 Removes the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Remove-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="7e72e-109">Эта команда удаляет правило маршрутизации для заданной webapp ячейки.</span><span class="sxs-lookup"><span data-stu-id="7e72e-109">This command removes a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="7e72e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7e72e-110">PARAMETERS</span></span>

### <span data-ttu-id="7e72e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e72e-111">-DefaultProfile</span></span>
<span data-ttu-id="7e72e-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7e72e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e72e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e72e-113">-ResourceGroupName</span></span>
<span data-ttu-id="7e72e-114">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="7e72e-114">Resource Group Name</span></span>

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

### <span data-ttu-id="7e72e-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="7e72e-115">-RuleName</span></span>
<span data-ttu-id="7e72e-116">Имя правила</span><span class="sxs-lookup"><span data-stu-id="7e72e-116">Rule Name</span></span>

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

### <span data-ttu-id="7e72e-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="7e72e-117">-WebAppName</span></span>
<span data-ttu-id="7e72e-118">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="7e72e-118">WebApp Name</span></span>

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

### <span data-ttu-id="7e72e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e72e-119">-PassThru</span></span>
<span data-ttu-id="7e72e-120">Возврат объекта конфигурации ограничения доступа.</span><span class="sxs-lookup"><span data-stu-id="7e72e-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="7e72e-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e72e-121">-Confirm</span></span>
<span data-ttu-id="7e72e-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7e72e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e72e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e72e-123">-WhatIf</span></span>
<span data-ttu-id="7e72e-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7e72e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e72e-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7e72e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e72e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e72e-126">CommonParameters</span></span>
<span data-ttu-id="7e72e-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7e72e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e72e-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e72e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e72e-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7e72e-129">INPUTS</span></span>

### <span data-ttu-id="7e72e-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="7e72e-130">None</span></span>

## <span data-ttu-id="7e72e-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e72e-131">OUTPUTS</span></span>

### <span data-ttu-id="7e72e-132">Microsoft. Azure. Management. website. Models. RampUpRule</span><span class="sxs-lookup"><span data-stu-id="7e72e-132">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="7e72e-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="7e72e-133">NOTES</span></span>

## <span data-ttu-id="7e72e-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e72e-134">RELATED LINKS</span></span>
[<span data-ttu-id="7e72e-135">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="7e72e-135">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="7e72e-136">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="7e72e-136">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="7e72e-137">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="7e72e-137">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)