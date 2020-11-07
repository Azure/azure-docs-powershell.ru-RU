---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmDisk.md
ms.openlocfilehash: 81cf8a6d011575702f8eead878e8987a5a0fd456
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734891"
---
# <span data-ttu-id="2b9b7-101">Update-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="2b9b7-101">Update-AzureRmDisk</span></span>

## <span data-ttu-id="2b9b7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2b9b7-102">SYNOPSIS</span></span>
<span data-ttu-id="2b9b7-103">Обновление диска.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-103">Updates a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b9b7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2b9b7-104">SYNTAX</span></span>

### <span data-ttu-id="2b9b7-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2b9b7-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-DiskUpdate] <PSDiskUpdate>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b9b7-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="2b9b7-106">FriendMethod</span></span>
```
Update-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b9b7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b9b7-107">DESCRIPTION</span></span>
<span data-ttu-id="2b9b7-108">Командлет **Update-AzureRmDisk** обновляет диск.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-108">The **Update-AzureRmDisk** cmdlet updates a disk.</span></span>

## <span data-ttu-id="2b9b7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2b9b7-109">EXAMPLES</span></span>

### <span data-ttu-id="2b9b7-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2b9b7-110">Example 1</span></span>
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

<span data-ttu-id="2b9b7-111">Первая команда создает локальный пустой объект обновления диска с размером 10 ГБ в Premium_LRS тип учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-111">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="2b9b7-112">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="2b9b7-113">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта обновления диска.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-113">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="2b9b7-114">Последняя команда принимает объект обновления диска и обновляет существующий диск с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="2b9b7-114">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="2b9b7-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2b9b7-115">Example 2</span></span>
```
PS C:\> New-AzureRmDiskUpdateConfig -DiskSizeGB 10 | Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="2b9b7-116">Эта команда обновляет существующий диск с именем "Disk01" в группе ресурсов "ResourceGroup01" на диск размером 10 ГБ.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-116">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="2b9b7-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="2b9b7-117">Example 3</span></span>
```
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
PS C:\> $disk.DiskSizeGB = 10;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $disk;
```

<span data-ttu-id="2b9b7-118">Эти команды также возобновляют существующий диск с именем "Disk01" в группе ресурсов "ResourceGroup01" на диск размером 10 ГБ.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-118">These commands also update an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="2b9b7-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2b9b7-119">PARAMETERS</span></span>

### <span data-ttu-id="2b9b7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b9b7-120">-DefaultProfile</span></span>
<span data-ttu-id="2b9b7-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b9b7-122">-Диск</span><span class="sxs-lookup"><span data-stu-id="2b9b7-122">-Disk</span></span>
<span data-ttu-id="2b9b7-123">Указывает локальный дисковый объект.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-123">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b9b7-124">-DiskName</span><span class="sxs-lookup"><span data-stu-id="2b9b7-124">-DiskName</span></span>
<span data-ttu-id="2b9b7-125">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-125">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="2b9b7-126">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="2b9b7-126">-DiskUpdate</span></span>
<span data-ttu-id="2b9b7-127">Указывает объект обновления локального диска.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-127">Specifies a local disk update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b9b7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b9b7-128">-ResourceGroupName</span></span>
<span data-ttu-id="2b9b7-129">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-129">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2b9b7-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b9b7-130">-Confirm</span></span>
<span data-ttu-id="2b9b7-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b9b7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b9b7-132">-WhatIf</span></span>
<span data-ttu-id="2b9b7-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b9b7-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b9b7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b9b7-135">CommonParameters</span></span>
<span data-ttu-id="2b9b7-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2b9b7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b9b7-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b9b7-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b9b7-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2b9b7-138">INPUTS</span></span>

### <span data-ttu-id="2b9b7-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2b9b7-139">System.String</span></span>
<span data-ttu-id="2b9b7-140">Microsoft. Azure. Management. COMPUTE. Models. DiskUpdate Microsoft. Azure. Management. COMPUTE. Models. Disk</span><span class="sxs-lookup"><span data-stu-id="2b9b7-140">Microsoft.Azure.Management.Compute.Models.DiskUpdate Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="2b9b7-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b9b7-141">OUTPUTS</span></span>

### <span data-ttu-id="2b9b7-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="2b9b7-142">System.Object</span></span>

## <span data-ttu-id="2b9b7-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="2b9b7-143">NOTES</span></span>

## <span data-ttu-id="2b9b7-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b9b7-144">RELATED LINKS</span></span>

