---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImage.md
ms.openlocfilehash: 054462398a0f7b3e8710928000f9c10fb42f04db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732546"
---
# <span data-ttu-id="bc746-101">Remove-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="bc746-101">Remove-AzureRmImage</span></span>

## <span data-ttu-id="bc746-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bc746-102">SYNOPSIS</span></span>
<span data-ttu-id="bc746-103">Удаление изображения.</span><span class="sxs-lookup"><span data-stu-id="bc746-103">Removes an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc746-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bc746-104">SYNTAX</span></span>

```
Remove-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bc746-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc746-105">DESCRIPTION</span></span>
<span data-ttu-id="bc746-106">Командлет **Remove-AzureRmImage** удаляет изображение..</span><span class="sxs-lookup"><span data-stu-id="bc746-106">The **Remove-AzureRmImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="bc746-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bc746-107">EXAMPLES</span></span>

### <span data-ttu-id="bc746-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bc746-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="bc746-109">Эта команда удаляет изображение с именем "image01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="bc746-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="bc746-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bc746-110">PARAMETERS</span></span>

### <span data-ttu-id="bc746-111">-Force</span><span class="sxs-lookup"><span data-stu-id="bc746-111">-Force</span></span>
<span data-ttu-id="bc746-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="bc746-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc746-113">-ImageName</span><span class="sxs-lookup"><span data-stu-id="bc746-113">-ImageName</span></span>
<span data-ttu-id="bc746-114">Указывает имя изображения.</span><span class="sxs-lookup"><span data-stu-id="bc746-114">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="bc746-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc746-115">-ResourceGroupName</span></span>
<span data-ttu-id="bc746-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bc746-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="bc746-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc746-117">-Confirm</span></span>
<span data-ttu-id="bc746-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bc746-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc746-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc746-119">-WhatIf</span></span>
<span data-ttu-id="bc746-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bc746-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc746-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bc746-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc746-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc746-122">CommonParameters</span></span>
<span data-ttu-id="bc746-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bc746-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc746-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc746-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc746-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bc746-125">INPUTS</span></span>

### <span data-ttu-id="bc746-126">System. String</span><span class="sxs-lookup"><span data-stu-id="bc746-126">System.String</span></span>

## <span data-ttu-id="bc746-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc746-127">OUTPUTS</span></span>

### <span data-ttu-id="bc746-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="bc746-128">System.Object</span></span>

## <span data-ttu-id="bc746-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="bc746-129">NOTES</span></span>

## <span data-ttu-id="bc746-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc746-130">RELATED LINKS</span></span>

