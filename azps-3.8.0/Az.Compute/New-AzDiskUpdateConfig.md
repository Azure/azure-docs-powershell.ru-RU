---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
ms.openlocfilehash: f6c60538062f39f15e37773604aee302793134f1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065933"
---
# <span data-ttu-id="94937-101">New-AzDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="94937-101">New-AzDiskUpdateConfig</span></span>

## <span data-ttu-id="94937-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="94937-102">SYNOPSIS</span></span>
<span data-ttu-id="94937-103">Создание настраиваемого объекта обновления диска.</span><span class="sxs-lookup"><span data-stu-id="94937-103">Creates a configurable disk update object.</span></span>

## <span data-ttu-id="94937-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="94937-104">SYNTAX</span></span>

```
New-AzDiskUpdateConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Tag] <Hashtable>] [-DiskIOPSReadWrite <Int32>] [-DiskMBpsReadWrite <Int32>]
 [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DiskEncryptionSetId <String>] [-EncryptionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94937-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94937-105">DESCRIPTION</span></span>
<span data-ttu-id="94937-106">Командлет **New-AzDiskUpdateConfig** создает настраиваемый объект обновления диска.</span><span class="sxs-lookup"><span data-stu-id="94937-106">The **New-AzDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="94937-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="94937-107">EXAMPLES</span></span>

### <span data-ttu-id="94937-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="94937-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="94937-109">Первая команда создает локальный пустой объект обновления диска с размером 10 ГБ в Premium_LRS тип учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="94937-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="94937-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="94937-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="94937-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта обновления диска.</span><span class="sxs-lookup"><span data-stu-id="94937-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="94937-112">Последняя команда принимает объект обновления диска и обновляет существующий диск с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="94937-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="94937-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="94937-113">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="94937-114">Эта команда обновляет существующий диск с именем "Disk01" в группе ресурсов "ResourceGroup01" на диск размером 10 ГБ.</span><span class="sxs-lookup"><span data-stu-id="94937-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="94937-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="94937-115">PARAMETERS</span></span>

### <span data-ttu-id="94937-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94937-116">-DefaultProfile</span></span>
<span data-ttu-id="94937-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="94937-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94937-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="94937-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="94937-119">Указывает объект ключа шифрования диска на диске.</span><span class="sxs-lookup"><span data-stu-id="94937-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="94937-120">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="94937-120">-DiskEncryptionSetId</span></span>
<span data-ttu-id="94937-121">Указывает идентификатор ресурса, установленный для шифрования диска, используемого для включения шифрования на остальных.</span><span class="sxs-lookup"><span data-stu-id="94937-121">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="94937-122">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="94937-122">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="94937-123">Количество операций ввода/вывода, разрешенных для этого диска; только устанавливаемые для UltraSSD дисков.</span><span class="sxs-lookup"><span data-stu-id="94937-123">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="94937-124">Одна операция может переключаться между 4 КБ и 256 Кбайт.</span><span class="sxs-lookup"><span data-stu-id="94937-124">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="94937-125">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="94937-125">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="94937-126">Пропускная способность, разрешенная для этого диска; только устанавливаемые для UltraSSD дисков.</span><span class="sxs-lookup"><span data-stu-id="94937-126">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="94937-127">Мбит/с — миллионные байты в секунду – используется нотация ISO с числом степеней 10.</span><span class="sxs-lookup"><span data-stu-id="94937-127">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="94937-128">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="94937-128">-DiskSizeGB</span></span>
<span data-ttu-id="94937-129">Задает размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="94937-129">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="94937-130">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="94937-130">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="94937-131">Включите параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="94937-131">Enable encryption settings.</span></span>

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

### <span data-ttu-id="94937-132">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="94937-132">-EncryptionType</span></span>
<span data-ttu-id="94937-133">Тип ключа, используемого для шифрования данных диска.</span><span class="sxs-lookup"><span data-stu-id="94937-133">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="94937-134">Доступны следующие значения: "EncryptionAtRestWithPlatformKey", "EncryptionAtRestWithCustomerKey"</span><span class="sxs-lookup"><span data-stu-id="94937-134">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="94937-135">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="94937-135">-KeyEncryptionKey</span></span>
<span data-ttu-id="94937-136">Задает ключ шифрования ключа на диске.</span><span class="sxs-lookup"><span data-stu-id="94937-136">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="94937-137">-OsType</span><span class="sxs-lookup"><span data-stu-id="94937-137">-OsType</span></span>
<span data-ttu-id="94937-138">Указывает тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="94937-138">Specifies the OS type.</span></span>

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

### <span data-ttu-id="94937-139">-SkuName</span><span class="sxs-lookup"><span data-stu-id="94937-139">-SkuName</span></span>
<span data-ttu-id="94937-140">Указывает имя SKU учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="94937-140">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="94937-141">Доступные значения: Standard_LRS, Premium_LRS, StandardSSD_LRS и UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="94937-141">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="94937-142">UltraSSD_LRS можно использовать только с пустым значением для параметра CreateOption.</span><span class="sxs-lookup"><span data-stu-id="94937-142">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="94937-143">-Тег</span><span class="sxs-lookup"><span data-stu-id="94937-143">-Tag</span></span>
<span data-ttu-id="94937-144">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="94937-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="94937-145">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="94937-145">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="94937-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94937-146">-Confirm</span></span>
<span data-ttu-id="94937-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="94937-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94937-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94937-148">-WhatIf</span></span>
<span data-ttu-id="94937-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="94937-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94937-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="94937-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94937-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94937-151">CommonParameters</span></span>
<span data-ttu-id="94937-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="94937-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94937-153">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94937-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94937-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="94937-154">INPUTS</span></span>

### <span data-ttu-id="94937-155">System. String</span><span class="sxs-lookup"><span data-stu-id="94937-155">System.String</span></span>

### <span data-ttu-id="94937-156">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="94937-156">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="94937-157">System. Int32</span><span class="sxs-lookup"><span data-stu-id="94937-157">System.Int32</span></span>

### <span data-ttu-id="94937-158">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="94937-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="94937-159">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="94937-159">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="94937-160">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="94937-160">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="94937-161">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="94937-161">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="94937-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="94937-162">OUTPUTS</span></span>

### <span data-ttu-id="94937-163">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="94937-163">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="94937-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="94937-164">NOTES</span></span>

## <span data-ttu-id="94937-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94937-165">RELATED LINKS</span></span>
