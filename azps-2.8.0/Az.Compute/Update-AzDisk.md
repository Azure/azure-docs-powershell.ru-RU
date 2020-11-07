---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDisk.md
ms.openlocfilehash: 382bbb84a12834ea35bf42d2a1cce95afa5d93de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721632"
---
# <span data-ttu-id="21fa6-101">Update-AzDisk</span><span class="sxs-lookup"><span data-stu-id="21fa6-101">Update-AzDisk</span></span>

## <span data-ttu-id="21fa6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="21fa6-102">SYNOPSIS</span></span>
<span data-ttu-id="21fa6-103">Обновление диска.</span><span class="sxs-lookup"><span data-stu-id="21fa6-103">Updates a disk.</span></span>

## <span data-ttu-id="21fa6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="21fa6-104">SYNTAX</span></span>

### <span data-ttu-id="21fa6-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="21fa6-105">DefaultParameter (Default)</span></span>
```
Update-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-DiskUpdate] <PSDiskUpdate> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21fa6-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="21fa6-106">FriendMethod</span></span>
```
Update-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21fa6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="21fa6-107">DESCRIPTION</span></span>
<span data-ttu-id="21fa6-108">Командлет **Update-AzDisk** обновляет диск.</span><span class="sxs-lookup"><span data-stu-id="21fa6-108">The **Update-AzDisk** cmdlet updates a disk.</span></span>

## <span data-ttu-id="21fa6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="21fa6-109">EXAMPLES</span></span>

### <span data-ttu-id="21fa6-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="21fa6-110">Example 1</span></span>
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

<span data-ttu-id="21fa6-111">Первая команда создает локальный пустой объект обновления диска с размером 10 ГБ в Premium_LRS тип учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="21fa6-111">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="21fa6-112">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="21fa6-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="21fa6-113">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта обновления диска.</span><span class="sxs-lookup"><span data-stu-id="21fa6-113">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="21fa6-114">Последняя команда принимает объект обновления диска и обновляет существующий диск с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="21fa6-114">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="21fa6-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="21fa6-115">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="21fa6-116">Эта команда обновляет существующий диск с именем "Disk01" в группе ресурсов "ResourceGroup01" на диск размером 10 ГБ.</span><span class="sxs-lookup"><span data-stu-id="21fa6-116">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="21fa6-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="21fa6-117">Example 3</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
PS C:\> $disk.DiskSizeGB = 10;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $disk;
```

<span data-ttu-id="21fa6-118">Эти команды также возобновляют существующий диск с именем "Disk01" в группе ресурсов "ResourceGroup01" на диск размером 10 ГБ.</span><span class="sxs-lookup"><span data-stu-id="21fa6-118">These commands also update an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="21fa6-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="21fa6-119">PARAMETERS</span></span>

### <span data-ttu-id="21fa6-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21fa6-120">-AsJob</span></span>
<span data-ttu-id="21fa6-121">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="21fa6-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="21fa6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21fa6-122">-DefaultProfile</span></span>
<span data-ttu-id="21fa6-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="21fa6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21fa6-124">-Диск</span><span class="sxs-lookup"><span data-stu-id="21fa6-124">-Disk</span></span>
<span data-ttu-id="21fa6-125">Указывает локальный дисковый объект.</span><span class="sxs-lookup"><span data-stu-id="21fa6-125">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21fa6-126">-DiskName</span><span class="sxs-lookup"><span data-stu-id="21fa6-126">-DiskName</span></span>
<span data-ttu-id="21fa6-127">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="21fa6-127">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="21fa6-128">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="21fa6-128">-DiskUpdate</span></span>
<span data-ttu-id="21fa6-129">Указывает объект обновления локального диска.</span><span class="sxs-lookup"><span data-stu-id="21fa6-129">Specifies a local disk update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21fa6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21fa6-130">-ResourceGroupName</span></span>
<span data-ttu-id="21fa6-131">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="21fa6-131">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="21fa6-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21fa6-132">-Confirm</span></span>
<span data-ttu-id="21fa6-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="21fa6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21fa6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21fa6-134">-WhatIf</span></span>
<span data-ttu-id="21fa6-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="21fa6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21fa6-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="21fa6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21fa6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21fa6-137">CommonParameters</span></span>
<span data-ttu-id="21fa6-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="21fa6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21fa6-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21fa6-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21fa6-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="21fa6-140">INPUTS</span></span>

### <span data-ttu-id="21fa6-141">System. String</span><span class="sxs-lookup"><span data-stu-id="21fa6-141">System.String</span></span>

### <span data-ttu-id="21fa6-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="21fa6-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="21fa6-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="21fa6-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="21fa6-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="21fa6-144">OUTPUTS</span></span>

### <span data-ttu-id="21fa6-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="21fa6-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="21fa6-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="21fa6-146">NOTES</span></span>

## <span data-ttu-id="21fa6-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="21fa6-147">RELATED LINKS</span></span>
