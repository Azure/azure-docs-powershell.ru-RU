---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2A8BE3EB-4929-4B40-82EA-5434C09A5251
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1974de3f5c4bf39aa32100e67bb04642ebcfe3da
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075651"
---
# <span data-ttu-id="f6d92-101">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="f6d92-101">Get-AzureDataDisk</span></span>

## <span data-ttu-id="f6d92-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f6d92-102">SYNOPSIS</span></span>
<span data-ttu-id="f6d92-103">Получает диски данных Azure.</span><span class="sxs-lookup"><span data-stu-id="f6d92-103">Gets Azure data disks.</span></span>

## <span data-ttu-id="f6d92-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f6d92-104">SYNTAX</span></span>

```
Get-AzureDataDisk [[-Lun] <Int32>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f6d92-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6d92-105">DESCRIPTION</span></span>
<span data-ttu-id="f6d92-106">Командлет **Get-AzureDataDisk** получает объект, который представляет диски данных на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="f6d92-106">The **Get-AzureDataDisk** cmdlet gets an object that represents the data disks on an Azure virtual machine.</span></span>
<span data-ttu-id="f6d92-107">Чтобы получить конкретный объект диска данных, укажите логический номер устройства (LUN) диска.</span><span class="sxs-lookup"><span data-stu-id="f6d92-107">To get a specific data disk object, specify the logical unit number (LUN) of the disk.</span></span>

## <span data-ttu-id="f6d92-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f6d92-108">EXAMPLES</span></span>

### <span data-ttu-id="f6d92-109">Пример 1: получение всех дисков с данными для виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="f6d92-109">Example 1: Get all data disks for a virtual machine</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk
```

<span data-ttu-id="f6d92-110">Эта команда получает виртуальную машину с именем VirtualMachine07 в службе с именем ContosoService с помощью командлета **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="f6d92-110">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="f6d92-111">Команда передает виртуальную машину в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="f6d92-111">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f6d92-112">Текущий командлет получает все диски данных для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f6d92-112">The current cmdlet gets all the data disks for this virtual machine.</span></span>

### <span data-ttu-id="f6d92-113">Пример 2: получение определенного диска с данными для vituralvirtual machinevirtual</span><span class="sxs-lookup"><span data-stu-id="f6d92-113">Example 2: Get a specific data disk for a vituralvirtual machinevirtual</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk -LUN 2
```

<span data-ttu-id="f6d92-114">Эта команда получает виртуальную машину с именем VirtualMachine07 в службе с именем ContosoService.</span><span class="sxs-lookup"><span data-stu-id="f6d92-114">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService.</span></span>
<span data-ttu-id="f6d92-115">Команда передает виртуальную машину в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="f6d92-115">The command passes the virtual machine to the current cmdlet.</span></span>
<span data-ttu-id="f6d92-116">Текущий командлет получает диск данных, на котором установлен LUN 2.</span><span class="sxs-lookup"><span data-stu-id="f6d92-116">The current cmdlet gets the data disk that has the LUN 2.</span></span>

## <span data-ttu-id="f6d92-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f6d92-117">PARAMETERS</span></span>

### <span data-ttu-id="f6d92-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f6d92-118">-InformationAction</span></span>
<span data-ttu-id="f6d92-119">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="f6d92-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f6d92-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f6d92-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f6d92-121">Продолжал</span><span class="sxs-lookup"><span data-stu-id="f6d92-121">Continue</span></span>
- <span data-ttu-id="f6d92-122">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="f6d92-122">Ignore</span></span>
- <span data-ttu-id="f6d92-123">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="f6d92-123">Inquire</span></span>
- <span data-ttu-id="f6d92-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f6d92-124">SilentlyContinue</span></span>
- <span data-ttu-id="f6d92-125">Остановить</span><span class="sxs-lookup"><span data-stu-id="f6d92-125">Stop</span></span>
- <span data-ttu-id="f6d92-126">Рвать</span><span class="sxs-lookup"><span data-stu-id="f6d92-126">Suspend</span></span>

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

### <span data-ttu-id="f6d92-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f6d92-127">-InformationVariable</span></span>
<span data-ttu-id="f6d92-128">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="f6d92-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f6d92-129">-LUN</span><span class="sxs-lookup"><span data-stu-id="f6d92-129">-Lun</span></span>
<span data-ttu-id="f6d92-130">Указывает LUN для диска данных в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="f6d92-130">Specifies the LUN for the data drive in the virtual machine.</span></span>
<span data-ttu-id="f6d92-131">Допустимые значения: от 0 до 15.</span><span class="sxs-lookup"><span data-stu-id="f6d92-131">Valid values are: 0 through 15.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6d92-132">-Profile</span><span class="sxs-lookup"><span data-stu-id="f6d92-132">-Profile</span></span>
<span data-ttu-id="f6d92-133">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f6d92-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f6d92-134">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f6d92-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f6d92-135">-VM</span><span class="sxs-lookup"><span data-stu-id="f6d92-135">-VM</span></span>
<span data-ttu-id="f6d92-136">Указывает объект виртуальной машины, для которого этот командлет получает диски данных.</span><span class="sxs-lookup"><span data-stu-id="f6d92-136">Specifies the virtual machine object for which this cmdlet gets data disks.</span></span>
<span data-ttu-id="f6d92-137">Чтобы получить объект виртуальной машины, используйте командлет **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="f6d92-137">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="f6d92-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6d92-138">CommonParameters</span></span>
<span data-ttu-id="f6d92-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f6d92-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6d92-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6d92-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6d92-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f6d92-141">INPUTS</span></span>

## <span data-ttu-id="f6d92-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6d92-142">OUTPUTS</span></span>

## <span data-ttu-id="f6d92-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="f6d92-143">NOTES</span></span>

## <span data-ttu-id="f6d92-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6d92-144">RELATED LINKS</span></span>

[<span data-ttu-id="f6d92-145">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="f6d92-145">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="f6d92-146">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f6d92-146">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="f6d92-147">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="f6d92-147">Remove-AzureDataDisk</span></span>](./Remove-AzureDataDisk.md)

[<span data-ttu-id="f6d92-148">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="f6d92-148">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)


