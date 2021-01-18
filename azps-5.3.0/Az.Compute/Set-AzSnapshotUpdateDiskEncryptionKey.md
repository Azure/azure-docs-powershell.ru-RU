---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotupdatediskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateDiskEncryptionKey.md
ms.openlocfilehash: b43593650e3eaed25e59526a067c4c569d19d28a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519475"
---
# <span data-ttu-id="ede2f-101">Set-AzSnapshotUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ede2f-101">Set-AzSnapshotUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="ede2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ede2f-102">SYNOPSIS</span></span>
<span data-ttu-id="ede2f-103">Задает свойства ключа шифрования диска для объекта обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="ede2f-103">Sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="ede2f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ede2f-104">SYNTAX</span></span>

```
Set-AzSnapshotUpdateDiskEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ede2f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ede2f-105">DESCRIPTION</span></span>
<span data-ttu-id="ede2f-106">Cmdlet **Set-AzSnapshotUpdateDiskEncryptionKey** задает свойства ключа шифрования диска для объекта обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="ede2f-106">The **Set-AzSnapshotUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="ede2f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ede2f-107">EXAMPLES</span></span>

### <span data-ttu-id="ede2f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ede2f-108">Example 1</span></span>
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

<span data-ttu-id="ede2f-109">Первая команда создает локальный пустой объект обновления моментального снимка с размером 10 ГБ Premium_LRS типа учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="ede2f-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="ede2f-110">Она также задает тип ос Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="ede2f-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="ede2f-111">Вторая и третья команды настраивают параметры ключа шифрования диска и ключа шифрования для объекта обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="ede2f-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="ede2f-112">Последняя команда принимает объект обновления моментального снимка и обновляет существующий моментальный снимок с именем "Моментальный снимок01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="ede2f-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ede2f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ede2f-113">PARAMETERS</span></span>

### <span data-ttu-id="ede2f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ede2f-114">-DefaultProfile</span></span>
<span data-ttu-id="ede2f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ede2f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ede2f-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="ede2f-116">-SecretUrl</span></span>
<span data-ttu-id="ede2f-117">Указывает секретный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="ede2f-117">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="ede2f-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="ede2f-118">-SnapshotUpdate</span></span>
<span data-ttu-id="ede2f-119">Определяет локальный объект обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="ede2f-119">Specifies a local snapshot update object.</span></span>

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

### <span data-ttu-id="ede2f-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="ede2f-120">-SourceVaultId</span></span>
<span data-ttu-id="ede2f-121">Определяет код источника хранилища.</span><span class="sxs-lookup"><span data-stu-id="ede2f-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="ede2f-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ede2f-122">-Confirm</span></span>
<span data-ttu-id="ede2f-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ede2f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ede2f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ede2f-124">-WhatIf</span></span>
<span data-ttu-id="ede2f-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ede2f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ede2f-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ede2f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ede2f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ede2f-127">CommonParameters</span></span>
<span data-ttu-id="ede2f-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ede2f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ede2f-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ede2f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ede2f-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ede2f-130">INPUTS</span></span>

### <span data-ttu-id="ede2f-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="ede2f-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="ede2f-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ede2f-132">System.String</span></span>

## <span data-ttu-id="ede2f-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ede2f-133">OUTPUTS</span></span>

### <span data-ttu-id="ede2f-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="ede2f-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="ede2f-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ede2f-135">NOTES</span></span>

## <span data-ttu-id="ede2f-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ede2f-136">RELATED LINKS</span></span>
