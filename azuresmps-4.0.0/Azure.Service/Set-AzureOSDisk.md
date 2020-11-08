---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 02DB15F5-5CE0-4FF0-8863-AF1B2BA5E775
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41f72ace02132ba4184af08e995404b47f76d0b0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075828"
---
# <span data-ttu-id="51cd6-101">Set-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="51cd6-101">Set-AzureOSDisk</span></span>

## <span data-ttu-id="51cd6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="51cd6-102">SYNOPSIS</span></span>
<span data-ttu-id="51cd6-103">Изменение режима кэширования узла для виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="51cd6-103">Modifies the host cache mode of an Azure virtual machine.</span></span>

## <span data-ttu-id="51cd6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="51cd6-104">SYNTAX</span></span>

### <span data-ttu-id="51cd6-105">NoResize</span><span class="sxs-lookup"><span data-stu-id="51cd6-105">NoResize</span></span>
```
Set-AzureOSDisk [-HostCaching] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="51cd6-106">Изменение размера</span><span class="sxs-lookup"><span data-stu-id="51cd6-106">Resize</span></span>
```
Set-AzureOSDisk [[-HostCaching] <String>] [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="51cd6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="51cd6-107">DESCRIPTION</span></span>
<span data-ttu-id="51cd6-108">Командлет **Set-AzureOSDisk** изменяет режим кэширования хоста на диске операционной системы виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="51cd6-108">The **Set-AzureOSDisk** cmdlet modifies the host cache mode of the operating system disk of an Azure virtual machine.</span></span>
<span data-ttu-id="51cd6-109">Поддерживаемые режимы кэширования узла: ReadOnly и ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="51cd6-109">The supported host cache modes are ReadOnly and ReadWrite.</span></span>
<span data-ttu-id="51cd6-110">Если запустить этот командлет на работающей виртуальной машине, эта виртуальная машина будет перезапущена.</span><span class="sxs-lookup"><span data-stu-id="51cd6-110">If you run this cmdlet on a virtual machine that is running, that virtual machine restarts.</span></span>

## <span data-ttu-id="51cd6-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="51cd6-111">EXAMPLES</span></span>

### <span data-ttu-id="51cd6-112">Пример 1: Настройка режима кэширования узла на ReadOnly с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="51cd6-112">Example 1: Set the host cache mode to ReadOnly by using the pipeline</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02" | Set-AzureOSDisk -HostCaching "ReadOnly"
```

<span data-ttu-id="51cd6-113">Эта команда получает виртуальную машину с именем VirtualMachine02 в службе с именем ContosoService с помощью командлета **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="51cd6-113">This command gets the virtual machine named VirtualMachine02 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="51cd6-114">Команда передает виртуальную машину в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="51cd6-114">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="51cd6-115">Текущий командлет устанавливает режим кэширования на диске операционной системы для виртуальной машины на ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="51cd6-115">The current cmdlet sets the host cache mode of the operating system disk of that virtual machine to be ReadOnly.</span></span>

### <span data-ttu-id="51cd6-116">Пример 2: Настройка режима кэширования узла на ReadWrite</span><span class="sxs-lookup"><span data-stu-id="51cd6-116">Example 2: Set the host cache mode to ReadWrite</span></span>
```
PS C:\> $VM = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02"
PS C:\> Set-AzureOSDisk "ReadWrite" -VM $myVM2
```

<span data-ttu-id="51cd6-117">Первая команда получает виртуальную машину с именем VirtualMachine02 в службе с именем ContosoService и сохраняет ее в переменной.</span><span class="sxs-lookup"><span data-stu-id="51cd6-117">The first command gets the virtual machine named VirtualMachine02 in the service named ContosoService, and then stores it in the variable.</span></span>

<span data-ttu-id="51cd6-118">Вторая команда задает в качестве режима кэширования на диске операционной системы для виртуальной машины значение ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="51cd6-118">The second command sets the host cache mode of the operating system disk of that virtual machine to be ReadWrite.</span></span>

## <span data-ttu-id="51cd6-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="51cd6-119">PARAMETERS</span></span>

### <span data-ttu-id="51cd6-120">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="51cd6-120">-HostCaching</span></span>
<span data-ttu-id="51cd6-121">Задает атрибут кэша узла для диска с операционной системой.</span><span class="sxs-lookup"><span data-stu-id="51cd6-121">Specifies the host cache attribute for the operating system disk.</span></span>
<span data-ttu-id="51cd6-122">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="51cd6-122">Valid values are:</span></span> 

- <span data-ttu-id="51cd6-123">Чтения</span><span class="sxs-lookup"><span data-stu-id="51cd6-123">ReadOnly</span></span> 
- <span data-ttu-id="51cd6-124">Операцию</span><span class="sxs-lookup"><span data-stu-id="51cd6-124">ReadWrite</span></span>

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

```yaml
Type: String
Parameter Sets: Resize
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51cd6-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="51cd6-125">-InformationAction</span></span>
<span data-ttu-id="51cd6-126">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="51cd6-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="51cd6-127">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="51cd6-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="51cd6-128">Продолжал</span><span class="sxs-lookup"><span data-stu-id="51cd6-128">Continue</span></span>
- <span data-ttu-id="51cd6-129">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="51cd6-129">Ignore</span></span>
- <span data-ttu-id="51cd6-130">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="51cd6-130">Inquire</span></span>
- <span data-ttu-id="51cd6-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="51cd6-131">SilentlyContinue</span></span>
- <span data-ttu-id="51cd6-132">Остановить</span><span class="sxs-lookup"><span data-stu-id="51cd6-132">Stop</span></span>
- <span data-ttu-id="51cd6-133">Рвать</span><span class="sxs-lookup"><span data-stu-id="51cd6-133">Suspend</span></span>

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

### <span data-ttu-id="51cd6-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="51cd6-134">-InformationVariable</span></span>
<span data-ttu-id="51cd6-135">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="51cd6-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="51cd6-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="51cd6-136">-Profile</span></span>
<span data-ttu-id="51cd6-137">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="51cd6-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="51cd6-138">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="51cd6-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="51cd6-139">-ResizedSizeInGB</span><span class="sxs-lookup"><span data-stu-id="51cd6-139">-ResizedSizeInGB</span></span>
<span data-ttu-id="51cd6-140">Указывает новый размер (в гигабайтах) для диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="51cd6-140">Specifies a new size, in gigabytes, for the operating system disk.</span></span>
<span data-ttu-id="51cd6-141">Размер должен быть больше текущего размера.</span><span class="sxs-lookup"><span data-stu-id="51cd6-141">The size must be larger than the current size.</span></span>

```yaml
Type: Int32
Parameter Sets: Resize
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51cd6-142">-VM</span><span class="sxs-lookup"><span data-stu-id="51cd6-142">-VM</span></span>
<span data-ttu-id="51cd6-143">Указывает виртуальную машину, для которой этот командлет изменяет диск операционной системы.</span><span class="sxs-lookup"><span data-stu-id="51cd6-143">Specifies the virtual machine for which this cmdlet modifies the operating system disk.</span></span>
<span data-ttu-id="51cd6-144">Чтобы получить объект виртуальной машины, используйте командлет **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="51cd6-144">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="51cd6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51cd6-145">CommonParameters</span></span>
<span data-ttu-id="51cd6-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="51cd6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51cd6-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51cd6-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51cd6-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="51cd6-148">INPUTS</span></span>

## <span data-ttu-id="51cd6-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="51cd6-149">OUTPUTS</span></span>

## <span data-ttu-id="51cd6-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="51cd6-150">NOTES</span></span>

## <span data-ttu-id="51cd6-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="51cd6-151">RELATED LINKS</span></span>

[<span data-ttu-id="51cd6-152">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="51cd6-152">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="51cd6-153">Get-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="51cd6-153">Get-AzureOSDisk</span></span>](./Get-AzureOSDisk.md)

[<span data-ttu-id="51cd6-154">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="51cd6-154">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="51cd6-155">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="51cd6-155">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="51cd6-156">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="51cd6-156">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)

[<span data-ttu-id="51cd6-157">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="51cd6-157">Update-AzureVM</span></span>](./Update-AzureVM.md)


