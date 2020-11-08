---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 99DC239C-EA68-4830-9345-762CD6A3F68C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 320b95add2806f48121151a71bdf36a572fa05a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075718"
---
# <span data-ttu-id="c9cdc-101">Add-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="c9cdc-101">Add-AzureVhd</span></span>

## <span data-ttu-id="c9cdc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c9cdc-102">SYNOPSIS</span></span>
<span data-ttu-id="c9cdc-103">Передает VHD-файл с локального компьютера на большой двоичный объект в учетной записи облачного хранилища в Azure.</span><span class="sxs-lookup"><span data-stu-id="c9cdc-103">Uploads a VHD file from an on-premise computer to a blob in a cloud storage account in Azure.</span></span>

## <span data-ttu-id="c9cdc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c9cdc-104">SYNTAX</span></span>

```
Add-AzureVhd [-Destination] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfUploaderThreads] <Int32>]
 [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c9cdc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9cdc-105">DESCRIPTION</span></span>
<span data-ttu-id="c9cdc-106">Командлет **Add-AzureVhd** отправляет образы локальных виртуальных жестких дисков (VHD) в учетную запись хранения BLOB-файлов в формате fixed. VHD.</span><span class="sxs-lookup"><span data-stu-id="c9cdc-106">The **Add-AzureVhd** cmdlet uploads on premise Virtual hard disk (VHD) images to a blob storage account as fixed .vhd images.</span></span>
<span data-ttu-id="c9cdc-107">У него есть параметры, позволяющие настроить процесс отправки, например указать количество потоков отправки, которые будут использоваться или перезаписывая большой двоичный объект, уже существующий в указанном URI назначения.</span><span class="sxs-lookup"><span data-stu-id="c9cdc-107">It has parameters to configure the upload process such as specifying the number of uploader threads that will be used or overwriting a blob which already exists in the specified destination URI.</span></span>
<span data-ttu-id="c9cdc-108">Для локальных образов VHD также поддерживается сценарий исправлений, так что образы дисков различий можно отправить, не открывая уже загруженные базовые образы.</span><span class="sxs-lookup"><span data-stu-id="c9cdc-108">For on premise VHD images, patching scenario is also supported so that diff disk images can be uploaded without having to upload the already uploaded base images.</span></span> <span data-ttu-id="c9cdc-109">Также поддерживается URI-адрес подписи общего доступа (SAS).</span><span class="sxs-lookup"><span data-stu-id="c9cdc-109">Shared Access Signature (SAS) URI is also supported.</span></span>

## <span data-ttu-id="c9cdc-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c9cdc-110">EXAMPLES</span></span>

### <span data-ttu-id="c9cdc-111">Пример 1: Добавление VHD-файла</span><span class="sxs-lookup"><span data-stu-id="c9cdc-111">Example 1: Add a VHD file</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="c9cdc-112">Эта команда добавляет VHD-файл в учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="c9cdc-112">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="c9cdc-113">Пример 2: Добавление файла виртуального жесткого диска и переопределение места назначения</span><span class="sxs-lookup"><span data-stu-id="c9cdc-113">Example 2: Add a VHD file and overwrite the destination</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="c9cdc-114">Эта команда добавляет VHD-файл в учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="c9cdc-114">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="c9cdc-115">Пример 3: Добавление файла виртуального жесткого диска и указание количества потоков</span><span class="sxs-lookup"><span data-stu-id="c9cdc-115">Example 3: Add a VHD file and specify the number of threads</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

<span data-ttu-id="c9cdc-116">Эта команда добавляет VHD-файл в учетную запись хранения и определяет количество потоков, используемых для отправки файла.</span><span class="sxs-lookup"><span data-stu-id="c9cdc-116">This command adds a .vhd file to a storage account and specifies the number of threads to use to upload the file.</span></span>

### <span data-ttu-id="c9cdc-117">Пример 4: Добавление файла виртуального жесткого диска и указание URI SAS</span><span class="sxs-lookup"><span data-stu-id="c9cdc-117">Example 4: Add a VHD file and specify the SAS URI</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01-09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveOSIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

<span data-ttu-id="c9cdc-118">Эта команда добавляет VHD-файл в учетную запись хранения и определяет универсальный код ресурса (URI) SAS.</span><span class="sxs-lookup"><span data-stu-id="c9cdc-118">This command adds a .vhd file to a storage account and specifies the SAS URI.</span></span>

## <span data-ttu-id="c9cdc-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c9cdc-119">PARAMETERS</span></span>

### <span data-ttu-id="c9cdc-120">-BaseImageUriToPatch</span><span class="sxs-lookup"><span data-stu-id="c9cdc-120">-BaseImageUriToPatch</span></span>
<span data-ttu-id="c9cdc-121">Задает универсальный код ресурса (URI) базового объекта Image в хранилище BLOB-объектов Azure.</span><span class="sxs-lookup"><span data-stu-id="c9cdc-121">Specifies an URI to a base image blob in Azure Blob Storage.</span></span>
<span data-ttu-id="c9cdc-122">SAS также поддерживается и в входных данных URI.</span><span class="sxs-lookup"><span data-stu-id="c9cdc-122">SAS in URI input is supported as well.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: bs

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9cdc-123">-Destination</span><span class="sxs-lookup"><span data-stu-id="c9cdc-123">-Destination</span></span>
<span data-ttu-id="c9cdc-124">Задает универсальный код ресурса (BLOB) в хранилище BLOB-объектов Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c9cdc-124">Specifies a URI to a blob in Microsoft Azure Blob Storage.</span></span>
<span data-ttu-id="c9cdc-125">В входных данных URI поддерживается сопоставление безопасности.</span><span class="sxs-lookup"><span data-stu-id="c9cdc-125">SAS in URI input is supported.</span></span>
<span data-ttu-id="c9cdc-126">Однако в сценариях исправления назначение не может быть URI SAS.</span><span class="sxs-lookup"><span data-stu-id="c9cdc-126">However, in patching scenarios the destination cannot be a SAS URI.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: dst

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9cdc-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c9cdc-127">-InformationAction</span></span>
<span data-ttu-id="c9cdc-128">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="c9cdc-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c9cdc-129">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c9cdc-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c9cdc-130">Продолжал</span><span class="sxs-lookup"><span data-stu-id="c9cdc-130">Continue</span></span>
- <span data-ttu-id="c9cdc-131">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="c9cdc-131">Ignore</span></span>
- <span data-ttu-id="c9cdc-132">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="c9cdc-132">Inquire</span></span>
- <span data-ttu-id="c9cdc-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c9cdc-133">SilentlyContinue</span></span>
- <span data-ttu-id="c9cdc-134">Остановить</span><span class="sxs-lookup"><span data-stu-id="c9cdc-134">Stop</span></span>
- <span data-ttu-id="c9cdc-135">Рвать</span><span class="sxs-lookup"><span data-stu-id="c9cdc-135">Suspend</span></span>

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

### <span data-ttu-id="c9cdc-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c9cdc-136">-InformationVariable</span></span>
<span data-ttu-id="c9cdc-137">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="c9cdc-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c9cdc-138">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="c9cdc-138">-LocalFilePath</span></span>
<span data-ttu-id="c9cdc-139">Форель путь к файлу для локального VHD-файла.</span><span class="sxs-lookup"><span data-stu-id="c9cdc-139">Species the file path of the local .vhd file.</span></span>

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9cdc-140">-NumberOfUploaderThreads</span><span class="sxs-lookup"><span data-stu-id="c9cdc-140">-NumberOfUploaderThreads</span></span>
<span data-ttu-id="c9cdc-141">Указывает количество потоков, используемых для отправки.</span><span class="sxs-lookup"><span data-stu-id="c9cdc-141">Specifies the number of threads to use for upload.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9cdc-142">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="c9cdc-142">-OverWrite</span></span>
<span data-ttu-id="c9cdc-143">Указывает на то, что этот командлет удаляет существующий большой двоичный объект в указанном URI назначения, если он существует.</span><span class="sxs-lookup"><span data-stu-id="c9cdc-143">Specifies that this cmdlet deletes the existing blob in the specified destination URI if it exists.</span></span>

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

### <span data-ttu-id="c9cdc-144">-Profile</span><span class="sxs-lookup"><span data-stu-id="c9cdc-144">-Profile</span></span>
<span data-ttu-id="c9cdc-145">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c9cdc-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c9cdc-146">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c9cdc-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c9cdc-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9cdc-147">CommonParameters</span></span>
<span data-ttu-id="c9cdc-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c9cdc-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9cdc-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9cdc-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9cdc-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c9cdc-150">INPUTS</span></span>

## <span data-ttu-id="c9cdc-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9cdc-151">OUTPUTS</span></span>

## <span data-ttu-id="c9cdc-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="c9cdc-152">NOTES</span></span>

## <span data-ttu-id="c9cdc-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c9cdc-153">RELATED LINKS</span></span>

[<span data-ttu-id="c9cdc-154">Сохранить — AzureVhd</span><span class="sxs-lookup"><span data-stu-id="c9cdc-154">Save-AzureVhd</span></span>](./Save-AzureVhd.md)


