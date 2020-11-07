---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGallery.md
ms.openlocfilehash: 5d8ed5a26e141d0ae8d6eb7494a76d8c53590d29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733878"
---
# <span data-ttu-id="366df-101">Update-AzureRmGallery</span><span class="sxs-lookup"><span data-stu-id="366df-101">Update-AzureRmGallery</span></span>

## <span data-ttu-id="366df-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="366df-102">SYNOPSIS</span></span>
<span data-ttu-id="366df-103">Обновление коллекции.</span><span class="sxs-lookup"><span data-stu-id="366df-103">Update a gallery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="366df-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="366df-104">SYNTAX</span></span>

### <span data-ttu-id="366df-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="366df-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Description <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="366df-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="366df-106">ResourceIdParameter</span></span>
```
Update-AzureRmGallery [-ResourceId] <String> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="366df-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="366df-107">ObjectParameter</span></span>
```
Update-AzureRmGallery [-InputObject] <PSGallery> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="366df-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="366df-108">DESCRIPTION</span></span>
<span data-ttu-id="366df-109">Обновление коллекции.</span><span class="sxs-lookup"><span data-stu-id="366df-109">Update a gallery.</span></span>

## <span data-ttu-id="366df-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="366df-110">EXAMPLES</span></span>

### <span data-ttu-id="366df-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="366df-111">Example 1</span></span>
```powershell
PS C:\> Update-AzureRmGallery -ResourceGroupName $rgname -Name $galleryName -Description $galleryDescription
```

<span data-ttu-id="366df-112">Обновление коллекции.</span><span class="sxs-lookup"><span data-stu-id="366df-112">Update a gallery.</span></span>

## <span data-ttu-id="366df-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="366df-113">PARAMETERS</span></span>

### <span data-ttu-id="366df-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="366df-114">-AsJob</span></span>
<span data-ttu-id="366df-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="366df-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="366df-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="366df-116">-DefaultProfile</span></span>
<span data-ttu-id="366df-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="366df-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="366df-118">-Описание</span><span class="sxs-lookup"><span data-stu-id="366df-118">-Description</span></span>
<span data-ttu-id="366df-119">Описание ресурса коллекции.</span><span class="sxs-lookup"><span data-stu-id="366df-119">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="366df-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="366df-120">-InputObject</span></span>
<span data-ttu-id="366df-121">Объект коллекции PS.</span><span class="sxs-lookup"><span data-stu-id="366df-121">The PS Gallery Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery
Parameter Sets: ObjectParameter
Aliases: Gallery

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="366df-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="366df-122">-Name</span></span>
<span data-ttu-id="366df-123">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="366df-123">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="366df-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="366df-124">-ResourceGroupName</span></span>
<span data-ttu-id="366df-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="366df-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="366df-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="366df-126">-ResourceId</span></span>
<span data-ttu-id="366df-127">Идентификатор ресурса для коллекции</span><span class="sxs-lookup"><span data-stu-id="366df-127">The resource Id for the gallery</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="366df-128">-Тег</span><span class="sxs-lookup"><span data-stu-id="366df-128">-Tag</span></span>
<span data-ttu-id="366df-129">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="366df-129">Resource tags</span></span>

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

### <span data-ttu-id="366df-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="366df-130">-Confirm</span></span>
<span data-ttu-id="366df-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="366df-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="366df-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="366df-132">-WhatIf</span></span>
<span data-ttu-id="366df-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="366df-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="366df-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="366df-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="366df-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="366df-135">CommonParameters</span></span>
<span data-ttu-id="366df-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="366df-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="366df-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="366df-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="366df-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="366df-138">INPUTS</span></span>

### <span data-ttu-id="366df-139">System. String</span><span class="sxs-lookup"><span data-stu-id="366df-139">System.String</span></span>

### <span data-ttu-id="366df-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="366df-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

### <span data-ttu-id="366df-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="366df-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="366df-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="366df-142">OUTPUTS</span></span>

### <span data-ttu-id="366df-143">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="366df-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="366df-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="366df-144">NOTES</span></span>

## <span data-ttu-id="366df-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="366df-145">RELATED LINKS</span></span>
