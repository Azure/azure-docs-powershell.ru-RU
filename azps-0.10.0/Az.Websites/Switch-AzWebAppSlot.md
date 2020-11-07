---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/switch-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Switch-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Switch-AzWebAppSlot.md
ms.openlocfilehash: e30179ce2e9198729771d406d1963ff0048e05b1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910549"
---
# <span data-ttu-id="40484-101">Switch-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="40484-101">Switch-AzWebAppSlot</span></span>

## <span data-ttu-id="40484-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="40484-102">SYNOPSIS</span></span>
<span data-ttu-id="40484-103">Замена двух слотов с помощью веб-приложения</span><span class="sxs-lookup"><span data-stu-id="40484-103">Swap two slots with a Web App</span></span>

## <span data-ttu-id="40484-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="40484-104">SYNTAX</span></span>

### <span data-ttu-id="40484-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="40484-105">S1</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40484-106">S2</span><span class="sxs-lookup"><span data-stu-id="40484-106">S2</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40484-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40484-107">DESCRIPTION</span></span>
<span data-ttu-id="40484-108">**Коммутатор-AzWebAppSlot** переключает два слота, связанных с веб-приложением Azure.</span><span class="sxs-lookup"><span data-stu-id="40484-108">The **Switch-AzWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="40484-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="40484-109">EXAMPLES</span></span>

### <span data-ttu-id="40484-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="40484-110">Example 1</span></span>
```
PS C:\> Switch-AzWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="40484-111">Эта команда переключает слот "sourceslot" на "destinationslot" для веб-приложения ContosoWebApp, связанного с группой ресурсов по умолчанию-веб-WestUS</span><span class="sxs-lookup"><span data-stu-id="40484-111">This command will switch slot "sourceslot" slot with "destinationslot" for for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="40484-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="40484-112">PARAMETERS</span></span>

### <span data-ttu-id="40484-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40484-113">-DefaultProfile</span></span>
<span data-ttu-id="40484-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40484-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40484-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="40484-115">-DestinationSlotName</span></span>
<span data-ttu-id="40484-116">Имя конечного слота</span><span class="sxs-lookup"><span data-stu-id="40484-116">Destination Slot Name</span></span>

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

### <span data-ttu-id="40484-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="40484-117">-Name</span></span>
<span data-ttu-id="40484-118">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="40484-118">WebApp Name</span></span>

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

### <span data-ttu-id="40484-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="40484-119">-PreserveVnet</span></span>
<span data-ttu-id="40484-120">Сохранение логического значения для виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="40484-120">Preserve Vnet Boolean</span></span>

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

### <span data-ttu-id="40484-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40484-121">-ResourceGroupName</span></span>
<span data-ttu-id="40484-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="40484-122">Resource Group Name</span></span>

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

### <span data-ttu-id="40484-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="40484-123">-SourceSlotName</span></span>
<span data-ttu-id="40484-124">Имя исходного слота</span><span class="sxs-lookup"><span data-stu-id="40484-124">Source Slot Name</span></span>

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

### <span data-ttu-id="40484-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="40484-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="40484-126">Замена с помощью команды Предварительный просмотр</span><span class="sxs-lookup"><span data-stu-id="40484-126">Swap With Preview Action</span></span>

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

### <span data-ttu-id="40484-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="40484-127">-WebApp</span></span>
<span data-ttu-id="40484-128">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="40484-128">WebApp Object</span></span>

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

### <span data-ttu-id="40484-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40484-129">-Confirm</span></span>
<span data-ttu-id="40484-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="40484-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40484-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40484-131">-WhatIf</span></span>
<span data-ttu-id="40484-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="40484-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40484-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="40484-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40484-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40484-134">CommonParameters</span></span>
<span data-ttu-id="40484-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="40484-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40484-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40484-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40484-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="40484-137">INPUTS</span></span>

### <span data-ttu-id="40484-138">Семейств</span><span class="sxs-lookup"><span data-stu-id="40484-138">Site</span></span>
<span data-ttu-id="40484-139">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="40484-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="40484-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="40484-140">OUTPUTS</span></span>

## <span data-ttu-id="40484-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="40484-141">NOTES</span></span>

## <span data-ttu-id="40484-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40484-142">RELATED LINKS</span></span>

