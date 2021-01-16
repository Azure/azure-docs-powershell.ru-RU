---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
ms.openlocfilehash: 404b34c7e0d169e1d123a5c1ded8e6b5bef2fe2e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414884"
---
# <span data-ttu-id="6ffae-101">New-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="6ffae-101">New-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="6ffae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ffae-102">SYNOPSIS</span></span>
<span data-ttu-id="6ffae-103">Создание учетных данных задания</span><span class="sxs-lookup"><span data-stu-id="6ffae-103">Creates a new job credential</span></span>

## <span data-ttu-id="6ffae-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6ffae-104">SYNTAX</span></span>

### <span data-ttu-id="6ffae-105">DefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6ffae-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ffae-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="6ffae-106">ObjectSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ffae-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6ffae-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ffae-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ffae-108">DESCRIPTION</span></span>
<span data-ttu-id="6ffae-109">Новый New-AzSqlElasticJobCredential создает учетные данные задания.</span><span class="sxs-lookup"><span data-stu-id="6ffae-109">The New-AzSqlElasticJobCredential cmdlet creates a new job credential</span></span>

## <span data-ttu-id="6ffae-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6ffae-110">EXAMPLES</span></span>

### <span data-ttu-id="6ffae-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6ffae-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="6ffae-112">Создание учетных данных задания</span><span class="sxs-lookup"><span data-stu-id="6ffae-112">Creates a new job credential</span></span>

## <span data-ttu-id="6ffae-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ffae-113">PARAMETERS</span></span>

### <span data-ttu-id="6ffae-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="6ffae-114">-AgentName</span></span>
<span data-ttu-id="6ffae-115">Имя агента</span><span class="sxs-lookup"><span data-stu-id="6ffae-115">The agent name</span></span>

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

### <span data-ttu-id="6ffae-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="6ffae-116">-Credential</span></span>
<span data-ttu-id="6ffae-117">Учетные данные</span><span class="sxs-lookup"><span data-stu-id="6ffae-117">The credential</span></span>

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

### <span data-ttu-id="6ffae-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ffae-118">-DefaultProfile</span></span>
<span data-ttu-id="6ffae-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6ffae-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ffae-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6ffae-120">-Name</span></span>
<span data-ttu-id="6ffae-121">Имя учетных данных задания</span><span class="sxs-lookup"><span data-stu-id="6ffae-121">The job credential name</span></span>

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

### <span data-ttu-id="6ffae-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6ffae-122">-ParentObject</span></span>
<span data-ttu-id="6ffae-123">Объект агента</span><span class="sxs-lookup"><span data-stu-id="6ffae-123">The agent object</span></span>

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

### <span data-ttu-id="6ffae-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6ffae-124">-ParentResourceId</span></span>
<span data-ttu-id="6ffae-125">ИД агента ресурса</span><span class="sxs-lookup"><span data-stu-id="6ffae-125">The agent resource id</span></span>

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

### <span data-ttu-id="6ffae-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ffae-126">-ResourceGroupName</span></span>
<span data-ttu-id="6ffae-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6ffae-127">The resource group name</span></span>

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

### <span data-ttu-id="6ffae-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6ffae-128">-ServerName</span></span>
<span data-ttu-id="6ffae-129">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="6ffae-129">The server name</span></span>

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

### <span data-ttu-id="6ffae-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ffae-130">-Confirm</span></span>
<span data-ttu-id="6ffae-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6ffae-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ffae-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ffae-132">-WhatIf</span></span>
<span data-ttu-id="6ffae-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ffae-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ffae-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6ffae-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ffae-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ffae-135">CommonParameters</span></span>
<span data-ttu-id="6ffae-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ffae-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ffae-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ffae-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ffae-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6ffae-138">INPUTS</span></span>

### <span data-ttu-id="6ffae-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="6ffae-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="6ffae-140">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="6ffae-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="6ffae-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6ffae-141">OUTPUTS</span></span>

### <span data-ttu-id="6ffae-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="6ffae-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="6ffae-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6ffae-143">NOTES</span></span>

## <span data-ttu-id="6ffae-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6ffae-144">RELATED LINKS</span></span>