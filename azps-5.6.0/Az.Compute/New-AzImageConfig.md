---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azimageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
ms.openlocfilehash: de59e8a9dc2fdcc4fa29409eaffc7f82e7d57b52
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977523"
---
# <span data-ttu-id="e9ce7-101">New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="e9ce7-101">New-AzImageConfig</span></span>

## <span data-ttu-id="e9ce7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9ce7-102">SYNOPSIS</span></span>
<span data-ttu-id="e9ce7-103">Создание настраиваемого объекта изображения.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-103">Creates a configurable image object.</span></span>

## <span data-ttu-id="e9ce7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e9ce7-104">SYNTAX</span></span>

```
New-AzImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-HyperVGeneration <String>] [-DataDisk <ImageDataDisk[]>] [-ZoneResilient]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9ce7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9ce7-105">DESCRIPTION</span></span>
<span data-ttu-id="e9ce7-106">Для создания настраиваемого объекта изображения будет создаваться **cmdlet New-AzImageConfig.**</span><span class="sxs-lookup"><span data-stu-id="e9ce7-106">The **New-AzImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="e9ce7-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e9ce7-107">EXAMPLES</span></span>

### <span data-ttu-id="e9ce7-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e9ce7-108">Example 1</span></span>
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

<span data-ttu-id="e9ce7-109">Первая команда создает объект изображения, а затем сохраняет его в переменной $imageConfig изображения.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="e9ce7-110">Следующие три команды назначают пути диска оси и два диска данных переменным $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="e9ce7-111">Этот подход подходит только для учитаемости следующих команд:</span><span class="sxs-lookup"><span data-stu-id="e9ce7-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="e9ce7-112">Следующие три команды добавляют диск оси и два диска данных к изображению, хранямуся в $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="e9ce7-113">URI каждого диска хранится в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="e9ce7-114">Конечная команда создает изображение с именем "ИмяСхема01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="e9ce7-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e9ce7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9ce7-115">PARAMETERS</span></span>

### <span data-ttu-id="e9ce7-116">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="e9ce7-116">-DataDisk</span></span>
<span data-ttu-id="e9ce7-117">Определяет объект диска данных.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-117">Specifies the data disk object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9ce7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9ce7-118">-DefaultProfile</span></span>
<span data-ttu-id="e9ce7-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9ce7-120">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="e9ce7-120">-HyperVGeneration</span></span>
<span data-ttu-id="e9ce7-121">Тип HyperVGeneration для виртуальной машины, созданной на изображении.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-121">Specifies the HyperVGeneration Type for the virtual machine created from the image.</span></span>  <span data-ttu-id="e9ce7-122">Допустимые значения: V1 и V2.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-122">Allowed values are V1 and V2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9ce7-123">-Location</span><span class="sxs-lookup"><span data-stu-id="e9ce7-123">-Location</span></span>
<span data-ttu-id="e9ce7-124">Определяет расположение.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-124">Specifies a location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9ce7-125">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="e9ce7-125">-OsDisk</span></span>
<span data-ttu-id="e9ce7-126">Определяет диск операционной системы.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-126">Specifies the operating system Disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageOSDisk
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9ce7-127">-SourceVirtualMavireId</span><span class="sxs-lookup"><span data-stu-id="e9ce7-127">-SourceVirtualMachineId</span></span>
<span data-ttu-id="e9ce7-128">Определяет исходный код виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-128">Specifies the source virtual machine ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9ce7-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="e9ce7-129">-Tag</span></span>
<span data-ttu-id="e9ce7-130">Пары "ключевое значение" в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e9ce7-131">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="e9ce7-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9ce7-132">-ZoneResilient</span><span class="sxs-lookup"><span data-stu-id="e9ce7-132">-ZoneResilient</span></span>
<span data-ttu-id="e9ce7-133">Отказоустойчивые зоны</span><span class="sxs-lookup"><span data-stu-id="e9ce7-133">Enable zone resilient</span></span>

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

### <span data-ttu-id="e9ce7-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9ce7-134">-Confirm</span></span>
<span data-ttu-id="e9ce7-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9ce7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9ce7-136">-WhatIf</span></span>
<span data-ttu-id="e9ce7-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e9ce7-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9ce7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9ce7-139">CommonParameters</span></span>
<span data-ttu-id="e9ce7-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9ce7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9ce7-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9ce7-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9ce7-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e9ce7-142">INPUTS</span></span>

### <span data-ttu-id="e9ce7-143">System.String</span><span class="sxs-lookup"><span data-stu-id="e9ce7-143">System.String</span></span>

### <span data-ttu-id="e9ce7-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e9ce7-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e9ce7-145">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span><span class="sxs-lookup"><span data-stu-id="e9ce7-145">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span></span>

### <span data-ttu-id="e9ce7-146">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span><span class="sxs-lookup"><span data-stu-id="e9ce7-146">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="e9ce7-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e9ce7-147">OUTPUTS</span></span>

### <span data-ttu-id="e9ce7-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="e9ce7-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="e9ce7-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e9ce7-149">NOTES</span></span>

## <span data-ttu-id="e9ce7-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e9ce7-150">RELATED LINKS</span></span>
