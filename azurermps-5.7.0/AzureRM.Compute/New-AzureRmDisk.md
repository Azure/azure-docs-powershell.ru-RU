---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDisk.md
ms.openlocfilehash: 04106c91e99372b985c0a10ac12a7944fdcb4e41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734471"
---
# <span data-ttu-id="ce1b6-101">New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="ce1b6-101">New-AzureRmDisk</span></span>

## <span data-ttu-id="ce1b6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ce1b6-102">SYNOPSIS</span></span>
<span data-ttu-id="ce1b6-103">Создание управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="ce1b6-103">Creates a managed disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce1b6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ce1b6-104">SYNTAX</span></span>

```
New-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <Disk> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce1b6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce1b6-105">DESCRIPTION</span></span>
<span data-ttu-id="ce1b6-106">Командлет **New-AzureRmDisk** создает управляемый диск.</span><span class="sxs-lookup"><span data-stu-id="ce1b6-106">The **New-AzureRmDisk** cmdlet creates a managed disk.</span></span>

## <span data-ttu-id="ce1b6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ce1b6-107">EXAMPLES</span></span>

### <span data-ttu-id="ce1b6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ce1b6-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzureRmDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzureRmDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="ce1b6-109">Первая команда создает локальный пустой объект диска с размером 5GB в Standard_LRS типе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="ce1b6-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="ce1b6-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="ce1b6-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="ce1b6-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта диска.</span><span class="sxs-lookup"><span data-stu-id="ce1b6-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="ce1b6-112">Последняя команда принимает объект диска и создает диск с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="ce1b6-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ce1b6-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ce1b6-113">PARAMETERS</span></span>

### <span data-ttu-id="ce1b6-114">-Диск</span><span class="sxs-lookup"><span data-stu-id="ce1b6-114">-Disk</span></span>
<span data-ttu-id="ce1b6-115">Указывает локальный дисковый объект.</span><span class="sxs-lookup"><span data-stu-id="ce1b6-115">Specifies a local disk object.</span></span>

```yaml
Type: Disk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce1b6-116">-DiskName</span><span class="sxs-lookup"><span data-stu-id="ce1b6-116">-DiskName</span></span>
<span data-ttu-id="ce1b6-117">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="ce1b6-117">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="ce1b6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce1b6-118">-ResourceGroupName</span></span>
<span data-ttu-id="ce1b6-119">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ce1b6-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ce1b6-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce1b6-120">-Confirm</span></span>
<span data-ttu-id="ce1b6-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ce1b6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce1b6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce1b6-122">-WhatIf</span></span>
<span data-ttu-id="ce1b6-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ce1b6-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce1b6-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ce1b6-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce1b6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce1b6-125">CommonParameters</span></span>
<span data-ttu-id="ce1b6-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ce1b6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce1b6-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce1b6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce1b6-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ce1b6-128">INPUTS</span></span>

### <span data-ttu-id="ce1b6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ce1b6-129">System.String</span></span>
<span data-ttu-id="ce1b6-130">Microsoft. Azure. Management. COMPUTE. Models.</span><span class="sxs-lookup"><span data-stu-id="ce1b6-130">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="ce1b6-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce1b6-131">OUTPUTS</span></span>

### <span data-ttu-id="ce1b6-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="ce1b6-132">System.Object</span></span>

## <span data-ttu-id="ce1b6-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="ce1b6-133">NOTES</span></span>

## <span data-ttu-id="ce1b6-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ce1b6-134">RELATED LINKS</span></span>

