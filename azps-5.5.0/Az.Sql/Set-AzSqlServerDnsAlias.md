---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
ms.openlocfilehash: 791658e9f4f10fdbb8b1000d6b1bc88d392aaf46
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100222025"
---
# <span data-ttu-id="6cc8a-101">Set-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="6cc8a-101">Set-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="6cc8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cc8a-102">SYNOPSIS</span></span>
<span data-ttu-id="6cc8a-103">Изменяет сервер, на который SQL Server ALIAs DNS Azure</span><span class="sxs-lookup"><span data-stu-id="6cc8a-103">Modifies the server to which Azure SQL Server DNS Alias is pointing</span></span>

## <span data-ttu-id="6cc8a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6cc8a-104">SYNTAX</span></span>

```
Set-AzSqlServerDnsAlias -Name <String> -TargetServerName <String> [-ResourceGroupName] <String>
 -SourceServerName <String> -SourceServerResourceGroupName <String> -SourceServerSubscriptionId <Guid> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cc8a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6cc8a-105">DESCRIPTION</span></span>
<span data-ttu-id="6cc8a-106">Эта команда обновляет сервер, на который указывают псевдонимы.</span><span class="sxs-lookup"><span data-stu-id="6cc8a-106">This command is updating the server to which alias is pointing.</span></span> <span data-ttu-id="6cc8a-107">Эта команда должна быть выдана при входе в подписку на новом сервере, на который будет размещен псевдоним.</span><span class="sxs-lookup"><span data-stu-id="6cc8a-107">This command needs to be issued while logged into subscription where new server to which alias is going to point is located.</span></span>

## <span data-ttu-id="6cc8a-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6cc8a-108">EXAMPLES</span></span>

### <span data-ttu-id="6cc8a-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6cc8a-109">Example 1</span></span>
```
PS C:\> Set-AzSqlServerDnsAlias -ResourceGroupName rg -DnsAliasName aliasName -TargetServerName newServer -SourceServerName oldServer -SourceServerResourceGroupName SourceServerRG -SourceServerSubscriptionId 0000-0000-0000-0000
```

<span data-ttu-id="6cc8a-110">Эта команда обновляет псевдоним, который ранее навел на сервер oldServer таким образом, чтобы он навел указатель на сервер newServer.</span><span class="sxs-lookup"><span data-stu-id="6cc8a-110">This command is updating alias which was previously pointing to oldServer to point to server newServer</span></span>

## <span data-ttu-id="6cc8a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cc8a-111">PARAMETERS</span></span>

### <span data-ttu-id="6cc8a-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6cc8a-112">-AsJob</span></span>
<span data-ttu-id="6cc8a-113">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6cc8a-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6cc8a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cc8a-114">-DefaultProfile</span></span>
<span data-ttu-id="6cc8a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6cc8a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cc8a-116">-Name</span><span class="sxs-lookup"><span data-stu-id="6cc8a-116">-Name</span></span>
<span data-ttu-id="6cc8a-117">Имя псевдонима Dns для Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="6cc8a-117">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc8a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cc8a-118">-ResourceGroupName</span></span>
<span data-ttu-id="6cc8a-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6cc8a-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc8a-120">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="6cc8a-120">-SourceServerName</span></span>
<span data-ttu-id="6cc8a-121">Имя сервера Azure Sql Server, на который сейчас указывают псевдонимы.</span><span class="sxs-lookup"><span data-stu-id="6cc8a-121">The name of Azure Sql Server to which alias is currently pointing.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc8a-122">-SourceServerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cc8a-122">-SourceServerResourceGroupName</span></span>
<span data-ttu-id="6cc8a-123">Имя группы ресурсов на сервере-источнике.</span><span class="sxs-lookup"><span data-stu-id="6cc8a-123">The name of resource group of the source server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc8a-124">-SourceServerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6cc8a-124">-SourceServerSubscriptionId</span></span>
<span data-ttu-id="6cc8a-125">Код подписки на исходный сервер</span><span class="sxs-lookup"><span data-stu-id="6cc8a-125">The subscription id of the source server</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc8a-126">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="6cc8a-126">-TargetServerName</span></span>
<span data-ttu-id="6cc8a-127">Имя azure Sql Server, на который должен указывают псевдонимы.</span><span class="sxs-lookup"><span data-stu-id="6cc8a-127">The name of Azure Sql Server to which alias should point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc8a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6cc8a-128">-Confirm</span></span>
<span data-ttu-id="6cc8a-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6cc8a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cc8a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cc8a-130">-WhatIf</span></span>
<span data-ttu-id="6cc8a-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cc8a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cc8a-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6cc8a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cc8a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cc8a-133">CommonParameters</span></span>
<span data-ttu-id="6cc8a-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cc8a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cc8a-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6cc8a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cc8a-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6cc8a-136">INPUTS</span></span>

### <span data-ttu-id="6cc8a-137">System.String</span><span class="sxs-lookup"><span data-stu-id="6cc8a-137">System.String</span></span>

## <span data-ttu-id="6cc8a-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6cc8a-138">OUTPUTS</span></span>

### <span data-ttu-id="6cc8a-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="6cc8a-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="6cc8a-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6cc8a-140">NOTES</span></span>

## <span data-ttu-id="6cc8a-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6cc8a-141">RELATED LINKS</span></span>
