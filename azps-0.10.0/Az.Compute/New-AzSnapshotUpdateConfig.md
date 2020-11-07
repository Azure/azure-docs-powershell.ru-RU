---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
ms.openlocfilehash: c2c17fe3329170d65d61e5439e614717a8119f26
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911467"
---
# <span data-ttu-id="0e9d8-101">New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="0e9d8-101">New-AzSnapshotUpdateConfig</span></span>

## <span data-ttu-id="0e9d8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0e9d8-102">SYNOPSIS</span></span>
<span data-ttu-id="0e9d8-103">Создание настраиваемого объекта обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="0e9d8-103">Creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="0e9d8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0e9d8-104">SYNTAX</span></span>

```
New-AzSnapshotUpdateConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e9d8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e9d8-105">DESCRIPTION</span></span>
<span data-ttu-id="0e9d8-106">Командлет **New-AzSnapshotUpdateConfig** создает настраиваемый объект обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="0e9d8-106">The **New-AzSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="0e9d8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0e9d8-107">EXAMPLES</span></span>

### <span data-ttu-id="0e9d8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0e9d8-108">Example 1</span></span>
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

<span data-ttu-id="0e9d8-109">Первая команда создает локальный пустой объект обновления моментального снимка с размером 10 ГБ в Premium_LRS типе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0e9d8-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="0e9d8-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="0e9d8-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="0e9d8-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="0e9d8-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span> <span data-ttu-id="0e9d8-112">Последняя команда принимает объект обновления моментального снимка и обновляет существующий моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="0e9d8-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="0e9d8-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0e9d8-113">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="0e9d8-114">Эта команда обновляет существующий моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01" на диск размером 10 ГБ.</span><span class="sxs-lookup"><span data-stu-id="0e9d8-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="0e9d8-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0e9d8-115">PARAMETERS</span></span>

### <span data-ttu-id="0e9d8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e9d8-116">-DefaultProfile</span></span>
<span data-ttu-id="0e9d8-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0e9d8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e9d8-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="0e9d8-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="0e9d8-119">Задает объект ключа шифрования диска для снимка.</span><span class="sxs-lookup"><span data-stu-id="0e9d8-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="0e9d8-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="0e9d8-120">-DiskSizeGB</span></span>
<span data-ttu-id="0e9d8-121">Задает размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="0e9d8-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="0e9d8-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="0e9d8-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="0e9d8-123">Включите параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="0e9d8-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="0e9d8-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="0e9d8-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="0e9d8-125">Задает ключ шифрования ключа для снимка.</span><span class="sxs-lookup"><span data-stu-id="0e9d8-125">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="0e9d8-126">-OsType</span><span class="sxs-lookup"><span data-stu-id="0e9d8-126">-OsType</span></span>
<span data-ttu-id="0e9d8-127">Указывает тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="0e9d8-127">Specifies the OS type.</span></span>

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

### <span data-ttu-id="0e9d8-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="0e9d8-128">-SkuName</span></span>
<span data-ttu-id="0e9d8-129">Указывает имя SKU учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0e9d8-129">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="0e9d8-130">-Тег</span><span class="sxs-lookup"><span data-stu-id="0e9d8-130">-Tag</span></span>
<span data-ttu-id="0e9d8-131">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="0e9d8-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0e9d8-132">Например:</span><span class="sxs-lookup"><span data-stu-id="0e9d8-132">For example:</span></span>

<span data-ttu-id="0e9d8-133">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="0e9d8-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0e9d8-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0e9d8-134">-Confirm</span></span>
<span data-ttu-id="0e9d8-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0e9d8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e9d8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e9d8-136">-WhatIf</span></span>
<span data-ttu-id="0e9d8-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0e9d8-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0e9d8-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0e9d8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e9d8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e9d8-139">CommonParameters</span></span>
<span data-ttu-id="0e9d8-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0e9d8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e9d8-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e9d8-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e9d8-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0e9d8-142">INPUTS</span></span>

### <span data-ttu-id="0e9d8-143">Ничего</span><span class="sxs-lookup"><span data-stu-id="0e9d8-143">None</span></span>
<span data-ttu-id="0e9d8-144">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="0e9d8-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0e9d8-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e9d8-145">OUTPUTS</span></span>

### <span data-ttu-id="0e9d8-146">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="0e9d8-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="0e9d8-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="0e9d8-147">NOTES</span></span>

## <span data-ttu-id="0e9d8-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0e9d8-148">RELATED LINKS</span></span>

