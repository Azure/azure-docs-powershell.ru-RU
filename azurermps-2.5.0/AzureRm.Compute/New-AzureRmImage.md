---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermimage
schema: 2.0.0
ms.openlocfilehash: 0a03126be62c528d0879eaff093d6a3969802ce5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913489"
---
# <span data-ttu-id="d80c2-101">New-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="d80c2-101">New-AzureRmImage</span></span>

## <span data-ttu-id="d80c2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d80c2-102">SYNOPSIS</span></span>
<span data-ttu-id="d80c2-103">Создание изображения.</span><span class="sxs-lookup"><span data-stu-id="d80c2-103">Creates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d80c2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d80c2-104">SYNTAX</span></span>

```
New-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d80c2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d80c2-105">DESCRIPTION</span></span>
<span data-ttu-id="d80c2-106">Командлет **New-AzureRmImage** создает изображение.</span><span class="sxs-lookup"><span data-stu-id="d80c2-106">The **New-AzureRmImage** cmdlet creates an image.</span></span>

## <span data-ttu-id="d80c2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d80c2-107">EXAMPLES</span></span>

### <span data-ttu-id="d80c2-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d80c2-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzureRmImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzureRmImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzureRmImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="d80c2-109">В первой команде создается объект Image, который затем сохраняется в переменной $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="d80c2-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="d80c2-110">Следующие три команды назначают пути к диску операционной системы и двум дискам данных в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2 переменные.</span><span class="sxs-lookup"><span data-stu-id="d80c2-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="d80c2-111">Этот подход предназначен для чтения следующих команд.</span><span class="sxs-lookup"><span data-stu-id="d80c2-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="d80c2-112">Следующие три команды добавляют диск операционной системы и два диска данных в образ, хранящийся в $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="d80c2-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="d80c2-113">Универсальный код ресурса (URI) каждого диска хранится в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="d80c2-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="d80c2-114">Последняя команда создает изображение с именем "ImageName01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="d80c2-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="d80c2-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d80c2-115">PARAMETERS</span></span>

### <span data-ttu-id="d80c2-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d80c2-116">-AsJob</span></span>
<span data-ttu-id="d80c2-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d80c2-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d80c2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d80c2-118">-DefaultProfile</span></span>
<span data-ttu-id="d80c2-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d80c2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d80c2-120">-Image</span><span class="sxs-lookup"><span data-stu-id="d80c2-120">-Image</span></span>
<span data-ttu-id="d80c2-121">Указывает локальный объект изображения.</span><span class="sxs-lookup"><span data-stu-id="d80c2-121">Specifies a local image object.</span></span>

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

### <span data-ttu-id="d80c2-122">-ImageName</span><span class="sxs-lookup"><span data-stu-id="d80c2-122">-ImageName</span></span>
<span data-ttu-id="d80c2-123">Указывает имя изображения.</span><span class="sxs-lookup"><span data-stu-id="d80c2-123">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="d80c2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d80c2-124">-ResourceGroupName</span></span>
<span data-ttu-id="d80c2-125">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d80c2-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d80c2-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d80c2-126">-Confirm</span></span>
<span data-ttu-id="d80c2-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d80c2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d80c2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d80c2-128">-WhatIf</span></span>
<span data-ttu-id="d80c2-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d80c2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d80c2-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d80c2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d80c2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d80c2-131">CommonParameters</span></span>
<span data-ttu-id="d80c2-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d80c2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d80c2-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d80c2-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d80c2-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d80c2-134">INPUTS</span></span>

### <span data-ttu-id="d80c2-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d80c2-135">System.String</span></span>
<span data-ttu-id="d80c2-136">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="d80c2-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="d80c2-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d80c2-137">OUTPUTS</span></span>

### <span data-ttu-id="d80c2-138">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="d80c2-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="d80c2-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="d80c2-139">System.Object</span></span>

## <span data-ttu-id="d80c2-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="d80c2-140">NOTES</span></span>

## <span data-ttu-id="d80c2-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d80c2-141">RELATED LINKS</span></span>

