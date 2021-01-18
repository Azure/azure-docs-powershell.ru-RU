---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
ms.openlocfilehash: 87ac0ddaa205c2b257a3aadf9ceea5a6ec302eab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506471"
---
# <span data-ttu-id="ef0c6-101">Set-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="ef0c6-101">Set-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="ef0c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef0c6-102">SYNOPSIS</span></span>
<span data-ttu-id="ef0c6-103">Обновление учетных данных задания</span><span class="sxs-lookup"><span data-stu-id="ef0c6-103">Updates a job credential</span></span>

## <span data-ttu-id="ef0c6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ef0c6-104">SYNTAX</span></span>

### <span data-ttu-id="ef0c6-105">DefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ef0c6-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef0c6-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="ef0c6-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef0c6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ef0c6-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceId] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef0c6-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef0c6-108">DESCRIPTION</span></span>
<span data-ttu-id="ef0c6-109">Новый Set-AzSqlElasticJobCredential обновляет учетные данные задания</span><span class="sxs-lookup"><span data-stu-id="ef0c6-109">The Set-AzSqlElasticJobCredential cmdlet updates a job credential</span></span>

## <span data-ttu-id="ef0c6-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ef0c6-110">EXAMPLES</span></span>

### <span data-ttu-id="ef0c6-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ef0c6-111">Example 1</span></span>
```
PS C:\> $cred = Get-AzSqlElasticJobCredential -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name cred1
$cred | Set-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="ef0c6-112">Обновление учетных данных задания</span><span class="sxs-lookup"><span data-stu-id="ef0c6-112">Updates a job credential</span></span>

## <span data-ttu-id="ef0c6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef0c6-113">PARAMETERS</span></span>

### <span data-ttu-id="ef0c6-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="ef0c6-114">-AgentName</span></span>
<span data-ttu-id="ef0c6-115">Имя агента</span><span class="sxs-lookup"><span data-stu-id="ef0c6-115">The agent name</span></span>

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

### <span data-ttu-id="ef0c6-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="ef0c6-116">-Credential</span></span>
<span data-ttu-id="ef0c6-117">Учетные данные</span><span class="sxs-lookup"><span data-stu-id="ef0c6-117">The credential</span></span>

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

### <span data-ttu-id="ef0c6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef0c6-118">-DefaultProfile</span></span>
<span data-ttu-id="ef0c6-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ef0c6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef0c6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef0c6-120">-InputObject</span></span>
<span data-ttu-id="ef0c6-121">Объект учетных данных задания</span><span class="sxs-lookup"><span data-stu-id="ef0c6-121">The job credential object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef0c6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ef0c6-122">-Name</span></span>
<span data-ttu-id="ef0c6-123">Имя учетных данных задания</span><span class="sxs-lookup"><span data-stu-id="ef0c6-123">The job credential name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: CredentialName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef0c6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef0c6-124">-ResourceGroupName</span></span>
<span data-ttu-id="ef0c6-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ef0c6-125">The resource group name</span></span>

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

### <span data-ttu-id="ef0c6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef0c6-126">-ResourceId</span></span>
<span data-ttu-id="ef0c6-127">ИД ресурса учетных данных задания</span><span class="sxs-lookup"><span data-stu-id="ef0c6-127">The job credential resource id</span></span>

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

### <span data-ttu-id="ef0c6-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ef0c6-128">-ServerName</span></span>
<span data-ttu-id="ef0c6-129">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="ef0c6-129">The server name</span></span>

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

### <span data-ttu-id="ef0c6-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef0c6-130">-Confirm</span></span>
<span data-ttu-id="ef0c6-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef0c6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef0c6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef0c6-132">-WhatIf</span></span>
<span data-ttu-id="ef0c6-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef0c6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef0c6-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ef0c6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef0c6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef0c6-135">CommonParameters</span></span>
<span data-ttu-id="ef0c6-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef0c6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef0c6-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef0c6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef0c6-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef0c6-138">INPUTS</span></span>

### <span data-ttu-id="ef0c6-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="ef0c6-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="ef0c6-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="ef0c6-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="ef0c6-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ef0c6-141">OUTPUTS</span></span>

### <span data-ttu-id="ef0c6-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="ef0c6-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="ef0c6-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ef0c6-143">NOTES</span></span>

## <span data-ttu-id="ef0c6-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef0c6-144">RELATED LINKS</span></span>
