---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
ms.openlocfilehash: 2989a5be6ef6eee137f296ab1379931070082fe9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912146"
---
# <span data-ttu-id="a1f23-101">New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="a1f23-101">New-AzSnapshotConfig</span></span>

## <span data-ttu-id="a1f23-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a1f23-102">SYNOPSIS</span></span>
<span data-ttu-id="a1f23-103">Создание настраиваемого объекта снимка.</span><span class="sxs-lookup"><span data-stu-id="a1f23-103">Creates a configurable snapshot object.</span></span>

## <span data-ttu-id="a1f23-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a1f23-104">SYNTAX</span></span>

```
New-AzSnapshotConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-HyperVGeneration <String>] [-Incremental] [-Tag <Hashtable>] [-CreateOption <String>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1f23-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1f23-105">DESCRIPTION</span></span>
<span data-ttu-id="a1f23-106">Командлет **New-AzSnapshotConfig** создает настраиваемый объект снимка.</span><span class="sxs-lookup"><span data-stu-id="a1f23-106">The **New-AzSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="a1f23-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a1f23-107">EXAMPLES</span></span>

### <span data-ttu-id="a1f23-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a1f23-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="a1f23-109">В первой команде создается локальный пустой объект Snapshot с размером 5GB в Standard_LRS типе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="a1f23-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="a1f23-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="a1f23-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="a1f23-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта snapshot.</span><span class="sxs-lookup"><span data-stu-id="a1f23-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="a1f23-112">Последняя команда принимает объект snapshot и создает моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="a1f23-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="a1f23-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a1f23-113">PARAMETERS</span></span>

### <span data-ttu-id="a1f23-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="a1f23-114">-CreateOption</span></span>
<span data-ttu-id="a1f23-115">Указывает, создает ли этот командлет диск на виртуальной машине из платформы или пользовательского образа, создает пустой диск или прикрепляет существующий диск.</span><span class="sxs-lookup"><span data-stu-id="a1f23-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="a1f23-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1f23-116">-DefaultProfile</span></span>
<span data-ttu-id="a1f23-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a1f23-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1f23-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a1f23-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="a1f23-119">Задает объект ключа шифрования диска для снимка.</span><span class="sxs-lookup"><span data-stu-id="a1f23-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="a1f23-120">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="a1f23-120">-DiskEncryptionSetId</span></span>
<span data-ttu-id="a1f23-121">Указывает идентификатор ресурса, установленный для шифрования диска, используемого для включения шифрования на остальных.</span><span class="sxs-lookup"><span data-stu-id="a1f23-121">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="a1f23-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="a1f23-122">-DiskSizeGB</span></span>
<span data-ttu-id="a1f23-123">Задает размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="a1f23-123">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="a1f23-124">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="a1f23-124">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="a1f23-125">Включите параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="a1f23-125">Enable encryption settings.</span></span>

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

### <span data-ttu-id="a1f23-126">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="a1f23-126">-EncryptionType</span></span>
<span data-ttu-id="a1f23-127">Тип ключа, используемого для шифрования данных диска.</span><span class="sxs-lookup"><span data-stu-id="a1f23-127">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="a1f23-128">Доступны следующие значения: "EncryptionAtRestWithPlatformKey", "EncryptionAtRestWithCustomerKey"</span><span class="sxs-lookup"><span data-stu-id="a1f23-128">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="a1f23-129">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="a1f23-129">-HyperVGeneration</span></span>
<span data-ttu-id="a1f23-130">Создание гипервизора виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a1f23-130">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="a1f23-131">Применимо только к дискам ОС.</span><span class="sxs-lookup"><span data-stu-id="a1f23-131">Applicable to OS disks only.</span></span>  <span data-ttu-id="a1f23-132">Допустимые значения: v1 и v2.</span><span class="sxs-lookup"><span data-stu-id="a1f23-132">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="a1f23-133">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="a1f23-133">-ImageReference</span></span>
<span data-ttu-id="a1f23-134">Указывает ссылку на изображение в снимке.</span><span class="sxs-lookup"><span data-stu-id="a1f23-134">Specifies the image reference on a snapshot.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDiskReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1f23-135">-Инкрементное</span><span class="sxs-lookup"><span data-stu-id="a1f23-135">-Incremental</span></span>
<span data-ttu-id="a1f23-136">Задает инкрементный снимок.</span><span class="sxs-lookup"><span data-stu-id="a1f23-136">Specifies an incremental snapshot.</span></span> <span data-ttu-id="a1f23-137">Добавочные снимки на том же диске занимают меньше места, чем полные снимки, и могут быть непонятными.</span><span class="sxs-lookup"><span data-stu-id="a1f23-137">Incremental snapshots on the same disk occupy less space than full snapshots and can be diffed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1f23-138">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a1f23-138">-KeyEncryptionKey</span></span>
<span data-ttu-id="a1f23-139">Задает ключ шифрования ключа для снимка.</span><span class="sxs-lookup"><span data-stu-id="a1f23-139">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="a1f23-140">-Location</span><span class="sxs-lookup"><span data-stu-id="a1f23-140">-Location</span></span>
<span data-ttu-id="a1f23-141">Задает расположение.</span><span class="sxs-lookup"><span data-stu-id="a1f23-141">Specifies a location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1f23-142">-OsType</span><span class="sxs-lookup"><span data-stu-id="a1f23-142">-OsType</span></span>
<span data-ttu-id="a1f23-143">Указывает тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="a1f23-143">Specifies the OS type.</span></span>

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

### <span data-ttu-id="a1f23-144">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a1f23-144">-SkuName</span></span>
<span data-ttu-id="a1f23-145">Указывает имя SKU учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="a1f23-145">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="a1f23-146">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="a1f23-146">-SourceResourceId</span></span>
<span data-ttu-id="a1f23-147">Указывает исходный идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="a1f23-147">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="a1f23-148">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="a1f23-148">-SourceUri</span></span>
<span data-ttu-id="a1f23-149">Указывает универсальный код ресурса (URI) источника.</span><span class="sxs-lookup"><span data-stu-id="a1f23-149">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="a1f23-150">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a1f23-150">-StorageAccountId</span></span>
<span data-ttu-id="a1f23-151">Указывает идентификатор учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="a1f23-151">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="a1f23-152">-Тег</span><span class="sxs-lookup"><span data-stu-id="a1f23-152">-Tag</span></span>
<span data-ttu-id="a1f23-153">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="a1f23-153">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a1f23-154">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="a1f23-154">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1f23-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1f23-155">-Confirm</span></span>
<span data-ttu-id="a1f23-156">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a1f23-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1f23-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1f23-157">-WhatIf</span></span>
<span data-ttu-id="a1f23-158">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a1f23-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1f23-159">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a1f23-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1f23-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1f23-160">CommonParameters</span></span>
<span data-ttu-id="a1f23-161">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a1f23-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1f23-162">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1f23-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1f23-163">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a1f23-163">INPUTS</span></span>

### <span data-ttu-id="a1f23-164">System. String</span><span class="sxs-lookup"><span data-stu-id="a1f23-164">System.String</span></span>

### <span data-ttu-id="a1f23-165">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="a1f23-165">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="a1f23-166">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a1f23-166">System.Int32</span></span>

### <span data-ttu-id="a1f23-167">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a1f23-167">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a1f23-168">Microsoft. Azure. Management. COMPUTE. Models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="a1f23-168">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="a1f23-169">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a1f23-169">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a1f23-170">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="a1f23-170">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="a1f23-171">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="a1f23-171">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="a1f23-172">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1f23-172">OUTPUTS</span></span>

### <span data-ttu-id="a1f23-173">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="a1f23-173">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="a1f23-174">Пуск</span><span class="sxs-lookup"><span data-stu-id="a1f23-174">NOTES</span></span>

## <span data-ttu-id="a1f23-175">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1f23-175">RELATED LINKS</span></span>
