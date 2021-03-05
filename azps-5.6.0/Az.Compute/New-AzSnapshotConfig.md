---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
ms.openlocfilehash: 8407cb1f8968d1e7d9e469b4ca3ccd1cb49742a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007107"
---
# <span data-ttu-id="ae58c-101">New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="ae58c-101">New-AzSnapshotConfig</span></span>

## <span data-ttu-id="ae58c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae58c-102">SYNOPSIS</span></span>
<span data-ttu-id="ae58c-103">Создание настраиваемого объекта моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="ae58c-103">Creates a configurable snapshot object.</span></span>

## <span data-ttu-id="ae58c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ae58c-104">SYNTAX</span></span>

```
New-AzSnapshotConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-HyperVGeneration <String>] [-Incremental] [-Tag <Hashtable>] [-CreateOption <String>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [DiskAccessId <String>]
 [-NetworkAccessPolicy <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae58c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae58c-105">DESCRIPTION</span></span>
<span data-ttu-id="ae58c-106">Для создания настраиваемого объекта снимка создается новый объект **AzSnapshotConfig.**</span><span class="sxs-lookup"><span data-stu-id="ae58c-106">The **New-AzSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="ae58c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ae58c-107">EXAMPLES</span></span>

### <span data-ttu-id="ae58c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ae58c-108">Example 1</span></span>
```powershell
PS C:\> $snapshotconfig = New-AzSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="ae58c-109">Первая команда создает локальный пустой объект моментального снимка размером 5 ГБ Standard_LRS типа учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="ae58c-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="ae58c-110">Она также задает тип ОС Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="ae58c-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="ae58c-111">Вторая и третья команды настраивают параметры ключа шифрования диска и ключа шифрования для объекта моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="ae58c-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="ae58c-112">Последняя команда принимает объект моментального снимка и создает моментальный снимок с именем "Моментальный снимок01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="ae58c-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="ae58c-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ae58c-113">Example 2</span></span>

