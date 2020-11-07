---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azimageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzImageConfig.md
ms.openlocfilehash: de6c09c6c86fa4da7eff57439f556d21d18d94a0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911472"
---
# <span data-ttu-id="75bd1-101">New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="75bd1-101">New-AzImageConfig</span></span>

## <span data-ttu-id="75bd1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="75bd1-102">SYNOPSIS</span></span>
<span data-ttu-id="75bd1-103">Создание настраиваемого объекта изображения.</span><span class="sxs-lookup"><span data-stu-id="75bd1-103">Creates a configurable image object.</span></span>

## <span data-ttu-id="75bd1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="75bd1-104">SYNTAX</span></span>

```
New-AzImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-DataDisk <ImageDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75bd1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75bd1-105">DESCRIPTION</span></span>
<span data-ttu-id="75bd1-106">Командлет **New-AzImageConfig** создает настраиваемый объект Image.</span><span class="sxs-lookup"><span data-stu-id="75bd1-106">The **New-AzImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="75bd1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="75bd1-107">EXAMPLES</span></span>

### <span data-ttu-id="75bd1-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="75bd1-108">Example 1</span></span>
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

<span data-ttu-id="75bd1-109">В первой команде создается объект Image, который затем сохраняется в переменной $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="75bd1-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="75bd1-110">Следующие три команды назначают пути к диску операционной системы и двум дискам данных в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2 переменные.</span><span class="sxs-lookup"><span data-stu-id="75bd1-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="75bd1-111">Этот подход предназначен для чтения следующих команд.</span><span class="sxs-lookup"><span data-stu-id="75bd1-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="75bd1-112">Следующие три команды добавляют диск операционной системы и два диска данных в образ, хранящийся в $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="75bd1-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="75bd1-113">Универсальный код ресурса (URI) каждого диска хранится в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="75bd1-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="75bd1-114">Последняя команда создает изображение с именем "ImageName01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="75bd1-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="75bd1-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="75bd1-115">PARAMETERS</span></span>

### <span data-ttu-id="75bd1-116">-Диск</span><span class="sxs-lookup"><span data-stu-id="75bd1-116">-DataDisk</span></span>
<span data-ttu-id="75bd1-117">Указывает объект диска данных.</span><span class="sxs-lookup"><span data-stu-id="75bd1-117">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="75bd1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75bd1-118">-DefaultProfile</span></span>
<span data-ttu-id="75bd1-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="75bd1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75bd1-120">-Location</span><span class="sxs-lookup"><span data-stu-id="75bd1-120">-Location</span></span>
<span data-ttu-id="75bd1-121">Задает расположение.</span><span class="sxs-lookup"><span data-stu-id="75bd1-121">Specifies a location.</span></span>

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

### <span data-ttu-id="75bd1-122">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="75bd1-122">-OsDisk</span></span>
<span data-ttu-id="75bd1-123">Указывает диск операционной системы.</span><span class="sxs-lookup"><span data-stu-id="75bd1-123">Specifies the operating system Disk.</span></span>

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

### <span data-ttu-id="75bd1-124">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="75bd1-124">-SourceVirtualMachineId</span></span>
<span data-ttu-id="75bd1-125">Указывает идентификатор исходной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="75bd1-125">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="75bd1-126">-Тег</span><span class="sxs-lookup"><span data-stu-id="75bd1-126">-Tag</span></span>
<span data-ttu-id="75bd1-127">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="75bd1-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="75bd1-128">Например:</span><span class="sxs-lookup"><span data-stu-id="75bd1-128">For example:</span></span>

<span data-ttu-id="75bd1-129">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="75bd1-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="75bd1-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75bd1-130">-Confirm</span></span>
<span data-ttu-id="75bd1-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="75bd1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75bd1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75bd1-132">-WhatIf</span></span>
<span data-ttu-id="75bd1-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="75bd1-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75bd1-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="75bd1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75bd1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75bd1-135">CommonParameters</span></span>
<span data-ttu-id="75bd1-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="75bd1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75bd1-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75bd1-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75bd1-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="75bd1-138">INPUTS</span></span>

### <span data-ttu-id="75bd1-139">Ничего</span><span class="sxs-lookup"><span data-stu-id="75bd1-139">None</span></span>
<span data-ttu-id="75bd1-140">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="75bd1-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="75bd1-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="75bd1-141">OUTPUTS</span></span>

### <span data-ttu-id="75bd1-142">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="75bd1-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="75bd1-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="75bd1-143">NOTES</span></span>

## <span data-ttu-id="75bd1-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75bd1-144">RELATED LINKS</span></span>

