---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5141D84C-3C58-42B9-890F-C3C9049BC1C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclusterdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
ms.openlocfilehash: b3421fa4382912d11a3e3a28b81acffb7be123a2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311837"
---
# <span data-ttu-id="94a52-101">Set-AzHDInsightClusterDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="94a52-101">Set-AzHDInsightClusterDiskEncryptionKey</span></span>

## <span data-ttu-id="94a52-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="94a52-102">SYNOPSIS</span></span>
<span data-ttu-id="94a52-103">Поворачивает ключ шифрования диска для указанного кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="94a52-103">Rotates the disk encryption key of the specified HDInsight cluster.</span></span>

## <span data-ttu-id="94a52-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="94a52-104">SYNTAX</span></span>

### <span data-ttu-id="94a52-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="94a52-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceGroupName] <String> [-Name] <String>
 -EncryptionKeyName <String> -EncryptionKeyVersion <String> -EncryptionVaultUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94a52-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94a52-106">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceId] <String> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94a52-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="94a52-107">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-InputObject] <AzureHDInsightCluster> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94a52-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94a52-108">DESCRIPTION</span></span>
<span data-ttu-id="94a52-109">Поворот ключа шифрования диска для указанного кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="94a52-109">Rotate the disk encryption key of the specified HDInsight cluster.</span></span> <span data-ttu-id="94a52-110">Для этой операции кластер должен иметь доступ к текущему ключу и предполагаемому новому ключу, в противном случае произойдет сбой операции с клавишей "поворот".</span><span class="sxs-lookup"><span data-stu-id="94a52-110">For this operation, the cluster must have access to both the current key and the intended new key, otherwise the rotate key operation will fail.</span></span>

## <span data-ttu-id="94a52-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="94a52-111">EXAMPLES</span></span>

### <span data-ttu-id="94a52-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="94a52-112">Example 1</span></span>
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

### <span data-ttu-id="94a52-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="94a52-113">Example 2</span></span>
```powershell
PS C:\> # Cluster configuration info
        $clusterName = "your-cmk-cluster"

$cluster= Get-AzHDInsightCluster -ClusterName $clusterName 
$cluster |  Set-AzHDInsightClusterDiskEncryptionKey `
    -EncryptionKeyName new-key `
    -EncryptionVaultUri https://MyKeyVault.vault.azure.net `
    -EncryptionKeyVersion 00000000000000000000000000000000
```

## <span data-ttu-id="94a52-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="94a52-114">PARAMETERS</span></span>

### <span data-ttu-id="94a52-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94a52-115">-DefaultProfile</span></span>
<span data-ttu-id="94a52-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="94a52-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94a52-117">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="94a52-117">-EncryptionKeyName</span></span>
<span data-ttu-id="94a52-118">Возвращает или задает имя ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="94a52-118">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="94a52-119">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="94a52-119">-EncryptionKeyVersion</span></span>
<span data-ttu-id="94a52-120">Возвращает или задает версию ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="94a52-120">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="94a52-121">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="94a52-121">-EncryptionVaultUri</span></span>
<span data-ttu-id="94a52-122">Возвращает или задает универсальный код ресурса (URI) для хранилища шифрования.</span><span class="sxs-lookup"><span data-stu-id="94a52-122">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="94a52-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94a52-123">-InputObject</span></span>
<span data-ttu-id="94a52-124">Возвращает или задает объект ввода.</span><span class="sxs-lookup"><span data-stu-id="94a52-124">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="94a52-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="94a52-125">-Name</span></span>
<span data-ttu-id="94a52-126">Возвращает или задает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="94a52-126">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="94a52-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94a52-127">-ResourceGroupName</span></span>
<span data-ttu-id="94a52-128">Возвращает или задает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94a52-128">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="94a52-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94a52-129">-ResourceId</span></span>
<span data-ttu-id="94a52-130">Возвращает или задает идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="94a52-130">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="94a52-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94a52-131">-Confirm</span></span>
<span data-ttu-id="94a52-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="94a52-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94a52-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94a52-133">-WhatIf</span></span>
<span data-ttu-id="94a52-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="94a52-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94a52-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="94a52-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94a52-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94a52-136">CommonParameters</span></span>
<span data-ttu-id="94a52-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="94a52-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94a52-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94a52-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94a52-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="94a52-139">INPUTS</span></span>

### <span data-ttu-id="94a52-140">Ничего</span><span class="sxs-lookup"><span data-stu-id="94a52-140">None</span></span>

## <span data-ttu-id="94a52-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="94a52-141">OUTPUTS</span></span>

### <span data-ttu-id="94a52-142">Microsoft. Azure. Management. HDInsight. Models. Cluster</span><span class="sxs-lookup"><span data-stu-id="94a52-142">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="94a52-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="94a52-143">NOTES</span></span>

## <span data-ttu-id="94a52-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94a52-144">RELATED LINKS</span></span>

[<span data-ttu-id="94a52-145">Шифрование диска с управляемым ключом пользователя</span><span class="sxs-lookup"><span data-stu-id="94a52-145">Customer-managed key disk encryption</span></span>](https://docs.microsoft.com/en-us/azure/hdinsight/disk-encryption)
