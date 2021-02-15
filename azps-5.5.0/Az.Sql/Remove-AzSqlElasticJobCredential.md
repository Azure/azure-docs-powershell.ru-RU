---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
ms.openlocfilehash: e9d684be7119ccc0ed991f825d8c7c372e7fdc6e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210897"
---
# <span data-ttu-id="aaaa6-101">Remove-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="aaaa6-101">Remove-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="aaaa6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aaaa6-102">SYNOPSIS</span></span>
<span data-ttu-id="aaaa6-103">Удаляет эластичные учетные данные задания.</span><span class="sxs-lookup"><span data-stu-id="aaaa6-103">Removes the elastic job credential</span></span>

## <span data-ttu-id="aaaa6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="aaaa6-104">SYNTAX</span></span>

### <span data-ttu-id="aaaa6-105">DefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aaaa6-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aaaa6-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="aaaa6-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aaaa6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="aaaa6-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aaaa6-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aaaa6-108">DESCRIPTION</span></span>
<span data-ttu-id="aaaa6-109">Новый Remove-AzSqlElasticJobCredential удаляет учетные данные задания</span><span class="sxs-lookup"><span data-stu-id="aaaa6-109">The Remove-AzSqlElasticJobCredential cmdlet removes a job credential</span></span>

## <span data-ttu-id="aaaa6-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="aaaa6-110">EXAMPLES</span></span>

### <span data-ttu-id="aaaa6-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="aaaa6-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="aaaa6-112">Удаление учетных данных задания</span><span class="sxs-lookup"><span data-stu-id="aaaa6-112">Removes a job credential</span></span>

## <span data-ttu-id="aaaa6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aaaa6-113">PARAMETERS</span></span>

### <span data-ttu-id="aaaa6-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="aaaa6-114">-AgentName</span></span>
<span data-ttu-id="aaaa6-115">Имя агента</span><span class="sxs-lookup"><span data-stu-id="aaaa6-115">The agent name</span></span>

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

### <span data-ttu-id="aaaa6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaaa6-116">-DefaultProfile</span></span>
<span data-ttu-id="aaaa6-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aaaa6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aaaa6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aaaa6-118">-InputObject</span></span>
<span data-ttu-id="aaaa6-119">Объект учетных данных задания</span><span class="sxs-lookup"><span data-stu-id="aaaa6-119">The job credential object</span></span>

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

### <span data-ttu-id="aaaa6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="aaaa6-120">-Name</span></span>
<span data-ttu-id="aaaa6-121">Имя учетных данных задания</span><span class="sxs-lookup"><span data-stu-id="aaaa6-121">The job credential name</span></span>

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

### <span data-ttu-id="aaaa6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaaa6-122">-ResourceGroupName</span></span>
<span data-ttu-id="aaaa6-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="aaaa6-123">The resource group name</span></span>

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

### <span data-ttu-id="aaaa6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aaaa6-124">-ResourceId</span></span>
<span data-ttu-id="aaaa6-125">ИД ресурса учетных данных задания</span><span class="sxs-lookup"><span data-stu-id="aaaa6-125">The job credential resource id</span></span>

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

### <span data-ttu-id="aaaa6-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="aaaa6-126">-ServerName</span></span>
<span data-ttu-id="aaaa6-127">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="aaaa6-127">The server name</span></span>

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

### <span data-ttu-id="aaaa6-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aaaa6-128">-Confirm</span></span>
<span data-ttu-id="aaaa6-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aaaa6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaaa6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaaa6-130">-WhatIf</span></span>
<span data-ttu-id="aaaa6-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aaaa6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aaaa6-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="aaaa6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaaa6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaaa6-133">CommonParameters</span></span>
<span data-ttu-id="aaaa6-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaaa6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaaa6-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aaaa6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaaa6-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aaaa6-136">INPUTS</span></span>

### <span data-ttu-id="aaaa6-137">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="aaaa6-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="aaaa6-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="aaaa6-138">OUTPUTS</span></span>

### <span data-ttu-id="aaaa6-139">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="aaaa6-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="aaaa6-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="aaaa6-140">NOTES</span></span>

## <span data-ttu-id="aaaa6-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aaaa6-141">RELATED LINKS</span></span>
