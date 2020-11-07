---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzSnapshot.md
ms.openlocfilehash: eaf02348525cb1d6833ec52a0c4608e4a362ccd4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731197"
---
# <span data-ttu-id="7d2a5-101">Update-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="7d2a5-101">Update-AzSnapshot</span></span>

## <span data-ttu-id="7d2a5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7d2a5-102">SYNOPSIS</span></span>
<span data-ttu-id="7d2a5-103">Обновляет снимок.</span><span class="sxs-lookup"><span data-stu-id="7d2a5-103">Updates a snapshot.</span></span>

## <span data-ttu-id="7d2a5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7d2a5-104">SYNTAX</span></span>

### <span data-ttu-id="7d2a5-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7d2a5-105">DefaultParameter (Default)</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-SnapshotUpdate] <PSSnapshotUpdate>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d2a5-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="7d2a5-106">FriendMethod</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d2a5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d2a5-107">DESCRIPTION</span></span>
<span data-ttu-id="7d2a5-108">Командлет **Update-AzSnapshot** обновляет снимок.</span><span class="sxs-lookup"><span data-stu-id="7d2a5-108">The **Update-AzSnapshot** cmdlet updates a snapshot.</span></span>

## <span data-ttu-id="7d2a5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7d2a5-109">EXAMPLES</span></span>

### <span data-ttu-id="7d2a5-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7d2a5-110">Example 1</span></span>
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

<span data-ttu-id="7d2a5-111">Первая команда создает локальный пустой объект обновления моментального снимка с размером 10 ГБ в Premium_LRS типе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="7d2a5-111">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="7d2a5-112">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="7d2a5-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="7d2a5-113">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="7d2a5-113">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="7d2a5-114">Последняя команда принимает объект обновления моментального снимка и обновляет существующий моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="7d2a5-114">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="7d2a5-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7d2a5-115">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="7d2a5-116">Эта команда обновляет существующий моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01" на диск размером 10 ГБ.</span><span class="sxs-lookup"><span data-stu-id="7d2a5-116">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="7d2a5-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="7d2a5-117">Example 3</span></span>
```
PS C:\> $snapshot = Get-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

<span data-ttu-id="7d2a5-118">Эти команды также обновляют существующий моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01" на диск размером 10 ГБ.</span><span class="sxs-lookup"><span data-stu-id="7d2a5-118">These commands also update an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="7d2a5-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7d2a5-119">PARAMETERS</span></span>

### <span data-ttu-id="7d2a5-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d2a5-120">-AsJob</span></span>
<span data-ttu-id="7d2a5-121">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="7d2a5-121">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d2a5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d2a5-122">-DefaultProfile</span></span>
<span data-ttu-id="7d2a5-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7d2a5-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d2a5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d2a5-124">-ResourceGroupName</span></span>
<span data-ttu-id="7d2a5-125">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7d2a5-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d2a5-126">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="7d2a5-126">-Snapshot</span></span>
<span data-ttu-id="7d2a5-127">Указывает локальный объект снимка.</span><span class="sxs-lookup"><span data-stu-id="7d2a5-127">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d2a5-128">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="7d2a5-128">-SnapshotName</span></span>
<span data-ttu-id="7d2a5-129">Указывает имя снимка.</span><span class="sxs-lookup"><span data-stu-id="7d2a5-129">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d2a5-130">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="7d2a5-130">-SnapshotUpdate</span></span>
<span data-ttu-id="7d2a5-131">Указывает локальный объект обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="7d2a5-131">Specifies a local snapshot update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d2a5-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d2a5-132">-Confirm</span></span>
<span data-ttu-id="7d2a5-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7d2a5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d2a5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d2a5-134">-WhatIf</span></span>
<span data-ttu-id="7d2a5-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7d2a5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d2a5-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7d2a5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d2a5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d2a5-137">CommonParameters</span></span>
<span data-ttu-id="7d2a5-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7d2a5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d2a5-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d2a5-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d2a5-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7d2a5-140">INPUTS</span></span>

### <span data-ttu-id="7d2a5-141">System. String</span><span class="sxs-lookup"><span data-stu-id="7d2a5-141">System.String</span></span>

### <span data-ttu-id="7d2a5-142">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="7d2a5-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="7d2a5-143">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="7d2a5-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="7d2a5-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d2a5-144">OUTPUTS</span></span>

### <span data-ttu-id="7d2a5-145">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="7d2a5-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="7d2a5-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="7d2a5-146">NOTES</span></span>

## <span data-ttu-id="7d2a5-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d2a5-147">RELATED LINKS</span></span>
