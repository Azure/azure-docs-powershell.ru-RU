---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImage.md
ms.openlocfilehash: a95e577ee216d420ba419b200bbb8fffb676f8b6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721840"
---
# <span data-ttu-id="3ded0-101">New-AzImage</span><span class="sxs-lookup"><span data-stu-id="3ded0-101">New-AzImage</span></span>

## <span data-ttu-id="3ded0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3ded0-102">SYNOPSIS</span></span>
<span data-ttu-id="3ded0-103">Создание изображения.</span><span class="sxs-lookup"><span data-stu-id="3ded0-103">Creates an image.</span></span>

## <span data-ttu-id="3ded0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3ded0-104">SYNTAX</span></span>

```
New-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ded0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ded0-105">DESCRIPTION</span></span>
<span data-ttu-id="3ded0-106">Командлет **New-AzImage** создает изображение.</span><span class="sxs-lookup"><span data-stu-id="3ded0-106">The **New-AzImage** cmdlet creates an image.</span></span>

## <span data-ttu-id="3ded0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3ded0-107">EXAMPLES</span></span>

### <span data-ttu-id="3ded0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3ded0-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="3ded0-109">В первой команде создается объект Image, который затем сохраняется в переменной $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="3ded0-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="3ded0-110">Следующие три команды назначают пути к диску операционной системы и двум дискам данных в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2 переменные.</span><span class="sxs-lookup"><span data-stu-id="3ded0-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="3ded0-111">Этот подход предназначен для чтения следующих команд.</span><span class="sxs-lookup"><span data-stu-id="3ded0-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="3ded0-112">Следующие три команды добавляют диск операционной системы и два диска данных в образ, хранящийся в $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="3ded0-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="3ded0-113">Универсальный код ресурса (URI) каждого диска хранится в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="3ded0-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="3ded0-114">Последняя команда создает изображение с именем "ImageName01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="3ded0-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="3ded0-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3ded0-115">PARAMETERS</span></span>

### <span data-ttu-id="3ded0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ded0-116">-AsJob</span></span>
<span data-ttu-id="3ded0-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3ded0-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3ded0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ded0-118">-DefaultProfile</span></span>
<span data-ttu-id="3ded0-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3ded0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ded0-120">-Image</span><span class="sxs-lookup"><span data-stu-id="3ded0-120">-Image</span></span>
<span data-ttu-id="3ded0-121">Указывает локальный объект изображения.</span><span class="sxs-lookup"><span data-stu-id="3ded0-121">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ded0-122">-ImageName</span><span class="sxs-lookup"><span data-stu-id="3ded0-122">-ImageName</span></span>
<span data-ttu-id="3ded0-123">Указывает имя изображения.</span><span class="sxs-lookup"><span data-stu-id="3ded0-123">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ded0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ded0-124">-ResourceGroupName</span></span>
<span data-ttu-id="3ded0-125">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3ded0-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ded0-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ded0-126">-Confirm</span></span>
<span data-ttu-id="3ded0-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3ded0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ded0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ded0-128">-WhatIf</span></span>
<span data-ttu-id="3ded0-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3ded0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ded0-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3ded0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ded0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ded0-131">CommonParameters</span></span>
<span data-ttu-id="3ded0-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3ded0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ded0-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ded0-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ded0-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3ded0-134">INPUTS</span></span>

### <span data-ttu-id="3ded0-135">System. String</span><span class="sxs-lookup"><span data-stu-id="3ded0-135">System.String</span></span>

### <span data-ttu-id="3ded0-136">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="3ded0-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="3ded0-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ded0-137">OUTPUTS</span></span>

### <span data-ttu-id="3ded0-138">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="3ded0-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="3ded0-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="3ded0-139">NOTES</span></span>

## <span data-ttu-id="3ded0-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ded0-140">RELATED LINKS</span></span>
