---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
ms.openlocfilehash: a738ec606fc982573c4062879e9da4becee43df2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246244"
---
# <span data-ttu-id="40412-101">New-AzDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="40412-101">New-AzDiskUpdateConfig</span></span>

## <span data-ttu-id="40412-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="40412-102">SYNOPSIS</span></span>
<span data-ttu-id="40412-103">Создание настраиваемого объекта обновления диска.</span><span class="sxs-lookup"><span data-stu-id="40412-103">Creates a configurable disk update object.</span></span>

## <span data-ttu-id="40412-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="40412-104">SYNTAX</span></span>

```
New-AzDiskUpdateConfig [[-SkuName] <String>] [-Tier <String>] [-DiskIOPSReadOnly <Int64>]
 [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>] [-NetworkAccessPolicy <String>] [-DiskAccessId <String>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-DiskIOPSReadWrite <Int32>]
 [-DiskMBpsReadWrite <Int32>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40412-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40412-105">DESCRIPTION</span></span>
<span data-ttu-id="40412-106">Командлет **New-AzDiskUpdateConfig** создает настраиваемый объект обновления диска.</span><span class="sxs-lookup"><span data-stu-id="40412-106">The **New-AzDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="40412-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="40412-107">EXAMPLES</span></span>

### <span data-ttu-id="40412-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="40412-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -SkuName Premium_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="40412-109">Первая команда создает локальный пустой объект обновления диска с размером 10 ГБ в Premium_LRS тип учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="40412-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="40412-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="40412-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="40412-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта обновления диска.</span><span class="sxs-lookup"><span data-stu-id="40412-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="40412-112">Последняя команда принимает объект обновления диска и обновляет существующий диск с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="40412-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="40412-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="40412-113">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="40412-114">Эта команда обновляет существующий диск с именем "Disk01" в группе ресурсов "ResourceGroup01" на диск размером 10 ГБ.</span><span class="sxs-lookup"><span data-stu-id="40412-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="40412-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="40412-115">PARAMETERS</span></span>

### <span data-ttu-id="40412-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40412-116">-DefaultProfile</span></span>
<span data-ttu-id="40412-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40412-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40412-118">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="40412-118">-DiskAccessId</span></span>
<span data-ttu-id="40412-119">{{Fill DiskAccessId Description}}</span><span class="sxs-lookup"><span data-stu-id="40412-119">{{ Fill DiskAccessId Description }}</span></span>

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

### <span data-ttu-id="40412-120">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="40412-120">-DiskEncryptionKey</span></span>
<span data-ttu-id="40412-121">Указывает объект ключа шифрования диска на диске.</span><span class="sxs-lookup"><span data-stu-id="40412-121">Specifies the disk encryption key object on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40412-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="40412-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="40412-123">Указывает идентификатор ресурса, установленный для шифрования диска, используемого для включения шифрования на остальных.</span><span class="sxs-lookup"><span data-stu-id="40412-123">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="40412-124">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="40412-124">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="40412-125">Общее количество операций ввода/вывода, которые будут разрешены на всех виртуальных машинах, применяющих общий диск для чтения.</span><span class="sxs-lookup"><span data-stu-id="40412-125">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="40412-126">Одна операция может переключаться между 4 КБ и 256 Кбайт.</span><span class="sxs-lookup"><span data-stu-id="40412-126">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40412-127">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="40412-127">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="40412-128">Количество операций ввода/вывода, разрешенных для этого диска; только устанавливаемые для UltraSSD дисков.</span><span class="sxs-lookup"><span data-stu-id="40412-128">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="40412-129">Одна операция может переключаться между 4 КБ и 256 Кбайт.</span><span class="sxs-lookup"><span data-stu-id="40412-129">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40412-130">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="40412-130">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="40412-131">Общая пропускная способность (Мбит/с), которая будет разрешена на всех виртуальных машинах, применяющих общий диск для чтения.</span><span class="sxs-lookup"><span data-stu-id="40412-131">The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="40412-132">Мбит/с — миллионные байты в секунду – используется нотация ISO с числом степеней 10.</span><span class="sxs-lookup"><span data-stu-id="40412-132">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40412-133">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="40412-133">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="40412-134">Пропускная способность, разрешенная для этого диска; только устанавливаемые для UltraSSD дисков.</span><span class="sxs-lookup"><span data-stu-id="40412-134">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="40412-135">Мбит/с — миллионные байты в секунду – используется нотация ISO с числом степеней 10.</span><span class="sxs-lookup"><span data-stu-id="40412-135">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40412-136">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="40412-136">-DiskSizeGB</span></span>
<span data-ttu-id="40412-137">Задает размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="40412-137">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40412-138">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="40412-138">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="40412-139">Включите параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="40412-139">Enable encryption settings.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40412-140">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="40412-140">-EncryptionType</span></span>
<span data-ttu-id="40412-141">Тип ключа, используемого для шифрования данных диска.</span><span class="sxs-lookup"><span data-stu-id="40412-141">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="40412-142">Доступны следующие значения: "EncryptionAtRestWithPlatformKey", "EncryptionAtRestWithCustomerKey"</span><span class="sxs-lookup"><span data-stu-id="40412-142">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="40412-143">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="40412-143">-KeyEncryptionKey</span></span>
<span data-ttu-id="40412-144">Задает ключ шифрования ключа на диске.</span><span class="sxs-lookup"><span data-stu-id="40412-144">Specifies the Key encryption key on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40412-145">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="40412-145">-MaxSharesCount</span></span>
<span data-ttu-id="40412-146">Максимальное количество виртуальных машин, которые могут одновременно присоединиться к диску.</span><span class="sxs-lookup"><span data-stu-id="40412-146">The maximum number of VMs that can attach to the disk at the same time.</span></span> <span data-ttu-id="40412-147">Значение больше единицы указывает диск, который можно подключить к нескольким виртуальным машинам одновременно.</span><span class="sxs-lookup"><span data-stu-id="40412-147">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40412-148">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="40412-148">-NetworkAccessPolicy</span></span>
<span data-ttu-id="40412-149">{{Fill NetworkAccessPolicy Description}}</span><span class="sxs-lookup"><span data-stu-id="40412-149">{{ Fill NetworkAccessPolicy Description }}</span></span>

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

### <span data-ttu-id="40412-150">-OsType</span><span class="sxs-lookup"><span data-stu-id="40412-150">-OsType</span></span>
<span data-ttu-id="40412-151">Указывает тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="40412-151">Specifies the OS type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40412-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="40412-152">-SkuName</span></span>
<span data-ttu-id="40412-153">Указывает имя SKU учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="40412-153">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="40412-154">Доступные значения: Standard_LRS, Premium_LRS, StandardSSD_LRS и UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="40412-154">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="40412-155">UltraSSD_LRS можно использовать только с пустым значением для параметра CreateOption.</span><span class="sxs-lookup"><span data-stu-id="40412-155">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40412-156">-Тег</span><span class="sxs-lookup"><span data-stu-id="40412-156">-Tag</span></span>
<span data-ttu-id="40412-157">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="40412-157">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="40412-158">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="40412-158">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40412-159">Уровень</span><span class="sxs-lookup"><span data-stu-id="40412-159">-Tier</span></span>
<span data-ttu-id="40412-160">Уровень производительности диска.</span><span class="sxs-lookup"><span data-stu-id="40412-160">Performance tier of the disk.</span></span>

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

### <span data-ttu-id="40412-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40412-161">-Confirm</span></span>
<span data-ttu-id="40412-162">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="40412-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40412-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40412-163">-WhatIf</span></span>
<span data-ttu-id="40412-164">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="40412-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="40412-165">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="40412-165">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40412-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40412-166">CommonParameters</span></span>
<span data-ttu-id="40412-167">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="40412-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40412-168">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40412-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40412-169">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="40412-169">INPUTS</span></span>

### <span data-ttu-id="40412-170">System. String</span><span class="sxs-lookup"><span data-stu-id="40412-170">System.String</span></span>

### <span data-ttu-id="40412-171">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="40412-171">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="40412-172">System. Int32</span><span class="sxs-lookup"><span data-stu-id="40412-172">System.Int32</span></span>

### <span data-ttu-id="40412-173">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="40412-173">System.Collections.Hashtable</span></span>

### <span data-ttu-id="40412-174">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="40412-174">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="40412-175">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="40412-175">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="40412-176">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="40412-176">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="40412-177">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="40412-177">OUTPUTS</span></span>

### <span data-ttu-id="40412-178">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="40412-178">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="40412-179">Пуск</span><span class="sxs-lookup"><span data-stu-id="40412-179">NOTES</span></span>

## <span data-ttu-id="40412-180">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40412-180">RELATED LINKS</span></span>
