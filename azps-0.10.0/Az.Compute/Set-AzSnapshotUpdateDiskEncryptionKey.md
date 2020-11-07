---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotupdatediskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzSnapshotUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzSnapshotUpdateDiskEncryptionKey.md
ms.openlocfilehash: c427c63e6d7e954e2ce832b3d6e5fe3bf7c4a851
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911362"
---
# <span data-ttu-id="6a355-101">Set-AzSnapshotUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="6a355-101">Set-AzSnapshotUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="6a355-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6a355-102">SYNOPSIS</span></span>
<span data-ttu-id="6a355-103">Задает свойства ключа шифрования диска для объекта обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="6a355-103">Sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="6a355-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6a355-104">SYNTAX</span></span>

```
Set-AzSnapshotUpdateDiskEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6a355-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a355-105">DESCRIPTION</span></span>
<span data-ttu-id="6a355-106">Командлет **Set-AzSnapshotUpdateDiskEncryptionKey** задает свойства ключа шифрования диска в объекте обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="6a355-106">The **Set-AzSnapshotUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="6a355-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6a355-107">EXAMPLES</span></span>

### <span data-ttu-id="6a355-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6a355-108">Example 1</span></span>
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

<span data-ttu-id="6a355-109">Первая команда создает локальный пустой объект обновления моментального снимка с размером 10 ГБ в Premium_LRS типе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="6a355-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="6a355-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="6a355-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="6a355-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="6a355-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="6a355-112">Последняя команда принимает объект обновления моментального снимка и обновляет существующий моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="6a355-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="6a355-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6a355-113">PARAMETERS</span></span>

### <span data-ttu-id="6a355-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a355-114">-DefaultProfile</span></span>
<span data-ttu-id="6a355-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6a355-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a355-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="6a355-116">-SecretUrl</span></span>
<span data-ttu-id="6a355-117">Specifes секретный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="6a355-117">Specifes the secret Url.</span></span>

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

### <span data-ttu-id="6a355-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="6a355-118">-SnapshotUpdate</span></span>
<span data-ttu-id="6a355-119">Указывает локальный объект обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="6a355-119">Specifies a local snapshot update object.</span></span>

```yaml
Type: PSSnapshotUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a355-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="6a355-120">-SourceVaultId</span></span>
<span data-ttu-id="6a355-121">Указывает идентификатор исходного хранилища.</span><span class="sxs-lookup"><span data-stu-id="6a355-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="6a355-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a355-122">-Confirm</span></span>
<span data-ttu-id="6a355-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6a355-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a355-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a355-124">-WhatIf</span></span>
<span data-ttu-id="6a355-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6a355-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a355-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6a355-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a355-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a355-127">CommonParameters</span></span>
<span data-ttu-id="6a355-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6a355-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a355-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a355-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a355-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6a355-130">INPUTS</span></span>

### <span data-ttu-id="6a355-131">Microsoft. Azure. Management. COMPUTE. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="6a355-131">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>
<span data-ttu-id="6a355-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6a355-132">System.String</span></span>

## <span data-ttu-id="6a355-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a355-133">OUTPUTS</span></span>

### <span data-ttu-id="6a355-134">Microsoft. Azure. Management. COMPUTE. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="6a355-134">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="6a355-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="6a355-135">NOTES</span></span>

## <span data-ttu-id="6a355-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6a355-136">RELATED LINKS</span></span>

