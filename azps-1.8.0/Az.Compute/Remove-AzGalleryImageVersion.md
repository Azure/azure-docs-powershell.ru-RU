---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
ms.openlocfilehash: adbfd3515763427118fb7876fadd247d4240fd97
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901214"
---
# <span data-ttu-id="32b93-101">Remove-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="32b93-101">Remove-AzGalleryImageVersion</span></span>

## <span data-ttu-id="32b93-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="32b93-102">SYNOPSIS</span></span>
<span data-ttu-id="32b93-103">Удалить версию картинки из коллекции.</span><span class="sxs-lookup"><span data-stu-id="32b93-103">Delete a gallery image version.</span></span>

## <span data-ttu-id="32b93-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="32b93-104">SYNTAX</span></span>

### <span data-ttu-id="32b93-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="32b93-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32b93-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="32b93-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32b93-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="32b93-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32b93-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32b93-108">DESCRIPTION</span></span>
<span data-ttu-id="32b93-109">Удалить версию картинки из коллекции.</span><span class="sxs-lookup"><span data-stu-id="32b93-109">Delete a gallery image version.</span></span>

## <span data-ttu-id="32b93-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="32b93-110">EXAMPLES</span></span>

### <span data-ttu-id="32b93-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="32b93-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -ImageDefinitionName $image -GalleryImageVersionName $version
```

<span data-ttu-id="32b93-112">Удаление указанной версии изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="32b93-112">Delete the given gallery image version.</span></span>

## <span data-ttu-id="32b93-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="32b93-113">PARAMETERS</span></span>

### <span data-ttu-id="32b93-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32b93-114">-AsJob</span></span>
<span data-ttu-id="32b93-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="32b93-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="32b93-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32b93-116">-DefaultProfile</span></span>
<span data-ttu-id="32b93-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32b93-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32b93-118">-Force</span><span class="sxs-lookup"><span data-stu-id="32b93-118">-Force</span></span>
<span data-ttu-id="32b93-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="32b93-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="32b93-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="32b93-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="32b93-121">Имя определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="32b93-121">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="32b93-122">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="32b93-122">-GalleryName</span></span>
<span data-ttu-id="32b93-123">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="32b93-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="32b93-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32b93-124">-InputObject</span></span>
<span data-ttu-id="32b93-125">Объект версии изображения в коллекции PS</span><span class="sxs-lookup"><span data-stu-id="32b93-125">The PS Gallery Image Version Object</span></span>

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

### <span data-ttu-id="32b93-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="32b93-126">-Name</span></span>
<span data-ttu-id="32b93-127">Имя версии изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="32b93-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="32b93-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32b93-128">-ResourceGroupName</span></span>
<span data-ttu-id="32b93-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="32b93-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="32b93-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32b93-130">-ResourceId</span></span>
<span data-ttu-id="32b93-131">Идентификатор ресурса для версии изображения коллекции</span><span class="sxs-lookup"><span data-stu-id="32b93-131">The resource ID for gallery image version</span></span>

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

### <span data-ttu-id="32b93-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32b93-132">-Confirm</span></span>
<span data-ttu-id="32b93-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="32b93-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32b93-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32b93-134">-WhatIf</span></span>
<span data-ttu-id="32b93-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="32b93-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32b93-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="32b93-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32b93-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32b93-137">CommonParameters</span></span>
<span data-ttu-id="32b93-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="32b93-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32b93-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32b93-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32b93-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="32b93-140">INPUTS</span></span>

### <span data-ttu-id="32b93-141">System. String</span><span class="sxs-lookup"><span data-stu-id="32b93-141">System.String</span></span>

### <span data-ttu-id="32b93-142">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="32b93-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="32b93-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="32b93-143">OUTPUTS</span></span>

### <span data-ttu-id="32b93-144">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="32b93-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="32b93-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="32b93-145">NOTES</span></span>

## <span data-ttu-id="32b93-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32b93-146">RELATED LINKS</span></span>
