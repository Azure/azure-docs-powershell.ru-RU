---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionsetconfig.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
ms.openlocfilehash: bfcb306b12c047c9207e0ef2f1d82bf6eaffc4d3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391204"
---
# <span data-ttu-id="82173-101">New-AzDiskEncryptionSetConfig</span><span class="sxs-lookup"><span data-stu-id="82173-101">New-AzDiskEncryptionSetConfig</span></span>

## <span data-ttu-id="82173-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82173-102">SYNOPSIS</span></span>
<span data-ttu-id="82173-103">Создание настраиваемого объекта набора шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="82173-103">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="82173-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="82173-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSetConfig [-Location] <String> [[-Tag] <Hashtable>] [[-IdentityType] <String>]
 [[-SourceVaultId] <String>] [-KeyUrl <String>] [-EncryptionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82173-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82173-105">DESCRIPTION</span></span>
<span data-ttu-id="82173-106">Создание настраиваемого объекта набора шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="82173-106">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="82173-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="82173-107">EXAMPLES</span></span>

### <span data-ttu-id="82173-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="82173-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="82173-109">Создает набор шифрования диска с помощью заданного активного ключа в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="82173-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="82173-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82173-110">PARAMETERS</span></span>

### <span data-ttu-id="82173-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82173-111">-DefaultProfile</span></span>
<span data-ttu-id="82173-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="82173-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82173-113">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="82173-113">-EncryptionType</span></span>
<span data-ttu-id="82173-114">Этот код используется для того, чтобы настроить тип шифрования набора шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="82173-114">Use this to set the encryption type of the disk encryption set.</span></span> <span data-ttu-id="82173-115">Доступны такие значения: EncryptionAtRestWithPlatformKey, "EncryptionAtRestWithCustomerKey".</span><span class="sxs-lookup"><span data-stu-id="82173-115">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82173-116">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="82173-116">-IdentityType</span></span>
<span data-ttu-id="82173-117">Тип управляемого удостоверения, используемого набором DiskEncryptionSet.</span><span class="sxs-lookup"><span data-stu-id="82173-117">The type of Managed Identity used by the DiskEncryptionSet.</span></span> <span data-ttu-id="82173-118">Поддерживается только systemAssigned.</span><span class="sxs-lookup"><span data-stu-id="82173-118">Only SystemAssigned is supported.</span></span>

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

### <span data-ttu-id="82173-119">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="82173-119">-KeyUrl</span></span>
<span data-ttu-id="82173-120">URL-адрес, на который указывают активные клавиши в KeyVault</span><span class="sxs-lookup"><span data-stu-id="82173-120">Url pointing to the active key in KeyVault</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82173-121">-Location</span><span class="sxs-lookup"><span data-stu-id="82173-121">-Location</span></span>
<span data-ttu-id="82173-122">Определяет расположение.</span><span class="sxs-lookup"><span data-stu-id="82173-122">Specifies a location.</span></span>

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

### <span data-ttu-id="82173-123">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="82173-123">-SourceVaultId</span></span>
<span data-ttu-id="82173-124">ИД ресурса keyVault, содержащего активный ключ.</span><span class="sxs-lookup"><span data-stu-id="82173-124">Resource id of the KeyVault containing the active key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82173-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="82173-125">-Tag</span></span>
<span data-ttu-id="82173-126">Пары "ключевое значение" в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="82173-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="82173-127">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="82173-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82173-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82173-128">-Confirm</span></span>
<span data-ttu-id="82173-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82173-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82173-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82173-130">-WhatIf</span></span>
<span data-ttu-id="82173-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82173-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82173-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="82173-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82173-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82173-133">CommonParameters</span></span>
<span data-ttu-id="82173-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82173-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82173-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82173-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82173-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82173-136">INPUTS</span></span>

### <span data-ttu-id="82173-137">System.String</span><span class="sxs-lookup"><span data-stu-id="82173-137">System.String</span></span>

### <span data-ttu-id="82173-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="82173-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="82173-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="82173-139">OUTPUTS</span></span>

### <span data-ttu-id="82173-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="82173-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="82173-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="82173-141">NOTES</span></span>

## <span data-ttu-id="82173-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82173-142">RELATED LINKS</span></span>
