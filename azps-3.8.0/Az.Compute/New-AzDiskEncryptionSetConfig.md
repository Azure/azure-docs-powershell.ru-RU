---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionsetconfig.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
ms.openlocfilehash: 5d38a1104d1f2d1f569560027c540a2c8605bdae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065937"
---
# <span data-ttu-id="6a23e-101">New-AzDiskEncryptionSetConfig</span><span class="sxs-lookup"><span data-stu-id="6a23e-101">New-AzDiskEncryptionSetConfig</span></span>

## <span data-ttu-id="6a23e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6a23e-102">SYNOPSIS</span></span>
<span data-ttu-id="6a23e-103">Создание настраиваемого объекта с набором шифрования дисков.</span><span class="sxs-lookup"><span data-stu-id="6a23e-103">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="6a23e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6a23e-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSetConfig [-Location] <String> [[-Tag] <Hashtable>] [[-IdentityType] <String>]
 [[-SourceVaultId] <String>] [-KeyUrl <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6a23e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a23e-105">DESCRIPTION</span></span>
<span data-ttu-id="6a23e-106">Создание настраиваемого объекта с набором шифрования дисков.</span><span class="sxs-lookup"><span data-stu-id="6a23e-106">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="6a23e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6a23e-107">EXAMPLES</span></span>

### <span data-ttu-id="6a23e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6a23e-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="6a23e-109">Создание шифрования диска с помощью заданного активного ключа в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="6a23e-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="6a23e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6a23e-110">PARAMETERS</span></span>

### <span data-ttu-id="6a23e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a23e-111">-DefaultProfile</span></span>
<span data-ttu-id="6a23e-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6a23e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a23e-113">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="6a23e-113">-IdentityType</span></span>
<span data-ttu-id="6a23e-114">Тип управляемого удостоверения, используемого DiskEncryptionSet.</span><span class="sxs-lookup"><span data-stu-id="6a23e-114">The type of Managed Identity used by the DiskEncryptionSet.</span></span> <span data-ttu-id="6a23e-115">Поддерживается только SystemAssigned.</span><span class="sxs-lookup"><span data-stu-id="6a23e-115">Only SystemAssigned is supported.</span></span>

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

### <span data-ttu-id="6a23e-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="6a23e-116">-KeyUrl</span></span>
<span data-ttu-id="6a23e-117">URL-адрес, указывающий на активный ключ в KeyVault</span><span class="sxs-lookup"><span data-stu-id="6a23e-117">Url pointing to the active key in KeyVault</span></span>

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

### <span data-ttu-id="6a23e-118">-Location</span><span class="sxs-lookup"><span data-stu-id="6a23e-118">-Location</span></span>
<span data-ttu-id="6a23e-119">Задает расположение.</span><span class="sxs-lookup"><span data-stu-id="6a23e-119">Specifies a location.</span></span>

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

### <span data-ttu-id="6a23e-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="6a23e-120">-SourceVaultId</span></span>
<span data-ttu-id="6a23e-121">Идентификатор ресурса KeyVault, содержащего активный ключ.</span><span class="sxs-lookup"><span data-stu-id="6a23e-121">Resource id of the KeyVault containing the active key.</span></span>

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

### <span data-ttu-id="6a23e-122">-Тег</span><span class="sxs-lookup"><span data-stu-id="6a23e-122">-Tag</span></span>
<span data-ttu-id="6a23e-123">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="6a23e-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6a23e-124">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="6a23e-124">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6a23e-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a23e-125">-Confirm</span></span>
<span data-ttu-id="6a23e-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6a23e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a23e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a23e-127">-WhatIf</span></span>
<span data-ttu-id="6a23e-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6a23e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a23e-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6a23e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a23e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a23e-130">CommonParameters</span></span>
<span data-ttu-id="6a23e-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6a23e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a23e-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a23e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a23e-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6a23e-133">INPUTS</span></span>

### <span data-ttu-id="6a23e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6a23e-134">System.String</span></span>

### <span data-ttu-id="6a23e-135">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6a23e-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6a23e-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a23e-136">OUTPUTS</span></span>

### <span data-ttu-id="6a23e-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="6a23e-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="6a23e-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="6a23e-138">NOTES</span></span>

## <span data-ttu-id="6a23e-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6a23e-139">RELATED LINKS</span></span>
