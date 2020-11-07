---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzSnapshot.md
ms.openlocfilehash: db26ee59bfeab521658d990836062da7dac594d2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910446"
---
# <span data-ttu-id="d4ec9-101">Update-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="d4ec9-101">Update-AzSnapshot</span></span>

## <span data-ttu-id="d4ec9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d4ec9-102">SYNOPSIS</span></span>
<span data-ttu-id="d4ec9-103">Обновляет снимок.</span><span class="sxs-lookup"><span data-stu-id="d4ec9-103">Updates a snapshot.</span></span>

## <span data-ttu-id="d4ec9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d4ec9-104">SYNTAX</span></span>

### <span data-ttu-id="d4ec9-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d4ec9-105">DefaultParameter (Default)</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String>
 [-SnapshotUpdate] <PSSnapshotUpdate> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4ec9-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="d4ec9-106">FriendMethod</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4ec9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4ec9-107">DESCRIPTION</span></span>
<span data-ttu-id="d4ec9-108">Командлет **Update-AzSnapshot** обновляет снимок.</span><span class="sxs-lookup"><span data-stu-id="d4ec9-108">The **Update-AzSnapshot** cmdlet updates a snapshot.</span></span>

## <span data-ttu-id="d4ec9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d4ec9-109">EXAMPLES</span></span>

### <span data-ttu-id="d4ec9-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d4ec9-110">Example 1</span></span>
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

<span data-ttu-id="d4ec9-111">Первая команда создает локальный пустой объект обновления моментального снимка с размером 10 ГБ в Premium_LRS типе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d4ec9-111">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="d4ec9-112">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="d4ec9-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="d4ec9-113">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="d4ec9-113">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="d4ec9-114">Последняя команда принимает объект обновления моментального снимка и обновляет существующий моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="d4ec9-114">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="d4ec9-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d4ec9-115">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="d4ec9-116">Эта команда обновляет существующий моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01" на диск размером 10 ГБ.</span><span class="sxs-lookup"><span data-stu-id="d4ec9-116">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="d4ec9-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d4ec9-117">Example 3</span></span>
```
PS C:\> $snapshot = Get-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

<span data-ttu-id="d4ec9-118">Эти команды также обновляют существующий моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01" на диск размером 10 ГБ.</span><span class="sxs-lookup"><span data-stu-id="d4ec9-118">These commands also update an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="d4ec9-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d4ec9-119">PARAMETERS</span></span>

### <span data-ttu-id="d4ec9-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4ec9-120">-AsJob</span></span>
<span data-ttu-id="d4ec9-121">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="d4ec9-121">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4ec9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4ec9-122">-DefaultProfile</span></span>
<span data-ttu-id="d4ec9-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d4ec9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4ec9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4ec9-124">-ResourceGroupName</span></span>
<span data-ttu-id="d4ec9-125">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d4ec9-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d4ec9-126">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="d4ec9-126">-Snapshot</span></span>
<span data-ttu-id="d4ec9-127">Указывает локальный объект снимка.</span><span class="sxs-lookup"><span data-stu-id="d4ec9-127">Specifies a local snapshot object.</span></span>

```yaml
Type: PSSnapshot
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4ec9-128">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="d4ec9-128">-SnapshotName</span></span>
<span data-ttu-id="d4ec9-129">Указывает имя снимка.</span><span class="sxs-lookup"><span data-stu-id="d4ec9-129">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="d4ec9-130">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="d4ec9-130">-SnapshotUpdate</span></span>
<span data-ttu-id="d4ec9-131">Указывает локальный объект обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="d4ec9-131">Specifies a local snapshot update object.</span></span>

```yaml
Type: PSSnapshotUpdate
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4ec9-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4ec9-132">-Confirm</span></span>
<span data-ttu-id="d4ec9-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d4ec9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4ec9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4ec9-134">-WhatIf</span></span>
<span data-ttu-id="d4ec9-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d4ec9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4ec9-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d4ec9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4ec9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4ec9-137">CommonParameters</span></span>
<span data-ttu-id="d4ec9-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d4ec9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4ec9-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4ec9-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4ec9-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d4ec9-140">INPUTS</span></span>

### <span data-ttu-id="d4ec9-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d4ec9-141">System.String</span></span>
<span data-ttu-id="d4ec9-142">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshotUpdate Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="d4ec9-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="d4ec9-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4ec9-143">OUTPUTS</span></span>

### <span data-ttu-id="d4ec9-144">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="d4ec9-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="d4ec9-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="d4ec9-145">NOTES</span></span>

## <span data-ttu-id="d4ec9-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4ec9-146">RELATED LINKS</span></span>

