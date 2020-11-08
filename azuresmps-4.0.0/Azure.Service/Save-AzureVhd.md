---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E4660D0A-26CB-488C-9A29-3ED94A0DCDA2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e62cb7ed272a5c0d5ff4ff0ecbafe30a0c5ee9e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075461"
---
# <span data-ttu-id="6f550-101">Save-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="6f550-101">Save-AzureVhd</span></span>

## <span data-ttu-id="6f550-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6f550-102">SYNOPSIS</span></span>
<span data-ttu-id="6f550-103">Включает скачивание VHD-изображений.</span><span class="sxs-lookup"><span data-stu-id="6f550-103">Enables download of .vhd images.</span></span>

## <span data-ttu-id="6f550-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6f550-104">SYNTAX</span></span>

```
Save-AzureVhd [-Source] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfThreads] <Int32>] [[-StorageKey] <String>]
 [-OverWrite] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6f550-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f550-105">DESCRIPTION</span></span>
<span data-ttu-id="6f550-106">Командлет **Save-AzureVhd** позволяет загружать файлы VHD из большого двоичного объекта, где они хранятся в файле.</span><span class="sxs-lookup"><span data-stu-id="6f550-106">The **Save-AzureVhd** cmdlet enables download of .vhd images from a blob where they are stored to a file.</span></span>
<span data-ttu-id="6f550-107">У него есть параметры, позволяющие настроить процесс загрузки, указав количество потоков загрузчика, используемых или перезаписанных файлов, которые уже есть в указанном пути к файлу.</span><span class="sxs-lookup"><span data-stu-id="6f550-107">It has parameters to configure the download process by specifying the number of downloader threads that are used or overwriting the file which already exists in the specified file path.</span></span>

<span data-ttu-id="6f550-108">Параметр **Save-AzureVhd** не выполняет преобразование формата виртуального жесткого диска и загружает большой двоичный объект.</span><span class="sxs-lookup"><span data-stu-id="6f550-108">**Save-AzureVhd** does not do any VHD format conversion and the blob is downloaded as it is.</span></span>

## <span data-ttu-id="6f550-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6f550-109">EXAMPLES</span></span>

### <span data-ttu-id="6f550-110">Пример 1: загрузка VHD-файла</span><span class="sxs-lookup"><span data-stu-id="6f550-110">Example 1: Download a VHD file</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="6f550-111">Эта команда загружает VHD-файл.</span><span class="sxs-lookup"><span data-stu-id="6f550-111">This command downloads a .vhd file.</span></span>

### <span data-ttu-id="6f550-112">Пример 2: Загрузка файла виртуального жесткого диска и перезапись локального файла</span><span class="sxs-lookup"><span data-stu-id="6f550-112">Example 2: Download a VHD file and overwrite the local file</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="6f550-113">Эта команда загружает VHD-файл и перезаписывает любой файл в конечном пути.</span><span class="sxs-lookup"><span data-stu-id="6f550-113">This command downloads a .vhd file and overwrites any file in the destination path.</span></span>

### <span data-ttu-id="6f550-114">Пример 3: Загрузка файла виртуального жесткого диска и указание количества потоков</span><span class="sxs-lookup"><span data-stu-id="6f550-114">Example 3: Download a VHD file and specify the number of threads</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

<span data-ttu-id="6f550-115">Эта команда загружает VHD-файл и определяет количество потоков.</span><span class="sxs-lookup"><span data-stu-id="6f550-115">This command downloads a .vhd file and specifies the number of threads.</span></span>

### <span data-ttu-id="6f550-116">Пример 4: Загрузка файла виртуального жесткого диска и указание ключа хранилища</span><span class="sxs-lookup"><span data-stu-id="6f550-116">Example 4: Download a VHD file and specify the storage key</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw=="
```

<span data-ttu-id="6f550-117">Эта команда загружает VHD-файл и определяет ключ хранилища.</span><span class="sxs-lookup"><span data-stu-id="6f550-117">This command downloads a .vhd file and specifies the storage key.</span></span>

