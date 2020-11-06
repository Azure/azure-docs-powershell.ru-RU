---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermsnapshotupdatediskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmSnapshotUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmSnapshotUpdateDiskEncryptionKey.md
ms.openlocfilehash: 2a6f1fdc21b013e8a0aa0d34690b8e43319b306e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568937"
---
# <span data-ttu-id="580aa-101">Set-AzureRmSnapshotUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="580aa-101">Set-AzureRmSnapshotUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="580aa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="580aa-102">SYNOPSIS</span></span>
<span data-ttu-id="580aa-103">Задает свойства ключа шифрования диска для объекта обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="580aa-103">Sets the disk encryption key properties on a snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="580aa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="580aa-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotUpdateDiskEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="580aa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="580aa-105">DESCRIPTION</span></span>
<span data-ttu-id="580aa-106">Командлет **Set-AzureRmSnapshotUpdateDiskEncryptionKey** задает свойства ключа шифрования диска в объекте обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="580aa-106">The **Set-AzureRmSnapshotUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="580aa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="580aa-107">EXAMPLES</span></span>

### <span data-ttu-id="580aa-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="580aa-108">Example 1</span></span>
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

<span data-ttu-id="580aa-109">Первая команда создает локальный пустой объект обновления моментального снимка с размером 10 ГБ в Premium_LRS типе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="580aa-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="580aa-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="580aa-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="580aa-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="580aa-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="580aa-112">Последняя команда принимает объект обновления моментального снимка и обновляет существующий моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="580aa-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="580aa-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="580aa-113">PARAMETERS</span></span>

### <span data-ttu-id="580aa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="580aa-114">-DefaultProfile</span></span>
<span data-ttu-id="580aa-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="580aa-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="580aa-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="580aa-116">-SecretUrl</span></span>
<span data-ttu-id="580aa-117">Specifes секретный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="580aa-117">Specifes the secret Url.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="580aa-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="580aa-118">-SnapshotUpdate</span></span>
<span data-ttu-id="580aa-119">Указывает локальный объект обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="580aa-119">Specifies a local snapshot update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="580aa-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="580aa-120">-SourceVaultId</span></span>
<span data-ttu-id="580aa-121">Указывает идентификатор исходного хранилища.</span><span class="sxs-lookup"><span data-stu-id="580aa-121">Specifies the source vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="580aa-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="580aa-122">-Confirm</span></span>
<span data-ttu-id="580aa-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="580aa-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="580aa-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="580aa-124">-WhatIf</span></span>
<span data-ttu-id="580aa-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="580aa-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="580aa-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="580aa-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="580aa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="580aa-127">CommonParameters</span></span>
<span data-ttu-id="580aa-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="580aa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="580aa-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="580aa-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="580aa-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="580aa-130">INPUTS</span></span>

### <span data-ttu-id="580aa-131">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="580aa-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="580aa-132">System. String</span><span class="sxs-lookup"><span data-stu-id="580aa-132">System.String</span></span>

## <span data-ttu-id="580aa-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="580aa-133">OUTPUTS</span></span>

### <span data-ttu-id="580aa-134">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="580aa-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="580aa-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="580aa-135">NOTES</span></span>

## <span data-ttu-id="580aa-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="580aa-136">RELATED LINKS</span></span>
