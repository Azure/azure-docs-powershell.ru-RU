---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/enable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
ms.openlocfilehash: 7ec91d5ab23322185c2920655410b39e2d1a1dce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214665"
---
# <span data-ttu-id="97770-101">Enable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="97770-101">Enable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="97770-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97770-102">SYNOPSIS</span></span>
<span data-ttu-id="97770-103">Включает мониторинг в кластере HDInsight, а соответствующие журналы отправляются в рабочее пространство мониторинга, заданное во время его работы.</span><span class="sxs-lookup"><span data-stu-id="97770-103">Enables monitoring in a HDInsight cluster and relevant logs will be sent to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="97770-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="97770-104">SYNTAX</span></span>

```
Enable-AzHDInsightMonitoring [-Name] <String> [-WorkspaceId] <String> [-PrimaryKey] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="97770-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="97770-105">DESCRIPTION</span></span>
<span data-ttu-id="97770-106">С **помощью cmdlet Enable-AzHDInsightMonitoring** можно вести мониторинг в кластере Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="97770-106">The **Enable-AzHDInsightMonitoring** cmdlet enables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="97770-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="97770-107">EXAMPLES</span></span>

### <span data-ttu-id="97770-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="97770-108">Example 1</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="97770-109">Мониторинг будет включен на кластере HDInsight, а соответствующие журналы будут отправлены в рабочее пространство мониторинга с id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="97770-109">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="97770-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="97770-110">Example 2</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="97770-111">Мониторинг будет включен в кластере HDInsight, а соответствующие журналы будут отправлены в рабочее пространство мониторинга с id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="97770-111">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="97770-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97770-112">PARAMETERS</span></span>

### <span data-ttu-id="97770-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97770-113">-DefaultProfile</span></span>
<span data-ttu-id="97770-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="97770-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97770-115">-Name</span><span class="sxs-lookup"><span data-stu-id="97770-115">-Name</span></span>
<span data-ttu-id="97770-116">Название кластера для отслеживания.</span><span class="sxs-lookup"><span data-stu-id="97770-116">The name of the cluster to enable monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97770-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="97770-117">-PrimaryKey</span></span>
<span data-ttu-id="97770-118">Первичный ключ рабочей области мониторинга.</span><span class="sxs-lookup"><span data-stu-id="97770-118">The primary key of the monitoring workspace.</span></span>

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

### <span data-ttu-id="97770-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97770-119">-ResourceGroupName</span></span>
<span data-ttu-id="97770-120">Группа ресурсов в кластере.</span><span class="sxs-lookup"><span data-stu-id="97770-120">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="97770-121">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="97770-121">-WorkspaceId</span></span>
<span data-ttu-id="97770-122">Id рабочей области мониторинга.</span><span class="sxs-lookup"><span data-stu-id="97770-122">The id of the monitoring workspace.</span></span>

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

### <span data-ttu-id="97770-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="97770-123">-Confirm</span></span>
<span data-ttu-id="97770-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97770-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97770-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97770-125">-WhatIf</span></span>
<span data-ttu-id="97770-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97770-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97770-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="97770-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97770-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97770-128">CommonParameters</span></span>
<span data-ttu-id="97770-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97770-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97770-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97770-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97770-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="97770-131">INPUTS</span></span>

### <span data-ttu-id="97770-132">System.String</span><span class="sxs-lookup"><span data-stu-id="97770-132">System.String</span></span>

## <span data-ttu-id="97770-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="97770-133">OUTPUTS</span></span>

### <span data-ttu-id="97770-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="97770-134">System.Boolean</span></span>

## <span data-ttu-id="97770-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="97770-135">NOTES</span></span>

## <span data-ttu-id="97770-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="97770-136">RELATED LINKS</span></span>
