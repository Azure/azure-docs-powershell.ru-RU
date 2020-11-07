---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermimageconfig
schema: 2.0.0
ms.openlocfilehash: ef9fc830b59568ad039b265fb182dbbdbd13a00d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913487"
---
# <span data-ttu-id="5a6bb-101">New-AzureRmImageConfig</span><span class="sxs-lookup"><span data-stu-id="5a6bb-101">New-AzureRmImageConfig</span></span>

## <span data-ttu-id="5a6bb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5a6bb-102">SYNOPSIS</span></span>
<span data-ttu-id="5a6bb-103">Создание настраиваемого объекта изображения.</span><span class="sxs-lookup"><span data-stu-id="5a6bb-103">Creates a configurable image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a6bb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5a6bb-104">SYNTAX</span></span>

```
New-AzureRmImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-DataDisk <ImageDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a6bb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a6bb-105">DESCRIPTION</span></span>
<span data-ttu-id="5a6bb-106">Командлет **New-AzureRmImageConfig** создает настраиваемый объект Image.</span><span class="sxs-lookup"><span data-stu-id="5a6bb-106">The **New-AzureRmImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="5a6bb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5a6bb-107">EXAMPLES</span></span>

### <span data-ttu-id="5a6bb-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5a6bb-108">Example 1</span></span>
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

<span data-ttu-id="5a6bb-109">В первой команде создается объект Image, который затем сохраняется в переменной $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="5a6bb-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="5a6bb-110">Следующие три команды назначают пути к диску операционной системы и двум дискам данных в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2 переменные.</span><span class="sxs-lookup"><span data-stu-id="5a6bb-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="5a6bb-111">Этот подход предназначен для чтения следующих команд.</span><span class="sxs-lookup"><span data-stu-id="5a6bb-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="5a6bb-112">Следующие три команды добавляют диск операционной системы и два диска данных в образ, хранящийся в $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="5a6bb-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="5a6bb-113">Универсальный код ресурса (URI) каждого диска хранится в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="5a6bb-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="5a6bb-114">Последняя команда создает изображение с именем "ImageName01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="5a6bb-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="5a6bb-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5a6bb-115">PARAMETERS</span></span>

### <span data-ttu-id="5a6bb-116">-Диск</span><span class="sxs-lookup"><span data-stu-id="5a6bb-116">-DataDisk</span></span>
<span data-ttu-id="5a6bb-117">Указывает объект диска данных.</span><span class="sxs-lookup"><span data-stu-id="5a6bb-117">Specifies the data disk object.</span></span>

```yaml
Type: ImageDataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a6bb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a6bb-118">-DefaultProfile</span></span>
<span data-ttu-id="5a6bb-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5a6bb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a6bb-120">-Location</span><span class="sxs-lookup"><span data-stu-id="5a6bb-120">-Location</span></span>
<span data-ttu-id="5a6bb-121">Задает расположение.</span><span class="sxs-lookup"><span data-stu-id="5a6bb-121">Specifies a location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a6bb-122">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="5a6bb-122">-OsDisk</span></span>
<span data-ttu-id="5a6bb-123">Указывает диск операционной системы.</span><span class="sxs-lookup"><span data-stu-id="5a6bb-123">Specifies the operating system Disk.</span></span>

```yaml
Type: ImageOSDisk
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a6bb-124">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="5a6bb-124">-SourceVirtualMachineId</span></span>
<span data-ttu-id="5a6bb-125">Указывает идентификатор исходной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5a6bb-125">Specifies the source virtual machine ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a6bb-126">-Тег</span><span class="sxs-lookup"><span data-stu-id="5a6bb-126">-Tag</span></span>
<span data-ttu-id="5a6bb-127">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="5a6bb-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5a6bb-128">Например:</span><span class="sxs-lookup"><span data-stu-id="5a6bb-128">For example:</span></span>

<span data-ttu-id="5a6bb-129">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="5a6bb-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a6bb-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a6bb-130">-Confirm</span></span>
<span data-ttu-id="5a6bb-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5a6bb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a6bb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a6bb-132">-WhatIf</span></span>
<span data-ttu-id="5a6bb-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5a6bb-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a6bb-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5a6bb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a6bb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a6bb-135">CommonParameters</span></span>
<span data-ttu-id="5a6bb-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5a6bb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a6bb-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a6bb-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a6bb-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5a6bb-138">INPUTS</span></span>

### <span data-ttu-id="5a6bb-139">Ничего</span><span class="sxs-lookup"><span data-stu-id="5a6bb-139">None</span></span>
<span data-ttu-id="5a6bb-140">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="5a6bb-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5a6bb-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a6bb-141">OUTPUTS</span></span>

### <span data-ttu-id="5a6bb-142">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="5a6bb-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="5a6bb-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="5a6bb-143">NOTES</span></span>

## <span data-ttu-id="5a6bb-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a6bb-144">RELATED LINKS</span></span>

