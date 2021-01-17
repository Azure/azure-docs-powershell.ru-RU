---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImage.md
ms.openlocfilehash: ff291afae70636863dff8ce34b5610cd77ce1251
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323053"
---
# <span data-ttu-id="0411f-101">New-AzImage</span><span class="sxs-lookup"><span data-stu-id="0411f-101">New-AzImage</span></span>

## <span data-ttu-id="0411f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0411f-102">SYNOPSIS</span></span>
<span data-ttu-id="0411f-103">Создает изображение.</span><span class="sxs-lookup"><span data-stu-id="0411f-103">Creates an image.</span></span>

## <span data-ttu-id="0411f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0411f-104">SYNTAX</span></span>

```
New-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0411f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0411f-105">DESCRIPTION</span></span>
<span data-ttu-id="0411f-106">Для **этого создается новый cmdlet AzImage.**</span><span class="sxs-lookup"><span data-stu-id="0411f-106">The **New-AzImage** cmdlet creates an image.</span></span>

## <span data-ttu-id="0411f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0411f-107">EXAMPLES</span></span>

### <span data-ttu-id="0411f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0411f-108">Example 1</span></span>
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

<span data-ttu-id="0411f-109">Первая команда создает объект изображения, а затем сохраняет его в переменной $imageConfig изображения.</span><span class="sxs-lookup"><span data-stu-id="0411f-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="0411f-110">Следующие три команды назначают пути диска оси и два диска данных переменным $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="0411f-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="0411f-111">Этот подход подходит только для учитаемости следующих команд:</span><span class="sxs-lookup"><span data-stu-id="0411f-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="0411f-112">Следующие три команды добавляют диск оси и два диска данных к изображению, хранямуся в $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="0411f-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="0411f-113">URI каждого диска хранится в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="0411f-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="0411f-114">Конечная команда создает изображение с именем "ИмяСхема01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="0411f-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="0411f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0411f-115">PARAMETERS</span></span>

### <span data-ttu-id="0411f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0411f-116">-AsJob</span></span>
<span data-ttu-id="0411f-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0411f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0411f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0411f-118">-DefaultProfile</span></span>
<span data-ttu-id="0411f-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0411f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0411f-120">-Image</span><span class="sxs-lookup"><span data-stu-id="0411f-120">-Image</span></span>
<span data-ttu-id="0411f-121">Определяет объект локального изображения.</span><span class="sxs-lookup"><span data-stu-id="0411f-121">Specifies a local image object.</span></span>

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

### <span data-ttu-id="0411f-122">-ImageName</span><span class="sxs-lookup"><span data-stu-id="0411f-122">-ImageName</span></span>
<span data-ttu-id="0411f-123">Определяет имя изображения.</span><span class="sxs-lookup"><span data-stu-id="0411f-123">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="0411f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0411f-124">-ResourceGroupName</span></span>
<span data-ttu-id="0411f-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0411f-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0411f-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0411f-126">-Confirm</span></span>
<span data-ttu-id="0411f-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0411f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0411f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0411f-128">-WhatIf</span></span>
<span data-ttu-id="0411f-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0411f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0411f-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0411f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0411f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0411f-131">CommonParameters</span></span>
<span data-ttu-id="0411f-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0411f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0411f-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0411f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0411f-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0411f-134">INPUTS</span></span>

### <span data-ttu-id="0411f-135">System.String</span><span class="sxs-lookup"><span data-stu-id="0411f-135">System.String</span></span>

### <span data-ttu-id="0411f-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="0411f-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="0411f-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0411f-137">OUTPUTS</span></span>

### <span data-ttu-id="0411f-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="0411f-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="0411f-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0411f-139">NOTES</span></span>

## <span data-ttu-id="0411f-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0411f-140">RELATED LINKS</span></span>
