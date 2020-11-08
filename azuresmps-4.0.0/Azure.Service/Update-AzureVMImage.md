---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5544F2E2-27EF-4079-8E13-6B85DF2018A2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a71ad8b25a17c1c2933cdcf305ba0b53f67bf0f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076583"
---
# <span data-ttu-id="f3382-101">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="f3382-101">Update-AzureVMImage</span></span>

## <span data-ttu-id="f3382-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f3382-102">SYNOPSIS</span></span>
<span data-ttu-id="f3382-103">Обновляет метку образа операционной системы в репозитории изображений.</span><span class="sxs-lookup"><span data-stu-id="f3382-103">Updates the label of an operating system image in the image repository.</span></span>

## <span data-ttu-id="f3382-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f3382-104">SYNTAX</span></span>

```
Update-AzureVMImage [-ImageName] <String> [-Label] <String> [[-Eula] <String>] [[-Description] <String>]
 [[-ImageFamily] <String>] [[-PublishedDate] <DateTime>] [[-PrivacyUri] <Uri>] [[-RecommendedVMSize] <String>]
 [[-DiskConfig] <VirtualMachineImageDiskConfigSet>] [[-Language] <String>] [[-IconName] <String>]
 [[-SmallIconName] <String>] [-DontShowInGui] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f3382-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3382-105">DESCRIPTION</span></span>
<span data-ttu-id="f3382-106">Командлет **Update-AzureVMImage** обновляет метку на образе операционной системы в репозитории изображений.</span><span class="sxs-lookup"><span data-stu-id="f3382-106">The **Update-AzureVMImage** cmdlet updates the label on an operating system image in the image repository.</span></span>
<span data-ttu-id="f3382-107">Функция возвращает объект Image со сведениями об обновленном изображении.</span><span class="sxs-lookup"><span data-stu-id="f3382-107">It returns an image object with information about the updated image.</span></span>

## <span data-ttu-id="f3382-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f3382-108">EXAMPLES</span></span>

### <span data-ttu-id="f3382-109">Пример 1: обновление изображения путем изменения метки изображения</span><span class="sxs-lookup"><span data-stu-id="f3382-109">Example 1: Update an image by changing the image label</span></span>
```
PS C:\> Update-AzureVMImage -ImageName "Windows-Server-2008-SP2" -Label "DoNotUse"
```

<span data-ttu-id="f3382-110">Эта команда обновляет образ с именем Windows-Server-2008-SP2, изменяя метку изображения на DoNotUse.</span><span class="sxs-lookup"><span data-stu-id="f3382-110">This command updates the image named Windows-Server-2008-SP2 by changing the image label to DoNotUse.</span></span>

### <span data-ttu-id="f3382-111">Пример 2: получение всех операционных систем по метке, а затем обновление метки</span><span class="sxs-lookup"><span data-stu-id="f3382-111">Example 2: Get all operating systems by label and then update the label</span></span>
```
PS C:\> Get-AzureVMImage | Where-Object {$_.Label -eq "DoNotUse" } | Update-AzureVMImage -Label "Updated"
```

<span data-ttu-id="f3382-112">Эта команда получает все образы операционной системы с меткой DoNotUse и изменяет метку на "Обновлено".</span><span class="sxs-lookup"><span data-stu-id="f3382-112">This command gets all the operating system images labeled DoNotUse and changes the label to Updated.</span></span>

## <span data-ttu-id="f3382-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f3382-113">PARAMETERS</span></span>

### <span data-ttu-id="f3382-114">-Описание</span><span class="sxs-lookup"><span data-stu-id="f3382-114">-Description</span></span>
<span data-ttu-id="f3382-115">Задает описание образа операционной системы.</span><span class="sxs-lookup"><span data-stu-id="f3382-115">Specifies the description of the operating system image.</span></span>

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

### <span data-ttu-id="f3382-116">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="f3382-116">-DiskConfig</span></span>
<span data-ttu-id="f3382-117">Задает диск операционной системы и конфигурацию диска данных для образа виртуальной машины, созданного с помощью командлетов **New-AzureVMImageDiskConfigSet** , **Set-AzureVMImageOSDiskConfig** и **Set-AzureVMImageDataDiskConfig** .</span><span class="sxs-lookup"><span data-stu-id="f3382-117">Specifies the operating system disk and data disk configuration for the virtual machine image created by using the **New-AzureVMImageDiskConfigSet** , **Set-AzureVMImageOSDiskConfig** , and **Set-AzureVMImageDataDiskConfig** cmdlets.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3382-118">-DontShowInGui</span><span class="sxs-lookup"><span data-stu-id="f3382-118">-DontShowInGui</span></span>
<span data-ttu-id="f3382-119">Указывает на то, что этот командлет не показывает изображение в графическом интерфейсе пользователя.</span><span class="sxs-lookup"><span data-stu-id="f3382-119">Indicates that this cmdlet does not show the image in the GUI.</span></span>

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

### <span data-ttu-id="f3382-120">-EULA</span><span class="sxs-lookup"><span data-stu-id="f3382-120">-Eula</span></span>
<span data-ttu-id="f3382-121">Задает лицензионное соглашение конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="f3382-121">Specifies the End User License Agreement.</span></span>
<span data-ttu-id="f3382-122">Рекомендуется, чтобы значение было URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="f3382-122">We recommend that the value is a URL.</span></span>

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

### <span data-ttu-id="f3382-123">-IconName</span><span class="sxs-lookup"><span data-stu-id="f3382-123">-IconName</span></span>
<span data-ttu-id="f3382-124">Указывает стандартное имя значка для образа операционной системы или виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f3382-124">Specifies the standard icon name for the operating system or virtual machine image.</span></span>

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

### <span data-ttu-id="f3382-125">-ImageFamily</span><span class="sxs-lookup"><span data-stu-id="f3382-125">-ImageFamily</span></span>
<span data-ttu-id="f3382-126">Указывает значение, которое можно использовать для группирования образов операционной системы или виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="f3382-126">Specifies a value that can be used to group operating system or virtual machine images.</span></span>

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

### <span data-ttu-id="f3382-127">-ImageName</span><span class="sxs-lookup"><span data-stu-id="f3382-127">-ImageName</span></span>
<span data-ttu-id="f3382-128">Указывает имя обновляемого изображения в репозитории изображений.</span><span class="sxs-lookup"><span data-stu-id="f3382-128">Specifies the name of the image to update in the image repository.</span></span>

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

### <span data-ttu-id="f3382-129">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f3382-129">-InformationAction</span></span>
<span data-ttu-id="f3382-130">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="f3382-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f3382-131">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f3382-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f3382-132">Продолжал</span><span class="sxs-lookup"><span data-stu-id="f3382-132">Continue</span></span>
- <span data-ttu-id="f3382-133">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="f3382-133">Ignore</span></span>
- <span data-ttu-id="f3382-134">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="f3382-134">Inquire</span></span>
- <span data-ttu-id="f3382-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f3382-135">SilentlyContinue</span></span>
- <span data-ttu-id="f3382-136">Остановить</span><span class="sxs-lookup"><span data-stu-id="f3382-136">Stop</span></span>
- <span data-ttu-id="f3382-137">Рвать</span><span class="sxs-lookup"><span data-stu-id="f3382-137">Suspend</span></span>

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

### <span data-ttu-id="f3382-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f3382-138">-InformationVariable</span></span>
<span data-ttu-id="f3382-139">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="f3382-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f3382-140">-Label</span><span class="sxs-lookup"><span data-stu-id="f3382-140">-Label</span></span>
<span data-ttu-id="f3382-141">Задает новую метку изображения.</span><span class="sxs-lookup"><span data-stu-id="f3382-141">Specifies the new label of the image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3382-142">-Language</span><span class="sxs-lookup"><span data-stu-id="f3382-142">-Language</span></span>
<span data-ttu-id="f3382-143">Указывает язык операционной системы в образе виртуальной машины или операционной системы.</span><span class="sxs-lookup"><span data-stu-id="f3382-143">Specifies the language for the operating system in the virtual machine or operating system image.</span></span>

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

### <span data-ttu-id="f3382-144">-PrivacyUri</span><span class="sxs-lookup"><span data-stu-id="f3382-144">-PrivacyUri</span></span>
<span data-ttu-id="f3382-145">Указывает URI, указывающий на документ, который содержит политику конфиденциальности, относящуюся к образу операционной системы.</span><span class="sxs-lookup"><span data-stu-id="f3382-145">Specifies the URI that points to a document that contains the privacy policy related to the operating system image.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3382-146">-Profile</span><span class="sxs-lookup"><span data-stu-id="f3382-146">-Profile</span></span>
<span data-ttu-id="f3382-147">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f3382-147">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f3382-148">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f3382-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f3382-149">-PublishedDate</span><span class="sxs-lookup"><span data-stu-id="f3382-149">-PublishedDate</span></span>
<span data-ttu-id="f3382-150">Указывает дату добавления образа операционной системы в репозиторий изображений.</span><span class="sxs-lookup"><span data-stu-id="f3382-150">Specifies the date when the operating system image was added to the image repository.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3382-151">-RecommendedVMSize</span><span class="sxs-lookup"><span data-stu-id="f3382-151">-RecommendedVMSize</span></span>
<span data-ttu-id="f3382-152">Задает размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f3382-152">Specifies the size of the virtual machine.</span></span>

<span data-ttu-id="f3382-153">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f3382-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f3382-154">Канал</span><span class="sxs-lookup"><span data-stu-id="f3382-154">Medium</span></span>
- <span data-ttu-id="f3382-155">Достаточ</span><span class="sxs-lookup"><span data-stu-id="f3382-155">Large</span></span>
- <span data-ttu-id="f3382-156">ExtraLarge</span><span class="sxs-lookup"><span data-stu-id="f3382-156">ExtraLarge</span></span>
- <span data-ttu-id="f3382-157">Ячейк</span><span class="sxs-lookup"><span data-stu-id="f3382-157">A5</span></span>
- <span data-ttu-id="f3382-158">A6</span><span class="sxs-lookup"><span data-stu-id="f3382-158">A6</span></span>
- <span data-ttu-id="f3382-159">Ответ</span><span class="sxs-lookup"><span data-stu-id="f3382-159">A7</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3382-160">-SmallIconName</span><span class="sxs-lookup"><span data-stu-id="f3382-160">-SmallIconName</span></span>
<span data-ttu-id="f3382-161">Задает маленький значок имени для операционной системы или образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f3382-161">Specifies the small icon name for the operating system or virtual machine image.</span></span>

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

### <span data-ttu-id="f3382-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3382-162">CommonParameters</span></span>
<span data-ttu-id="f3382-163">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f3382-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3382-164">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3382-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3382-165">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f3382-165">INPUTS</span></span>

## <span data-ttu-id="f3382-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3382-166">OUTPUTS</span></span>

### <span data-ttu-id="f3382-167">OSImageContext</span><span class="sxs-lookup"><span data-stu-id="f3382-167">OSImageContext</span></span>

## <span data-ttu-id="f3382-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="f3382-168">NOTES</span></span>

## <span data-ttu-id="f3382-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3382-169">RELATED LINKS</span></span>

[<span data-ttu-id="f3382-170">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="f3382-170">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="f3382-171">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="f3382-171">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="f3382-172">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="f3382-172">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="f3382-173">Сохранить — AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="f3382-173">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="f3382-174">New-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="f3382-174">New-AzureVMImageDiskConfigSet</span></span>](./New-AzureVMImageDiskConfigSet.md)

[<span data-ttu-id="f3382-175">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="f3382-175">Set-AzureVMImageOSDiskConfig</span></span>](./Set-AzureVMImageOSDiskConfig.md)

[<span data-ttu-id="f3382-176">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="f3382-176">Set-AzureVMImageDataDiskConfig</span></span>](./Set-AzureVMImageDataDiskConfig.md)


