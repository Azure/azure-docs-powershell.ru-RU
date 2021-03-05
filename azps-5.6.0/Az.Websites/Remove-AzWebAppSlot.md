---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
ms.openlocfilehash: cca1cc480f529c49f679930d9d88f39f69f6e966
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983784"
---
# <span data-ttu-id="7fd66-101">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7fd66-101">Remove-AzWebAppSlot</span></span>

## <span data-ttu-id="7fd66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fd66-102">SYNOPSIS</span></span>

## <span data-ttu-id="7fd66-103">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7fd66-103">SYNTAX</span></span>

### <span data-ttu-id="7fd66-104">S1</span><span class="sxs-lookup"><span data-stu-id="7fd66-104">S1</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fd66-105">S2</span><span class="sxs-lookup"><span data-stu-id="7fd66-105">S2</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fd66-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fd66-106">DESCRIPTION</span></span>
<span data-ttu-id="7fd66-107">С **помощью cmdlet Remove-AzWebAppSlot** удаляется слот Azure Web App при условии, что группа ресурсов и имя веб-приложения были присвоены.</span><span class="sxs-lookup"><span data-stu-id="7fd66-107">The **Remove-AzWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="7fd66-108">Этот cmdlet по умолчанию также удаляет все слоты и метрики.</span><span class="sxs-lookup"><span data-stu-id="7fd66-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="7fd66-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7fd66-109">EXAMPLES</span></span>

### <span data-ttu-id="7fd66-110">Пример 1. Удаление слота веб-приложения</span><span class="sxs-lookup"><span data-stu-id="7fd66-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="7fd66-111">Эта команда удаляет слот Slot001, связанный с веб-приложением ContosoSite, который принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="7fd66-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="7fd66-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7fd66-112">PARAMETERS</span></span>

### <span data-ttu-id="7fd66-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7fd66-113">-AsJob</span></span>
<span data-ttu-id="7fd66-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7fd66-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7fd66-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fd66-115">-DefaultProfile</span></span>
<span data-ttu-id="7fd66-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7fd66-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fd66-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7fd66-117">-Force</span></span>
<span data-ttu-id="7fd66-118">Параметр "Принудительно удалить"</span><span class="sxs-lookup"><span data-stu-id="7fd66-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="7fd66-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7fd66-119">-Name</span></span>
<span data-ttu-id="7fd66-120">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="7fd66-120">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fd66-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fd66-121">-ResourceGroupName</span></span>
<span data-ttu-id="7fd66-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="7fd66-122">Resource Group Name</span></span>

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

### <span data-ttu-id="7fd66-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="7fd66-123">-Slot</span></span>
<span data-ttu-id="7fd66-124">Название слота WebApp</span><span class="sxs-lookup"><span data-stu-id="7fd66-124">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd66-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="7fd66-125">-WebApp</span></span>
<span data-ttu-id="7fd66-126">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="7fd66-126">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fd66-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7fd66-127">-Confirm</span></span>
<span data-ttu-id="7fd66-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7fd66-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fd66-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fd66-129">-WhatIf</span></span>
<span data-ttu-id="7fd66-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7fd66-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fd66-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7fd66-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fd66-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fd66-132">CommonParameters</span></span>
<span data-ttu-id="7fd66-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fd66-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fd66-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fd66-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fd66-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7fd66-135">INPUTS</span></span>

### <span data-ttu-id="7fd66-136">System.String</span><span class="sxs-lookup"><span data-stu-id="7fd66-136">System.String</span></span>

### <span data-ttu-id="7fd66-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="7fd66-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="7fd66-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7fd66-138">OUTPUTS</span></span>

### <span data-ttu-id="7fd66-139">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="7fd66-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="7fd66-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7fd66-140">NOTES</span></span>

## <span data-ttu-id="7fd66-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7fd66-141">RELATED LINKS</span></span>

[<span data-ttu-id="7fd66-142">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7fd66-142">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="7fd66-143">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7fd66-143">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="7fd66-144">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7fd66-144">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="7fd66-145">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7fd66-145">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="7fd66-146">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7fd66-146">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="7fd66-147">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7fd66-147">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="7fd66-148">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7fd66-148">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
