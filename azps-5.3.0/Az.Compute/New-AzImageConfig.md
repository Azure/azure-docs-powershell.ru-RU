---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azimageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
ms.openlocfilehash: 56834ad267b4ac60613afc4dbd08499eae212512
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509097"
---
# <span data-ttu-id="1d94e-101">New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="1d94e-101">New-AzImageConfig</span></span>

## <span data-ttu-id="1d94e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d94e-102">SYNOPSIS</span></span>
<span data-ttu-id="1d94e-103">Создание настраиваемого объекта изображения.</span><span class="sxs-lookup"><span data-stu-id="1d94e-103">Creates a configurable image object.</span></span>

## <span data-ttu-id="1d94e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1d94e-104">SYNTAX</span></span>

```
New-AzImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-HyperVGeneration <String>] [-DataDisk <ImageDataDisk[]>] [-ZoneResilient]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d94e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d94e-105">DESCRIPTION</span></span>
<span data-ttu-id="1d94e-106">Для создания настраиваемого объекта изображения будет создаваться **cmdlet New-AzImageConfig.**</span><span class="sxs-lookup"><span data-stu-id="1d94e-106">The **New-AzImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="1d94e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1d94e-107">EXAMPLES</span></span>

### <span data-ttu-id="1d94e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1d94e-108">Example 1</span></span>
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

<span data-ttu-id="1d94e-109">Первая команда создает объект изображения, а затем сохраняет его в $imageConfig переменной.</span><span class="sxs-lookup"><span data-stu-id="1d94e-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="1d94e-110">Следующие три команды назначают пути диска оси и два диска данных переменным $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="1d94e-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="1d94e-111">Этот подход подходит только для учитаемости следующих команд:</span><span class="sxs-lookup"><span data-stu-id="1d94e-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="1d94e-112">Следующие три команды добавляют диск оси и два диска данных к изображению, хранямуся в $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="1d94e-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="1d94e-113">URI каждого диска хранится в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="1d94e-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="1d94e-114">В конечная команда создается изображение с именем "ИмяСхема01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="1d94e-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="1d94e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d94e-115">PARAMETERS</span></span>

### <span data-ttu-id="1d94e-116">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="1d94e-116">-DataDisk</span></span>
<span data-ttu-id="1d94e-117">Определяет объект диска данных.</span><span class="sxs-lookup"><span data-stu-id="1d94e-117">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="1d94e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d94e-118">-DefaultProfile</span></span>
<span data-ttu-id="1d94e-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1d94e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d94e-120">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="1d94e-120">-HyperVGeneration</span></span>
<span data-ttu-id="1d94e-121">Тип HyperVGeneration для виртуальной машины, созданной на изображении.</span><span class="sxs-lookup"><span data-stu-id="1d94e-121">Specifies the HyperVGeneration Type for the virtual machine created from the image.</span></span>  <span data-ttu-id="1d94e-122">Допустимые значения: V1 и V2.</span><span class="sxs-lookup"><span data-stu-id="1d94e-122">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="1d94e-123">-Location</span><span class="sxs-lookup"><span data-stu-id="1d94e-123">-Location</span></span>
<span data-ttu-id="1d94e-124">Определяет расположение.</span><span class="sxs-lookup"><span data-stu-id="1d94e-124">Specifies a location.</span></span>

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

### <span data-ttu-id="1d94e-125">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="1d94e-125">-OsDisk</span></span>
<span data-ttu-id="1d94e-126">Определяет диск операционной системы.</span><span class="sxs-lookup"><span data-stu-id="1d94e-126">Specifies the operating system Disk.</span></span>

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

### <span data-ttu-id="1d94e-127">-SourceVirtualMavireId</span><span class="sxs-lookup"><span data-stu-id="1d94e-127">-SourceVirtualMachineId</span></span>
<span data-ttu-id="1d94e-128">Определяет исходный код виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1d94e-128">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="1d94e-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="1d94e-129">-Tag</span></span>
<span data-ttu-id="1d94e-130">Пары значений ключа в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="1d94e-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1d94e-131">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="1d94e-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1d94e-132">-ZoneResilient</span><span class="sxs-lookup"><span data-stu-id="1d94e-132">-ZoneResilient</span></span>
<span data-ttu-id="1d94e-133">Отказоустойчивые зоны</span><span class="sxs-lookup"><span data-stu-id="1d94e-133">Enable zone resilient</span></span>

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

### <span data-ttu-id="1d94e-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d94e-134">-Confirm</span></span>
<span data-ttu-id="1d94e-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d94e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d94e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d94e-136">-WhatIf</span></span>
<span data-ttu-id="1d94e-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d94e-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1d94e-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1d94e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d94e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d94e-139">CommonParameters</span></span>
<span data-ttu-id="1d94e-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d94e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d94e-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d94e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d94e-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d94e-142">INPUTS</span></span>

### <span data-ttu-id="1d94e-143">System.String</span><span class="sxs-lookup"><span data-stu-id="1d94e-143">System.String</span></span>

### <span data-ttu-id="1d94e-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1d94e-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1d94e-145">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span><span class="sxs-lookup"><span data-stu-id="1d94e-145">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span></span>

### <span data-ttu-id="1d94e-146">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span><span class="sxs-lookup"><span data-stu-id="1d94e-146">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="1d94e-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1d94e-147">OUTPUTS</span></span>

### <span data-ttu-id="1d94e-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="1d94e-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="1d94e-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1d94e-149">NOTES</span></span>

## <span data-ttu-id="1d94e-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1d94e-150">RELATED LINKS</span></span>