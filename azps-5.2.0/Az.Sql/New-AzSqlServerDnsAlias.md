---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
ms.openlocfilehash: 66f8c3acc178a922868177200e6d4f1f8f50931f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417199"
---
# <span data-ttu-id="c722c-101">New-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="c722c-101">New-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="c722c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c722c-102">SYNOPSIS</span></span>
<span data-ttu-id="c722c-103">Эта команда создает новый псевдоним DNS для Azure SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="c722c-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="c722c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c722c-104">SYNTAX</span></span>

```
New-AzSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c722c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c722c-105">DESCRIPTION</span></span>
<span data-ttu-id="c722c-106">Создает новый псевдоним DNS для Azure SQL Server, который указывает на указанный сервер.</span><span class="sxs-lookup"><span data-stu-id="c722c-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="c722c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c722c-107">EXAMPLES</span></span>

### <span data-ttu-id="c722c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c722c-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="c722c-109">Эта команда создает псевдоним DNS Azure SQL Server с именем, которое назовет имя сервера</span><span class="sxs-lookup"><span data-stu-id="c722c-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="c722c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c722c-110">PARAMETERS</span></span>

### <span data-ttu-id="c722c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c722c-111">-AsJob</span></span>
<span data-ttu-id="c722c-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c722c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c722c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c722c-113">-DefaultProfile</span></span>
<span data-ttu-id="c722c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c722c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c722c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c722c-115">-Name</span></span>
<span data-ttu-id="c722c-116">Имя псевдонима Dns для Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="c722c-116">The Azure Sql Server Dns Alias name.</span></span>

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

### <span data-ttu-id="c722c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c722c-117">-ResourceGroupName</span></span>
<span data-ttu-id="c722c-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c722c-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="c722c-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c722c-119">-ServerName</span></span>
<span data-ttu-id="c722c-120">Имя Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="c722c-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="c722c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c722c-121">-Confirm</span></span>
<span data-ttu-id="c722c-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c722c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c722c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c722c-123">-WhatIf</span></span>
<span data-ttu-id="c722c-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c722c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c722c-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c722c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c722c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c722c-126">CommonParameters</span></span>
<span data-ttu-id="c722c-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c722c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c722c-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c722c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c722c-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c722c-129">INPUTS</span></span>

### <span data-ttu-id="c722c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c722c-130">System.String</span></span>

## <span data-ttu-id="c722c-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c722c-131">OUTPUTS</span></span>

### <span data-ttu-id="c722c-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="c722c-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="c722c-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c722c-133">NOTES</span></span>

## <span data-ttu-id="c722c-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c722c-134">RELATED LINKS</span></span>
