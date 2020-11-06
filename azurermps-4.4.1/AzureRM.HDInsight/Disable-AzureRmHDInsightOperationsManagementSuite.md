---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Disable-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Disable-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: c7a4488c606206c1a5a6043140abfbd125cc6b21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566722"
---
# <span data-ttu-id="4ba0b-101">Disable-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="4ba0b-101">Disable-AzureRmHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="4ba0b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4ba0b-102">SYNOPSIS</span></span>
<span data-ttu-id="4ba0b-103">Отключает набор Operations Management Suite (OMS) в HDInsight кластере, и необходимые журналы перестают передаваться в рабочую область OMS, указанную во время включения.</span><span class="sxs-lookup"><span data-stu-id="4ba0b-103">Disables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will stop flowing to the OMS workspace specified during enable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ba0b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4ba0b-104">SYNTAX</span></span>

```
Disable-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ba0b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ba0b-105">DESCRIPTION</span></span>
<span data-ttu-id="4ba0b-106">Командлет **Disable-AzureRmHDInsightOperationsManagementSuite** отключает набор Operations Management Suite (OMS) в кластере Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4ba0b-106">The **Disable-AzureRmHDInsightOperationsManagementSuite** cmdlet disables Operations Management Suite (OMS) in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="4ba0b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4ba0b-107">EXAMPLES</span></span>

### <span data-ttu-id="4ba0b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4ba0b-108">Example 1</span></span>
```
PS C:\> Disable-AzureRmHDInsightOMS -Name testcluster

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="4ba0b-109">Набор Operations Management Suite (OMS) будет отключен в кластере HDInsight, а связанные журналы будут остановлены в рабочую область OMS.</span><span class="sxs-lookup"><span data-stu-id="4ba0b-109">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

### <span data-ttu-id="4ba0b-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4ba0b-110">Example 2</span></span>
```
PS C:\> Disable-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="4ba0b-111">Набор Operations Management Suite (OMS) будет отключен в кластере HDInsight, а связанные журналы будут остановлены в рабочую область OMS.</span><span class="sxs-lookup"><span data-stu-id="4ba0b-111">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

## <span data-ttu-id="4ba0b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4ba0b-112">PARAMETERS</span></span>

### <span data-ttu-id="4ba0b-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4ba0b-113">-Name</span></span>
<span data-ttu-id="4ba0b-114">Имя кластера, на котором нужно отключить набор Operations Management Suite (OMS).</span><span class="sxs-lookup"><span data-stu-id="4ba0b-114">The name of the cluster to disable Operations Management Suite(OMS).</span></span>

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

### <span data-ttu-id="4ba0b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ba0b-115">-ResourceGroupName</span></span>
<span data-ttu-id="4ba0b-116">Группа ресурсов кластера.</span><span class="sxs-lookup"><span data-stu-id="4ba0b-116">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="4ba0b-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ba0b-117">-Confirm</span></span>
<span data-ttu-id="4ba0b-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4ba0b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ba0b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ba0b-119">-DefaultProfile</span></span>
<span data-ttu-id="4ba0b-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4ba0b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ba0b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ba0b-121">-WhatIf</span></span>
<span data-ttu-id="4ba0b-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4ba0b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ba0b-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4ba0b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ba0b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ba0b-124">CommonParameters</span></span>
<span data-ttu-id="4ba0b-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4ba0b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ba0b-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ba0b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ba0b-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4ba0b-127">INPUTS</span></span>

### <span data-ttu-id="4ba0b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4ba0b-128">System.String</span></span>

## <span data-ttu-id="4ba0b-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ba0b-129">OUTPUTS</span></span>

### <span data-ttu-id="4ba0b-130">Microsoft. Azure. Management. HDInsight. Models. OperationResource</span><span class="sxs-lookup"><span data-stu-id="4ba0b-130">Microsoft.Azure.Management.HDInsight.Models.OperationResource</span></span>

## <span data-ttu-id="4ba0b-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="4ba0b-131">NOTES</span></span>

## <span data-ttu-id="4ba0b-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ba0b-132">RELATED LINKS</span></span>

