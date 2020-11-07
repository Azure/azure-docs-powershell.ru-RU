---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermimage
schema: 2.0.0
ms.openlocfilehash: f1309453384f028c51bea20703d6ec75cc8a3a36
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915329"
---
# <span data-ttu-id="1af6b-101">Update-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="1af6b-101">Update-AzureRmImage</span></span>

## <span data-ttu-id="1af6b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1af6b-102">SYNOPSIS</span></span>
<span data-ttu-id="1af6b-103">Обновляет изображение.</span><span class="sxs-lookup"><span data-stu-id="1af6b-103">Updates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1af6b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1af6b-104">SYNTAX</span></span>

```
Update-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1af6b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1af6b-105">DESCRIPTION</span></span>
<span data-ttu-id="1af6b-106">Командлет **Update-AzureRmImage** обновляет изображение.</span><span class="sxs-lookup"><span data-stu-id="1af6b-106">The **Update-AzureRmImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="1af6b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1af6b-107">EXAMPLES</span></span>

### <span data-ttu-id="1af6b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1af6b-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="1af6b-109">Эта команда удаляет диск данных логического устройства с номером 1 из существующего образа "image01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="1af6b-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="1af6b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1af6b-110">PARAMETERS</span></span>

### <span data-ttu-id="1af6b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1af6b-111">-AsJob</span></span>
<span data-ttu-id="1af6b-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1af6b-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1af6b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1af6b-113">-DefaultProfile</span></span>
<span data-ttu-id="1af6b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1af6b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1af6b-115">-Image</span><span class="sxs-lookup"><span data-stu-id="1af6b-115">-Image</span></span>
<span data-ttu-id="1af6b-116">Указывает локальный объект изображения.</span><span class="sxs-lookup"><span data-stu-id="1af6b-116">Specifies a local image object.</span></span>

```yaml
Type: PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1af6b-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="1af6b-117">-ImageName</span></span>
<span data-ttu-id="1af6b-118">Указывает имя изображения.</span><span class="sxs-lookup"><span data-stu-id="1af6b-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="1af6b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1af6b-119">-ResourceGroupName</span></span>
<span data-ttu-id="1af6b-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1af6b-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1af6b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1af6b-121">-Confirm</span></span>
<span data-ttu-id="1af6b-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1af6b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1af6b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1af6b-123">-WhatIf</span></span>
<span data-ttu-id="1af6b-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1af6b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1af6b-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1af6b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1af6b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1af6b-126">CommonParameters</span></span>
<span data-ttu-id="1af6b-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1af6b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1af6b-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1af6b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1af6b-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1af6b-129">INPUTS</span></span>

### <span data-ttu-id="1af6b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1af6b-130">System.String</span></span>
<span data-ttu-id="1af6b-131">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="1af6b-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="1af6b-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1af6b-132">OUTPUTS</span></span>

### <span data-ttu-id="1af6b-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="1af6b-133">System.Object</span></span>

## <span data-ttu-id="1af6b-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="1af6b-134">NOTES</span></span>

## <span data-ttu-id="1af6b-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1af6b-135">RELATED LINKS</span></span>

