---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
ms.openlocfilehash: 795f7392015ff2fd5085265b6b4da83300dad64e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721854"
---
# <span data-ttu-id="a09e8-101">New-AzDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="a09e8-101">New-AzDiskUpdateConfig</span></span>

## <span data-ttu-id="a09e8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a09e8-102">SYNOPSIS</span></span>
<span data-ttu-id="a09e8-103">Создание настраиваемого объекта обновления диска.</span><span class="sxs-lookup"><span data-stu-id="a09e8-103">Creates a configurable disk update object.</span></span>

## <span data-ttu-id="a09e8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a09e8-104">SYNTAX</span></span>

```
New-AzDiskUpdateConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Tag] <Hashtable>] [-DiskIOPSReadWrite <Int32>] [-DiskMBpsReadWrite <Int32>]
 [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a09e8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a09e8-105">DESCRIPTION</span></span>
<span data-ttu-id="a09e8-106">Командлет **New-AzDiskUpdateConfig** создает настраиваемый объект обновления диска.</span><span class="sxs-lookup"><span data-stu-id="a09e8-106">The **New-AzDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="a09e8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a09e8-107">EXAMPLES</span></span>

### <span data-ttu-id="a09e8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a09e8-108">Example 1</span></span>
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

<span data-ttu-id="a09e8-109">Первая команда создает локальный пустой объект обновления диска с размером 10 ГБ в Premium_LRS тип учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="a09e8-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="a09e8-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="a09e8-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="a09e8-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта обновления диска.</span><span class="sxs-lookup"><span data-stu-id="a09e8-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="a09e8-112">Последняя команда принимает объект обновления диска и обновляет существующий диск с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="a09e8-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="a09e8-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a09e8-113">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="a09e8-114">Эта команда обновляет существующий диск с именем "Disk01" в группе ресурсов "ResourceGroup01" на диск размером 10 ГБ.</span><span class="sxs-lookup"><span data-stu-id="a09e8-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="a09e8-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a09e8-115">PARAMETERS</span></span>

### <span data-ttu-id="a09e8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a09e8-116">-DefaultProfile</span></span>
<span data-ttu-id="a09e8-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a09e8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a09e8-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a09e8-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="a09e8-119">Указывает объект ключа шифрования диска на диске.</span><span class="sxs-lookup"><span data-stu-id="a09e8-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="a09e8-120">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="a09e8-120">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="a09e8-121">Количество операций ввода/вывода, разрешенных для этого диска; только устанавливаемые для UltraSSD дисков.</span><span class="sxs-lookup"><span data-stu-id="a09e8-121">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="a09e8-122">Одна операция может переключаться между 4 КБ и 256 Кбайт.</span><span class="sxs-lookup"><span data-stu-id="a09e8-122">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="a09e8-123">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="a09e8-123">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="a09e8-124">Пропускная способность, разрешенная для этого диска; только устанавливаемые для UltraSSD дисков.</span><span class="sxs-lookup"><span data-stu-id="a09e8-124">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="a09e8-125">Мбит/с — миллионные байты в секунду – используется нотация ISO с числом степеней 10.</span><span class="sxs-lookup"><span data-stu-id="a09e8-125">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="a09e8-126">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="a09e8-126">-DiskSizeGB</span></span>
<span data-ttu-id="a09e8-127">Задает размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="a09e8-127">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="a09e8-128">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="a09e8-128">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="a09e8-129">Включите параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="a09e8-129">Enable encryption settings.</span></span>

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

### <span data-ttu-id="a09e8-130">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a09e8-130">-KeyEncryptionKey</span></span>
<span data-ttu-id="a09e8-131">Задает ключ шифрования ключа на диске.</span><span class="sxs-lookup"><span data-stu-id="a09e8-131">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="a09e8-132">-OsType</span><span class="sxs-lookup"><span data-stu-id="a09e8-132">-OsType</span></span>
<span data-ttu-id="a09e8-133">Указывает тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="a09e8-133">Specifies the OS type.</span></span>

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

### <span data-ttu-id="a09e8-134">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a09e8-134">-SkuName</span></span>
<span data-ttu-id="a09e8-135">Указывает имя SKU учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="a09e8-135">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="a09e8-136">Доступные значения: Standard_LRS, Premium_LRS, StandardSSD_LRS и UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="a09e8-136">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="a09e8-137">UltraSSD_LRS можно использовать только с пустым значением для параметра CreateOption.</span><span class="sxs-lookup"><span data-stu-id="a09e8-137">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="a09e8-138">-Тег</span><span class="sxs-lookup"><span data-stu-id="a09e8-138">-Tag</span></span>
<span data-ttu-id="a09e8-139">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="a09e8-139">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a09e8-140">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="a09e8-140">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a09e8-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a09e8-141">-Confirm</span></span>
<span data-ttu-id="a09e8-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a09e8-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a09e8-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a09e8-143">-WhatIf</span></span>
<span data-ttu-id="a09e8-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a09e8-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a09e8-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a09e8-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a09e8-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a09e8-146">CommonParameters</span></span>
<span data-ttu-id="a09e8-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a09e8-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a09e8-148">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a09e8-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a09e8-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a09e8-149">INPUTS</span></span>

### <span data-ttu-id="a09e8-150">System. String</span><span class="sxs-lookup"><span data-stu-id="a09e8-150">System.String</span></span>

### <span data-ttu-id="a09e8-151">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="a09e8-151">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="a09e8-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a09e8-152">System.Int32</span></span>

### <span data-ttu-id="a09e8-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a09e8-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a09e8-154">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a09e8-154">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a09e8-155">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="a09e8-155">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="a09e8-156">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="a09e8-156">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="a09e8-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a09e8-157">OUTPUTS</span></span>

### <span data-ttu-id="a09e8-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="a09e8-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="a09e8-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="a09e8-159">NOTES</span></span>

## <span data-ttu-id="a09e8-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a09e8-160">RELATED LINKS</span></span>
