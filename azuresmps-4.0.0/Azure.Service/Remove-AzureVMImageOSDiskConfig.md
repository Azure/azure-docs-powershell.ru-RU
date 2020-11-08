---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1E1F98E9-FC45-4BEF-90F6-A21D7DB7C82F
online version: ''
schema: 2.0.0
ms.openlocfilehash: eac6db4400e5c51f295e0bbf549117ffdbc97644
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076445"
---
# <span data-ttu-id="8e7f0-101">Remove-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="8e7f0-101">Remove-AzureVMImageOSDiskConfig</span></span>

## <span data-ttu-id="8e7f0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8e7f0-102">SYNOPSIS</span></span>
<span data-ttu-id="8e7f0-103">Удаляет конфигурацию диска операционной системы из объекта DiskConfigSet.</span><span class="sxs-lookup"><span data-stu-id="8e7f0-103">Removes the operating system disk configuration from the DiskConfigSet object.</span></span>

## <span data-ttu-id="8e7f0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8e7f0-104">SYNTAX</span></span>

```
Remove-AzureVMImageOSDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8e7f0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e7f0-105">DESCRIPTION</span></span>
<span data-ttu-id="8e7f0-106">Командлет **Remove-AzureVMImageOSDiskConfig** удаляет конфигурацию диска операционной системы из объекта DiskConfigSet.</span><span class="sxs-lookup"><span data-stu-id="8e7f0-106">The **Remove-AzureVMImageOSDiskConfig** cmdlet removes the operating system disk configuration from the DiskConfigSet object.</span></span>

## <span data-ttu-id="8e7f0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8e7f0-107">EXAMPLES</span></span>

### <span data-ttu-id="8e7f0-108">Пример 1: Удаление конфигурации диска операционной системы из DiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="8e7f0-108">Example 1: Remove the operating system disk configuration from a DiskConfigSet</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> Remove-AzureVMImageOSDiskConfig -DiskConfig $Disk
```

<span data-ttu-id="8e7f0-109">Эта команда удаляет конфигурацию диска операционной системы из объекта DiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="8e7f0-109">This command removes the operating system disk configuration from the DiskConfigSet object</span></span>

## <span data-ttu-id="8e7f0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8e7f0-110">PARAMETERS</span></span>

### <span data-ttu-id="8e7f0-111">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="8e7f0-111">-DiskConfig</span></span>
<span data-ttu-id="8e7f0-112">Указывает объект конфигурации диска, который инкапсулирует объекты операционной системы и дискового диска данных.</span><span class="sxs-lookup"><span data-stu-id="8e7f0-112">Specifies the disk configuration object that encapsulates the operating system disk and Data Disk objects.</span></span>

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

### <span data-ttu-id="8e7f0-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8e7f0-113">-InformationAction</span></span>
<span data-ttu-id="8e7f0-114">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="8e7f0-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8e7f0-115">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="8e7f0-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8e7f0-116">Продолжал</span><span class="sxs-lookup"><span data-stu-id="8e7f0-116">Continue</span></span>
- <span data-ttu-id="8e7f0-117">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="8e7f0-117">Ignore</span></span>
- <span data-ttu-id="8e7f0-118">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="8e7f0-118">Inquire</span></span>
- <span data-ttu-id="8e7f0-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8e7f0-119">SilentlyContinue</span></span>
- <span data-ttu-id="8e7f0-120">Остановить</span><span class="sxs-lookup"><span data-stu-id="8e7f0-120">Stop</span></span>
- <span data-ttu-id="8e7f0-121">Рвать</span><span class="sxs-lookup"><span data-stu-id="8e7f0-121">Suspend</span></span>

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

### <span data-ttu-id="8e7f0-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8e7f0-122">-InformationVariable</span></span>
<span data-ttu-id="8e7f0-123">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="8e7f0-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8e7f0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e7f0-124">CommonParameters</span></span>
<span data-ttu-id="8e7f0-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8e7f0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e7f0-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e7f0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e7f0-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8e7f0-127">INPUTS</span></span>

## <span data-ttu-id="8e7f0-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e7f0-128">OUTPUTS</span></span>

### <span data-ttu-id="8e7f0-129">Microsoft. WindowsAzure. Commands. ServiceManagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="8e7f0-129">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="8e7f0-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="8e7f0-130">NOTES</span></span>

## <span data-ttu-id="8e7f0-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e7f0-131">RELATED LINKS</span></span>

[<span data-ttu-id="8e7f0-132">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="8e7f0-132">Set-AzureVMImageOSDiskConfig</span></span>](./Set-AzureVMImageOSDiskConfig.md)


