---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
ms.openlocfilehash: a738ec606fc982573c4062879e9da4becee43df2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394900"
---
# <span data-ttu-id="c28c9-101">New-AzDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="c28c9-101">New-AzDiskUpdateConfig</span></span>

## <span data-ttu-id="c28c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c28c9-102">SYNOPSIS</span></span>
<span data-ttu-id="c28c9-103">Создание настраиваемого объекта обновления диска.</span><span class="sxs-lookup"><span data-stu-id="c28c9-103">Creates a configurable disk update object.</span></span>

## <span data-ttu-id="c28c9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c28c9-104">SYNTAX</span></span>

```
New-AzDiskUpdateConfig [[-SkuName] <String>] [-Tier <String>] [-DiskIOPSReadOnly <Int64>]
 [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>] [-NetworkAccessPolicy <String>] [-DiskAccessId <String>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-DiskIOPSReadWrite <Int32>]
 [-DiskMBpsReadWrite <Int32>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c28c9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c28c9-105">DESCRIPTION</span></span>
<span data-ttu-id="c28c9-106">Для создания настраиваемого объекта обновления диска создается проектлет **New-AzDiskUpdateConfig.**</span><span class="sxs-lookup"><span data-stu-id="c28c9-106">The **New-AzDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="c28c9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c28c9-107">EXAMPLES</span></span>

### <span data-ttu-id="c28c9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c28c9-108">Example 1</span></span>
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

<span data-ttu-id="c28c9-109">Первая команда создает объект обновления локального пустого диска с размером 10 ГБ Premium_LRS типа учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="c28c9-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="c28c9-110">Она также задает тип ОС Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="c28c9-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="c28c9-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта обновления диска.</span><span class="sxs-lookup"><span data-stu-id="c28c9-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="c28c9-112">Последняя команда принимает объект обновления диска и обновляет существующий диск с именем "Диск01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="c28c9-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="c28c9-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c28c9-113">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="c28c9-114">Эта команда обновляет существующий диск с именем "Диск01" в группе ресурсов "Группа ресурсов01" до размера диска 10 ГБ.</span><span class="sxs-lookup"><span data-stu-id="c28c9-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="c28c9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c28c9-115">PARAMETERS</span></span>

### <span data-ttu-id="c28c9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c28c9-116">-DefaultProfile</span></span>
<span data-ttu-id="c28c9-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c28c9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c28c9-118">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="c28c9-118">-DiskAccessId</span></span>
<span data-ttu-id="c28c9-119">{{ Fill DiskAccessId Description }}</span><span class="sxs-lookup"><span data-stu-id="c28c9-119">{{ Fill DiskAccessId Description }}</span></span>

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

### <span data-ttu-id="c28c9-120">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="c28c9-120">-DiskEncryptionKey</span></span>
<span data-ttu-id="c28c9-121">Определяет объект ключа шифрования диска на диске.</span><span class="sxs-lookup"><span data-stu-id="c28c9-121">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="c28c9-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="c28c9-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="c28c9-123">Определяет код ресурса набора шифрования диска, который нужно использовать для включения шифрования во время работы.</span><span class="sxs-lookup"><span data-stu-id="c28c9-123">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="c28c9-124">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="c28c9-124">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="c28c9-125">Общее количество IOPS, которое будет разрешено для всех ВМ-сообщений, которые имеют общий диск с иконой ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="c28c9-125">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="c28c9-126">Одна операция может передаваться между 4k и 256k bytes.</span><span class="sxs-lookup"><span data-stu-id="c28c9-126">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="c28c9-127">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="c28c9-127">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="c28c9-128">Количество IOPS, разрешенных для этого диска; только для дисков UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="c28c9-128">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="c28c9-129">Одна операция может передаваться между 4k и 256k bytes.</span><span class="sxs-lookup"><span data-stu-id="c28c9-129">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="c28c9-130">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="c28c9-130">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="c28c9-131">Общая пропускная способность (MBPS), которая будет разрешена для всех ВМ-сообщений на общем диске как ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="c28c9-131">The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="c28c9-132">MBps означает миллионыбайт в секунду. В этом случае используется нотация ISO с полномочиями 10.</span><span class="sxs-lookup"><span data-stu-id="c28c9-132">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="c28c9-133">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="c28c9-133">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="c28c9-134">пропускная способность, допустимая для этого диска; только для дисков UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="c28c9-134">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="c28c9-135">MBps означает миллионыбайтов в секунду. В этом случае используется нотация ISO с полномочиями 10.</span><span class="sxs-lookup"><span data-stu-id="c28c9-135">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="c28c9-136">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="c28c9-136">-DiskSizeGB</span></span>
<span data-ttu-id="c28c9-137">Определяет размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="c28c9-137">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="c28c9-138">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="c28c9-138">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="c28c9-139">Включить параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="c28c9-139">Enable encryption settings.</span></span>

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

### <span data-ttu-id="c28c9-140">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="c28c9-140">-EncryptionType</span></span>
<span data-ttu-id="c28c9-141">Тип ключа, используемого для шифрования данных на диске.</span><span class="sxs-lookup"><span data-stu-id="c28c9-141">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="c28c9-142">Доступны такие значения: EncryptionAtRestWithPlatformKey, 'EncryptionAtRestWithCustomerKey'</span><span class="sxs-lookup"><span data-stu-id="c28c9-142">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="c28c9-143">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="c28c9-143">-KeyEncryptionKey</span></span>
<span data-ttu-id="c28c9-144">Указывает ключ шифрования ключа на диске.</span><span class="sxs-lookup"><span data-stu-id="c28c9-144">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="c28c9-145">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="c28c9-145">-MaxSharesCount</span></span>
<span data-ttu-id="c28c9-146">Максимальное количество ВТБ, которые можно одновременно прикрепить к диску.</span><span class="sxs-lookup"><span data-stu-id="c28c9-146">The maximum number of VMs that can attach to the disk at the same time.</span></span> <span data-ttu-id="c28c9-147">Значение больше одного указывает на диск, который может быть одновременно установлен на нескольких ВМ-дисках.</span><span class="sxs-lookup"><span data-stu-id="c28c9-147">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

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

### <span data-ttu-id="c28c9-148">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c28c9-148">-NetworkAccessPolicy</span></span>
<span data-ttu-id="c28c9-149">{{ Fill NetworkAccessPolicy Description }}</span><span class="sxs-lookup"><span data-stu-id="c28c9-149">{{ Fill NetworkAccessPolicy Description }}</span></span>

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

### <span data-ttu-id="c28c9-150">-OsType</span><span class="sxs-lookup"><span data-stu-id="c28c9-150">-OsType</span></span>
<span data-ttu-id="c28c9-151">Тип ОС.</span><span class="sxs-lookup"><span data-stu-id="c28c9-151">Specifies the OS type.</span></span>

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

### <span data-ttu-id="c28c9-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c28c9-152">-SkuName</span></span>
<span data-ttu-id="c28c9-153">Указывает имя SKU учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="c28c9-153">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="c28c9-154">Доступны значения Standard_LRS, Premium_LRS, StandardSSD_LRS и UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="c28c9-154">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="c28c9-155">UltraSSD_LRS можно использовать только с пустым значением для параметра CreateOption.</span><span class="sxs-lookup"><span data-stu-id="c28c9-155">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="c28c9-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="c28c9-156">-Tag</span></span>
<span data-ttu-id="c28c9-157">Пары значений ключа в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="c28c9-157">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c28c9-158">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="c28c9-158">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c28c9-159">-Tier</span><span class="sxs-lookup"><span data-stu-id="c28c9-159">-Tier</span></span>
<span data-ttu-id="c28c9-160">Уровень производительности диска.</span><span class="sxs-lookup"><span data-stu-id="c28c9-160">Performance tier of the disk.</span></span>

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

### <span data-ttu-id="c28c9-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c28c9-161">-Confirm</span></span>
<span data-ttu-id="c28c9-162">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c28c9-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c28c9-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c28c9-163">-WhatIf</span></span>
<span data-ttu-id="c28c9-164">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c28c9-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c28c9-165">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c28c9-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c28c9-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c28c9-166">CommonParameters</span></span>
<span data-ttu-id="c28c9-167">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c28c9-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c28c9-168">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c28c9-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c28c9-169">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c28c9-169">INPUTS</span></span>

### <span data-ttu-id="c28c9-170">System.String</span><span class="sxs-lookup"><span data-stu-id="c28c9-170">System.String</span></span>

### <span data-ttu-id="c28c9-171">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="c28c9-171">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="c28c9-172">System.Int32</span><span class="sxs-lookup"><span data-stu-id="c28c9-172">System.Int32</span></span>

### <span data-ttu-id="c28c9-173">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c28c9-173">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c28c9-174">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c28c9-174">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c28c9-175">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="c28c9-175">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="c28c9-176">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="c28c9-176">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="c28c9-177">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c28c9-177">OUTPUTS</span></span>

### <span data-ttu-id="c28c9-178">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="c28c9-178">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="c28c9-179">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c28c9-179">NOTES</span></span>

## <span data-ttu-id="c28c9-180">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c28c9-180">RELATED LINKS</span></span>