<span data-ttu-id="ae58c-114">Создание настраиваемого объекта моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="ae58c-114">Creates a configurable snapshot object.</span></span> <span data-ttu-id="ae58c-115">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="ae58c-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzSnapshotConfig -CreateOption Empty -Location 'Central US' -SourceUri 'https://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd'
```

## <span data-ttu-id="ae58c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae58c-116">PARAMETERS</span></span>

### <span data-ttu-id="ae58c-117">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="ae58c-117">-CreateOption</span></span>
<span data-ttu-id="ae58c-118">Указывает, создает ли этот cmdlet диск в виртуальной машине из платформы или изображения пользователя, создает пустой диск или влог существующий диск.</span><span class="sxs-lookup"><span data-stu-id="ae58c-118">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="ae58c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae58c-119">-DefaultProfile</span></span>
<span data-ttu-id="ae58c-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ae58c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae58c-121">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ae58c-121">-DiskEncryptionKey</span></span>
<span data-ttu-id="ae58c-122">Определяет объект ключа шифрования диска для моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="ae58c-122">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="ae58c-123">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="ae58c-123">-DiskEncryptionSetId</span></span>
<span data-ttu-id="ae58c-124">Определяет код ресурса набора шифрования диска, который нужно использовать для включения шифрования во время работы.</span><span class="sxs-lookup"><span data-stu-id="ae58c-124">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="ae58c-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="ae58c-125">-DiskSizeGB</span></span>
<span data-ttu-id="ae58c-126">Определяет размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="ae58c-126">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="ae58c-127">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="ae58c-127">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="ae58c-128">Включить параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="ae58c-128">Enable encryption settings.</span></span>

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

### <span data-ttu-id="ae58c-129">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="ae58c-129">-EncryptionType</span></span>
<span data-ttu-id="ae58c-130">Тип ключа, используемого для шифрования данных диска.</span><span class="sxs-lookup"><span data-stu-id="ae58c-130">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="ae58c-131">Доступны такие значения: EncryptionAtRestWithPlatformKey, 'EncryptionAtRestWithCustomerKey'</span><span class="sxs-lookup"><span data-stu-id="ae58c-131">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="ae58c-132">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="ae58c-132">-DiskAccessId</span></span>
<span data-ttu-id="ae58c-133">Возвращает или ARM для ресурса DiskAccess для использования частных конечных точек.</span><span class="sxs-lookup"><span data-stu-id="ae58c-133">Gets or sets ARM id of the DiskAccess resource for using private endpoints on.</span></span>

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

### <span data-ttu-id="ae58c-134">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ae58c-134">-NetworkAccessPolicy</span></span>
<span data-ttu-id="ae58c-135">Политика доступа к сети определяет политику доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="ae58c-135">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="ae58c-136">Возможные значения: 'AllowAll', 'AllowPrivate', 'DenyAll'</span><span class="sxs-lookup"><span data-stu-id="ae58c-136">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

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

### <span data-ttu-id="ae58c-137">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="ae58c-137">-HyperVGeneration</span></span>
<span data-ttu-id="ae58c-138">Генерация гипервизора виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ae58c-138">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="ae58c-139">Применимо только к дискам ОС.</span><span class="sxs-lookup"><span data-stu-id="ae58c-139">Applicable to OS disks only.</span></span>  <span data-ttu-id="ae58c-140">Допустимые значения: V1 и V2.</span><span class="sxs-lookup"><span data-stu-id="ae58c-140">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="ae58c-141">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="ae58c-141">-ImageReference</span></span>
<span data-ttu-id="ae58c-142">Указывает ссылку на изображение на моментальный снимок.</span><span class="sxs-lookup"><span data-stu-id="ae58c-142">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="ae58c-143">-Incremental</span><span class="sxs-lookup"><span data-stu-id="ae58c-143">-Incremental</span></span>
<span data-ttu-id="ae58c-144">Определяет добавоальный моментальный снимок.</span><span class="sxs-lookup"><span data-stu-id="ae58c-144">Specifies an incremental snapshot.</span></span> <span data-ttu-id="ae58c-145">Добавоонные моментальные снимки на одном диске занимают меньше места, чем полные снимки, и их можно заохиметь.</span><span class="sxs-lookup"><span data-stu-id="ae58c-145">Incremental snapshots on the same disk occupy less space than full snapshots and can be diffed.</span></span>

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

### <span data-ttu-id="ae58c-146">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ae58c-146">-KeyEncryptionKey</span></span>
<span data-ttu-id="ae58c-147">Указывает ключ шифрования ключа для моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="ae58c-147">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="ae58c-148">-Location</span><span class="sxs-lookup"><span data-stu-id="ae58c-148">-Location</span></span>
<span data-ttu-id="ae58c-149">Определяет расположение.</span><span class="sxs-lookup"><span data-stu-id="ae58c-149">Specifies a location.</span></span>

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

### <span data-ttu-id="ae58c-150">-OsType</span><span class="sxs-lookup"><span data-stu-id="ae58c-150">-OsType</span></span>
<span data-ttu-id="ae58c-151">Тип ОС.</span><span class="sxs-lookup"><span data-stu-id="ae58c-151">Specifies the OS type.</span></span>

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

### <span data-ttu-id="ae58c-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ae58c-152">-SkuName</span></span>
<span data-ttu-id="ae58c-153">Указывает имя SKU учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="ae58c-153">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="ae58c-154">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="ae58c-154">-SourceResourceId</span></span>
<span data-ttu-id="ae58c-155">Определяет код источника ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ae58c-155">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="ae58c-156">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="ae58c-156">-SourceUri</span></span>
<span data-ttu-id="ae58c-157">Определяет исходный URI.</span><span class="sxs-lookup"><span data-stu-id="ae58c-157">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="ae58c-158">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="ae58c-158">-StorageAccountId</span></span>
<span data-ttu-id="ae58c-159">Определяет ИД учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="ae58c-159">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="ae58c-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="ae58c-160">-Tag</span></span>
<span data-ttu-id="ae58c-161">Пары "ключевое значение" в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="ae58c-161">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ae58c-162">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="ae58c-162">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ae58c-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae58c-163">-Confirm</span></span>
<span data-ttu-id="ae58c-164">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae58c-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae58c-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae58c-165">-WhatIf</span></span>
<span data-ttu-id="ae58c-166">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae58c-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae58c-167">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ae58c-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae58c-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae58c-168">CommonParameters</span></span>
<span data-ttu-id="ae58c-169">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae58c-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae58c-170">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae58c-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae58c-171">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ae58c-171">INPUTS</span></span>

### <span data-ttu-id="ae58c-172">System.String</span><span class="sxs-lookup"><span data-stu-id="ae58c-172">System.String</span></span>

### <span data-ttu-id="ae58c-173">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ae58c-173">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="ae58c-174">System.Int32</span><span class="sxs-lookup"><span data-stu-id="ae58c-174">System.Int32</span></span>

### <span data-ttu-id="ae58c-175">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ae58c-175">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ae58c-176">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="ae58c-176">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="ae58c-177">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ae58c-177">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ae58c-178">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="ae58c-178">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="ae58c-179">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="ae58c-179">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="ae58c-180">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ae58c-180">OUTPUTS</span></span>

### <span data-ttu-id="ae58c-181">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="ae58c-181">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="ae58c-182">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ae58c-182">NOTES</span></span>

## <span data-ttu-id="ae58c-183">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae58c-183">RELATED LINKS</span></span>
