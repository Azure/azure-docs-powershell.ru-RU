---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmImage.md
ms.openlocfilehash: 34c4eefe2792de239b2f3ae2a9348704497a4bd5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732987"
---
# <span data-ttu-id="b9e5e-101">Update-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="b9e5e-101">Update-AzureRmImage</span></span>

## <span data-ttu-id="b9e5e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b9e5e-102">SYNOPSIS</span></span>
<span data-ttu-id="b9e5e-103">Обновляет изображение.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-103">Updates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9e5e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b9e5e-104">SYNTAX</span></span>

```
Update-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9e5e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9e5e-105">DESCRIPTION</span></span>
<span data-ttu-id="b9e5e-106">Командлет **Update-AzureRmImage** обновляет изображение.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-106">The **Update-AzureRmImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="b9e5e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b9e5e-107">EXAMPLES</span></span>

### <span data-ttu-id="b9e5e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b9e5e-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="b9e5e-109">Эта команда удаляет диск данных логического устройства с номером 1 из существующего образа "image01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="b9e5e-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="b9e5e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b9e5e-110">PARAMETERS</span></span>

### <span data-ttu-id="b9e5e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9e5e-111">-AsJob</span></span>
<span data-ttu-id="b9e5e-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b9e5e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b9e5e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9e5e-113">-DefaultProfile</span></span>
<span data-ttu-id="b9e5e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9e5e-115">-Image</span><span class="sxs-lookup"><span data-stu-id="b9e5e-115">-Image</span></span>
<span data-ttu-id="b9e5e-116">Указывает локальный объект изображения.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-116">Specifies a local image object.</span></span>

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

### <span data-ttu-id="b9e5e-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="b9e5e-117">-ImageName</span></span>
<span data-ttu-id="b9e5e-118">Указывает имя изображения.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="b9e5e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9e5e-119">-ResourceGroupName</span></span>
<span data-ttu-id="b9e5e-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b9e5e-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9e5e-121">-Confirm</span></span>
<span data-ttu-id="b9e5e-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9e5e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9e5e-123">-WhatIf</span></span>
<span data-ttu-id="b9e5e-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9e5e-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9e5e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9e5e-126">CommonParameters</span></span>
<span data-ttu-id="b9e5e-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9e5e-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9e5e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9e5e-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b9e5e-129">INPUTS</span></span>

### <span data-ttu-id="b9e5e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b9e5e-130">System.String</span></span>

### <span data-ttu-id="b9e5e-131">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="b9e5e-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>
<span data-ttu-id="b9e5e-132">Параметры: Image (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b9e5e-132">Parameters: Image (ByValue)</span></span>

## <span data-ttu-id="b9e5e-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9e5e-133">OUTPUTS</span></span>

### <span data-ttu-id="b9e5e-134">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="b9e5e-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="b9e5e-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="b9e5e-135">NOTES</span></span>

## <span data-ttu-id="b9e5e-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9e5e-136">RELATED LINKS</span></span>
