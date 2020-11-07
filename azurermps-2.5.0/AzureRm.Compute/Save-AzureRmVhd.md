---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 18E1AD70-42A6-47A2-A685-6E218B6DC4BE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/save-azurermvhd
schema: 2.0.0
ms.openlocfilehash: 86a4cdb4fc0d6709d6cb9311d243f12dcb65e5de
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915369"
---
# <span data-ttu-id="729b2-101">Save-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="729b2-101">Save-AzureRmVhd</span></span>

## <span data-ttu-id="729b2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="729b2-102">SYNOPSIS</span></span>
<span data-ttu-id="729b2-103">Сохранение скачанных VHD-изображений на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="729b2-103">Saves downloaded .vhd images locally.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="729b2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="729b2-104">SYNTAX</span></span>

### <span data-ttu-id="729b2-105">ResourceGroupParameterSetName</span><span class="sxs-lookup"><span data-stu-id="729b2-105">ResourceGroupParameterSetName</span></span>
```
Save-AzureRmVhd [-ResourceGroupName] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="729b2-106">StorageKeyParameterSetName</span><span class="sxs-lookup"><span data-stu-id="729b2-106">StorageKeyParameterSetName</span></span>
```
Save-AzureRmVhd [-StorageKey] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="729b2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="729b2-107">DESCRIPTION</span></span>
<span data-ttu-id="729b2-108">Командлет **Save-AzureRmVhd** сохраняет файлы. VHD из большого двоичного объекта, в котором они хранятся в файле.</span><span class="sxs-lookup"><span data-stu-id="729b2-108">The **Save-AzureRmVhd** cmdlet saves .vhd images from a blob where they are stored to a file.</span></span>
<span data-ttu-id="729b2-109">Вы можете указать количество потоков загрузчика, используемых процессом, и определить, следует ли заменять уже существующий файл.</span><span class="sxs-lookup"><span data-stu-id="729b2-109">You can specify the number of downloader threads that the process uses and whether to replace a file that already exists.</span></span>

<span data-ttu-id="729b2-110">Этот командлет загружает содержимое в том виде, в котором оно установлено.</span><span class="sxs-lookup"><span data-stu-id="729b2-110">This cmdlet downloads content as it is.</span></span>
<span data-ttu-id="729b2-111">Преобразование форматов виртуальных жестких дисков (VHD) не применяется.</span><span class="sxs-lookup"><span data-stu-id="729b2-111">It does not apply any Virtual Hard Disk (VHD) format conversion.</span></span>

## <span data-ttu-id="729b2-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="729b2-112">EXAMPLES</span></span>

### <span data-ttu-id="729b2-113">Пример 1: Загрузка изображения</span><span class="sxs-lookup"><span data-stu-id="729b2-113">Example 1: Download an image</span></span>
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -ResourceGroupName "rgname"
```

<span data-ttu-id="729b2-114">Эта команда загружает VHD-файл и сохраняет его в локальном пути. C:\vhd\Win7Image.vhd.</span><span class="sxs-lookup"><span data-stu-id="729b2-114">This command downloads a .vhd file, and stores it in the local path C:\vhd\Win7Image.vhd.</span></span>

### <span data-ttu-id="729b2-115">Пример 2: скачивание изображения и перезапись локального файла</span><span class="sxs-lookup"><span data-stu-id="729b2-115">Example 2: Download an image and overwrite the local file</span></span>
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite -ResourceGroupName "rgname"
```

<span data-ttu-id="729b2-116">Эта команда загружает VHD-файл и сохраняет его в локальном пути.</span><span class="sxs-lookup"><span data-stu-id="729b2-116">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="729b2-117">Команда включает параметр *перезаписи* .</span><span class="sxs-lookup"><span data-stu-id="729b2-117">The command includes the *Overwrite* parameter.</span></span>
<span data-ttu-id="729b2-118">Таким образом, если C:\vhd\Win7Image.vhd уже существует, эта команда заменяет ее.</span><span class="sxs-lookup"><span data-stu-id="729b2-118">Therefore, if C:\vhd\Win7Image.vhd already exists, this command replaces it.</span></span>

