---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
ms.openlocfilehash: 404b34c7e0d169e1d123a5c1ded8e6b5bef2fe2e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246675"
---
# <span data-ttu-id="dd14c-101">New-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="dd14c-101">New-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="dd14c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dd14c-102">SYNOPSIS</span></span>
<span data-ttu-id="dd14c-103">Создание новых учетных данных задания</span><span class="sxs-lookup"><span data-stu-id="dd14c-103">Creates a new job credential</span></span>

## <span data-ttu-id="dd14c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dd14c-104">SYNTAX</span></span>

### <span data-ttu-id="dd14c-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dd14c-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd14c-106">Объект</span><span class="sxs-lookup"><span data-stu-id="dd14c-106">ObjectSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd14c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="dd14c-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd14c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd14c-108">DESCRIPTION</span></span>
<span data-ttu-id="dd14c-109">Командлет New-AzSqlElasticJobCredential создает новые учетные данные задания</span><span class="sxs-lookup"><span data-stu-id="dd14c-109">The New-AzSqlElasticJobCredential cmdlet creates a new job credential</span></span>

## <span data-ttu-id="dd14c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dd14c-110">EXAMPLES</span></span>

### <span data-ttu-id="dd14c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dd14c-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="dd14c-112">Создание новых учетных данных задания</span><span class="sxs-lookup"><span data-stu-id="dd14c-112">Creates a new job credential</span></span>

## <span data-ttu-id="dd14c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dd14c-113">PARAMETERS</span></span>

### <span data-ttu-id="dd14c-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="dd14c-114">-AgentName</span></span>
<span data-ttu-id="dd14c-115">Имя агента</span><span class="sxs-lookup"><span data-stu-id="dd14c-115">The agent name</span></span>

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

### <span data-ttu-id="dd14c-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="dd14c-116">-Credential</span></span>
<span data-ttu-id="dd14c-117">Учетные данные</span><span class="sxs-lookup"><span data-stu-id="dd14c-117">The credential</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd14c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd14c-118">-DefaultProfile</span></span>
<span data-ttu-id="dd14c-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dd14c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd14c-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dd14c-120">-Name</span></span>
<span data-ttu-id="dd14c-121">Имя учетных данных задания</span><span class="sxs-lookup"><span data-stu-id="dd14c-121">The job credential name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CredentialName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd14c-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="dd14c-122">-ParentObject</span></span>
<span data-ttu-id="dd14c-123">Объект Agent</span><span class="sxs-lookup"><span data-stu-id="dd14c-123">The agent object</span></span>

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

### <span data-ttu-id="dd14c-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="dd14c-124">-ParentResourceId</span></span>
<span data-ttu-id="dd14c-125">Идентификатор ресурса агента</span><span class="sxs-lookup"><span data-stu-id="dd14c-125">The agent resource id</span></span>

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

### <span data-ttu-id="dd14c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd14c-126">-ResourceGroupName</span></span>
<span data-ttu-id="dd14c-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="dd14c-127">The resource group name</span></span>

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

### <span data-ttu-id="dd14c-128">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="dd14c-128">-ServerName</span></span>
<span data-ttu-id="dd14c-129">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="dd14c-129">The server name</span></span>

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

### <span data-ttu-id="dd14c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd14c-130">-Confirm</span></span>
<span data-ttu-id="dd14c-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dd14c-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd14c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd14c-132">-WhatIf</span></span>
<span data-ttu-id="dd14c-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dd14c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd14c-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dd14c-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd14c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd14c-135">CommonParameters</span></span>
<span data-ttu-id="dd14c-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dd14c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd14c-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd14c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd14c-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dd14c-138">INPUTS</span></span>

### <span data-ttu-id="dd14c-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="dd14c-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="dd14c-140">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="dd14c-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="dd14c-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd14c-141">OUTPUTS</span></span>

### <span data-ttu-id="dd14c-142">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="dd14c-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="dd14c-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="dd14c-143">NOTES</span></span>

## <span data-ttu-id="dd14c-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd14c-144">RELATED LINKS</span></span>
