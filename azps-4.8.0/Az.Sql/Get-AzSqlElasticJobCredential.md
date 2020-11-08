---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
ms.openlocfilehash: 1cd466581a89e49280d2a6cacdd74d4d37ac208d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236603"
---
# <span data-ttu-id="840aa-101">Get-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="840aa-101">Get-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="840aa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="840aa-102">SYNOPSIS</span></span>
<span data-ttu-id="840aa-103">Возвращает одну или несколько учетных данных.</span><span class="sxs-lookup"><span data-stu-id="840aa-103">Gets one or more credentials</span></span>

## <span data-ttu-id="840aa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="840aa-104">SYNTAX</span></span>

### <span data-ttu-id="840aa-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="840aa-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="840aa-106">Объект</span><span class="sxs-lookup"><span data-stu-id="840aa-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="840aa-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="840aa-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="840aa-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="840aa-108">DESCRIPTION</span></span>
<span data-ttu-id="840aa-109">Командлет Get-AzSqlElasticJobCredential получает одну или несколько учетных данных задания.</span><span class="sxs-lookup"><span data-stu-id="840aa-109">The Get-AzSqlElasticJobCredential cmdlet gets one or more job credentials</span></span>

## <span data-ttu-id="840aa-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="840aa-110">EXAMPLES</span></span>

### <span data-ttu-id="840aa-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="840aa-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="840aa-112">Получение учетных данных задания</span><span class="sxs-lookup"><span data-stu-id="840aa-112">Gets a job credential</span></span>

## <span data-ttu-id="840aa-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="840aa-113">PARAMETERS</span></span>

### <span data-ttu-id="840aa-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="840aa-114">-AgentName</span></span>
<span data-ttu-id="840aa-115">Имя агента</span><span class="sxs-lookup"><span data-stu-id="840aa-115">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="840aa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="840aa-116">-DefaultProfile</span></span>
<span data-ttu-id="840aa-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="840aa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="840aa-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="840aa-118">-Name</span></span>
<span data-ttu-id="840aa-119">Имя учетных данных задания</span><span class="sxs-lookup"><span data-stu-id="840aa-119">The job credential name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CredentialName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="840aa-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="840aa-120">-ParentObject</span></span>
<span data-ttu-id="840aa-121">Объект Agent</span><span class="sxs-lookup"><span data-stu-id="840aa-121">The agent object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="840aa-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="840aa-122">-ParentResourceId</span></span>
<span data-ttu-id="840aa-123">Идентификатор ресурса агента</span><span class="sxs-lookup"><span data-stu-id="840aa-123">The agent resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="840aa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="840aa-124">-ResourceGroupName</span></span>
<span data-ttu-id="840aa-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="840aa-125">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="840aa-126">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="840aa-126">-ServerName</span></span>
<span data-ttu-id="840aa-127">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="840aa-127">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="840aa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="840aa-128">CommonParameters</span></span>
<span data-ttu-id="840aa-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="840aa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="840aa-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="840aa-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="840aa-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="840aa-131">INPUTS</span></span>

### <span data-ttu-id="840aa-132">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="840aa-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="840aa-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="840aa-133">OUTPUTS</span></span>

### <span data-ttu-id="840aa-134">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="840aa-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="840aa-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="840aa-135">NOTES</span></span>

## <span data-ttu-id="840aa-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="840aa-136">RELATED LINKS</span></span>
