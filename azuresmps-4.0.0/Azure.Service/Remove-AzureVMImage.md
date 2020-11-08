---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C9470E5-21D2-4AF5-9F11-F66F94B133C0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23f4511f8e0439c1581cc388843a37266092f4d0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076454"
---
# <span data-ttu-id="fa0d7-101">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="fa0d7-101">Remove-AzureVMImage</span></span>

## <span data-ttu-id="fa0d7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fa0d7-102">SYNOPSIS</span></span>
<span data-ttu-id="fa0d7-103">Удаляет образ операционной системы из репозитория изображений.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-103">Removes an operating system image from the image repository.</span></span>

## <span data-ttu-id="fa0d7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fa0d7-104">SYNTAX</span></span>

```
Remove-AzureVMImage [-ImageName] <String> [-DeleteVHD] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fa0d7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa0d7-105">DESCRIPTION</span></span>
<span data-ttu-id="fa0d7-106">Командлет **Remove-AzureVMImage** удаляет образ операционной системы из репозитория изображений.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-106">The **Remove-AzureVMImage** cmdlet removes an operating system image from the image repository.</span></span>
<span data-ttu-id="fa0d7-107">По умолчанию этот командлет не удаляет связанный большой двоичный объект физического изображения из учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-107">By default, this cmdlet does not delete the associated physical image blob from the storage account.</span></span>
<span data-ttu-id="fa0d7-108">Чтобы удалить связанный виртуальный жесткий диск (VHD), используйте параметр **DeleteVHD** .</span><span class="sxs-lookup"><span data-stu-id="fa0d7-108">To delete the associated virtual hard drive (VHD), use the **DeleteVHD** parameter.</span></span>

## <span data-ttu-id="fa0d7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fa0d7-109">EXAMPLES</span></span>

### <span data-ttu-id="fa0d7-110">Пример 1: удаление изображения из репозитория изображений</span><span class="sxs-lookup"><span data-stu-id="fa0d7-110">Example 1: Remove an image from the image repository</span></span>
```
PS C:\> Remove-AzureVMImage -ImageName "Image001"
```

<span data-ttu-id="fa0d7-111">Эта команда удаляет изображение с именем Image001 из репозитория изображений.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-111">This command removes the image named Image001 from the image repository.</span></span>

### <span data-ttu-id="fa0d7-112">Пример 2: удаление изображения из репозитория изображений, а также виртуального жесткого диска</span><span class="sxs-lookup"><span data-stu-id="fa0d7-112">Example 2: Remove an image from the image repository and also the VHD</span></span>
```
PS C:\> Remove-AzureVMImage -ImageName " Image001" -DeleteVHD
```

<span data-ttu-id="fa0d7-113">Эта команда удаляет изображение с именем Image001 из репозитория изображений, а также физический образ VHD из учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-113">This command removes the image named Image001 from the image repository and also deletes the physical VHD image from the storage account.</span></span>

### <span data-ttu-id="fa0d7-114">Пример 3: Настройка контекста подписки и удаление всех изображений</span><span class="sxs-lookup"><span data-stu-id="fa0d7-114">Example 3: Set a subscription context and then remove all the images</span></span>
```
PS C:\> $SubsId = &amp;lt;MySubscriptionID&amp;gt;
PS C:\> $Cert = Get-AzureCertificate cert:\LocalMachine\MY\&amp;lt;CertificateThumbprint&amp;gt;
PS C:\> Get-AzureVMImage `
| Where-Object {$_.Label -match "Beta" }`
| Foreach-Object {Remove-AzureVMImage -ImageName $_.name }
```

<span data-ttu-id="fa0d7-115">Эта команда задает контекст подписки, а затем удаляет все изображения из репозитория изображений, метка которого содержит имя Beta.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-115">This command sets the subscription context and then removes all the images from the image repository whose Label includes the name Beta.</span></span>

## <span data-ttu-id="fa0d7-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fa0d7-116">PARAMETERS</span></span>

### <span data-ttu-id="fa0d7-117">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="fa0d7-117">-DeleteVHD</span></span>
<span data-ttu-id="fa0d7-118">Указывает, что этот командлет удаляет большой двоичный объект физического образа VHD из учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-118">Indicates that this cmdlet deletes the physical VHD image blob from the storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa0d7-119">-ImageName</span><span class="sxs-lookup"><span data-stu-id="fa0d7-119">-ImageName</span></span>
<span data-ttu-id="fa0d7-120">Указывает операционную систему или образ виртуальной машины, которые нужно удалить из репозитория изображений.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-120">Specifies the operating system or virtual machine image to remove from the image repository.</span></span>

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

### <span data-ttu-id="fa0d7-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="fa0d7-121">-InformationAction</span></span>
<span data-ttu-id="fa0d7-122">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fa0d7-123">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fa0d7-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fa0d7-124">Продолжал</span><span class="sxs-lookup"><span data-stu-id="fa0d7-124">Continue</span></span>
- <span data-ttu-id="fa0d7-125">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="fa0d7-125">Ignore</span></span>
- <span data-ttu-id="fa0d7-126">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="fa0d7-126">Inquire</span></span>
- <span data-ttu-id="fa0d7-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fa0d7-127">SilentlyContinue</span></span>
- <span data-ttu-id="fa0d7-128">Остановить</span><span class="sxs-lookup"><span data-stu-id="fa0d7-128">Stop</span></span>
- <span data-ttu-id="fa0d7-129">Рвать</span><span class="sxs-lookup"><span data-stu-id="fa0d7-129">Suspend</span></span>

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

### <span data-ttu-id="fa0d7-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fa0d7-130">-InformationVariable</span></span>
<span data-ttu-id="fa0d7-131">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fa0d7-132">-Profile</span><span class="sxs-lookup"><span data-stu-id="fa0d7-132">-Profile</span></span>
<span data-ttu-id="fa0d7-133">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fa0d7-134">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fa0d7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa0d7-135">CommonParameters</span></span>
<span data-ttu-id="fa0d7-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fa0d7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa0d7-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa0d7-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa0d7-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fa0d7-138">INPUTS</span></span>

## <span data-ttu-id="fa0d7-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa0d7-139">OUTPUTS</span></span>

## <span data-ttu-id="fa0d7-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="fa0d7-140">NOTES</span></span>

## <span data-ttu-id="fa0d7-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fa0d7-141">RELATED LINKS</span></span>

[<span data-ttu-id="fa0d7-142">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="fa0d7-142">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="fa0d7-143">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="fa0d7-143">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="fa0d7-144">Сохранить — AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="fa0d7-144">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="fa0d7-145">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="fa0d7-145">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


