---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
ms.openlocfilehash: 0e95179dcd2b1948b55526f3f2a8bfd5bb1a8834
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504643"
---
# <span data-ttu-id="08fc0-101">Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="08fc0-101">Update-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="08fc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08fc0-102">SYNOPSIS</span></span>
<span data-ttu-id="08fc0-103">Обновляет набор шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="08fc0-103">Updates a disk encryption set.</span></span>

## <span data-ttu-id="08fc0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="08fc0-104">SYNTAX</span></span>

### <span data-ttu-id="08fc0-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="08fc0-105">DefaultParameter (Default)</span></span>
```
Update-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-KeyUrl <String>]
 [-SourceVaultId <String>] [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08fc0-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="08fc0-106">ResourceIdParameter</span></span>
```
Update-AzDiskEncryptionSet [-ResourceId] <String> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="08fc0-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="08fc0-107">ObjectParameter</span></span>
```
Update-AzDiskEncryptionSet [-InputObject] <PSDiskEncryptionSet> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08fc0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="08fc0-108">DESCRIPTION</span></span>
<span data-ttu-id="08fc0-109">Обновляет набор шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="08fc0-109">Updates a disk encryption set.</span></span>

## <span data-ttu-id="08fc0-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="08fc0-110">EXAMPLES</span></span>

### <span data-ttu-id="08fc0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="08fc0-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1;
```

<span data-ttu-id="08fc0-112">Обновляет набор шифрования диска, используя заданный активный ключ в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="08fc0-112">Updates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="08fc0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08fc0-113">PARAMETERS</span></span>

### <span data-ttu-id="08fc0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08fc0-114">-AsJob</span></span>
<span data-ttu-id="08fc0-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="08fc0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="08fc0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08fc0-116">-DefaultProfile</span></span>
<span data-ttu-id="08fc0-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="08fc0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08fc0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08fc0-118">-InputObject</span></span>
<span data-ttu-id="08fc0-119">Локальный объект набора шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="08fc0-119">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: ObjectParameter
Aliases: DiskEncryptionSet

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08fc0-120">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="08fc0-120">-KeyUrl</span></span>
<span data-ttu-id="08fc0-121">URL-адрес, на который указывают активные клавиши в KeyVault</span><span class="sxs-lookup"><span data-stu-id="08fc0-121">Url pointing to the active key in KeyVault</span></span>

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

### <span data-ttu-id="08fc0-122">-Name</span><span class="sxs-lookup"><span data-stu-id="08fc0-122">-Name</span></span>
<span data-ttu-id="08fc0-123">Имя набора шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="08fc0-123">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08fc0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08fc0-124">-ResourceGroupName</span></span>
<span data-ttu-id="08fc0-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="08fc0-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08fc0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08fc0-126">-ResourceId</span></span>
<span data-ttu-id="08fc0-127">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="08fc0-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08fc0-128">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="08fc0-128">-SourceVaultId</span></span>
<span data-ttu-id="08fc0-129">ИД ресурса keyVault, содержащего активный ключ.</span><span class="sxs-lookup"><span data-stu-id="08fc0-129">Resource id of the KeyVault containing the active key.</span></span>

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

### <span data-ttu-id="08fc0-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="08fc0-130">-Tag</span></span>
<span data-ttu-id="08fc0-131">Пары значений ключа в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="08fc0-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="08fc0-132">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="08fc0-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="08fc0-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="08fc0-133">-Confirm</span></span>
<span data-ttu-id="08fc0-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08fc0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08fc0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08fc0-135">-WhatIf</span></span>
<span data-ttu-id="08fc0-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08fc0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08fc0-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="08fc0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08fc0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08fc0-138">CommonParameters</span></span>
<span data-ttu-id="08fc0-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08fc0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08fc0-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="08fc0-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08fc0-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="08fc0-141">INPUTS</span></span>

### <span data-ttu-id="08fc0-142">System.String</span><span class="sxs-lookup"><span data-stu-id="08fc0-142">System.String</span></span>

### <span data-ttu-id="08fc0-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="08fc0-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

### <span data-ttu-id="08fc0-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="08fc0-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="08fc0-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="08fc0-145">OUTPUTS</span></span>

### <span data-ttu-id="08fc0-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="08fc0-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="08fc0-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="08fc0-147">NOTES</span></span>

## <span data-ttu-id="08fc0-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="08fc0-148">RELATED LINKS</span></span>
