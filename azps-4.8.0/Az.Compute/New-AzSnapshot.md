---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshot.md
ms.openlocfilehash: f22a5b4bc9b30e152827f1914bd03a4a6cee4971
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243107"
---
# <span data-ttu-id="060c3-101">New-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="060c3-101">New-AzSnapshot</span></span>

## <span data-ttu-id="060c3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="060c3-102">SYNOPSIS</span></span>
<span data-ttu-id="060c3-103">Создание снимка.</span><span class="sxs-lookup"><span data-stu-id="060c3-103">Creates a snapshot.</span></span>

## <span data-ttu-id="060c3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="060c3-104">SYNTAX</span></span>

```
New-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="060c3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="060c3-105">DESCRIPTION</span></span>
<span data-ttu-id="060c3-106">Командлет **New-AzSnapshot** создает снимок.</span><span class="sxs-lookup"><span data-stu-id="060c3-106">The **New-AzSnapshot** cmdlet creates a snapshot.</span></span>

## <span data-ttu-id="060c3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="060c3-107">EXAMPLES</span></span>

### <span data-ttu-id="060c3-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="060c3-108">Example 1</span></span>
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

<span data-ttu-id="060c3-109">В первой команде создается локальный пустой объект Snapshot с размером 5GB в Standard_LRS типе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="060c3-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="060c3-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="060c3-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="060c3-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта snapshot.</span><span class="sxs-lookup"><span data-stu-id="060c3-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="060c3-112">Последняя команда принимает объект snapshot и создает моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="060c3-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="060c3-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="060c3-113">PARAMETERS</span></span>

### <span data-ttu-id="060c3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="060c3-114">-AsJob</span></span>
<span data-ttu-id="060c3-115">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="060c3-115">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="060c3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="060c3-116">-DefaultProfile</span></span>
<span data-ttu-id="060c3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="060c3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="060c3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="060c3-118">-ResourceGroupName</span></span>
<span data-ttu-id="060c3-119">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="060c3-119">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="060c3-120">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="060c3-120">-Snapshot</span></span>
<span data-ttu-id="060c3-121">Указывает локальный объект снимка.</span><span class="sxs-lookup"><span data-stu-id="060c3-121">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="060c3-122">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="060c3-122">-SnapshotName</span></span>
<span data-ttu-id="060c3-123">Указывает имя снимка.</span><span class="sxs-lookup"><span data-stu-id="060c3-123">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="060c3-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="060c3-124">-Confirm</span></span>
<span data-ttu-id="060c3-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="060c3-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="060c3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="060c3-126">-WhatIf</span></span>
<span data-ttu-id="060c3-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="060c3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="060c3-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="060c3-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="060c3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="060c3-129">CommonParameters</span></span>
<span data-ttu-id="060c3-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="060c3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="060c3-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="060c3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="060c3-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="060c3-132">INPUTS</span></span>

### <span data-ttu-id="060c3-133">System. String</span><span class="sxs-lookup"><span data-stu-id="060c3-133">System.String</span></span>

### <span data-ttu-id="060c3-134">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="060c3-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="060c3-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="060c3-135">OUTPUTS</span></span>

### <span data-ttu-id="060c3-136">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="060c3-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="060c3-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="060c3-137">NOTES</span></span>

## <span data-ttu-id="060c3-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="060c3-138">RELATED LINKS</span></span>
