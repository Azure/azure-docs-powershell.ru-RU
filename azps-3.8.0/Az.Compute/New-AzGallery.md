---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
ms.openlocfilehash: d1a25b3e8466c691272f4c556fe728cbce47a718
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065935"
---
# <span data-ttu-id="89ef9-101">New-AzGallery</span><span class="sxs-lookup"><span data-stu-id="89ef9-101">New-AzGallery</span></span>

## <span data-ttu-id="89ef9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="89ef9-102">SYNOPSIS</span></span>
<span data-ttu-id="89ef9-103">Создание коллекции.</span><span class="sxs-lookup"><span data-stu-id="89ef9-103">Create a gallery.</span></span>

## <span data-ttu-id="89ef9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="89ef9-104">SYNTAX</span></span>

```
New-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Location] <String>
 [-Description <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89ef9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89ef9-105">DESCRIPTION</span></span>
<span data-ttu-id="89ef9-106">Создание коллекции.</span><span class="sxs-lookup"><span data-stu-id="89ef9-106">Create a gallery.</span></span>

## <span data-ttu-id="89ef9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="89ef9-107">EXAMPLES</span></span>

### <span data-ttu-id="89ef9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="89ef9-108">Example 1</span></span>
```powershell
PS C:\> New-AzGallery -ResourceGroupName $rgname -Name $galleryName -Location $location -Description $galleryDescription
```

<span data-ttu-id="89ef9-109">Создание коллекции.</span><span class="sxs-lookup"><span data-stu-id="89ef9-109">Create a gallery.</span></span>

## <span data-ttu-id="89ef9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="89ef9-110">PARAMETERS</span></span>

### <span data-ttu-id="89ef9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89ef9-111">-AsJob</span></span>
<span data-ttu-id="89ef9-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="89ef9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="89ef9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89ef9-113">-DefaultProfile</span></span>
<span data-ttu-id="89ef9-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="89ef9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89ef9-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="89ef9-115">-Description</span></span>
<span data-ttu-id="89ef9-116">Описание ресурса коллекции.</span><span class="sxs-lookup"><span data-stu-id="89ef9-116">The description of the gallery resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89ef9-117">-Location</span><span class="sxs-lookup"><span data-stu-id="89ef9-117">-Location</span></span>
<span data-ttu-id="89ef9-118">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="89ef9-118">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89ef9-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="89ef9-119">-Name</span></span>
<span data-ttu-id="89ef9-120">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="89ef9-120">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89ef9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89ef9-121">-ResourceGroupName</span></span>
<span data-ttu-id="89ef9-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="89ef9-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89ef9-123">-Тег</span><span class="sxs-lookup"><span data-stu-id="89ef9-123">-Tag</span></span>
<span data-ttu-id="89ef9-124">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="89ef9-124">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89ef9-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89ef9-125">-Confirm</span></span>
<span data-ttu-id="89ef9-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="89ef9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89ef9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89ef9-127">-WhatIf</span></span>
<span data-ttu-id="89ef9-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="89ef9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89ef9-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="89ef9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89ef9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89ef9-130">CommonParameters</span></span>
<span data-ttu-id="89ef9-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="89ef9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89ef9-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89ef9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89ef9-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="89ef9-133">INPUTS</span></span>

### <span data-ttu-id="89ef9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="89ef9-134">System.String</span></span>

### <span data-ttu-id="89ef9-135">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="89ef9-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="89ef9-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="89ef9-136">OUTPUTS</span></span>

### <span data-ttu-id="89ef9-137">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="89ef9-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="89ef9-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="89ef9-138">NOTES</span></span>

## <span data-ttu-id="89ef9-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89ef9-139">RELATED LINKS</span></span>
