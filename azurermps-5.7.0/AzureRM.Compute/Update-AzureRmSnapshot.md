---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmSnapshot.md
ms.openlocfilehash: ff70d3879685b0cdc9fcc42732a68e6b85bbd580
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557472"
---
# <span data-ttu-id="b1df2-101">Update-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="b1df2-101">Update-AzureRmSnapshot</span></span>

## <span data-ttu-id="b1df2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b1df2-102">SYNOPSIS</span></span>
<span data-ttu-id="b1df2-103">Обновляет снимок.</span><span class="sxs-lookup"><span data-stu-id="b1df2-103">Updates a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1df2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b1df2-104">SYNTAX</span></span>

### <span data-ttu-id="b1df2-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b1df2-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String>
 [-SnapshotUpdate] <SnapshotUpdate> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1df2-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="b1df2-106">FriendMethod</span></span>
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <Snapshot> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1df2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1df2-107">DESCRIPTION</span></span>
<span data-ttu-id="b1df2-108">Командлет **Update-AzureRmSnapshot** обновляет снимок.</span><span class="sxs-lookup"><span data-stu-id="b1df2-108">The **Update-AzureRmSnapshot** cmdlet updates a snapshot.</span></span>

## <span data-ttu-id="b1df2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b1df2-109">EXAMPLES</span></span>

### <span data-ttu-id="b1df2-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b1df2-110">Example 1</span></span>
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

<span data-ttu-id="b1df2-111">Первая команда создает локальный пустой объект обновления моментального снимка с размером 10 ГБ в Premium_LRS типе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b1df2-111">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="b1df2-112">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="b1df2-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="b1df2-113">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="b1df2-113">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="b1df2-114">Последняя команда принимает объект обновления моментального снимка и обновляет существующий моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="b1df2-114">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="b1df2-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b1df2-115">Example 2</span></span>
```
PS C:\> New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="b1df2-116">Эта команда обновляет существующий моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01" на диск размером 10 ГБ.</span><span class="sxs-lookup"><span data-stu-id="b1df2-116">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="b1df2-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="b1df2-117">Example 3</span></span>
```
PS C:\> $snapshot = Get-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

<span data-ttu-id="b1df2-118">Эти команды также обновляют существующий моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01" на диск размером 10 ГБ.</span><span class="sxs-lookup"><span data-stu-id="b1df2-118">These commands also update an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="b1df2-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b1df2-119">PARAMETERS</span></span>

### <span data-ttu-id="b1df2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1df2-120">-ResourceGroupName</span></span>
<span data-ttu-id="b1df2-121">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b1df2-121">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1df2-122">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="b1df2-122">-Snapshot</span></span>
<span data-ttu-id="b1df2-123">Указывает локальный объект снимка.</span><span class="sxs-lookup"><span data-stu-id="b1df2-123">Specifies a local snapshot object.</span></span>

```yaml
Type: Snapshot
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1df2-124">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="b1df2-124">-SnapshotName</span></span>
<span data-ttu-id="b1df2-125">Указывает имя снимка.</span><span class="sxs-lookup"><span data-stu-id="b1df2-125">Specifies the name of a snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1df2-126">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="b1df2-126">-SnapshotUpdate</span></span>
<span data-ttu-id="b1df2-127">Указывает локальный объект обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="b1df2-127">Specifies a local snapshot update object.</span></span>

```yaml
Type: SnapshotUpdate
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1df2-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1df2-128">-Confirm</span></span>
<span data-ttu-id="b1df2-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b1df2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1df2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1df2-130">-WhatIf</span></span>
<span data-ttu-id="b1df2-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b1df2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1df2-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b1df2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1df2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1df2-133">CommonParameters</span></span>
<span data-ttu-id="b1df2-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b1df2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1df2-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1df2-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1df2-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b1df2-136">INPUTS</span></span>

### <span data-ttu-id="b1df2-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b1df2-137">System.String</span></span>
<span data-ttu-id="b1df2-138">Microsoft. Azure. Management. COMPUTE. Models. SnapshotUpdate Microsoft. Azure. Management. COMPUTE. Models. Snapshot</span><span class="sxs-lookup"><span data-stu-id="b1df2-138">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="b1df2-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1df2-139">OUTPUTS</span></span>

### <span data-ttu-id="b1df2-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="b1df2-140">System.Object</span></span>

## <span data-ttu-id="b1df2-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="b1df2-141">NOTES</span></span>

## <span data-ttu-id="b1df2-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1df2-142">RELATED LINKS</span></span>

