---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5CAF2D29-F4AE-4322-AA4F-61267723B955
online version: ''
schema: 2.0.0
ms.openlocfilehash: b2e19ad4b56e5141458f1fe9305a0c33691d024d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075497"
---
# <span data-ttu-id="9ac19-101">Remove-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="9ac19-101">Remove-AzureVMImageDataDiskConfig</span></span>

## <span data-ttu-id="9ac19-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9ac19-102">SYNOPSIS</span></span>
<span data-ttu-id="9ac19-103">Удаляет конфигурацию диска с данными из объекта DiskConfigSet.</span><span class="sxs-lookup"><span data-stu-id="9ac19-103">Removes the data disk configuration from the DiskConfigSet object.</span></span>

## <span data-ttu-id="9ac19-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9ac19-104">SYNTAX</span></span>

### <span data-ttu-id="9ac19-105">RemoveByDiskName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9ac19-105">RemoveByDiskName (Default)</span></span>
```
Remove-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-DataDiskName] <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="9ac19-106">RemoveByDiskLun</span><span class="sxs-lookup"><span data-stu-id="9ac19-106">RemoveByDiskLun</span></span>
```
Remove-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-Lun] <Int32>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9ac19-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ac19-107">DESCRIPTION</span></span>
<span data-ttu-id="9ac19-108">Командлет **Remove-AzureVMImageDataDiskConfig** удаляет конфигурацию диска с данными из объекта **DiskConfigSet** .</span><span class="sxs-lookup"><span data-stu-id="9ac19-108">The **Remove-AzureVMImageDataDiskConfig** cmdlet removes the data disk configuration from the **DiskConfigSet** object.</span></span>

## <span data-ttu-id="9ac19-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9ac19-109">EXAMPLES</span></span>

### <span data-ttu-id="9ac19-110">Пример 1: Удаление конфигурации диска с данными из объекта DiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="9ac19-110">Example 1: Remove the data disk configuration from the DiskConfigSet object</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> Remove-AzureVMImageDataDiskConfig -DiskConfig $Disk
```

<span data-ttu-id="9ac19-111">В этом примере создается **DiskConfigSet** , настраивается, а затем удаляется диск данных.</span><span class="sxs-lookup"><span data-stu-id="9ac19-111">This example creates a **DiskConfigSet** , configures it, then removes the data disk.</span></span>

## <span data-ttu-id="9ac19-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9ac19-112">PARAMETERS</span></span>

### <span data-ttu-id="9ac19-113">-DataDiskName</span><span class="sxs-lookup"><span data-stu-id="9ac19-113">-DataDiskName</span></span>
<span data-ttu-id="9ac19-114">Указывает имя диска данных, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="9ac19-114">Specifies the name of the data disk that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDiskName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ac19-115">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="9ac19-115">-DiskConfig</span></span>
<span data-ttu-id="9ac19-116">Указывает объект конфигурации диска, который инкапсулирует объекты операционной системы и дискового диска данных.</span><span class="sxs-lookup"><span data-stu-id="9ac19-116">Specifies the disk configuration object that encapsulates the operating system disk and data disk objects.</span></span>

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

### <span data-ttu-id="9ac19-117">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9ac19-117">-InformationAction</span></span>
<span data-ttu-id="9ac19-118">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="9ac19-118">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9ac19-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9ac19-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9ac19-120">Продолжал</span><span class="sxs-lookup"><span data-stu-id="9ac19-120">Continue</span></span>
- <span data-ttu-id="9ac19-121">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="9ac19-121">Ignore</span></span>
- <span data-ttu-id="9ac19-122">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="9ac19-122">Inquire</span></span>
- <span data-ttu-id="9ac19-123">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9ac19-123">SilentlyContinue</span></span>
- <span data-ttu-id="9ac19-124">Остановить</span><span class="sxs-lookup"><span data-stu-id="9ac19-124">Stop</span></span>
- <span data-ttu-id="9ac19-125">Рвать</span><span class="sxs-lookup"><span data-stu-id="9ac19-125">Suspend</span></span>

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

### <span data-ttu-id="9ac19-126">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9ac19-126">-InformationVariable</span></span>
<span data-ttu-id="9ac19-127">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="9ac19-127">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9ac19-128">-LUN</span><span class="sxs-lookup"><span data-stu-id="9ac19-128">-Lun</span></span>
<span data-ttu-id="9ac19-129">Указывает ячейку, в которой на виртуальной машине монтируется диск данных.</span><span class="sxs-lookup"><span data-stu-id="9ac19-129">Specifies the slot where the data drive is mounted in the virtual machine.</span></span>

```yaml
Type: Int32
Parameter Sets: RemoveByDiskLun
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ac19-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ac19-130">CommonParameters</span></span>
<span data-ttu-id="9ac19-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9ac19-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ac19-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ac19-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ac19-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9ac19-133">INPUTS</span></span>

## <span data-ttu-id="9ac19-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ac19-134">OUTPUTS</span></span>

### <span data-ttu-id="9ac19-135">Microsoft. WindowsAzure. Commands. ServiceManagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="9ac19-135">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="9ac19-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="9ac19-136">NOTES</span></span>

## <span data-ttu-id="9ac19-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ac19-137">RELATED LINKS</span></span>

[<span data-ttu-id="9ac19-138">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="9ac19-138">Set-AzureVMImageDataDiskConfig</span></span>](./Set-AzureVMImageDataDiskConfig.md)


