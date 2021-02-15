---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
ms.openlocfilehash: 66f8c3acc178a922868177200e6d4f1f8f50931f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210921"
---
# <span data-ttu-id="b443b-101">New-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="b443b-101">New-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="b443b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b443b-102">SYNOPSIS</span></span>
<span data-ttu-id="b443b-103">Эта команда создает новый псевдоним DNS для Azure SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="b443b-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="b443b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b443b-104">SYNTAX</span></span>

```
New-AzSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b443b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b443b-105">DESCRIPTION</span></span>
<span data-ttu-id="b443b-106">Создает новый псевдоним DNS для Azure SQL Server, который указывает на указанный сервер.</span><span class="sxs-lookup"><span data-stu-id="b443b-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="b443b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b443b-107">EXAMPLES</span></span>

### <span data-ttu-id="b443b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b443b-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="b443b-109">Эта команда создает псевдоним DNS Azure SQL Server с именем, которое назовет имя сервера</span><span class="sxs-lookup"><span data-stu-id="b443b-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="b443b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b443b-110">PARAMETERS</span></span>

### <span data-ttu-id="b443b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b443b-111">-AsJob</span></span>
<span data-ttu-id="b443b-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b443b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b443b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b443b-113">-DefaultProfile</span></span>
<span data-ttu-id="b443b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b443b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b443b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b443b-115">-Name</span></span>
<span data-ttu-id="b443b-116">Имя псевдонима Dns для Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="b443b-116">The Azure Sql Server Dns Alias name.</span></span>

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

### <span data-ttu-id="b443b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b443b-117">-ResourceGroupName</span></span>
<span data-ttu-id="b443b-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b443b-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="b443b-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b443b-119">-ServerName</span></span>
<span data-ttu-id="b443b-120">Имя Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="b443b-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="b443b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b443b-121">-Confirm</span></span>
<span data-ttu-id="b443b-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b443b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b443b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b443b-123">-WhatIf</span></span>
<span data-ttu-id="b443b-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b443b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b443b-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b443b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b443b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b443b-126">CommonParameters</span></span>
<span data-ttu-id="b443b-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b443b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b443b-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b443b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b443b-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b443b-129">INPUTS</span></span>

### <span data-ttu-id="b443b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b443b-130">System.String</span></span>

## <span data-ttu-id="b443b-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b443b-131">OUTPUTS</span></span>

### <span data-ttu-id="b443b-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="b443b-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="b443b-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b443b-133">NOTES</span></span>

## <span data-ttu-id="b443b-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b443b-134">RELATED LINKS</span></span>
