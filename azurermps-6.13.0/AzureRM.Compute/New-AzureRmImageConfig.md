---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermimageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmImageConfig.md
ms.openlocfilehash: f2d5903de64655b79765774f7232790f8a00ffc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734685"
---
# <span data-ttu-id="52a34-101">New-AzureRmImageConfig</span><span class="sxs-lookup"><span data-stu-id="52a34-101">New-AzureRmImageConfig</span></span>

## <span data-ttu-id="52a34-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="52a34-102">SYNOPSIS</span></span>
<span data-ttu-id="52a34-103">Создание настраиваемого объекта изображения.</span><span class="sxs-lookup"><span data-stu-id="52a34-103">Creates a configurable image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52a34-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="52a34-104">SYNTAX</span></span>

```
New-AzureRmImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-DataDisk <ImageDataDisk[]>] [-ZoneResilient]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52a34-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="52a34-105">DESCRIPTION</span></span>
<span data-ttu-id="52a34-106">Командлет **New-AzureRmImageConfig** создает настраиваемый объект Image.</span><span class="sxs-lookup"><span data-stu-id="52a34-106">The **New-AzureRmImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="52a34-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="52a34-107">EXAMPLES</span></span>

### <span data-ttu-id="52a34-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="52a34-108">Example 1</span></span>
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

<span data-ttu-id="52a34-109">В первой команде создается объект Image, который затем сохраняется в переменной $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="52a34-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="52a34-110">Следующие три команды назначают пути к диску операционной системы и двум дискам данных в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2 переменные.</span><span class="sxs-lookup"><span data-stu-id="52a34-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="52a34-111">Этот подход предназначен для чтения следующих команд.</span><span class="sxs-lookup"><span data-stu-id="52a34-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="52a34-112">Следующие три команды добавляют диск операционной системы и два диска данных в образ, хранящийся в $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="52a34-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="52a34-113">Универсальный код ресурса (URI) каждого диска хранится в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="52a34-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="52a34-114">Последняя команда создает изображение с именем "ImageName01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="52a34-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="52a34-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="52a34-115">PARAMETERS</span></span>

### <span data-ttu-id="52a34-116">-Диск</span><span class="sxs-lookup"><span data-stu-id="52a34-116">-DataDisk</span></span>
<span data-ttu-id="52a34-117">Указывает объект диска данных.</span><span class="sxs-lookup"><span data-stu-id="52a34-117">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="52a34-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52a34-118">-DefaultProfile</span></span>
<span data-ttu-id="52a34-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="52a34-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52a34-120">-Location</span><span class="sxs-lookup"><span data-stu-id="52a34-120">-Location</span></span>
<span data-ttu-id="52a34-121">Задает расположение.</span><span class="sxs-lookup"><span data-stu-id="52a34-121">Specifies a location.</span></span>

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

### <span data-ttu-id="52a34-122">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="52a34-122">-OsDisk</span></span>
<span data-ttu-id="52a34-123">Указывает диск операционной системы.</span><span class="sxs-lookup"><span data-stu-id="52a34-123">Specifies the operating system Disk.</span></span>

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

### <span data-ttu-id="52a34-124">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="52a34-124">-SourceVirtualMachineId</span></span>
<span data-ttu-id="52a34-125">Указывает идентификатор исходной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="52a34-125">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="52a34-126">-Тег</span><span class="sxs-lookup"><span data-stu-id="52a34-126">-Tag</span></span>
<span data-ttu-id="52a34-127">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="52a34-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="52a34-128">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="52a34-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="52a34-129">-ZoneResilient</span><span class="sxs-lookup"><span data-stu-id="52a34-129">-ZoneResilient</span></span>
<span data-ttu-id="52a34-130">Включение отказоустойчивости зоны</span><span class="sxs-lookup"><span data-stu-id="52a34-130">Enable zone resilient</span></span>

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

### <span data-ttu-id="52a34-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52a34-131">-Confirm</span></span>
<span data-ttu-id="52a34-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="52a34-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52a34-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52a34-133">-WhatIf</span></span>
<span data-ttu-id="52a34-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="52a34-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52a34-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="52a34-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52a34-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52a34-136">CommonParameters</span></span>
<span data-ttu-id="52a34-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="52a34-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52a34-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52a34-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52a34-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="52a34-139">INPUTS</span></span>

### <span data-ttu-id="52a34-140">System. String</span><span class="sxs-lookup"><span data-stu-id="52a34-140">System.String</span></span>

### <span data-ttu-id="52a34-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="52a34-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="52a34-142">Microsoft. Azure. Management. COMPUTE. Models. ImageOSDisk</span><span class="sxs-lookup"><span data-stu-id="52a34-142">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span></span>

### <span data-ttu-id="52a34-143">Microsoft. Azure. Management. COMPUTE. Models. ImageDataDisk []</span><span class="sxs-lookup"><span data-stu-id="52a34-143">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="52a34-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="52a34-144">OUTPUTS</span></span>

### <span data-ttu-id="52a34-145">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="52a34-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="52a34-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="52a34-146">NOTES</span></span>

## <span data-ttu-id="52a34-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="52a34-147">RELATED LINKS</span></span>
