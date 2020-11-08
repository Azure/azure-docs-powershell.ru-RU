---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F420A47F-D036-4B31-AA59-97CFC9C79E75
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a53d0821832b29f0f1f6a0b2ab5f1353e3331a3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076198"
---
# <span data-ttu-id="b34e8-101">New-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="b34e8-101">New-AzureVMImageDiskConfigSet</span></span>

## <span data-ttu-id="b34e8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b34e8-102">SYNOPSIS</span></span>
<span data-ttu-id="b34e8-103">Создание объекта набор конфигураций диска.</span><span class="sxs-lookup"><span data-stu-id="b34e8-103">Creates a disk configuration set object.</span></span>

## <span data-ttu-id="b34e8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b34e8-104">SYNTAX</span></span>

```
New-AzureVMImageDiskConfigSet [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="b34e8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b34e8-105">DESCRIPTION</span></span>
<span data-ttu-id="b34e8-106">Командлет **New-AzureVMImageDiskConfigSet** создает объект набор конфигураций диска, передаваемый командлету обновления изображений.</span><span class="sxs-lookup"><span data-stu-id="b34e8-106">The **New-AzureVMImageDiskConfigSet** cmdlet creates a disk configuration set object that is passed to the image update cmdlet.</span></span>
<span data-ttu-id="b34e8-107">Он инкапсулирует объект OSDiskConfig и DataDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="b34e8-107">It encapsulates the OSDiskConfig and the DataDiskConfig object.</span></span>
<span data-ttu-id="b34e8-108">Используйте командлеты **Set-AzureVMImageOSDiskConfig** и **Set-AzureVMImageDataDiskConfig** для задания свойств диска операционной системы и диска данных для образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b34e8-108">Use the **Set-AzureVMImageOSDiskConfig** and **Set-AzureVMImageDataDiskConfig** cmdlets to set the OS Disk and Data Disk properties for the virtual machine image.</span></span>

## <span data-ttu-id="b34e8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b34e8-109">EXAMPLES</span></span>

### <span data-ttu-id="b34e8-110">Пример 1: создание объекта "набор конфигурации диска"</span><span class="sxs-lookup"><span data-stu-id="b34e8-110">Example 1: Create a disk configuration set object</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

<span data-ttu-id="b34e8-111">Эта команда создает объект набор конфигураций диска и сохраняет результаты в переменной с именем $Disk.</span><span class="sxs-lookup"><span data-stu-id="b34e8-111">This command creates a disk configuration set object and stores the results in the variable named $Disk.</span></span>
<span data-ttu-id="b34e8-112">После создания конфигурации диска она используется для установки OSDiskConfig и DataDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="b34e8-112">After the disk configuration is created, it is used to set the OSDiskConfig and DataDiskConfig.</span></span>
<span data-ttu-id="b34e8-113">После этого виртуальная машина будет обновлена с учетом конфигурации.</span><span class="sxs-lookup"><span data-stu-id="b34e8-113">Then the virtual machine is updated with the configuration.</span></span>

## <span data-ttu-id="b34e8-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b34e8-114">PARAMETERS</span></span>

### <span data-ttu-id="b34e8-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b34e8-115">-InformationAction</span></span>
<span data-ttu-id="b34e8-116">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="b34e8-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b34e8-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b34e8-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b34e8-118">Продолжал</span><span class="sxs-lookup"><span data-stu-id="b34e8-118">Continue</span></span>
- <span data-ttu-id="b34e8-119">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="b34e8-119">Ignore</span></span>
- <span data-ttu-id="b34e8-120">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="b34e8-120">Inquire</span></span>
- <span data-ttu-id="b34e8-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b34e8-121">SilentlyContinue</span></span>
- <span data-ttu-id="b34e8-122">Остановить</span><span class="sxs-lookup"><span data-stu-id="b34e8-122">Stop</span></span>
- <span data-ttu-id="b34e8-123">Рвать</span><span class="sxs-lookup"><span data-stu-id="b34e8-123">Suspend</span></span>

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

### <span data-ttu-id="b34e8-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b34e8-124">-InformationVariable</span></span>
<span data-ttu-id="b34e8-125">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="b34e8-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b34e8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b34e8-126">CommonParameters</span></span>
<span data-ttu-id="b34e8-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b34e8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b34e8-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b34e8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b34e8-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b34e8-129">INPUTS</span></span>

## <span data-ttu-id="b34e8-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b34e8-130">OUTPUTS</span></span>

### <span data-ttu-id="b34e8-131">Microsoft. WindowsAzure. Commands. ServiceManagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="b34e8-131">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="b34e8-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="b34e8-132">NOTES</span></span>

## <span data-ttu-id="b34e8-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b34e8-133">RELATED LINKS</span></span>

[<span data-ttu-id="b34e8-134">Get-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="b34e8-134">Get-AzureVMImageDiskConfigSet</span></span>](./Get-AzureVMImageDiskConfigSet.md)

[<span data-ttu-id="b34e8-135">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="b34e8-135">Set-AzureVMImageOSDiskConfig</span></span>](./Set-AzureVMImageOSDiskConfig.md)

[<span data-ttu-id="b34e8-136">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="b34e8-136">Set-AzureVMImageDataDiskConfig</span></span>](./Set-AzureVMImageDataDiskConfig.md)


