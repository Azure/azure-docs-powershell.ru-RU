---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDisk.md
ms.openlocfilehash: bbb450aebe4b24aa887c8592acfab04e84bfd944
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249408"
---
# <span data-ttu-id="c454b-101">New-AzDisk</span><span class="sxs-lookup"><span data-stu-id="c454b-101">New-AzDisk</span></span>

## <span data-ttu-id="c454b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c454b-102">SYNOPSIS</span></span>
<span data-ttu-id="c454b-103">Создание управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="c454b-103">Creates a managed disk.</span></span>

## <span data-ttu-id="c454b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c454b-104">SYNTAX</span></span>

```
New-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c454b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c454b-105">DESCRIPTION</span></span>
<span data-ttu-id="c454b-106">Командлет **New-AzDisk** создает управляемый диск.</span><span class="sxs-lookup"><span data-stu-id="c454b-106">The **New-AzDisk** cmdlet creates a managed disk.</span></span>

## <span data-ttu-id="c454b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c454b-107">EXAMPLES</span></span>

### <span data-ttu-id="c454b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c454b-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -SkuName Standard_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="c454b-109">Первая команда создает локальный пустой объект диска с размером 5GB в Standard_LRS типе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="c454b-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="c454b-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="c454b-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="c454b-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта диска.</span><span class="sxs-lookup"><span data-stu-id="c454b-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="c454b-112">Последняя команда принимает объект диска и создает диск с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="c454b-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="c454b-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c454b-113">Example 2</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -SkuName Standard_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $diskConfig.EncryptionSettingsCollection = New-Object Microsoft.Azure.Management.Compute.Models.EncryptionSettingsCollection

PS C:\> $encryptionSettingsElement1 = New-Object Microsoft.Azure.Management.Compute.Models.EncryptionSettingsElement
PS C:\> $encryptionSettingsElement1.DiskEncryptionKey = New-Object Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference
PS C:\> $encryptionSettingsElement1.DiskEncryptionKey.SourceVault = New-Object Microsoft.Azure.Management.Compute.Models.SourceVault
PS C:\> $encryptionSettingsElement1.DiskEncryptionKey.SourceVault.Id = $disk_encryption_key_id_1
PS C:\> $encryptionSettingsElement1.DiskEncryptionKey.SecretUrl = $disk_encryption_secret_url_1
PS C:\> $encryptionSettingsElement1.KeyEncryptionKey = New-Object Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PS C:\> $encryptionSettingsElement1.KeyEncryptionKey.SourceVault = New-Object Microsoft.Azure.Management.Compute.Models.SourceVault
PS C:\> $encryptionSettingsElement1.KeyEncryptionKey.SourceVault.Id = $key_encryption_key_id_1
PS C:\> $encryptionSettingsElement1.KeyEncryptionKey.KeyUrl = $key_encryption_key_url_1

PS C:\> $encryptionSettingsElement2 = New-Object Microsoft.Azure.Management.Compute.Models.EncryptionSettingsElement
PS C:\> $encryptionSettingsElement2.DiskEncryptionKey = New-Object Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference
PS C:\> $encryptionSettingsElement2.DiskEncryptionKey.SourceVault = New-Object Microsoft.Azure.Management.Compute.Models.SourceVault
PS C:\> $encryptionSettingsElement2.DiskEncryptionKey.SourceVault.Id = $disk_encryption_key_id_2
PS C:\> $encryptionSettingsElement2.DiskEncryptionKey.SecretUrl = $disk_encryption_secret_url_2
PS C:\> $encryptionSettingsElement2.KeyEncryptionKey = New-Object Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PS C:\> $encryptionSettingsElement2.KeyEncryptionKey.SourceVault = New-Object Microsoft.Azure.Management.Compute.Models.SourceVault
PS C:\> $encryptionSettingsElement2.KeyEncryptionKey.SourceVault.Id = $key_encryption_key_id_2
PS C:\> $encryptionSettingsElement2.KeyEncryptionKey.KeyUrl = $key_encryption_key_url_2

PS C:\> $diskConfig.EncryptionSettingsCollection.EncryptionSettings += $encryptionSettingsElement1
PS C:\> $diskConfig.EncryptionSettingsCollection.EncryptionSettings += $encryptionSettingsElement2
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="c454b-114">В приведенной выше команде создается диск с двумя параметрами шифрования.</span><span class="sxs-lookup"><span data-stu-id="c454b-114">The above command creates a disk with two encryption settings.</span></span>

## <span data-ttu-id="c454b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c454b-115">PARAMETERS</span></span>

### <span data-ttu-id="c454b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c454b-116">-AsJob</span></span>
<span data-ttu-id="c454b-117">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="c454b-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c454b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c454b-118">-DefaultProfile</span></span>
<span data-ttu-id="c454b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c454b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c454b-120">-Диск</span><span class="sxs-lookup"><span data-stu-id="c454b-120">-Disk</span></span>
<span data-ttu-id="c454b-121">Указывает локальный дисковый объект.</span><span class="sxs-lookup"><span data-stu-id="c454b-121">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c454b-122">-DiskName</span><span class="sxs-lookup"><span data-stu-id="c454b-122">-DiskName</span></span>
<span data-ttu-id="c454b-123">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="c454b-123">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="c454b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c454b-124">-ResourceGroupName</span></span>
<span data-ttu-id="c454b-125">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c454b-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c454b-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c454b-126">-Confirm</span></span>
<span data-ttu-id="c454b-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c454b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c454b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c454b-128">-WhatIf</span></span>
<span data-ttu-id="c454b-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c454b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c454b-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c454b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c454b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c454b-131">CommonParameters</span></span>
<span data-ttu-id="c454b-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c454b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c454b-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c454b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c454b-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c454b-134">INPUTS</span></span>

### <span data-ttu-id="c454b-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c454b-135">System.String</span></span>

### <span data-ttu-id="c454b-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="c454b-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="c454b-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c454b-137">OUTPUTS</span></span>

### <span data-ttu-id="c454b-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="c454b-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="c454b-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="c454b-139">NOTES</span></span>

## <span data-ttu-id="c454b-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c454b-140">RELATED LINKS</span></span>
