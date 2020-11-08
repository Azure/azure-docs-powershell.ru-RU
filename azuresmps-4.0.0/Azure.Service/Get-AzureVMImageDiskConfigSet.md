---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: ACBE32E5-AA8C-43CA-9FF4-4B59906C6B85
online version: ''
schema: 2.0.0
ms.openlocfilehash: 45d18179fba41d39456a11575fc2041ad4be8557
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076530"
---
# <span data-ttu-id="8fe90-101">Get-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="8fe90-101">Get-AzureVMImageDiskConfigSet</span></span>

## <span data-ttu-id="8fe90-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8fe90-102">SYNOPSIS</span></span>
<span data-ttu-id="8fe90-103">Получает объект набор конфигураций диска из контекста входного изображения.</span><span class="sxs-lookup"><span data-stu-id="8fe90-103">Gets a disk configuration set object from the input image context.</span></span>

## <span data-ttu-id="8fe90-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8fe90-104">SYNTAX</span></span>

```
Get-AzureVMImageDiskConfigSet [[-ImageContext] <OSImageContext>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8fe90-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8fe90-105">DESCRIPTION</span></span>
<span data-ttu-id="8fe90-106">Командлет **Get-AzureVMImageDiskConfigSet** получает объект набор конфигураций диска из контекста входного изображения.</span><span class="sxs-lookup"><span data-stu-id="8fe90-106">The **Get-AzureVMImageDiskConfigSet** cmdlet gets a disk configuration set object from the input image context.</span></span>

## <span data-ttu-id="8fe90-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8fe90-107">EXAMPLES</span></span>

### <span data-ttu-id="8fe90-108">Пример 1: получение объекта набором конфигурации диска для виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="8fe90-108">Example 1: Get a disk configuration set object from a virtual machine</span></span>
```
PS C:\> Get-AzureVMImage -ImageName $Img | Get-AzureVMImageDiskConfigSet
```

<span data-ttu-id="8fe90-109">Эта команда получает объект набор конфигураций диска из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8fe90-109">This command gets a disk configuration set object from a virtual machine.</span></span>

## <span data-ttu-id="8fe90-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8fe90-110">PARAMETERS</span></span>

### <span data-ttu-id="8fe90-111">-ImageContext</span><span class="sxs-lookup"><span data-stu-id="8fe90-111">-ImageContext</span></span>
<span data-ttu-id="8fe90-112">Указывает контекст образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8fe90-112">Specifies the virtual machine image context.</span></span>

```yaml
Type: OSImageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe90-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8fe90-113">-InformationAction</span></span>
<span data-ttu-id="8fe90-114">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="8fe90-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8fe90-115">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="8fe90-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8fe90-116">Продолжал</span><span class="sxs-lookup"><span data-stu-id="8fe90-116">Continue</span></span>
- <span data-ttu-id="8fe90-117">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="8fe90-117">Ignore</span></span>
- <span data-ttu-id="8fe90-118">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="8fe90-118">Inquire</span></span>
- <span data-ttu-id="8fe90-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8fe90-119">SilentlyContinue</span></span>
- <span data-ttu-id="8fe90-120">Остановить</span><span class="sxs-lookup"><span data-stu-id="8fe90-120">Stop</span></span>
- <span data-ttu-id="8fe90-121">Рвать</span><span class="sxs-lookup"><span data-stu-id="8fe90-121">Suspend</span></span>

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

### <span data-ttu-id="8fe90-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8fe90-122">-InformationVariable</span></span>
<span data-ttu-id="8fe90-123">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="8fe90-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8fe90-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fe90-124">CommonParameters</span></span>
<span data-ttu-id="8fe90-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8fe90-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fe90-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fe90-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fe90-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8fe90-127">INPUTS</span></span>

## <span data-ttu-id="8fe90-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8fe90-128">OUTPUTS</span></span>

### <span data-ttu-id="8fe90-129">Microsoft. WindowsAzure. Commands. ServiceManagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="8fe90-129">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="8fe90-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="8fe90-130">NOTES</span></span>

## <span data-ttu-id="8fe90-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8fe90-131">RELATED LINKS</span></span>

[<span data-ttu-id="8fe90-132">New-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="8fe90-132">New-AzureVMImageDiskConfigSet</span></span>](./New-AzureVMImageDiskConfigSet.md)

[<span data-ttu-id="8fe90-133">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="8fe90-133">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)


