---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/enable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
ms.openlocfilehash: 7ec91d5ab23322185c2920655410b39e2d1a1dce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242761"
---
# <span data-ttu-id="fbdd6-101">Enable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="fbdd6-101">Enable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="fbdd6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fbdd6-102">SYNOPSIS</span></span>
<span data-ttu-id="fbdd6-103">Включает мониторинг в кластере HDInsight, и необходимые журналы будут отправлены в рабочую область мониторинга, указанную во время включения.</span><span class="sxs-lookup"><span data-stu-id="fbdd6-103">Enables monitoring in a HDInsight cluster and relevant logs will be sent to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="fbdd6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fbdd6-104">SYNTAX</span></span>

```
Enable-AzHDInsightMonitoring [-Name] <String> [-WorkspaceId] <String> [-PrimaryKey] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fbdd6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbdd6-105">DESCRIPTION</span></span>
<span data-ttu-id="fbdd6-106">Командлет **Enable-AzHDInsightMonitoring** включает мониторинг в кластере Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="fbdd6-106">The **Enable-AzHDInsightMonitoring** cmdlet enables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="fbdd6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fbdd6-107">EXAMPLES</span></span>

### <span data-ttu-id="fbdd6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fbdd6-108">Example 1</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="fbdd6-109">В кластере HDInsight будут включены контрольные записи, и необходимые журналы будут отправлены в рабочую область мониторинга с ИД 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="fbdd6-109">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="fbdd6-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fbdd6-110">Example 2</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="fbdd6-111">В кластере HDInsight будут включены контрольные записи, и необходимые журналы будут отправлены в рабочую область мониторинга с ИД 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="fbdd6-111">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="fbdd6-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fbdd6-112">PARAMETERS</span></span>

### <span data-ttu-id="fbdd6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbdd6-113">-DefaultProfile</span></span>
<span data-ttu-id="fbdd6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="fbdd6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbdd6-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fbdd6-115">-Name</span></span>
<span data-ttu-id="fbdd6-116">Имя кластера для включения мониторинга.</span><span class="sxs-lookup"><span data-stu-id="fbdd6-116">The name of the cluster to enable monitoring.</span></span>

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

### <span data-ttu-id="fbdd6-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="fbdd6-117">-PrimaryKey</span></span>
<span data-ttu-id="fbdd6-118">Первичный ключ рабочей области "Мониторинг".</span><span class="sxs-lookup"><span data-stu-id="fbdd6-118">The primary key of the monitoring workspace.</span></span>

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

### <span data-ttu-id="fbdd6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbdd6-119">-ResourceGroupName</span></span>
<span data-ttu-id="fbdd6-120">Группа ресурсов кластера.</span><span class="sxs-lookup"><span data-stu-id="fbdd6-120">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="fbdd6-121">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="fbdd6-121">-WorkspaceId</span></span>
<span data-ttu-id="fbdd6-122">Идентификатор рабочей области мониторинга.</span><span class="sxs-lookup"><span data-stu-id="fbdd6-122">The id of the monitoring workspace.</span></span>

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

### <span data-ttu-id="fbdd6-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fbdd6-123">-Confirm</span></span>
<span data-ttu-id="fbdd6-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fbdd6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbdd6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbdd6-125">-WhatIf</span></span>
<span data-ttu-id="fbdd6-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fbdd6-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fbdd6-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fbdd6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbdd6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbdd6-128">CommonParameters</span></span>
<span data-ttu-id="fbdd6-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fbdd6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbdd6-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbdd6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbdd6-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fbdd6-131">INPUTS</span></span>

### <span data-ttu-id="fbdd6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fbdd6-132">System.String</span></span>

## <span data-ttu-id="fbdd6-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbdd6-133">OUTPUTS</span></span>

### <span data-ttu-id="fbdd6-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fbdd6-134">System.Boolean</span></span>

## <span data-ttu-id="fbdd6-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="fbdd6-135">NOTES</span></span>

## <span data-ttu-id="fbdd6-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fbdd6-136">RELATED LINKS</span></span>
