---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmImage.md
ms.openlocfilehash: 3976418d89076b290500343775ca42e2fb975659
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565570"
---
# <span data-ttu-id="52d61-101">Get-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="52d61-101">Get-AzureRmImage</span></span>

## <span data-ttu-id="52d61-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="52d61-102">SYNOPSIS</span></span>
<span data-ttu-id="52d61-103">Получает свойства изображения.</span><span class="sxs-lookup"><span data-stu-id="52d61-103">Gets the properties of an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52d61-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="52d61-104">SYNTAX</span></span>

```
Get-AzureRmImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="52d61-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="52d61-105">DESCRIPTION</span></span>
<span data-ttu-id="52d61-106">Командлет **Get-AzureRmImage** получает свойства изображения.</span><span class="sxs-lookup"><span data-stu-id="52d61-106">The **Get-AzureRmImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="52d61-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="52d61-107">EXAMPLES</span></span>

### <span data-ttu-id="52d61-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="52d61-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'
```

<span data-ttu-id="52d61-109">Эта команда получает свойства изображения с именем "image01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="52d61-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="52d61-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="52d61-110">Example 2</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="52d61-111">Эта команда получает свойства всех изображений в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="52d61-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="52d61-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="52d61-112">Example 3</span></span>
```
PS C:\> Get-AzureRmImage
```

<span data-ttu-id="52d61-113">Эта команда получает свойства всех изображений в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="52d61-113">This command gets the properties of all images under the subscription.</span></span>

## <span data-ttu-id="52d61-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="52d61-114">PARAMETERS</span></span>

### <span data-ttu-id="52d61-115">-Expand</span><span class="sxs-lookup"><span data-stu-id="52d61-115">-Expand</span></span>
<span data-ttu-id="52d61-116">Указывает запрос на расширение выражения.</span><span class="sxs-lookup"><span data-stu-id="52d61-116">Specifies the expand expression query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52d61-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="52d61-117">-ImageName</span></span>
<span data-ttu-id="52d61-118">Указывает имя изображения.</span><span class="sxs-lookup"><span data-stu-id="52d61-118">Specifies the name of an image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52d61-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52d61-119">-ResourceGroupName</span></span>
<span data-ttu-id="52d61-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="52d61-120">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52d61-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52d61-121">CommonParameters</span></span>
<span data-ttu-id="52d61-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="52d61-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52d61-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52d61-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52d61-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="52d61-124">INPUTS</span></span>

### <span data-ttu-id="52d61-125">System. String</span><span class="sxs-lookup"><span data-stu-id="52d61-125">System.String</span></span>

## <span data-ttu-id="52d61-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="52d61-126">OUTPUTS</span></span>

### <span data-ttu-id="52d61-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="52d61-127">System.Object</span></span>

## <span data-ttu-id="52d61-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="52d61-128">NOTES</span></span>

## <span data-ttu-id="52d61-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="52d61-129">RELATED LINKS</span></span>

