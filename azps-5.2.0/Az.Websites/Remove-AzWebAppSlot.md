---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
ms.openlocfilehash: 88eaf66ea8584913c7816fd12be19509aec49de5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326076"
---
# <span data-ttu-id="0952c-101">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0952c-101">Remove-AzWebAppSlot</span></span>

## <span data-ttu-id="0952c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0952c-102">SYNOPSIS</span></span>

## <span data-ttu-id="0952c-103">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0952c-103">SYNTAX</span></span>

### <span data-ttu-id="0952c-104">S1</span><span class="sxs-lookup"><span data-stu-id="0952c-104">S1</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0952c-105">S2</span><span class="sxs-lookup"><span data-stu-id="0952c-105">S2</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0952c-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0952c-106">DESCRIPTION</span></span>
<span data-ttu-id="0952c-107">С **помощью cmdlet Remove-AzWebAppSlot** удаляется слот Azure Web App при условии, что группа ресурсов и имя веб-приложения были присвоены.</span><span class="sxs-lookup"><span data-stu-id="0952c-107">The **Remove-AzWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="0952c-108">Этот cmdlet по умолчанию также удаляет все слоты и метрики.</span><span class="sxs-lookup"><span data-stu-id="0952c-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="0952c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0952c-109">EXAMPLES</span></span>

### <span data-ttu-id="0952c-110">Пример 1. Удаление слота веб-приложения</span><span class="sxs-lookup"><span data-stu-id="0952c-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="0952c-111">Эта команда удаляет слот Slot001, связанный с веб-приложением ContosoSite, который принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="0952c-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="0952c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0952c-112">PARAMETERS</span></span>

### <span data-ttu-id="0952c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0952c-113">-AsJob</span></span>
<span data-ttu-id="0952c-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0952c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0952c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0952c-115">-DefaultProfile</span></span>
<span data-ttu-id="0952c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0952c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0952c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0952c-117">-Force</span></span>
<span data-ttu-id="0952c-118">Параметр "Принудительно удалить"</span><span class="sxs-lookup"><span data-stu-id="0952c-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="0952c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0952c-119">-Name</span></span>
<span data-ttu-id="0952c-120">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="0952c-120">WebApp Name</span></span>

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

### <span data-ttu-id="0952c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0952c-121">-ResourceGroupName</span></span>
<span data-ttu-id="0952c-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="0952c-122">Resource Group Name</span></span>

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

### <span data-ttu-id="0952c-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="0952c-123">-Slot</span></span>
<span data-ttu-id="0952c-124">Название слота WebApp</span><span class="sxs-lookup"><span data-stu-id="0952c-124">WebApp Slot Name</span></span>

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

### <span data-ttu-id="0952c-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="0952c-125">-WebApp</span></span>
<span data-ttu-id="0952c-126">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="0952c-126">WebApp Object</span></span>

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

### <span data-ttu-id="0952c-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0952c-127">-Confirm</span></span>
<span data-ttu-id="0952c-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0952c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0952c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0952c-129">-WhatIf</span></span>
<span data-ttu-id="0952c-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0952c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0952c-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0952c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0952c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0952c-132">CommonParameters</span></span>
<span data-ttu-id="0952c-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0952c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0952c-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0952c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0952c-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0952c-135">INPUTS</span></span>

### <span data-ttu-id="0952c-136">System.String</span><span class="sxs-lookup"><span data-stu-id="0952c-136">System.String</span></span>

### <span data-ttu-id="0952c-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="0952c-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0952c-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0952c-138">OUTPUTS</span></span>

### <span data-ttu-id="0952c-139">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0952c-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="0952c-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0952c-140">NOTES</span></span>

## <span data-ttu-id="0952c-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0952c-141">RELATED LINKS</span></span>

[<span data-ttu-id="0952c-142">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0952c-142">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="0952c-143">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0952c-143">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="0952c-144">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0952c-144">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="0952c-145">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0952c-145">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="0952c-146">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0952c-146">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="0952c-147">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0952c-147">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="0952c-148">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0952c-148">Get-AzWebApp</span></span>](./Get-AzWebApp.md)