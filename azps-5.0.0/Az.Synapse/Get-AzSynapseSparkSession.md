---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
ms.openlocfilehash: 587183d72c6fdeec965f1ec1aa6aa88f5d6f36f9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317486"
---
# <span data-ttu-id="71d02-101">Get-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="71d02-101">Get-AzSynapseSparkSession</span></span>

## <span data-ttu-id="71d02-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="71d02-102">SYNOPSIS</span></span>
<span data-ttu-id="71d02-103">Получение сеанса Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="71d02-103">Gets a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="71d02-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="71d02-104">SYNTAX</span></span>

### <span data-ttu-id="71d02-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="71d02-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71d02-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="71d02-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71d02-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71d02-107">DESCRIPTION</span></span>
<span data-ttu-id="71d02-108">Командлет **Get-AzSynapseSparkSession** получает сведения о сеансе Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="71d02-108">The **Get-AzSynapseSparkSession** cmdlet gets information about an Azure Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="71d02-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="71d02-109">EXAMPLES</span></span>

### <span data-ttu-id="71d02-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="71d02-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="71d02-111">Эта команда получает все сеансы Spark из указанного пула Spark.</span><span class="sxs-lookup"><span data-stu-id="71d02-111">This command gets all the Spark sessions under the specified Spark pool.</span></span>

### <span data-ttu-id="71d02-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="71d02-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 1
```

<span data-ttu-id="71d02-113">Эта команда получает сеанс Spark с указанным ИДЕНТИФИКАТОРом Livy.</span><span class="sxs-lookup"><span data-stu-id="71d02-113">This command gets the Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="71d02-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="71d02-114">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkSession
```

<span data-ttu-id="71d02-115">Эта команда получает все сеансы Spark из указанного пула Spark с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="71d02-115">This command gets all the Spark sessions under the specified Spark pool through pipeline.</span></span>

## <span data-ttu-id="71d02-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="71d02-116">PARAMETERS</span></span>

### <span data-ttu-id="71d02-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="71d02-117">-ApplicationId</span></span>
<span data-ttu-id="71d02-118">Идентификатор приложения сеанса.</span><span class="sxs-lookup"><span data-stu-id="71d02-118">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="71d02-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71d02-119">-DefaultProfile</span></span>
<span data-ttu-id="71d02-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="71d02-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71d02-121">-LivyId</span><span class="sxs-lookup"><span data-stu-id="71d02-121">-LivyId</span></span>
<span data-ttu-id="71d02-122">Идентификатор сеанса Spark.</span><span class="sxs-lookup"><span data-stu-id="71d02-122">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="71d02-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="71d02-123">-Name</span></span>
<span data-ttu-id="71d02-124">Название пула Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="71d02-124">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="71d02-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="71d02-125">-SparkPoolName</span></span>
<span data-ttu-id="71d02-126">Название пула Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="71d02-126">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71d02-127">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="71d02-127">-SparkPoolObject</span></span>
<span data-ttu-id="71d02-128">Входной объект пула Spark, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="71d02-128">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71d02-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="71d02-129">-WorkspaceName</span></span>
<span data-ttu-id="71d02-130">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="71d02-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71d02-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71d02-131">CommonParameters</span></span>
<span data-ttu-id="71d02-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="71d02-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71d02-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71d02-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71d02-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="71d02-134">INPUTS</span></span>

### <span data-ttu-id="71d02-135">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="71d02-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="71d02-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="71d02-136">OUTPUTS</span></span>

### <span data-ttu-id="71d02-137">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="71d02-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="71d02-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="71d02-138">NOTES</span></span>

## <span data-ttu-id="71d02-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71d02-139">RELATED LINKS</span></span>
