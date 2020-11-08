---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 02DECCEE-86C8-4662-9ED0-D1BDB4E687C2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 68efd1c750646abffa90eb8318d0df189a4c9eb9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075715"
---
# <span data-ttu-id="5ff57-101">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="5ff57-101">Add-AzureVMImage</span></span>

## <span data-ttu-id="5ff57-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5ff57-102">SYNOPSIS</span></span>
<span data-ttu-id="5ff57-103">Добавление нового образа операционной системы или нового образа виртуальной машины в репозиторий изображений.</span><span class="sxs-lookup"><span data-stu-id="5ff57-103">Adds a new operating system image or a new virtual machine image to the image repository.</span></span>

## <span data-ttu-id="5ff57-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5ff57-104">SYNTAX</span></span>

### <span data-ttu-id="5ff57-105">OSImage (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5ff57-105">OSImage (Default)</span></span>
```
Add-AzureVMImage [-ImageName] <String> [-MediaLocation] <String> [-OS] <String> [[-Label] <String>]
 [[-Eula] <String>] [[-Description] <String>] [[-ImageFamily] <String>] [[-PublishedDate] <DateTime>]
 [[-PrivacyUri] <Uri>] [[-RecommendedVMSize] <String>] [[-IconName] <String>] [[-SmallIconName] <String>]
 [-ShowInGui] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5ff57-106">VMImage</span><span class="sxs-lookup"><span data-stu-id="5ff57-106">VMImage</span></span>
```
Add-AzureVMImage [-ImageName] <String> [-DiskConfig] <VirtualMachineImageDiskConfigSet> [[-OS] <String>]
 [[-Label] <String>] [[-Eula] <String>] [[-Description] <String>] [[-ImageFamily] <String>]
 [[-PublishedDate] <DateTime>] [[-PrivacyUri] <Uri>] [[-RecommendedVMSize] <String>] [[-IconName] <String>]
 [[-SmallIconName] <String>] [-ShowInGui] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5ff57-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ff57-107">DESCRIPTION</span></span>
<span data-ttu-id="5ff57-108">Командлет **Add-AzureVMImage** добавляет новый образ операционной системы или новый образ виртуальной машины в репозиторий образов.</span><span class="sxs-lookup"><span data-stu-id="5ff57-108">The **Add-AzureVMImage** cmdlet adds a new operating system image or a new virtual machine image to the image repository.</span></span>
<span data-ttu-id="5ff57-109">Изображение — это обобщенный образ операционной системы с помощью программы Sysprep для Windows или (для Linux) с использованием соответствующего средства для распространения.</span><span class="sxs-lookup"><span data-stu-id="5ff57-109">The image is a generalized operating system image, using either Sysprep for Windows or, for Linux, using the appropriate tool for the distribution.</span></span>

## <span data-ttu-id="5ff57-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5ff57-110">EXAMPLES</span></span>

### <span data-ttu-id="5ff57-111">Пример 1: Добавление образа операционной системы в репозиторий</span><span class="sxs-lookup"><span data-stu-id="5ff57-111">Example 1: Add an operating system image to the repository</span></span>
```
PS C:\> $S = New-AzureVMImageDiskConfigSet
PS C:\> Set-AzureVMImageOSDiskConfig -DiskConfig $S -HostCaching ReadWrite -OSState "Generalized" -OS "Windows" -MediaLink $Link
PS C:\> Set-AzureVMImageDataDiskConfig -DiskConfig $S -DataDiskName "Test1" -HostCaching ReadWrite -Lun 0 -MediaLink $Link1
PS C:\> Set-AzureVMImageDataDiskConfig -DiskConfig $S -DataDiskName "Test4" -HostCaching ReadWrite -Lun 0 -MediaLink $Link
PS C:\> Remove-AzureVMImageDataDiskConfig -DiskConfig $S -DataDiskName "Test4"
PS C:\> $IMGName = "TestCREATEvmimage2";
PS C:\> Add-AzureVMImage -ImageName $IMGName -Label "Test1" -Description "Test1" -DiskConfig $S -Eula "http://www.contoso.com" -ImageFamily Windows -PublishedDate (Get-Date) -PrivacyUri "http://www.test.com" -RecommendedVMSize Small -IconName "Icon01" -SmallIconName "SmallIcon01" -ShowInGui
```

<span data-ttu-id="5ff57-112">В этом примере в репозиторий добавляется образ операционной системы.</span><span class="sxs-lookup"><span data-stu-id="5ff57-112">This example adds an operating system image to the repository.</span></span>