## <span data-ttu-id="6f550-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6f550-118">PARAMETERS</span></span>

### <span data-ttu-id="6f550-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6f550-119">-InformationAction</span></span>
<span data-ttu-id="6f550-120">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="6f550-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6f550-121">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6f550-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6f550-122">Продолжал</span><span class="sxs-lookup"><span data-stu-id="6f550-122">Continue</span></span>
- <span data-ttu-id="6f550-123">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="6f550-123">Ignore</span></span>
- <span data-ttu-id="6f550-124">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="6f550-124">Inquire</span></span>
- <span data-ttu-id="6f550-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6f550-125">SilentlyContinue</span></span>
- <span data-ttu-id="6f550-126">Остановить</span><span class="sxs-lookup"><span data-stu-id="6f550-126">Stop</span></span>
- <span data-ttu-id="6f550-127">Рвать</span><span class="sxs-lookup"><span data-stu-id="6f550-127">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f550-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6f550-128">-InformationVariable</span></span>
<span data-ttu-id="6f550-129">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="6f550-129">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f550-130">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="6f550-130">-LocalFilePath</span></span>
<span data-ttu-id="6f550-131">Указывает путь к локальному файлу.</span><span class="sxs-lookup"><span data-stu-id="6f550-131">Specifies the local file path.</span></span>

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

### <span data-ttu-id="6f550-132">-NumberOfThreads</span><span class="sxs-lookup"><span data-stu-id="6f550-132">-NumberOfThreads</span></span>
<span data-ttu-id="6f550-133">Указывает количество потоков скачивания, используемых этим командлетом во время скачивания.</span><span class="sxs-lookup"><span data-stu-id="6f550-133">Specifies the number of download threads that this cmdlet uses during download.</span></span>

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

### <span data-ttu-id="6f550-134">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="6f550-134">-OverWrite</span></span>
<span data-ttu-id="6f550-135">Указывает на то, что этот командлет удаляет файл, указанный в файле *LocalFilePath* , если он существует.</span><span class="sxs-lookup"><span data-stu-id="6f550-135">Specifies that this cmdlet deletes the file specified by *LocalFilePath* file if it exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f550-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="6f550-136">-Profile</span></span>
<span data-ttu-id="6f550-137">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6f550-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6f550-138">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6f550-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f550-139">-Source (источник)</span><span class="sxs-lookup"><span data-stu-id="6f550-139">-Source</span></span>
<span data-ttu-id="6f550-140">Задает универсальный код ресурса (URI) для BLOB-объекта `Azure` .</span><span class="sxs-lookup"><span data-stu-id="6f550-140">Specifies the Uniform Resource Identifier (URI) to the blob in `Azure`.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: src

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f550-141">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="6f550-141">-StorageKey</span></span>
<span data-ttu-id="6f550-142">Указывает ключ хранилища для учетной записи хранения BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="6f550-142">Specifies the storage key of the blob storage account.</span></span>
<span data-ttu-id="6f550-143">Если он не предоставлен, **AzureVhd** пытается определить ключ хранения учетной записи в *sourceUri* из Azure.</span><span class="sxs-lookup"><span data-stu-id="6f550-143">If it is not provided, **Save-AzureVhd** attempts to determine the storage key of the account in *SourceUri* from Azure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: sk

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f550-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f550-144">CommonParameters</span></span>
<span data-ttu-id="6f550-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6f550-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f550-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f550-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f550-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6f550-147">INPUTS</span></span>

## <span data-ttu-id="6f550-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f550-148">OUTPUTS</span></span>

## <span data-ttu-id="6f550-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="6f550-149">NOTES</span></span>

## <span data-ttu-id="6f550-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f550-150">RELATED LINKS</span></span>

[<span data-ttu-id="6f550-151">Add-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="6f550-151">Add-AzureVhd</span></span>](./Add-AzureVhd.md)


