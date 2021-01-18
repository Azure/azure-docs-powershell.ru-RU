---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDisk.md
ms.openlocfilehash: 18f013643ad65bd4f7c70f3181e5950e10aa08ac
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519434"
---
# <span data-ttu-id="256b2-101">Update-AzDisk</span><span class="sxs-lookup"><span data-stu-id="256b2-101">Update-AzDisk</span></span>

## <span data-ttu-id="256b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="256b2-102">SYNOPSIS</span></span>
<span data-ttu-id="256b2-103">Обновляет диск.</span><span class="sxs-lookup"><span data-stu-id="256b2-103">Updates a disk.</span></span>

## <span data-ttu-id="256b2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="256b2-104">SYNTAX</span></span>

### <span data-ttu-id="256b2-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="256b2-105">DefaultParameter (Default)</span></span>
```
Update-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-DiskUpdate] <PSDiskUpdate> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="256b2-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="256b2-106">FriendMethod</span></span>
```
Update-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="256b2-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="256b2-107">DESCRIPTION</span></span>
<span data-ttu-id="256b2-108">Для **диска обновляется cmdlet Update-AzDisk.**</span><span class="sxs-lookup"><span data-stu-id="256b2-108">The **Update-AzDisk** cmdlet updates a disk.</span></span>

## <span data-ttu-id="256b2-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="256b2-109">EXAMPLES</span></span>

### <span data-ttu-id="256b2-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="256b2-110">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -SkuName Premium_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="256b2-111">Первая команда создает объект обновления локального пустого диска с размером 10 ГБ Premium_LRS типа учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="256b2-111">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="256b2-112">Она также задает тип ОС Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="256b2-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="256b2-113">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта обновления диска.</span><span class="sxs-lookup"><span data-stu-id="256b2-113">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="256b2-114">Последняя команда принимает объект обновления диска и обновляет существующий диск с именем "Диск01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="256b2-114">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="256b2-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="256b2-115">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="256b2-116">Эта команда обновляет существующий диск с именем "Диск01" в группе ресурсов "Группа ресурсов01" до размера диска 10 ГБ.</span><span class="sxs-lookup"><span data-stu-id="256b2-116">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="256b2-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="256b2-117">Example 3</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
PS C:\> $disk.DiskSizeGB = 10;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $disk;
```

<span data-ttu-id="256b2-118">Эти команды также обновляют существующий диск с именем "Диск01" в группе ресурсов "Группа ресурсов01" до размера диска 10 ГБ.</span><span class="sxs-lookup"><span data-stu-id="256b2-118">These commands also update an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="256b2-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="256b2-119">PARAMETERS</span></span>

### <span data-ttu-id="256b2-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="256b2-120">-AsJob</span></span>
<span data-ttu-id="256b2-121">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="256b2-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="256b2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="256b2-122">-DefaultProfile</span></span>
<span data-ttu-id="256b2-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="256b2-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="256b2-124">-Диск</span><span class="sxs-lookup"><span data-stu-id="256b2-124">-Disk</span></span>
<span data-ttu-id="256b2-125">Определяет объект локального диска.</span><span class="sxs-lookup"><span data-stu-id="256b2-125">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="256b2-126">-DiskName</span><span class="sxs-lookup"><span data-stu-id="256b2-126">-DiskName</span></span>
<span data-ttu-id="256b2-127">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="256b2-127">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="256b2-128">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="256b2-128">-DiskUpdate</span></span>
<span data-ttu-id="256b2-129">Определяет объект обновления локального диска.</span><span class="sxs-lookup"><span data-stu-id="256b2-129">Specifies a local disk update object.</span></span>

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

### <span data-ttu-id="256b2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="256b2-130">-ResourceGroupName</span></span>
<span data-ttu-id="256b2-131">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="256b2-131">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="256b2-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="256b2-132">-Confirm</span></span>
<span data-ttu-id="256b2-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="256b2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="256b2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="256b2-134">-WhatIf</span></span>
<span data-ttu-id="256b2-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="256b2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="256b2-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="256b2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="256b2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="256b2-137">CommonParameters</span></span>
<span data-ttu-id="256b2-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="256b2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="256b2-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="256b2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="256b2-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="256b2-140">INPUTS</span></span>

### <span data-ttu-id="256b2-141">System.String</span><span class="sxs-lookup"><span data-stu-id="256b2-141">System.String</span></span>

### <span data-ttu-id="256b2-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="256b2-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="256b2-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDокне</span><span class="sxs-lookup"><span data-stu-id="256b2-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="256b2-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="256b2-144">OUTPUTS</span></span>

### <span data-ttu-id="256b2-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSDокне</span><span class="sxs-lookup"><span data-stu-id="256b2-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="256b2-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="256b2-146">NOTES</span></span>

## <span data-ttu-id="256b2-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="256b2-147">RELATED LINKS</span></span>
