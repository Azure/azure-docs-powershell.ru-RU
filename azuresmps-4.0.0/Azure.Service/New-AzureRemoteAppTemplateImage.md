---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DBC4A0B8-A34A-47AC-930B-EFE23A95A216
online version: ''
schema: 2.0.0
ms.openlocfilehash: 178349299767eefb1d89c31a0199f53373bd2ae2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075995"
---
# <span data-ttu-id="ddc7e-101">New-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="ddc7e-101">New-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="ddc7e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ddc7e-102">SYNOPSIS</span></span>
<span data-ttu-id="ddc7e-103">Отправляет или импортирует образ шаблона Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="ddc7e-103">Uploads or imports an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="ddc7e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ddc7e-104">SYNTAX</span></span>

### <span data-ttu-id="ddc7e-105">UploadLocalVhd (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ddc7e-105">UploadLocalVhd (Default)</span></span>
```
New-AzureRemoteAppTemplateImage [-ImageName] <String> [-Location] <String> [-Path] <String> [-Resume]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ddc7e-106">AzureVmUpload</span><span class="sxs-lookup"><span data-stu-id="ddc7e-106">AzureVmUpload</span></span>
```
New-AzureRemoteAppTemplateImage [-ImageName] <String> [-Location] <String> -AzureVmImageName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ddc7e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddc7e-107">DESCRIPTION</span></span>
<span data-ttu-id="ddc7e-108">Командлет **New-AzureRemoteAppTemplateImage** отправляет или импортирует изображение шаблона Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="ddc7e-108">The **New-AzureRemoteAppTemplateImage** cmdlet uploads or imports an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="ddc7e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ddc7e-109">EXAMPLES</span></span>

### <span data-ttu-id="ddc7e-110">Пример 1: отправка VHD-файла для создания образа шаблона</span><span class="sxs-lookup"><span data-stu-id="ddc7e-110">Example 1: Upload a VHD file to create a template image</span></span>
```
PS C:\> New-AzureRemoteAppTemplateImage -ImageName "ContosoApps" -Location "North Europe" -Path "C:\RemoteAppImages\ContosoApps.vhd"
```

<span data-ttu-id="ddc7e-111">Эта команда отправляет C:\RemoteAppImages\ContosoApps.vhd, чтобы создать образ шаблона с именем ContosoApps в центре обработки данных в Северной Европе.</span><span class="sxs-lookup"><span data-stu-id="ddc7e-111">This command uploads C:\RemoteAppImages\ContosoApps.vhd to create a template image named ContosoApps in the North Europe data center.</span></span>

## <span data-ttu-id="ddc7e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ddc7e-112">PARAMETERS</span></span>

### <span data-ttu-id="ddc7e-113">-AzureVmImageName</span><span class="sxs-lookup"><span data-stu-id="ddc7e-113">-AzureVmImageName</span></span>
<span data-ttu-id="ddc7e-114">Указывает имя виртуальной машины Azure, используемой в качестве изображения шаблона.</span><span class="sxs-lookup"><span data-stu-id="ddc7e-114">Specifies the name of an Azure virtual machine to use as a template image.</span></span>

```yaml
Type: String
Parameter Sets: AzureVmUpload
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddc7e-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="ddc7e-115">-ImageName</span></span>
<span data-ttu-id="ddc7e-116">Указывает имя образа шаблона Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="ddc7e-116">Specifies the name of an Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ddc7e-117">-Location</span><span class="sxs-lookup"><span data-stu-id="ddc7e-117">-Location</span></span>
<span data-ttu-id="ddc7e-118">Указывает регион Azure для образа шаблона.</span><span class="sxs-lookup"><span data-stu-id="ddc7e-118">Specifies the Azure region of the template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddc7e-119">-Path</span><span class="sxs-lookup"><span data-stu-id="ddc7e-119">-Path</span></span>
<span data-ttu-id="ddc7e-120">Задает путь к файлу изображения шаблона.</span><span class="sxs-lookup"><span data-stu-id="ddc7e-120">Specifies the file path of the template image.</span></span>

```yaml
Type: String
Parameter Sets: UploadLocalVhd
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddc7e-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="ddc7e-121">-Profile</span></span>
<span data-ttu-id="ddc7e-122">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ddc7e-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ddc7e-123">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ddc7e-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ddc7e-124">-Резюме</span><span class="sxs-lookup"><span data-stu-id="ddc7e-124">-Resume</span></span>
<span data-ttu-id="ddc7e-125">Указывает на то, что этот командлет продолжит работу, если отправка изображения шаблона прерывается.</span><span class="sxs-lookup"><span data-stu-id="ddc7e-125">Indicates that this cmdlet resumes if the upload of a template image is interrupted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UploadLocalVhd
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc7e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddc7e-126">CommonParameters</span></span>
<span data-ttu-id="ddc7e-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ddc7e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddc7e-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddc7e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddc7e-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ddc7e-129">INPUTS</span></span>

## <span data-ttu-id="ddc7e-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddc7e-130">OUTPUTS</span></span>

## <span data-ttu-id="ddc7e-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="ddc7e-131">NOTES</span></span>

## <span data-ttu-id="ddc7e-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ddc7e-132">RELATED LINKS</span></span>

[<span data-ttu-id="ddc7e-133">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="ddc7e-133">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="ddc7e-134">Remove-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="ddc7e-134">Remove-AzureRemoteAppTemplateImage</span></span>](./Remove-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="ddc7e-135">Rename-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="ddc7e-135">Rename-AzureRemoteAppTemplateImage</span></span>](./Rename-AzureRemoteAppTemplateImage.md)


