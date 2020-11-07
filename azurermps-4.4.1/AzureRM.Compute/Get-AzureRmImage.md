---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmImage.md
ms.openlocfilehash: c1d7a7128c0fd4774c99799695e0d041a08c8053
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734574"
---
# <span data-ttu-id="6148a-101">Get-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="6148a-101">Get-AzureRmImage</span></span>

## <span data-ttu-id="6148a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6148a-102">SYNOPSIS</span></span>
<span data-ttu-id="6148a-103">Получает свойства изображения.</span><span class="sxs-lookup"><span data-stu-id="6148a-103">Gets the properties of an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6148a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6148a-104">SYNTAX</span></span>

```
Get-AzureRmImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6148a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6148a-105">DESCRIPTION</span></span>
<span data-ttu-id="6148a-106">Командлет **Get-AzureRmImage** получает свойства изображения.</span><span class="sxs-lookup"><span data-stu-id="6148a-106">The **Get-AzureRmImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="6148a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6148a-107">EXAMPLES</span></span>

### <span data-ttu-id="6148a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6148a-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'
```

<span data-ttu-id="6148a-109">Эта команда получает свойства изображения с именем "image01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="6148a-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="6148a-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6148a-110">Example 2</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="6148a-111">Эта команда получает свойства всех изображений в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="6148a-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="6148a-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="6148a-112">Example 3</span></span>
```
PS C:\> Get-AzureRmImage
```

<span data-ttu-id="6148a-113">Эта команда получает свойства всех изображений в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="6148a-113">This command gets the properties of all images under the subscription.</span></span>

## <span data-ttu-id="6148a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6148a-114">PARAMETERS</span></span>

### <span data-ttu-id="6148a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6148a-115">-DefaultProfile</span></span>
<span data-ttu-id="6148a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6148a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6148a-117">-Expand</span><span class="sxs-lookup"><span data-stu-id="6148a-117">-Expand</span></span>
<span data-ttu-id="6148a-118">Указывает запрос на расширение выражения.</span><span class="sxs-lookup"><span data-stu-id="6148a-118">Specifies the expand expression query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6148a-119">-ImageName</span><span class="sxs-lookup"><span data-stu-id="6148a-119">-ImageName</span></span>
<span data-ttu-id="6148a-120">Указывает имя изображения.</span><span class="sxs-lookup"><span data-stu-id="6148a-120">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6148a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6148a-121">-ResourceGroupName</span></span>
<span data-ttu-id="6148a-122">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6148a-122">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6148a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6148a-123">CommonParameters</span></span>
<span data-ttu-id="6148a-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6148a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6148a-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6148a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6148a-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6148a-126">INPUTS</span></span>

### <span data-ttu-id="6148a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="6148a-127">System.String</span></span>

## <span data-ttu-id="6148a-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6148a-128">OUTPUTS</span></span>

### <span data-ttu-id="6148a-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="6148a-129">System.Object</span></span>

## <span data-ttu-id="6148a-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="6148a-130">NOTES</span></span>

## <span data-ttu-id="6148a-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6148a-131">RELATED LINKS</span></span>

