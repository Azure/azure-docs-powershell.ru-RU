---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E712421A-FA69-46E7-A0DE-F2734D767F2D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8355e0a1d36a6c1dc5b2ca8172cde5bf94480bbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076532"
---
# <span data-ttu-id="6ec79-101">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="6ec79-101">Get-AzureVMImage</span></span>

## <span data-ttu-id="6ec79-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6ec79-102">SYNOPSIS</span></span>
<span data-ttu-id="6ec79-103">Получает свойства одного или списка операционных систем или образа виртуальной машины в репозитории изображений.</span><span class="sxs-lookup"><span data-stu-id="6ec79-103">Gets the properties on one or a list of operating systems or a virtual machine image in the image repository.</span></span>

## <span data-ttu-id="6ec79-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6ec79-104">SYNTAX</span></span>

```
Get-AzureVMImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6ec79-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ec79-105">DESCRIPTION</span></span>
<span data-ttu-id="6ec79-106">Командлет **Get-AzureVMImage** получает свойства одного или списка операционных систем или образа виртуальной машины в репозитории изображений.</span><span class="sxs-lookup"><span data-stu-id="6ec79-106">The **Get-AzureVMImage** cmdlet gets properties on one or a list of operating systems or a virtual machine image in the image repository.</span></span>
<span data-ttu-id="6ec79-107">Командлет возвращает сведения обо всех изображениях в репозитории или об определенном изображении, если оно указано.</span><span class="sxs-lookup"><span data-stu-id="6ec79-107">The cmdlet returns information for all images in the repository, or about a specific image if its image name is provided.</span></span>

## <span data-ttu-id="6ec79-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6ec79-108">EXAMPLES</span></span>

### <span data-ttu-id="6ec79-109">Пример 1: получение определенного объекта изображения из текущего репозитория изображений.</span><span class="sxs-lookup"><span data-stu-id="6ec79-109">Example 1: Get a specific image object from the current image repository.</span></span>
```
PS C:\> Get-AzureVMImage -ImageName Image001
```

<span data-ttu-id="6ec79-110">Эта команда получает объект Image с именем Image001 из текущего репозитория изображений.</span><span class="sxs-lookup"><span data-stu-id="6ec79-110">This command gets the image object named Image001 from the current image repository.</span></span>

### <span data-ttu-id="6ec79-111">Пример 2: получение всех изображений из текущего репозитория изображений</span><span class="sxs-lookup"><span data-stu-id="6ec79-111">Example 2: Get all images from the current image repository</span></span>
```
PS C:\> Get-AzureVMImage
```

<span data-ttu-id="6ec79-112">Эта команда извлекает все изображения из текущего репозитория изображений.</span><span class="sxs-lookup"><span data-stu-id="6ec79-112">This command retrieves all the images from the current image repository.</span></span>

### <span data-ttu-id="6ec79-113">Пример 3: Настройка контекста подписки, а затем получение всех изображений</span><span class="sxs-lookup"><span data-stu-id="6ec79-113">Example 3: Set the subscription context and then get all the images</span></span>
```
PS C:\> $SubsId = <MySubscriptionID>
C:\PS>$Cert = Get-AzureCertificate cert:\LocalMachine\MY\<CertificateThumbprint>
C:\PS>$MyOSImages = Get-AzureVMImage
```

<span data-ttu-id="6ec79-114">Эта команда задает контекст подписки, а затем извлекает все изображения из репозитория изображений.</span><span class="sxs-lookup"><span data-stu-id="6ec79-114">This command sets the subscription context and then retrieves all the images from the image repository.</span></span>

## <span data-ttu-id="6ec79-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6ec79-115">PARAMETERS</span></span>

### <span data-ttu-id="6ec79-116">-ImageName</span><span class="sxs-lookup"><span data-stu-id="6ec79-116">-ImageName</span></span>
<span data-ttu-id="6ec79-117">Указывает имя операционной системы или образа виртуальной машины в репозитории изображений.</span><span class="sxs-lookup"><span data-stu-id="6ec79-117">Specifies the name of the operating system or virtual machine image in the image repository.</span></span>
<span data-ttu-id="6ec79-118">Если этот параметр не указан, возвращаются все изображения.</span><span class="sxs-lookup"><span data-stu-id="6ec79-118">If you do not specify this parameter, all the images are returned.</span></span>

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

### <span data-ttu-id="6ec79-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6ec79-119">-InformationAction</span></span>
<span data-ttu-id="6ec79-120">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="6ec79-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6ec79-121">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6ec79-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6ec79-122">Продолжал</span><span class="sxs-lookup"><span data-stu-id="6ec79-122">Continue</span></span>
- <span data-ttu-id="6ec79-123">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="6ec79-123">Ignore</span></span>
- <span data-ttu-id="6ec79-124">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="6ec79-124">Inquire</span></span>
- <span data-ttu-id="6ec79-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6ec79-125">SilentlyContinue</span></span>
- <span data-ttu-id="6ec79-126">Остановить</span><span class="sxs-lookup"><span data-stu-id="6ec79-126">Stop</span></span>
- <span data-ttu-id="6ec79-127">Рвать</span><span class="sxs-lookup"><span data-stu-id="6ec79-127">Suspend</span></span>

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

### <span data-ttu-id="6ec79-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6ec79-128">-InformationVariable</span></span>
<span data-ttu-id="6ec79-129">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="6ec79-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6ec79-130">-Profile</span><span class="sxs-lookup"><span data-stu-id="6ec79-130">-Profile</span></span>
<span data-ttu-id="6ec79-131">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6ec79-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6ec79-132">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6ec79-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6ec79-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ec79-133">CommonParameters</span></span>
<span data-ttu-id="6ec79-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6ec79-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ec79-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ec79-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ec79-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6ec79-136">INPUTS</span></span>

## <span data-ttu-id="6ec79-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ec79-137">OUTPUTS</span></span>

## <span data-ttu-id="6ec79-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="6ec79-138">NOTES</span></span>

## <span data-ttu-id="6ec79-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6ec79-139">RELATED LINKS</span></span>

[<span data-ttu-id="6ec79-140">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="6ec79-140">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="6ec79-141">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="6ec79-141">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="6ec79-142">Сохранить — AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="6ec79-142">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="6ec79-143">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="6ec79-143">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


