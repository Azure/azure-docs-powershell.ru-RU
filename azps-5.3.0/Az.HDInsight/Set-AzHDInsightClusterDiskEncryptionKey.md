---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5141D84C-3C58-42B9-890F-C3C9049BC1C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclusterdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
ms.openlocfilehash: b3421fa4382912d11a3e3a28b81acffb7be123a2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506292"
---
# <span data-ttu-id="fda80-101">Set-AzHDInsightClusterDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="fda80-101">Set-AzHDInsightClusterDiskEncryptionKey</span></span>

## <span data-ttu-id="fda80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fda80-102">SYNOPSIS</span></span>
<span data-ttu-id="fda80-103">Поворот ключа шифрования диска для указанного кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="fda80-103">Rotates the disk encryption key of the specified HDInsight cluster.</span></span>

## <span data-ttu-id="fda80-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fda80-104">SYNTAX</span></span>

### <span data-ttu-id="fda80-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fda80-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceGroupName] <String> [-Name] <String>
 -EncryptionKeyName <String> -EncryptionKeyVersion <String> -EncryptionVaultUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fda80-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fda80-106">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceId] <String> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fda80-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fda80-107">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-InputObject] <AzureHDInsightCluster> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fda80-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fda80-108">DESCRIPTION</span></span>
<span data-ttu-id="fda80-109">Поверните ключ шифрования диска для указанного кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="fda80-109">Rotate the disk encryption key of the specified HDInsight cluster.</span></span> <span data-ttu-id="fda80-110">Для этой операции кластер должен иметь доступ как к текущему, так и к новому ключу, иначе операция поворота не будет работать.</span><span class="sxs-lookup"><span data-stu-id="fda80-110">For this operation, the cluster must have access to both the current key and the intended new key, otherwise the rotate key operation will fail.</span></span>

## <span data-ttu-id="fda80-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fda80-111">EXAMPLES</span></span>

### <span data-ttu-id="fda80-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fda80-112">Example 1</span></span>
```powershell
PS C:\> # Cluster configuration info
        $clusterResourceGroupName = "Group"
        $clusterName = "your-cmk-cluster"

Set-AzHDInsightClusterDiskEncryptionKey `
        -ResourceGroupName $clusterResourceGroupName `
        -ClusterName $clusterName `
        -EncryptionKeyName new-key `
        -EncryptionVaultUri https://MyKeyVault.vault.azure.net `
        -EncryptionKeyVersion 00000000000000000000000000000000
```

### <span data-ttu-id="fda80-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fda80-113">Example 2</span></span>
```powershell
PS C:\> # Cluster configuration info
        $clusterName = "your-cmk-cluster"

$cluster= Get-AzHDInsightCluster -ClusterName $clusterName 
$cluster |  Set-AzHDInsightClusterDiskEncryptionKey `
    -EncryptionKeyName new-key `
    -EncryptionVaultUri https://MyKeyVault.vault.azure.net `
    -EncryptionKeyVersion 00000000000000000000000000000000
```

## <span data-ttu-id="fda80-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fda80-114">PARAMETERS</span></span>

### <span data-ttu-id="fda80-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fda80-115">-DefaultProfile</span></span>
<span data-ttu-id="fda80-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fda80-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fda80-117">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="fda80-117">-EncryptionKeyName</span></span>
<span data-ttu-id="fda80-118">Получает или задает имя ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="fda80-118">Gets or sets the encryption key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fda80-119">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="fda80-119">-EncryptionKeyVersion</span></span>
<span data-ttu-id="fda80-120">Возвращает или задает версию ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="fda80-120">Gets or sets the encryption key version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fda80-121">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="fda80-121">-EncryptionVaultUri</span></span>
<span data-ttu-id="fda80-122">Получает или задает uri хранилища шифрования.</span><span class="sxs-lookup"><span data-stu-id="fda80-122">Gets or sets the encryption vault uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fda80-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fda80-123">-InputObject</span></span>
<span data-ttu-id="fda80-124">Возвращает или задает объект ввода.</span><span class="sxs-lookup"><span data-stu-id="fda80-124">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fda80-125">-Name</span><span class="sxs-lookup"><span data-stu-id="fda80-125">-Name</span></span>
<span data-ttu-id="fda80-126">Возвращает или задает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="fda80-126">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fda80-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fda80-127">-ResourceGroupName</span></span>
<span data-ttu-id="fda80-128">Возвращает или задает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fda80-128">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fda80-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fda80-129">-ResourceId</span></span>
<span data-ttu-id="fda80-130">Возвращает или задает ид ресурса.</span><span class="sxs-lookup"><span data-stu-id="fda80-130">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fda80-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fda80-131">-Confirm</span></span>
<span data-ttu-id="fda80-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="fda80-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fda80-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fda80-133">-WhatIf</span></span>
<span data-ttu-id="fda80-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fda80-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fda80-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fda80-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fda80-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fda80-136">CommonParameters</span></span>
<span data-ttu-id="fda80-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fda80-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fda80-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fda80-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fda80-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fda80-139">INPUTS</span></span>

### <span data-ttu-id="fda80-140">Нет</span><span class="sxs-lookup"><span data-stu-id="fda80-140">None</span></span>

## <span data-ttu-id="fda80-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fda80-141">OUTPUTS</span></span>

### <span data-ttu-id="fda80-142">Microsoft.Azure.Management.HDInsight.Models.Cluster</span><span class="sxs-lookup"><span data-stu-id="fda80-142">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="fda80-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fda80-143">NOTES</span></span>

## <span data-ttu-id="fda80-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fda80-144">RELATED LINKS</span></span>

[<span data-ttu-id="fda80-145">Шифрование диска под управлением клиента</span><span class="sxs-lookup"><span data-stu-id="fda80-145">Customer-managed key disk encryption</span></span>](https://docs.microsoft.com/en-us/azure/hdinsight/disk-encryption)
