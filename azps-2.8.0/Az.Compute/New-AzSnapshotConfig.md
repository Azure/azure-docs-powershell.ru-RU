---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
ms.openlocfilehash: c42aae31bb525f9da6a2963a945a6244373ac8db
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721832"
---
# <span data-ttu-id="0d7c2-101">New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="0d7c2-101">New-AzSnapshotConfig</span></span>

## <span data-ttu-id="0d7c2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d7c2-102">SYNOPSIS</span></span>
<span data-ttu-id="0d7c2-103">Создание настраиваемого объекта снимка.</span><span class="sxs-lookup"><span data-stu-id="0d7c2-103">Creates a configurable snapshot object.</span></span>

## <span data-ttu-id="0d7c2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d7c2-104">SYNTAX</span></span>

```
New-AzSnapshotConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-HyperVGeneration <String>] [-Incremental] [-Tag <Hashtable>] [-CreateOption <String>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d7c2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d7c2-105">DESCRIPTION</span></span>
<span data-ttu-id="0d7c2-106">Командлет **New-AzSnapshotConfig** создает настраиваемый объект снимка.</span><span class="sxs-lookup"><span data-stu-id="0d7c2-106">The **New-AzSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="0d7c2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d7c2-107">EXAMPLES</span></span>

### <span data-ttu-id="0d7c2-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0d7c2-108">Example 1</span></span>
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

<span data-ttu-id="0d7c2-109">В первой команде создается локальный пустой объект Snapshot с размером 5GB в Standard_LRS типе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0d7c2-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="0d7c2-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="0d7c2-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="0d7c2-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта snapshot.</span><span class="sxs-lookup"><span data-stu-id="0d7c2-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="0d7c2-112">Последняя команда принимает объект snapshot и создает моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="0d7c2-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="0d7c2-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d7c2-113">PARAMETERS</span></span>

### <span data-ttu-id="0d7c2-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="0d7c2-114">-CreateOption</span></span>
<span data-ttu-id="0d7c2-115">Указывает, создает ли этот командлет диск на виртуальной машине из платформы или пользовательского образа, создает пустой диск или прикрепляет существующий диск.</span><span class="sxs-lookup"><span data-stu-id="0d7c2-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="0d7c2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d7c2-116">-DefaultProfile</span></span>
<span data-ttu-id="0d7c2-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0d7c2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d7c2-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="0d7c2-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="0d7c2-119">Задает объект ключа шифрования диска для снимка.</span><span class="sxs-lookup"><span data-stu-id="0d7c2-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="0d7c2-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="0d7c2-120">-DiskSizeGB</span></span>
<span data-ttu-id="0d7c2-121">Задает размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="0d7c2-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="0d7c2-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="0d7c2-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="0d7c2-123">Включите параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="0d7c2-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="0d7c2-124">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="0d7c2-124">-HyperVGeneration</span></span>
<span data-ttu-id="0d7c2-125">Создание гипервизора виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0d7c2-125">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="0d7c2-126">Применимо только к дискам ОС.</span><span class="sxs-lookup"><span data-stu-id="0d7c2-126">Applicable to OS disks only.</span></span>  <span data-ttu-id="0d7c2-127">Допустимые значения: v1 и v2.</span><span class="sxs-lookup"><span data-stu-id="0d7c2-127">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="0d7c2-128">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="0d7c2-128">-ImageReference</span></span>
<span data-ttu-id="0d7c2-129">Указывает ссылку на изображение в снимке.</span><span class="sxs-lookup"><span data-stu-id="0d7c2-129">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="0d7c2-130">-Инкрементное</span><span class="sxs-lookup"><span data-stu-id="0d7c2-130">-Incremental</span></span>
<span data-ttu-id="0d7c2-131">Задает инкрементный снимок.</span><span class="sxs-lookup"><span data-stu-id="0d7c2-131">Specifies an incremental snapshot.</span></span> <span data-ttu-id="0d7c2-132">Добавочные снимки на том же диске занимают меньше места, чем полные снимки, и могут быть непонятными.</span><span class="sxs-lookup"><span data-stu-id="0d7c2-132">Incremental snapshots on the same disk occupy less space than full snapshots and can be diffed.</span></span>

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

### <span data-ttu-id="0d7c2-133">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="0d7c2-133">-KeyEncryptionKey</span></span>
<span data-ttu-id="0d7c2-134">Задает ключ шифрования ключа для снимка.</span><span class="sxs-lookup"><span data-stu-id="0d7c2-134">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="0d7c2-135">-Location</span><span class="sxs-lookup"><span data-stu-id="0d7c2-135">-Location</span></span>
<span data-ttu-id="0d7c2-136">Задает расположение.</span><span class="sxs-lookup"><span data-stu-id="0d7c2-136">Specifies a location.</span></span>

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

### <span data-ttu-id="0d7c2-137">-OsType</span><span class="sxs-lookup"><span data-stu-id="0d7c2-137">-OsType</span></span>
<span data-ttu-id="0d7c2-138">Указывает тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="0d7c2-138">Specifies the OS type.</span></span>

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

### <span data-ttu-id="0d7c2-139">-SkuName</span><span class="sxs-lookup"><span data-stu-id="0d7c2-139">-SkuName</span></span>
<span data-ttu-id="0d7c2-140">Указывает имя SKU учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0d7c2-140">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="0d7c2-141">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="0d7c2-141">-SourceResourceId</span></span>
<span data-ttu-id="0d7c2-142">Указывает исходный идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="0d7c2-142">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="0d7c2-143">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="0d7c2-143">-SourceUri</span></span>
<span data-ttu-id="0d7c2-144">Указывает универсальный код ресурса (URI) источника.</span><span class="sxs-lookup"><span data-stu-id="0d7c2-144">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="0d7c2-145">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="0d7c2-145">-StorageAccountId</span></span>
<span data-ttu-id="0d7c2-146">Указывает идентификатор учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0d7c2-146">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="0d7c2-147">-Тег</span><span class="sxs-lookup"><span data-stu-id="0d7c2-147">-Tag</span></span>
<span data-ttu-id="0d7c2-148">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="0d7c2-148">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0d7c2-149">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="0d7c2-149">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0d7c2-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d7c2-150">-Confirm</span></span>
<span data-ttu-id="0d7c2-151">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0d7c2-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d7c2-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d7c2-152">-WhatIf</span></span>
<span data-ttu-id="0d7c2-153">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0d7c2-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d7c2-154">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0d7c2-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d7c2-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d7c2-155">CommonParameters</span></span>
<span data-ttu-id="0d7c2-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d7c2-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d7c2-157">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d7c2-157">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d7c2-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d7c2-158">INPUTS</span></span>

### <span data-ttu-id="0d7c2-159">System. String</span><span class="sxs-lookup"><span data-stu-id="0d7c2-159">System.String</span></span>

### <span data-ttu-id="0d7c2-160">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="0d7c2-160">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="0d7c2-161">System. Int32</span><span class="sxs-lookup"><span data-stu-id="0d7c2-161">System.Int32</span></span>

### <span data-ttu-id="0d7c2-162">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0d7c2-162">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0d7c2-163">Microsoft. Azure. Management. COMPUTE. Models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="0d7c2-163">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="0d7c2-164">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0d7c2-164">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0d7c2-165">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="0d7c2-165">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="0d7c2-166">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="0d7c2-166">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="0d7c2-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d7c2-167">OUTPUTS</span></span>

### <span data-ttu-id="0d7c2-168">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="0d7c2-168">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="0d7c2-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d7c2-169">NOTES</span></span>

## <span data-ttu-id="0d7c2-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d7c2-170">RELATED LINKS</span></span>
