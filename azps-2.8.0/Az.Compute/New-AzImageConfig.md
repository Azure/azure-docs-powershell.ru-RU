---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azimageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
ms.openlocfilehash: c76ccab31b3c5c11216a1a929e2a78df55713325
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721839"
---
# <span data-ttu-id="51538-101">New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="51538-101">New-AzImageConfig</span></span>

## <span data-ttu-id="51538-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="51538-102">SYNOPSIS</span></span>
<span data-ttu-id="51538-103">Создание настраиваемого объекта изображения.</span><span class="sxs-lookup"><span data-stu-id="51538-103">Creates a configurable image object.</span></span>

## <span data-ttu-id="51538-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="51538-104">SYNTAX</span></span>

```
New-AzImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-HyperVGeneration <String>] [-DataDisk <ImageDataDisk[]>] [-ZoneResilient]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51538-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="51538-105">DESCRIPTION</span></span>
<span data-ttu-id="51538-106">Командлет **New-AzImageConfig** создает настраиваемый объект Image.</span><span class="sxs-lookup"><span data-stu-id="51538-106">The **New-AzImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="51538-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="51538-107">EXAMPLES</span></span>

### <span data-ttu-id="51538-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="51538-108">Example 1</span></span>
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

<span data-ttu-id="51538-109">В первой команде создается объект Image, который затем сохраняется в переменной $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="51538-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="51538-110">Следующие три команды назначают пути к диску операционной системы и двум дискам данных в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2 переменные.</span><span class="sxs-lookup"><span data-stu-id="51538-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="51538-111">Этот подход предназначен для чтения следующих команд.</span><span class="sxs-lookup"><span data-stu-id="51538-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="51538-112">Следующие три команды добавляют диск операционной системы и два диска данных в образ, хранящийся в $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="51538-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="51538-113">Универсальный код ресурса (URI) каждого диска хранится в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="51538-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="51538-114">Последняя команда создает изображение с именем "ImageName01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="51538-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="51538-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="51538-115">PARAMETERS</span></span>

### <span data-ttu-id="51538-116">-Диск</span><span class="sxs-lookup"><span data-stu-id="51538-116">-DataDisk</span></span>
<span data-ttu-id="51538-117">Указывает объект диска данных.</span><span class="sxs-lookup"><span data-stu-id="51538-117">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="51538-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51538-118">-DefaultProfile</span></span>
<span data-ttu-id="51538-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="51538-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51538-120">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="51538-120">-HyperVGeneration</span></span>
<span data-ttu-id="51538-121">Указывает тип HyperVGeneration для виртуальной машины, созданной из образа.</span><span class="sxs-lookup"><span data-stu-id="51538-121">Specifies the HyperVGeneration Type for the virtual machine created from the image.</span></span>  <span data-ttu-id="51538-122">Допустимые значения: v1 и v2.</span><span class="sxs-lookup"><span data-stu-id="51538-122">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="51538-123">-Location</span><span class="sxs-lookup"><span data-stu-id="51538-123">-Location</span></span>
<span data-ttu-id="51538-124">Задает расположение.</span><span class="sxs-lookup"><span data-stu-id="51538-124">Specifies a location.</span></span>

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

### <span data-ttu-id="51538-125">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="51538-125">-OsDisk</span></span>
<span data-ttu-id="51538-126">Указывает диск операционной системы.</span><span class="sxs-lookup"><span data-stu-id="51538-126">Specifies the operating system Disk.</span></span>

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

### <span data-ttu-id="51538-127">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="51538-127">-SourceVirtualMachineId</span></span>
<span data-ttu-id="51538-128">Указывает идентификатор исходной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="51538-128">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="51538-129">-Тег</span><span class="sxs-lookup"><span data-stu-id="51538-129">-Tag</span></span>
<span data-ttu-id="51538-130">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="51538-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="51538-131">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="51538-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="51538-132">-ZoneResilient</span><span class="sxs-lookup"><span data-stu-id="51538-132">-ZoneResilient</span></span>
<span data-ttu-id="51538-133">Включение отказоустойчивости зоны</span><span class="sxs-lookup"><span data-stu-id="51538-133">Enable zone resilient</span></span>

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

### <span data-ttu-id="51538-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51538-134">-Confirm</span></span>
<span data-ttu-id="51538-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="51538-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51538-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51538-136">-WhatIf</span></span>
<span data-ttu-id="51538-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="51538-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51538-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="51538-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51538-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51538-139">CommonParameters</span></span>
<span data-ttu-id="51538-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="51538-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51538-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51538-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51538-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="51538-142">INPUTS</span></span>

### <span data-ttu-id="51538-143">System. String</span><span class="sxs-lookup"><span data-stu-id="51538-143">System.String</span></span>

### <span data-ttu-id="51538-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="51538-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="51538-145">Microsoft. Azure. Management. COMPUTE. Models. ImageOSDisk</span><span class="sxs-lookup"><span data-stu-id="51538-145">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span></span>

### <span data-ttu-id="51538-146">Microsoft. Azure. Management. COMPUTE. Models. ImageDataDisk []</span><span class="sxs-lookup"><span data-stu-id="51538-146">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="51538-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="51538-147">OUTPUTS</span></span>

### <span data-ttu-id="51538-148">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="51538-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="51538-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="51538-149">NOTES</span></span>

## <span data-ttu-id="51538-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="51538-150">RELATED LINKS</span></span>
