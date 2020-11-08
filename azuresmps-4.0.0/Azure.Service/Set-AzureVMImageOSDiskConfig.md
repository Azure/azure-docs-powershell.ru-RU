---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9CD39F1C-D858-4275-A6DE-10901DC962FE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4cb2557b411d46ce718f97ba7939efb4571ce025
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075444"
---
# <span data-ttu-id="bc835-101">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="bc835-101">Set-AzureVMImageOSDiskConfig</span></span>

## <span data-ttu-id="bc835-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bc835-102">SYNOPSIS</span></span>
<span data-ttu-id="bc835-103">Задает свойства диска операционной системы для образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bc835-103">Sets the operating system disk properties on a virtual machine image.</span></span>

## <span data-ttu-id="bc835-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bc835-104">SYNTAX</span></span>

### <span data-ttu-id="bc835-105">UpdateAzureVMImageParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bc835-105">UpdateAzureVMImageParamSet (Default)</span></span>
```
Set-AzureVMImageOSDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [[-HostCaching] <String>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="bc835-106">AddAzureVMImageParamSet</span><span class="sxs-lookup"><span data-stu-id="bc835-106">AddAzureVMImageParamSet</span></span>
```
Set-AzureVMImageOSDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [[-HostCaching] <String>]
 [-MediaLink] <Uri> [-OSState] <String> [-OS] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="bc835-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc835-107">DESCRIPTION</span></span>
<span data-ttu-id="bc835-108">Командлет **Set-AzureVMImageOSDiskConfig** задает свойства диска операционной системы для образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bc835-108">The **Set-AzureVMImageOSDiskConfig** cmdlet sets the operating system disk properties on a virtual machine image.</span></span>

## <span data-ttu-id="bc835-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bc835-109">EXAMPLES</span></span>

### <span data-ttu-id="bc835-110">Пример 1: Настройка свойств диска операционной системы для образа виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="bc835-110">Example 1: Set the operating system disk properties on a virtual machine image</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

<span data-ttu-id="bc835-111">В этом примере задаются свойства диска операционной системы для образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bc835-111">This example sets the operating system disk properties on a virtual machine image.</span></span>

## <span data-ttu-id="bc835-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bc835-112">PARAMETERS</span></span>

### <span data-ttu-id="bc835-113">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="bc835-113">-DiskConfig</span></span>
<span data-ttu-id="bc835-114">Указывает объект конфигурации диска, который инкапсулирует объекты операционной системы и дискового диска данных.</span><span class="sxs-lookup"><span data-stu-id="bc835-114">Specifies the disk configuration object that encapsulates the operating system disk and Data Disk objects.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc835-115">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="bc835-115">-HostCaching</span></span>
<span data-ttu-id="bc835-116">Задает атрибут кэша узла для диска с операционной системой.</span><span class="sxs-lookup"><span data-stu-id="bc835-116">Specifies the host cache attribute for the operating system disk.</span></span>

<span data-ttu-id="bc835-117">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="bc835-117">Valid values are:</span></span>

<span data-ttu-id="bc835-118">-ReadOnly — ReadWrite</span><span class="sxs-lookup"><span data-stu-id="bc835-118">--ReadOnly --ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc835-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="bc835-119">-InformationAction</span></span>
<span data-ttu-id="bc835-120">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="bc835-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="bc835-121">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="bc835-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bc835-122">Продолжал</span><span class="sxs-lookup"><span data-stu-id="bc835-122">Continue</span></span>
- <span data-ttu-id="bc835-123">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="bc835-123">Ignore</span></span>
- <span data-ttu-id="bc835-124">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="bc835-124">Inquire</span></span>
- <span data-ttu-id="bc835-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="bc835-125">SilentlyContinue</span></span>
- <span data-ttu-id="bc835-126">Остановить</span><span class="sxs-lookup"><span data-stu-id="bc835-126">Stop</span></span>
- <span data-ttu-id="bc835-127">Рвать</span><span class="sxs-lookup"><span data-stu-id="bc835-127">Suspend</span></span>

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

### <span data-ttu-id="bc835-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="bc835-128">-InformationVariable</span></span>
<span data-ttu-id="bc835-129">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="bc835-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="bc835-130">-MediaLink</span><span class="sxs-lookup"><span data-stu-id="bc835-130">-MediaLink</span></span>
<span data-ttu-id="bc835-131">Задает универсальный код ресурса (URI) места, где создается новый виртуальный жесткий диск при добавлении нового диска с данными.</span><span class="sxs-lookup"><span data-stu-id="bc835-131">Specifies the URI of the location where the new virtual hard drive is created when the new data disk is added.</span></span>

```yaml
Type: Uri
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc835-132">-OS</span><span class="sxs-lookup"><span data-stu-id="bc835-132">-OS</span></span>
<span data-ttu-id="bc835-133">Задает операционную систему для конфигурации диска.</span><span class="sxs-lookup"><span data-stu-id="bc835-133">Specifies the operating system of the disk configuration.</span></span>

<span data-ttu-id="bc835-134">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="bc835-134">Valid values are:</span></span>

- <span data-ttu-id="bc835-135">Windows</span><span class="sxs-lookup"><span data-stu-id="bc835-135">Windows</span></span>
- <span data-ttu-id="bc835-136">Linux</span><span class="sxs-lookup"><span data-stu-id="bc835-136">Linux</span></span>

```yaml
Type: String
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc835-137">-OSState</span><span class="sxs-lookup"><span data-stu-id="bc835-137">-OSState</span></span>
<span data-ttu-id="bc835-138">Задает состояние операционной системы для образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bc835-138">Specifies the operating system state for virtual machine image</span></span>

<span data-ttu-id="bc835-139">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="bc835-139">Valid values are:</span></span>

- <span data-ttu-id="bc835-140">Обобщенного</span><span class="sxs-lookup"><span data-stu-id="bc835-140">Generalized</span></span>
- <span data-ttu-id="bc835-141">Специализированных</span><span class="sxs-lookup"><span data-stu-id="bc835-141">Specialized</span></span>

<span data-ttu-id="bc835-142">Использование этого параметра указывает на то, что вы собираетесь записать образ виртуальной машины в Azure.</span><span class="sxs-lookup"><span data-stu-id="bc835-142">The use of this parameter indicates your intent to capture the virtual machine image to Azure.</span></span>

```yaml
Type: String
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc835-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc835-143">CommonParameters</span></span>
<span data-ttu-id="bc835-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bc835-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc835-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc835-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc835-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bc835-146">INPUTS</span></span>

## <span data-ttu-id="bc835-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc835-147">OUTPUTS</span></span>

### <span data-ttu-id="bc835-148">Microsoft. WindowsAzure. Commands. ServiceManagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="bc835-148">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="bc835-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="bc835-149">NOTES</span></span>

## <span data-ttu-id="bc835-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc835-150">RELATED LINKS</span></span>

[<span data-ttu-id="bc835-151">Remove-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="bc835-151">Remove-AzureVMImageOSDiskConfig</span></span>](./Remove-AzureVMImageOSDiskConfig.md)


