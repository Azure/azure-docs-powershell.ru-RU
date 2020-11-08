---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
ms.openlocfilehash: d1a25b3e8466c691272f4c556fe728cbce47a718
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079135"
---
# <span data-ttu-id="525bc-101">New-AzGallery</span><span class="sxs-lookup"><span data-stu-id="525bc-101">New-AzGallery</span></span>

## <span data-ttu-id="525bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="525bc-102">SYNOPSIS</span></span>
<span data-ttu-id="525bc-103">Создание коллекции.</span><span class="sxs-lookup"><span data-stu-id="525bc-103">Create a gallery.</span></span>

## <span data-ttu-id="525bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="525bc-104">SYNTAX</span></span>

```
New-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Location] <String>
 [-Description <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="525bc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="525bc-105">DESCRIPTION</span></span>
<span data-ttu-id="525bc-106">Создание коллекции.</span><span class="sxs-lookup"><span data-stu-id="525bc-106">Create a gallery.</span></span>

## <span data-ttu-id="525bc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="525bc-107">EXAMPLES</span></span>

### <span data-ttu-id="525bc-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="525bc-108">Example 1</span></span>
```powershell
PS C:\> New-AzGallery -ResourceGroupName $rgname -Name $galleryName -Location $location -Description $galleryDescription
```

<span data-ttu-id="525bc-109">Создание коллекции.</span><span class="sxs-lookup"><span data-stu-id="525bc-109">Create a gallery.</span></span>

## <span data-ttu-id="525bc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="525bc-110">PARAMETERS</span></span>

### <span data-ttu-id="525bc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="525bc-111">-AsJob</span></span>
<span data-ttu-id="525bc-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="525bc-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="525bc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="525bc-113">-DefaultProfile</span></span>
<span data-ttu-id="525bc-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="525bc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="525bc-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="525bc-115">-Description</span></span>
<span data-ttu-id="525bc-116">Описание ресурса коллекции.</span><span class="sxs-lookup"><span data-stu-id="525bc-116">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="525bc-117">-Location</span><span class="sxs-lookup"><span data-stu-id="525bc-117">-Location</span></span>
<span data-ttu-id="525bc-118">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="525bc-118">Resource location</span></span>

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

### <span data-ttu-id="525bc-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="525bc-119">-Name</span></span>
<span data-ttu-id="525bc-120">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="525bc-120">The name of the gallery.</span></span>

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

### <span data-ttu-id="525bc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="525bc-121">-ResourceGroupName</span></span>
<span data-ttu-id="525bc-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="525bc-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="525bc-123">-Тег</span><span class="sxs-lookup"><span data-stu-id="525bc-123">-Tag</span></span>
<span data-ttu-id="525bc-124">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="525bc-124">Resource tags</span></span>

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

### <span data-ttu-id="525bc-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="525bc-125">-Confirm</span></span>
<span data-ttu-id="525bc-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="525bc-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="525bc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="525bc-127">-WhatIf</span></span>
<span data-ttu-id="525bc-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="525bc-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="525bc-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="525bc-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="525bc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="525bc-130">CommonParameters</span></span>
<span data-ttu-id="525bc-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="525bc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="525bc-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="525bc-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="525bc-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="525bc-133">INPUTS</span></span>

### <span data-ttu-id="525bc-134">System. String</span><span class="sxs-lookup"><span data-stu-id="525bc-134">System.String</span></span>

### <span data-ttu-id="525bc-135">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="525bc-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="525bc-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="525bc-136">OUTPUTS</span></span>

### <span data-ttu-id="525bc-137">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="525bc-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="525bc-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="525bc-138">NOTES</span></span>

## <span data-ttu-id="525bc-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="525bc-139">RELATED LINKS</span></span>