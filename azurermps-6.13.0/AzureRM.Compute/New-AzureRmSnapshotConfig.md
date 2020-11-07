---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmSnapshotConfig.md
ms.openlocfilehash: 2050536a39c8ebcd5a1269709d25af100cc251b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733002"
---
# <span data-ttu-id="f09cc-101">New-AzureRmSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="f09cc-101">New-AzureRmSnapshotConfig</span></span>

## <span data-ttu-id="f09cc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f09cc-102">SYNOPSIS</span></span>
<span data-ttu-id="f09cc-103">Создание настраиваемого объекта снимка.</span><span class="sxs-lookup"><span data-stu-id="f09cc-103">Creates a configurable snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f09cc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f09cc-104">SYNTAX</span></span>

```
New-AzureRmSnapshotConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f09cc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f09cc-105">DESCRIPTION</span></span>
<span data-ttu-id="f09cc-106">Командлет **New-AzureRmSnapshotConfig** создает настраиваемый объект снимка.</span><span class="sxs-lookup"><span data-stu-id="f09cc-106">The **New-AzureRmSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="f09cc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f09cc-107">EXAMPLES</span></span>

### <span data-ttu-id="f09cc-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f09cc-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzureRmSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzureRmSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="f09cc-109">В первой команде создается локальный пустой объект Snapshot с размером 5GB в Standard_LRS типе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f09cc-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="f09cc-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="f09cc-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="f09cc-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта snapshot.</span><span class="sxs-lookup"><span data-stu-id="f09cc-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="f09cc-112">Последняя команда принимает объект snapshot и создает моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="f09cc-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="f09cc-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f09cc-113">PARAMETERS</span></span>

### <span data-ttu-id="f09cc-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="f09cc-114">-CreateOption</span></span>
<span data-ttu-id="f09cc-115">Указывает, создает ли этот командлет диск на виртуальной машине из платформы или пользовательского образа, создает пустой диск или прикрепляет существующий диск.</span><span class="sxs-lookup"><span data-stu-id="f09cc-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="f09cc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f09cc-116">-DefaultProfile</span></span>
<span data-ttu-id="f09cc-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f09cc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f09cc-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="f09cc-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="f09cc-119">Задает объект ключа шифрования диска для снимка.</span><span class="sxs-lookup"><span data-stu-id="f09cc-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="f09cc-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="f09cc-120">-DiskSizeGB</span></span>
<span data-ttu-id="f09cc-121">Задает размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="f09cc-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="f09cc-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="f09cc-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="f09cc-123">Включите параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="f09cc-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="f09cc-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="f09cc-124">-ImageReference</span></span>
<span data-ttu-id="f09cc-125">Указывает ссылку на изображение в снимке.</span><span class="sxs-lookup"><span data-stu-id="f09cc-125">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="f09cc-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="f09cc-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="f09cc-127">Задает ключ шифрования ключа для снимка.</span><span class="sxs-lookup"><span data-stu-id="f09cc-127">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="f09cc-128">-Location</span><span class="sxs-lookup"><span data-stu-id="f09cc-128">-Location</span></span>
<span data-ttu-id="f09cc-129">Задает расположение.</span><span class="sxs-lookup"><span data-stu-id="f09cc-129">Specifies a location.</span></span>

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

### <span data-ttu-id="f09cc-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="f09cc-130">-OsType</span></span>
<span data-ttu-id="f09cc-131">Указывает тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="f09cc-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="f09cc-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f09cc-132">-SkuName</span></span>
<span data-ttu-id="f09cc-133">Указывает имя SKU учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f09cc-133">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="f09cc-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="f09cc-134">-SourceResourceId</span></span>
<span data-ttu-id="f09cc-135">Указывает исходный идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="f09cc-135">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="f09cc-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="f09cc-136">-SourceUri</span></span>
<span data-ttu-id="f09cc-137">Указывает универсальный код ресурса (URI) источника.</span><span class="sxs-lookup"><span data-stu-id="f09cc-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="f09cc-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f09cc-138">-StorageAccountId</span></span>
<span data-ttu-id="f09cc-139">Указывает идентификатор учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f09cc-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="f09cc-140">-Тег</span><span class="sxs-lookup"><span data-stu-id="f09cc-140">-Tag</span></span>
<span data-ttu-id="f09cc-141">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="f09cc-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f09cc-142">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="f09cc-142">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f09cc-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f09cc-143">-Confirm</span></span>
<span data-ttu-id="f09cc-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f09cc-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f09cc-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f09cc-145">-WhatIf</span></span>
<span data-ttu-id="f09cc-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f09cc-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f09cc-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f09cc-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f09cc-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f09cc-148">CommonParameters</span></span>
<span data-ttu-id="f09cc-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f09cc-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f09cc-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f09cc-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f09cc-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f09cc-151">INPUTS</span></span>

### <span data-ttu-id="f09cc-152">System. String</span><span class="sxs-lookup"><span data-stu-id="f09cc-152">System.String</span></span>

### <span data-ttu-id="f09cc-153">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 21.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="f09cc-153">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="f09cc-154">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f09cc-154">System.Int32</span></span>

### <span data-ttu-id="f09cc-155">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f09cc-155">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f09cc-156">Microsoft. Azure. Management. COMPUTE. Models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="f09cc-156">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="f09cc-157">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f09cc-157">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="f09cc-158">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="f09cc-158">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="f09cc-159">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="f09cc-159">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="f09cc-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f09cc-160">OUTPUTS</span></span>

### <span data-ttu-id="f09cc-161">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="f09cc-161">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="f09cc-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="f09cc-162">NOTES</span></span>

## <span data-ttu-id="f09cc-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f09cc-163">RELATED LINKS</span></span>
