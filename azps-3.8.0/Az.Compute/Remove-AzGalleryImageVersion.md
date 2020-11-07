---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
ms.openlocfilehash: addf292e2a73b27f6e1e40258c0d8c60e54cfaed
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93913050"
---
# <span data-ttu-id="98c83-101">Remove-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="98c83-101">Remove-AzGalleryImageVersion</span></span>

## <span data-ttu-id="98c83-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="98c83-102">SYNOPSIS</span></span>
<span data-ttu-id="98c83-103">Удалить версию картинки из коллекции.</span><span class="sxs-lookup"><span data-stu-id="98c83-103">Delete a gallery image version.</span></span>

## <span data-ttu-id="98c83-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="98c83-104">SYNTAX</span></span>

### <span data-ttu-id="98c83-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="98c83-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98c83-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="98c83-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98c83-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="98c83-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98c83-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98c83-108">DESCRIPTION</span></span>
<span data-ttu-id="98c83-109">Удалить версию картинки из коллекции.</span><span class="sxs-lookup"><span data-stu-id="98c83-109">Delete a gallery image version.</span></span>

## <span data-ttu-id="98c83-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="98c83-110">EXAMPLES</span></span>

### <span data-ttu-id="98c83-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="98c83-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -ImageDefinitionName $image -GalleryImageVersionName $version
```

<span data-ttu-id="98c83-112">Удаление указанной версии изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="98c83-112">Delete the given gallery image version.</span></span>

## <span data-ttu-id="98c83-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="98c83-113">PARAMETERS</span></span>

### <span data-ttu-id="98c83-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98c83-114">-AsJob</span></span>
<span data-ttu-id="98c83-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="98c83-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="98c83-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98c83-116">-DefaultProfile</span></span>
<span data-ttu-id="98c83-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="98c83-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98c83-118">-Force</span><span class="sxs-lookup"><span data-stu-id="98c83-118">-Force</span></span>
<span data-ttu-id="98c83-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="98c83-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="98c83-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="98c83-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="98c83-121">Имя определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="98c83-121">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98c83-122">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="98c83-122">-GalleryName</span></span>
<span data-ttu-id="98c83-123">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="98c83-123">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98c83-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98c83-124">-InputObject</span></span>
<span data-ttu-id="98c83-125">Объект версии изображения в коллекции PS</span><span class="sxs-lookup"><span data-stu-id="98c83-125">The PS Gallery Image Version Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion
Parameter Sets: ObjectParameter
Aliases: GalleryImageVersion

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98c83-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="98c83-126">-Name</span></span>
<span data-ttu-id="98c83-127">Имя версии изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="98c83-127">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98c83-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98c83-128">-ResourceGroupName</span></span>
<span data-ttu-id="98c83-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="98c83-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="98c83-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98c83-130">-ResourceId</span></span>
<span data-ttu-id="98c83-131">Идентификатор ресурса для версии изображения коллекции</span><span class="sxs-lookup"><span data-stu-id="98c83-131">The resource ID for gallery image version</span></span>

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

### <span data-ttu-id="98c83-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98c83-132">-Confirm</span></span>
<span data-ttu-id="98c83-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="98c83-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98c83-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98c83-134">-WhatIf</span></span>
<span data-ttu-id="98c83-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="98c83-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98c83-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="98c83-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98c83-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98c83-137">CommonParameters</span></span>
<span data-ttu-id="98c83-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="98c83-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98c83-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98c83-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98c83-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="98c83-140">INPUTS</span></span>

### <span data-ttu-id="98c83-141">System. String</span><span class="sxs-lookup"><span data-stu-id="98c83-141">System.String</span></span>

### <span data-ttu-id="98c83-142">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="98c83-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="98c83-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="98c83-143">OUTPUTS</span></span>

### <span data-ttu-id="98c83-144">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="98c83-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="98c83-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="98c83-145">NOTES</span></span>

## <span data-ttu-id="98c83-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98c83-146">RELATED LINKS</span></span>
