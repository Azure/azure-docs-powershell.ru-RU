---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C6DFD49F-26A5-4199-A844-CA0FC405BEDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: f9fc407e2cf7375708fe82253f3d2fb40eb78f60
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076197"
---
# <span data-ttu-id="e33f2-101">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="e33f2-101">New-AzureVMConfig</span></span>

## <span data-ttu-id="e33f2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e33f2-102">SYNOPSIS</span></span>
<span data-ttu-id="e33f2-103">Создает объект конфигурации виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="e33f2-103">Creates an Azure virtual machine configuration object.</span></span>

## <span data-ttu-id="e33f2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e33f2-104">SYNTAX</span></span>

### <span data-ttu-id="e33f2-105">ImageName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e33f2-105">ImageName (Default)</span></span>
```
New-AzureVMConfig [-Name] <String> [-InstanceSize] <String> [[-HostCaching] <String>]
 [[-AvailabilitySetName] <String>] [[-Label] <String>] [-ImageName] <String> [[-MediaLocation] <String>]
 [[-DiskLabel] <String>] [-DisableBootDiagnostics] [-LicenseType <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="e33f2-106">DiskName</span><span class="sxs-lookup"><span data-stu-id="e33f2-106">DiskName</span></span>
```
New-AzureVMConfig [-Name] <String> [-InstanceSize] <String> [[-HostCaching] <String>]
 [[-AvailabilitySetName] <String>] [[-Label] <String>] [-DiskName] <String> [-DisableBootDiagnostics]
 [-LicenseType <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e33f2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e33f2-107">DESCRIPTION</span></span>
<span data-ttu-id="e33f2-108">Командлет **New-AzureVMConfig** создает объект конфигурации виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="e33f2-108">The **New-AzureVMConfig** cmdlet creates an Azure  virtual machine configuration object.</span></span>
<span data-ttu-id="e33f2-109">Вы можете использовать этот объект, чтобы выполнить новое развертывание и добавить новую виртуальную машину в существующее развертывание.</span><span class="sxs-lookup"><span data-stu-id="e33f2-109">You can use this object to perform a new deployment and add a new virtual machine to an existing deployment.</span></span>

## <span data-ttu-id="e33f2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e33f2-110">EXAMPLES</span></span>

### <span data-ttu-id="e33f2-111">Пример 1: создание конфигурации виртуальной машины Windows</span><span class="sxs-lookup"><span data-stu-id="e33f2-111">Example 1: Create a Windows virtual machine configuration</span></span>
```
PS C:\> $Image = (Get-AzureVMImage)[4].ImageName 
C:\PS> New-AzureVMConfig -Name "MyVM1" -InstanceSize ExtraSmall -ImageName $Image | Add-AzureProvisioningConfig -Windows -Password $AdminPassword | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "Datadisk1" -LUN 0 | New-AzureVM -ServiceName "MySvc1"
```

<span data-ttu-id="e33f2-112">Эта команда создает конфигурацию виртуальной машины Windows с диском операционной системы, диском данных и конфигурацией подготовки.</span><span class="sxs-lookup"><span data-stu-id="e33f2-112">This command creates a Windows virtual machine configuration with operating system disk, data disk and provisioning configuration.</span></span>
<span data-ttu-id="e33f2-113">Затем эта конфигурация используется для создания новой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e33f2-113">This configuration is then used to create a new virtual machine.</span></span>

### <span data-ttu-id="e33f2-114">Пример 2: создание конфигурации виртуальной машины Linux</span><span class="sxs-lookup"><span data-stu-id="e33f2-114">Example 2: Create a Linux virtual machine configuration</span></span>
```
PS C:\> $Image = (Get-AzureVMImage)[7].ImageName
C:\PS> New-AzureVMConfig -Name "MyVM1" -InstanceSize ExtraSmall -ImageName $Image | Add-AzureProvisioningConfig -Linux -LinuxUser $LinuxUser -Password $AdminPassword | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "Datadisk1" -LUN 0 | New-AzureVM -ServiceName "MySvc1"
```

<span data-ttu-id="e33f2-115">Эта команда создает новую конфигурацию виртуальной машины Linux с диском операционной системы, диском данных и конфигурацией подготовки.</span><span class="sxs-lookup"><span data-stu-id="e33f2-115">This command creates a new Linux virtual machine configuration with operating system disk, data disk and provisioning configuration.</span></span>
<span data-ttu-id="e33f2-116">Затем эта конфигурация используется для создания новой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e33f2-116">This configuration is then used to create a new virtual machine.</span></span>

## <span data-ttu-id="e33f2-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e33f2-117">PARAMETERS</span></span>

### <span data-ttu-id="e33f2-118">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="e33f2-118">-AvailabilitySetName</span></span>
<span data-ttu-id="e33f2-119">Указывает имя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="e33f2-119">Specifies the name of the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e33f2-120">-DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="e33f2-120">-DisableBootDiagnostics</span></span>
<span data-ttu-id="e33f2-121">Указывает, что конфигурация отключает диагностику загрузки.</span><span class="sxs-lookup"><span data-stu-id="e33f2-121">Indicates that the configuration disables boot diagnostics.</span></span>
<span data-ttu-id="e33f2-122">По умолчанию Диагностика загрузки включена на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="e33f2-122">By default, boot diagnostics are enabled on the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e33f2-123">-DiskLabel</span><span class="sxs-lookup"><span data-stu-id="e33f2-123">-DiskLabel</span></span>
<span data-ttu-id="e33f2-124">Указывает метку для диска с операционной системой.</span><span class="sxs-lookup"><span data-stu-id="e33f2-124">Specifies a label for the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: ImageName
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e33f2-125">-DiskName</span><span class="sxs-lookup"><span data-stu-id="e33f2-125">-DiskName</span></span>
<span data-ttu-id="e33f2-126">Указывает имя диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="e33f2-126">Specifies a name for the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: DiskName
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e33f2-127">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="e33f2-127">-HostCaching</span></span>
<span data-ttu-id="e33f2-128">Задает режим кэширования узла для диска с операционной системой.</span><span class="sxs-lookup"><span data-stu-id="e33f2-128">Specifies the host caching mode for the operating system disk.</span></span>

<span data-ttu-id="e33f2-129">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="e33f2-129">Valid values are:</span></span>

- <span data-ttu-id="e33f2-130">Чтения</span><span class="sxs-lookup"><span data-stu-id="e33f2-130">ReadOnly</span></span>
- <span data-ttu-id="e33f2-131">Операцию</span><span class="sxs-lookup"><span data-stu-id="e33f2-131">ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e33f2-132">-ImageName</span><span class="sxs-lookup"><span data-stu-id="e33f2-132">-ImageName</span></span>
<span data-ttu-id="e33f2-133">Указывает имя образа виртуальной машины, который будет использоваться для диска с операционной системой.</span><span class="sxs-lookup"><span data-stu-id="e33f2-133">Specifies the name of the virtual machine image to use for the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: ImageName
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e33f2-134">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e33f2-134">-InformationAction</span></span>
<span data-ttu-id="e33f2-135">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="e33f2-135">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e33f2-136">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e33f2-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e33f2-137">Продолжал</span><span class="sxs-lookup"><span data-stu-id="e33f2-137">Continue</span></span>
- <span data-ttu-id="e33f2-138">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="e33f2-138">Ignore</span></span>
- <span data-ttu-id="e33f2-139">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="e33f2-139">Inquire</span></span>
- <span data-ttu-id="e33f2-140">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e33f2-140">SilentlyContinue</span></span>
- <span data-ttu-id="e33f2-141">Остановить</span><span class="sxs-lookup"><span data-stu-id="e33f2-141">Stop</span></span>
- <span data-ttu-id="e33f2-142">Рвать</span><span class="sxs-lookup"><span data-stu-id="e33f2-142">Suspend</span></span>

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

### <span data-ttu-id="e33f2-143">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e33f2-143">-InformationVariable</span></span>
<span data-ttu-id="e33f2-144">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="e33f2-144">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e33f2-145">-InstanceSize</span><span class="sxs-lookup"><span data-stu-id="e33f2-145">-InstanceSize</span></span>
<span data-ttu-id="e33f2-146">Задает размер экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e33f2-146">Specifies the size of the instance.</span></span>

<span data-ttu-id="e33f2-147">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e33f2-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e33f2-148">ExtraSmall</span><span class="sxs-lookup"><span data-stu-id="e33f2-148">ExtraSmall</span></span>
- <span data-ttu-id="e33f2-149">Малого</span><span class="sxs-lookup"><span data-stu-id="e33f2-149">Small</span></span>
- <span data-ttu-id="e33f2-150">Канал</span><span class="sxs-lookup"><span data-stu-id="e33f2-150">Medium</span></span>
- <span data-ttu-id="e33f2-151">Достаточ</span><span class="sxs-lookup"><span data-stu-id="e33f2-151">Large</span></span>
- <span data-ttu-id="e33f2-152">ExtraLarge</span><span class="sxs-lookup"><span data-stu-id="e33f2-152">ExtraLarge</span></span>
- <span data-ttu-id="e33f2-153">Ячейк</span><span class="sxs-lookup"><span data-stu-id="e33f2-153">A5</span></span>
- <span data-ttu-id="e33f2-154">A6</span><span class="sxs-lookup"><span data-stu-id="e33f2-154">A6</span></span>
- <span data-ttu-id="e33f2-155">Ответ</span><span class="sxs-lookup"><span data-stu-id="e33f2-155">A7</span></span>
- <span data-ttu-id="e33f2-156">A8</span><span class="sxs-lookup"><span data-stu-id="e33f2-156">A8</span></span>
- <span data-ttu-id="e33f2-157">A9</span><span class="sxs-lookup"><span data-stu-id="e33f2-157">A9</span></span>
- <span data-ttu-id="e33f2-158">Basic_A0</span><span class="sxs-lookup"><span data-stu-id="e33f2-158">Basic_A0</span></span>
- <span data-ttu-id="e33f2-159">Basic_A1</span><span class="sxs-lookup"><span data-stu-id="e33f2-159">Basic_A1</span></span>
- <span data-ttu-id="e33f2-160">Basic_A2</span><span class="sxs-lookup"><span data-stu-id="e33f2-160">Basic_A2</span></span>
- <span data-ttu-id="e33f2-161">Basic_A3</span><span class="sxs-lookup"><span data-stu-id="e33f2-161">Basic_A3</span></span>
- <span data-ttu-id="e33f2-162">Basic_A4</span><span class="sxs-lookup"><span data-stu-id="e33f2-162">Basic_A4</span></span>
- <span data-ttu-id="e33f2-163">Standard_D1</span><span class="sxs-lookup"><span data-stu-id="e33f2-163">Standard_D1</span></span>
- <span data-ttu-id="e33f2-164">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="e33f2-164">Standard_D2</span></span>
- <span data-ttu-id="e33f2-165">Standard_D3</span><span class="sxs-lookup"><span data-stu-id="e33f2-165">Standard_D3</span></span>
- <span data-ttu-id="e33f2-166">Standard_D4</span><span class="sxs-lookup"><span data-stu-id="e33f2-166">Standard_D4</span></span>
- <span data-ttu-id="e33f2-167">Standard_D11</span><span class="sxs-lookup"><span data-stu-id="e33f2-167">Standard_D11</span></span>
- <span data-ttu-id="e33f2-168">Standard_D12</span><span class="sxs-lookup"><span data-stu-id="e33f2-168">Standard_D12</span></span>
- <span data-ttu-id="e33f2-169">Standard_D13</span><span class="sxs-lookup"><span data-stu-id="e33f2-169">Standard_D13</span></span>
- <span data-ttu-id="e33f2-170">Standard_D14</span><span class="sxs-lookup"><span data-stu-id="e33f2-170">Standard_D14</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e33f2-171">-Label</span><span class="sxs-lookup"><span data-stu-id="e33f2-171">-Label</span></span>
<span data-ttu-id="e33f2-172">Указывает метку, которую нужно назначить виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="e33f2-172">Specifies a label to assign to the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e33f2-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="e33f2-173">-LicenseType</span></span>
<span data-ttu-id="e33f2-174">Указывает тип лицензии для образа или диска, для которого выполняется локальная лицензия.</span><span class="sxs-lookup"><span data-stu-id="e33f2-174">Specifies the type of license for an image or disk that is licensed on-premises.</span></span>
<span data-ttu-id="e33f2-175">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e33f2-175">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e33f2-176">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="e33f2-176">Windows_Client</span></span>
- <span data-ttu-id="e33f2-177">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="e33f2-177">Windows_Server</span></span> 

<span data-ttu-id="e33f2-178">Указывайте этот параметр только для изображений, которые содержат операционную систему Windows Server.</span><span class="sxs-lookup"><span data-stu-id="e33f2-178">Specify this parameter only for images that contain the Windows Server operating system.</span></span>

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

### <span data-ttu-id="e33f2-179">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="e33f2-179">-MediaLocation</span></span>
<span data-ttu-id="e33f2-180">Указывает место хранения Azure для нового диска виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e33f2-180">Specifies the Azure storage location for the new virtual machine disk.</span></span>

```yaml
Type: String
Parameter Sets: ImageName
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e33f2-181">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e33f2-181">-Name</span></span>
<span data-ttu-id="e33f2-182">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e33f2-182">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e33f2-183">-Profile</span><span class="sxs-lookup"><span data-stu-id="e33f2-183">-Profile</span></span>
<span data-ttu-id="e33f2-184">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e33f2-184">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e33f2-185">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e33f2-185">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e33f2-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e33f2-186">CommonParameters</span></span>
<span data-ttu-id="e33f2-187">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e33f2-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e33f2-188">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e33f2-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e33f2-189">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e33f2-189">INPUTS</span></span>

## <span data-ttu-id="e33f2-190">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e33f2-190">OUTPUTS</span></span>

## <span data-ttu-id="e33f2-191">Пуск</span><span class="sxs-lookup"><span data-stu-id="e33f2-191">NOTES</span></span>

## <span data-ttu-id="e33f2-192">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e33f2-192">RELATED LINKS</span></span>

