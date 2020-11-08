---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FDEDBF4F-7507-43FF-A983-7E431C0C1950
online version: ''
schema: 2.0.0
ms.openlocfilehash: 967fbaf83efa12bd305fc9fe075a9abffdd62dc3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075735"
---
# <span data-ttu-id="b9610-101">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="b9610-101">Add-AzureDataDisk</span></span>

## <span data-ttu-id="b9610-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b9610-102">SYNOPSIS</span></span>
<span data-ttu-id="b9610-103">Добавляет диск с данными на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="b9610-103">Adds a data disk to a virtual machine.</span></span>

## <span data-ttu-id="b9610-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b9610-104">SYNTAX</span></span>

### <span data-ttu-id="b9610-105">CreateNew (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b9610-105">CreateNew (Default)</span></span>
```
Add-AzureDataDisk [-CreateNew] [-DiskSizeInGB] <Int32> [-DiskLabel] <String> [-LUN] <Int32>
 [-MediaLocation <String>] [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b9610-106">Импортируем</span><span class="sxs-lookup"><span data-stu-id="b9610-106">Import</span></span>
```
Add-AzureDataDisk [-Import] [-DiskName] <String> [-LUN] <Int32> [-HostCaching <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="b9610-107">ImportFrom</span><span class="sxs-lookup"><span data-stu-id="b9610-107">ImportFrom</span></span>
```
Add-AzureDataDisk [-ImportFrom] [-DiskLabel] <String> [-LUN] <Int32> -MediaLocation <String>
 [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b9610-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9610-108">DESCRIPTION</span></span>
<span data-ttu-id="b9610-109">Командлет **Add-AzureDataDisk** добавляет новый или существующий диск данных в объект виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="b9610-109">The **Add-AzureDataDisk** cmdlet adds a new or existing data disk to an Azure virtual machine object.</span></span>
<span data-ttu-id="b9610-110">С помощью параметра *CreateNew* создайте новый диск с данными, который содержит заданные размер и метку.</span><span class="sxs-lookup"><span data-stu-id="b9610-110">Use the *CreateNew* parameter to create a new data disk that has a specified size and label.</span></span>
<span data-ttu-id="b9610-111">С помощью параметра *Import* вы можете подключить существующий диск из репозитория изображений.</span><span class="sxs-lookup"><span data-stu-id="b9610-111">Use the *Import* parameter to attach an existing disk from the image repository.</span></span>
<span data-ttu-id="b9610-112">Используйте параметр *ImportFrom* , чтобы присоединить существующий диск из большого двоичного объекта в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b9610-112">Use the *ImportFrom* parameter to attach an existing disk from a blob in a storage account.</span></span>
<span data-ttu-id="b9610-113">Вы можете указать режим кэширования хост-данных для подключенного диска с данными.</span><span class="sxs-lookup"><span data-stu-id="b9610-113">You can specify the host-cache mode of the attached data disk.</span></span>

## <span data-ttu-id="b9610-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b9610-114">EXAMPLES</span></span>

### <span data-ttu-id="b9610-115">Пример 1: импорт диска с данными из репозитория</span><span class="sxs-lookup"><span data-stu-id="b9610-115">Example 1: Import a data disk from the repository</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Add-AzureDataDisk -Import -DiskName "Disk68" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="b9610-116">Эта команда получает объект виртуальной машины для виртуальной машины с именем VirtualMachine07 в облачной службе ContosoService с помощью командлета **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="b9610-116">This command gets a virtual machine object for the virtual machine named VirtualMachine07 in the ContosoService cloud service by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="b9610-117">Команда передается текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="b9610-117">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b9610-118">Эта команда подключает существующий диск с данными из репозитория к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="b9610-118">That command attaches an existing data disk from the repository to the virtual machine.</span></span>
<span data-ttu-id="b9610-119">Диск с данными имеет LUN 0.</span><span class="sxs-lookup"><span data-stu-id="b9610-119">The data disk has a LUN of 0.</span></span>
<span data-ttu-id="b9610-120">Команда обновляет виртуальную машину, отображая изменения с помощью командлета **Update-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="b9610-120">The command updates the virtual machine to reflect your changes by using the **Update-AzureVM** cmdlet.</span></span>

### <span data-ttu-id="b9610-121">Пример 2: Добавление нового диска с данными</span><span class="sxs-lookup"><span data-stu-id="b9610-121">Example 2: Add a new data disk</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine08" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 128 -DiskLabel "main" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="b9610-122">Эта команда получает объект виртуальной машины для виртуальной машины с именем VirtualMachine08.</span><span class="sxs-lookup"><span data-stu-id="b9610-122">This command gets a virtual machine object for the virtual machine named VirtualMachine08.</span></span>
<span data-ttu-id="b9610-123">Команда передается текущему командлету.</span><span class="sxs-lookup"><span data-stu-id="b9610-123">The command passes it to the current cmdlet.</span></span>
<span data-ttu-id="b9610-124">Эта команда прикрепляет новый диск с данными с именем MyNewDisk. VHD.</span><span class="sxs-lookup"><span data-stu-id="b9610-124">That command attaches a new data disk named MyNewDisk.vhd.</span></span>
<span data-ttu-id="b9610-125">Командлет создает диск в контейнере виртуальных жестких дисков в учетной записи хранения по умолчанию текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="b9610-125">The cmdlet creates the disk in the vhds container in the default storage account of the current subscription.</span></span>
<span data-ttu-id="b9610-126">Команда обновит виртуальную машину, чтобы отразить ваши изменения.</span><span class="sxs-lookup"><span data-stu-id="b9610-126">The command updates the virtual machine to reflect your changes.</span></span>

### <span data-ttu-id="b9610-127">Пример 3: Добавление диска с данными из указанного места</span><span class="sxs-lookup"><span data-stu-id="b9610-127">Example 3: Add a data disk from a specified location</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "Database" | Add-AzureDataDisk -ImportFrom -MediaLocation "https://contosostorage.blob.core.windows.net/container07/Disk14.vhd" -DiskLabel "main" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="b9610-128">Эта команда получает объект виртуальной машины для виртуальной машины с именем Database.</span><span class="sxs-lookup"><span data-stu-id="b9610-128">This command gets a virtual machine object for the virtual machine named Database.</span></span>
<span data-ttu-id="b9610-129">Команда передается текущему командлету.</span><span class="sxs-lookup"><span data-stu-id="b9610-129">The command passes it to the current cmdlet.</span></span>
<span data-ttu-id="b9610-130">Эта команда подключает существующий диск данных с именем Disk14. VHD из указанного места.</span><span class="sxs-lookup"><span data-stu-id="b9610-130">That command attaches an existing data disk named Disk14.vhd from the specified location.</span></span>
<span data-ttu-id="b9610-131">Команда обновит виртуальную машину, чтобы отразить ваши изменения.</span><span class="sxs-lookup"><span data-stu-id="b9610-131">The command updates the virtual machine to reflect your changes.</span></span>

## <span data-ttu-id="b9610-132">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b9610-132">PARAMETERS</span></span>

### <span data-ttu-id="b9610-133">-CreateNew</span><span class="sxs-lookup"><span data-stu-id="b9610-133">-CreateNew</span></span>
<span data-ttu-id="b9610-134">Указывает на то, что этот командлет создает диск с данными.</span><span class="sxs-lookup"><span data-stu-id="b9610-134">Indicates that this cmdlet creates a data disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9610-135">-DiskLabel</span><span class="sxs-lookup"><span data-stu-id="b9610-135">-DiskLabel</span></span>
<span data-ttu-id="b9610-136">Указывает метку диска для нового диска с данными.</span><span class="sxs-lookup"><span data-stu-id="b9610-136">Specifies the disk label for a new data disk.</span></span>

```yaml
Type: String
Parameter Sets: CreateNew, ImportFrom
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9610-137">-DiskName</span><span class="sxs-lookup"><span data-stu-id="b9610-137">-DiskName</span></span>
<span data-ttu-id="b9610-138">Указывает имя диска данных в репозитории дисков.</span><span class="sxs-lookup"><span data-stu-id="b9610-138">Specifies the name of a data disk in the disk repository.</span></span>

```yaml
Type: String
Parameter Sets: Import
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9610-139">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="b9610-139">-DiskSizeInGB</span></span>
<span data-ttu-id="b9610-140">Задает размер логического диска (в гигабайтах) для нового диска с данными.</span><span class="sxs-lookup"><span data-stu-id="b9610-140">Specifies the logical disk size, in gigabytes, for a new data disk.</span></span>

```yaml
Type: Int32
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9610-141">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="b9610-141">-HostCaching</span></span>
<span data-ttu-id="b9610-142">Задает параметры кэширования на уровне узла для диска.</span><span class="sxs-lookup"><span data-stu-id="b9610-142">Specifies the host level caching settings of the disk.</span></span>
<span data-ttu-id="b9610-143">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="b9610-143">Valid values are:</span></span> 

- <span data-ttu-id="b9610-144">Ничего</span><span class="sxs-lookup"><span data-stu-id="b9610-144">None</span></span> 
- <span data-ttu-id="b9610-145">Чтения</span><span class="sxs-lookup"><span data-stu-id="b9610-145">ReadOnly</span></span> 
- <span data-ttu-id="b9610-146">Операцию</span><span class="sxs-lookup"><span data-stu-id="b9610-146">ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9610-147">-Import</span><span class="sxs-lookup"><span data-stu-id="b9610-147">-Import</span></span>
<span data-ttu-id="b9610-148">Указывает на то, что этот командлет импортирует существующий диск с данными из репозитория изображений.</span><span class="sxs-lookup"><span data-stu-id="b9610-148">Indicates that this cmdlet imports an existing data disk from the image repository.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Import
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9610-149">-ImportFrom</span><span class="sxs-lookup"><span data-stu-id="b9610-149">-ImportFrom</span></span>
<span data-ttu-id="b9610-150">Указывает на то, что этот командлет импортирует существующий диск с данными из большого двоичного объекта в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b9610-150">Indicates that this cmdlet imports an existing data disk from a blob in a storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ImportFrom
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9610-151">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b9610-151">-InformationAction</span></span>
<span data-ttu-id="b9610-152">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="b9610-152">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b9610-153">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b9610-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b9610-154">Продолжал</span><span class="sxs-lookup"><span data-stu-id="b9610-154">Continue</span></span>
- <span data-ttu-id="b9610-155">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="b9610-155">Ignore</span></span>
- <span data-ttu-id="b9610-156">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="b9610-156">Inquire</span></span>
- <span data-ttu-id="b9610-157">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b9610-157">SilentlyContinue</span></span>
- <span data-ttu-id="b9610-158">Остановить</span><span class="sxs-lookup"><span data-stu-id="b9610-158">Stop</span></span>
- <span data-ttu-id="b9610-159">Рвать</span><span class="sxs-lookup"><span data-stu-id="b9610-159">Suspend</span></span>

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

### <span data-ttu-id="b9610-160">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b9610-160">-InformationVariable</span></span>
<span data-ttu-id="b9610-161">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="b9610-161">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b9610-162">-LUN</span><span class="sxs-lookup"><span data-stu-id="b9610-162">-LUN</span></span>
<span data-ttu-id="b9610-163">Задает логический номер устройства (LUN) для диска данных в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="b9610-163">Specifies the logical unit number (LUN) for the data drive in the virtual machine.</span></span>
<span data-ttu-id="b9610-164">Допустимые значения: от 0 до 15.</span><span class="sxs-lookup"><span data-stu-id="b9610-164">Valid values are: 0 through 15.</span></span>
<span data-ttu-id="b9610-165">Каждый диск данных должен иметь уникальный LUN.</span><span class="sxs-lookup"><span data-stu-id="b9610-165">Each data disk must have a unique LUN.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9610-166">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="b9610-166">-MediaLocation</span></span>
<span data-ttu-id="b9610-167">Указывает расположение большого двоичного объекта в учетной записи хранения Azure, в котором этот командлет хранит диск данных.</span><span class="sxs-lookup"><span data-stu-id="b9610-167">Specifies the location of the blob in an Azure storage account where this cmdlet stores the data disk.</span></span>
<span data-ttu-id="b9610-168">Если расположение не задано, командлет сохраняет диск данных в контейнере VHDs в учетной записи хранения по умолчанию для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="b9610-168">If you do not specify a location, the cmdlet stores the data disk in the vhds container in the default storage account for the current subscription.</span></span>
<span data-ttu-id="b9610-169">Если контейнер виртуальных жестких дисков не существует, командлет создает контейнер виртуальных жестких дисков.</span><span class="sxs-lookup"><span data-stu-id="b9610-169">If a vhds container does not exist, the cmdlet creates a vhds container.</span></span>

```yaml
Type: String
Parameter Sets: CreateNew
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ImportFrom
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9610-170">-Profile</span><span class="sxs-lookup"><span data-stu-id="b9610-170">-Profile</span></span>
<span data-ttu-id="b9610-171">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b9610-171">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b9610-172">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b9610-172">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b9610-173">-VM</span><span class="sxs-lookup"><span data-stu-id="b9610-173">-VM</span></span>
<span data-ttu-id="b9610-174">Указывает объект виртуальной машины, к которому этот командлет прикрепляет диск данных.</span><span class="sxs-lookup"><span data-stu-id="b9610-174">Specifies the virtual machine object to which this cmdlet attaches a data disk.</span></span>
<span data-ttu-id="b9610-175">Чтобы получить объект виртуальной машины, используйте командлет **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="b9610-175">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="b9610-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9610-176">CommonParameters</span></span>
<span data-ttu-id="b9610-177">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b9610-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9610-178">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9610-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9610-179">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b9610-179">INPUTS</span></span>

## <span data-ttu-id="b9610-180">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9610-180">OUTPUTS</span></span>

## <span data-ttu-id="b9610-181">Пуск</span><span class="sxs-lookup"><span data-stu-id="b9610-181">NOTES</span></span>

## <span data-ttu-id="b9610-182">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9610-182">RELATED LINKS</span></span>

[<span data-ttu-id="b9610-183">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="b9610-183">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="b9610-184">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="b9610-184">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="b9610-185">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="b9610-185">Remove-AzureDataDisk</span></span>](./Remove-AzureDataDisk.md)

[<span data-ttu-id="b9610-186">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="b9610-186">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)

[<span data-ttu-id="b9610-187">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="b9610-187">Update-AzureVM</span></span>](./Update-AzureVM.md)


