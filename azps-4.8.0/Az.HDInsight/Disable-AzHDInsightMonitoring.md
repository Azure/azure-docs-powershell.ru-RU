---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/disable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
ms.openlocfilehash: 9a65a82808c78fe878ba4a61f8be01f37fc11771
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242760"
---
# <span data-ttu-id="1747f-101">Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="1747f-101">Disable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="1747f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1747f-102">SYNOPSIS</span></span>
<span data-ttu-id="1747f-103">Отключение мониторинга в кластере HDInsight и необходимые журналы будут прекращаться в рабочую область мониторинга, указанную во время включения.</span><span class="sxs-lookup"><span data-stu-id="1747f-103">Disables monitoring in a HDInsight cluster and relevant logs will stop flowing to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="1747f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1747f-104">SYNTAX</span></span>

```
Disable-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1747f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1747f-105">DESCRIPTION</span></span>
<span data-ttu-id="1747f-106">Командлет **Disable-AzHDInsightMonitoring** отключает мониторинг в кластере Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1747f-106">The **Disable-AzHDInsightMonitoring** cmdlet disables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="1747f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1747f-107">EXAMPLES</span></span>

### <span data-ttu-id="1747f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1747f-108">Example 1</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster

True
```

<span data-ttu-id="1747f-109">Наблюдение будет отключено в кластере HDInsight, и связанные журналы будут прекращаться в рабочую область Monitoring.</span><span class="sxs-lookup"><span data-stu-id="1747f-109">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

### <span data-ttu-id="1747f-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1747f-110">Example 2</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

True
```

<span data-ttu-id="1747f-111">Наблюдение будет отключено в кластере HDInsight, и связанные журналы будут прекращаться в рабочую область Monitoring.</span><span class="sxs-lookup"><span data-stu-id="1747f-111">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

## <span data-ttu-id="1747f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1747f-112">PARAMETERS</span></span>

### <span data-ttu-id="1747f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1747f-113">-DefaultProfile</span></span>
<span data-ttu-id="1747f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1747f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1747f-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1747f-115">-Name</span></span>
<span data-ttu-id="1747f-116">Имя кластера для отключения наблюдения.</span><span class="sxs-lookup"><span data-stu-id="1747f-116">The name of the cluster to disable Monitoring.</span></span>

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

### <span data-ttu-id="1747f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1747f-117">-ResourceGroupName</span></span>
<span data-ttu-id="1747f-118">Группа ресурсов кластера.</span><span class="sxs-lookup"><span data-stu-id="1747f-118">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="1747f-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1747f-119">-Confirm</span></span>
<span data-ttu-id="1747f-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1747f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1747f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1747f-121">-WhatIf</span></span>
<span data-ttu-id="1747f-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1747f-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1747f-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1747f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1747f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1747f-124">CommonParameters</span></span>
<span data-ttu-id="1747f-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1747f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1747f-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1747f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1747f-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1747f-127">INPUTS</span></span>

### <span data-ttu-id="1747f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1747f-128">System.String</span></span>

## <span data-ttu-id="1747f-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1747f-129">OUTPUTS</span></span>

### <span data-ttu-id="1747f-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1747f-130">System.Boolean</span></span>

## <span data-ttu-id="1747f-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="1747f-131">NOTES</span></span>

## <span data-ttu-id="1747f-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1747f-132">RELATED LINKS</span></span>
