---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/switch-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Switch-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Switch-AzureRmWebAppSlot.md
ms.openlocfilehash: e1cfb3e70ab8176cfd686dc404b13dbbfb23e4e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558700"
---
# <span data-ttu-id="ed540-101">Switch-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ed540-101">Switch-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="ed540-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ed540-102">SYNOPSIS</span></span>
<span data-ttu-id="ed540-103">Замена двух слотов с помощью веб-приложения</span><span class="sxs-lookup"><span data-stu-id="ed540-103">Swap two slots with a Web App</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed540-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ed540-104">SYNTAX</span></span>

### <span data-ttu-id="ed540-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="ed540-105">S1</span></span>
```
Switch-AzureRmWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed540-106">S2</span><span class="sxs-lookup"><span data-stu-id="ed540-106">S2</span></span>
```
Switch-AzureRmWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed540-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed540-107">DESCRIPTION</span></span>
<span data-ttu-id="ed540-108">**Коммутатор-AzureRmWebAppSlot** переключает два слота, связанных с веб-приложением Azure.</span><span class="sxs-lookup"><span data-stu-id="ed540-108">The **Switch-AzureRmWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="ed540-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ed540-109">EXAMPLES</span></span>

### <span data-ttu-id="ed540-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ed540-110">Example 1</span></span>
```
PS C:\> Switch-AzureRmWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="ed540-111">Эта команда переключает слот "sourceslot" на "destinationslot" для веб-приложения ContosoWebApp, связанного с группой ресурсов по умолчанию-веб-WestUS</span><span class="sxs-lookup"><span data-stu-id="ed540-111">This command will switch slot "sourceslot" slot with "destinationslot" for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="ed540-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ed540-112">PARAMETERS</span></span>

### <span data-ttu-id="ed540-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed540-113">-DefaultProfile</span></span>
<span data-ttu-id="ed540-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ed540-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed540-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="ed540-115">-DestinationSlotName</span></span>
<span data-ttu-id="ed540-116">Имя конечного слота</span><span class="sxs-lookup"><span data-stu-id="ed540-116">Destination Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed540-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ed540-117">-Name</span></span>
<span data-ttu-id="ed540-118">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="ed540-118">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed540-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="ed540-119">-PreserveVnet</span></span>
<span data-ttu-id="ed540-120">Сохранение логического значения для виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="ed540-120">Preserve Vnet Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed540-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed540-121">-ResourceGroupName</span></span>
<span data-ttu-id="ed540-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ed540-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed540-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="ed540-123">-SourceSlotName</span></span>
<span data-ttu-id="ed540-124">Имя исходного слота</span><span class="sxs-lookup"><span data-stu-id="ed540-124">Source Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed540-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="ed540-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="ed540-126">Замена с помощью команды Предварительный просмотр</span><span class="sxs-lookup"><span data-stu-id="ed540-126">Swap With Preview Action</span></span>

```yaml
Type: SwapWithPreviewAction
Parameter Sets: (All)
Aliases: 
Accepted values: ApplySlotConfig, CompleteSlotSwap, ResetSlotSwap

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed540-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ed540-127">-WebApp</span></span>
<span data-ttu-id="ed540-128">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="ed540-128">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed540-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed540-129">-Confirm</span></span>
<span data-ttu-id="ed540-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ed540-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed540-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed540-131">-WhatIf</span></span>
<span data-ttu-id="ed540-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ed540-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed540-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ed540-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed540-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed540-134">CommonParameters</span></span>
<span data-ttu-id="ed540-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ed540-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed540-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed540-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed540-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ed540-137">INPUTS</span></span>

### <span data-ttu-id="ed540-138">Семейств</span><span class="sxs-lookup"><span data-stu-id="ed540-138">Site</span></span>
<span data-ttu-id="ed540-139">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="ed540-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ed540-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed540-140">OUTPUTS</span></span>

## <span data-ttu-id="ed540-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="ed540-141">NOTES</span></span>

## <span data-ttu-id="ed540-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed540-142">RELATED LINKS</span></span>

