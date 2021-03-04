---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
ms.openlocfilehash: 46a3476d5ae4cead17eba0d03412ad2db57b01a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955208"
---
# <span data-ttu-id="d22b5-101">New-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="d22b5-101">New-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="d22b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d22b5-102">SYNOPSIS</span></span>
<span data-ttu-id="d22b5-103">Эта команда создает новый псевдоним DNS для Azure SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="d22b5-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="d22b5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d22b5-104">SYNTAX</span></span>

```
New-AzSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d22b5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d22b5-105">DESCRIPTION</span></span>
<span data-ttu-id="d22b5-106">Создает новый псевдоним DNS для Azure SQL Server, который указывает на указанный сервер.</span><span class="sxs-lookup"><span data-stu-id="d22b5-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="d22b5-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d22b5-107">EXAMPLES</span></span>

### <span data-ttu-id="d22b5-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d22b5-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="d22b5-109">Эта команда создает псевдоним DNS Azure SQL Server с именем, которое назовет имя сервера</span><span class="sxs-lookup"><span data-stu-id="d22b5-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="d22b5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d22b5-110">PARAMETERS</span></span>

### <span data-ttu-id="d22b5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d22b5-111">-AsJob</span></span>
<span data-ttu-id="d22b5-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d22b5-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d22b5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d22b5-113">-DefaultProfile</span></span>
<span data-ttu-id="d22b5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d22b5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d22b5-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d22b5-115">-Name</span></span>
<span data-ttu-id="d22b5-116">Имя псевдонима Dns для Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="d22b5-116">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22b5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d22b5-117">-ResourceGroupName</span></span>
<span data-ttu-id="d22b5-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d22b5-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d22b5-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d22b5-119">-ServerName</span></span>
<span data-ttu-id="d22b5-120">Имя Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="d22b5-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="d22b5-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d22b5-121">-Confirm</span></span>
<span data-ttu-id="d22b5-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d22b5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d22b5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d22b5-123">-WhatIf</span></span>
<span data-ttu-id="d22b5-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d22b5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d22b5-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d22b5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d22b5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d22b5-126">CommonParameters</span></span>
<span data-ttu-id="d22b5-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d22b5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d22b5-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d22b5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d22b5-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d22b5-129">INPUTS</span></span>

### <span data-ttu-id="d22b5-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d22b5-130">System.String</span></span>

## <span data-ttu-id="d22b5-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d22b5-131">OUTPUTS</span></span>

### <span data-ttu-id="d22b5-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="d22b5-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="d22b5-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d22b5-133">NOTES</span></span>

## <span data-ttu-id="d22b5-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d22b5-134">RELATED LINKS</span></span>
