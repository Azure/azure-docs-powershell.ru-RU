---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 3F321D94-2B0B-48CA-9778-8090373F7FE0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/grant-azurermhdinsighthttpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightHttpServicesAccess.md
ms.openlocfilehash: 644fd5ff1b038f275288e30d85fbc653b6107b1c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734965"
---
# <span data-ttu-id="5ad73-101">Grant-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="5ad73-101">Grant-AzureRmHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="5ad73-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5ad73-102">SYNOPSIS</span></span>
<span data-ttu-id="5ad73-103">Предоставление доступа к кластеру через HTTP.</span><span class="sxs-lookup"><span data-stu-id="5ad73-103">Grants HTTP access to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ad73-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5ad73-104">SYNTAX</span></span>

```
Grant-AzureRmHDInsightHttpServicesAccess [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ad73-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ad73-105">DESCRIPTION</span></span>
<span data-ttu-id="5ad73-106">Командлет **Grant-AzureRmHDInsightHttpServicesAccess** предоставляет доступ по протоколу HTTP к кластеру HDInsight Azure с помощью ODBC, Ambari, Oozie и веб-служб.</span><span class="sxs-lookup"><span data-stu-id="5ad73-106">The **Grant-AzureRmHDInsightHttpServicesAccess** cmdlet grants HTTP access to an Azure HDInsight cluster using ODBC, Ambari, Oozie and web services.</span></span>

## <span data-ttu-id="5ad73-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5ad73-107">EXAMPLES</span></span>

### <span data-ttu-id="5ad73-108">Пример 1: предоставление доступа HTTP к кластеру HDInsight Azure</span><span class="sxs-lookup"><span data-stu-id="5ad73-108">Example 1: Grant HTTP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzureRmHDInsightHttpServicesAccess `
            -ClusterName $clusterName `
            -HttpCredential $newClusterCreds
```

<span data-ttu-id="5ad73-109">Эта команда предоставляет доступ по протоколу HTTP к кластеру с именем-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="5ad73-109">This command grants HTTP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="5ad73-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5ad73-110">PARAMETERS</span></span>

### <span data-ttu-id="5ad73-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="5ad73-111">-ClusterName</span></span>
<span data-ttu-id="5ad73-112">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="5ad73-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad73-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ad73-113">-DefaultProfile</span></span>
<span data-ttu-id="5ad73-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5ad73-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ad73-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="5ad73-115">-HttpCredential</span></span>
<span data-ttu-id="5ad73-116">Задает учетные данные для входа в кластер (HTTP) для кластера.</span><span class="sxs-lookup"><span data-stu-id="5ad73-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad73-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ad73-117">-ResourceGroupName</span></span>
<span data-ttu-id="5ad73-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5ad73-118">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad73-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ad73-119">CommonParameters</span></span>
<span data-ttu-id="5ad73-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5ad73-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ad73-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ad73-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ad73-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5ad73-122">INPUTS</span></span>

### <span data-ttu-id="5ad73-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="5ad73-123">None</span></span>

## <span data-ttu-id="5ad73-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ad73-124">OUTPUTS</span></span>

### <span data-ttu-id="5ad73-125">Microsoft. Azure. Management. HDInsight. Models. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="5ad73-125">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="5ad73-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="5ad73-126">NOTES</span></span>

## <span data-ttu-id="5ad73-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ad73-127">RELATED LINKS</span></span>

[<span data-ttu-id="5ad73-128">REVOKE-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="5ad73-128">Revoke-AzureRmHDInsightHttpServicesAccess</span></span>](./Revoke-AzureRmHDInsightHttpServicesAccess.md)


