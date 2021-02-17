---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotkeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotKeyEncryptionKey.md
ms.openlocfilehash: c8a3ce4f0e21ac12f73fbcef6a4cb6c3b6b65bad
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233257"
---
# <span data-ttu-id="9a5da-101">Set-AzSnapshotKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="9a5da-101">Set-AzSnapshotKeyEncryptionKey</span></span>

## <span data-ttu-id="9a5da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a5da-102">SYNOPSIS</span></span>
<span data-ttu-id="9a5da-103">Задает свойства ключа шифрования ключа для объекта моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="9a5da-103">Sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="9a5da-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9a5da-104">SYNTAX</span></span>

```
Set-AzSnapshotKeyEncryptionKey [-Snapshot] <PSSnapshot> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a5da-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a5da-105">DESCRIPTION</span></span>
<span data-ttu-id="9a5da-106">Cmdlet **Set-AzSnapshotKeyEncryptionKey** задает свойства ключа шифрования ключа для объекта моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="9a5da-106">The **Set-AzSnapshotKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="9a5da-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9a5da-107">EXAMPLES</span></span>

### <span data-ttu-id="9a5da-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9a5da-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="9a5da-109">Первая команда создает локальный пустой объект моментального снимка с размером 5 ГБ Standard_LRS типа учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="9a5da-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="9a5da-110">Она также задает тип ос Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="9a5da-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="9a5da-111">Вторая и третья команды настраивают параметры ключа шифрования диска и ключа шифрования для объекта моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="9a5da-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="9a5da-112">Последняя команда принимает объект моментального снимка и создает моментальный снимок с именем "Моментальный снимок01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="9a5da-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="9a5da-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a5da-113">PARAMETERS</span></span>

### <span data-ttu-id="9a5da-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a5da-114">-DefaultProfile</span></span>
<span data-ttu-id="9a5da-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9a5da-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a5da-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="9a5da-116">-KeyUrl</span></span>
<span data-ttu-id="9a5da-117">Указывает URL-адрес ключа.</span><span class="sxs-lookup"><span data-stu-id="9a5da-117">Specifies the key Url.</span></span>

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

### <span data-ttu-id="9a5da-118">-Моментальный снимок</span><span class="sxs-lookup"><span data-stu-id="9a5da-118">-Snapshot</span></span>
<span data-ttu-id="9a5da-119">Определяет локальный объект моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="9a5da-119">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a5da-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="9a5da-120">-SourceVaultId</span></span>
<span data-ttu-id="9a5da-121">Определяет код источника хранилища.</span><span class="sxs-lookup"><span data-stu-id="9a5da-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="9a5da-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a5da-122">-Confirm</span></span>
<span data-ttu-id="9a5da-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a5da-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a5da-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a5da-124">-WhatIf</span></span>
<span data-ttu-id="9a5da-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a5da-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a5da-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9a5da-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a5da-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a5da-127">CommonParameters</span></span>
<span data-ttu-id="9a5da-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a5da-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a5da-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a5da-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a5da-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9a5da-130">INPUTS</span></span>

### <span data-ttu-id="9a5da-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="9a5da-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="9a5da-132">System.String</span><span class="sxs-lookup"><span data-stu-id="9a5da-132">System.String</span></span>

## <span data-ttu-id="9a5da-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9a5da-133">OUTPUTS</span></span>

### <span data-ttu-id="9a5da-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="9a5da-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="9a5da-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9a5da-135">NOTES</span></span>

## <span data-ttu-id="9a5da-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a5da-136">RELATED LINKS</span></span>
