---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
ms.openlocfilehash: 49a175606526979acb4c44ddc4cb23ca7bbc33ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978083"
---
# <span data-ttu-id="8aaea-101">Get-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="8aaea-101">Get-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="8aaea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8aaea-102">SYNOPSIS</span></span>
<span data-ttu-id="8aaea-103">Получает или перечисляет псевдоним DNS Azure SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="8aaea-103">Gets or lists Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="8aaea-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8aaea-104">SYNTAX</span></span>

```
Get-AzSqlServerDnsAlias [-Name <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8aaea-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8aaea-105">DESCRIPTION</span></span>
<span data-ttu-id="8aaea-106">Получить определенный псевдоним DNS для Azure SQL Server или перечислить все псевдонимы DNS-сервера для сервера</span><span class="sxs-lookup"><span data-stu-id="8aaea-106">Get the specific Azure SQL Server DNS Alias or lists all Server DNS Aliases for the server</span></span>

## <span data-ttu-id="8aaea-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8aaea-107">EXAMPLES</span></span>

### <span data-ttu-id="8aaea-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8aaea-108">Example 1</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="8aaea-109">Список всех псевдонимов DNS сервера для определенного сервера</span><span class="sxs-lookup"><span data-stu-id="8aaea-109">Lists all Server DNS Aliases for the specific server</span></span>

### <span data-ttu-id="8aaea-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8aaea-110">Example 2</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -DnsAliasName dnsaliasname -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="8aaea-111">Gets Server DNS Alias specified by server and alias name</span><span class="sxs-lookup"><span data-stu-id="8aaea-111">Gets Server DNS Alias specified by server and alias name</span></span>

### <span data-ttu-id="8aaea-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="8aaea-112">Example 3</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname -DnsAliasName "dnsaliasname*"

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="8aaea-113">Список всех псевдонимов DNS сервера для определенного сервера, который начинается с "dnsaliasname".</span><span class="sxs-lookup"><span data-stu-id="8aaea-113">Lists all Server DNS Aliases for the specific server that start with "dnsaliasname".</span></span>

## <span data-ttu-id="8aaea-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8aaea-114">PARAMETERS</span></span>

### <span data-ttu-id="8aaea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aaea-115">-DefaultProfile</span></span>
<span data-ttu-id="8aaea-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8aaea-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8aaea-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8aaea-117">-Name</span></span>
<span data-ttu-id="8aaea-118">Имя псевдонима DNS для Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="8aaea-118">The Azure Sql Server DNS Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aaea-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8aaea-119">-ResourceGroupName</span></span>
<span data-ttu-id="8aaea-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8aaea-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="8aaea-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8aaea-121">-ServerName</span></span>
<span data-ttu-id="8aaea-122">Имя Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="8aaea-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="8aaea-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8aaea-123">-Confirm</span></span>
<span data-ttu-id="8aaea-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8aaea-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8aaea-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8aaea-125">-WhatIf</span></span>
<span data-ttu-id="8aaea-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8aaea-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8aaea-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8aaea-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8aaea-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aaea-128">CommonParameters</span></span>
<span data-ttu-id="8aaea-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8aaea-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aaea-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8aaea-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aaea-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8aaea-131">INPUTS</span></span>

### <span data-ttu-id="8aaea-132">System.String</span><span class="sxs-lookup"><span data-stu-id="8aaea-132">System.String</span></span>

## <span data-ttu-id="8aaea-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8aaea-133">OUTPUTS</span></span>

### <span data-ttu-id="8aaea-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="8aaea-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="8aaea-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8aaea-135">NOTES</span></span>

## <span data-ttu-id="8aaea-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8aaea-136">RELATED LINKS</span></span>
