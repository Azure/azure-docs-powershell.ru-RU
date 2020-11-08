---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D563ACF6-6BCD-4463-8731-175BA047A74D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ceb2af6b359d5b9660397ef654d6c56e045ce64
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076166"
---
# <span data-ttu-id="54138-101">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="54138-101">Remove-AzureDataDisk</span></span>

## <span data-ttu-id="54138-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="54138-102">SYNOPSIS</span></span>
<span data-ttu-id="54138-103">Удаление диска с данными из виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="54138-103">Removes a data disk from an Azure virtual machine.</span></span>

## <span data-ttu-id="54138-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="54138-104">SYNTAX</span></span>

```
Remove-AzureDataDisk [-LUN] <Int32> [-DeleteVHD] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="54138-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54138-105">DESCRIPTION</span></span>
<span data-ttu-id="54138-106">Командлет **Remove-AzureDataDisk** удаляет диск с данными из виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="54138-106">The **Remove-AzureDataDisk** cmdlet removes a data disk from an Azure virtual machine.</span></span>
<span data-ttu-id="54138-107">По умолчанию этот командлет не удаляет большой двоичный объект диска данных из учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="54138-107">By default, this cmdlet does not remove the data disk blob from the storage account.</span></span>

## <span data-ttu-id="54138-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="54138-108">EXAMPLES</span></span>

### <span data-ttu-id="54138-109">Пример 1: удаление диска с данными</span><span class="sxs-lookup"><span data-stu-id="54138-109">Example 1: Remove a data disk</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureDataDisk -LUN 0
```

<span data-ttu-id="54138-110">Эта команда получает виртуальную машину с именем VirtualMachine07 в службе с именем ContosoService с помощью командлета **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="54138-110">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="54138-111">Команда передает виртуальную машину в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="54138-111">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="54138-112">Текущий командлет удаляет диск с данными LUN 0.</span><span class="sxs-lookup"><span data-stu-id="54138-112">The current cmdlet removes the data disk that has the LUN 0.</span></span>

### <span data-ttu-id="54138-113">Пример 2: удаление диска с данными и файла виртуального жесткого диска</span><span class="sxs-lookup"><span data-stu-id="54138-113">Example 2: Remove a data disk and the virtual hard disk file</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureDataDisk -LUN 0 -DeleteVHD | Update-AzureVM
```

<span data-ttu-id="54138-114">Эта команда получает виртуальную машину с именем VirtualMachine07 в службе с именем ContosoService.</span><span class="sxs-lookup"><span data-stu-id="54138-114">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService.</span></span>
<span data-ttu-id="54138-115">Команда передает виртуальную машину в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="54138-115">The command passes the virtual machine to the current cmdlet.</span></span>
<span data-ttu-id="54138-116">Текущий командлет удаляет диск с данными LUN 0.</span><span class="sxs-lookup"><span data-stu-id="54138-116">The current cmdlet removes the data disk that has the LUN 0.</span></span>
<span data-ttu-id="54138-117">Команда содержит параметр *DeleteVHD* .</span><span class="sxs-lookup"><span data-stu-id="54138-117">The command includes the *DeleteVHD* parameter.</span></span>
<span data-ttu-id="54138-118">Таким образом, он также удаляет базовый виртуальный жесткий диск.</span><span class="sxs-lookup"><span data-stu-id="54138-118">Therefore, it also deletes the underlying virtual hard disk.</span></span>
<span data-ttu-id="54138-119">Команда обновляет виртуальную машину, отображая изменения с помощью командлета **Update-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="54138-119">The command updates the virtual machine to reflect your changes by using the **Update-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="54138-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="54138-120">PARAMETERS</span></span>

### <span data-ttu-id="54138-121">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="54138-121">-DeleteVHD</span></span>
<span data-ttu-id="54138-122">Указывает, что этот командлет удаляет диск данных и виртуальный жесткий диск (VHD) из хранилища BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="54138-122">Indicates that this cmdlet removes the data disk and the virtual hard disk (VHD) from blob storage.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54138-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="54138-123">-InformationAction</span></span>
<span data-ttu-id="54138-124">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="54138-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="54138-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="54138-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="54138-126">Продолжал</span><span class="sxs-lookup"><span data-stu-id="54138-126">Continue</span></span>
- <span data-ttu-id="54138-127">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="54138-127">Ignore</span></span>
- <span data-ttu-id="54138-128">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="54138-128">Inquire</span></span>
- <span data-ttu-id="54138-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="54138-129">SilentlyContinue</span></span>
- <span data-ttu-id="54138-130">Остановить</span><span class="sxs-lookup"><span data-stu-id="54138-130">Stop</span></span>
- <span data-ttu-id="54138-131">Рвать</span><span class="sxs-lookup"><span data-stu-id="54138-131">Suspend</span></span>

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

### <span data-ttu-id="54138-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="54138-132">-InformationVariable</span></span>
<span data-ttu-id="54138-133">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="54138-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="54138-134">-LUN</span><span class="sxs-lookup"><span data-stu-id="54138-134">-LUN</span></span>
<span data-ttu-id="54138-135">Задает логический номер устройства (LUN) для диска данных в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="54138-135">Specifies the logical unit number (LUN) for the data drive in the virtual machine.</span></span>
<span data-ttu-id="54138-136">Допустимые значения: от 0 до 15.</span><span class="sxs-lookup"><span data-stu-id="54138-136">Valid values are: 0 through 15.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54138-137">-Profile</span><span class="sxs-lookup"><span data-stu-id="54138-137">-Profile</span></span>
<span data-ttu-id="54138-138">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="54138-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="54138-139">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="54138-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="54138-140">-VM</span><span class="sxs-lookup"><span data-stu-id="54138-140">-VM</span></span>
<span data-ttu-id="54138-141">Указывает объект виртуальной машины, прикрепленный к диску данных.</span><span class="sxs-lookup"><span data-stu-id="54138-141">Specifies the virtual machine object that is attached to the data disk.</span></span>
<span data-ttu-id="54138-142">Чтобы получить объект виртуальной машины, используйте командлет **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="54138-142">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="54138-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54138-143">CommonParameters</span></span>
<span data-ttu-id="54138-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="54138-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54138-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54138-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54138-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="54138-146">INPUTS</span></span>

## <span data-ttu-id="54138-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="54138-147">OUTPUTS</span></span>

## <span data-ttu-id="54138-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="54138-148">NOTES</span></span>

## <span data-ttu-id="54138-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54138-149">RELATED LINKS</span></span>

[<span data-ttu-id="54138-150">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="54138-150">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="54138-151">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="54138-151">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="54138-152">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="54138-152">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="54138-153">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="54138-153">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)

[<span data-ttu-id="54138-154">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="54138-154">Update-AzureVM</span></span>](./Update-AzureVM.md)


