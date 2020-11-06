---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmImage.md
ms.openlocfilehash: b7c5155706b968973bef6a5cf1ce2285caee819d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557479"
---
# <span data-ttu-id="48f7b-101">Update-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="48f7b-101">Update-AzureRmImage</span></span>

## <span data-ttu-id="48f7b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="48f7b-102">SYNOPSIS</span></span>
<span data-ttu-id="48f7b-103">Обновляет изображение.</span><span class="sxs-lookup"><span data-stu-id="48f7b-103">Updates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48f7b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="48f7b-104">SYNTAX</span></span>

```
Update-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <Image> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="48f7b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="48f7b-105">DESCRIPTION</span></span>
<span data-ttu-id="48f7b-106">Командлет **Update-AzureRmImage** обновляет изображение.</span><span class="sxs-lookup"><span data-stu-id="48f7b-106">The **Update-AzureRmImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="48f7b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="48f7b-107">EXAMPLES</span></span>

### <span data-ttu-id="48f7b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="48f7b-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="48f7b-109">Эта команда удаляет диск данных логического устройства с номером 1 из существующего образа "image01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="48f7b-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="48f7b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="48f7b-110">PARAMETERS</span></span>

### <span data-ttu-id="48f7b-111">-Image</span><span class="sxs-lookup"><span data-stu-id="48f7b-111">-Image</span></span>
<span data-ttu-id="48f7b-112">Указывает локальный объект изображения.</span><span class="sxs-lookup"><span data-stu-id="48f7b-112">Specifies a local image object.</span></span>

```yaml
Type: Image
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48f7b-113">-ImageName</span><span class="sxs-lookup"><span data-stu-id="48f7b-113">-ImageName</span></span>
<span data-ttu-id="48f7b-114">Указывает имя изображения.</span><span class="sxs-lookup"><span data-stu-id="48f7b-114">Specifies the name of an image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48f7b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48f7b-115">-ResourceGroupName</span></span>
<span data-ttu-id="48f7b-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="48f7b-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48f7b-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48f7b-117">-Confirm</span></span>
<span data-ttu-id="48f7b-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="48f7b-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48f7b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48f7b-119">-WhatIf</span></span>
<span data-ttu-id="48f7b-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="48f7b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48f7b-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="48f7b-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48f7b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48f7b-122">CommonParameters</span></span>
<span data-ttu-id="48f7b-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="48f7b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48f7b-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48f7b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48f7b-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="48f7b-125">INPUTS</span></span>

### <span data-ttu-id="48f7b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="48f7b-126">System.String</span></span>
<span data-ttu-id="48f7b-127">Microsoft. Azure. Management. COMPUTE. Models.</span><span class="sxs-lookup"><span data-stu-id="48f7b-127">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="48f7b-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="48f7b-128">OUTPUTS</span></span>

### <span data-ttu-id="48f7b-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="48f7b-129">System.Object</span></span>

## <span data-ttu-id="48f7b-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="48f7b-130">NOTES</span></span>

## <span data-ttu-id="48f7b-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="48f7b-131">RELATED LINKS</span></span>

