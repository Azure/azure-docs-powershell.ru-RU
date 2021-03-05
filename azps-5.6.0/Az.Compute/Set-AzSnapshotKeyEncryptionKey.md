---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azsnapshotkeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotKeyEncryptionKey.md
ms.openlocfilehash: c03056d9e563d9c96df54e1d3e37d4c9f86dc572
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007016"
---
# <span data-ttu-id="bc5b8-101">Set-AzSnapshotKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="bc5b8-101">Set-AzSnapshotKeyEncryptionKey</span></span>

## <span data-ttu-id="bc5b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc5b8-102">SYNOPSIS</span></span>
<span data-ttu-id="bc5b8-103">Задает свойства ключа шифрования ключа для объекта моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="bc5b8-103">Sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="bc5b8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bc5b8-104">SYNTAX</span></span>

```
Set-AzSnapshotKeyEncryptionKey [-Snapshot] <PSSnapshot> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc5b8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc5b8-105">DESCRIPTION</span></span>
<span data-ttu-id="bc5b8-106">Cmdlet **Set-AzSnapshotKeyEncryptionKey** задает свойства ключа шифрования ключа для объекта моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="bc5b8-106">The **Set-AzSnapshotKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="bc5b8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bc5b8-107">EXAMPLES</span></span>

### <span data-ttu-id="bc5b8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bc5b8-108">Example 1</span></span>
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

<span data-ttu-id="bc5b8-109">Первая команда создает локальный пустой объект моментального снимка размером 5 ГБ Standard_LRS типа учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="bc5b8-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="bc5b8-110">Она также задает тип ос Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="bc5b8-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="bc5b8-111">Вторая и третья команды настраивают параметры ключа шифрования диска и ключа шифрования для объекта моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="bc5b8-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="bc5b8-112">Последняя команда принимает объект моментального снимка и создает моментальный снимок с именем "Снимок01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="bc5b8-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="bc5b8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc5b8-113">PARAMETERS</span></span>

### <span data-ttu-id="bc5b8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc5b8-114">-DefaultProfile</span></span>
<span data-ttu-id="bc5b8-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bc5b8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc5b8-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="bc5b8-116">-KeyUrl</span></span>
<span data-ttu-id="bc5b8-117">Указывает URL-адрес ключа.</span><span class="sxs-lookup"><span data-stu-id="bc5b8-117">Specifies the key Url.</span></span>

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

### <span data-ttu-id="bc5b8-118">-Моментальный снимок</span><span class="sxs-lookup"><span data-stu-id="bc5b8-118">-Snapshot</span></span>
<span data-ttu-id="bc5b8-119">Определяет локальный объект моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="bc5b8-119">Specifies a local snapshot object.</span></span>

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

### <span data-ttu-id="bc5b8-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="bc5b8-120">-SourceVaultId</span></span>
<span data-ttu-id="bc5b8-121">Определяет код источника хранилища.</span><span class="sxs-lookup"><span data-stu-id="bc5b8-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="bc5b8-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc5b8-122">-Confirm</span></span>
<span data-ttu-id="bc5b8-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc5b8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc5b8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc5b8-124">-WhatIf</span></span>
<span data-ttu-id="bc5b8-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc5b8-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc5b8-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bc5b8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc5b8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc5b8-127">CommonParameters</span></span>
<span data-ttu-id="bc5b8-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc5b8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc5b8-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc5b8-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc5b8-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bc5b8-130">INPUTS</span></span>

### <span data-ttu-id="bc5b8-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="bc5b8-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="bc5b8-132">System.String</span><span class="sxs-lookup"><span data-stu-id="bc5b8-132">System.String</span></span>

## <span data-ttu-id="bc5b8-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bc5b8-133">OUTPUTS</span></span>

### <span data-ttu-id="bc5b8-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="bc5b8-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="bc5b8-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bc5b8-135">NOTES</span></span>

## <span data-ttu-id="bc5b8-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc5b8-136">RELATED LINKS</span></span>
