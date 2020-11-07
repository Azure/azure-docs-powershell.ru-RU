---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermsnapshotconfig
schema: 2.0.0
ms.openlocfilehash: a18eb8513e419d174efac9179cb65fe175d12dd1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914921"
---
# <span data-ttu-id="499a9-101">New-AzureRmSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="499a9-101">New-AzureRmSnapshotConfig</span></span>

## <span data-ttu-id="499a9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="499a9-102">SYNOPSIS</span></span>
<span data-ttu-id="499a9-103">Создание настраиваемого объекта снимка.</span><span class="sxs-lookup"><span data-stu-id="499a9-103">Creates a configurable snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="499a9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="499a9-104">SYNTAX</span></span>

```
New-AzureRmSnapshotConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Tag <Hashtable>] [-CreateOption <DiskCreateOption>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="499a9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="499a9-105">DESCRIPTION</span></span>
<span data-ttu-id="499a9-106">Командлет **New-AzureRmSnapshotConfig** создает настраиваемый объект снимка.</span><span class="sxs-lookup"><span data-stu-id="499a9-106">The **New-AzureRmSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="499a9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="499a9-107">EXAMPLES</span></span>

### <span data-ttu-id="499a9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="499a9-108">Example 1</span></span>
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

<span data-ttu-id="499a9-109">В первой команде создается локальный пустой объект Snapshot с размером 5GB в Standard_LRS типе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="499a9-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="499a9-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="499a9-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="499a9-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта snapshot.</span><span class="sxs-lookup"><span data-stu-id="499a9-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="499a9-112">Последняя команда принимает объект snapshot и создает моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="499a9-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="499a9-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="499a9-113">PARAMETERS</span></span>

### <span data-ttu-id="499a9-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="499a9-114">-CreateOption</span></span>
<span data-ttu-id="499a9-115">Указывает, создает ли этот командлет диск на виртуальной машине из платформы или пользовательского образа, создает пустой диск или прикрепляет существующий диск.</span><span class="sxs-lookup"><span data-stu-id="499a9-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

```yaml
Type: DiskCreateOption
Parameter Sets: (All)
Aliases: 
Accepted values: Empty, Attach, FromImage, Import, Copy

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="499a9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="499a9-116">-DefaultProfile</span></span>
<span data-ttu-id="499a9-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="499a9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="499a9-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="499a9-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="499a9-119">Задает объект ключа шифрования диска для снимка.</span><span class="sxs-lookup"><span data-stu-id="499a9-119">Specifies the disk encryption key object on a snapshot.</span></span>

```yaml
Type: KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="499a9-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="499a9-120">-DiskSizeGB</span></span>
<span data-ttu-id="499a9-121">Задает размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="499a9-121">Specifies the size of the disk in GB.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="499a9-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="499a9-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="499a9-123">Включите параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="499a9-123">Enable encryption settings.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="499a9-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="499a9-124">-ImageReference</span></span>
<span data-ttu-id="499a9-125">Указывает ссылку на изображение в снимке.</span><span class="sxs-lookup"><span data-stu-id="499a9-125">Specifies the image reference on a snapshot.</span></span>

```yaml
Type: ImageDiskReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="499a9-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="499a9-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="499a9-127">Задает ключ шифрования ключа для снимка.</span><span class="sxs-lookup"><span data-stu-id="499a9-127">Specifies the Key encryption key on a snapshot.</span></span>

```yaml
Type: KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="499a9-128">-Location</span><span class="sxs-lookup"><span data-stu-id="499a9-128">-Location</span></span>
<span data-ttu-id="499a9-129">Задает расположение.</span><span class="sxs-lookup"><span data-stu-id="499a9-129">Specifies a location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="499a9-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="499a9-130">-OsType</span></span>
<span data-ttu-id="499a9-131">Указывает тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="499a9-131">Specifies the OS type.</span></span>

```yaml
Type: OperatingSystemTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="499a9-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="499a9-132">-SkuName</span></span>
<span data-ttu-id="499a9-133">Указывает имя SKU учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="499a9-133">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: AccountType
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="499a9-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="499a9-134">-SourceResourceId</span></span>
<span data-ttu-id="499a9-135">Указывает исходный идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="499a9-135">Specifies the source resource ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="499a9-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="499a9-136">-SourceUri</span></span>
<span data-ttu-id="499a9-137">Указывает универсальный код ресурса (URI) источника.</span><span class="sxs-lookup"><span data-stu-id="499a9-137">Specifies the source Uri.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="499a9-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="499a9-138">-StorageAccountId</span></span>
<span data-ttu-id="499a9-139">Указывает идентификатор учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="499a9-139">Specifies the storage account ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="499a9-140">-Тег</span><span class="sxs-lookup"><span data-stu-id="499a9-140">-Tag</span></span>
<span data-ttu-id="499a9-141">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="499a9-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="499a9-142">Например:</span><span class="sxs-lookup"><span data-stu-id="499a9-142">For example:</span></span>

<span data-ttu-id="499a9-143">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="499a9-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="499a9-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="499a9-144">-Confirm</span></span>
<span data-ttu-id="499a9-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="499a9-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="499a9-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="499a9-146">-WhatIf</span></span>
<span data-ttu-id="499a9-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="499a9-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="499a9-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="499a9-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="499a9-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="499a9-149">CommonParameters</span></span>
<span data-ttu-id="499a9-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="499a9-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="499a9-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="499a9-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="499a9-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="499a9-152">INPUTS</span></span>

### <span data-ttu-id="499a9-153">Ничего</span><span class="sxs-lookup"><span data-stu-id="499a9-153">None</span></span>
<span data-ttu-id="499a9-154">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="499a9-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="499a9-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="499a9-155">OUTPUTS</span></span>

### <span data-ttu-id="499a9-156">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="499a9-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="499a9-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="499a9-157">NOTES</span></span>

## <span data-ttu-id="499a9-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="499a9-158">RELATED LINKS</span></span>

