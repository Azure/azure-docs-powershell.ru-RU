---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
ms.openlocfilehash: 3798fccf0d3869d17fd0f79283aac93d0869a0e6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721626"
---
# <span data-ttu-id="3ed7c-101">Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="3ed7c-101">Update-AzImage</span></span>

## <span data-ttu-id="3ed7c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3ed7c-102">SYNOPSIS</span></span>
<span data-ttu-id="3ed7c-103">Обновляет изображение.</span><span class="sxs-lookup"><span data-stu-id="3ed7c-103">Updates an image.</span></span>

## <span data-ttu-id="3ed7c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3ed7c-104">SYNTAX</span></span>

### <span data-ttu-id="3ed7c-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3ed7c-105">DefaultParameter (Default)</span></span>
```
Update-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ed7c-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="3ed7c-106">ResourceIdParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ed7c-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="3ed7c-107">ObjectParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-Image] <PSImage> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ed7c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ed7c-108">DESCRIPTION</span></span>
<span data-ttu-id="3ed7c-109">Командлет **Update-AzImage** обновляет изображение.</span><span class="sxs-lookup"><span data-stu-id="3ed7c-109">The **Update-AzImage** cmdlet updates an image.</span></span>
<span data-ttu-id="3ed7c-110">В настоящее время можно обновлять только теги.</span><span class="sxs-lookup"><span data-stu-id="3ed7c-110">Currently, only the Tags can be updated.</span></span>

## <span data-ttu-id="3ed7c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3ed7c-111">EXAMPLES</span></span>

### <span data-ttu-id="3ed7c-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3ed7c-112">Example 1</span></span>
```
PS C:\> $image = Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' 
PS C:\> $image.Tags = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\> $image.Tags.Add("key1", "val1")
PS C:\> Update-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Image $image
```

<span data-ttu-id="3ed7c-113">Эта команда обновляет значение Tag существующего изображения "image01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="3ed7c-113">This command updates the Tag value of the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="3ed7c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3ed7c-114">PARAMETERS</span></span>

### <span data-ttu-id="3ed7c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ed7c-115">-AsJob</span></span>
<span data-ttu-id="3ed7c-116">Запустите командлет в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="3ed7c-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="3ed7c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ed7c-117">-DefaultProfile</span></span>
<span data-ttu-id="3ed7c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3ed7c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ed7c-119">-Image</span><span class="sxs-lookup"><span data-stu-id="3ed7c-119">-Image</span></span>
<span data-ttu-id="3ed7c-120">Указывает локальный объект изображения.</span><span class="sxs-lookup"><span data-stu-id="3ed7c-120">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ed7c-121">-ImageName</span><span class="sxs-lookup"><span data-stu-id="3ed7c-121">-ImageName</span></span>
<span data-ttu-id="3ed7c-122">Указывает имя изображения.</span><span class="sxs-lookup"><span data-stu-id="3ed7c-122">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ed7c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ed7c-123">-ResourceGroupName</span></span>
<span data-ttu-id="3ed7c-124">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3ed7c-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3ed7c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ed7c-125">-ResourceId</span></span>
<span data-ttu-id="3ed7c-126">Идентификатор ресурса для изображения</span><span class="sxs-lookup"><span data-stu-id="3ed7c-126">The resource Id for the image</span></span>

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

### <span data-ttu-id="3ed7c-127">-Тег</span><span class="sxs-lookup"><span data-stu-id="3ed7c-127">-Tag</span></span>
<span data-ttu-id="3ed7c-128">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="3ed7c-128">Resource tags</span></span>

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

### <span data-ttu-id="3ed7c-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ed7c-129">-Confirm</span></span>
<span data-ttu-id="3ed7c-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3ed7c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ed7c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ed7c-131">-WhatIf</span></span>
<span data-ttu-id="3ed7c-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3ed7c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ed7c-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3ed7c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ed7c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ed7c-134">CommonParameters</span></span>
<span data-ttu-id="3ed7c-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3ed7c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ed7c-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ed7c-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ed7c-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3ed7c-137">INPUTS</span></span>

### <span data-ttu-id="3ed7c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3ed7c-138">System.String</span></span>

### <span data-ttu-id="3ed7c-139">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="3ed7c-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="3ed7c-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ed7c-140">OUTPUTS</span></span>

### <span data-ttu-id="3ed7c-141">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="3ed7c-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="3ed7c-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="3ed7c-142">NOTES</span></span>

## <span data-ttu-id="3ed7c-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ed7c-143">RELATED LINKS</span></span>
