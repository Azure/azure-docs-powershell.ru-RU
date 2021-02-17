---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotupdatekeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateKeyEncryptionKey.md
ms.openlocfilehash: a7a52aaa97518fd239e35ea7cf8e4d60689d8888
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238673"
---
# <span data-ttu-id="8a8b6-101">Set-AzSnapshotUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="8a8b6-101">Set-AzSnapshotUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="8a8b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a8b6-102">SYNOPSIS</span></span>
<span data-ttu-id="8a8b6-103">Задает свойства ключа шифрования ключа для объекта обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="8a8b6-103">Sets the key encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="8a8b6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8a8b6-104">SYNTAX</span></span>

```
Set-AzSnapshotUpdateKeyEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-KeyUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8a8b6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a8b6-105">DESCRIPTION</span></span>
<span data-ttu-id="8a8b6-106">Cmdlet **Set-AzSnapshotUpdateKeyEncryptionKey** задает свойства ключа шифрования ключа для объекта обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="8a8b6-106">The **Set-AzSnapshotUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="8a8b6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8a8b6-107">EXAMPLES</span></span>

### <span data-ttu-id="8a8b6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8a8b6-108">Example 1</span></span>
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

<span data-ttu-id="8a8b6-109">Первая команда создает локальный пустой объект обновления моментального снимка с размером 10 ГБ Premium_LRS типа учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="8a8b6-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="8a8b6-110">Она также задает тип ОС Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="8a8b6-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="8a8b6-111">Вторая и третья команды настраивают параметры ключа шифрования диска и ключа шифрования для объекта обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="8a8b6-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="8a8b6-112">Последняя команда принимает объект обновления моментального снимка и обновляет существующий моментальный снимок с именем "Моментальный снимок01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="8a8b6-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="8a8b6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a8b6-113">PARAMETERS</span></span>

### <span data-ttu-id="8a8b6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a8b6-114">-DefaultProfile</span></span>
<span data-ttu-id="8a8b6-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8a8b6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a8b6-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="8a8b6-116">-KeyUrl</span></span>
<span data-ttu-id="8a8b6-117">Указывает URL-адрес ключа.</span><span class="sxs-lookup"><span data-stu-id="8a8b6-117">Specifies the key Url.</span></span>

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

### <span data-ttu-id="8a8b6-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="8a8b6-118">-SnapshotUpdate</span></span>
<span data-ttu-id="8a8b6-119">Определяет локальный объект обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="8a8b6-119">Specifies a local snapshot update object.</span></span>

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

### <span data-ttu-id="8a8b6-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="8a8b6-120">-SourceVaultId</span></span>
<span data-ttu-id="8a8b6-121">Определяет код источника хранилища.</span><span class="sxs-lookup"><span data-stu-id="8a8b6-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="8a8b6-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8a8b6-122">-Confirm</span></span>
<span data-ttu-id="8a8b6-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a8b6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a8b6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a8b6-124">-WhatIf</span></span>
<span data-ttu-id="8a8b6-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a8b6-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8a8b6-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8a8b6-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a8b6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a8b6-127">CommonParameters</span></span>
<span data-ttu-id="8a8b6-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a8b6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a8b6-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a8b6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a8b6-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8a8b6-130">INPUTS</span></span>

### <span data-ttu-id="8a8b6-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="8a8b6-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="8a8b6-132">System.String</span><span class="sxs-lookup"><span data-stu-id="8a8b6-132">System.String</span></span>

## <span data-ttu-id="8a8b6-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8a8b6-133">OUTPUTS</span></span>

### <span data-ttu-id="8a8b6-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="8a8b6-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="8a8b6-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8a8b6-135">NOTES</span></span>

## <span data-ttu-id="8a8b6-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a8b6-136">RELATED LINKS</span></span>
