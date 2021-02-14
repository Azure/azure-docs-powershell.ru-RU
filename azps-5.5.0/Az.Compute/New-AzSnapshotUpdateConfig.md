---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
ms.openlocfilehash: 1a90a1ff260d143cf4df52ad160b4c05e781bd2e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244096"
---
# <span data-ttu-id="75c44-101">New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="75c44-101">New-AzSnapshotUpdateConfig</span></span>

## <span data-ttu-id="75c44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75c44-102">SYNOPSIS</span></span>
<span data-ttu-id="75c44-103">Создает настраиваемый объект обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="75c44-103">Creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="75c44-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="75c44-104">SYNTAX</span></span>

```
New-AzSnapshotUpdateConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DiskEncryptionSetId <String>] [-EncryptionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75c44-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75c44-105">DESCRIPTION</span></span>
<span data-ttu-id="75c44-106">Для создания настраиваемого объекта обновления моментального снимка создается новый объект **AzSnapshotUpdateConfig.**</span><span class="sxs-lookup"><span data-stu-id="75c44-106">The **New-AzSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="75c44-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="75c44-107">EXAMPLES</span></span>

### <span data-ttu-id="75c44-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="75c44-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="75c44-109">Первая команда создает локальный пустой объект обновления моментального снимка с размером 10 ГБ Premium_LRS типа учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="75c44-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="75c44-110">Она также задает тип ос Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="75c44-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="75c44-111">Вторая и третья команды настраивают параметры ключа шифрования диска и ключа шифрования для объекта обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="75c44-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span> <span data-ttu-id="75c44-112">Последняя команда принимает объект обновления моментального снимка и обновляет существующий моментальный снимок с именем "Снимок01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="75c44-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="75c44-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="75c44-113">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="75c44-114">Эта команда обновляет существующий моментальный снимок с именем "Моментальный снимок01" в группе ресурсов "Группа ресурсов01" до размера диска 10 ГБ.</span><span class="sxs-lookup"><span data-stu-id="75c44-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="75c44-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75c44-115">PARAMETERS</span></span>

### <span data-ttu-id="75c44-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75c44-116">-DefaultProfile</span></span>
<span data-ttu-id="75c44-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="75c44-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75c44-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="75c44-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="75c44-119">Определяет объект ключа шифрования диска для моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="75c44-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="75c44-120">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="75c44-120">-DiskEncryptionSetId</span></span>
<span data-ttu-id="75c44-121">Определяет код ресурса набора шифрования диска, который нужно использовать для включения шифрования во время работы.</span><span class="sxs-lookup"><span data-stu-id="75c44-121">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="75c44-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="75c44-122">-DiskSizeGB</span></span>
<span data-ttu-id="75c44-123">Определяет размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="75c44-123">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="75c44-124">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="75c44-124">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="75c44-125">Включить параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="75c44-125">Enable encryption settings.</span></span>

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

### <span data-ttu-id="75c44-126">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="75c44-126">-EncryptionType</span></span>
<span data-ttu-id="75c44-127">Тип ключа, используемого для шифрования данных диска.</span><span class="sxs-lookup"><span data-stu-id="75c44-127">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="75c44-128">Доступны такие значения: EncryptionAtRestWithPlatformKey, 'EncryptionAtRestWithCustomerKey'</span><span class="sxs-lookup"><span data-stu-id="75c44-128">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="75c44-129">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="75c44-129">-KeyEncryptionKey</span></span>
<span data-ttu-id="75c44-130">Указывает ключ шифрования ключа для моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="75c44-130">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="75c44-131">-OsType</span><span class="sxs-lookup"><span data-stu-id="75c44-131">-OsType</span></span>
<span data-ttu-id="75c44-132">Тип ОС.</span><span class="sxs-lookup"><span data-stu-id="75c44-132">Specifies the OS type.</span></span>

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

### <span data-ttu-id="75c44-133">-SkuName</span><span class="sxs-lookup"><span data-stu-id="75c44-133">-SkuName</span></span>
<span data-ttu-id="75c44-134">Указывает имя SKU учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="75c44-134">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="75c44-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="75c44-135">-Tag</span></span>
<span data-ttu-id="75c44-136">Пары "ключевое значение" в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="75c44-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="75c44-137">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="75c44-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="75c44-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75c44-138">-Confirm</span></span>
<span data-ttu-id="75c44-139">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75c44-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75c44-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75c44-140">-WhatIf</span></span>
<span data-ttu-id="75c44-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75c44-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75c44-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="75c44-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75c44-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75c44-143">CommonParameters</span></span>
<span data-ttu-id="75c44-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75c44-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75c44-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75c44-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75c44-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75c44-146">INPUTS</span></span>

### <span data-ttu-id="75c44-147">System.String</span><span class="sxs-lookup"><span data-stu-id="75c44-147">System.String</span></span>

### <span data-ttu-id="75c44-148">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="75c44-148">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="75c44-149">System.Int32</span><span class="sxs-lookup"><span data-stu-id="75c44-149">System.Int32</span></span>

### <span data-ttu-id="75c44-150">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="75c44-150">System.Collections.Hashtable</span></span>

### <span data-ttu-id="75c44-151">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="75c44-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="75c44-152">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="75c44-152">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="75c44-153">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="75c44-153">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="75c44-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="75c44-154">OUTPUTS</span></span>

### <span data-ttu-id="75c44-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="75c44-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="75c44-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="75c44-156">NOTES</span></span>

## <span data-ttu-id="75c44-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75c44-157">RELATED LINKS</span></span>
