---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/switch-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
ms.openlocfilehash: 1f1bcd7b0eb7318746f2f5a48ce5ccd58941196c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236906"
---
# <span data-ttu-id="384b5-101">Switch-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="384b5-101">Switch-AzWebAppSlot</span></span>

## <span data-ttu-id="384b5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="384b5-102">SYNOPSIS</span></span>
<span data-ttu-id="384b5-103">Замена двух слотов с помощью веб-приложения</span><span class="sxs-lookup"><span data-stu-id="384b5-103">Swap two slots with a Web App</span></span>

## <span data-ttu-id="384b5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="384b5-104">SYNTAX</span></span>

### <span data-ttu-id="384b5-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="384b5-105">S1</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="384b5-106">S2</span><span class="sxs-lookup"><span data-stu-id="384b5-106">S2</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="384b5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="384b5-107">DESCRIPTION</span></span>
<span data-ttu-id="384b5-108">**Коммутатор-AzWebAppSlot** переключает два слота, связанных с веб-приложением Azure.</span><span class="sxs-lookup"><span data-stu-id="384b5-108">The **Switch-AzWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="384b5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="384b5-109">EXAMPLES</span></span>

### <span data-ttu-id="384b5-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="384b5-110">Example 1</span></span>
```
PS C:\> Switch-AzWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="384b5-111">Эта команда переключает слот "sourceslot" на "destinationslot" веб-приложение ContosoWebApp связанное с группой ресурсов по умолчанию — веб-WestUS</span><span class="sxs-lookup"><span data-stu-id="384b5-111">This command will switch slot "sourceslot" slot with "destinationslot" the Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="384b5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="384b5-112">PARAMETERS</span></span>

### <span data-ttu-id="384b5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="384b5-113">-DefaultProfile</span></span>
<span data-ttu-id="384b5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="384b5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="384b5-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="384b5-115">-DestinationSlotName</span></span>
<span data-ttu-id="384b5-116">Имя конечного слота</span><span class="sxs-lookup"><span data-stu-id="384b5-116">Destination Slot Name</span></span>

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

### <span data-ttu-id="384b5-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="384b5-117">-Name</span></span>
<span data-ttu-id="384b5-118">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="384b5-118">WebApp Name</span></span>

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

### <span data-ttu-id="384b5-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="384b5-119">-PreserveVnet</span></span>
<span data-ttu-id="384b5-120">Сохранение логического значения для виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="384b5-120">Preserve Vnet Boolean</span></span>

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

### <span data-ttu-id="384b5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="384b5-121">-ResourceGroupName</span></span>
<span data-ttu-id="384b5-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="384b5-122">Resource Group Name</span></span>

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

### <span data-ttu-id="384b5-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="384b5-123">-SourceSlotName</span></span>
<span data-ttu-id="384b5-124">Имя исходного слота</span><span class="sxs-lookup"><span data-stu-id="384b5-124">Source Slot Name</span></span>

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

### <span data-ttu-id="384b5-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="384b5-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="384b5-126">Замена с помощью команды Предварительный просмотр</span><span class="sxs-lookup"><span data-stu-id="384b5-126">Swap With Preview Action</span></span>

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

### <span data-ttu-id="384b5-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="384b5-127">-WebApp</span></span>
<span data-ttu-id="384b5-128">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="384b5-128">WebApp Object</span></span>

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

### <span data-ttu-id="384b5-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="384b5-129">-Confirm</span></span>
<span data-ttu-id="384b5-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="384b5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="384b5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="384b5-131">-WhatIf</span></span>
<span data-ttu-id="384b5-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="384b5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="384b5-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="384b5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="384b5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="384b5-134">CommonParameters</span></span>
<span data-ttu-id="384b5-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="384b5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="384b5-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="384b5-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="384b5-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="384b5-137">INPUTS</span></span>

### <span data-ttu-id="384b5-138">System. String</span><span class="sxs-lookup"><span data-stu-id="384b5-138">System.String</span></span>

### <span data-ttu-id="384b5-139">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="384b5-139">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="384b5-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="384b5-140">OUTPUTS</span></span>

### <span data-ttu-id="384b5-141">System. void</span><span class="sxs-lookup"><span data-stu-id="384b5-141">System.Void</span></span>

## <span data-ttu-id="384b5-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="384b5-142">NOTES</span></span>

## <span data-ttu-id="384b5-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="384b5-143">RELATED LINKS</span></span>