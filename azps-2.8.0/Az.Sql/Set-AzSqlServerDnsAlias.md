---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
ms.openlocfilehash: 7022f8655e1b87bc55ddd90cbd0aca512eeec0a1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905926"
---
# <span data-ttu-id="96e74-101">Set-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="96e74-101">Set-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="96e74-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="96e74-102">SYNOPSIS</span></span>
<span data-ttu-id="96e74-103">Изменяет сервер, на который указывает DNS-псевдоним Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="96e74-103">Modifies the server to which Azure SQL Server DNS Alias is pointing</span></span>

## <span data-ttu-id="96e74-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="96e74-104">SYNTAX</span></span>

```
Set-AzSqlServerDnsAlias -Name <String> -TargetServerName <String> [-ResourceGroupName] <String>
 -SourceServerName <String> -SourceServerResourceGroupName <String> -SourceServerSubscriptionId <Guid> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96e74-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96e74-105">DESCRIPTION</span></span>
<span data-ttu-id="96e74-106">Эта команда обновляет сервер, на который указывает псевдоним.</span><span class="sxs-lookup"><span data-stu-id="96e74-106">This command is updating the server to which alias is pointing.</span></span> <span data-ttu-id="96e74-107">Эта команда должна быть выполнена при входе в подписку, в которой находится новый сервер, на который будет указывать псевдоним.</span><span class="sxs-lookup"><span data-stu-id="96e74-107">This command needs to be issued while logged into subscription where new server to which alias is going to point is located.</span></span>

## <span data-ttu-id="96e74-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="96e74-108">EXAMPLES</span></span>

### <span data-ttu-id="96e74-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="96e74-109">Example 1</span></span>
```
PS C:\> Set-AzSqlServerDnsAlias -ResourceGroupName rg -DnsAliasName aliasName -TargetServerName newServer -SourceServerName oldServer -SourceServerResourceGroupName SourceServerRG -SourceServerSubscriptionId 0000-0000-0000-0000
```

<span data-ttu-id="96e74-110">Эта команда обновляет псевдоним, который ранее указывал на oldServer для указания на сервер newServer</span><span class="sxs-lookup"><span data-stu-id="96e74-110">This command is updating alias which was previously pointing to oldServer to point to server newServer</span></span>

## <span data-ttu-id="96e74-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="96e74-111">PARAMETERS</span></span>

### <span data-ttu-id="96e74-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96e74-112">-AsJob</span></span>
<span data-ttu-id="96e74-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="96e74-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="96e74-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96e74-114">-DefaultProfile</span></span>
<span data-ttu-id="96e74-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="96e74-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96e74-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="96e74-116">-Name</span></span>
<span data-ttu-id="96e74-117">Имя псевдонима DNS для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="96e74-117">The Azure Sql Server Dns Alias name.</span></span>

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

### <span data-ttu-id="96e74-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96e74-118">-ResourceGroupName</span></span>
<span data-ttu-id="96e74-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="96e74-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="96e74-120">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="96e74-120">-SourceServerName</span></span>
<span data-ttu-id="96e74-121">Имя сервера Azure SQL Server, на который в данный момент указывает псевдоним.</span><span class="sxs-lookup"><span data-stu-id="96e74-121">The name of Azure Sql Server to which alias is currently pointing.</span></span>

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

### <span data-ttu-id="96e74-122">-SourceServerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96e74-122">-SourceServerResourceGroupName</span></span>
<span data-ttu-id="96e74-123">Имя группы ресурсов исходного сервера.</span><span class="sxs-lookup"><span data-stu-id="96e74-123">The name of resource group of the source server.</span></span>

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

### <span data-ttu-id="96e74-124">-SourceServerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="96e74-124">-SourceServerSubscriptionId</span></span>
<span data-ttu-id="96e74-125">Идентификатор подписки исходного сервера</span><span class="sxs-lookup"><span data-stu-id="96e74-125">The subscription id of the source server</span></span>

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

### <span data-ttu-id="96e74-126">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="96e74-126">-TargetServerName</span></span>
<span data-ttu-id="96e74-127">Имя сервера Azure SQL Server, на который должна указывать псевдоним.</span><span class="sxs-lookup"><span data-stu-id="96e74-127">The name of Azure Sql Server to which alias should point.</span></span>

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

### <span data-ttu-id="96e74-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96e74-128">-Confirm</span></span>
<span data-ttu-id="96e74-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="96e74-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96e74-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96e74-130">-WhatIf</span></span>
<span data-ttu-id="96e74-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="96e74-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96e74-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="96e74-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96e74-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96e74-133">CommonParameters</span></span>
<span data-ttu-id="96e74-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="96e74-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96e74-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96e74-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96e74-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="96e74-136">INPUTS</span></span>

### <span data-ttu-id="96e74-137">System. String</span><span class="sxs-lookup"><span data-stu-id="96e74-137">System.String</span></span>

## <span data-ttu-id="96e74-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="96e74-138">OUTPUTS</span></span>

### <span data-ttu-id="96e74-139">Microsoft. Azure. Commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="96e74-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="96e74-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="96e74-140">NOTES</span></span>

## <span data-ttu-id="96e74-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96e74-141">RELATED LINKS</span></span>
