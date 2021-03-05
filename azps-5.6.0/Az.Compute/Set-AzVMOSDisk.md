---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
ms.openlocfilehash: 07d71e8fa7cd5c19cfc6f4aab8d27e5c5758b41c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998189"
---
# <span data-ttu-id="24bf0-101">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="24bf0-101">Set-AzVMOSDisk</span></span>

## <span data-ttu-id="24bf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24bf0-102">SYNOPSIS</span></span>
<span data-ttu-id="24bf0-103">Задает свойства диска операционной системы на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="24bf0-103">Sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="24bf0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="24bf0-104">SYNTAX</span></span>

### <span data-ttu-id="24bf0-105">DefaultParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="24bf0-105">DefaultParamSet (Default)</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24bf0-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="24bf0-106">WindowsParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24bf0-107">WindowsDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="24bf0-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24bf0-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="24bf0-108">LinuxParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24bf0-109">LinuxDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="24bf0-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24bf0-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="24bf0-110">DESCRIPTION</span></span>
<span data-ttu-id="24bf0-111">**Cmdlet Set-AzVMOSDisk** задает свойства диска операционной системы на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="24bf0-111">The **Set-AzVMOSDisk** cmdlet sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="24bf0-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="24bf0-112">EXAMPLES</span></span>

### <span data-ttu-id="24bf0-113">Пример 1. Настройка свойств на виртуальной машине из изображения платформы</span><span class="sxs-lookup"><span data-stu-id="24bf0-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="24bf0-114">Первая команда получает набор доступности с именем AvailabilitySet13 в группе ресурсов ResourceGroup11, а затем сохраняет этот объект в переменной $AvailabilitySet ресурса.</span><span class="sxs-lookup"><span data-stu-id="24bf0-114">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="24bf0-115">Вторая команда создает объект виртуальной машины, а затем сохраняет его в $VirtualMachine переменной.</span><span class="sxs-lookup"><span data-stu-id="24bf0-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="24bf0-116">Эта команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="24bf0-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="24bf0-117">Виртуальная машину входит в набор доступности, который хранится в $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="24bf0-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="24bf0-118">Конечная команда задает свойства на виртуальной машине в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="24bf0-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="24bf0-119">Пример 2. Задает свойства на виртуальной машине на основе изображения пользователя</span><span class="sxs-lookup"><span data-stu-id="24bf0-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="24bf0-120">Первая команда получает набор доступности с именем AvailabilitySet13 в группе ресурсов ResourceGroup11 и сохраняет этот объект в переменной $AvailabilitySet ресурса.</span><span class="sxs-lookup"><span data-stu-id="24bf0-120">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="24bf0-121">Вторая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="24bf0-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="24bf0-122">Эта команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="24bf0-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="24bf0-123">Виртуальная машину входит в набор доступности, который хранится в $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="24bf0-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="24bf0-124">Конечная команда задает свойства на виртуальной машине в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="24bf0-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="24bf0-125">Пример 3. Задает свойства на виртуальной машине со специализированным изображением пользователя</span><span class="sxs-lookup"><span data-stu-id="24bf0-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="24bf0-126">Первая команда получает набор доступности с именем AvailabilitySet13 в группе ресурсов ResourceGroup11 и сохраняет этот объект в переменной $AvailabilitySet ресурса.</span><span class="sxs-lookup"><span data-stu-id="24bf0-126">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="24bf0-127">Вторая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="24bf0-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="24bf0-128">Эта команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="24bf0-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="24bf0-129">Виртуальная машину входит в набор доступности, который хранится в $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="24bf0-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="24bf0-130">Конечная команда задает свойства на виртуальной машине в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="24bf0-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="24bf0-131">Пример 4. Настройка параметров шифрования диска на диске операционной системы виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="24bf0-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="24bf0-132">В этом примере за устанавливаются параметры шифрования диска на диске операционной системы виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="24bf0-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="24bf0-133">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24bf0-133">PARAMETERS</span></span>

