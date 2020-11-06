---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
ms.openlocfilehash: 4115cabbeeb2a7c458ce52e80eb251cb972491f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559163"
---
# <span data-ttu-id="34640-101">Remove-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="34640-101">Remove-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="34640-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="34640-102">SYNOPSIS</span></span>
<span data-ttu-id="34640-103">Удаляет диск с данными из объекта Image.</span><span class="sxs-lookup"><span data-stu-id="34640-103">Removes a data disk from an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34640-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="34640-104">SYNTAX</span></span>

```
Remove-AzureRmImageDataDisk [-Image] <Image> [-Lun] <Int32> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34640-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34640-105">DESCRIPTION</span></span>
<span data-ttu-id="34640-106">Командлет **Remove-AzureRmImageDataDisk** удаляет диск с данными из объекта Image.</span><span class="sxs-lookup"><span data-stu-id="34640-106">The **Remove-AzureRmImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="34640-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="34640-107">EXAMPLES</span></span>

### <span data-ttu-id="34640-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="34640-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="34640-109">Эта команда удаляет диск данных логического устройства с номером 1 из существующего образа "image01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="34640-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="34640-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="34640-110">PARAMETERS</span></span>

### <span data-ttu-id="34640-111">-Image</span><span class="sxs-lookup"><span data-stu-id="34640-111">-Image</span></span>
<span data-ttu-id="34640-112">Указывает локальный объект изображения.</span><span class="sxs-lookup"><span data-stu-id="34640-112">Specifies a local image object.</span></span>

```yaml
Type: Image
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34640-113">-LUN</span><span class="sxs-lookup"><span data-stu-id="34640-113">-Lun</span></span>
<span data-ttu-id="34640-114">Задает логический номер устройства (LUN).</span><span class="sxs-lookup"><span data-stu-id="34640-114">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34640-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34640-115">-Confirm</span></span>
<span data-ttu-id="34640-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="34640-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34640-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34640-117">-WhatIf</span></span>
<span data-ttu-id="34640-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="34640-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="34640-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="34640-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34640-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34640-120">CommonParameters</span></span>
<span data-ttu-id="34640-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="34640-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34640-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34640-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34640-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="34640-123">INPUTS</span></span>

### <span data-ttu-id="34640-124">Microsoft. Azure. Management. COMPUTE. Models.</span><span class="sxs-lookup"><span data-stu-id="34640-124">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="34640-125">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="34640-125">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="34640-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="34640-126">OUTPUTS</span></span>

### <span data-ttu-id="34640-127">Microsoft. Azure. Management. COMPUTE. Models.</span><span class="sxs-lookup"><span data-stu-id="34640-127">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="34640-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="34640-128">NOTES</span></span>

## <span data-ttu-id="34640-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34640-129">RELATED LINKS</span></span>

