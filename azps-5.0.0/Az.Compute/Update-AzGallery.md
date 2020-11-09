---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
ms.openlocfilehash: 32628ff27485f70f9451a5ea331d8d3d60824cc4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311939"
---
# <span data-ttu-id="0c99e-101">Update-AzGallery</span><span class="sxs-lookup"><span data-stu-id="0c99e-101">Update-AzGallery</span></span>

## <span data-ttu-id="0c99e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0c99e-102">SYNOPSIS</span></span>
<span data-ttu-id="0c99e-103">Обновление коллекции.</span><span class="sxs-lookup"><span data-stu-id="0c99e-103">Update a gallery.</span></span>

## <span data-ttu-id="0c99e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0c99e-104">SYNTAX</span></span>

### <span data-ttu-id="0c99e-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0c99e-105">DefaultParameter (Default)</span></span>
```
Update-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Description <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c99e-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="0c99e-106">ResourceIdParameter</span></span>
```
Update-AzGallery [-ResourceId] <String> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c99e-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="0c99e-107">ObjectParameter</span></span>
```
Update-AzGallery [-InputObject] <PSGallery> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c99e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c99e-108">DESCRIPTION</span></span>
<span data-ttu-id="0c99e-109">Обновление коллекции.</span><span class="sxs-lookup"><span data-stu-id="0c99e-109">Update a gallery.</span></span>

## <span data-ttu-id="0c99e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0c99e-110">EXAMPLES</span></span>

### <span data-ttu-id="0c99e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0c99e-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGallery -ResourceGroupName $rgname -Name $galleryName -Description $galleryDescription
```

<span data-ttu-id="0c99e-112">Обновление коллекции.</span><span class="sxs-lookup"><span data-stu-id="0c99e-112">Update a gallery.</span></span>

## <span data-ttu-id="0c99e-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0c99e-113">PARAMETERS</span></span>

### <span data-ttu-id="0c99e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c99e-114">-AsJob</span></span>
<span data-ttu-id="0c99e-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0c99e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0c99e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c99e-116">-DefaultProfile</span></span>
<span data-ttu-id="0c99e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0c99e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c99e-118">-Описание</span><span class="sxs-lookup"><span data-stu-id="0c99e-118">-Description</span></span>
<span data-ttu-id="0c99e-119">Описание ресурса коллекции.</span><span class="sxs-lookup"><span data-stu-id="0c99e-119">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="0c99e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c99e-120">-InputObject</span></span>
<span data-ttu-id="0c99e-121">Объект коллекции PS.</span><span class="sxs-lookup"><span data-stu-id="0c99e-121">The PS Gallery Object.</span></span>

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

### <span data-ttu-id="0c99e-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0c99e-122">-Name</span></span>
<span data-ttu-id="0c99e-123">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="0c99e-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="0c99e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c99e-124">-ResourceGroupName</span></span>
<span data-ttu-id="0c99e-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0c99e-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="0c99e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c99e-126">-ResourceId</span></span>
<span data-ttu-id="0c99e-127">Идентификатор ресурса для коллекции</span><span class="sxs-lookup"><span data-stu-id="0c99e-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="0c99e-128">-Тег</span><span class="sxs-lookup"><span data-stu-id="0c99e-128">-Tag</span></span>
<span data-ttu-id="0c99e-129">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="0c99e-129">Resource tags</span></span>

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

### <span data-ttu-id="0c99e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c99e-130">-Confirm</span></span>
<span data-ttu-id="0c99e-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0c99e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c99e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c99e-132">-WhatIf</span></span>
<span data-ttu-id="0c99e-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0c99e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c99e-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0c99e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c99e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c99e-135">CommonParameters</span></span>
<span data-ttu-id="0c99e-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0c99e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c99e-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c99e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c99e-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0c99e-138">INPUTS</span></span>

### <span data-ttu-id="0c99e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0c99e-139">System.String</span></span>

### <span data-ttu-id="0c99e-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="0c99e-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

### <span data-ttu-id="0c99e-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0c99e-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0c99e-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c99e-142">OUTPUTS</span></span>

### <span data-ttu-id="0c99e-143">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="0c99e-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="0c99e-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="0c99e-144">NOTES</span></span>

## <span data-ttu-id="0c99e-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c99e-145">RELATED LINKS</span></span>
