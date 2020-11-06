---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImage.md
ms.openlocfilehash: 02255fd8fd4db5747c820755bfd46ee3251aab9e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557907"
---
# <span data-ttu-id="66105-101">New-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="66105-101">New-AzureRmImage</span></span>

## <span data-ttu-id="66105-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="66105-102">SYNOPSIS</span></span>
<span data-ttu-id="66105-103">Создание изображения.</span><span class="sxs-lookup"><span data-stu-id="66105-103">Creates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66105-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="66105-104">SYNTAX</span></span>

```
New-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66105-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="66105-105">DESCRIPTION</span></span>
<span data-ttu-id="66105-106">Командлет **New-AzureRmImage** создает изображение.</span><span class="sxs-lookup"><span data-stu-id="66105-106">The **New-AzureRmImage** cmdlet creates an image.</span></span>

## <span data-ttu-id="66105-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="66105-107">EXAMPLES</span></span>

### <span data-ttu-id="66105-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="66105-108">Example 1</span></span>
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

<span data-ttu-id="66105-109">В первой команде создается объект Image, который затем сохраняется в переменной $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="66105-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="66105-110">Следующие три команды назначают пути к диску операционной системы и двум дискам данных в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2 переменные.</span><span class="sxs-lookup"><span data-stu-id="66105-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="66105-111">Этот подход предназначен для чтения следующих команд.</span><span class="sxs-lookup"><span data-stu-id="66105-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="66105-112">Следующие три команды добавляют диск операционной системы и два диска данных в образ, хранящийся в $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="66105-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="66105-113">Универсальный код ресурса (URI) каждого диска хранится в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="66105-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="66105-114">Последняя команда создает изображение с именем "ImageName01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="66105-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="66105-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="66105-115">PARAMETERS</span></span>

### <span data-ttu-id="66105-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66105-116">-DefaultProfile</span></span>
<span data-ttu-id="66105-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="66105-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66105-118">-Image</span><span class="sxs-lookup"><span data-stu-id="66105-118">-Image</span></span>
<span data-ttu-id="66105-119">Указывает локальный объект изображения.</span><span class="sxs-lookup"><span data-stu-id="66105-119">Specifies a local image object.</span></span>

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

### <span data-ttu-id="66105-120">-ImageName</span><span class="sxs-lookup"><span data-stu-id="66105-120">-ImageName</span></span>
<span data-ttu-id="66105-121">Указывает имя изображения.</span><span class="sxs-lookup"><span data-stu-id="66105-121">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="66105-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66105-122">-ResourceGroupName</span></span>
<span data-ttu-id="66105-123">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="66105-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="66105-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66105-124">-Confirm</span></span>
<span data-ttu-id="66105-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="66105-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66105-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66105-126">-WhatIf</span></span>
<span data-ttu-id="66105-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="66105-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66105-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="66105-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66105-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66105-129">CommonParameters</span></span>
<span data-ttu-id="66105-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="66105-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66105-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66105-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66105-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="66105-132">INPUTS</span></span>

### <span data-ttu-id="66105-133">System. String</span><span class="sxs-lookup"><span data-stu-id="66105-133">System.String</span></span>
<span data-ttu-id="66105-134">Microsoft. Azure. Management. COMPUTE. Models.</span><span class="sxs-lookup"><span data-stu-id="66105-134">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="66105-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="66105-135">OUTPUTS</span></span>

### <span data-ttu-id="66105-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="66105-136">System.Object</span></span>

## <span data-ttu-id="66105-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="66105-137">NOTES</span></span>

## <span data-ttu-id="66105-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="66105-138">RELATED LINKS</span></span>

