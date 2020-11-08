---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
ms.openlocfilehash: 81323c1a35e36b036e759911bbfec2dde764ac8f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078121"
---
# <span data-ttu-id="27fa5-101">Remove-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="27fa5-101">Remove-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="27fa5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="27fa5-102">SYNOPSIS</span></span>
<span data-ttu-id="27fa5-103">Удаление определения картинки из коллекции.</span><span class="sxs-lookup"><span data-stu-id="27fa5-103">Delete a gallery image definition.</span></span>

## <span data-ttu-id="27fa5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="27fa5-104">SYNTAX</span></span>

### <span data-ttu-id="27fa5-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="27fa5-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27fa5-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="27fa5-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27fa5-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="27fa5-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-InputObject] <PSGalleryImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27fa5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27fa5-108">DESCRIPTION</span></span>
<span data-ttu-id="27fa5-109">Удаление определения картинки из коллекции.</span><span class="sxs-lookup"><span data-stu-id="27fa5-109">Delete a gallery image definition.</span></span>

## <span data-ttu-id="27fa5-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="27fa5-110">EXAMPLES</span></span>

### <span data-ttu-id="27fa5-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="27fa5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $galleryImage
```

<span data-ttu-id="27fa5-112">Удалите определение изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="27fa5-112">Remove the gallery image definition.</span></span>

## <span data-ttu-id="27fa5-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="27fa5-113">PARAMETERS</span></span>

### <span data-ttu-id="27fa5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27fa5-114">-AsJob</span></span>
<span data-ttu-id="27fa5-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="27fa5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="27fa5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27fa5-116">-DefaultProfile</span></span>
<span data-ttu-id="27fa5-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="27fa5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27fa5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="27fa5-118">-Force</span></span>
<span data-ttu-id="27fa5-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="27fa5-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="27fa5-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="27fa5-120">-GalleryName</span></span>
<span data-ttu-id="27fa5-121">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="27fa5-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="27fa5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27fa5-122">-InputObject</span></span>
<span data-ttu-id="27fa5-123">Объект определения изображения в коллекции PS</span><span class="sxs-lookup"><span data-stu-id="27fa5-123">The PS Gallery Image Definition Object</span></span>

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

### <span data-ttu-id="27fa5-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="27fa5-124">-Name</span></span>
<span data-ttu-id="27fa5-125">Имя определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="27fa5-125">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="27fa5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27fa5-126">-ResourceGroupName</span></span>
<span data-ttu-id="27fa5-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="27fa5-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="27fa5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27fa5-128">-ResourceId</span></span>
<span data-ttu-id="27fa5-129">Идентификатор ресурса для определения изображения коллекции</span><span class="sxs-lookup"><span data-stu-id="27fa5-129">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="27fa5-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27fa5-130">-Confirm</span></span>
<span data-ttu-id="27fa5-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="27fa5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27fa5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27fa5-132">-WhatIf</span></span>
<span data-ttu-id="27fa5-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="27fa5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27fa5-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="27fa5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27fa5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27fa5-135">CommonParameters</span></span>
<span data-ttu-id="27fa5-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="27fa5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27fa5-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27fa5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27fa5-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="27fa5-138">INPUTS</span></span>

### <span data-ttu-id="27fa5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="27fa5-139">System.String</span></span>

### <span data-ttu-id="27fa5-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="27fa5-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="27fa5-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="27fa5-141">OUTPUTS</span></span>

### <span data-ttu-id="27fa5-142">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="27fa5-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="27fa5-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="27fa5-143">NOTES</span></span>

## <span data-ttu-id="27fa5-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27fa5-144">RELATED LINKS</span></span>
