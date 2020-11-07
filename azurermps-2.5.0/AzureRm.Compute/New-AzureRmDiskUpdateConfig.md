---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermdiskupdateconfig
schema: 2.0.0
ms.openlocfilehash: 790d366ced8b9466a906df2d3f1717ad9277ca9f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914609"
---
# <span data-ttu-id="1c494-101">New-AzureRmDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="1c494-101">New-AzureRmDiskUpdateConfig</span></span>

## <span data-ttu-id="1c494-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1c494-102">SYNOPSIS</span></span>
<span data-ttu-id="1c494-103">Создание настраиваемого объекта обновления диска.</span><span class="sxs-lookup"><span data-stu-id="1c494-103">Creates a configurable disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c494-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1c494-104">SYNTAX</span></span>

```
New-AzureRmDiskUpdateConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c494-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c494-105">DESCRIPTION</span></span>
<span data-ttu-id="1c494-106">Командлет **New-AzureRmDiskUpdateConfig** создает настраиваемый объект обновления диска.</span><span class="sxs-lookup"><span data-stu-id="1c494-106">The **New-AzureRmDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="1c494-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1c494-107">EXAMPLES</span></span>

### <span data-ttu-id="1c494-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1c494-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="1c494-109">Первая команда создает локальный пустой объект обновления диска с размером 10 ГБ в Premium_LRS тип учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="1c494-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="1c494-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="1c494-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="1c494-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта обновления диска.</span><span class="sxs-lookup"><span data-stu-id="1c494-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="1c494-112">Последняя команда принимает объект обновления диска и обновляет существующий диск с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="1c494-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="1c494-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1c494-113">Example 2</span></span>
```
PS C:\> New-AzureRmDiskUpdateConfig -DiskSizeGB 10 | Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="1c494-114">Эта команда обновляет существующий диск с именем "Disk01" в группе ресурсов "ResourceGroup01" на диск размером 10 ГБ.</span><span class="sxs-lookup"><span data-stu-id="1c494-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="1c494-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1c494-115">PARAMETERS</span></span>

### <span data-ttu-id="1c494-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c494-116">-DefaultProfile</span></span>
<span data-ttu-id="1c494-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1c494-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c494-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="1c494-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="1c494-119">Указывает объект ключа шифрования диска на диске.</span><span class="sxs-lookup"><span data-stu-id="1c494-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="1c494-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="1c494-120">-DiskSizeGB</span></span>
<span data-ttu-id="1c494-121">Задает размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="1c494-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="1c494-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="1c494-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="1c494-123">Включите параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="1c494-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="1c494-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="1c494-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="1c494-125">Задает ключ шифрования ключа на диске.</span><span class="sxs-lookup"><span data-stu-id="1c494-125">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="1c494-126">-OsType</span><span class="sxs-lookup"><span data-stu-id="1c494-126">-OsType</span></span>
<span data-ttu-id="1c494-127">Указывает тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="1c494-127">Specifies the OS type.</span></span>

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

### <span data-ttu-id="1c494-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="1c494-128">-SkuName</span></span>
<span data-ttu-id="1c494-129">Указывает имя SKU учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="1c494-129">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="1c494-130">-Тег</span><span class="sxs-lookup"><span data-stu-id="1c494-130">-Tag</span></span>
<span data-ttu-id="1c494-131">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="1c494-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1c494-132">Например:</span><span class="sxs-lookup"><span data-stu-id="1c494-132">For example:</span></span>

<span data-ttu-id="1c494-133">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="1c494-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c494-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c494-134">-Confirm</span></span>
<span data-ttu-id="1c494-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1c494-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c494-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c494-136">-WhatIf</span></span>
<span data-ttu-id="1c494-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1c494-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c494-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1c494-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c494-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c494-139">CommonParameters</span></span>
<span data-ttu-id="1c494-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1c494-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c494-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c494-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c494-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1c494-142">INPUTS</span></span>

### <span data-ttu-id="1c494-143">Ничего</span><span class="sxs-lookup"><span data-stu-id="1c494-143">None</span></span>
<span data-ttu-id="1c494-144">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="1c494-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1c494-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c494-145">OUTPUTS</span></span>

### <span data-ttu-id="1c494-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="1c494-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="1c494-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="1c494-147">NOTES</span></span>

## <span data-ttu-id="1c494-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1c494-148">RELATED LINKS</span></span>

