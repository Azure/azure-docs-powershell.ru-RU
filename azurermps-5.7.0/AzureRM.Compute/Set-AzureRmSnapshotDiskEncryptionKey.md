---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotDiskEncryptionKey.md
ms.openlocfilehash: 05e48bc312dcbbf317906fadb63b9777765032ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561895"
---
# <span data-ttu-id="0b3ea-101">Set-AzureRmSnapshotDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="0b3ea-101">Set-AzureRmSnapshotDiskEncryptionKey</span></span>

## <span data-ttu-id="0b3ea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0b3ea-102">SYNOPSIS</span></span>
<span data-ttu-id="0b3ea-103">Задает свойства ключа шифрования диска для объекта-снимка.</span><span class="sxs-lookup"><span data-stu-id="0b3ea-103">Sets the disk encryption key properties on a snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b3ea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0b3ea-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotDiskEncryptionKey [-Snapshot] <Snapshot> [[-SecretUrl] <String>] [[-SourceVaultId] <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b3ea-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b3ea-105">DESCRIPTION</span></span>
<span data-ttu-id="0b3ea-106">Командлет **Set-AzureRmSnapshotDiskEncryptionKey** задает свойства ключа шифрования диска для объекта-снимка.</span><span class="sxs-lookup"><span data-stu-id="0b3ea-106">The **Set-AzureRmSnapshotDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="0b3ea-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0b3ea-107">EXAMPLES</span></span>

### <span data-ttu-id="0b3ea-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0b3ea-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzureRmSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzureRmSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="0b3ea-109">В первой команде создается локальный пустой объект Snapshot с размером 5GB в Standard_LRS типе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0b3ea-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="0b3ea-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="0b3ea-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="0b3ea-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта snapshot.</span><span class="sxs-lookup"><span data-stu-id="0b3ea-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="0b3ea-112">Последняя команда принимает объект snapshot и создает моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="0b3ea-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="0b3ea-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0b3ea-113">PARAMETERS</span></span>

### <span data-ttu-id="0b3ea-114">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="0b3ea-114">-SecretUrl</span></span>
<span data-ttu-id="0b3ea-115">Задает секретный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="0b3ea-115">Specifies the secret Url.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b3ea-116">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="0b3ea-116">-Snapshot</span></span>
<span data-ttu-id="0b3ea-117">Указывает локальный объект снимка.</span><span class="sxs-lookup"><span data-stu-id="0b3ea-117">Specifies a local snapshot object.</span></span>

```yaml
Type: Snapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b3ea-118">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="0b3ea-118">-SourceVaultId</span></span>
<span data-ttu-id="0b3ea-119">Указывает идентификатор исходного хранилища.</span><span class="sxs-lookup"><span data-stu-id="0b3ea-119">Specifies the source vault ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b3ea-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b3ea-120">-Confirm</span></span>
<span data-ttu-id="0b3ea-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0b3ea-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b3ea-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b3ea-122">-WhatIf</span></span>
<span data-ttu-id="0b3ea-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0b3ea-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b3ea-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0b3ea-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b3ea-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b3ea-125">CommonParameters</span></span>
<span data-ttu-id="0b3ea-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0b3ea-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b3ea-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b3ea-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b3ea-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0b3ea-128">INPUTS</span></span>

### <span data-ttu-id="0b3ea-129">Microsoft. Azure. Management. COMPUTE. Models. Snapshot</span><span class="sxs-lookup"><span data-stu-id="0b3ea-129">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="0b3ea-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0b3ea-130">System.String</span></span>

## <span data-ttu-id="0b3ea-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b3ea-131">OUTPUTS</span></span>

### <span data-ttu-id="0b3ea-132">Microsoft. Azure. Management. COMPUTE. Models. Snapshot</span><span class="sxs-lookup"><span data-stu-id="0b3ea-132">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="0b3ea-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="0b3ea-133">NOTES</span></span>

## <span data-ttu-id="0b3ea-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0b3ea-134">RELATED LINKS</span></span>

