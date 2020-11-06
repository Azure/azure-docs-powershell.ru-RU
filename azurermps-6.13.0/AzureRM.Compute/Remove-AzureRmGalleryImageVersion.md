---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmGalleryImageVersion.md
ms.openlocfilehash: c2a65eeb742d4182dfad0cd32be1d78951977096
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561023"
---
# <span data-ttu-id="5ab01-101">Remove-AzureRmGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="5ab01-101">Remove-AzureRmGalleryImageVersion</span></span>

## <span data-ttu-id="5ab01-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5ab01-102">SYNOPSIS</span></span>
<span data-ttu-id="5ab01-103">Удалить версию картинки из коллекции.</span><span class="sxs-lookup"><span data-stu-id="5ab01-103">Delete a gallery image version.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ab01-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5ab01-104">SYNTAX</span></span>

### <span data-ttu-id="5ab01-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5ab01-105">DefaultParameter (Default)</span></span>
```
Remove-AzureRmGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ab01-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="5ab01-106">ResourceIdParameter</span></span>
```
Remove-AzureRmGalleryImageVersion [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ab01-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="5ab01-107">ObjectParameter</span></span>
```
Remove-AzureRmGalleryImageVersion [-Force] [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ab01-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ab01-108">DESCRIPTION</span></span>
<span data-ttu-id="5ab01-109">Удалить версию картинки из коллекции.</span><span class="sxs-lookup"><span data-stu-id="5ab01-109">Delete a gallery image version.</span></span>

## <span data-ttu-id="5ab01-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5ab01-110">EXAMPLES</span></span>

### <span data-ttu-id="5ab01-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5ab01-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -ImageDefinitionName $image -GalleryImageVersionName $version
```

<span data-ttu-id="5ab01-112">Удаление указанной версии изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="5ab01-112">Delete the given gallery image version.</span></span>

## <span data-ttu-id="5ab01-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5ab01-113">PARAMETERS</span></span>

### <span data-ttu-id="5ab01-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ab01-114">-AsJob</span></span>
<span data-ttu-id="5ab01-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5ab01-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5ab01-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ab01-116">-DefaultProfile</span></span>
<span data-ttu-id="5ab01-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5ab01-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ab01-118">-Force</span><span class="sxs-lookup"><span data-stu-id="5ab01-118">-Force</span></span>
<span data-ttu-id="5ab01-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="5ab01-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5ab01-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="5ab01-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="5ab01-121">Имя определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="5ab01-121">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="5ab01-122">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="5ab01-122">-GalleryName</span></span>
<span data-ttu-id="5ab01-123">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="5ab01-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="5ab01-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ab01-124">-InputObject</span></span>
<span data-ttu-id="5ab01-125">Объект версии изображения в коллекции PS</span><span class="sxs-lookup"><span data-stu-id="5ab01-125">The PS Gallery Image Version Object</span></span>

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

### <span data-ttu-id="5ab01-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5ab01-126">-Name</span></span>
<span data-ttu-id="5ab01-127">Имя версии изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="5ab01-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="5ab01-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ab01-128">-ResourceGroupName</span></span>
<span data-ttu-id="5ab01-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5ab01-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="5ab01-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ab01-130">-ResourceId</span></span>
<span data-ttu-id="5ab01-131">Идентификатор ресурса для версии изображения коллекции</span><span class="sxs-lookup"><span data-stu-id="5ab01-131">The resource ID for gallery image version</span></span>

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

### <span data-ttu-id="5ab01-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ab01-132">-Confirm</span></span>
<span data-ttu-id="5ab01-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5ab01-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ab01-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ab01-134">-WhatIf</span></span>
<span data-ttu-id="5ab01-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5ab01-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ab01-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5ab01-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ab01-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ab01-137">CommonParameters</span></span>
<span data-ttu-id="5ab01-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5ab01-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ab01-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ab01-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ab01-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5ab01-140">INPUTS</span></span>

### <span data-ttu-id="5ab01-141">System. String</span><span class="sxs-lookup"><span data-stu-id="5ab01-141">System.String</span></span>

### <span data-ttu-id="5ab01-142">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="5ab01-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="5ab01-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ab01-143">OUTPUTS</span></span>

### <span data-ttu-id="5ab01-144">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="5ab01-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="5ab01-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="5ab01-145">NOTES</span></span>

## <span data-ttu-id="5ab01-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ab01-146">RELATED LINKS</span></span>