### <span data-ttu-id="24bf0-134">-Кэшинг</span><span class="sxs-lookup"><span data-stu-id="24bf0-134">-Caching</span></span>
<span data-ttu-id="24bf0-135">Определяет режим кэшации диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="24bf0-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="24bf0-136">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="24bf0-136">Valid values are:</span></span> 
- <span data-ttu-id="24bf0-137">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="24bf0-137">ReadOnly</span></span>
- <span data-ttu-id="24bf0-138">Значением по умолчанию readWrite является ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="24bf0-138">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="24bf0-139">Изменение значения кэшинга приводит к перезапуску виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="24bf0-139">Changing the caching value causes the virtual machine to restart.</span></span>
<span data-ttu-id="24bf0-140">Этот параметр влияет на производительность диска.</span><span class="sxs-lookup"><span data-stu-id="24bf0-140">This setting affects the performance of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bf0-141">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="24bf0-141">-CreateOption</span></span>
<span data-ttu-id="24bf0-142">Определяет, создает ли этот cmdlet диск в виртуальной машине из платформы или изображения пользователя либо влог существующий диск.</span><span class="sxs-lookup"><span data-stu-id="24bf0-142">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="24bf0-143">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="24bf0-143">Valid values are:</span></span> 
- <span data-ttu-id="24bf0-144">Вложите.</span><span class="sxs-lookup"><span data-stu-id="24bf0-144">Attach.</span></span>
<span data-ttu-id="24bf0-145">Укажите этот параметр, чтобы создать виртуальную машину на специализированном диске.</span><span class="sxs-lookup"><span data-stu-id="24bf0-145">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="24bf0-146">При указании этого параметра не укажите параметр *SourceImageUri.*</span><span class="sxs-lookup"><span data-stu-id="24bf0-146">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="24bf0-147">Вместо этого используйте Set-AzVMSourceImage.</span><span class="sxs-lookup"><span data-stu-id="24bf0-147">Instead, use the Set-AzVMSourceImage cmdlet.</span></span>
<span data-ttu-id="24bf0-148">Кроме того, с помощью параметров *Windows* или *Linux* необходимо укаймь платформы Azure тип операционной системы на VHD.</span><span class="sxs-lookup"><span data-stu-id="24bf0-148">You must also use the use the *Windows* or *Linux* parameters to tell the azure platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="24bf0-149">Параметр *VhdUri* достаточно для определения расположения диска для вложения на платформе Azure.</span><span class="sxs-lookup"><span data-stu-id="24bf0-149">The *VhdUri* parameter is enough to tell the azure platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="24bf0-150">FromImage.</span><span class="sxs-lookup"><span data-stu-id="24bf0-150">FromImage.</span></span>
<span data-ttu-id="24bf0-151">Укажите этот параметр, чтобы создать виртуальную машину на платформе или обобщенное изображение пользователя.</span><span class="sxs-lookup"><span data-stu-id="24bf0-151">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="24bf0-152">В случае обобщенного изображения пользователя необходимо указать параметр *SourceImageUri,* а также параметры *Windows* или *Linux,* чтобы указать платформе Azure расположение и тип VHD-диска операционной системы вместо использования cmdlet **Set-AzVMSourceImage.**</span><span class="sxs-lookup"><span data-stu-id="24bf0-152">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="24bf0-153">В случае изображения платформы достаточно *параметра VhdUri.*</span><span class="sxs-lookup"><span data-stu-id="24bf0-153">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="24bf0-154">"Пустая".</span><span class="sxs-lookup"><span data-stu-id="24bf0-154">Empty.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bf0-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24bf0-155">-DefaultProfile</span></span>
<span data-ttu-id="24bf0-156">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="24bf0-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bf0-157">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="24bf0-157">-DiffDiskSetting</span></span>
<span data-ttu-id="24bf0-158">Определяет различные параметры диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="24bf0-158">Specifies the differencing disk settings for operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24bf0-159">-DiskEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="24bf0-159">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="24bf0-160">Определяет расположение ключа шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="24bf0-160">Specifies the location of the disk encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: True
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bf0-161">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="24bf0-161">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="24bf0-162">Определяет код ресурса хранилища ключа, содержащего ключ шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="24bf0-162">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: True
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bf0-163">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="24bf0-163">-DiskEncryptionSetId</span></span>
<span data-ttu-id="24bf0-164">Определяет код ресурса для набора шифрования диска, управляемого клиентом.</span><span class="sxs-lookup"><span data-stu-id="24bf0-164">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="24bf0-165">Эта проверка может быть задана только для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="24bf0-165">This can only be specified for managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bf0-166">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="24bf0-166">-DiskSizeInGB</span></span>
<span data-ttu-id="24bf0-167">Определяет размер диска операционной системы в ГБ.</span><span class="sxs-lookup"><span data-stu-id="24bf0-167">Specifies the size, in GB, of the operating system disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bf0-168">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="24bf0-168">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="24bf0-169">Определяет расположение ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="24bf0-169">Specifies the location of the key encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bf0-170">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="24bf0-170">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="24bf0-171">Определяет код ресурса хранилища ключей, содержащий ключ шифрования.</span><span class="sxs-lookup"><span data-stu-id="24bf0-171">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bf0-172">-Linux</span><span class="sxs-lookup"><span data-stu-id="24bf0-172">-Linux</span></span>
<span data-ttu-id="24bf0-173">Указывает на то, что операционная система на изображении пользователя — Linux.</span><span class="sxs-lookup"><span data-stu-id="24bf0-173">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="24bf0-174">Укажите этот параметр для развертывания виртуальной машины на основе изображений пользователя.</span><span class="sxs-lookup"><span data-stu-id="24bf0-174">Specify this parameter for user image based virtual machine deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LinuxParamSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bf0-175">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="24bf0-175">-ManagedDiskId</span></span>
<span data-ttu-id="24bf0-176">Определяет ИД управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="24bf0-176">Specifies the ID of a managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bf0-177">-Name</span><span class="sxs-lookup"><span data-stu-id="24bf0-177">-Name</span></span>
<span data-ttu-id="24bf0-178">Указывает имя диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="24bf0-178">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OSDiskName, DiskName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bf0-179">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="24bf0-179">-SourceImageUri</span></span>
<span data-ttu-id="24bf0-180">Определяет URI VHD для сценариев использования изображений пользователей.</span><span class="sxs-lookup"><span data-stu-id="24bf0-180">Specifies the URI of the VHD for user image scenarios.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bf0-181">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="24bf0-181">-StorageAccountType</span></span>
<span data-ttu-id="24bf0-182">Определяет тип учетной записи хранения управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="24bf0-182">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bf0-183">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="24bf0-183">-VhdUri</span></span>
<span data-ttu-id="24bf0-184">Указывает URI виртуального жесткого диска (VHD).</span><span class="sxs-lookup"><span data-stu-id="24bf0-184">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>
<span data-ttu-id="24bf0-185">Для виртуальной машины на основе изображений этот параметр определяет VHD-файл, который будет создаваться при указании изображения платформы или изображения пользователя.</span><span class="sxs-lookup"><span data-stu-id="24bf0-185">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="24bf0-186">Это расположение, из которого копируется изображение двоичного большого объекта (BLOB-объекта), чтобы запустить виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="24bf0-186">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>
<span data-ttu-id="24bf0-187">Для сценария загрузки виртуальной машины на диске этот параметр указывает VHD-файл, который используется виртуальной машиной непосредственно для запуска.</span><span class="sxs-lookup"><span data-stu-id="24bf0-187">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OSDiskVhdUri, DiskVhdUri

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bf0-188">-VM</span><span class="sxs-lookup"><span data-stu-id="24bf0-188">-VM</span></span>
<span data-ttu-id="24bf0-189">Определяет объект локальной виртуальной машины, для которого нужно настроить свойства диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="24bf0-189">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="24bf0-190">Чтобы получить объект виртуальной машины, воспользуйтесь Get-AzVM..</span><span class="sxs-lookup"><span data-stu-id="24bf0-190">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24bf0-191">-Windows</span><span class="sxs-lookup"><span data-stu-id="24bf0-191">-Windows</span></span>
<span data-ttu-id="24bf0-192">Указывает на то, что операционная система на изображении пользователя — Windows.</span><span class="sxs-lookup"><span data-stu-id="24bf0-192">Indicates that the operating system on the user image is Windows.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsParamSet, WindowsDiskEncryptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bf0-193">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="24bf0-193">-WriteAccelerator</span></span>
<span data-ttu-id="24bf0-194">Указывает, следует ли включить или отключить WriteAccelerator на диске ОС.</span><span class="sxs-lookup"><span data-stu-id="24bf0-194">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bf0-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24bf0-195">CommonParameters</span></span>
<span data-ttu-id="24bf0-196">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24bf0-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24bf0-197">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24bf0-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24bf0-198">INPUTS</span><span class="sxs-lookup"><span data-stu-id="24bf0-198">INPUTS</span></span>

### <span data-ttu-id="24bf0-199">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="24bf0-199">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="24bf0-200">System.String</span><span class="sxs-lookup"><span data-stu-id="24bf0-200">System.String</span></span>

## <span data-ttu-id="24bf0-201">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="24bf0-201">OUTPUTS</span></span>

### <span data-ttu-id="24bf0-202">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="24bf0-202">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="24bf0-203">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="24bf0-203">NOTES</span></span>

## <span data-ttu-id="24bf0-204">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="24bf0-204">RELATED LINKS</span></span>

[<span data-ttu-id="24bf0-205">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="24bf0-205">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="24bf0-206">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="24bf0-206">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="24bf0-207">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="24bf0-207">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


