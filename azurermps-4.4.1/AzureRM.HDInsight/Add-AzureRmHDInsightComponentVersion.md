---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 774848C9-47A1-4C43-B6FA-B3C0C3C76470
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightComponentVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightComponentVersion.md
ms.openlocfilehash: 300244048ae6855c7c621f9950677c985dcb78cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570408"
---
# <span data-ttu-id="81a7c-101">Add-AzureRmHDInsightComponentVersion</span><span class="sxs-lookup"><span data-stu-id="81a7c-101">Add-AzureRmHDInsightComponentVersion</span></span>

## <span data-ttu-id="81a7c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="81a7c-102">SYNOPSIS</span></span>
<span data-ttu-id="81a7c-103">Добавляет версию службы, работающей на кластере, в объект конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="81a7c-103">Adds a version for a service running in a cluster to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81a7c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="81a7c-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightComponentVersion [-Config] <AzureHDInsightConfig> [-ComponentName] <String>
 [-ComponentVersion] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81a7c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="81a7c-105">DESCRIPTION</span></span>
<span data-ttu-id="81a7c-106">Командлет Add-AzureRmHDInsightComponentVersion добавляет версию для службы, работающей на кластере, в объект конфигурации HDInsight Azure, созданный командлетом New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="81a7c-106">The Add-AzureRmHDInsightComponentVersion cmdlet adds a version for a service running in a cluster to the Azure HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="81a7c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="81a7c-107">EXAMPLES</span></span>

### <span data-ttu-id="81a7c-108">--------------------------Пример 1: добавьте версию Spark в объект конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="81a7c-108">--------------------------  Example 1: Add a version for Spark to the cluster configuration object.</span></span>  --------------------------
<span data-ttu-id="81a7c-109">@ {абзац = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="81a7c-109">@{paragraph=PS C:\\\>}</span></span>







```
PS C:\> # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzureStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container001"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-spark-001"
        $clusterCreds = Get-Credential
        $sshClusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        #   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightComponentVersion `
                -ComponentName "Spark" `
                -ComponentVersion "2.0" `
            | New-AzureRmHDInsightCluster `
                -ClusterType Spark `
                -OSType Linux `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer `
                -SshCredential $sshCredentials `
                -Version "3.5"
```

<span data-ttu-id="81a7c-110">Эта команда добавляет версию Spark в кластер HDInsight с именем "от-Spark-001".</span><span class="sxs-lookup"><span data-stu-id="81a7c-110">This command adds the version of Spark to the HDInsight cluster named 'your-spark-001'.</span></span>

## <span data-ttu-id="81a7c-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="81a7c-111">PARAMETERS</span></span>

### <span data-ttu-id="81a7c-112">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="81a7c-112">-ComponentName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81a7c-113">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="81a7c-113">-ComponentVersion</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81a7c-114">-Config</span><span class="sxs-lookup"><span data-stu-id="81a7c-114">-Config</span></span>
```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81a7c-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81a7c-115">-Confirm</span></span>
<span data-ttu-id="81a7c-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="81a7c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81a7c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81a7c-117">-WhatIf</span></span>
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

### <span data-ttu-id="81a7c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81a7c-118">-DefaultProfile</span></span>
<span data-ttu-id="81a7c-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="81a7c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81a7c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81a7c-120">CommonParameters</span></span>
<span data-ttu-id="81a7c-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="81a7c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81a7c-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81a7c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81a7c-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="81a7c-123">INPUTS</span></span>

### <span data-ttu-id="81a7c-124">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="81a7c-124">AzureHDInsightConfig</span></span>
<span data-ttu-id="81a7c-125">Параметр config принимает значение типа "AzureHDInsightConfig" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="81a7c-125">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="81a7c-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="81a7c-126">OUTPUTS</span></span>

### <span data-ttu-id="81a7c-127">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="81a7c-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="81a7c-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="81a7c-128">NOTES</span></span>

## <span data-ttu-id="81a7c-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="81a7c-129">RELATED LINKS</span></span>

