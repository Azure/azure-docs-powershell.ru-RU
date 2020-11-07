---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Enable-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Enable-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: fcaa5c1342801c4c0ef00e1a4c48abf4a6b4da41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733118"
---
# <span data-ttu-id="7edae-101">Enable-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="7edae-101">Enable-AzureRmHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="7edae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7edae-102">SYNOPSIS</span></span>
<span data-ttu-id="7edae-103">Включает набор Operations Management Suite (OMS) в кластере HDInsight, и необходимые журналы будут отправлены в рабочую область OMS, указанную во время включения.</span><span class="sxs-lookup"><span data-stu-id="7edae-103">Enables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will be sent to the OMS workspace specified during enable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7edae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7edae-104">SYNTAX</span></span>

```
Enable-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-WorkspaceId] <String>
 [-PrimaryKey] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7edae-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7edae-105">DESCRIPTION</span></span>
<span data-ttu-id="7edae-106">Командлет **Enable-AzureRmHDInsightOperationsManagementSuite** включает набор Operations Management Suite (OMS) в кластере Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="7edae-106">The **Enable-AzureRmHDInsightOperationsManagementSuite** cmdlet enables Operations Management Suite (OMS) in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="7edae-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7edae-107">EXAMPLES</span></span>

### <span data-ttu-id="7edae-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7edae-108">Example 1</span></span>
```
PS C:\> Enable-AzureRmHDInsightOMS -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="7edae-109">В кластере HDInsight будет включена поддержка Operations Management Suite (OMS), и необходимые журналы будут отправлены в рабочую область OMS с ИД 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="7edae-109">Operations Management Suite (OMS) will be enabled on the HDInsight cluster and relevant logs will be sent to the OMS workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="7edae-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7edae-110">Example 2</span></span>
```
PS C:\> Enable-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="7edae-111">В кластере HDInsight будет включена поддержка Operations Management Suite (OMS), и необходимые журналы будут отправлены в рабочую область OMS с ИД 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="7edae-111">Operations Management Suite (OMS) will be enabled on the HDInsight cluster and relevant logs will be sent to the OMS workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="7edae-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7edae-112">PARAMETERS</span></span>

### <span data-ttu-id="7edae-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7edae-113">-Name</span></span>
<span data-ttu-id="7edae-114">Имя кластера, включающее набор Operations Management Suite (OMS).</span><span class="sxs-lookup"><span data-stu-id="7edae-114">The name of the cluster to enable Operations Management Suite(OMS).</span></span>

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

### <span data-ttu-id="7edae-115">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="7edae-115">-PrimaryKey</span></span>
<span data-ttu-id="7edae-116">Первичный ключ рабочей области набора Operations Management Suite (OMS).</span><span class="sxs-lookup"><span data-stu-id="7edae-116">The primary key of the Operations Management Suite(OMS) workspace.</span></span>

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

### <span data-ttu-id="7edae-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7edae-117">-ResourceGroupName</span></span>
<span data-ttu-id="7edae-118">Группа ресурсов кластера.</span><span class="sxs-lookup"><span data-stu-id="7edae-118">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="7edae-119">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="7edae-119">-WorkspaceId</span></span>
<span data-ttu-id="7edae-120">Идентификатор рабочей области Operations Management Suite (OMS).</span><span class="sxs-lookup"><span data-stu-id="7edae-120">The id of the Operations Management Suite(OMS) workspace.</span></span>

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

### <span data-ttu-id="7edae-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7edae-121">-Confirm</span></span>
<span data-ttu-id="7edae-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7edae-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7edae-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7edae-123">-DefaultProfile</span></span>
<span data-ttu-id="7edae-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7edae-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7edae-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7edae-125">-WhatIf</span></span>
<span data-ttu-id="7edae-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7edae-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7edae-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7edae-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7edae-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7edae-128">CommonParameters</span></span>
<span data-ttu-id="7edae-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7edae-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7edae-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7edae-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7edae-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7edae-131">INPUTS</span></span>

### <span data-ttu-id="7edae-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7edae-132">System.String</span></span>

## <span data-ttu-id="7edae-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7edae-133">OUTPUTS</span></span>

### <span data-ttu-id="7edae-134">Microsoft. Azure. Management. HDInsight. Models. OperationResource</span><span class="sxs-lookup"><span data-stu-id="7edae-134">Microsoft.Azure.Management.HDInsight.Models.OperationResource</span></span>

## <span data-ttu-id="7edae-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="7edae-135">NOTES</span></span>

## <span data-ttu-id="7edae-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7edae-136">RELATED LINKS</span></span>

