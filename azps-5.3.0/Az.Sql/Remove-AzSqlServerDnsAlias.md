---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
ms.openlocfilehash: d611f0bc14d657f47881cbdfbb1326111873114a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504783"
---
# <span data-ttu-id="31a83-101">Remove-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="31a83-101">Remove-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="31a83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31a83-102">SYNOPSIS</span></span>
<span data-ttu-id="31a83-103">Удаляет псевдоним DNS для Azure SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="31a83-103">Removes Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="31a83-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="31a83-104">SYNTAX</span></span>

### <span data-ttu-id="31a83-105">Удаление псевдонима DNS сервера из параметров ввода для cmdlet</span><span class="sxs-lookup"><span data-stu-id="31a83-105">Remove a Server Dns Alias from cmdlet input parameters</span></span>
```
Remove-AzSqlServerDnsAlias -Name <String> -ServerName <String> [-ResourceGroupName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31a83-106">Удаление псевдонима DNS сервера из определения экземпляра AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="31a83-106">Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition</span></span>
```
Remove-AzSqlServerDnsAlias -InputObject <AzureSqlServerDnsAliasModel> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31a83-107">Удаление псевдонима DNS сервера из ид ресурса Azure</span><span class="sxs-lookup"><span data-stu-id="31a83-107">Remove a Server Dns Alias from an Azure resource id</span></span>
```
Remove-AzSqlServerDnsAlias -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31a83-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31a83-108">DESCRIPTION</span></span>
<span data-ttu-id="31a83-109">Эти команды удаляют псевдоним azure SQL Server DNS с сервера, не удаляя сервер.</span><span class="sxs-lookup"><span data-stu-id="31a83-109">This commands remove Azure SQL Server DNS Alias from the server leaving server intact.</span></span>

## <span data-ttu-id="31a83-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="31a83-110">EXAMPLES</span></span>

### <span data-ttu-id="31a83-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="31a83-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlServerDnsAlias -DnsAliasName aliasName -ServerName serverName -ResourceGroupName rg
```

<span data-ttu-id="31a83-112">Удаляет псевдоним DNS azure SQL Server с именем сервера с именем сервера.</span><span class="sxs-lookup"><span data-stu-id="31a83-112">Removes Azure SQL Server DNS Alias with the name aliasName from the server with the name serverName</span></span>

## <span data-ttu-id="31a83-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31a83-113">PARAMETERS</span></span>

### <span data-ttu-id="31a83-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31a83-114">-AsJob</span></span>
<span data-ttu-id="31a83-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="31a83-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31a83-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31a83-116">-DefaultProfile</span></span>
<span data-ttu-id="31a83-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="31a83-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31a83-118">-Force</span><span class="sxs-lookup"><span data-stu-id="31a83-118">-Force</span></span>
<span data-ttu-id="31a83-119">Пропустить сообщение с подтверждением выполнения действия</span><span class="sxs-lookup"><span data-stu-id="31a83-119">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31a83-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31a83-120">-InputObject</span></span>
<span data-ttu-id="31a83-121">Объект DNS Alias сервера, который нужно удалить</span><span class="sxs-lookup"><span data-stu-id="31a83-121">The Server Dns Alias object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel
Parameter Sets: Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31a83-122">-Name</span><span class="sxs-lookup"><span data-stu-id="31a83-122">-Name</span></span>
<span data-ttu-id="31a83-123">Azure Sql Server Dns Alias name</span><span class="sxs-lookup"><span data-stu-id="31a83-123">Azure Sql Server Dns Alias name</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31a83-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31a83-124">-ResourceGroupName</span></span>
<span data-ttu-id="31a83-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="31a83-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31a83-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31a83-126">-ResourceId</span></span>
<span data-ttu-id="31a83-127">ИД ресурса объекта Dns Alias сервера, который нужно удалить</span><span class="sxs-lookup"><span data-stu-id="31a83-127">The resource id of Server Dns Alias object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from an Azure resource id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31a83-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="31a83-128">-ServerName</span></span>
<span data-ttu-id="31a83-129">Имя Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="31a83-129">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31a83-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31a83-130">-Confirm</span></span>
<span data-ttu-id="31a83-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="31a83-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31a83-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31a83-132">-WhatIf</span></span>
<span data-ttu-id="31a83-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31a83-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31a83-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="31a83-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31a83-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31a83-135">CommonParameters</span></span>
<span data-ttu-id="31a83-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31a83-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31a83-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31a83-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31a83-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="31a83-138">INPUTS</span></span>

### <span data-ttu-id="31a83-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="31a83-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

### <span data-ttu-id="31a83-140">System.String</span><span class="sxs-lookup"><span data-stu-id="31a83-140">System.String</span></span>

## <span data-ttu-id="31a83-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="31a83-141">OUTPUTS</span></span>

### <span data-ttu-id="31a83-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="31a83-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="31a83-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="31a83-143">NOTES</span></span>

## <span data-ttu-id="31a83-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31a83-144">RELATED LINKS</span></span>
