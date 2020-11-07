---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmDisk.md
ms.openlocfilehash: 30a6ac1a3d74423302cc8b39e8b494e2f1ee2e22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732028"
---
# <span data-ttu-id="3e707-101">Update-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="3e707-101">Update-AzureRmDisk</span></span>

## <span data-ttu-id="3e707-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e707-102">SYNOPSIS</span></span>
<span data-ttu-id="3e707-103">Обновление диска.</span><span class="sxs-lookup"><span data-stu-id="3e707-103">Updates a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e707-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e707-104">SYNTAX</span></span>

### <span data-ttu-id="3e707-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3e707-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-DiskUpdate] <DiskUpdate> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e707-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="3e707-106">FriendMethod</span></span>
```
Update-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <Disk> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e707-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e707-107">DESCRIPTION</span></span>
<span data-ttu-id="3e707-108">Командлет **Update-AzureRmDisk** обновляет диск.</span><span class="sxs-lookup"><span data-stu-id="3e707-108">The **Update-AzureRmDisk** cmdlet updates a disk.</span></span>

## <span data-ttu-id="3e707-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e707-109">EXAMPLES</span></span>

### <span data-ttu-id="3e707-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3e707-110">Example 1</span></span>
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

<span data-ttu-id="3e707-111">Первая команда создает локальный пустой объект обновления диска с размером 10 ГБ в Premium_LRS тип учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="3e707-111">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="3e707-112">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="3e707-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="3e707-113">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта обновления диска.</span><span class="sxs-lookup"><span data-stu-id="3e707-113">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="3e707-114">Последняя команда принимает объект обновления диска и обновляет существующий диск с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="3e707-114">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="3e707-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3e707-115">Example 2</span></span>
```
PS C:\> New-AzureRmDiskUpdateConfig -DiskSizeGB 10 | Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="3e707-116">Эта команда обновляет существующий диск с именем "Disk01" в группе ресурсов "ResourceGroup01" на диск размером 10 ГБ.</span><span class="sxs-lookup"><span data-stu-id="3e707-116">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="3e707-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="3e707-117">Example 3</span></span>
```
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
PS C:\> $disk.DiskSizeGB = 10;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $disk;
```

<span data-ttu-id="3e707-118">Эти команды также возобновляют существующий диск с именем "Disk01" в группе ресурсов "ResourceGroup01" на диск размером 10 ГБ.</span><span class="sxs-lookup"><span data-stu-id="3e707-118">These commands also update an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="3e707-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e707-119">PARAMETERS</span></span>

### <span data-ttu-id="3e707-120">-Диск</span><span class="sxs-lookup"><span data-stu-id="3e707-120">-Disk</span></span>
<span data-ttu-id="3e707-121">Указывает локальный дисковый объект.</span><span class="sxs-lookup"><span data-stu-id="3e707-121">Specifies a local disk object.</span></span>

```yaml
Type: Disk
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e707-122">-DiskName</span><span class="sxs-lookup"><span data-stu-id="3e707-122">-DiskName</span></span>
<span data-ttu-id="3e707-123">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="3e707-123">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="3e707-124">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="3e707-124">-DiskUpdate</span></span>
<span data-ttu-id="3e707-125">Указывает объект обновления локального диска.</span><span class="sxs-lookup"><span data-stu-id="3e707-125">Specifies a local disk update object.</span></span>

```yaml
Type: DiskUpdate
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e707-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e707-126">-ResourceGroupName</span></span>
<span data-ttu-id="3e707-127">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3e707-127">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3e707-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e707-128">-Confirm</span></span>
<span data-ttu-id="3e707-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3e707-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e707-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e707-130">-WhatIf</span></span>
<span data-ttu-id="3e707-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3e707-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e707-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3e707-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e707-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e707-133">CommonParameters</span></span>
<span data-ttu-id="3e707-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e707-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e707-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e707-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e707-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e707-136">INPUTS</span></span>

### <span data-ttu-id="3e707-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3e707-137">System.String</span></span>
<span data-ttu-id="3e707-138">Microsoft. Azure. Management. COMPUTE. Models. DiskUpdate Microsoft. Azure. Management. COMPUTE. Models. Disk</span><span class="sxs-lookup"><span data-stu-id="3e707-138">Microsoft.Azure.Management.Compute.Models.DiskUpdate Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="3e707-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e707-139">OUTPUTS</span></span>

### <span data-ttu-id="3e707-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="3e707-140">System.Object</span></span>

## <span data-ttu-id="3e707-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e707-141">NOTES</span></span>

## <span data-ttu-id="3e707-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e707-142">RELATED LINKS</span></span>

