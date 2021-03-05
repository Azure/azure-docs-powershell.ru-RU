---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/disable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
ms.openlocfilehash: 04e4a2e45f799367060c76e30807f75eaedb0465
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968995"
---
# <span data-ttu-id="98cb8-101">Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="98cb8-101">Disable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="98cb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98cb8-102">SYNOPSIS</span></span>
<span data-ttu-id="98cb8-103">Отключение мониторинга в кластере HDInsight, и соответствующие журналы перестанут поступать в рабочее пространство мониторинга, указанное во время его включения.</span><span class="sxs-lookup"><span data-stu-id="98cb8-103">Disables monitoring in a HDInsight cluster and relevant logs will stop flowing to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="98cb8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="98cb8-104">SYNTAX</span></span>

```
Disable-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98cb8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98cb8-105">DESCRIPTION</span></span>
<span data-ttu-id="98cb8-106">Для кластера Azure HDInsight отключается мониторинг с использованием **cmdlet Disable-AzHDInsightMonitoring.**</span><span class="sxs-lookup"><span data-stu-id="98cb8-106">The **Disable-AzHDInsightMonitoring** cmdlet disables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="98cb8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="98cb8-107">EXAMPLES</span></span>

### <span data-ttu-id="98cb8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="98cb8-108">Example 1</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster

True
```

<span data-ttu-id="98cb8-109">Мониторинг будет отключен на кластере HDInsight, и соответствующие журналы перестанут поступать в рабочее пространство мониторинга.</span><span class="sxs-lookup"><span data-stu-id="98cb8-109">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

### <span data-ttu-id="98cb8-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="98cb8-110">Example 2</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

True
```

<span data-ttu-id="98cb8-111">Мониторинг будет отключен на кластере HDInsight, и соответствующие журналы перестанут поступать в рабочее пространство мониторинга.</span><span class="sxs-lookup"><span data-stu-id="98cb8-111">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

## <span data-ttu-id="98cb8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98cb8-112">PARAMETERS</span></span>

### <span data-ttu-id="98cb8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98cb8-113">-DefaultProfile</span></span>
<span data-ttu-id="98cb8-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="98cb8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98cb8-115">-Name</span><span class="sxs-lookup"><span data-stu-id="98cb8-115">-Name</span></span>
<span data-ttu-id="98cb8-116">Название кластера для отключения мониторинга.</span><span class="sxs-lookup"><span data-stu-id="98cb8-116">The name of the cluster to disable Monitoring.</span></span>

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

### <span data-ttu-id="98cb8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98cb8-117">-ResourceGroupName</span></span>
<span data-ttu-id="98cb8-118">Группа ресурсов в кластере.</span><span class="sxs-lookup"><span data-stu-id="98cb8-118">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="98cb8-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98cb8-119">-Confirm</span></span>
<span data-ttu-id="98cb8-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="98cb8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98cb8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98cb8-121">-WhatIf</span></span>
<span data-ttu-id="98cb8-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98cb8-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98cb8-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="98cb8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98cb8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98cb8-124">CommonParameters</span></span>
<span data-ttu-id="98cb8-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98cb8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98cb8-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98cb8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98cb8-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="98cb8-127">INPUTS</span></span>

### <span data-ttu-id="98cb8-128">System.String</span><span class="sxs-lookup"><span data-stu-id="98cb8-128">System.String</span></span>

## <span data-ttu-id="98cb8-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="98cb8-129">OUTPUTS</span></span>

### <span data-ttu-id="98cb8-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="98cb8-130">System.Boolean</span></span>

## <span data-ttu-id="98cb8-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="98cb8-131">NOTES</span></span>

## <span data-ttu-id="98cb8-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98cb8-132">RELATED LINKS</span></span>
