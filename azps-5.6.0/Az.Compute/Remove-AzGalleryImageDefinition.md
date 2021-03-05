---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
ms.openlocfilehash: d632f3f9717c706adf2881aa177d9cb7ff2425dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988347"
---
# <span data-ttu-id="defef-101">Remove-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="defef-101">Remove-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="defef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="defef-102">SYNOPSIS</span></span>
<span data-ttu-id="defef-103">Удаление определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="defef-103">Delete a gallery image definition.</span></span>

## <span data-ttu-id="defef-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="defef-104">SYNTAX</span></span>

### <span data-ttu-id="defef-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="defef-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="defef-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="defef-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="defef-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="defef-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-InputObject] <PSGalleryImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="defef-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="defef-108">DESCRIPTION</span></span>
<span data-ttu-id="defef-109">Удаление определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="defef-109">Delete a gallery image definition.</span></span>

## <span data-ttu-id="defef-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="defef-110">EXAMPLES</span></span>

### <span data-ttu-id="defef-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="defef-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $galleryImage
```

<span data-ttu-id="defef-112">Удалите определение изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="defef-112">Remove the gallery image definition.</span></span>

## <span data-ttu-id="defef-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="defef-113">PARAMETERS</span></span>

### <span data-ttu-id="defef-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="defef-114">-AsJob</span></span>
<span data-ttu-id="defef-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="defef-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="defef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="defef-116">-DefaultProfile</span></span>
<span data-ttu-id="defef-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="defef-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="defef-118">-Force</span><span class="sxs-lookup"><span data-stu-id="defef-118">-Force</span></span>
<span data-ttu-id="defef-119">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="defef-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="defef-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="defef-120">-GalleryName</span></span>
<span data-ttu-id="defef-121">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="defef-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="defef-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="defef-122">-InputObject</span></span>
<span data-ttu-id="defef-123">Объект определения изображения коллекции PS</span><span class="sxs-lookup"><span data-stu-id="defef-123">The PS Gallery Image Definition Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage
Parameter Sets: ObjectParameter
Aliases: GalleryImageDefinition

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="defef-124">-Name</span><span class="sxs-lookup"><span data-stu-id="defef-124">-Name</span></span>
<span data-ttu-id="defef-125">Имя определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="defef-125">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="defef-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="defef-126">-ResourceGroupName</span></span>
<span data-ttu-id="defef-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="defef-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="defef-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="defef-128">-ResourceId</span></span>
<span data-ttu-id="defef-129">ИД ресурса для определения изображения коллекции</span><span class="sxs-lookup"><span data-stu-id="defef-129">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="defef-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="defef-130">-Confirm</span></span>
<span data-ttu-id="defef-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="defef-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="defef-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="defef-132">-WhatIf</span></span>
<span data-ttu-id="defef-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="defef-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="defef-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="defef-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="defef-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="defef-135">CommonParameters</span></span>
<span data-ttu-id="defef-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="defef-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="defef-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="defef-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="defef-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="defef-138">INPUTS</span></span>

### <span data-ttu-id="defef-139">System.String</span><span class="sxs-lookup"><span data-stu-id="defef-139">System.String</span></span>

### <span data-ttu-id="defef-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="defef-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="defef-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="defef-141">OUTPUTS</span></span>

### <span data-ttu-id="defef-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="defef-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="defef-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="defef-143">NOTES</span></span>

## <span data-ttu-id="defef-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="defef-144">RELATED LINKS</span></span>
