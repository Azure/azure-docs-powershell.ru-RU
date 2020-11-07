---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/switch-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: 9671c2041f767df5066353988eb633318289de47
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913524"
---
# <span data-ttu-id="ae13c-101">Switch-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ae13c-101">Switch-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="ae13c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ae13c-102">SYNOPSIS</span></span>
<span data-ttu-id="ae13c-103">Замена двух слотов с помощью веб-приложения</span><span class="sxs-lookup"><span data-stu-id="ae13c-103">Swap two slots with a Web App</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae13c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ae13c-104">SYNTAX</span></span>

### <span data-ttu-id="ae13c-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="ae13c-105">S1</span></span>
```
Switch-AzureRmWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae13c-106">S2</span><span class="sxs-lookup"><span data-stu-id="ae13c-106">S2</span></span>
```
Switch-AzureRmWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae13c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae13c-107">DESCRIPTION</span></span>
<span data-ttu-id="ae13c-108">**Коммутатор-AzureRmWebAppSlot** переключает два слота, связанных с веб-приложением Azure.</span><span class="sxs-lookup"><span data-stu-id="ae13c-108">The **Switch-AzureRmWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="ae13c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ae13c-109">EXAMPLES</span></span>

### <span data-ttu-id="ae13c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ae13c-110">Example 1</span></span>
```
PS C:\> Switch-AzureRmWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="ae13c-111">Эта команда переключает слот "sourceslot" на "destinationslot" для веб-приложения ContosoWebApp, связанного с группой ресурсов по умолчанию-веб-WestUS</span><span class="sxs-lookup"><span data-stu-id="ae13c-111">This command will switch slot "sourceslot" slot with "destinationslot" for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="ae13c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ae13c-112">PARAMETERS</span></span>

### <span data-ttu-id="ae13c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae13c-113">-DefaultProfile</span></span>
<span data-ttu-id="ae13c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ae13c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae13c-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="ae13c-115">-DestinationSlotName</span></span>
<span data-ttu-id="ae13c-116">Имя конечного слота</span><span class="sxs-lookup"><span data-stu-id="ae13c-116">Destination Slot Name</span></span>

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

### <span data-ttu-id="ae13c-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ae13c-117">-Name</span></span>
<span data-ttu-id="ae13c-118">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="ae13c-118">WebApp Name</span></span>

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

### <span data-ttu-id="ae13c-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="ae13c-119">-PreserveVnet</span></span>
<span data-ttu-id="ae13c-120">Сохранение логического значения для виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="ae13c-120">Preserve Vnet Boolean</span></span>

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

### <span data-ttu-id="ae13c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae13c-121">-ResourceGroupName</span></span>
<span data-ttu-id="ae13c-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ae13c-122">Resource Group Name</span></span>

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

### <span data-ttu-id="ae13c-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="ae13c-123">-SourceSlotName</span></span>
<span data-ttu-id="ae13c-124">Имя исходного слота</span><span class="sxs-lookup"><span data-stu-id="ae13c-124">Source Slot Name</span></span>

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

### <span data-ttu-id="ae13c-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="ae13c-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="ae13c-126">Замена с помощью команды Предварительный просмотр</span><span class="sxs-lookup"><span data-stu-id="ae13c-126">Swap With Preview Action</span></span>

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

### <span data-ttu-id="ae13c-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ae13c-127">-WebApp</span></span>
<span data-ttu-id="ae13c-128">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="ae13c-128">WebApp Object</span></span>

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

### <span data-ttu-id="ae13c-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae13c-129">-Confirm</span></span>
<span data-ttu-id="ae13c-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ae13c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae13c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae13c-131">-WhatIf</span></span>
<span data-ttu-id="ae13c-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ae13c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae13c-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ae13c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae13c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae13c-134">CommonParameters</span></span>
<span data-ttu-id="ae13c-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ae13c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae13c-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae13c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae13c-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ae13c-137">INPUTS</span></span>

### <span data-ttu-id="ae13c-138">Семейств</span><span class="sxs-lookup"><span data-stu-id="ae13c-138">Site</span></span>
<span data-ttu-id="ae13c-139">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="ae13c-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ae13c-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae13c-140">OUTPUTS</span></span>

## <span data-ttu-id="ae13c-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="ae13c-141">NOTES</span></span>

## <span data-ttu-id="ae13c-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae13c-142">RELATED LINKS</span></span>