## <span data-ttu-id="5ff57-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5ff57-113">PARAMETERS</span></span>

### <span data-ttu-id="5ff57-114">-Описание</span><span class="sxs-lookup"><span data-stu-id="5ff57-114">-Description</span></span>
<span data-ttu-id="5ff57-115">Задает описание образа операционной системы.</span><span class="sxs-lookup"><span data-stu-id="5ff57-115">Specifies the description of the operating system image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ff57-116">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="5ff57-116">-DiskConfig</span></span>
<span data-ttu-id="5ff57-117">Указывает конфигурацию диска операционной системы для образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5ff57-117">Specifies the operating system disk configuration for the virtual machine image.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: VMImage
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ff57-118">-EULA</span><span class="sxs-lookup"><span data-stu-id="5ff57-118">-Eula</span></span>
<span data-ttu-id="5ff57-119">Задает лицензионное соглашение конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="5ff57-119">Specifies the End User License Agreement.</span></span>
<span data-ttu-id="5ff57-120">Рекомендуется использовать URL-адрес для этого значения.</span><span class="sxs-lookup"><span data-stu-id="5ff57-120">It is recommended that you use an URL for this value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ff57-121">-IconName</span><span class="sxs-lookup"><span data-stu-id="5ff57-121">-IconName</span></span>
<span data-ttu-id="5ff57-122">Указывает имя значка, который используется при добавлении изображения в репозиторий.</span><span class="sxs-lookup"><span data-stu-id="5ff57-122">Specifies the name of the icon that is used when the image is added to the repository.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IconUri

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ff57-123">-ImageFamily</span><span class="sxs-lookup"><span data-stu-id="5ff57-123">-ImageFamily</span></span>
<span data-ttu-id="5ff57-124">Указывает значение, используемое для группировки изображений операционной системы.</span><span class="sxs-lookup"><span data-stu-id="5ff57-124">Specifies a value that is used to group operating system images.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ff57-125">-ImageName</span><span class="sxs-lookup"><span data-stu-id="5ff57-125">-ImageName</span></span>
<span data-ttu-id="5ff57-126">Указывает имя изображения, добавляемого в репозиторий изображений.</span><span class="sxs-lookup"><span data-stu-id="5ff57-126">Specifies the name of the image being added to the image repository.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ff57-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5ff57-127">-InformationAction</span></span>
<span data-ttu-id="5ff57-128">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="5ff57-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5ff57-129">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5ff57-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5ff57-130">Продолжал</span><span class="sxs-lookup"><span data-stu-id="5ff57-130">Continue</span></span>
- <span data-ttu-id="5ff57-131">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="5ff57-131">Ignore</span></span>
- <span data-ttu-id="5ff57-132">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="5ff57-132">Inquire</span></span>
- <span data-ttu-id="5ff57-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5ff57-133">SilentlyContinue</span></span>
- <span data-ttu-id="5ff57-134">Остановить</span><span class="sxs-lookup"><span data-stu-id="5ff57-134">Stop</span></span>
- <span data-ttu-id="5ff57-135">Рвать</span><span class="sxs-lookup"><span data-stu-id="5ff57-135">Suspend</span></span>

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

### <span data-ttu-id="5ff57-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5ff57-136">-InformationVariable</span></span>
<span data-ttu-id="5ff57-137">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="5ff57-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5ff57-138">-Label</span><span class="sxs-lookup"><span data-stu-id="5ff57-138">-Label</span></span>
<span data-ttu-id="5ff57-139">Указывает метку для присвоения изображения.</span><span class="sxs-lookup"><span data-stu-id="5ff57-139">Specifies a label to give the image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ff57-140">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="5ff57-140">-MediaLocation</span></span>
<span data-ttu-id="5ff57-141">Задает расположение страницы физического большого двоичного объекта, в которой находится изображение.</span><span class="sxs-lookup"><span data-stu-id="5ff57-141">Specifies the location of the physical blob page where the image resides.</span></span>
<span data-ttu-id="5ff57-142">Это ссылка на страницу больших двоичных объектов в хранилище текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="5ff57-142">This is a link to a blob page in the current subscription's storage.</span></span>

