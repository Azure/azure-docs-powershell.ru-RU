---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
ms.openlocfilehash: 1cd466581a89e49280d2a6cacdd74d4d37ac208d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245840"
---
# <span data-ttu-id="d0d36-101">Get-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="d0d36-101">Get-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="d0d36-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d0d36-102">SYNOPSIS</span></span>
<span data-ttu-id="d0d36-103">Возвращает одну или несколько учетных данных.</span><span class="sxs-lookup"><span data-stu-id="d0d36-103">Gets one or more credentials</span></span>

## <span data-ttu-id="d0d36-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d0d36-104">SYNTAX</span></span>

### <span data-ttu-id="d0d36-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d0d36-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0d36-106">Объект</span><span class="sxs-lookup"><span data-stu-id="d0d36-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0d36-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d0d36-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0d36-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0d36-108">DESCRIPTION</span></span>
<span data-ttu-id="d0d36-109">Командлет Get-AzSqlElasticJobCredential получает одну или несколько учетных данных задания.</span><span class="sxs-lookup"><span data-stu-id="d0d36-109">The Get-AzSqlElasticJobCredential cmdlet gets one or more job credentials</span></span>

## <span data-ttu-id="d0d36-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d0d36-110">EXAMPLES</span></span>

### <span data-ttu-id="d0d36-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d0d36-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="d0d36-112">Получение учетных данных задания</span><span class="sxs-lookup"><span data-stu-id="d0d36-112">Gets a job credential</span></span>

## <span data-ttu-id="d0d36-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d0d36-113">PARAMETERS</span></span>

### <span data-ttu-id="d0d36-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="d0d36-114">-AgentName</span></span>
<span data-ttu-id="d0d36-115">Имя агента</span><span class="sxs-lookup"><span data-stu-id="d0d36-115">The agent name</span></span>

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

### <span data-ttu-id="d0d36-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0d36-116">-DefaultProfile</span></span>
<span data-ttu-id="d0d36-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d0d36-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0d36-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d0d36-118">-Name</span></span>
<span data-ttu-id="d0d36-119">Имя учетных данных задания</span><span class="sxs-lookup"><span data-stu-id="d0d36-119">The job credential name</span></span>

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

### <span data-ttu-id="d0d36-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d0d36-120">-ParentObject</span></span>
<span data-ttu-id="d0d36-121">Объект Agent</span><span class="sxs-lookup"><span data-stu-id="d0d36-121">The agent object</span></span>

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

### <span data-ttu-id="d0d36-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d0d36-122">-ParentResourceId</span></span>
<span data-ttu-id="d0d36-123">Идентификатор ресурса агента</span><span class="sxs-lookup"><span data-stu-id="d0d36-123">The agent resource id</span></span>

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

### <span data-ttu-id="d0d36-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0d36-124">-ResourceGroupName</span></span>
<span data-ttu-id="d0d36-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d0d36-125">The resource group name</span></span>

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

### <span data-ttu-id="d0d36-126">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="d0d36-126">-ServerName</span></span>
<span data-ttu-id="d0d36-127">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="d0d36-127">The server name</span></span>

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

### <span data-ttu-id="d0d36-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0d36-128">CommonParameters</span></span>
<span data-ttu-id="d0d36-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d0d36-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0d36-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0d36-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0d36-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d0d36-131">INPUTS</span></span>

### <span data-ttu-id="d0d36-132">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="d0d36-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="d0d36-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0d36-133">OUTPUTS</span></span>

### <span data-ttu-id="d0d36-134">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="d0d36-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="d0d36-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="d0d36-135">NOTES</span></span>

## <span data-ttu-id="d0d36-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d0d36-136">RELATED LINKS</span></span>