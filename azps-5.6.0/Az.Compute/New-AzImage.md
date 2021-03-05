---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImage.md
ms.openlocfilehash: 77a4879d403b52a828460bcfec5666b7071dcea9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959667"
---
# <span data-ttu-id="c62f3-101">New-AzImage</span><span class="sxs-lookup"><span data-stu-id="c62f3-101">New-AzImage</span></span>

## <span data-ttu-id="c62f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c62f3-102">SYNOPSIS</span></span>
<span data-ttu-id="c62f3-103">Создает изображение.</span><span class="sxs-lookup"><span data-stu-id="c62f3-103">Creates an image.</span></span>

## <span data-ttu-id="c62f3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c62f3-104">SYNTAX</span></span>

```
New-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c62f3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c62f3-105">DESCRIPTION</span></span>
<span data-ttu-id="c62f3-106">Для **этого создается новый cmdlet AzImage.**</span><span class="sxs-lookup"><span data-stu-id="c62f3-106">The **New-AzImage** cmdlet creates an image.</span></span>

## <span data-ttu-id="c62f3-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c62f3-107">EXAMPLES</span></span>

### <span data-ttu-id="c62f3-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c62f3-108">Example 1</span></span>
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

<span data-ttu-id="c62f3-109">Первая команда создает объект изображения, а затем сохраняет его в $imageConfig переменной.</span><span class="sxs-lookup"><span data-stu-id="c62f3-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="c62f3-110">Следующие три команды назначают пути диска оси и два диска данных переменным $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="c62f3-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="c62f3-111">Этот подход подходит только для учитаемости следующих команд:</span><span class="sxs-lookup"><span data-stu-id="c62f3-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="c62f3-112">Следующие три команды добавляют диск оси и два диска данных к изображению, хранямуся в $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="c62f3-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="c62f3-113">URI каждого диска хранится в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="c62f3-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="c62f3-114">В конечная команда создается изображение с именем "ИмяСхема01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="c62f3-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="c62f3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c62f3-115">PARAMETERS</span></span>

### <span data-ttu-id="c62f3-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c62f3-116">-AsJob</span></span>
<span data-ttu-id="c62f3-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c62f3-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c62f3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c62f3-118">-DefaultProfile</span></span>
<span data-ttu-id="c62f3-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c62f3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c62f3-120">-Image</span><span class="sxs-lookup"><span data-stu-id="c62f3-120">-Image</span></span>
<span data-ttu-id="c62f3-121">Определяет объект локального изображения.</span><span class="sxs-lookup"><span data-stu-id="c62f3-121">Specifies a local image object.</span></span>

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

### <span data-ttu-id="c62f3-122">-ImageName</span><span class="sxs-lookup"><span data-stu-id="c62f3-122">-ImageName</span></span>
<span data-ttu-id="c62f3-123">Определяет имя изображения.</span><span class="sxs-lookup"><span data-stu-id="c62f3-123">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="c62f3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c62f3-124">-ResourceGroupName</span></span>
<span data-ttu-id="c62f3-125">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c62f3-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c62f3-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c62f3-126">-Confirm</span></span>
<span data-ttu-id="c62f3-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c62f3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c62f3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c62f3-128">-WhatIf</span></span>
<span data-ttu-id="c62f3-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c62f3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c62f3-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c62f3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c62f3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c62f3-131">CommonParameters</span></span>
<span data-ttu-id="c62f3-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c62f3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c62f3-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c62f3-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c62f3-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c62f3-134">INPUTS</span></span>

### <span data-ttu-id="c62f3-135">System.String</span><span class="sxs-lookup"><span data-stu-id="c62f3-135">System.String</span></span>

### <span data-ttu-id="c62f3-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="c62f3-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="c62f3-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c62f3-137">OUTPUTS</span></span>

### <span data-ttu-id="c62f3-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="c62f3-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="c62f3-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c62f3-139">NOTES</span></span>

## <span data-ttu-id="c62f3-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c62f3-140">RELATED LINKS</span></span>