```yaml
Type: String
Parameter Sets: OSImage
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ff57-143">-OS</span><span class="sxs-lookup"><span data-stu-id="5ff57-143">-OS</span></span>
<span data-ttu-id="5ff57-144">Задает версию операционной системы для образа.</span><span class="sxs-lookup"><span data-stu-id="5ff57-144">Specifies the operating system version of the image.</span></span>

```yaml
Type: String
Parameter Sets: OSImage
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: VMImage
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ff57-145">-PrivacyUri</span><span class="sxs-lookup"><span data-stu-id="5ff57-145">-PrivacyUri</span></span>
<span data-ttu-id="5ff57-146">Указывает URL-адрес, указывающий на документ, который содержит политику конфиденциальности, относящуюся к образу операционной системы.</span><span class="sxs-lookup"><span data-stu-id="5ff57-146">Specifies the URL that points to a document that contains the privacy policy related to the operating system image.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ff57-147">-Profile</span><span class="sxs-lookup"><span data-stu-id="5ff57-147">-Profile</span></span>
<span data-ttu-id="5ff57-148">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5ff57-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5ff57-149">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5ff57-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5ff57-150">-PublishedDate</span><span class="sxs-lookup"><span data-stu-id="5ff57-150">-PublishedDate</span></span>
<span data-ttu-id="5ff57-151">Указывает дату добавления образа операционной системы в репозиторий изображений.</span><span class="sxs-lookup"><span data-stu-id="5ff57-151">Specifies the date when the operating system image was added to the image repository.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ff57-152">-RecommendedVMSize</span><span class="sxs-lookup"><span data-stu-id="5ff57-152">-RecommendedVMSize</span></span>
<span data-ttu-id="5ff57-153">Задает размер виртуальной машины, созданной из образа операционной системы.</span><span class="sxs-lookup"><span data-stu-id="5ff57-153">Specifies the size to use for the virtual machine that is created from the operating system image.</span></span>

<span data-ttu-id="5ff57-154">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5ff57-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5ff57-155">Канал</span><span class="sxs-lookup"><span data-stu-id="5ff57-155">Medium</span></span>
- <span data-ttu-id="5ff57-156">Достаточ</span><span class="sxs-lookup"><span data-stu-id="5ff57-156">Large</span></span>
- <span data-ttu-id="5ff57-157">ExtraLarge</span><span class="sxs-lookup"><span data-stu-id="5ff57-157">ExtraLarge</span></span>
- <span data-ttu-id="5ff57-158">Ячейк</span><span class="sxs-lookup"><span data-stu-id="5ff57-158">A5</span></span>
- <span data-ttu-id="5ff57-159">A6</span><span class="sxs-lookup"><span data-stu-id="5ff57-159">A6</span></span>
- <span data-ttu-id="5ff57-160">Ответ</span><span class="sxs-lookup"><span data-stu-id="5ff57-160">A7</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ff57-161">-ShowInGui</span><span class="sxs-lookup"><span data-stu-id="5ff57-161">-ShowInGui</span></span>
<span data-ttu-id="5ff57-162">Указывает на то, что этот командлет показывает изображение в графическом интерфейсе пользователя.</span><span class="sxs-lookup"><span data-stu-id="5ff57-162">Indicates that this cmdlet shows the image in the GUI.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ff57-163">-SmallIconName</span><span class="sxs-lookup"><span data-stu-id="5ff57-163">-SmallIconName</span></span>
<span data-ttu-id="5ff57-164">Указывает имя маленького значка, который используется при добавлении изображения в репозиторий.</span><span class="sxs-lookup"><span data-stu-id="5ff57-164">Specifies the name of the small icon that is used when the image is added to the repository.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SmallIconUri

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ff57-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ff57-165">CommonParameters</span></span>
<span data-ttu-id="5ff57-166">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5ff57-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ff57-167">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ff57-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ff57-168">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5ff57-168">INPUTS</span></span>

## <span data-ttu-id="5ff57-169">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ff57-169">OUTPUTS</span></span>

### <span data-ttu-id="5ff57-170">OSImageContext</span><span class="sxs-lookup"><span data-stu-id="5ff57-170">OSImageContext</span></span>

## <span data-ttu-id="5ff57-171">Пуск</span><span class="sxs-lookup"><span data-stu-id="5ff57-171">NOTES</span></span>

## <span data-ttu-id="5ff57-172">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ff57-172">RELATED LINKS</span></span>

[<span data-ttu-id="5ff57-173">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="5ff57-173">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="5ff57-174">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="5ff57-174">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="5ff57-175">Сохранить — AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="5ff57-175">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="5ff57-176">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="5ff57-176">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


