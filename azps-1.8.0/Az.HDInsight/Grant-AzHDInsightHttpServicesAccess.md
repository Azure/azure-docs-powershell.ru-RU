---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 3F321D94-2B0B-48CA-9778-8090373F7FE0
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/grant-azhdinsighthttpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightHttpServicesAccess.md
ms.openlocfilehash: c531135af3d118a9987a3c328eb4c06847e75fe6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900490"
---
# <span data-ttu-id="816f4-101">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="816f4-101">Grant-AzHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="816f4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="816f4-102">SYNOPSIS</span></span>
<span data-ttu-id="816f4-103">Предоставление доступа к кластеру через HTTP.</span><span class="sxs-lookup"><span data-stu-id="816f4-103">Grants HTTP access to the cluster.</span></span>

## <span data-ttu-id="816f4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="816f4-104">SYNTAX</span></span>

```
Grant-AzHDInsightHttpServicesAccess [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="816f4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="816f4-105">DESCRIPTION</span></span>
<span data-ttu-id="816f4-106">Командлет **Grant-AzHDInsightHttpServicesAccess** предоставляет доступ по протоколу HTTP к кластеру HDInsight Azure с помощью ODBC, Ambari, Oozie и веб-служб.</span><span class="sxs-lookup"><span data-stu-id="816f4-106">The **Grant-AzHDInsightHttpServicesAccess** cmdlet grants HTTP access to an Azure HDInsight cluster using ODBC, Ambari, Oozie and web services.</span></span>

## <span data-ttu-id="816f4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="816f4-107">EXAMPLES</span></span>

### <span data-ttu-id="816f4-108">Пример 1: предоставление доступа HTTP к кластеру HDInsight Azure</span><span class="sxs-lookup"><span data-stu-id="816f4-108">Example 1: Grant HTTP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzHDInsightHttpServicesAccess `
            -ClusterName $clusterName `
            -HttpCredential $newClusterCreds
```

<span data-ttu-id="816f4-109">Эта команда предоставляет доступ по протоколу HTTP к кластеру с именем-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="816f4-109">This command grants HTTP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="816f4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="816f4-110">PARAMETERS</span></span>

### <span data-ttu-id="816f4-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="816f4-111">-ClusterName</span></span>
<span data-ttu-id="816f4-112">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="816f4-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="816f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="816f4-113">-DefaultProfile</span></span>
<span data-ttu-id="816f4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="816f4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="816f4-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="816f4-115">-HttpCredential</span></span>
<span data-ttu-id="816f4-116">Задает учетные данные для входа в кластер (HTTP) для кластера.</span><span class="sxs-lookup"><span data-stu-id="816f4-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="816f4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="816f4-117">-ResourceGroupName</span></span>
<span data-ttu-id="816f4-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="816f4-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="816f4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="816f4-119">CommonParameters</span></span>
<span data-ttu-id="816f4-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="816f4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="816f4-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="816f4-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="816f4-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="816f4-122">INPUTS</span></span>

### <span data-ttu-id="816f4-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="816f4-123">None</span></span>

## <span data-ttu-id="816f4-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="816f4-124">OUTPUTS</span></span>

### <span data-ttu-id="816f4-125">Microsoft. Azure. Management. HDInsight. Models. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="816f4-125">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="816f4-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="816f4-126">NOTES</span></span>

## <span data-ttu-id="816f4-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="816f4-127">RELATED LINKS</span></span>

[<span data-ttu-id="816f4-128">REVOKE-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="816f4-128">Revoke-AzHDInsightHttpServicesAccess</span></span>](./Revoke-AzHDInsightHttpServicesAccess.md)


