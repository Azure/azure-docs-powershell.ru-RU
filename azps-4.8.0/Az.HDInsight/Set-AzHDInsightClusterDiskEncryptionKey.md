---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5141D84C-3C58-42B9-890F-C3C9049BC1C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclusterdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
ms.openlocfilehash: b3421fa4382912d11a3e3a28b81acffb7be123a2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243386"
---
# <span data-ttu-id="ea900-101">Set-AzHDInsightClusterDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ea900-101">Set-AzHDInsightClusterDiskEncryptionKey</span></span>

## <span data-ttu-id="ea900-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ea900-102">SYNOPSIS</span></span>
<span data-ttu-id="ea900-103">Поворачивает ключ шифрования диска для указанного кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ea900-103">Rotates the disk encryption key of the specified HDInsight cluster.</span></span>

## <span data-ttu-id="ea900-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ea900-104">SYNTAX</span></span>

### <span data-ttu-id="ea900-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ea900-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceGroupName] <String> [-Name] <String>
 -EncryptionKeyName <String> -EncryptionKeyVersion <String> -EncryptionVaultUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea900-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea900-106">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceId] <String> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea900-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea900-107">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-InputObject] <AzureHDInsightCluster> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea900-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea900-108">DESCRIPTION</span></span>
<span data-ttu-id="ea900-109">Поворот ключа шифрования диска для указанного кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ea900-109">Rotate the disk encryption key of the specified HDInsight cluster.</span></span> <span data-ttu-id="ea900-110">Для этой операции кластер должен иметь доступ к текущему ключу и предполагаемому новому ключу, в противном случае произойдет сбой операции с клавишей "поворот".</span><span class="sxs-lookup"><span data-stu-id="ea900-110">For this operation, the cluster must have access to both the current key and the intended new key, otherwise the rotate key operation will fail.</span></span>

## <span data-ttu-id="ea900-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ea900-111">EXAMPLES</span></span>

### <span data-ttu-id="ea900-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ea900-112">Example 1</span></span>
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

### <span data-ttu-id="ea900-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ea900-113">Example 2</span></span>
```powershell
PS C:\> # Cluster configuration info
        $clusterName = "your-cmk-cluster"

$cluster= Get-AzHDInsightCluster -ClusterName $clusterName 
$cluster |  Set-AzHDInsightClusterDiskEncryptionKey `
    -EncryptionKeyName new-key `
    -EncryptionVaultUri https://MyKeyVault.vault.azure.net `
    -EncryptionKeyVersion 00000000000000000000000000000000
```

## <span data-ttu-id="ea900-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ea900-114">PARAMETERS</span></span>

### <span data-ttu-id="ea900-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea900-115">-DefaultProfile</span></span>
<span data-ttu-id="ea900-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ea900-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea900-117">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="ea900-117">-EncryptionKeyName</span></span>
<span data-ttu-id="ea900-118">Возвращает или задает имя ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="ea900-118">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="ea900-119">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="ea900-119">-EncryptionKeyVersion</span></span>
<span data-ttu-id="ea900-120">Возвращает или задает версию ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="ea900-120">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="ea900-121">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="ea900-121">-EncryptionVaultUri</span></span>
<span data-ttu-id="ea900-122">Возвращает или задает универсальный код ресурса (URI) для хранилища шифрования.</span><span class="sxs-lookup"><span data-stu-id="ea900-122">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="ea900-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea900-123">-InputObject</span></span>
<span data-ttu-id="ea900-124">Возвращает или задает объект ввода.</span><span class="sxs-lookup"><span data-stu-id="ea900-124">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="ea900-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ea900-125">-Name</span></span>
<span data-ttu-id="ea900-126">Возвращает или задает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="ea900-126">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="ea900-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea900-127">-ResourceGroupName</span></span>
<span data-ttu-id="ea900-128">Возвращает или задает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ea900-128">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="ea900-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea900-129">-ResourceId</span></span>
<span data-ttu-id="ea900-130">Возвращает или задает идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="ea900-130">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="ea900-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea900-131">-Confirm</span></span>
<span data-ttu-id="ea900-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ea900-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea900-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea900-133">-WhatIf</span></span>
<span data-ttu-id="ea900-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ea900-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea900-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ea900-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea900-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea900-136">CommonParameters</span></span>
<span data-ttu-id="ea900-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ea900-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea900-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea900-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea900-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ea900-139">INPUTS</span></span>

### <span data-ttu-id="ea900-140">Ничего</span><span class="sxs-lookup"><span data-stu-id="ea900-140">None</span></span>

## <span data-ttu-id="ea900-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea900-141">OUTPUTS</span></span>

### <span data-ttu-id="ea900-142">Microsoft. Azure. Management. HDInsight. Models. Cluster</span><span class="sxs-lookup"><span data-stu-id="ea900-142">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="ea900-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="ea900-143">NOTES</span></span>

## <span data-ttu-id="ea900-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea900-144">RELATED LINKS</span></span>

[<span data-ttu-id="ea900-145">Шифрование диска с управляемым ключом пользователя</span><span class="sxs-lookup"><span data-stu-id="ea900-145">Customer-managed key disk encryption</span></span>](https://docs.microsoft.com/en-us/azure/hdinsight/disk-encryption)
