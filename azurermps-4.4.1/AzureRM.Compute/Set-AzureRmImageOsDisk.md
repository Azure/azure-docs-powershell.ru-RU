---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmImageOsDisk.md
ms.openlocfilehash: 3e9fd68c43bda2d98fe2c2948d32032f7f687d72
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557839"
---
# <span data-ttu-id="cca6c-101">Set-AzureRmImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="cca6c-101">Set-AzureRmImageOsDisk</span></span>

## <span data-ttu-id="cca6c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cca6c-102">SYNOPSIS</span></span>
<span data-ttu-id="cca6c-103">Задает свойства диска операционной системы для объекта Image.</span><span class="sxs-lookup"><span data-stu-id="cca6c-103">Sets the operating system disk properties on an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cca6c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cca6c-104">SYNTAX</span></span>

```
Set-AzureRmImageOsDisk [-Image] <PSImage> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <StorageAccountTypes>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cca6c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cca6c-105">DESCRIPTION</span></span>
<span data-ttu-id="cca6c-106">Командлет **Set-AzureRmImageOsDisk** задает свойства диска операционной системы для объекта Image.</span><span class="sxs-lookup"><span data-stu-id="cca6c-106">The **Set-AzureRmImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="cca6c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cca6c-107">EXAMPLES</span></span>

### <span data-ttu-id="cca6c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cca6c-108">Example 1</span></span>
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

<span data-ttu-id="cca6c-109">В первой команде создается объект Image, который затем сохраняется в переменной $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="cca6c-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="cca6c-110">Следующие три команды назначают пути к диску операционной системы и двум дискам данных в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2 переменные.</span><span class="sxs-lookup"><span data-stu-id="cca6c-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="cca6c-111">Этот подход предназначен для чтения следующих команд.</span><span class="sxs-lookup"><span data-stu-id="cca6c-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="cca6c-112">Следующие три команды добавляют диск операционной системы и два диска данных в образ, хранящийся в $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="cca6c-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="cca6c-113">Универсальный код ресурса (URI) каждого диска хранится в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="cca6c-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="cca6c-114">Последняя команда создает изображение с именем "ImageName01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="cca6c-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="cca6c-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cca6c-115">PARAMETERS</span></span>

### <span data-ttu-id="cca6c-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="cca6c-116">-BlobUri</span></span>
<span data-ttu-id="cca6c-117">Задает универсальный код ресурса (URI) большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="cca6c-117">Specifies the Uri of the blob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cca6c-118">-Caching</span><span class="sxs-lookup"><span data-stu-id="cca6c-118">-Caching</span></span>
<span data-ttu-id="cca6c-119">Задает режим кэширования диска.</span><span class="sxs-lookup"><span data-stu-id="cca6c-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cca6c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cca6c-120">-DefaultProfile</span></span>
<span data-ttu-id="cca6c-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cca6c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cca6c-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="cca6c-122">-DiskSizeGB</span></span>
<span data-ttu-id="cca6c-123">Задает размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="cca6c-123">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cca6c-124">-Image</span><span class="sxs-lookup"><span data-stu-id="cca6c-124">-Image</span></span>
<span data-ttu-id="cca6c-125">Указывает локальный объект изображения.</span><span class="sxs-lookup"><span data-stu-id="cca6c-125">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cca6c-126">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="cca6c-126">-ManagedDiskId</span></span>
<span data-ttu-id="cca6c-127">Указывает идентификатор управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="cca6c-127">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="cca6c-128">-OsState</span><span class="sxs-lookup"><span data-stu-id="cca6c-128">-OsState</span></span>
<span data-ttu-id="cca6c-129">Указывает состояние операционной системы.</span><span class="sxs-lookup"><span data-stu-id="cca6c-129">Specifies the OS state.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: Generalized, Specialized

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cca6c-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="cca6c-130">-OsType</span></span>
<span data-ttu-id="cca6c-131">Указывает тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="cca6c-131">Specifies the OS type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cca6c-132">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="cca6c-132">-SnapshotId</span></span>
<span data-ttu-id="cca6c-133">Указывает идентификатор снимка.</span><span class="sxs-lookup"><span data-stu-id="cca6c-133">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="cca6c-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="cca6c-134">-StorageAccountType</span></span>
<span data-ttu-id="cca6c-135">Тип учетной записи хранения на диске образа операционной системы</span><span class="sxs-lookup"><span data-stu-id="cca6c-135">The Storage Account type of Os Image Disk</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cca6c-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cca6c-136">-Confirm</span></span>
<span data-ttu-id="cca6c-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cca6c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cca6c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cca6c-138">-WhatIf</span></span>
<span data-ttu-id="cca6c-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cca6c-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cca6c-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cca6c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cca6c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cca6c-141">CommonParameters</span></span>
<span data-ttu-id="cca6c-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cca6c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cca6c-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cca6c-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cca6c-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cca6c-144">INPUTS</span></span>

### <span data-ttu-id="cca6c-145">Microsoft. Azure. Management. COMPUTE. Models.</span><span class="sxs-lookup"><span data-stu-id="cca6c-145">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="cca6c-146">System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[Microsoft. Azure. Management. COMPUTE. Version = 14.0.0.0, Culture. OperatingSystemStateTypes;. System. String.. Nullable, # = 31bf3856ad364e35]] String. строковых параметров `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` : NULL 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="cca6c-146">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.String System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="cca6c-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cca6c-147">OUTPUTS</span></span>

### <span data-ttu-id="cca6c-148">Microsoft. Azure. Management. COMPUTE. Models.</span><span class="sxs-lookup"><span data-stu-id="cca6c-148">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="cca6c-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="cca6c-149">NOTES</span></span>

## <span data-ttu-id="cca6c-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cca6c-150">RELATED LINKS</span></span>

