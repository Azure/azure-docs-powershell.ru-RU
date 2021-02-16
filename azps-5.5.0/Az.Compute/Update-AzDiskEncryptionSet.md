---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
ms.openlocfilehash: 0e95179dcd2b1948b55526f3f2a8bfd5bb1a8834
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211473"
---
# <span data-ttu-id="1a479-101">Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="1a479-101">Update-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="1a479-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a479-102">SYNOPSIS</span></span>
<span data-ttu-id="1a479-103">Обновляет набор шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="1a479-103">Updates a disk encryption set.</span></span>

## <span data-ttu-id="1a479-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1a479-104">SYNTAX</span></span>

### <span data-ttu-id="1a479-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1a479-105">DefaultParameter (Default)</span></span>
```
Update-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-KeyUrl <String>]
 [-SourceVaultId <String>] [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a479-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="1a479-106">ResourceIdParameter</span></span>
```
Update-AzDiskEncryptionSet [-ResourceId] <String> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a479-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="1a479-107">ObjectParameter</span></span>
```
Update-AzDiskEncryptionSet [-InputObject] <PSDiskEncryptionSet> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1a479-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a479-108">DESCRIPTION</span></span>
<span data-ttu-id="1a479-109">Обновляет набор шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="1a479-109">Updates a disk encryption set.</span></span>

## <span data-ttu-id="1a479-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1a479-110">EXAMPLES</span></span>

### <span data-ttu-id="1a479-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1a479-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1;
```

<span data-ttu-id="1a479-112">Обновляет набор шифрования диска, используя заданный активный ключ в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="1a479-112">Updates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="1a479-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a479-113">PARAMETERS</span></span>

### <span data-ttu-id="1a479-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a479-114">-AsJob</span></span>
<span data-ttu-id="1a479-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1a479-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a479-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a479-116">-DefaultProfile</span></span>
<span data-ttu-id="1a479-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1a479-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a479-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a479-118">-InputObject</span></span>
<span data-ttu-id="1a479-119">Локальный объект набора шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="1a479-119">The local object of the disk encryption set.</span></span>

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

### <span data-ttu-id="1a479-120">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="1a479-120">-KeyUrl</span></span>
<span data-ttu-id="1a479-121">URL-адрес, на который указывают активные клавиши в KeyVault</span><span class="sxs-lookup"><span data-stu-id="1a479-121">Url pointing to the active key in KeyVault</span></span>

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

### <span data-ttu-id="1a479-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1a479-122">-Name</span></span>
<span data-ttu-id="1a479-123">Имя набора шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="1a479-123">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="1a479-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a479-124">-ResourceGroupName</span></span>
<span data-ttu-id="1a479-125">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1a479-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1a479-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a479-126">-ResourceId</span></span>
<span data-ttu-id="1a479-127">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="1a479-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="1a479-128">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="1a479-128">-SourceVaultId</span></span>
<span data-ttu-id="1a479-129">ИД ресурса keyVault, содержащего активный ключ.</span><span class="sxs-lookup"><span data-stu-id="1a479-129">Resource id of the KeyVault containing the active key.</span></span>

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

### <span data-ttu-id="1a479-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="1a479-130">-Tag</span></span>
<span data-ttu-id="1a479-131">Пары "ключевое значение" в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="1a479-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1a479-132">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="1a479-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1a479-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a479-133">-Confirm</span></span>
<span data-ttu-id="1a479-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1a479-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a479-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a479-135">-WhatIf</span></span>
<span data-ttu-id="1a479-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a479-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a479-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1a479-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a479-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a479-138">CommonParameters</span></span>
<span data-ttu-id="1a479-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a479-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a479-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a479-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a479-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1a479-141">INPUTS</span></span>

### <span data-ttu-id="1a479-142">System.String</span><span class="sxs-lookup"><span data-stu-id="1a479-142">System.String</span></span>

### <span data-ttu-id="1a479-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="1a479-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

### <span data-ttu-id="1a479-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1a479-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1a479-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1a479-145">OUTPUTS</span></span>

### <span data-ttu-id="1a479-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="1a479-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="1a479-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1a479-147">NOTES</span></span>

## <span data-ttu-id="1a479-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a479-148">RELATED LINKS</span></span>
