---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzSnapshotConfig.md
ms.openlocfilehash: 1afd1631e398b5726a8e1002b6739fc7ac9b67a8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911468"
---
# <span data-ttu-id="daf5a-101">New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="daf5a-101">New-AzSnapshotConfig</span></span>

## <span data-ttu-id="daf5a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="daf5a-102">SYNOPSIS</span></span>
<span data-ttu-id="daf5a-103">Создание настраиваемого объекта снимка.</span><span class="sxs-lookup"><span data-stu-id="daf5a-103">Creates a configurable snapshot object.</span></span>

## <span data-ttu-id="daf5a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="daf5a-104">SYNTAX</span></span>

```
New-AzSnapshotConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Tag <Hashtable>] [-CreateOption <DiskCreateOption>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="daf5a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="daf5a-105">DESCRIPTION</span></span>
<span data-ttu-id="daf5a-106">Командлет **New-AzSnapshotConfig** создает настраиваемый объект снимка.</span><span class="sxs-lookup"><span data-stu-id="daf5a-106">The **New-AzSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="daf5a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="daf5a-107">EXAMPLES</span></span>

### <span data-ttu-id="daf5a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="daf5a-108">Example 1</span></span>
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

<span data-ttu-id="daf5a-109">В первой команде создается локальный пустой объект Snapshot с размером 5GB в Standard_LRS типе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="daf5a-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="daf5a-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="daf5a-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="daf5a-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта snapshot.</span><span class="sxs-lookup"><span data-stu-id="daf5a-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="daf5a-112">Последняя команда принимает объект snapshot и создает моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="daf5a-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="daf5a-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="daf5a-113">PARAMETERS</span></span>

### <span data-ttu-id="daf5a-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="daf5a-114">-CreateOption</span></span>
<span data-ttu-id="daf5a-115">Указывает, создает ли этот командлет диск на виртуальной машине из платформы или пользовательского образа, создает пустой диск или прикрепляет существующий диск.</span><span class="sxs-lookup"><span data-stu-id="daf5a-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="daf5a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daf5a-116">-DefaultProfile</span></span>
<span data-ttu-id="daf5a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="daf5a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="daf5a-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="daf5a-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="daf5a-119">Задает объект ключа шифрования диска для снимка.</span><span class="sxs-lookup"><span data-stu-id="daf5a-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="daf5a-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="daf5a-120">-DiskSizeGB</span></span>
<span data-ttu-id="daf5a-121">Задает размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="daf5a-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="daf5a-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="daf5a-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="daf5a-123">Включите параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="daf5a-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="daf5a-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="daf5a-124">-ImageReference</span></span>
<span data-ttu-id="daf5a-125">Указывает ссылку на изображение в снимке.</span><span class="sxs-lookup"><span data-stu-id="daf5a-125">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="daf5a-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="daf5a-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="daf5a-127">Задает ключ шифрования ключа для снимка.</span><span class="sxs-lookup"><span data-stu-id="daf5a-127">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="daf5a-128">-Location</span><span class="sxs-lookup"><span data-stu-id="daf5a-128">-Location</span></span>
<span data-ttu-id="daf5a-129">Задает расположение.</span><span class="sxs-lookup"><span data-stu-id="daf5a-129">Specifies a location.</span></span>

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

### <span data-ttu-id="daf5a-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="daf5a-130">-OsType</span></span>
<span data-ttu-id="daf5a-131">Указывает тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="daf5a-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="daf5a-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="daf5a-132">-SkuName</span></span>
<span data-ttu-id="daf5a-133">Указывает имя SKU учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="daf5a-133">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="daf5a-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="daf5a-134">-SourceResourceId</span></span>
<span data-ttu-id="daf5a-135">Указывает исходный идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="daf5a-135">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="daf5a-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="daf5a-136">-SourceUri</span></span>
<span data-ttu-id="daf5a-137">Указывает универсальный код ресурса (URI) источника.</span><span class="sxs-lookup"><span data-stu-id="daf5a-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="daf5a-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="daf5a-138">-StorageAccountId</span></span>
<span data-ttu-id="daf5a-139">Указывает идентификатор учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="daf5a-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="daf5a-140">-Тег</span><span class="sxs-lookup"><span data-stu-id="daf5a-140">-Tag</span></span>
<span data-ttu-id="daf5a-141">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="daf5a-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="daf5a-142">Например:</span><span class="sxs-lookup"><span data-stu-id="daf5a-142">For example:</span></span>

<span data-ttu-id="daf5a-143">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="daf5a-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="daf5a-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="daf5a-144">-Confirm</span></span>
<span data-ttu-id="daf5a-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="daf5a-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="daf5a-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daf5a-146">-WhatIf</span></span>
<span data-ttu-id="daf5a-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="daf5a-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="daf5a-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="daf5a-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="daf5a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daf5a-149">CommonParameters</span></span>
<span data-ttu-id="daf5a-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="daf5a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daf5a-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daf5a-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daf5a-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="daf5a-152">INPUTS</span></span>

### <span data-ttu-id="daf5a-153">Ничего</span><span class="sxs-lookup"><span data-stu-id="daf5a-153">None</span></span>
<span data-ttu-id="daf5a-154">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="daf5a-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="daf5a-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="daf5a-155">OUTPUTS</span></span>

### <span data-ttu-id="daf5a-156">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="daf5a-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="daf5a-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="daf5a-157">NOTES</span></span>

## <span data-ttu-id="daf5a-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="daf5a-158">RELATED LINKS</span></span>

