---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/enable-azhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightOperationsManagementSuite.md
ms.openlocfilehash: c7d357df084a3843f8accbd3f54cc8aba9085012
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720839"
---
# <span data-ttu-id="11715-101">Enable-AzHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="11715-101">Enable-AzHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="11715-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="11715-102">SYNOPSIS</span></span>
<span data-ttu-id="11715-103">Включает набор Operations Management Suite (OMS) в кластере HDInsight, и необходимые журналы будут отправлены в рабочую область OMS, указанную во время включения.</span><span class="sxs-lookup"><span data-stu-id="11715-103">Enables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will be sent to the OMS workspace specified during enable.</span></span>

## <span data-ttu-id="11715-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="11715-104">SYNTAX</span></span>

```
Enable-AzHDInsightOperationsManagementSuite [-Name] <String> [-WorkspaceId] <String> [-PrimaryKey] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11715-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11715-105">DESCRIPTION</span></span>
<span data-ttu-id="11715-106">Командлет **Enable-AzHDInsightOperationsManagementSuite** включает набор Operations Management Suite (OMS) в кластере Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="11715-106">The **Enable-AzHDInsightOperationsManagementSuite** cmdlet enables Operations Management Suite (OMS) in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="11715-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="11715-107">EXAMPLES</span></span>

### <span data-ttu-id="11715-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="11715-108">Example 1</span></span>
```
PS C:\> Enable-AzHDInsightOMS -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="11715-109">В кластере HDInsight будет включена поддержка Operations Management Suite (OMS), и необходимые журналы будут отправлены в рабочую область OMS с ИД 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="11715-109">Operations Management Suite (OMS) will be enabled on the HDInsight cluster and relevant logs will be sent to the OMS workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="11715-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="11715-110">Example 2</span></span>
```
PS C:\> Enable-AzHDInsightOMS -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="11715-111">В кластере HDInsight будет включена поддержка Operations Management Suite (OMS), и необходимые журналы будут отправлены в рабочую область OMS с ИД 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="11715-111">Operations Management Suite (OMS) will be enabled on the HDInsight cluster and relevant logs will be sent to the OMS workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="11715-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="11715-112">PARAMETERS</span></span>

### <span data-ttu-id="11715-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11715-113">-DefaultProfile</span></span>
<span data-ttu-id="11715-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="11715-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11715-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="11715-115">-Name</span></span>
<span data-ttu-id="11715-116">Имя кластера, включающее набор Operations Management Suite (OMS).</span><span class="sxs-lookup"><span data-stu-id="11715-116">The name of the cluster to enable Operations Management Suite(OMS).</span></span>

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

### <span data-ttu-id="11715-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="11715-117">-PrimaryKey</span></span>
<span data-ttu-id="11715-118">Первичный ключ рабочей области набора Operations Management Suite (OMS).</span><span class="sxs-lookup"><span data-stu-id="11715-118">The primary key of the Operations Management Suite(OMS) workspace.</span></span>

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

### <span data-ttu-id="11715-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11715-119">-ResourceGroupName</span></span>
<span data-ttu-id="11715-120">Группа ресурсов кластера.</span><span class="sxs-lookup"><span data-stu-id="11715-120">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="11715-121">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="11715-121">-WorkspaceId</span></span>
<span data-ttu-id="11715-122">Идентификатор рабочей области Operations Management Suite (OMS).</span><span class="sxs-lookup"><span data-stu-id="11715-122">The id of the Operations Management Suite(OMS) workspace.</span></span>

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

### <span data-ttu-id="11715-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11715-123">-Confirm</span></span>
<span data-ttu-id="11715-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="11715-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11715-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11715-125">-WhatIf</span></span>
<span data-ttu-id="11715-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="11715-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11715-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="11715-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11715-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11715-128">CommonParameters</span></span>
<span data-ttu-id="11715-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="11715-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11715-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11715-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11715-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="11715-131">INPUTS</span></span>

### <span data-ttu-id="11715-132">System. String</span><span class="sxs-lookup"><span data-stu-id="11715-132">System.String</span></span>

## <span data-ttu-id="11715-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="11715-133">OUTPUTS</span></span>

### <span data-ttu-id="11715-134">Microsoft. Azure. Management. HDInsight. Models. OperationResource</span><span class="sxs-lookup"><span data-stu-id="11715-134">Microsoft.Azure.Management.HDInsight.Models.OperationResource</span></span>

## <span data-ttu-id="11715-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="11715-135">NOTES</span></span>

## <span data-ttu-id="11715-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11715-136">RELATED LINKS</span></span>
