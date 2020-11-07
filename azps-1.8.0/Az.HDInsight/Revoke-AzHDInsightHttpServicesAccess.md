---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 670EAFC0-3F8D-4F3D-8B62-448F04378F8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/revoke-azhdinsighthttpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightHttpServicesAccess.md
ms.openlocfilehash: ddc269d342a6119187ec578e236a30c928d9ea3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900445"
---
# <span data-ttu-id="bda26-101">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="bda26-101">Revoke-AzHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="bda26-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bda26-102">SYNOPSIS</span></span>
<span data-ttu-id="bda26-103">Отключает доступ к кластеру через HTTP.</span><span class="sxs-lookup"><span data-stu-id="bda26-103">Disables HTTP access to the cluster.</span></span>

## <span data-ttu-id="bda26-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bda26-104">SYNTAX</span></span>

```
Revoke-AzHDInsightHttpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bda26-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bda26-105">DESCRIPTION</span></span>
<span data-ttu-id="bda26-106">Командлет **REVOKE-AzHDInsightHttpServicesAccess** отключает доступ HTTP к кластеру HDInsight Azure для ODBC, Ambari, Oozie и webHCatalog веб-службам.</span><span class="sxs-lookup"><span data-stu-id="bda26-106">The **Revoke-AzHDInsightHttpServicesAccess** cmdlet disables HTTP access to an Azure HDInsight cluster for ODBC, Ambari, Oozie and webHCatalog web services.</span></span>

## <span data-ttu-id="bda26-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bda26-107">EXAMPLES</span></span>

### <span data-ttu-id="bda26-108">Пример 1: отключение доступа HTTP к кластеру</span><span class="sxs-lookup"><span data-stu-id="bda26-108">Example 1: Disable HTTP access to a cluster</span></span>
```
PS C:\>Revoke-AzHDInsightHttpServicesAccess `
       -ClusterName "your-hadoop_001"
```

<span data-ttu-id="bda26-109">Эта команда отменяет доступ по протоколу HTTP к кластеру с именем hadoop_001.</span><span class="sxs-lookup"><span data-stu-id="bda26-109">This command revokes HTTP access to the cluster named your-hadoop_001.</span></span>

## <span data-ttu-id="bda26-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bda26-110">PARAMETERS</span></span>

### <span data-ttu-id="bda26-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="bda26-111">-ClusterName</span></span>
<span data-ttu-id="bda26-112">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="bda26-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="bda26-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bda26-113">-DefaultProfile</span></span>
<span data-ttu-id="bda26-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bda26-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bda26-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bda26-115">-ResourceGroupName</span></span>
<span data-ttu-id="bda26-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bda26-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="bda26-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bda26-117">CommonParameters</span></span>
<span data-ttu-id="bda26-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bda26-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bda26-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bda26-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bda26-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bda26-120">INPUTS</span></span>

### <span data-ttu-id="bda26-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="bda26-121">None</span></span>

## <span data-ttu-id="bda26-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bda26-122">OUTPUTS</span></span>

### <span data-ttu-id="bda26-123">Microsoft. Azure. Management. HDInsight. Models. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="bda26-123">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="bda26-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="bda26-124">NOTES</span></span>

## <span data-ttu-id="bda26-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bda26-125">RELATED LINKS</span></span>

[<span data-ttu-id="bda26-126">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="bda26-126">Grant-AzHDInsightHttpServicesAccess</span></span>](./Grant-AzHDInsightHttpServicesAccess.md)


