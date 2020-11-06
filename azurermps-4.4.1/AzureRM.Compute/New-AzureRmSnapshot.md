---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshot.md
ms.openlocfilehash: c7d88f16ff9eb6bb32cdf286ef37a1aba17030cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569648"
---
# <span data-ttu-id="be534-101">New-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="be534-101">New-AzureRmSnapshot</span></span>

## <span data-ttu-id="be534-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="be534-102">SYNOPSIS</span></span>
<span data-ttu-id="be534-103">Создание снимка.</span><span class="sxs-lookup"><span data-stu-id="be534-103">Creates a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be534-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="be534-104">SYNTAX</span></span>

```
New-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be534-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be534-105">DESCRIPTION</span></span>
<span data-ttu-id="be534-106">Командлет **New-AzureRmSnapshot** создает снимок.</span><span class="sxs-lookup"><span data-stu-id="be534-106">The **New-AzureRmSnapshot** cmdlet creates a snapshot.</span></span>

## <span data-ttu-id="be534-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="be534-107">EXAMPLES</span></span>

### <span data-ttu-id="be534-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="be534-108">Example 1</span></span>
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

<span data-ttu-id="be534-109">В первой команде создается локальный пустой объект Snapshot с размером 5GB в Standard_LRS типе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="be534-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="be534-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="be534-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="be534-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта snapshot.</span><span class="sxs-lookup"><span data-stu-id="be534-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="be534-112">Последняя команда принимает объект snapshot и создает моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="be534-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="be534-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="be534-113">PARAMETERS</span></span>

### <span data-ttu-id="be534-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be534-114">-DefaultProfile</span></span>
<span data-ttu-id="be534-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="be534-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be534-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be534-116">-ResourceGroupName</span></span>
<span data-ttu-id="be534-117">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="be534-117">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be534-118">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="be534-118">-Snapshot</span></span>
<span data-ttu-id="be534-119">Указывает локальный объект снимка.</span><span class="sxs-lookup"><span data-stu-id="be534-119">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be534-120">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="be534-120">-SnapshotName</span></span>
<span data-ttu-id="be534-121">Указывает имя снимка.</span><span class="sxs-lookup"><span data-stu-id="be534-121">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be534-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be534-122">-Confirm</span></span>
<span data-ttu-id="be534-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="be534-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be534-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be534-124">-WhatIf</span></span>
<span data-ttu-id="be534-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="be534-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be534-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="be534-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be534-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be534-127">CommonParameters</span></span>
<span data-ttu-id="be534-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="be534-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be534-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be534-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be534-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="be534-130">INPUTS</span></span>

### <span data-ttu-id="be534-131">System. String</span><span class="sxs-lookup"><span data-stu-id="be534-131">System.String</span></span>
<span data-ttu-id="be534-132">Microsoft. Azure. Management. COMPUTE. Models. Snapshot</span><span class="sxs-lookup"><span data-stu-id="be534-132">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="be534-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="be534-133">OUTPUTS</span></span>

### <span data-ttu-id="be534-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="be534-134">System.Object</span></span>

## <span data-ttu-id="be534-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="be534-135">NOTES</span></span>

## <span data-ttu-id="be534-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be534-136">RELATED LINKS</span></span>

