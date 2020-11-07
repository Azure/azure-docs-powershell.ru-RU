---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmImage.md
ms.openlocfilehash: ccca83cdbebcf73df9059807dc5b030e4ab21736
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733124"
---
# <span data-ttu-id="dbad5-101">Update-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="dbad5-101">Update-AzureRmImage</span></span>

## <span data-ttu-id="dbad5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dbad5-102">SYNOPSIS</span></span>
<span data-ttu-id="dbad5-103">Обновляет изображение.</span><span class="sxs-lookup"><span data-stu-id="dbad5-103">Updates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbad5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dbad5-104">SYNTAX</span></span>

```
Update-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbad5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dbad5-105">DESCRIPTION</span></span>
<span data-ttu-id="dbad5-106">Командлет **Update-AzureRmImage** обновляет изображение.</span><span class="sxs-lookup"><span data-stu-id="dbad5-106">The **Update-AzureRmImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="dbad5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dbad5-107">EXAMPLES</span></span>

### <span data-ttu-id="dbad5-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dbad5-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="dbad5-109">Эта команда удаляет диск данных логического устройства с номером 1 из существующего образа "image01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="dbad5-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="dbad5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dbad5-110">PARAMETERS</span></span>

### <span data-ttu-id="dbad5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbad5-111">-DefaultProfile</span></span>
<span data-ttu-id="dbad5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dbad5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbad5-113">-Image</span><span class="sxs-lookup"><span data-stu-id="dbad5-113">-Image</span></span>
<span data-ttu-id="dbad5-114">Указывает локальный объект изображения.</span><span class="sxs-lookup"><span data-stu-id="dbad5-114">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbad5-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="dbad5-115">-ImageName</span></span>
<span data-ttu-id="dbad5-116">Указывает имя изображения.</span><span class="sxs-lookup"><span data-stu-id="dbad5-116">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbad5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbad5-117">-ResourceGroupName</span></span>
<span data-ttu-id="dbad5-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dbad5-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbad5-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dbad5-119">-Confirm</span></span>
<span data-ttu-id="dbad5-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dbad5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbad5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbad5-121">-WhatIf</span></span>
<span data-ttu-id="dbad5-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dbad5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbad5-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dbad5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbad5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbad5-124">CommonParameters</span></span>
<span data-ttu-id="dbad5-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dbad5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbad5-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbad5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbad5-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dbad5-127">INPUTS</span></span>

### <span data-ttu-id="dbad5-128">System. String</span><span class="sxs-lookup"><span data-stu-id="dbad5-128">System.String</span></span>
<span data-ttu-id="dbad5-129">Microsoft. Azure. Management. COMPUTE. Models.</span><span class="sxs-lookup"><span data-stu-id="dbad5-129">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="dbad5-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dbad5-130">OUTPUTS</span></span>

### <span data-ttu-id="dbad5-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="dbad5-131">System.Object</span></span>

## <span data-ttu-id="dbad5-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="dbad5-132">NOTES</span></span>

## <span data-ttu-id="dbad5-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dbad5-133">RELATED LINKS</span></span>

