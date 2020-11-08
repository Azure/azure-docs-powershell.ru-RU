---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 64EF867E-5142-4317-9552-8BC94117208D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 899ecd0256bc3d6f88b8f942fa488db444a9bb41
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076066"
---
# <span data-ttu-id="fad90-101">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="fad90-101">Set-AzureDataDisk</span></span>

## <span data-ttu-id="fad90-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fad90-102">SYNOPSIS</span></span>
<span data-ttu-id="fad90-103">Изменяет кэширование узла для существующего диска с данными на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="fad90-103">Modifies the host caching of an existing data disk on an Azure virtual machine.</span></span>

## <span data-ttu-id="fad90-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fad90-104">SYNTAX</span></span>

### <span data-ttu-id="fad90-105">NoResize</span><span class="sxs-lookup"><span data-stu-id="fad90-105">NoResize</span></span>
```
Set-AzureDataDisk [-HostCaching] <String> [-LUN] <Int32> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="fad90-106">Изменение размера</span><span class="sxs-lookup"><span data-stu-id="fad90-106">Resize</span></span>
```
Set-AzureDataDisk [-DiskName] <String> [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="fad90-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fad90-107">DESCRIPTION</span></span>
<span data-ttu-id="fad90-108">Командлет **Set-AzureDataDisk** изменяет атрибуты кэша для существующего диска с данными на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="fad90-108">The **Set-AzureDataDisk** cmdlet modifies the cache attributes of an existing data disk on an Azure virtual machine.</span></span>
<span data-ttu-id="fad90-109">Укажите, какой диск данных нужно обновить по его логическому номеру устройства (LUN).</span><span class="sxs-lookup"><span data-stu-id="fad90-109">Specify which data disk to update by its logical unit number (LUN).</span></span>

## <span data-ttu-id="fad90-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fad90-110">EXAMPLES</span></span>

### <span data-ttu-id="fad90-111">Пример 1: изменение кэширования узла для диска данных</span><span class="sxs-lookup"><span data-stu-id="fad90-111">Example 1: Modify the host caching for a data disk</span></span>
```
PS C:\> Get-AzureVM "ContosoService" | Set-AzureDataDisk -VM "VirtualMachine07" -LUN 2 -HostCaching ReadOnly | Update-AzureVM
```

<span data-ttu-id="fad90-112">Эта команда получает виртуальные машины, которые выполняются в службе с именем ContosoService, с помощью командлета **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="fad90-112">This command gets the virtual machines that run on the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="fad90-113">Команда передает их в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="fad90-113">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fad90-114">Этот командлет задает диск данных на LUN 2 виртуальной машины с именем VirtualMachine07, чтобы использовать кэширование узлов только для чтения.</span><span class="sxs-lookup"><span data-stu-id="fad90-114">That cmdlet sets the data disk at LUN 2 of the virtual machine named VirtualMachine07 to use ReadOnly host caching.</span></span>
<span data-ttu-id="fad90-115">Команда обновляет виртуальную машину, отображая изменения с помощью командлета **Update-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="fad90-115">The command updates the virtual machine to reflect your changes by using the **Update-AzureVM** cmdlet.</span></span>

### <span data-ttu-id="fad90-116">Пример 2: изменение кэширования узла для всех дисков данных на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="fad90-116">Example 2: Modify the host caching for all data disks on a virtual machine</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk | Set-AzureDataDisk -HostCaching ReadWrite | Update-AzureVM
```

<span data-ttu-id="fad90-117">Эта команда получает объект для виртуальной машины с именем VirtualMachine07 в облачной службе ContosoService.</span><span class="sxs-lookup"><span data-stu-id="fad90-117">This command gets an object for the virtual machine named VirtualMachine07 on the ContosoService cloud service.</span></span>
<span data-ttu-id="fad90-118">Команда передается командлету **Get-AzureDataDisk** , который получает диски данных для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fad90-118">The command passes it to the **Get-AzureDataDisk** cmdlet, which gets the data disks for that virtual machine.</span></span>
<span data-ttu-id="fad90-119">Затем текущий командлет задает режим кэширования узла для всех дисков с данными в ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="fad90-119">The current cmdlet then sets the host caching mode of each data disks to ReadWrite.</span></span>
<span data-ttu-id="fad90-120">Команда обновит виртуальную машину, чтобы отразить ваши изменения.</span><span class="sxs-lookup"><span data-stu-id="fad90-120">The command updates the virtual machine to reflect your changes.</span></span>

## <span data-ttu-id="fad90-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fad90-121">PARAMETERS</span></span>

### <span data-ttu-id="fad90-122">-DiskName</span><span class="sxs-lookup"><span data-stu-id="fad90-122">-DiskName</span></span>
<span data-ttu-id="fad90-123">Указывает имя конфигурации диска данных, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="fad90-123">Specifies the name of the data disk configuration that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: Resize
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fad90-124">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="fad90-124">-HostCaching</span></span>

> [!WARNING]
> <span data-ttu-id="fad90-125">Кэширование диска не поддерживается для дисков 4 TiB и более крупных.</span><span class="sxs-lookup"><span data-stu-id="fad90-125">Disk Caching is not supported for disks 4 TiB and larger.</span></span> <span data-ttu-id="fad90-126">Если к ВМ подключено несколько дисков, то каждый из дисков, размер которых меньше 4 TiB, будет поддерживать кэширование.</span><span class="sxs-lookup"><span data-stu-id="fad90-126">If multiple disks are attached to your VM, each disk that is smaller than 4 TiB will support caching.</span></span>
>
> <span data-ttu-id="fad90-127">Изменение параметра кэша диска Azure отсоединяет и повторно подключает конечный диск.</span><span class="sxs-lookup"><span data-stu-id="fad90-127">Changing the cache setting of an Azure disk detaches and re-attaches the target disk.</span></span> <span data-ttu-id="fad90-128">Если это диск операционной системы, виртуальная машина перезапускается.</span><span class="sxs-lookup"><span data-stu-id="fad90-128">If it is the operating system disk, the VM is restarted.</span></span> <span data-ttu-id="fad90-129">Перед изменением параметров кэша дисков Остановите все приложения и службы, которые могут повлиять на этот перерыв.</span><span class="sxs-lookup"><span data-stu-id="fad90-129">Stop all applications/services that might be affected by this disruption before changing the disk cache setting.</span></span> <span data-ttu-id="fad90-130">Отсутствие подписки на эти рекомендации может привести к повреждению данных.</span><span class="sxs-lookup"><span data-stu-id="fad90-130">Not following those recommendations could lead to data corruption.</span></span>

<span data-ttu-id="fad90-131">Задает параметры кэширования на уровне узла для диска.</span><span class="sxs-lookup"><span data-stu-id="fad90-131">Specifies the host level caching settings of the disk.</span></span>
<span data-ttu-id="fad90-132">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="fad90-132">Valid values are:</span></span>

- <span data-ttu-id="fad90-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="fad90-133">None</span></span>
- <span data-ttu-id="fad90-134">Чтения</span><span class="sxs-lookup"><span data-stu-id="fad90-134">ReadOnly</span></span>
- <span data-ttu-id="fad90-135">Операцию</span><span class="sxs-lookup"><span data-stu-id="fad90-135">ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: NoResize
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fad90-136">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="fad90-136">-InformationAction</span></span>
<span data-ttu-id="fad90-137">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="fad90-137">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fad90-138">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fad90-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fad90-139">Продолжал</span><span class="sxs-lookup"><span data-stu-id="fad90-139">Continue</span></span>
- <span data-ttu-id="fad90-140">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="fad90-140">Ignore</span></span>
- <span data-ttu-id="fad90-141">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="fad90-141">Inquire</span></span>
- <span data-ttu-id="fad90-142">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fad90-142">SilentlyContinue</span></span>
- <span data-ttu-id="fad90-143">Остановить</span><span class="sxs-lookup"><span data-stu-id="fad90-143">Stop</span></span>
- <span data-ttu-id="fad90-144">Рвать</span><span class="sxs-lookup"><span data-stu-id="fad90-144">Suspend</span></span>

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

### <span data-ttu-id="fad90-145">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fad90-145">-InformationVariable</span></span>
<span data-ttu-id="fad90-146">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="fad90-146">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fad90-147">-LUN</span><span class="sxs-lookup"><span data-stu-id="fad90-147">-LUN</span></span>
<span data-ttu-id="fad90-148">Указывает LUN для диска данных в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="fad90-148">Specifies the LUN for the data drive in the virtual machine.</span></span>
<span data-ttu-id="fad90-149">Допустимые значения: от 0 до 15.</span><span class="sxs-lookup"><span data-stu-id="fad90-149">Valid values are: 0 through 15.</span></span>

```yaml
Type: Int32
Parameter Sets: NoResize
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fad90-150">-Profile</span><span class="sxs-lookup"><span data-stu-id="fad90-150">-Profile</span></span>
<span data-ttu-id="fad90-151">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="fad90-151">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fad90-152">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fad90-152">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fad90-153">-ResizedSizeInGB</span><span class="sxs-lookup"><span data-stu-id="fad90-153">-ResizedSizeInGB</span></span>
<span data-ttu-id="fad90-154">Указывает новый размер (в гигабайтах) для диска с данными.</span><span class="sxs-lookup"><span data-stu-id="fad90-154">Specifies the new size, in gigabytes, for the data disk.</span></span>
<span data-ttu-id="fad90-155">Новый размер должен быть больше текущего размера.</span><span class="sxs-lookup"><span data-stu-id="fad90-155">The new size must be larger than the current size.</span></span>

```yaml
Type: Int32
Parameter Sets: Resize
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fad90-156">-VM</span><span class="sxs-lookup"><span data-stu-id="fad90-156">-VM</span></span>
<span data-ttu-id="fad90-157">Указывает объект виртуальной машины, прикрепленный к диску данных.</span><span class="sxs-lookup"><span data-stu-id="fad90-157">Specifies the virtual machine object that is attached to the data disk.</span></span>
<span data-ttu-id="fad90-158">Чтобы получить объект виртуальной машины, используйте командлет **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="fad90-158">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fad90-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fad90-159">CommonParameters</span></span>
<span data-ttu-id="fad90-160">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fad90-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fad90-161">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fad90-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fad90-162">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fad90-162">INPUTS</span></span>

## <span data-ttu-id="fad90-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fad90-163">OUTPUTS</span></span>

## <span data-ttu-id="fad90-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="fad90-164">NOTES</span></span>

## <span data-ttu-id="fad90-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fad90-165">RELATED LINKS</span></span>

[<span data-ttu-id="fad90-166">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="fad90-166">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="fad90-167">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="fad90-167">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="fad90-168">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="fad90-168">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="fad90-169">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="fad90-169">Remove-AzureDataDisk</span></span>](./Remove-AzureDataDisk.md)

[<span data-ttu-id="fad90-170">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="fad90-170">Update-AzureVM</span></span>](./Update-AzureVM.md)


