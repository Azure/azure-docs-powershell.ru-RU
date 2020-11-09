---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
ms.openlocfilehash: a553f5e1e6b4929997cbd850ca199e6fd7acef08
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317483"
---
# <span data-ttu-id="bbe9b-101">Get-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="bbe9b-101">Get-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="bbe9b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bbe9b-102">SYNOPSIS</span></span>
<span data-ttu-id="bbe9b-103">Возвращает Synapseную инструкцию аналитики Spark.</span><span class="sxs-lookup"><span data-stu-id="bbe9b-103">Gets a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="bbe9b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bbe9b-104">SYNTAX</span></span>

### <span data-ttu-id="bbe9b-105">GetSparkStatementsByIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bbe9b-105">GetSparkStatementsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>]
 -SessionId <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bbe9b-106">GetSparkStatementsByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbe9b-106">GetSparkStatementsByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> [-LivyId <Int32>] [-SessionId <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbe9b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbe9b-107">DESCRIPTION</span></span>
<span data-ttu-id="bbe9b-108">Командлет **Get-AzSynapseSparkStatement** получает сведения о инструкции Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="bbe9b-108">The **Get-AzSynapseSparkStatement** cmdlet gets information about an Azure Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="bbe9b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bbe9b-109">EXAMPLES</span></span>

### <span data-ttu-id="bbe9b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bbe9b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120
```

<span data-ttu-id="bbe9b-111">Эта команда получает все инструкции Spark из сеанса Spark.</span><span class="sxs-lookup"><span data-stu-id="bbe9b-111">This command gets all the Spark statements under a Spark session.</span></span>

### <span data-ttu-id="bbe9b-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="bbe9b-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120 -LivyId 0
```

<span data-ttu-id="bbe9b-113">Эта команда получает инструкцию Spark с указанным ИДЕНТИФИКАТОРом Livy.</span><span class="sxs-lookup"><span data-stu-id="bbe9b-113">This command gets the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="bbe9b-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="bbe9b-114">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 107
PS C:\> $session | Get-AzSynapseSparkStatement
```

<span data-ttu-id="bbe9b-115">Эта команда получает все инструкции Spark в сеансе Spark по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="bbe9b-115">This command gets all the Spark statements under a Spark session through pipeline.</span></span>

## <span data-ttu-id="bbe9b-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bbe9b-116">PARAMETERS</span></span>

### <span data-ttu-id="bbe9b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbe9b-117">-DefaultProfile</span></span>
<span data-ttu-id="bbe9b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bbe9b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbe9b-119">-LivyId</span><span class="sxs-lookup"><span data-stu-id="bbe9b-119">-LivyId</span></span>
<span data-ttu-id="bbe9b-120">Идентификатор инструкции Spark.</span><span class="sxs-lookup"><span data-stu-id="bbe9b-120">Identifier of Spark statement.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbe9b-121">-SessionId</span><span class="sxs-lookup"><span data-stu-id="bbe9b-121">-SessionId</span></span>
<span data-ttu-id="bbe9b-122">Идентификатор сеанса Spark.</span><span class="sxs-lookup"><span data-stu-id="bbe9b-122">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: GetSparkStatementsByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbe9b-123">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="bbe9b-123">-SessionObject</span></span>
<span data-ttu-id="bbe9b-124">Входной объект пула Spark, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="bbe9b-124">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: GetSparkStatementsByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbe9b-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="bbe9b-125">-SparkPoolName</span></span>
<span data-ttu-id="bbe9b-126">Название пула Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="bbe9b-126">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbe9b-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bbe9b-127">-WorkspaceName</span></span>
<span data-ttu-id="bbe9b-128">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="bbe9b-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbe9b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbe9b-129">CommonParameters</span></span>
<span data-ttu-id="bbe9b-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bbe9b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbe9b-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bbe9b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbe9b-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bbe9b-132">INPUTS</span></span>

### <span data-ttu-id="bbe9b-133">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="bbe9b-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="bbe9b-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbe9b-134">OUTPUTS</span></span>

### <span data-ttu-id="bbe9b-135">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="bbe9b-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkStatement</span></span>

## <span data-ttu-id="bbe9b-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="bbe9b-136">NOTES</span></span>

## <span data-ttu-id="bbe9b-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bbe9b-137">RELATED LINKS</span></span>
