---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshotUpdateConfig.md
ms.openlocfilehash: 00519ec40e4f173c7ecfbb37189835711184f2e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569639"
---
# <span data-ttu-id="f4c63-101">New-AzureRmSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="f4c63-101">New-AzureRmSnapshotUpdateConfig</span></span>

## <span data-ttu-id="f4c63-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f4c63-102">SYNOPSIS</span></span>
<span data-ttu-id="f4c63-103">Создание настраиваемого объекта обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="f4c63-103">Creates a configurable snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4c63-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f4c63-104">SYNTAX</span></span>

```
New-AzureRmSnapshotUpdateConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-CreateOption <DiskCreateOption>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-SourceUri <String>] [-SourceResourceId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4c63-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4c63-105">DESCRIPTION</span></span>
<span data-ttu-id="f4c63-106">Командлет **New-AzureRmSnapshotUpdateConfig** создает настраиваемый объект обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="f4c63-106">The **New-AzureRmSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="f4c63-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f4c63-107">EXAMPLES</span></span>

### <span data-ttu-id="f4c63-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f4c63-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="f4c63-109">Первая команда создает локальный пустой объект обновления моментального снимка с размером 10 ГБ в Premium_LRS типе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f4c63-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="f4c63-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="f4c63-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="f4c63-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="f4c63-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="f4c63-112">Последняя команда принимает объект обновления моментального снимка и обновляет существующий моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="f4c63-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="f4c63-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f4c63-113">Example 2</span></span>
```
PS C:\> New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="f4c63-114">Эта команда обновляет существующий моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01" на диск размером 10 ГБ.</span><span class="sxs-lookup"><span data-stu-id="f4c63-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="f4c63-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f4c63-115">PARAMETERS</span></span>

### <span data-ttu-id="f4c63-116">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="f4c63-116">-CreateOption</span></span>
<span data-ttu-id="f4c63-117">Указывает, создает ли этот командлет снимок на виртуальной машине из платформы или пользовательского образа, создает пустой диск или прикрепляет существующий диск.</span><span class="sxs-lookup"><span data-stu-id="f4c63-117">Specifies whether this cmdlet creates a snapshot in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.DiskCreateOption]
Parameter Sets: (All)
Aliases: 
Accepted values: Empty, Attach, FromImage, Import, Copy

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4c63-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4c63-118">-DefaultProfile</span></span>
<span data-ttu-id="f4c63-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4c63-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4c63-120">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="f4c63-120">-DiskEncryptionKey</span></span>
<span data-ttu-id="f4c63-121">Задает объект ключа шифрования диска для снимка.</span><span class="sxs-lookup"><span data-stu-id="f4c63-121">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="f4c63-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="f4c63-122">-DiskSizeGB</span></span>
<span data-ttu-id="f4c63-123">Задает размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="f4c63-123">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4c63-124">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="f4c63-124">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="f4c63-125">Включите параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="f4c63-125">Enable encryption settings.</span></span>

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

### <span data-ttu-id="f4c63-126">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="f4c63-126">-ImageReference</span></span>
<span data-ttu-id="f4c63-127">Указывает ссылку на изображение в снимке.</span><span class="sxs-lookup"><span data-stu-id="f4c63-127">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="f4c63-128">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="f4c63-128">-KeyEncryptionKey</span></span>
<span data-ttu-id="f4c63-129">Задает ключ шифрования ключа для снимка.</span><span class="sxs-lookup"><span data-stu-id="f4c63-129">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="f4c63-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="f4c63-130">-OsType</span></span>
<span data-ttu-id="f4c63-131">Указывает тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="f4c63-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="f4c63-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f4c63-132">-SkuName</span></span>
<span data-ttu-id="f4c63-133">Указывает имя SKU учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f4c63-133">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes]
Parameter Sets: (All)
Aliases: AccountType
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4c63-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="f4c63-134">-SourceResourceId</span></span>
<span data-ttu-id="f4c63-135">Указывает исходный идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="f4c63-135">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="f4c63-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="f4c63-136">-SourceUri</span></span>
<span data-ttu-id="f4c63-137">Указывает универсальный код ресурса (URI) источника.</span><span class="sxs-lookup"><span data-stu-id="f4c63-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="f4c63-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f4c63-138">-StorageAccountId</span></span>
<span data-ttu-id="f4c63-139">Указывает идентификатор учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f4c63-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="f4c63-140">-Тег</span><span class="sxs-lookup"><span data-stu-id="f4c63-140">-Tag</span></span>
<span data-ttu-id="f4c63-141">Указывает, что ресурсы и группы ресурсов можно пометить с помощью набора пар "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="f4c63-141">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

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

### <span data-ttu-id="f4c63-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4c63-142">-Confirm</span></span>
<span data-ttu-id="f4c63-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f4c63-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4c63-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4c63-144">-WhatIf</span></span>
<span data-ttu-id="f4c63-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f4c63-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4c63-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f4c63-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4c63-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4c63-147">CommonParameters</span></span>
<span data-ttu-id="f4c63-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f4c63-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4c63-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4c63-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4c63-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f4c63-150">INPUTS</span></span>

### <span data-ttu-id="f4c63-151">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. StorageAccountTypes, Microsoft. Azure. Management. COMPUTE, Version = 14.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="f4c63-151">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>
<span data-ttu-id="f4c63-152">System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, культура = нейтраль, PublicKeyToken = b77a5c561934e089]] System. Collections. Hashtable. Nullable `1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.String
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable` 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, культура = нейтраль, PublicKeyToken = b77a5c561934e089]] Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndSecretReference Microsoft. Azure. System. COMPUTE. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="f4c63-152">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.Collections.Hashtable System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.String
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="f4c63-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4c63-153">OUTPUTS</span></span>

### <span data-ttu-id="f4c63-154">Microsoft. Azure. Management. COMPUTE. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="f4c63-154">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="f4c63-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="f4c63-155">NOTES</span></span>

## <span data-ttu-id="f4c63-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4c63-156">RELATED LINKS</span></span>

