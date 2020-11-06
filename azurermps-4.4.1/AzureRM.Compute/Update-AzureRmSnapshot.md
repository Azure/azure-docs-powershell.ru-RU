---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmSnapshot.md
ms.openlocfilehash: 71407a78dd19f6324370b88be06841918a4c244a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566294"
---
# <span data-ttu-id="14076-101">Update-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="14076-101">Update-AzureRmSnapshot</span></span>

## <span data-ttu-id="14076-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="14076-102">SYNOPSIS</span></span>
<span data-ttu-id="14076-103">Обновляет снимок.</span><span class="sxs-lookup"><span data-stu-id="14076-103">Updates a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14076-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="14076-104">SYNTAX</span></span>

### <span data-ttu-id="14076-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="14076-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String>
 [-SnapshotUpdate] <PSSnapshotUpdate> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14076-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="14076-106">FriendMethod</span></span>
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14076-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14076-107">DESCRIPTION</span></span>
<span data-ttu-id="14076-108">Командлет **Update-AzureRmSnapshot** обновляет снимок.</span><span class="sxs-lookup"><span data-stu-id="14076-108">The **Update-AzureRmSnapshot** cmdlet updates a snapshot.</span></span>

## <span data-ttu-id="14076-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="14076-109">EXAMPLES</span></span>

### <span data-ttu-id="14076-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="14076-110">Example 1</span></span>
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

<span data-ttu-id="14076-111">Первая команда создает локальный пустой объект обновления моментального снимка с размером 10 ГБ в Premium_LRS типе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="14076-111">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="14076-112">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="14076-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="14076-113">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="14076-113">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="14076-114">Последняя команда принимает объект обновления моментального снимка и обновляет существующий моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="14076-114">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="14076-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="14076-115">Example 2</span></span>
```
PS C:\> New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="14076-116">Эта команда обновляет существующий моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01" на диск размером 10 ГБ.</span><span class="sxs-lookup"><span data-stu-id="14076-116">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="14076-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="14076-117">Example 3</span></span>
```
PS C:\> $snapshot = Get-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

<span data-ttu-id="14076-118">Эти команды также обновляют существующий моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01" на диск размером 10 ГБ.</span><span class="sxs-lookup"><span data-stu-id="14076-118">These commands also update an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="14076-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="14076-119">PARAMETERS</span></span>

### <span data-ttu-id="14076-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14076-120">-DefaultProfile</span></span>
<span data-ttu-id="14076-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="14076-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14076-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14076-122">-ResourceGroupName</span></span>
<span data-ttu-id="14076-123">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="14076-123">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14076-124">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="14076-124">-Snapshot</span></span>
<span data-ttu-id="14076-125">Указывает локальный объект снимка.</span><span class="sxs-lookup"><span data-stu-id="14076-125">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14076-126">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="14076-126">-SnapshotName</span></span>
<span data-ttu-id="14076-127">Указывает имя снимка.</span><span class="sxs-lookup"><span data-stu-id="14076-127">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14076-128">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="14076-128">-SnapshotUpdate</span></span>
<span data-ttu-id="14076-129">Указывает локальный объект обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="14076-129">Specifies a local snapshot update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14076-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14076-130">-Confirm</span></span>
<span data-ttu-id="14076-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="14076-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14076-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14076-132">-WhatIf</span></span>
<span data-ttu-id="14076-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="14076-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14076-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="14076-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14076-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14076-135">CommonParameters</span></span>
<span data-ttu-id="14076-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="14076-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14076-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14076-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14076-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="14076-138">INPUTS</span></span>

### <span data-ttu-id="14076-139">System. String</span><span class="sxs-lookup"><span data-stu-id="14076-139">System.String</span></span>
<span data-ttu-id="14076-140">Microsoft. Azure. Management. COMPUTE. Models. SnapshotUpdate Microsoft. Azure. Management. COMPUTE. Models. Snapshot</span><span class="sxs-lookup"><span data-stu-id="14076-140">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="14076-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="14076-141">OUTPUTS</span></span>

### <span data-ttu-id="14076-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="14076-142">System.Object</span></span>

## <span data-ttu-id="14076-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="14076-143">NOTES</span></span>

## <span data-ttu-id="14076-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14076-144">RELATED LINKS</span></span>

