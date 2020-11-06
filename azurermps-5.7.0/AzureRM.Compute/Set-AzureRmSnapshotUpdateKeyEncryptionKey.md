---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateKeyEncryptionKey.md
ms.openlocfilehash: 8745202e860cb71d20e17d68203a9bc79b3167ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557515"
---
# <span data-ttu-id="a0f2f-101">Set-AzureRmSnapshotUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a0f2f-101">Set-AzureRmSnapshotUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="a0f2f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a0f2f-102">SYNOPSIS</span></span>
<span data-ttu-id="a0f2f-103">Устанавливает свойства ключа шифрования для объекта обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="a0f2f-103">Sets the key encryption key properties on a snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0f2f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a0f2f-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotUpdateKeyEncryptionKey [-SnapshotUpdate] <SnapshotUpdate> [[-KeyUrl] <String>]
 [[-SourceVaultId] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0f2f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0f2f-105">DESCRIPTION</span></span>
<span data-ttu-id="a0f2f-106">Командлет **Set-AzureRmSnapshotUpdateKeyEncryptionKey** устанавливает свойства ключа шифрования для объекта обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="a0f2f-106">The **Set-AzureRmSnapshotUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="a0f2f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a0f2f-107">EXAMPLES</span></span>

### <span data-ttu-id="a0f2f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a0f2f-108">Example 1</span></span>
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

<span data-ttu-id="a0f2f-109">Первая команда создает локальный пустой объект обновления моментального снимка с размером 10 ГБ в Premium_LRS типе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="a0f2f-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="a0f2f-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="a0f2f-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="a0f2f-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="a0f2f-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="a0f2f-112">Последняя команда принимает объект обновления моментального снимка и обновляет существующий моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="a0f2f-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="a0f2f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a0f2f-113">PARAMETERS</span></span>

### <span data-ttu-id="a0f2f-114">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="a0f2f-114">-KeyUrl</span></span>
<span data-ttu-id="a0f2f-115">Specifes URL-адрес ключа.</span><span class="sxs-lookup"><span data-stu-id="a0f2f-115">Specifes the key Url.</span></span>

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

### <span data-ttu-id="a0f2f-116">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="a0f2f-116">-SnapshotUpdate</span></span>
<span data-ttu-id="a0f2f-117">Указывает локальный объект обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="a0f2f-117">Specifies a local snapshot update object.</span></span>

```yaml
Type: SnapshotUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0f2f-118">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="a0f2f-118">-SourceVaultId</span></span>
<span data-ttu-id="a0f2f-119">Указывает идентификатор исходного хранилища.</span><span class="sxs-lookup"><span data-stu-id="a0f2f-119">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="a0f2f-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0f2f-120">-Confirm</span></span>
<span data-ttu-id="a0f2f-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a0f2f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0f2f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0f2f-122">-WhatIf</span></span>
<span data-ttu-id="a0f2f-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a0f2f-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0f2f-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a0f2f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0f2f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0f2f-125">CommonParameters</span></span>
<span data-ttu-id="a0f2f-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a0f2f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0f2f-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0f2f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0f2f-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a0f2f-128">INPUTS</span></span>

### <span data-ttu-id="a0f2f-129">Microsoft. Azure. Management. COMPUTE. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="a0f2f-129">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>
<span data-ttu-id="a0f2f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a0f2f-130">System.String</span></span>

## <span data-ttu-id="a0f2f-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0f2f-131">OUTPUTS</span></span>

### <span data-ttu-id="a0f2f-132">Microsoft. Azure. Management. COMPUTE. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="a0f2f-132">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="a0f2f-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="a0f2f-133">NOTES</span></span>

## <span data-ttu-id="a0f2f-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a0f2f-134">RELATED LINKS</span></span>

