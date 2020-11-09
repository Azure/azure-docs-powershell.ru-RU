---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
ms.openlocfilehash: 87ac0ddaa205c2b257a3aadf9ceea5a6ec302eab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315968"
---
# <span data-ttu-id="9c399-101">Set-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="9c399-101">Set-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="9c399-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9c399-102">SYNOPSIS</span></span>
<span data-ttu-id="9c399-103">Обновление учетных данных задания</span><span class="sxs-lookup"><span data-stu-id="9c399-103">Updates a job credential</span></span>

## <span data-ttu-id="9c399-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9c399-104">SYNTAX</span></span>

### <span data-ttu-id="9c399-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9c399-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c399-106">Объект</span><span class="sxs-lookup"><span data-stu-id="9c399-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c399-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9c399-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceId] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c399-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c399-108">DESCRIPTION</span></span>
<span data-ttu-id="9c399-109">Командлет Set-AzSqlElasticJobCredential обновляет учетные данные задания</span><span class="sxs-lookup"><span data-stu-id="9c399-109">The Set-AzSqlElasticJobCredential cmdlet updates a job credential</span></span>

## <span data-ttu-id="9c399-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9c399-110">EXAMPLES</span></span>

### <span data-ttu-id="9c399-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9c399-111">Example 1</span></span>
```
PS C:\> $cred = Get-AzSqlElasticJobCredential -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name cred1
$cred | Set-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="9c399-112">Обновление учетных данных задания</span><span class="sxs-lookup"><span data-stu-id="9c399-112">Updates a job credential</span></span>

## <span data-ttu-id="9c399-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9c399-113">PARAMETERS</span></span>

### <span data-ttu-id="9c399-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="9c399-114">-AgentName</span></span>
<span data-ttu-id="9c399-115">Имя агента</span><span class="sxs-lookup"><span data-stu-id="9c399-115">The agent name</span></span>

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

### <span data-ttu-id="9c399-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="9c399-116">-Credential</span></span>
<span data-ttu-id="9c399-117">Учетные данные</span><span class="sxs-lookup"><span data-stu-id="9c399-117">The credential</span></span>

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

### <span data-ttu-id="9c399-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c399-118">-DefaultProfile</span></span>
<span data-ttu-id="9c399-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9c399-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c399-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c399-120">-InputObject</span></span>
<span data-ttu-id="9c399-121">Объект учетных данных задания</span><span class="sxs-lookup"><span data-stu-id="9c399-121">The job credential object</span></span>

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

### <span data-ttu-id="9c399-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9c399-122">-Name</span></span>
<span data-ttu-id="9c399-123">Имя учетных данных задания</span><span class="sxs-lookup"><span data-stu-id="9c399-123">The job credential name</span></span>

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

### <span data-ttu-id="9c399-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c399-124">-ResourceGroupName</span></span>
<span data-ttu-id="9c399-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="9c399-125">The resource group name</span></span>

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

### <span data-ttu-id="9c399-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c399-126">-ResourceId</span></span>
<span data-ttu-id="9c399-127">Идентификатор ресурса для учетных данных задания</span><span class="sxs-lookup"><span data-stu-id="9c399-127">The job credential resource id</span></span>

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

### <span data-ttu-id="9c399-128">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="9c399-128">-ServerName</span></span>
<span data-ttu-id="9c399-129">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="9c399-129">The server name</span></span>

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

### <span data-ttu-id="9c399-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c399-130">-Confirm</span></span>
<span data-ttu-id="9c399-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9c399-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c399-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c399-132">-WhatIf</span></span>
<span data-ttu-id="9c399-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9c399-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c399-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9c399-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c399-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c399-135">CommonParameters</span></span>
<span data-ttu-id="9c399-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9c399-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c399-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c399-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c399-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9c399-138">INPUTS</span></span>

### <span data-ttu-id="9c399-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="9c399-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="9c399-140">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="9c399-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="9c399-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c399-141">OUTPUTS</span></span>

### <span data-ttu-id="9c399-142">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="9c399-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="9c399-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="9c399-143">NOTES</span></span>

## <span data-ttu-id="9c399-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c399-144">RELATED LINKS</span></span>