### <span data-ttu-id="729b2-119">Пример 3: Загрузка изображения с указанным количеством потоков</span><span class="sxs-lookup"><span data-stu-id="729b2-119">Example 3: Download an image by using a specified number of threads</span></span>
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32 -ResourceGroupName "rgname"
```

<span data-ttu-id="729b2-120">Эта команда загружает VHD-файл и сохраняет его в локальном пути.</span><span class="sxs-lookup"><span data-stu-id="729b2-120">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="729b2-121">Команда задает значение 32 для параметра *NumberOfThreads* .</span><span class="sxs-lookup"><span data-stu-id="729b2-121">The command specifies a value of 32 for the *NumberOfThreads* parameter.</span></span>
<span data-ttu-id="729b2-122">Таким образом, командлет использует потоки 32 для этого действия.</span><span class="sxs-lookup"><span data-stu-id="729b2-122">Therefore, the cmdlet uses 32 threads for this action.</span></span>

### <span data-ttu-id="729b2-123">Пример 4: Загрузка изображения и указание ключа хранилища</span><span class="sxs-lookup"><span data-stu-id="729b2-123">Example 4: Download an image and specify the storage key</span></span>
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw==" -ResourceGroupName "rgname"
```

<span data-ttu-id="729b2-124">Эта команда загружает VHD-файл и определяет ключ хранилища.</span><span class="sxs-lookup"><span data-stu-id="729b2-124">This command downloads a .vhd file and specifies the storage key.</span></span>

## <span data-ttu-id="729b2-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="729b2-125">PARAMETERS</span></span>

### <span data-ttu-id="729b2-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="729b2-126">-AsJob</span></span>
<span data-ttu-id="729b2-127">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="729b2-127">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729b2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="729b2-128">-DefaultProfile</span></span>
<span data-ttu-id="729b2-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="729b2-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="729b2-130">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="729b2-130">-LocalFilePath</span></span>
<span data-ttu-id="729b2-131">Указывает путь к локальному файлу сохраненного изображения.</span><span class="sxs-lookup"><span data-stu-id="729b2-131">Specifies the local file path of the saved image.</span></span>

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729b2-132">-NumberOfThreads</span><span class="sxs-lookup"><span data-stu-id="729b2-132">-NumberOfThreads</span></span>
<span data-ttu-id="729b2-133">Указывает количество потоков скачивания, используемых этим командлетом во время скачивания.</span><span class="sxs-lookup"><span data-stu-id="729b2-133">Specifies the number of download threads that this cmdlet uses during download.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729b2-134">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="729b2-134">-OverWrite</span></span>
<span data-ttu-id="729b2-135">Указывает на то, что этот командлет заменяет файл, указанный в файле *LocalFilePath* , если он существует.</span><span class="sxs-lookup"><span data-stu-id="729b2-135">Indicates that this cmdlet replaces the file specified by *LocalFilePath* file if it exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729b2-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="729b2-136">-ResourceGroupName</span></span>
<span data-ttu-id="729b2-137">Указывает имя группы ресурсов для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="729b2-137">Specifies the name of the resource group of the storage account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="729b2-138">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="729b2-138">-SourceUri</span></span>
<span data-ttu-id="729b2-139">Задает универсальный код ресурса (URI) BLOB-объекта в `Azure` .</span><span class="sxs-lookup"><span data-stu-id="729b2-139">Specifies the Uniform Resource Identifier (URI) of the blob in `Azure`.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: src, Source

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="729b2-140">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="729b2-140">-StorageKey</span></span>
<span data-ttu-id="729b2-141">Указывает ключ хранилища для учетной записи хранения BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="729b2-141">Specifies the storage key of the blob storage account.</span></span>
<span data-ttu-id="729b2-142">Если ключ не указан, этот командлет пытается определить ключ хранилища учетной записи в *sourceUri* из Azure.</span><span class="sxs-lookup"><span data-stu-id="729b2-142">If you do not specify a key, this cmdlet attempts to determine the storage key of the account in *SourceUri* from Azure.</span></span>

```yaml
Type: String
Parameter Sets: StorageKeyParameterSetName
Aliases: sk

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729b2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="729b2-143">CommonParameters</span></span>
<span data-ttu-id="729b2-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="729b2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="729b2-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="729b2-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="729b2-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="729b2-146">INPUTS</span></span>

### <span data-ttu-id="729b2-147">Ничего</span><span class="sxs-lookup"><span data-stu-id="729b2-147">None</span></span>
<span data-ttu-id="729b2-148">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="729b2-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="729b2-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="729b2-149">OUTPUTS</span></span>

### <span data-ttu-id="729b2-150">Microsoft. Azure. Commands. COMPUTE. Models. VhdDownloadContext</span><span class="sxs-lookup"><span data-stu-id="729b2-150">Microsoft.Azure.Commands.Compute.Models.VhdDownloadContext</span></span>

## <span data-ttu-id="729b2-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="729b2-151">NOTES</span></span>

## <span data-ttu-id="729b2-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="729b2-152">RELATED LINKS</span></span>

[<span data-ttu-id="729b2-153">Add-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="729b2-153">Add-AzureRmVhd</span></span>](./Add-AzureRMVhd.md)


