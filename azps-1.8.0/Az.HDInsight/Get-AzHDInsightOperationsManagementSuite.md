---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightOperationsManagementSuite.md
ms.openlocfilehash: fa19e7817d9d9be5e0c941db6d814500bad33509
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900517"
---
# <span data-ttu-id="62023-101">Get-AzHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="62023-101">Get-AzHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="62023-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="62023-102">SYNOPSIS</span></span>
<span data-ttu-id="62023-103">Получает состояние установки Operations Management Suite (OMS) в кластере.</span><span class="sxs-lookup"><span data-stu-id="62023-103">Gets the status of Operations Management Suite (OMS) installation on the cluster.</span></span>

## <span data-ttu-id="62023-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="62023-104">SYNTAX</span></span>

```
Get-AzHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62023-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62023-105">DESCRIPTION</span></span>
<span data-ttu-id="62023-106">Командлет **Get-AzHDInsightOperationsManagementSuite** получает состояние установки OMS в кластере HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="62023-106">The **Get-AzHDInsightOperationsManagementSuite** cmdlet gets the status of OMS installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="62023-107">Если включена поддержка OMS, она также будет возвращать идентификатор рабочей области OMS.</span><span class="sxs-lookup"><span data-stu-id="62023-107">If OMS is enabled then it will also return the OMS workspace id.</span></span>

## <span data-ttu-id="62023-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="62023-108">EXAMPLES</span></span>

### <span data-ttu-id="62023-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="62023-109">Example 1</span></span>
```
PS C:\> Get-AzHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="62023-110">В кластере включена поддержка Operations Management Suite (OMS), так как свойство ClusterMonitoringEnabled имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="62023-110">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="62023-111">Идентификатор рабочей области OMS, в которой находятся журналы, 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="62023-111">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="62023-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="62023-112">Example 2</span></span>
```
PS C:\> Get-AzHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="62023-113">В кластере включена поддержка Operations Management Suite (OMS), так как свойство ClusterMonitoringEnabled имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="62023-113">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="62023-114">Идентификатор рабочей области OMS, в которой находятся журналы, 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="62023-114">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="62023-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="62023-115">Example 3</span></span>
```
PS C:\> Get-AzHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="62023-116">Набор Operations Management Suite (OMS) в кластере отключен, так как свойство ClusterMonitoringEnabled имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="62023-116">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="62023-117">Пример 4</span><span class="sxs-lookup"><span data-stu-id="62023-117">Example 4</span></span>
```
PS C:\> Get-AzHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="62023-118">Набор Operations Management Suite (OMS) в кластере отключен, так как свойство ClusterMonitoringEnabled имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="62023-118">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="62023-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="62023-119">PARAMETERS</span></span>

### <span data-ttu-id="62023-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62023-120">-DefaultProfile</span></span>
<span data-ttu-id="62023-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="62023-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62023-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="62023-122">-Name</span></span>
<span data-ttu-id="62023-123">Имя кластера, которое получает состояние набора Operations Management Suite (OMS).</span><span class="sxs-lookup"><span data-stu-id="62023-123">The name of the cluster to get the status of Operations Management Suite(OMS).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62023-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62023-124">-ResourceGroupName</span></span>
<span data-ttu-id="62023-125">Группа ресурсов кластера.</span><span class="sxs-lookup"><span data-stu-id="62023-125">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="62023-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62023-126">CommonParameters</span></span>
<span data-ttu-id="62023-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="62023-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62023-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62023-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62023-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="62023-129">INPUTS</span></span>

### <span data-ttu-id="62023-130">System. String</span><span class="sxs-lookup"><span data-stu-id="62023-130">System.String</span></span>

## <span data-ttu-id="62023-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="62023-131">OUTPUTS</span></span>

### <span data-ttu-id="62023-132">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="62023-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightOMS</span></span>

## <span data-ttu-id="62023-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="62023-133">NOTES</span></span>

## <span data-ttu-id="62023-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62023-134">RELATED LINKS</span></span>
