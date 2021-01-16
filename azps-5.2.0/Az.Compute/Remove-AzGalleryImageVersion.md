---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
ms.openlocfilehash: 4c4809ed022595af7c0ad977d082c6a52616e920
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412119"
---
# <span data-ttu-id="176e4-101">Remove-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="176e4-101">Remove-AzGalleryImageVersion</span></span>

## <span data-ttu-id="176e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="176e4-102">SYNOPSIS</span></span>
<span data-ttu-id="176e4-103">Удаление версии изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="176e4-103">Delete a gallery image version.</span></span>

## <span data-ttu-id="176e4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="176e4-104">SYNTAX</span></span>

### <span data-ttu-id="176e4-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="176e4-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="176e4-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="176e4-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="176e4-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="176e4-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="176e4-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="176e4-108">DESCRIPTION</span></span>
<span data-ttu-id="176e4-109">Удаление версии изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="176e4-109">Delete a gallery image version.</span></span>

## <span data-ttu-id="176e4-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="176e4-110">EXAMPLES</span></span>

### <span data-ttu-id="176e4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="176e4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $image -Name $version
```

<span data-ttu-id="176e4-112">Удалите версию изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="176e4-112">Delete the given gallery image version.</span></span>

## <span data-ttu-id="176e4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="176e4-113">PARAMETERS</span></span>

### <span data-ttu-id="176e4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="176e4-114">-AsJob</span></span>
<span data-ttu-id="176e4-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="176e4-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="176e4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="176e4-116">-DefaultProfile</span></span>
<span data-ttu-id="176e4-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="176e4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="176e4-118">-Force</span><span class="sxs-lookup"><span data-stu-id="176e4-118">-Force</span></span>
<span data-ttu-id="176e4-119">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="176e4-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="176e4-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="176e4-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="176e4-121">Имя определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="176e4-121">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="176e4-122">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="176e4-122">-GalleryName</span></span>
<span data-ttu-id="176e4-123">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="176e4-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="176e4-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="176e4-124">-InputObject</span></span>
<span data-ttu-id="176e4-125">Объект версии изображения коллекции PS</span><span class="sxs-lookup"><span data-stu-id="176e4-125">The PS Gallery Image Version Object</span></span>

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

### <span data-ttu-id="176e4-126">-Name</span><span class="sxs-lookup"><span data-stu-id="176e4-126">-Name</span></span>
<span data-ttu-id="176e4-127">Имя версии изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="176e4-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="176e4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="176e4-128">-ResourceGroupName</span></span>
<span data-ttu-id="176e4-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="176e4-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="176e4-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="176e4-130">-ResourceId</span></span>
<span data-ttu-id="176e4-131">ИД ресурса для версии изображения коллекции</span><span class="sxs-lookup"><span data-stu-id="176e4-131">The resource ID for gallery image version</span></span>

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

### <span data-ttu-id="176e4-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="176e4-132">-Confirm</span></span>
<span data-ttu-id="176e4-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="176e4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="176e4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="176e4-134">-WhatIf</span></span>
<span data-ttu-id="176e4-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="176e4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="176e4-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="176e4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="176e4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="176e4-137">CommonParameters</span></span>
<span data-ttu-id="176e4-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="176e4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="176e4-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="176e4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="176e4-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="176e4-140">INPUTS</span></span>

### <span data-ttu-id="176e4-141">System.String</span><span class="sxs-lookup"><span data-stu-id="176e4-141">System.String</span></span>

### <span data-ttu-id="176e4-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="176e4-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="176e4-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="176e4-143">OUTPUTS</span></span>

### <span data-ttu-id="176e4-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="176e4-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="176e4-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="176e4-145">NOTES</span></span>

## <span data-ttu-id="176e4-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="176e4-146">RELATED LINKS</span></span>
