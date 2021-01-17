---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/switch-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
ms.openlocfilehash: 1f1bcd7b0eb7318746f2f5a48ce5ccd58941196c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416780"
---
# <span data-ttu-id="53a94-101">Switch-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="53a94-101">Switch-AzWebAppSlot</span></span>

## <span data-ttu-id="53a94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53a94-102">SYNOPSIS</span></span>
<span data-ttu-id="53a94-103">Замена двух слотов веб-приложением</span><span class="sxs-lookup"><span data-stu-id="53a94-103">Swap two slots with a Web App</span></span>

## <span data-ttu-id="53a94-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="53a94-104">SYNTAX</span></span>

### <span data-ttu-id="53a94-105">S1</span><span class="sxs-lookup"><span data-stu-id="53a94-105">S1</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53a94-106">S2</span><span class="sxs-lookup"><span data-stu-id="53a94-106">S2</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53a94-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="53a94-107">DESCRIPTION</span></span>
<span data-ttu-id="53a94-108">**Переключение-AzWebAppSlot** переключает два слота, связанных с Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="53a94-108">The **Switch-AzWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="53a94-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="53a94-109">EXAMPLES</span></span>

### <span data-ttu-id="53a94-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="53a94-110">Example 1</span></span>
```
PS C:\> Switch-AzWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="53a94-111">Эта команда переключает слот sourceslot с destinationslot на web App ContosoWebApp, связанный с группой ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="53a94-111">This command will switch slot "sourceslot" slot with "destinationslot" the Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="53a94-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53a94-112">PARAMETERS</span></span>

### <span data-ttu-id="53a94-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53a94-113">-DefaultProfile</span></span>
<span data-ttu-id="53a94-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="53a94-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53a94-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="53a94-115">-DestinationSlotName</span></span>
<span data-ttu-id="53a94-116">Название места назначения</span><span class="sxs-lookup"><span data-stu-id="53a94-116">Destination Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53a94-117">-Name</span><span class="sxs-lookup"><span data-stu-id="53a94-117">-Name</span></span>
<span data-ttu-id="53a94-118">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="53a94-118">WebApp Name</span></span>

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

### <span data-ttu-id="53a94-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="53a94-119">-PreserveVnet</span></span>
<span data-ttu-id="53a94-120">Сохранение буллеа в Vnet</span><span class="sxs-lookup"><span data-stu-id="53a94-120">Preserve Vnet Boolean</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53a94-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53a94-121">-ResourceGroupName</span></span>
<span data-ttu-id="53a94-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="53a94-122">Resource Group Name</span></span>

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

### <span data-ttu-id="53a94-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="53a94-123">-SourceSlotName</span></span>
<span data-ttu-id="53a94-124">Имя источника слота</span><span class="sxs-lookup"><span data-stu-id="53a94-124">Source Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53a94-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="53a94-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="53a94-126">Обмен с помощью предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="53a94-126">Swap With Preview Action</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.WebApps.Utilities.SwapWithPreviewAction]
Parameter Sets: (All)
Aliases:
Accepted values: ApplySlotConfig, CompleteSlotSwap, ResetSlotSwap

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53a94-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="53a94-127">-WebApp</span></span>
<span data-ttu-id="53a94-128">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="53a94-128">WebApp Object</span></span>

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

### <span data-ttu-id="53a94-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53a94-129">-Confirm</span></span>
<span data-ttu-id="53a94-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="53a94-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53a94-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53a94-131">-WhatIf</span></span>
<span data-ttu-id="53a94-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53a94-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53a94-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="53a94-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53a94-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53a94-134">CommonParameters</span></span>
<span data-ttu-id="53a94-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53a94-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53a94-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53a94-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53a94-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53a94-137">INPUTS</span></span>

### <span data-ttu-id="53a94-138">System.String</span><span class="sxs-lookup"><span data-stu-id="53a94-138">System.String</span></span>

### <span data-ttu-id="53a94-139">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="53a94-139">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="53a94-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="53a94-140">OUTPUTS</span></span>

### <span data-ttu-id="53a94-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="53a94-141">System.Void</span></span>

## <span data-ttu-id="53a94-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="53a94-142">NOTES</span></span>

## <span data-ttu-id="53a94-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="53a94-143">RELATED LINKS</span></span>
