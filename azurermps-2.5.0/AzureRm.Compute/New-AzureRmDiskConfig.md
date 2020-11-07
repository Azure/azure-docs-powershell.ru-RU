---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermdiskconfig
schema: 2.0.0
ms.openlocfilehash: 8249bbb354d660f335316da503b0f19b6576fea6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913912"
---
# <span data-ttu-id="6ff16-101">New-AzureRmDiskConfig</span><span class="sxs-lookup"><span data-stu-id="6ff16-101">New-AzureRmDiskConfig</span></span>

## <span data-ttu-id="6ff16-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6ff16-102">SYNOPSIS</span></span>
<span data-ttu-id="6ff16-103">Создание настраиваемого объекта диска.</span><span class="sxs-lookup"><span data-stu-id="6ff16-103">Creates a configurable disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ff16-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6ff16-104">SYNTAX</span></span>

```
New-AzureRmDiskConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Zone <String[]>] [-Tag <Hashtable>]
 [-CreateOption <DiskCreateOption>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-SourceUri <String>] [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ff16-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ff16-105">DESCRIPTION</span></span>
<span data-ttu-id="6ff16-106">Командлет **New-AzureRmDiskConfig** создает настраиваемый объект диска.</span><span class="sxs-lookup"><span data-stu-id="6ff16-106">The **New-AzureRmDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="6ff16-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6ff16-107">EXAMPLES</span></span>

### <span data-ttu-id="6ff16-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6ff16-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzureRmDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzureRmDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="6ff16-109">Первая команда создает локальный пустой объект диска с размером 5GB в Standard_LRS типе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="6ff16-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="6ff16-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="6ff16-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="6ff16-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта диска.</span><span class="sxs-lookup"><span data-stu-id="6ff16-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="6ff16-112">Последняя команда принимает объект диска и создает диск с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="6ff16-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="6ff16-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6ff16-113">PARAMETERS</span></span>

### <span data-ttu-id="6ff16-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="6ff16-114">-CreateOption</span></span>
<span data-ttu-id="6ff16-115">Указывает, создает ли этот командлет диск на виртуальной машине из платформы или пользовательского образа, создает пустой диск или прикрепляет существующий диск.</span><span class="sxs-lookup"><span data-stu-id="6ff16-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="6ff16-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ff16-116">-DefaultProfile</span></span>
<span data-ttu-id="6ff16-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6ff16-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ff16-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="6ff16-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="6ff16-119">Указывает объект ключа шифрования диска на диске.</span><span class="sxs-lookup"><span data-stu-id="6ff16-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="6ff16-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="6ff16-120">-DiskSizeGB</span></span>
<span data-ttu-id="6ff16-121">Задает размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="6ff16-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="6ff16-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="6ff16-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="6ff16-123">Включите параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="6ff16-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="6ff16-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="6ff16-124">-ImageReference</span></span>
<span data-ttu-id="6ff16-125">Указывает ссылку на изображение на диске.</span><span class="sxs-lookup"><span data-stu-id="6ff16-125">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="6ff16-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="6ff16-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="6ff16-127">Задает ключ шифрования ключа на диске.</span><span class="sxs-lookup"><span data-stu-id="6ff16-127">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="6ff16-128">-Location</span><span class="sxs-lookup"><span data-stu-id="6ff16-128">-Location</span></span>
<span data-ttu-id="6ff16-129">Задает расположение.</span><span class="sxs-lookup"><span data-stu-id="6ff16-129">Specifies a location.</span></span>

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

### <span data-ttu-id="6ff16-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="6ff16-130">-OsType</span></span>
<span data-ttu-id="6ff16-131">Указывает тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="6ff16-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="6ff16-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="6ff16-132">-SkuName</span></span>
<span data-ttu-id="6ff16-133">Указывает имя SKU учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="6ff16-133">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="6ff16-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="6ff16-134">-SourceResourceId</span></span>
<span data-ttu-id="6ff16-135">Указывает исходный идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="6ff16-135">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="6ff16-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="6ff16-136">-SourceUri</span></span>
<span data-ttu-id="6ff16-137">Указывает универсальный код ресурса (URI) источника.</span><span class="sxs-lookup"><span data-stu-id="6ff16-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="6ff16-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="6ff16-138">-StorageAccountId</span></span>
<span data-ttu-id="6ff16-139">Указывает идентификатор учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="6ff16-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="6ff16-140">-Тег</span><span class="sxs-lookup"><span data-stu-id="6ff16-140">-Tag</span></span>
<span data-ttu-id="6ff16-141">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="6ff16-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6ff16-142">Например:</span><span class="sxs-lookup"><span data-stu-id="6ff16-142">For example:</span></span>

<span data-ttu-id="6ff16-143">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="6ff16-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6ff16-144">-Zone</span><span class="sxs-lookup"><span data-stu-id="6ff16-144">-Zone</span></span>
<span data-ttu-id="6ff16-145">Указывает список логических зон для диска.</span><span class="sxs-lookup"><span data-stu-id="6ff16-145">Specifies the logical zone list for Disk.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ff16-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ff16-146">-Confirm</span></span>
<span data-ttu-id="6ff16-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6ff16-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ff16-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ff16-148">-WhatIf</span></span>
<span data-ttu-id="6ff16-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6ff16-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ff16-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6ff16-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ff16-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ff16-151">CommonParameters</span></span>
<span data-ttu-id="6ff16-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6ff16-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ff16-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ff16-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ff16-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6ff16-154">INPUTS</span></span>

### <span data-ttu-id="6ff16-155">Ничего</span><span class="sxs-lookup"><span data-stu-id="6ff16-155">None</span></span>
<span data-ttu-id="6ff16-156">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="6ff16-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6ff16-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ff16-157">OUTPUTS</span></span>

### <span data-ttu-id="6ff16-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="6ff16-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="6ff16-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="6ff16-159">NOTES</span></span>

## <span data-ttu-id="6ff16-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6ff16-160">RELATED LINKS</span></span>

