---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6C7CB0AE-C788-4E6F-AD48-E30B547A2269
online version: ''
schema: 2.0.0
ms.openlocfilehash: a7512ef446227742c2a3564c5f3e5f38f1e2ccce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075436"
---
# <span data-ttu-id="d0fc0-101">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="d0fc0-101">Set-AzureVMImageDataDiskConfig</span></span>

## <span data-ttu-id="d0fc0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d0fc0-102">SYNOPSIS</span></span>
<span data-ttu-id="d0fc0-103">Задает свойства диска данных для образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d0fc0-103">Sets the Data Disk properties on the virtual machine image.</span></span>

## <span data-ttu-id="d0fc0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d0fc0-104">SYNTAX</span></span>

### <span data-ttu-id="d0fc0-105">UpdateAzureVMImageParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d0fc0-105">UpdateAzureVMImageParamSet (Default)</span></span>
```
Set-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-DataDiskName] <String>
 [-Lun] <Int32> [-HostCaching] <String> [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="d0fc0-106">AddAzureVMImageParamSet</span><span class="sxs-lookup"><span data-stu-id="d0fc0-106">AddAzureVMImageParamSet</span></span>
```
Set-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-Lun] <Int32>
 [-HostCaching] <String> [-MediaLink] <Uri> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d0fc0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0fc0-107">DESCRIPTION</span></span>
<span data-ttu-id="d0fc0-108">Командлет **Set-AzureVMImageDataDiskConfig** задает свойства диска данных в образе виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d0fc0-108">The **Set-AzureVMImageDataDiskConfig** cmdlet sets the Data Disk properties on the virtual machine image.</span></span>

## <span data-ttu-id="d0fc0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d0fc0-109">EXAMPLES</span></span>

### <span data-ttu-id="d0fc0-110">Пример 1: Настройка свойств диска для данных в образе виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="d0fc0-110">Example 1: Set Data Disk properties on a virtual machine image</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

<span data-ttu-id="d0fc0-111">Эта команда задает свойства диска для данных на виртуальной машине и обновляет образ виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d0fc0-111">This command sets data disk properties on a virtual machine then updates the virtual machine image.</span></span>

## <span data-ttu-id="d0fc0-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d0fc0-112">PARAMETERS</span></span>

### <span data-ttu-id="d0fc0-113">-DataDiskName</span><span class="sxs-lookup"><span data-stu-id="d0fc0-113">-DataDiskName</span></span>
<span data-ttu-id="d0fc0-114">Указывает имя диска данных, который настраивает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d0fc0-114">Specifies the name of the data disk that this cmdlet configures.</span></span>

```yaml
Type: String
Parameter Sets: UpdateAzureVMImageParamSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0fc0-115">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="d0fc0-115">-DiskConfig</span></span>
<span data-ttu-id="d0fc0-116">Указывает объект конфигурации диска, который инкапсулирует объекты операционной системы и дискового диска данных.</span><span class="sxs-lookup"><span data-stu-id="d0fc0-116">Specifies the disk configuration object that encapsulates the operating system disk and Data Disk objects.</span></span>

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

### <span data-ttu-id="d0fc0-117">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="d0fc0-117">-HostCaching</span></span>
<span data-ttu-id="d0fc0-118">Задает атрибут кэша узла для диска с операционной системой.</span><span class="sxs-lookup"><span data-stu-id="d0fc0-118">Specifies the host cache attribute for the operating system disk.</span></span>

<span data-ttu-id="d0fc0-119">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="d0fc0-119">Valid values are:</span></span>

<span data-ttu-id="d0fc0-120">-ReadOnly — ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d0fc0-120">--ReadOnly --ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0fc0-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d0fc0-121">-InformationAction</span></span>
<span data-ttu-id="d0fc0-122">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="d0fc0-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d0fc0-123">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d0fc0-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d0fc0-124">Продолжал</span><span class="sxs-lookup"><span data-stu-id="d0fc0-124">Continue</span></span>
- <span data-ttu-id="d0fc0-125">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="d0fc0-125">Ignore</span></span>
- <span data-ttu-id="d0fc0-126">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="d0fc0-126">Inquire</span></span>
- <span data-ttu-id="d0fc0-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d0fc0-127">SilentlyContinue</span></span>
- <span data-ttu-id="d0fc0-128">Остановить</span><span class="sxs-lookup"><span data-stu-id="d0fc0-128">Stop</span></span>
- <span data-ttu-id="d0fc0-129">Рвать</span><span class="sxs-lookup"><span data-stu-id="d0fc0-129">Suspend</span></span>

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

### <span data-ttu-id="d0fc0-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d0fc0-130">-InformationVariable</span></span>
<span data-ttu-id="d0fc0-131">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="d0fc0-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d0fc0-132">-LUN</span><span class="sxs-lookup"><span data-stu-id="d0fc0-132">-Lun</span></span>
<span data-ttu-id="d0fc0-133">Указывает ячейку, в которой на виртуальной машине монтируется диск данных.</span><span class="sxs-lookup"><span data-stu-id="d0fc0-133">Specifies the slot where the data drive is mounted in the virtual machine.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0fc0-134">-MediaLink</span><span class="sxs-lookup"><span data-stu-id="d0fc0-134">-MediaLink</span></span>
<span data-ttu-id="d0fc0-135">Задает универсальный код ресурса (URI) места, где создается новый виртуальный жесткий диск при добавлении нового диска с данными.</span><span class="sxs-lookup"><span data-stu-id="d0fc0-135">Specifies the URI of the location where the new virtual hard drive is created when the new data disk is added.</span></span>

```yaml
Type: Uri
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0fc0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0fc0-136">CommonParameters</span></span>
<span data-ttu-id="d0fc0-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d0fc0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0fc0-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0fc0-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0fc0-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d0fc0-139">INPUTS</span></span>

## <span data-ttu-id="d0fc0-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0fc0-140">OUTPUTS</span></span>

### <span data-ttu-id="d0fc0-141">Microsoft. WindowsAzure. Commands. ServiceManagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="d0fc0-141">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="d0fc0-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="d0fc0-142">NOTES</span></span>

## <span data-ttu-id="d0fc0-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d0fc0-143">RELATED LINKS</span></span>

[<span data-ttu-id="d0fc0-144">Remove-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="d0fc0-144">Remove-AzureVMImageDataDiskConfig</span></span>](./Remove-AzureVMImageDataDiskConfig.md)


