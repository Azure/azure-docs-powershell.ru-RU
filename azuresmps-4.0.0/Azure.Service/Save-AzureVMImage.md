---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9A1CE31E-0158-441E-BC2D-B5D21C9D9421
online version: ''
schema: 2.0.0
ms.openlocfilehash: a956aa7eaf383b0cf5cdb20b39d2f6b54e292f92
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075451"
---
# <span data-ttu-id="3740f-101">Save-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="3740f-101">Save-AzureVMImage</span></span>

## <span data-ttu-id="3740f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3740f-102">SYNOPSIS</span></span>
<span data-ttu-id="3740f-103">Захватывает и сохраняет изображение остановленной виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="3740f-103">Captures and saves the image of a stopped Azure virtual machine.</span></span>

## <span data-ttu-id="3740f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3740f-104">SYNTAX</span></span>

```
Save-AzureVMImage [-ServiceName] <String> [-Name] <String> [-ImageName] <String> [[-ImageLabel] <String>]
 [[-OSState] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3740f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3740f-105">DESCRIPTION</span></span>
<span data-ttu-id="3740f-106">Командлет **Save-AzureVMImage** захватывает и сохраняет изображение остановленной виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="3740f-106">The **Save-AzureVMImage** cmdlet captures and saves the image of a stopped Azure virtual machine.</span></span>
<span data-ttu-id="3740f-107">Для виртуальных машин Windows запустите средство Sysprep для подготовки образа перед его засбором.</span><span class="sxs-lookup"><span data-stu-id="3740f-107">For Windows virtual machines, run the Sysprep tool to prepare the image before it is captured.</span></span>
<span data-ttu-id="3740f-108">После того как изображение будет записано, виртуальная машина будет удалена.</span><span class="sxs-lookup"><span data-stu-id="3740f-108">After the image is captured, the virtual machine is deleted.</span></span>

## <span data-ttu-id="3740f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3740f-109">EXAMPLES</span></span>

### <span data-ttu-id="3740f-110">Пример 1: сохранение существующей виртуальной машины и удаление ее из развертывания</span><span class="sxs-lookup"><span data-stu-id="3740f-110">Example 1: Save an existing virtual machine and then delete it from a deployment</span></span>
```
PS C:\> Save-AzureVMImage -ServiceName "MyService" -Name "MyVM" -NewImageName "MyBaseImage" -NewImageLabel "MyBaseVM"
```

<span data-ttu-id="3740f-111">Эта команда перехватывает существующую виртуальную машину и удаляет ее из развертывания.</span><span class="sxs-lookup"><span data-stu-id="3740f-111">This command captures an existing virtual machine and deletes it from the deployment.</span></span>

## <span data-ttu-id="3740f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3740f-112">PARAMETERS</span></span>

### <span data-ttu-id="3740f-113">-ImageLabel</span><span class="sxs-lookup"><span data-stu-id="3740f-113">-ImageLabel</span></span>
<span data-ttu-id="3740f-114">Указывает метку образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3740f-114">Specifies the label of the virtual machine image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewImageLabel

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3740f-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="3740f-115">-ImageName</span></span>
<span data-ttu-id="3740f-116">Указывает имя образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3740f-116">Specifies the name of the virtual machine image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewImageName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3740f-117">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3740f-117">-InformationAction</span></span>
<span data-ttu-id="3740f-118">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="3740f-118">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3740f-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3740f-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3740f-120">Продолжал</span><span class="sxs-lookup"><span data-stu-id="3740f-120">Continue</span></span>
- <span data-ttu-id="3740f-121">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="3740f-121">Ignore</span></span>
- <span data-ttu-id="3740f-122">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="3740f-122">Inquire</span></span>
- <span data-ttu-id="3740f-123">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3740f-123">SilentlyContinue</span></span>
- <span data-ttu-id="3740f-124">Остановить</span><span class="sxs-lookup"><span data-stu-id="3740f-124">Stop</span></span>
- <span data-ttu-id="3740f-125">Рвать</span><span class="sxs-lookup"><span data-stu-id="3740f-125">Suspend</span></span>

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

### <span data-ttu-id="3740f-126">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3740f-126">-InformationVariable</span></span>
<span data-ttu-id="3740f-127">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="3740f-127">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3740f-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3740f-128">-Name</span></span>
<span data-ttu-id="3740f-129">Указывает имя исходной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3740f-129">Specifies the name of the source virtual machine.</span></span>

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

### <span data-ttu-id="3740f-130">-OSState</span><span class="sxs-lookup"><span data-stu-id="3740f-130">-OSState</span></span>
<span data-ttu-id="3740f-131">Задает состояние операционной системы для образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3740f-131">Specifies the operation system state for the virtual machine image.</span></span>
<span data-ttu-id="3740f-132">Используйте этот параметр, если вы собираетесь захватывать образ виртуальной машины в Azure.</span><span class="sxs-lookup"><span data-stu-id="3740f-132">Use this parameter if you intend to capture a virtual machine image to Azure.</span></span>

<span data-ttu-id="3740f-133">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="3740f-133">Valid values are:</span></span>

- <span data-ttu-id="3740f-134">Обобщенного</span><span class="sxs-lookup"><span data-stu-id="3740f-134">Generalized</span></span>
- <span data-ttu-id="3740f-135">Специализированных</span><span class="sxs-lookup"><span data-stu-id="3740f-135">Specialized</span></span>

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

### <span data-ttu-id="3740f-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="3740f-136">-Profile</span></span>
<span data-ttu-id="3740f-137">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3740f-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3740f-138">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3740f-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3740f-139">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3740f-139">-ServiceName</span></span>
<span data-ttu-id="3740f-140">Указывает имя службы Azure.</span><span class="sxs-lookup"><span data-stu-id="3740f-140">Specifies the name of the Azure service.</span></span>

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

### <span data-ttu-id="3740f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3740f-141">CommonParameters</span></span>
<span data-ttu-id="3740f-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3740f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3740f-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3740f-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3740f-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3740f-144">INPUTS</span></span>

## <span data-ttu-id="3740f-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3740f-145">OUTPUTS</span></span>

## <span data-ttu-id="3740f-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="3740f-146">NOTES</span></span>

## <span data-ttu-id="3740f-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3740f-147">RELATED LINKS</span></span>

[<span data-ttu-id="3740f-148">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="3740f-148">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="3740f-149">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="3740f-149">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="3740f-150">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="3740f-150">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="3740f-151">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="3740f-151">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


